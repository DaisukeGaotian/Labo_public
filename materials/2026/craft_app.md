# Craft-Application QUEST

**Author:** Daisuke Takada  

---

# Missionの目的

- まずは簡単なアプリケーションの開発をする事でスクリプトの書き方に慣れる

## まずはコピペしてみよう

1. 左上の `+` を押して、`shiny web app...` みたいなボタンを押す
2. 以下のスクリプトをコピペして、`Run` もしくは `Reload app` を押してみよう。

```r
library(shiny) 
ui <- fluidPage( 
  titlePanel("BMI計算ツール"), 
  sidebarLayout( 
    sidebarPanel( 
      h4("データ入力"), 
      numericInput("height", "身長 (cm):", value = 170.0, step = 0.1), 
      numericInput("weight", "体重 (kg):", value = 60.0, step = 0.1) 
    ), 
    mainPanel( 
      uiOutput("dynamic_result_box"), 
      hr() 
    ) 
  ) 
)

server <- function(input, output) { 
  output$dynamic_result_box <- renderUI({ 
    bmi <- input$weight / ((input$height / 100)^2) 
    ibw <- ((input$height / 100)^2) * 22 
    status <- cut( 
      bmi, 
      breaks = c(0, 18.5, 25, 30, 35, 40, Inf), 
      labels = c( 
        "低体重 (Underweight)", 
        "普通体重 (Normal)", 
        "肥満1度", 
        "肥満2度", 
        "肥満3度", 
        "肥満4度" 
      ) 
    ) 
    wellPanel( 
      h3("計算結果"), 
      tags$p(tags$strong("BMI: "), round(bmi, 2), style = "font-size: 18px;"), 
      tags$p(tags$strong("判定: "), status, style = "font-size: 18px; color: #d9534f;"), 
      tags$p(tags$strong("標準体重 (IBW): "), round(ibw, 1), " kg", style = "font-size: 18px;") 
    ) 
  }) 
} 

shinyApp(ui = ui, server = server) 
```

> [!IMPORTANT]
>`*20**_student`のリポジトリ(学生向けに補助資料あり)では解説付きが出ますが、自分の言葉で整理してください

---

# 課題

0. スクリプトの各行が何をしているのかを説明できるようにする（横のメモを解説できるよう）
1. なんでも変えてみて、何が変わるのか確認してください。例えば、色(`color: #d9534f`)を`#00BFFF`にするとか。
2. `selectInput("gender", "性別:", choices = c("男性" = "male", "女性" = "female")),`というスクリプトをUIのどこかに入れて、画面上で性別のデータを入力できるようにしてください。
3. 同様に、クレアチニン(`cre`)のデータをUI上で入力できるようにしてください。
4. `egfr <- .......`をどこかに入れて、eGFRの値を裏(server)で持てるようにしてください。
5. 計算結果の画面(UI)にeGFRも表示されるようにしてください(表現はお任せ)。
6. 参考文献に関する情報：`tags$ul(tags$li(tags$strong("eGFR (推算糸球体濾過量): "), "日本腎臓学会「日本人成人向けの推算式」（松尾ら, Am J Kidney Dis, 2009）。18歳以上の日本人が対象。")),`みたいな感じで画面に入れこんでみてください。
7. BMIと同様に、CKDステージに応じたeGFRのカットオフ値に従い、分類データとして裏で(server側で)作ってください。
8. CKDステージ何期か、を結果の画面に表示できるようにしてください。
9. エネルギー必要量・PNI (予後栄養指数)に関しても同様に組み込んでください。
10. 肝機能の評価に何が必要か調べて、何を基に計算しているか調べて、機能として埋め込んでください。

---

## 最終的には「栄養計算アプリ」とかも作れます

これらをデプロイすれば、ネット上で誰でもアクセスできるようになります。

こういったコマンドラインでの微調整が理解できるようになると、AIエージェントと簡単なアプリを作ることに応用できます。

---

> [!TIP]
> **MISSION DEBRIEFING**
> 
> 今回のQUESTのレベルでも、病院等のローカルな計算作業を自動化する事はできるようになるだろう。
> これから統計解析の勉強を頑張れば、図や表を作ったりとさまざまな複雑な事ができるようになってくる。
> その際に、もっと複雑な図を作ったり、解析結果を本人にすぐに返すようなアプリの機能をつける事も可能となるので、しっかりと復習をしておくように！
