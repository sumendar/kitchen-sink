@title["R Notebook"]
## The Kitchen Sink
##### <span style="font-family:Helvetica Neue; font-weight:bold">A <span style="color:#e49436">Git</span>Pitch Feature Tour</span>

---
@title[Title1]
This is an [R Markdown](http://rmarkdown.rstudio.com) Notebook. When you execute code within the notebook, the results appear beneath the code. 

Try executing this chunk by clicking the *Run* button within the chunk or by placing your cursor inside it and pressing *Ctrl+Shift+Enter*. 

---
@title[Title2]
```r
plot(cars)
```

![](ss_files/figure-html/unnamed-chunk-1-1.png)<!-- -->

---
@title[Title3]
Add a new chunk by clicking the *Insert Chunk* button on the toolbar or by pressing *Ctrl+Alt+I*.

When you save the notebook, an HTML file containing the code and output will be saved alongside it (click the *Preview* button or press *Ctrl+Shift+K* to preview the HTML file).

The preview shows you a rendered HTML copy of the contents of the editor. Consequently, unlike *Knit*, *Preview* does not run any R code chunks. Instead, the output of the chunk when it was last run in the editor is displayed.

---
@title[Title4]
```r
summary(mtcars)
```

```
##       mpg             cyl             disp             hp       
##  Min.   :10.40   Min.   :4.000   Min.   : 71.1   Min.   : 52.0  
##  1st Qu.:15.43   1st Qu.:4.000   1st Qu.:120.8   1st Qu.: 96.5  
##  Median :19.20   Median :6.000   Median :196.3   Median :123.0  
##  Mean   :20.09   Mean   :6.188   Mean   :230.7   Mean   :146.7  
##  3rd Qu.:22.80   3rd Qu.:8.000   3rd Qu.:326.0   3rd Qu.:180.0  
##  Max.   :33.90   Max.   :8.000   Max.   :472.0   Max.   :335.0  
##       drat             wt             qsec             vs        
##  Min.   :2.760   Min.   :1.513   Min.   :14.50   Min.   :0.0000  
##  1st Qu.:3.080   1st Qu.:2.581   1st Qu.:16.89   1st Qu.:0.0000  
##  Median :3.695   Median :3.325   Median :17.71   Median :0.0000  
##  Mean   :3.597   Mean   :3.217   Mean   :17.85   Mean   :0.4375  
##  3rd Qu.:3.920   3rd Qu.:3.610   3rd Qu.:18.90   3rd Qu.:1.0000  
##  Max.   :4.930   Max.   :5.424   Max.   :22.90   Max.   :1.0000  
##        am              gear            carb      
##  Min.   :0.0000   Min.   :3.000   Min.   :1.000  
##  1st Qu.:0.0000   1st Qu.:3.000   1st Qu.:2.000  
##  Median :0.0000   Median :4.000   Median :2.000  
##  Mean   :0.4062   Mean   :3.688   Mean   :2.812  
##  3rd Qu.:1.0000   3rd Qu.:4.000   3rd Qu.:4.000  
##  Max.   :1.0000   Max.   :5.000   Max.   :8.000
```
---
@title[Title5]
The preview shows you a rendered HTML copy of the contents of the editor. Consequently, unlike *Knit*, *Preview* does not run any R code chunks. Instead, the output of the chunk when it was last run in the editor is displayed.

---
@title[Title6]
```r
library(plotly)
```

```
## Loading required package: ggplot2
```

```
## 
## Attaching package: 'plotly'
```

```
## The following object is masked from 'package:ggplot2':
## 
##     last_plot
```

```
## The following object is masked from 'package:stats':
## 
##     filter
```

```
## The following object is masked from 'package:graphics':
## 
##     layout
```
---
@title[Title7]
```r
p <- plot_ly(y = ~rnorm(50), type = "box") %>%
  add_trace(y = ~rnorm(50, 1))

# Create a shareable link to your chart
# Set up API credentials: https://plot.ly/r/getting-started
p
```

<!--html_preserve--><div id="16948293b3" style="width:672px;height:480px;" class="plotly html-widget"></div>
<script type="application/json" data-for="16948293b3">{"x":{"visdat":{"169474ba5244":["function () ","plotlyVisDat"]},"cur_data":"169474ba5244","attrs":{"169474ba5244":{"y":{},"alpha":1,"sizes":[10,100],"type":"box"},"169474ba5244.1":{"y":{},"alpha":1,"sizes":[10,100],"type":"box"}},"layout":{"margin":{"b":40,"l":60,"t":25,"r":10},"yaxis":{"domain":[0,1],"title":"rnorm(50)"},"xaxis":{"domain":[0,1]},"hovermode":"closest","showlegend":true},"source":"A","config":{"modeBarButtonsToAdd":[{"name":"Collaborate","icon":{"width":1000,"ascent":500,"descent":-50,"path":"M487 375c7-10 9-23 5-36l-79-259c-3-12-11-23-22-31-11-8-22-12-35-12l-263 0c-15 0-29 5-43 15-13 10-23 23-28 37-5 13-5 25-1 37 0 0 0 3 1 7 1 5 1 8 1 11 0 2 0 4-1 6 0 3-1 5-1 6 1 2 2 4 3 6 1 2 2 4 4 6 2 3 4 5 5 7 5 7 9 16 13 26 4 10 7 19 9 26 0 2 0 5 0 9-1 4-1 6 0 8 0 2 2 5 4 8 3 3 5 5 5 7 4 6 8 15 12 26 4 11 7 19 7 26 1 1 0 4 0 9-1 4-1 7 0 8 1 2 3 5 6 8 4 4 6 6 6 7 4 5 8 13 13 24 4 11 7 20 7 28 1 1 0 4 0 7-1 3-1 6-1 7 0 2 1 4 3 6 1 1 3 4 5 6 2 3 3 5 5 6 1 2 3 5 4 9 2 3 3 7 5 10 1 3 2 6 4 10 2 4 4 7 6 9 2 3 4 5 7 7 3 2 7 3 11 3 3 0 8 0 13-1l0-1c7 2 12 2 14 2l218 0c14 0 25-5 32-16 8-10 10-23 6-37l-79-259c-7-22-13-37-20-43-7-7-19-10-37-10l-248 0c-5 0-9-2-11-5-2-3-2-7 0-12 4-13 18-20 41-20l264 0c5 0 10 2 16 5 5 3 8 6 10 11l85 282c2 5 2 10 2 17 7-3 13-7 17-13z m-304 0c-1-3-1-5 0-7 1-1 3-2 6-2l174 0c2 0 4 1 7 2 2 2 4 4 5 7l6 18c0 3 0 5-1 7-1 1-3 2-6 2l-173 0c-3 0-5-1-8-2-2-2-4-4-4-7z m-24-73c-1-3-1-5 0-7 2-2 3-2 6-2l174 0c2 0 5 0 7 2 3 2 4 4 5 7l6 18c1 2 0 5-1 6-1 2-3 3-5 3l-174 0c-3 0-5-1-7-3-3-1-4-4-5-6z"},"click":"function(gd) { \n        // is this being viewed in RStudio?\n        if (location.search == '?viewer_pane=1') {\n          alert('To learn about plotly for collaboration, visit:\\n https://cpsievert.github.io/plotly_book/plot-ly-for-collaboration.html');\n        } else {\n          window.open('https://cpsievert.github.io/plotly_book/plot-ly-for-collaboration.html', '_blank');\n        }\n      }"}],"cloud":false},"data":[{"y":[0.790324162113843,-0.61934285709051,-0.648232991814038,0.0179001948342495,1.42404415103018,-0.0863609707673116,0.65269064158795,1.74275047676012,-1.74374504568306,-0.281822641019249,-1.80252716465129,0.832522526259275,0.560511359843458,0.594549561981998,-0.783467733445876,0.354964548224137,1.19142820584551,0.03489182243914,-0.351003299053166,-2.1230918038508,-1.2497718458291,-1.93677545706978,-1.95188034668454,-1.20361705370745,-0.0739953225644678,-0.804748959250555,-0.828628795691817,-0.676827624337684,-0.640352846349252,1.27097680148883,-1.91241249889707,-1.81251843224161,-1.98081443857806,2.23910862252579,-1.63211449825168,0.191035555891405,-1.13732796434701,0.540240695909089,1.66433440808417,0.345035603806233,0.567312347714311,-0.59445012181596,0.260229742209618,0.954119525967178,-0.157305026322536,-1.13731181298738,0.133339993052818,-0.66774832685626,0.167203086428163,-0.771003959033167],"type":"box","line":{"fillcolor":"rgba(31,119,180,1)","color":"rgba(31,119,180,1)"},"xaxis":"x","yaxis":"y","frame":null},{"y":[2.07328387788874,0.968216917912981,0.803124541375328,1.64210035711648,0.909350048814651,0.544796747429193,0.857005400032128,-0.0767479827128577,2.75529208162095,-0.620909379245505,0.199797482103789,2.82539720864255,0.280887162023502,0.832943825510245,2.46981376067381,2.2776868578945,1.47563414490696,-0.0708423922572157,2.14572372692648,0.884518849084821,0.431492594176381,1.54008218594986,-0.171634280674563,1.18156094171135,2.24615386729203,0.679230509354025,1.92226572158644,0.992718168593589,0.696283652615769,0.559500351510037,-0.751803869663597,-1.9435973764459,2.65482261345514,1.06290961106876,1.88994414265307,1.47455861903843,0.536938813736978,0.599194154148622,0.692003983453388,0.864477146618113,0.584193514836586,1.24288709819709,0.471206450925897,1.84950486709927,-0.25799888005755,0.194648264628507,1.1606327089617,0.94592658729975,0.235489756636286,0.416464604617195],"type":"box","line":{"fillcolor":"rgba(255,127,14,1)","color":"rgba(255,127,14,1)"},"xaxis":"x","yaxis":"y","frame":null}],"highlight":{"on":"plotly_click","persistent":false,"dynamic":false,"selectize":false,"opacityDim":0.2,"selected":{"opacity":1}},"base_url":"https://plot.ly"},"evals":["config.modeBarButtonsToAdd.0.click"],"jsHooks":{"render":[{"code":"function(el, x) { var ctConfig = crosstalk.var('plotlyCrosstalkOpts').set({\"on\":\"plotly_click\",\"persistent\":false,\"dynamic\":false,\"selectize\":false,\"opacityDim\":0.2,\"selected\":{\"opacity\":1}}); }","data":null}]}}</script><!--/html_preserve-->
---
