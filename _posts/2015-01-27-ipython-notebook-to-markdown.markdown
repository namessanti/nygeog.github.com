---
layout: post
title: Using iPython Notebook with Pandas and exporting to Markdown
date:   2015-01-27 10:21:10
tags: ipython pandas markdown 
---

<!--##Using iPython Notebook for data analysis with Pandas
-->

In my [Exploratory Data Analysis and Visualization Course](http://nygeog.github.io/data/science/columbia/idse/2015/01/21/exploratory-data-analysis-and-visualization.html) we've been using [RStudio](http://www.rstudio.com/) for exploring and munging data. I'm used to doing this in Pandas and it sort of reminded me of [iPython Notebook](http://ipython.org/notebook.html). One of the great things about RStudio is the ability to create [Markdown](http://daringfireball.net/projects/markdown/) files that include your code and whatever text you'd like to include.  

So I looked into whether iPython notebook could export to Markdown and sure enough it does. Below is an example of exporting a **df.head** table. 

---

Below I'm importing **Pandas** as **pd**, then reading a project-file csv.

Next, I'm setting the display options to max columns of 5200 (5200 is arbitrary
number) as when you try to display a large dataframe sometimes it won't display
b/c it exceeds the defaut iPython Notebook settings.

Last, I used **df.head(15)** to show the first 15 records in the dataframe.




    import pandas as pd
    
    df = pd.read_csv('***/grid_sites.csv')
    
    pd.options.display.max_columns = 5200
    df.head(15)



###And now we can see this fantastically styled html table:

<div style="max-height:1000px;max-width:1500px;overflow:auto;">
<table border="1" class="dataframe">
  <thead>
    <tr style="text-align: right;">
      <th></th>
      <th>gid</th>
      <th>x</th>
      <th>y</th>
      <th>g_point_elev10ft</th>
      <th>g_pointwaternearangle</th>
      <th>g_pointwaternearfeet</th>
      <th>g_pointwaternearmeters</th>
      <th>gr0050morigsqmtrs</th>
      <th>gr0050mlandsqmtrs</th>
      <th>gr0100morigsqmtrs</th>
      <th>gr0100mlandsqmtrs</th>
      <th>gr0250morigsqmtrs</th>
      <th>gr0250mlandsqmtrs</th>
      <th>gr0500morigsqmtrs</th>
      <th>gr0500mlandsqmtrs</th>
      <th>gr1000morigsqmtrs</th>
      <th>gr1000mlandsqmtrs</th>
      <th>gr0050mtreecsqmtrs</th>
      <th>gr0100mtreecsqmtrs</th>
      <th>gr0250mtreecsqmtrs</th>
      <th>gr0500mtreecsqmtrs</th>
      <th>gr1000mtreecsqmtrs</th>
      <th>gr0050mtreecpctorig</th>
      <th>gr0050mtreecpctland</th>
      <th>gr0100mtreecpctorig</th>
      <th>gr0100mtreecpctland</th>
      <th>gr0250mtreecpctorig</th>
      <th>gr0250mtreecpctland</th>
      <th>gr0500mtreecpctorig</th>
      <th>gr0500mtreecpctland</th>
      <th>gr1000mtreecpctorig</th>
      <th>gr1000mtreecpctland</th>
      <th>gr0050melev10ftcount</th>
      <th>gr0050melev10ftmin</th>
      <th>gr0050melev10ftmax</th>
      <th>gr0050melev10ftmean</th>
      <th>gr0050melev10ftstd</th>
      <th>gr0100melev10ftcount</th>
      <th>gr0100melev10ftmin</th>
      <th>gr0100melev10ftmax</th>
      <th>gr0100melev10ftmean</th>
      <th>gr0100melev10ftstd</th>
      <th>gr0250melev10ftcount</th>
      <th>gr0250melev10ftmin</th>
      <th>gr0250melev10ftmax</th>
      <th>gr0250melev10ftmean</th>
      <th>gr0250melev10ftstd</th>
      <th>gr0500melev10ftcount</th>
      <th>gr0500melev10ftmin</th>
      <th>gr0500melev10ftmax</th>
      <th>gr0500melev10ftmean</th>
      <th>gr0500melev10ftstd</th>
      <th>gr1000melev10ftcount</th>
      <th>gr1000melev10ftmin</th>
      <th>gr1000melev10ftmax</th>
      <th>gr1000melev10ftmean</th>
      <th>gr1000melev10ftstd</th>
      <th>gr0050mbldgvol</th>
      <th>gr0100mbldgvol</th>
      <th>gr0250mbldgvol</th>
      <th>gr0500mbldgvol</th>
      <th>gr1000mbldgvol</th>
      <th>gr0050mbldgbulkorig</th>
      <th>gr0050mbldgbulkland</th>
      <th>gr0100mbldgbulkorig</th>
      <th>gr0100mbldgbulkland</th>
      <th>gr0250mbldgbulkorig</th>
      <th>gr0250mbldgbulkland</th>
      <th>gr0500mbldgbulkorig</th>
      <th>gr0500mbldgbulkland</th>
      <th>gr1000mbldgbulkorig</th>
      <th>gr1000mbldgbulkland</th>
      <th>trafesrigr0050mavg_20012012</th>
      <th>trafesrigr0100mavg_20012012</th>
      <th>trafesrigr0250mavg_20012012</th>
      <th>trafesrigr0500mavg_20012012</th>
      <th>trafesrigr1000mavg_20012012</th>
      <th>trafesrigr0050mavg_2001</th>
      <th>trafesrigr0050mavg_2002</th>
      <th>trafesrigr0050mavg_2003</th>
      <th>trafesrigr0050mavg_2004</th>
      <th>trafesrigr0050mavg_2005</th>
      <th>trafesrigr0050mavg_2006</th>
      <th>trafesrigr0050mavg_2007</th>
      <th>trafesrigr0050mavg_2008</th>
      <th>trafesrigr0050mavg_2009</th>
      <th>trafesrigr0050mavg_2010</th>
      <th>trafesrigr0100mavg_2001</th>
      <th>trafesrigr0100mavg_2002</th>
      <th>trafesrigr0100mavg_2003</th>
      <th>trafesrigr0100mavg_2004</th>
      <th>trafesrigr0100mavg_2005</th>
      <th>trafesrigr0100mavg_2006</th>
      <th>trafesrigr0100mavg_2007</th>
      <th>trafesrigr0100mavg_2008</th>
      <th>trafesrigr0100mavg_2009</th>
      <th>trafesrigr0100mavg_2010</th>
      <th>trafesrigr0100mavg_2011</th>
      <th>trafesrigr0250mavg_2001</th>
      <th>trafesrigr0250mavg_2002</th>
      <th>trafesrigr0250mavg_2003</th>
      <th>trafesrigr0250mavg_2004</th>
      <th>trafesrigr0250mavg_2005</th>
      <th>trafesrigr0250mavg_2006</th>
      <th>trafesrigr0250mavg_2007</th>
      <th>trafesrigr0250mavg_2008</th>
      <th>trafesrigr0250mavg_2009</th>
      <th>trafesrigr0250mavg_2010</th>
      <th>trafesrigr0250mavg_2011</th>
      <th>trafesrigr0500mavg_2001</th>
      <th>trafesrigr0500mavg_2002</th>
      <th>trafesrigr0500mavg_2003</th>
      <th>trafesrigr0500mavg_2004</th>
      <th>trafesrigr0500mavg_2005</th>
      <th>trafesrigr0500mavg_2006</th>
      <th>trafesrigr0500mavg_2007</th>
      <th>trafesrigr0500mavg_2008</th>
      <th>trafesrigr0500mavg_2009</th>
      <th>trafesrigr0500mavg_2010</th>
      <th>trafesrigr0500mavg_2011</th>
      <th>trafesrigr1000mavg_2001</th>
      <th>trafesrigr1000mavg_2002</th>
      <th>trafesrigr1000mavg_2003</th>
      <th>trafesrigr1000mavg_2004</th>
      <th>trafesrigr1000mavg_2005</th>
      <th>trafesrigr1000mavg_2006</th>
      <th>trafesrigr1000mavg_2007</th>
      <th>trafesrigr1000mavg_2008</th>
      <th>trafesrigr1000mavg_2009</th>
      <th>trafesrigr1000mavg_2010</th>
      <th>trafesrigr1000mavg_2011</th>
      <th>trafnysdgr0050mavg_2012</th>
      <th>trafnysdgr0100mavg_2012</th>
      <th>trafnysdgr0250mavg_2012</th>
      <th>trafnysdgr0500mavg_2012</th>
      <th>trafnysdgr1000mavg_2012</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>0 </th>
      <td> 100001</td>
      <td> 913307.305588</td>
      <td> 122566.653211</td>
      <td>-9999.000000</td>
      <td>   0.000000</td>
      <td>   0.000000</td>
      <td>   0.000000</td>
      <td> 7853.950214</td>
      <td>    0.000000</td>
      <td> 31415.800866</td>
      <td>     0.000000</td>
      <td> 196348.755435</td>
      <td>      0.000000</td>
      <td> 785395.021770</td>
      <td>      0.000000</td>
      <td> 3141580.087165</td>
      <td>       0.000000</td>
      <td> 0</td>
      <td>  3952.313778</td>
      <td> 48341.868204</td>
      <td> 141231.629924</td>
      <td> 451567.071377</td>
      <td> 0</td>
      <td> 0</td>
      <td> 0.125807</td>
      <td> 0.000000</td>
      <td> 0.246204</td>
      <td> 0.000000</td>
      <td> 0.179822</td>
      <td> 0.000000</td>
      <td> 0.143739</td>
      <td> 0.000000</td>
      <td>   0</td>
      <td>  0.00000</td>
      <td>  0.0000</td>
      <td>  0.0000</td>
      <td>  0.00000</td>
      <td>    0</td>
      <td>  0.000000</td>
      <td>  0.0000</td>
      <td>  0.0000</td>
      <td>  0.00000</td>
      <td>     0</td>
      <td> 0.000000</td>
      <td>  0.0000</td>
      <td>  0.0000</td>
      <td>  0.0000</td>
      <td>     0</td>
      <td> 0.000000</td>
      <td>  0.0000</td>
      <td>  0.0000</td>
      <td>  0.0000</td>
      <td>      0</td>
      <td> 0.000000</td>
      <td>  0.0000</td>
      <td>  0.0000</td>
      <td>  0.0000</td>
      <td>    0.000000</td>
      <td>  2619.499213</td>
      <td>   5729.645316</td>
      <td> 216666.220329</td>
      <td> 1245817.366172</td>
      <td> 0.000000</td>
      <td> 0.000000</td>
      <td> 0.083382</td>
      <td> 0.000000</td>
      <td> 0.029181</td>
      <td> 0.000000</td>
      <td> 0.275869</td>
      <td> 0.000000</td>
      <td> 0.396558</td>
      <td> 0.000000</td>
      <td> 0</td>
      <td> 0</td>
      <td> 0</td>
      <td>    0</td>
      <td>    0</td>
      <td> 0</td>
      <td> 0</td>
      <td> 0</td>
      <td> 0</td>
      <td> 0</td>
      <td> 0</td>
      <td> 0</td>
      <td> 0</td>
      <td> 0</td>
      <td> 0</td>
      <td> 0</td>
      <td> 0</td>
      <td> 0</td>
      <td> 0</td>
      <td> 0</td>
      <td> 0</td>
      <td> 0</td>
      <td> 0</td>
      <td> 0</td>
      <td> 0</td>
      <td> 0</td>
      <td> 0</td>
      <td> 0</td>
      <td> 0</td>
      <td> 0</td>
      <td> 0</td>
      <td> 0</td>
      <td> 0</td>
      <td> 0</td>
      <td> 0</td>
      <td> 0</td>
      <td> 0</td>
      <td> 0</td>
      <td> 0</td>
      <td> 0</td>
      <td> 0</td>
      <td> 0</td>
      <td> 0</td>
      <td> 0</td>
      <td> 0</td>
      <td> 0</td>
      <td>    0</td>
      <td> 0</td>
      <td> 0</td>
      <td> 0</td>
      <td> 0</td>
      <td> 0</td>
      <td> 0</td>
      <td> 0</td>
      <td> 0</td>
      <td> 0</td>
      <td> 0</td>
      <td>    0</td>
      <td> 0</td>
      <td> 0</td>
      <td>   0</td>
      <td>  292.0</td>
      <td> 5696.50</td>
      <td> 4057.00</td>
    </tr>
    <tr>
      <th>1 </th>
      <td> 100002</td>
      <td> 913307.305588</td>
      <td> 122894.737200</td>
      <td>    4.091254</td>
      <td>   0.000000</td>
      <td>   0.000000</td>
      <td>   0.000000</td>
      <td> 7853.950214</td>
      <td> 4002.041561</td>
      <td> 31415.800866</td>
      <td> 15455.731616</td>
      <td> 196348.755435</td>
      <td>  90498.329446</td>
      <td> 785395.021770</td>
      <td> 353746.383694</td>
      <td> 3141580.087165</td>
      <td> 1260083.346102</td>
      <td> 0</td>
      <td> 11093.497657</td>
      <td> 52914.680481</td>
      <td> 147391.944889</td>
      <td> 457270.916748</td>
      <td> 0</td>
      <td> 0</td>
      <td> 0.353118</td>
      <td> 0.717759</td>
      <td> 0.269493</td>
      <td> 0.584703</td>
      <td> 0.187666</td>
      <td> 0.416660</td>
      <td> 0.145554</td>
      <td> 0.362889</td>
      <td> 426</td>
      <td>  3.16432</td>
      <td> 11.9986</td>
      <td>  6.2407</td>
      <td>  1.26460</td>
      <td> 1663</td>
      <td>  2.982810</td>
      <td> 45.9997</td>
      <td> 15.5446</td>
      <td> 11.86370</td>
      <td>  9738</td>
      <td> 2.756890</td>
      <td> 70.9901</td>
      <td> 35.2858</td>
      <td> 18.8374</td>
      <td> 38074</td>
      <td> 1.999990</td>
      <td> 72.4902</td>
      <td> 38.7175</td>
      <td> 16.7106</td>
      <td> 135048</td>
      <td>-0.571724</td>
      <td> 80.4000</td>
      <td> 37.6836</td>
      <td> 18.9316</td>
      <td>    0.000000</td>
      <td>     0.000000</td>
      <td>  19214.061323</td>
      <td> 288823.918864</td>
      <td> 1369388.218735</td>
      <td> 0.000000</td>
      <td> 0.000000</td>
      <td> 0.000000</td>
      <td> 0.000000</td>
      <td> 0.097857</td>
      <td> 0.212314</td>
      <td> 0.367744</td>
      <td> 0.816472</td>
      <td> 0.435892</td>
      <td> 1.086744</td>
      <td> 0</td>
      <td> 0</td>
      <td> 0</td>
      <td>    0</td>
      <td>    0</td>
      <td> 0</td>
      <td> 0</td>
      <td> 0</td>
      <td> 0</td>
      <td> 0</td>
      <td> 0</td>
      <td> 0</td>
      <td> 0</td>
      <td> 0</td>
      <td> 0</td>
      <td> 0</td>
      <td> 0</td>
      <td> 0</td>
      <td> 0</td>
      <td> 0</td>
      <td> 0</td>
      <td> 0</td>
      <td> 0</td>
      <td> 0</td>
      <td> 0</td>
      <td> 0</td>
      <td> 0</td>
      <td> 0</td>
      <td> 0</td>
      <td> 0</td>
      <td> 0</td>
      <td> 0</td>
      <td> 0</td>
      <td> 0</td>
      <td> 0</td>
      <td> 0</td>
      <td> 0</td>
      <td> 0</td>
      <td> 0</td>
      <td> 0</td>
      <td> 0</td>
      <td> 0</td>
      <td> 0</td>
      <td> 0</td>
      <td> 0</td>
      <td> 0</td>
      <td>    0</td>
      <td> 0</td>
      <td> 0</td>
      <td> 0</td>
      <td> 0</td>
      <td> 0</td>
      <td> 0</td>
      <td> 0</td>
      <td> 0</td>
      <td> 0</td>
      <td> 0</td>
      <td>    0</td>
      <td> 0</td>
      <td> 0</td>
      <td>   0</td>
      <td>  292.0</td>
      <td> 6115.75</td>
      <td> 5783.57</td>
    </tr>
    <tr>
      <th>2 </th>
      <td> 100003</td>
      <td> 913307.305588</td>
      <td> 123222.821190</td>
      <td>    8.551375</td>
      <td> 179.351037</td>
      <td>  43.298329</td>
      <td>  13.197331</td>
      <td> 7853.950214</td>
      <td> 6015.726344</td>
      <td> 31415.800866</td>
      <td> 19405.331167</td>
      <td> 196348.755435</td>
      <td> 100369.997473</td>
      <td> 785395.021770</td>
      <td> 367448.179604</td>
      <td> 3141580.087165</td>
      <td> 1286631.025189</td>
      <td> 0</td>
      <td> 11937.307201</td>
      <td> 53841.962447</td>
      <td> 146602.206918</td>
      <td> 465608.381325</td>
      <td> 0</td>
      <td> 0</td>
      <td> 0.379978</td>
      <td> 0.615156</td>
      <td> 0.274216</td>
      <td> 0.536435</td>
      <td> 0.186660</td>
      <td> 0.398974</td>
      <td> 0.148208</td>
      <td> 0.361882</td>
      <td> 650</td>
      <td>  2.96409</td>
      <td> 29.9936</td>
      <td> 10.3767</td>
      <td>  5.06838</td>
      <td> 2090</td>
      <td>  2.887080</td>
      <td> 60.9857</td>
      <td> 21.9326</td>
      <td> 16.67590</td>
      <td> 10810</td>
      <td> 2.000700</td>
      <td> 72.4902</td>
      <td> 42.3306</td>
      <td> 21.3647</td>
      <td> 39543</td>
      <td> 0.000003</td>
      <td> 72.4902</td>
      <td> 40.5070</td>
      <td> 16.1305</td>
      <td> 137879</td>
      <td>-0.571724</td>
      <td> 81.3846</td>
      <td> 39.4516</td>
      <td> 18.8936</td>
      <td>    0.000000</td>
      <td>  1612.288123</td>
      <td>  45018.070029</td>
      <td> 338849.649981</td>
      <td> 1439584.329659</td>
      <td> 0.000000</td>
      <td> 0.000000</td>
      <td> 0.051321</td>
      <td> 0.083085</td>
      <td> 0.229276</td>
      <td> 0.448521</td>
      <td> 0.431438</td>
      <td> 0.922170</td>
      <td> 0.458236</td>
      <td> 1.118879</td>
      <td> 0</td>
      <td> 0</td>
      <td> 0</td>
      <td>    0</td>
      <td> 5921</td>
      <td> 0</td>
      <td> 0</td>
      <td> 0</td>
      <td> 0</td>
      <td> 0</td>
      <td> 0</td>
      <td> 0</td>
      <td> 0</td>
      <td> 0</td>
      <td> 0</td>
      <td> 0</td>
      <td> 0</td>
      <td> 0</td>
      <td> 0</td>
      <td> 0</td>
      <td> 0</td>
      <td> 0</td>
      <td> 0</td>
      <td> 0</td>
      <td> 0</td>
      <td> 0</td>
      <td> 0</td>
      <td> 0</td>
      <td> 0</td>
      <td> 0</td>
      <td> 0</td>
      <td> 0</td>
      <td> 0</td>
      <td> 0</td>
      <td> 0</td>
      <td> 0</td>
      <td> 0</td>
      <td> 0</td>
      <td> 0</td>
      <td> 0</td>
      <td> 0</td>
      <td> 0</td>
      <td> 0</td>
      <td> 0</td>
      <td> 0</td>
      <td> 0</td>
      <td>    0</td>
      <td> 0</td>
      <td> 0</td>
      <td> 0</td>
      <td> 0</td>
      <td> 0</td>
      <td> 0</td>
      <td> 0</td>
      <td> 0</td>
      <td> 0</td>
      <td> 0</td>
      <td> 5921</td>
      <td> 0</td>
      <td> 0</td>
      <td>   0</td>
      <td>  292.0</td>
      <td> 6708.14</td>
      <td> 4420.55</td>
    </tr>
    <tr>
      <th>3 </th>
      <td> 100004</td>
      <td> 913307.305588</td>
      <td> 123550.905179</td>
      <td>   10.467310</td>
      <td>-177.696901</td>
      <td>  32.267293</td>
      <td>   9.835071</td>
      <td> 7853.950214</td>
      <td> 5880.768441</td>
      <td> 31415.800866</td>
      <td> 19673.126953</td>
      <td> 196348.755435</td>
      <td> 107230.957454</td>
      <td> 785395.021770</td>
      <td> 369655.430725</td>
      <td> 3141580.087165</td>
      <td> 1304984.251624</td>
      <td> 0</td>
      <td>  9313.748868</td>
      <td> 50462.934751</td>
      <td> 138130.017630</td>
      <td> 456204.304060</td>
      <td> 0</td>
      <td> 0</td>
      <td> 0.296467</td>
      <td> 0.473425</td>
      <td> 0.257007</td>
      <td> 0.470600</td>
      <td> 0.175873</td>
      <td> 0.373672</td>
      <td> 0.145215</td>
      <td> 0.349586</td>
      <td> 633</td>
      <td>  5.00011</td>
      <td> 53.9978</td>
      <td> 21.2648</td>
      <td> 13.60150</td>
      <td> 2120</td>
      <td>  2.000090</td>
      <td> 70.4479</td>
      <td> 33.9770</td>
      <td> 22.38520</td>
      <td> 11545</td>
      <td> 2.000090</td>
      <td> 72.4902</td>
      <td> 45.0991</td>
      <td> 21.4402</td>
      <td> 39759</td>
      <td>-0.567119</td>
      <td> 72.4902</td>
      <td> 42.1236</td>
      <td> 15.6252</td>
      <td> 139880</td>
      <td>-0.571724</td>
      <td> 81.3846</td>
      <td> 40.9431</td>
      <td> 18.7664</td>
      <td>    0.000000</td>
      <td> 11215.466129</td>
      <td>  76477.878380</td>
      <td> 389016.150776</td>
      <td> 1512592.943686</td>
      <td> 0.000000</td>
      <td> 0.000000</td>
      <td> 0.357001</td>
      <td> 0.570091</td>
      <td> 0.389500</td>
      <td> 0.713207</td>
      <td> 0.495313</td>
      <td> 1.052375</td>
      <td> 0.481475</td>
      <td> 1.159089</td>
      <td> 0</td>
      <td> 0</td>
      <td> 0</td>
      <td>    0</td>
      <td> 3172</td>
      <td> 0</td>
      <td> 0</td>
      <td> 0</td>
      <td> 0</td>
      <td> 0</td>
      <td> 0</td>
      <td> 0</td>
      <td> 0</td>
      <td> 0</td>
      <td> 0</td>
      <td> 0</td>
      <td> 0</td>
      <td> 0</td>
      <td> 0</td>
      <td> 0</td>
      <td> 0</td>
      <td> 0</td>
      <td> 0</td>
      <td> 0</td>
      <td> 0</td>
      <td> 0</td>
      <td> 0</td>
      <td> 0</td>
      <td> 0</td>
      <td> 0</td>
      <td> 0</td>
      <td> 0</td>
      <td> 0</td>
      <td> 0</td>
      <td> 0</td>
      <td> 0</td>
      <td> 0</td>
      <td> 0</td>
      <td> 0</td>
      <td> 0</td>
      <td> 0</td>
      <td> 0</td>
      <td> 0</td>
      <td> 0</td>
      <td> 0</td>
      <td> 0</td>
      <td>    0</td>
      <td> 0</td>
      <td> 0</td>
      <td> 0</td>
      <td> 0</td>
      <td> 0</td>
      <td> 0</td>
      <td> 0</td>
      <td> 0</td>
      <td> 0</td>
      <td> 0</td>
      <td> 3172</td>
      <td> 0</td>
      <td> 0</td>
      <td>   0</td>
      <td>  292.0</td>
      <td> 7112.80</td>
      <td> 4550.44</td>
    </tr>
    <tr>
      <th>4 </th>
      <td> 100005</td>
      <td> 913307.305588</td>
      <td> 123878.989169</td>
      <td>   11.947045</td>
      <td> 178.242903</td>
      <td>  15.812024</td>
      <td>   4.819505</td>
      <td> 7853.950217</td>
      <td> 5651.420356</td>
      <td> 31415.800871</td>
      <td> 19634.119037</td>
      <td> 196348.755450</td>
      <td> 107940.774628</td>
      <td> 785395.021798</td>
      <td> 364151.650975</td>
      <td> 3141580.087222</td>
      <td> 1309911.503914</td>
      <td> 0</td>
      <td>  7535.803044</td>
      <td> 41917.311165</td>
      <td> 135291.915465</td>
      <td> 444299.917319</td>
      <td> 0</td>
      <td> 0</td>
      <td> 0.239873</td>
      <td> 0.383812</td>
      <td> 0.213484</td>
      <td> 0.388336</td>
      <td> 0.172260</td>
      <td> 0.371526</td>
      <td> 0.141426</td>
      <td> 0.339183</td>
      <td> 604</td>
      <td>  2.70946</td>
      <td> 61.9994</td>
      <td> 26.3050</td>
      <td> 18.87760</td>
      <td> 2109</td>
      <td>  3.045360</td>
      <td> 71.9000</td>
      <td> 39.6832</td>
      <td> 22.90150</td>
      <td> 11625</td>
      <td> 2.000090</td>
      <td> 72.4902</td>
      <td> 44.4567</td>
      <td> 21.1206</td>
      <td> 39160</td>
      <td>-0.056434</td>
      <td> 72.4902</td>
      <td> 43.0519</td>
      <td> 15.6687</td>
      <td> 140624</td>
      <td>-0.571724</td>
      <td> 81.3846</td>
      <td> 42.2975</td>
      <td> 18.6839</td>
      <td> 4704.419334</td>
      <td> 18160.057948</td>
      <td> 104013.332977</td>
      <td> 402625.521712</td>
      <td> 1576349.809436</td>
      <td> 0.598988</td>
      <td> 0.832431</td>
      <td> 0.578055</td>
      <td> 0.924923</td>
      <td> 0.529738</td>
      <td> 0.963615</td>
      <td> 0.512641</td>
      <td> 1.105653</td>
      <td> 0.501770</td>
      <td> 1.203402</td>
      <td> 0</td>
      <td> 0</td>
      <td> 0</td>
      <td>    0</td>
      <td> 3172</td>
      <td> 0</td>
      <td> 0</td>
      <td> 0</td>
      <td> 0</td>
      <td> 0</td>
      <td> 0</td>
      <td> 0</td>
      <td> 0</td>
      <td> 0</td>
      <td> 0</td>
      <td> 0</td>
      <td> 0</td>
      <td> 0</td>
      <td> 0</td>
      <td> 0</td>
      <td> 0</td>
      <td> 0</td>
      <td> 0</td>
      <td> 0</td>
      <td> 0</td>
      <td> 0</td>
      <td> 0</td>
      <td> 0</td>
      <td> 0</td>
      <td> 0</td>
      <td> 0</td>
      <td> 0</td>
      <td> 0</td>
      <td> 0</td>
      <td> 0</td>
      <td> 0</td>
      <td> 0</td>
      <td> 0</td>
      <td> 0</td>
      <td> 0</td>
      <td> 0</td>
      <td> 0</td>
      <td> 0</td>
      <td> 0</td>
      <td> 0</td>
      <td> 0</td>
      <td>    0</td>
      <td> 0</td>
      <td> 0</td>
      <td> 0</td>
      <td> 0</td>
      <td> 0</td>
      <td> 0</td>
      <td> 0</td>
      <td> 0</td>
      <td> 0</td>
      <td> 0</td>
      <td> 3172</td>
      <td> 0</td>
      <td> 0</td>
      <td>   0</td>
      <td> 6143.0</td>
      <td> 5107.80</td>
      <td> 4109.58</td>
    </tr>
    <tr>
      <th>5 </th>
      <td> 100006</td>
      <td> 913307.305588</td>
      <td> 124207.073158</td>
      <td>   22.624182</td>
      <td>-161.923546</td>
      <td>  79.396129</td>
      <td>  24.199940</td>
      <td> 7853.950217</td>
      <td> 6739.007056</td>
      <td> 31415.800871</td>
      <td> 21095.434941</td>
      <td> 196348.755450</td>
      <td>  98147.310302</td>
      <td> 785395.021798</td>
      <td> 352720.347034</td>
      <td> 3141580.087222</td>
      <td> 1302774.674229</td>
      <td> 0</td>
      <td>  7337.596454</td>
      <td> 34502.720968</td>
      <td> 132850.848030</td>
      <td> 417494.587341</td>
      <td> 0</td>
      <td> 0</td>
      <td> 0.233564</td>
      <td> 0.347829</td>
      <td> 0.175722</td>
      <td> 0.351540</td>
      <td> 0.169152</td>
      <td> 0.376646</td>
      <td> 0.132893</td>
      <td> 0.320466</td>
      <td> 727</td>
      <td>  4.00088</td>
      <td> 46.7818</td>
      <td> 23.0326</td>
      <td> 11.08500</td>
      <td> 2267</td>
      <td>  2.000180</td>
      <td> 68.5309</td>
      <td> 29.1116</td>
      <td> 16.65140</td>
      <td> 10549</td>
      <td> 0.000003</td>
      <td> 72.4902</td>
      <td> 43.2480</td>
      <td> 20.4839</td>
      <td> 37924</td>
      <td> 0.000202</td>
      <td> 72.4902</td>
      <td> 44.0058</td>
      <td> 15.4997</td>
      <td> 140158</td>
      <td>-0.056434</td>
      <td> 81.3846</td>
      <td> 43.4028</td>
      <td> 18.6851</td>
      <td> 6783.461332</td>
      <td> 24171.562636</td>
      <td> 115763.729527</td>
      <td> 407398.208171</td>
      <td> 1641226.048596</td>
      <td> 0.863701</td>
      <td> 1.006597</td>
      <td> 0.769408</td>
      <td> 1.145820</td>
      <td> 0.589582</td>
      <td> 1.179490</td>
      <td> 0.518718</td>
      <td> 1.155018</td>
      <td> 0.522421</td>
      <td> 1.259793</td>
      <td> 0</td>
      <td> 0</td>
      <td> 0</td>
      <td>    0</td>
      <td> 3172</td>
      <td> 0</td>
      <td> 0</td>
      <td> 0</td>
      <td> 0</td>
      <td> 0</td>
      <td> 0</td>
      <td> 0</td>
      <td> 0</td>
      <td> 0</td>
      <td> 0</td>
      <td> 0</td>
      <td> 0</td>
      <td> 0</td>
      <td> 0</td>
      <td> 0</td>
      <td> 0</td>
      <td> 0</td>
      <td> 0</td>
      <td> 0</td>
      <td> 0</td>
      <td> 0</td>
      <td> 0</td>
      <td> 0</td>
      <td> 0</td>
      <td> 0</td>
      <td> 0</td>
      <td> 0</td>
      <td> 0</td>
      <td> 0</td>
      <td> 0</td>
      <td> 0</td>
      <td> 0</td>
      <td> 0</td>
      <td> 0</td>
      <td> 0</td>
      <td> 0</td>
      <td> 0</td>
      <td> 0</td>
      <td> 0</td>
      <td> 0</td>
      <td> 0</td>
      <td>    0</td>
      <td> 0</td>
      <td> 0</td>
      <td> 0</td>
      <td> 0</td>
      <td> 0</td>
      <td> 0</td>
      <td> 0</td>
      <td> 0</td>
      <td> 0</td>
      <td> 0</td>
      <td> 3172</td>
      <td> 0</td>
      <td> 0</td>
      <td>   0</td>
      <td> 4454.0</td>
      <td> 2856.00</td>
      <td> 5352.36</td>
    </tr>
    <tr>
      <th>6 </th>
      <td> 100007</td>
      <td> 913307.305588</td>
      <td> 124535.157148</td>
      <td>    8.151647</td>
      <td> 129.986839</td>
      <td>  14.512148</td>
      <td>   4.423303</td>
      <td> 7853.950216</td>
      <td> 4616.186123</td>
      <td> 31415.800869</td>
      <td> 15732.207012</td>
      <td> 196348.755442</td>
      <td>  82684.172200</td>
      <td> 785395.021784</td>
      <td> 336553.331833</td>
      <td> 3141580.087194</td>
      <td> 1285053.695475</td>
      <td> 0</td>
      <td>  5358.238357</td>
      <td> 30564.717464</td>
      <td> 120886.097773</td>
      <td> 395407.195670</td>
      <td> 0</td>
      <td> 0</td>
      <td> 0.170559</td>
      <td> 0.340590</td>
      <td> 0.155665</td>
      <td> 0.369656</td>
      <td> 0.153918</td>
      <td> 0.359189</td>
      <td> 0.125863</td>
      <td> 0.307697</td>
      <td> 499</td>
      <td>  3.99929</td>
      <td> 23.3207</td>
      <td> 12.2677</td>
      <td>  5.41508</td>
      <td> 1690</td>
      <td>  0.745061</td>
      <td> 43.2001</td>
      <td> 18.7173</td>
      <td>  9.72519</td>
      <td>  8867</td>
      <td>-0.056434</td>
      <td> 71.9000</td>
      <td> 38.7254</td>
      <td> 18.6814</td>
      <td> 36192</td>
      <td>-0.056434</td>
      <td> 72.4902</td>
      <td> 43.8062</td>
      <td> 15.9603</td>
      <td> 138169</td>
      <td>-0.056434</td>
      <td> 81.3846</td>
      <td> 44.2498</td>
      <td> 18.7126</td>
      <td> 5773.110646</td>
      <td> 18733.478213</td>
      <td> 102679.547931</td>
      <td> 407044.663342</td>
      <td> 1642579.395792</td>
      <td> 0.735058</td>
      <td> 1.250623</td>
      <td> 0.596308</td>
      <td> 1.190772</td>
      <td> 0.522945</td>
      <td> 1.241828</td>
      <td> 0.518267</td>
      <td> 1.209451</td>
      <td> 0.522851</td>
      <td> 1.278218</td>
      <td> 0</td>
      <td> 0</td>
      <td> 0</td>
      <td>    0</td>
      <td> 3172</td>
      <td> 0</td>
      <td> 0</td>
      <td> 0</td>
      <td> 0</td>
      <td> 0</td>
      <td> 0</td>
      <td> 0</td>
      <td> 0</td>
      <td> 0</td>
      <td> 0</td>
      <td> 0</td>
      <td> 0</td>
      <td> 0</td>
      <td> 0</td>
      <td> 0</td>
      <td> 0</td>
      <td> 0</td>
      <td> 0</td>
      <td> 0</td>
      <td> 0</td>
      <td> 0</td>
      <td> 0</td>
      <td> 0</td>
      <td> 0</td>
      <td> 0</td>
      <td> 0</td>
      <td> 0</td>
      <td> 0</td>
      <td> 0</td>
      <td> 0</td>
      <td> 0</td>
      <td> 0</td>
      <td> 0</td>
      <td> 0</td>
      <td> 0</td>
      <td> 0</td>
      <td> 0</td>
      <td> 0</td>
      <td> 0</td>
      <td> 0</td>
      <td> 0</td>
      <td>    0</td>
      <td> 0</td>
      <td> 0</td>
      <td> 0</td>
      <td> 0</td>
      <td> 0</td>
      <td> 0</td>
      <td> 0</td>
      <td> 0</td>
      <td> 0</td>
      <td> 0</td>
      <td> 3172</td>
      <td> 0</td>
      <td> 0</td>
      <td>   0</td>
      <td> 6143.0</td>
      <td> 3351.17</td>
      <td> 4777.50</td>
    </tr>
    <tr>
      <th>7 </th>
      <td> 100008</td>
      <td> 913307.305588</td>
      <td> 124863.241137</td>
      <td>-9999.000000</td>
      <td>   0.000000</td>
      <td>   0.000000</td>
      <td>   0.000000</td>
      <td> 7853.950216</td>
      <td>    0.000000</td>
      <td> 31415.800869</td>
      <td>     0.000000</td>
      <td> 196348.755442</td>
      <td>      0.000000</td>
      <td> 785395.021784</td>
      <td>      0.000000</td>
      <td> 3141580.087194</td>
      <td>       0.000000</td>
      <td> 0</td>
      <td>   803.041086</td>
      <td> 27076.227876</td>
      <td> 104331.296215</td>
      <td> 381262.851315</td>
      <td> 0</td>
      <td> 0</td>
      <td> 0.025562</td>
      <td> 0.000000</td>
      <td> 0.137899</td>
      <td> 0.000000</td>
      <td> 0.132839</td>
      <td> 0.000000</td>
      <td> 0.121360</td>
      <td> 0.000000</td>
      <td>   0</td>
      <td>  0.00000</td>
      <td>  0.0000</td>
      <td>  0.0000</td>
      <td>  0.00000</td>
      <td>    0</td>
      <td>  0.000000</td>
      <td>  0.0000</td>
      <td>  0.0000</td>
      <td>  0.00000</td>
      <td>     0</td>
      <td> 0.000000</td>
      <td>  0.0000</td>
      <td>  0.0000</td>
      <td>  0.0000</td>
      <td>     0</td>
      <td> 0.000000</td>
      <td>  0.0000</td>
      <td>  0.0000</td>
      <td>  0.0000</td>
      <td>      0</td>
      <td> 0.000000</td>
      <td>  0.0000</td>
      <td>  0.0000</td>
      <td>  0.0000</td>
      <td>    0.000000</td>
      <td>  1047.157418</td>
      <td>  75018.148200</td>
      <td> 388421.430605</td>
      <td> 1600726.543975</td>
      <td> 0.000000</td>
      <td> 0.000000</td>
      <td> 0.033332</td>
      <td> 0.000000</td>
      <td> 0.382066</td>
      <td> 0.000000</td>
      <td> 0.494556</td>
      <td> 0.000000</td>
      <td> 0.509529</td>
      <td> 0.000000</td>
      <td> 0</td>
      <td> 0</td>
      <td> 0</td>
      <td> 5921</td>
      <td> 3172</td>
      <td> 0</td>
      <td> 0</td>
      <td> 0</td>
      <td> 0</td>
      <td> 0</td>
      <td> 0</td>
      <td> 0</td>
      <td> 0</td>
      <td> 0</td>
      <td> 0</td>
      <td> 0</td>
      <td> 0</td>
      <td> 0</td>
      <td> 0</td>
      <td> 0</td>
      <td> 0</td>
      <td> 0</td>
      <td> 0</td>
      <td> 0</td>
      <td> 0</td>
      <td> 0</td>
      <td> 0</td>
      <td> 0</td>
      <td> 0</td>
      <td> 0</td>
      <td> 0</td>
      <td> 0</td>
      <td> 0</td>
      <td> 0</td>
      <td> 0</td>
      <td> 0</td>
      <td> 0</td>
      <td> 0</td>
      <td> 0</td>
      <td> 0</td>
      <td> 0</td>
      <td> 0</td>
      <td> 0</td>
      <td> 0</td>
      <td> 0</td>
      <td> 0</td>
      <td> 5921</td>
      <td> 0</td>
      <td> 0</td>
      <td> 0</td>
      <td> 0</td>
      <td> 0</td>
      <td> 0</td>
      <td> 0</td>
      <td> 0</td>
      <td> 0</td>
      <td> 0</td>
      <td> 3172</td>
      <td> 0</td>
      <td> 0</td>
      <td>   0</td>
      <td>    0.0</td>
      <td> 3351.17</td>
      <td> 5010.33</td>
    </tr>
    <tr>
      <th>8 </th>
      <td> 100009</td>
      <td> 913635.389577</td>
      <td> 121910.485232</td>
      <td>-9999.000000</td>
      <td>   0.000000</td>
      <td>   0.000000</td>
      <td>   0.000000</td>
      <td> 7853.950217</td>
      <td>    0.000000</td>
      <td> 31415.800869</td>
      <td>     0.000000</td>
      <td> 196348.755442</td>
      <td>      0.000000</td>
      <td> 785395.021798</td>
      <td>      0.000000</td>
      <td> 3141580.087194</td>
      <td>       0.000000</td>
      <td> 0</td>
      <td>  5594.504963</td>
      <td> 43218.160325</td>
      <td> 161834.684399</td>
      <td> 457872.940419</td>
      <td> 0</td>
      <td> 0</td>
      <td> 0.178079</td>
      <td> 0.000000</td>
      <td> 0.220109</td>
      <td> 0.000000</td>
      <td> 0.206055</td>
      <td> 0.000000</td>
      <td> 0.145746</td>
      <td> 0.000000</td>
      <td>   0</td>
      <td>  0.00000</td>
      <td>  0.0000</td>
      <td>  0.0000</td>
      <td>  0.00000</td>
      <td>    0</td>
      <td>  0.000000</td>
      <td>  0.0000</td>
      <td>  0.0000</td>
      <td>  0.00000</td>
      <td>     0</td>
      <td> 0.000000</td>
      <td>  0.0000</td>
      <td>  0.0000</td>
      <td>  0.0000</td>
      <td>     0</td>
      <td> 0.000000</td>
      <td>  0.0000</td>
      <td>  0.0000</td>
      <td>  0.0000</td>
      <td>      0</td>
      <td> 0.000000</td>
      <td>  0.0000</td>
      <td>  0.0000</td>
      <td>  0.0000</td>
      <td>    0.000000</td>
      <td>     0.000000</td>
      <td>   6523.958023</td>
      <td> 165829.213717</td>
      <td> 1188020.850995</td>
      <td> 0.000000</td>
      <td> 0.000000</td>
      <td> 0.000000</td>
      <td> 0.000000</td>
      <td> 0.033226</td>
      <td> 0.000000</td>
      <td> 0.211141</td>
      <td> 0.000000</td>
      <td> 0.378160</td>
      <td> 0.000000</td>
      <td> 0</td>
      <td> 0</td>
      <td> 0</td>
      <td>    0</td>
      <td>    0</td>
      <td> 0</td>
      <td> 0</td>
      <td> 0</td>
      <td> 0</td>
      <td> 0</td>
      <td> 0</td>
      <td> 0</td>
      <td> 0</td>
      <td> 0</td>
      <td> 0</td>
      <td> 0</td>
      <td> 0</td>
      <td> 0</td>
      <td> 0</td>
      <td> 0</td>
      <td> 0</td>
      <td> 0</td>
      <td> 0</td>
      <td> 0</td>
      <td> 0</td>
      <td> 0</td>
      <td> 0</td>
      <td> 0</td>
      <td> 0</td>
      <td> 0</td>
      <td> 0</td>
      <td> 0</td>
      <td> 0</td>
      <td> 0</td>
      <td> 0</td>
      <td> 0</td>
      <td> 0</td>
      <td> 0</td>
      <td> 0</td>
      <td> 0</td>
      <td> 0</td>
      <td> 0</td>
      <td> 0</td>
      <td> 0</td>
      <td> 0</td>
      <td> 0</td>
      <td>    0</td>
      <td> 0</td>
      <td> 0</td>
      <td> 0</td>
      <td> 0</td>
      <td> 0</td>
      <td> 0</td>
      <td> 0</td>
      <td> 0</td>
      <td> 0</td>
      <td> 0</td>
      <td>    0</td>
      <td> 0</td>
      <td> 0</td>
      <td>   0</td>
      <td>    0.0</td>
      <td> 5696.50</td>
      <td> 4427.00</td>
    </tr>
    <tr>
      <th>9 </th>
      <td> 100010</td>
      <td> 913635.389577</td>
      <td> 122238.569221</td>
      <td>    6.932351</td>
      <td>-147.873600</td>
      <td>   0.861270</td>
      <td>   0.262515</td>
      <td> 7853.950216</td>
      <td> 4911.247372</td>
      <td> 31415.800869</td>
      <td> 18082.677132</td>
      <td> 196348.755442</td>
      <td> 105610.295941</td>
      <td> 785395.021784</td>
      <td> 378958.278703</td>
      <td> 3141580.087194</td>
      <td> 1305972.414625</td>
      <td> 0</td>
      <td>  9516.669674</td>
      <td> 58927.634732</td>
      <td> 163826.495231</td>
      <td> 481232.788348</td>
      <td> 0</td>
      <td> 0</td>
      <td> 0.302926</td>
      <td> 0.526287</td>
      <td> 0.300117</td>
      <td> 0.557972</td>
      <td> 0.208591</td>
      <td> 0.432307</td>
      <td> 0.153182</td>
      <td> 0.368486</td>
      <td> 530</td>
      <td>  2.83604</td>
      <td> 31.0923</td>
      <td> 17.3706</td>
      <td>  9.11595</td>
      <td> 1944</td>
      <td>  2.747340</td>
      <td> 33.0471</td>
      <td> 20.8994</td>
      <td>  8.48463</td>
      <td> 11361</td>
      <td> 2.000760</td>
      <td> 53.6699</td>
      <td> 27.1614</td>
      <td> 11.8520</td>
      <td> 40544</td>
      <td>-0.571724</td>
      <td> 72.4902</td>
      <td> 32.6554</td>
      <td> 16.1946</td>
      <td> 139999</td>
      <td>-0.571724</td>
      <td> 80.4000</td>
      <td> 34.7767</td>
      <td> 19.1416</td>
      <td> 1711.196101</td>
      <td>  3484.589228</td>
      <td>  13044.091922</td>
      <td> 255869.051505</td>
      <td> 1338189.244976</td>
      <td> 0.217877</td>
      <td> 0.348424</td>
      <td> 0.110918</td>
      <td> 0.192703</td>
      <td> 0.066433</td>
      <td> 0.123512</td>
      <td> 0.325784</td>
      <td> 0.675191</td>
      <td> 0.425961</td>
      <td> 1.024669</td>
      <td> 0</td>
      <td> 0</td>
      <td> 0</td>
      <td>    0</td>
      <td>    0</td>
      <td> 0</td>
      <td> 0</td>
      <td> 0</td>
      <td> 0</td>
      <td> 0</td>
      <td> 0</td>
      <td> 0</td>
      <td> 0</td>
      <td> 0</td>
      <td> 0</td>
      <td> 0</td>
      <td> 0</td>
      <td> 0</td>
      <td> 0</td>
      <td> 0</td>
      <td> 0</td>
      <td> 0</td>
      <td> 0</td>
      <td> 0</td>
      <td> 0</td>
      <td> 0</td>
      <td> 0</td>
      <td> 0</td>
      <td> 0</td>
      <td> 0</td>
      <td> 0</td>
      <td> 0</td>
      <td> 0</td>
      <td> 0</td>
      <td> 0</td>
      <td> 0</td>
      <td> 0</td>
      <td> 0</td>
      <td> 0</td>
      <td> 0</td>
      <td> 0</td>
      <td> 0</td>
      <td> 0</td>
      <td> 0</td>
      <td> 0</td>
      <td> 0</td>
      <td>    0</td>
      <td> 0</td>
      <td> 0</td>
      <td> 0</td>
      <td> 0</td>
      <td> 0</td>
      <td> 0</td>
      <td> 0</td>
      <td> 0</td>
      <td> 0</td>
      <td> 0</td>
      <td>    0</td>
      <td> 0</td>
      <td> 0</td>
      <td>   0</td>
      <td> 5696.5</td>
      <td> 5696.50</td>
      <td> 3804.14</td>
    </tr>
    <tr>
      <th>10</th>
      <td> 100011</td>
      <td> 913635.389577</td>
      <td> 122566.653211</td>
      <td>   25.593199</td>
      <td>-158.656462</td>
      <td> 143.401367</td>
      <td>  43.708737</td>
      <td> 7853.950214</td>
      <td> 7833.295299</td>
      <td> 31415.800866</td>
      <td> 26100.591560</td>
      <td> 196348.755435</td>
      <td> 123712.061411</td>
      <td> 785395.021770</td>
      <td> 415633.368788</td>
      <td> 3141580.087165</td>
      <td> 1382821.741367</td>
      <td> 0</td>
      <td> 12915.623512</td>
      <td> 69362.525664</td>
      <td> 166341.415814</td>
      <td> 499342.871997</td>
      <td> 0</td>
      <td> 0</td>
      <td> 0.411119</td>
      <td> 0.494840</td>
      <td> 0.353262</td>
      <td> 0.560677</td>
      <td> 0.211793</td>
      <td> 0.400212</td>
      <td> 0.158946</td>
      <td> 0.361104</td>
      <td> 847</td>
      <td>  5.17336</td>
      <td> 38.6465</td>
      <td> 23.7830</td>
      <td>  9.07310</td>
      <td> 2810</td>
      <td>  2.887140</td>
      <td> 48.0008</td>
      <td> 25.1452</td>
      <td> 11.43020</td>
      <td> 13318</td>
      <td> 2.000130</td>
      <td> 58.6473</td>
      <td> 32.3652</td>
      <td> 14.5568</td>
      <td> 44748</td>
      <td> 1.219650</td>
      <td> 72.4902</td>
      <td> 35.8613</td>
      <td> 16.3781</td>
      <td> 148264</td>
      <td>-0.571724</td>
      <td> 80.4338</td>
      <td> 36.4327</td>
      <td> 19.5750</td>
      <td>    0.000000</td>
      <td>  5729.645316</td>
      <td>  33354.668326</td>
      <td> 347689.984644</td>
      <td> 1480585.504400</td>
      <td> 0.000000</td>
      <td> 0.000000</td>
      <td> 0.182381</td>
      <td> 0.219522</td>
      <td> 0.169875</td>
      <td> 0.269615</td>
      <td> 0.442694</td>
      <td> 0.836530</td>
      <td> 0.471287</td>
      <td> 1.070699</td>
      <td> 0</td>
      <td> 0</td>
      <td> 0</td>
      <td>    0</td>
      <td>    0</td>
      <td> 0</td>
      <td> 0</td>
      <td> 0</td>
      <td> 0</td>
      <td> 0</td>
      <td> 0</td>
      <td> 0</td>
      <td> 0</td>
      <td> 0</td>
      <td> 0</td>
      <td> 0</td>
      <td> 0</td>
      <td> 0</td>
      <td> 0</td>
      <td> 0</td>
      <td> 0</td>
      <td> 0</td>
      <td> 0</td>
      <td> 0</td>
      <td> 0</td>
      <td> 0</td>
      <td> 0</td>
      <td> 0</td>
      <td> 0</td>
      <td> 0</td>
      <td> 0</td>
      <td> 0</td>
      <td> 0</td>
      <td> 0</td>
      <td> 0</td>
      <td> 0</td>
      <td> 0</td>
      <td> 0</td>
      <td> 0</td>
      <td> 0</td>
      <td> 0</td>
      <td> 0</td>
      <td> 0</td>
      <td> 0</td>
      <td> 0</td>
      <td> 0</td>
      <td>    0</td>
      <td> 0</td>
      <td> 0</td>
      <td> 0</td>
      <td> 0</td>
      <td> 0</td>
      <td> 0</td>
      <td> 0</td>
      <td> 0</td>
      <td> 0</td>
      <td> 0</td>
      <td>    0</td>
      <td> 0</td>
      <td> 0</td>
      <td>   0</td>
      <td> 5696.5</td>
      <td> 5696.50</td>
      <td> 4057.00</td>
    </tr>
    <tr>
      <th>11</th>
      <td> 100012</td>
      <td> 913635.389577</td>
      <td> 122894.737200</td>
      <td>   41.408394</td>
      <td>-160.210859</td>
      <td> 287.609447</td>
      <td>  87.663359</td>
      <td> 7853.950214</td>
      <td> 7833.295299</td>
      <td> 31415.800866</td>
      <td> 31097.243219</td>
      <td> 196348.755435</td>
      <td> 138442.450478</td>
      <td> 785395.021770</td>
      <td> 449511.606492</td>
      <td> 3141580.087165</td>
      <td> 1442080.725019</td>
      <td> 0</td>
      <td> 22701.336280</td>
      <td> 70677.418960</td>
      <td> 170197.971004</td>
      <td> 509770.468600</td>
      <td> 0</td>
      <td> 0</td>
      <td> 0.722609</td>
      <td> 0.730011</td>
      <td> 0.359959</td>
      <td> 0.510518</td>
      <td> 0.216704</td>
      <td> 0.378629</td>
      <td> 0.162266</td>
      <td> 0.353496</td>
      <td> 847</td>
      <td>  9.99947</td>
      <td> 52.9805</td>
      <td> 39.4566</td>
      <td>  9.96918</td>
      <td> 3347</td>
      <td>  3.999990</td>
      <td> 54.8000</td>
      <td> 34.1710</td>
      <td> 16.11760</td>
      <td> 14907</td>
      <td> 2.836040</td>
      <td> 72.4902</td>
      <td> 38.7016</td>
      <td> 17.5287</td>
      <td> 48389</td>
      <td> 2.000020</td>
      <td> 72.4902</td>
      <td> 37.9715</td>
      <td> 15.8371</td>
      <td> 154622</td>
      <td>-0.571724</td>
      <td> 81.3846</td>
      <td> 38.0431</td>
      <td> 19.8535</td>
      <td>    0.000000</td>
      <td>  2245.056088</td>
      <td>  67151.243771</td>
      <td> 423273.707064</td>
      <td> 1591062.584934</td>
      <td> 0.000000</td>
      <td> 0.000000</td>
      <td> 0.071463</td>
      <td> 0.072195</td>
      <td> 0.342000</td>
      <td> 0.485048</td>
      <td> 0.538931</td>
      <td> 0.941630</td>
      <td> 0.506453</td>
      <td> 1.103310</td>
      <td> 0</td>
      <td> 0</td>
      <td> 0</td>
      <td>    0</td>
      <td> 5921</td>
      <td> 0</td>
      <td> 0</td>
      <td> 0</td>
      <td> 0</td>
      <td> 0</td>
      <td> 0</td>
      <td> 0</td>
      <td> 0</td>
      <td> 0</td>
      <td> 0</td>
      <td> 0</td>
      <td> 0</td>
      <td> 0</td>
      <td> 0</td>
      <td> 0</td>
      <td> 0</td>
      <td> 0</td>
      <td> 0</td>
      <td> 0</td>
      <td> 0</td>
      <td> 0</td>
      <td> 0</td>
      <td> 0</td>
      <td> 0</td>
      <td> 0</td>
      <td> 0</td>
      <td> 0</td>
      <td> 0</td>
      <td> 0</td>
      <td> 0</td>
      <td> 0</td>
      <td> 0</td>
      <td> 0</td>
      <td> 0</td>
      <td> 0</td>
      <td> 0</td>
      <td> 0</td>
      <td> 0</td>
      <td> 0</td>
      <td> 0</td>
      <td> 0</td>
      <td>    0</td>
      <td> 0</td>
      <td> 0</td>
      <td> 0</td>
      <td> 0</td>
      <td> 0</td>
      <td> 0</td>
      <td> 0</td>
      <td> 0</td>
      <td> 0</td>
      <td> 0</td>
      <td> 5921</td>
      <td> 0</td>
      <td> 0</td>
      <td>   0</td>
      <td> 5696.5</td>
      <td> 6115.75</td>
      <td> 4486.19</td>
    </tr>
    <tr>
      <th>12</th>
      <td> 100013</td>
      <td> 913635.389577</td>
      <td> 123222.821190</td>
      <td>   53.034622</td>
      <td> 179.351037</td>
      <td> 371.361273</td>
      <td> 113.190916</td>
      <td> 7853.950214</td>
      <td> 7833.295299</td>
      <td> 31415.800866</td>
      <td> 31374.816076</td>
      <td> 196348.755435</td>
      <td> 149029.103334</td>
      <td> 785395.021770</td>
      <td> 465933.342537</td>
      <td> 3141580.087165</td>
      <td> 1473565.887536</td>
      <td> 0</td>
      <td> 20502.653239</td>
      <td> 65696.131131</td>
      <td> 175776.890151</td>
      <td> 514035.067600</td>
      <td> 0</td>
      <td> 0</td>
      <td> 0.652622</td>
      <td> 0.653475</td>
      <td> 0.334589</td>
      <td> 0.440828</td>
      <td> 0.223807</td>
      <td> 0.377258</td>
      <td> 0.163623</td>
      <td> 0.348838</td>
      <td> 847</td>
      <td> 22.67190</td>
      <td> 58.6473</td>
      <td> 49.6916</td>
      <td>  7.82488</td>
      <td> 3380</td>
      <td>  4.641180</td>
      <td> 66.9046</td>
      <td> 45.3308</td>
      <td> 16.76630</td>
      <td> 16050</td>
      <td> 2.000730</td>
      <td> 72.4902</td>
      <td> 44.5061</td>
      <td> 18.8185</td>
      <td> 50156</td>
      <td> 0.745061</td>
      <td> 72.4902</td>
      <td> 40.1434</td>
      <td> 15.1725</td>
      <td> 158030</td>
      <td>-0.571724</td>
      <td> 81.3846</td>
      <td> 39.8018</td>
      <td> 19.8079</td>
      <td>    0.000000</td>
      <td>  4842.944719</td>
      <td> 107110.174083</td>
      <td> 479774.104777</td>
      <td> 1725814.534356</td>
      <td> 0.000000</td>
      <td> 0.000000</td>
      <td> 0.154156</td>
      <td> 0.154358</td>
      <td> 0.545510</td>
      <td> 0.718720</td>
      <td> 0.610870</td>
      <td> 1.029705</td>
      <td> 0.549346</td>
      <td> 1.171182</td>
      <td> 0</td>
      <td> 0</td>
      <td> 0</td>
      <td>    0</td>
      <td> 3172</td>
      <td> 0</td>
      <td> 0</td>
      <td> 0</td>
      <td> 0</td>
      <td> 0</td>
      <td> 0</td>
      <td> 0</td>
      <td> 0</td>
      <td> 0</td>
      <td> 0</td>
      <td> 0</td>
      <td> 0</td>
      <td> 0</td>
      <td> 0</td>
      <td> 0</td>
      <td> 0</td>
      <td> 0</td>
      <td> 0</td>
      <td> 0</td>
      <td> 0</td>
      <td> 0</td>
      <td> 0</td>
      <td> 0</td>
      <td> 0</td>
      <td> 0</td>
      <td> 0</td>
      <td> 0</td>
      <td> 0</td>
      <td> 0</td>
      <td> 0</td>
      <td> 0</td>
      <td> 0</td>
      <td> 0</td>
      <td> 0</td>
      <td> 0</td>
      <td> 0</td>
      <td> 0</td>
      <td> 0</td>
      <td> 0</td>
      <td> 0</td>
      <td> 0</td>
      <td>    0</td>
      <td> 0</td>
      <td> 0</td>
      <td> 0</td>
      <td> 0</td>
      <td> 0</td>
      <td> 0</td>
      <td> 0</td>
      <td> 0</td>
      <td> 0</td>
      <td> 0</td>
      <td> 3172</td>
      <td> 0</td>
      <td> 0</td>
      <td> 292</td>
      <td>  292.0</td>
      <td> 6115.75</td>
      <td> 5596.54</td>
    </tr>
    <tr>
      <th>13</th>
      <td> 100014</td>
      <td> 913635.389577</td>
      <td> 123550.905179</td>
      <td>   65.846687</td>
      <td>-177.696901</td>
      <td> 360.086264</td>
      <td> 109.754293</td>
      <td> 7853.950214</td>
      <td> 7833.295299</td>
      <td> 31415.800866</td>
      <td> 31374.816075</td>
      <td> 196348.755435</td>
      <td> 154998.827199</td>
      <td> 785395.021770</td>
      <td> 467827.476764</td>
      <td> 3141580.087165</td>
      <td> 1493784.330328</td>
      <td> 0</td>
      <td> 12734.864784</td>
      <td> 66652.371304</td>
      <td> 173224.117863</td>
      <td> 514585.559920</td>
      <td> 0</td>
      <td> 0</td>
      <td> 0.405365</td>
      <td> 0.405894</td>
      <td> 0.339459</td>
      <td> 0.430019</td>
      <td> 0.220557</td>
      <td> 0.370274</td>
      <td> 0.163798</td>
      <td> 0.344485</td>
      <td> 844</td>
      <td> 51.99810</td>
      <td> 72.4902</td>
      <td> 65.2612</td>
      <td>  4.04759</td>
      <td> 3374</td>
      <td> 10.170900</td>
      <td> 72.4902</td>
      <td> 57.6892</td>
      <td> 14.00040</td>
      <td> 16683</td>
      <td> 3.999510</td>
      <td> 72.4902</td>
      <td> 47.9097</td>
      <td> 17.4790</td>
      <td> 50326</td>
      <td>-0.056434</td>
      <td> 72.4902</td>
      <td> 42.0102</td>
      <td> 14.6979</td>
      <td> 160214</td>
      <td>-0.571724</td>
      <td> 81.3846</td>
      <td> 41.4149</td>
      <td> 19.7177</td>
      <td> 3944.617269</td>
      <td> 20031.300381</td>
      <td> 137884.372519</td>
      <td> 513698.265307</td>
      <td> 1783185.553199</td>
      <td> 0.502246</td>
      <td> 0.503571</td>
      <td> 0.637619</td>
      <td> 0.638452</td>
      <td> 0.702242</td>
      <td> 0.889583</td>
      <td> 0.654064</td>
      <td> 1.098051</td>
      <td> 0.567608</td>
      <td> 1.193737</td>
      <td> 0</td>
      <td> 0</td>
      <td> 0</td>
      <td>    0</td>
      <td> 3172</td>
      <td> 0</td>
      <td> 0</td>
      <td> 0</td>
      <td> 0</td>
      <td> 0</td>
      <td> 0</td>
      <td> 0</td>
      <td> 0</td>
      <td> 0</td>
      <td> 0</td>
      <td> 0</td>
      <td> 0</td>
      <td> 0</td>
      <td> 0</td>
      <td> 0</td>
      <td> 0</td>
      <td> 0</td>
      <td> 0</td>
      <td> 0</td>
      <td> 0</td>
      <td> 0</td>
      <td> 0</td>
      <td> 0</td>
      <td> 0</td>
      <td> 0</td>
      <td> 0</td>
      <td> 0</td>
      <td> 0</td>
      <td> 0</td>
      <td> 0</td>
      <td> 0</td>
      <td> 0</td>
      <td> 0</td>
      <td> 0</td>
      <td> 0</td>
      <td> 0</td>
      <td> 0</td>
      <td> 0</td>
      <td> 0</td>
      <td> 0</td>
      <td> 0</td>
      <td>    0</td>
      <td> 0</td>
      <td> 0</td>
      <td> 0</td>
      <td> 0</td>
      <td> 0</td>
      <td> 0</td>
      <td> 0</td>
      <td> 0</td>
      <td> 0</td>
      <td> 0</td>
      <td> 3172</td>
      <td> 0</td>
      <td> 0</td>
      <td> 292</td>
      <td>  292.0</td>
      <td> 6115.75</td>
      <td> 4777.50</td>
    </tr>
    <tr>
      <th>14</th>
      <td> 100015</td>
      <td> 913635.389577</td>
      <td> 123878.989169</td>
      <td>   71.497841</td>
      <td> 178.242903</td>
      <td> 343.741749</td>
      <td> 104.772485</td>
      <td> 7853.950217</td>
      <td> 7833.295299</td>
      <td> 31415.800871</td>
      <td> 31374.816076</td>
      <td> 196348.755450</td>
      <td> 156508.233075</td>
      <td> 785395.021798</td>
      <td> 462348.481404</td>
      <td> 3141580.087222</td>
      <td> 1498173.381821</td>
      <td> 0</td>
      <td>  9341.121986</td>
      <td> 58698.232576</td>
      <td> 163120.219838</td>
      <td> 501240.054546</td>
      <td> 0</td>
      <td> 0</td>
      <td> 0.297338</td>
      <td> 0.297727</td>
      <td> 0.298949</td>
      <td> 0.375049</td>
      <td> 0.207692</td>
      <td> 0.352808</td>
      <td> 0.159550</td>
      <td> 0.334567</td>
      <td> 847</td>
      <td> 61.99970</td>
      <td> 72.4002</td>
      <td> 68.7901</td>
      <td>  2.05102</td>
      <td> 3380</td>
      <td> 10.003700</td>
      <td> 72.4902</td>
      <td> 60.7596</td>
      <td> 11.53860</td>
      <td> 16844</td>
      <td> 2.000090</td>
      <td> 72.4902</td>
      <td> 47.2621</td>
      <td> 17.9120</td>
      <td> 49723</td>
      <td> 0.000003</td>
      <td> 72.4902</td>
      <td> 43.4479</td>
      <td> 14.5707</td>
      <td> 160688</td>
      <td>-0.571724</td>
      <td> 85.5132</td>
      <td> 42.9071</td>
      <td> 19.5329</td>
      <td> 8162.291023</td>
      <td> 41514.745679</td>
      <td> 169223.516688</td>
      <td> 541549.758361</td>
      <td> 1861304.776658</td>
      <td> 1.039259</td>
      <td> 1.042000</td>
      <td> 1.321461</td>
      <td> 1.323187</td>
      <td> 0.861852</td>
      <td> 1.081244</td>
      <td> 0.689525</td>
      <td> 1.171302</td>
      <td> 0.592474</td>
      <td> 1.242383</td>
      <td> 0</td>
      <td> 0</td>
      <td> 0</td>
      <td>    0</td>
      <td> 3172</td>
      <td> 0</td>
      <td> 0</td>
      <td> 0</td>
      <td> 0</td>
      <td> 0</td>
      <td> 0</td>
      <td> 0</td>
      <td> 0</td>
      <td> 0</td>
      <td> 0</td>
      <td> 0</td>
      <td> 0</td>
      <td> 0</td>
      <td> 0</td>
      <td> 0</td>
      <td> 0</td>
      <td> 0</td>
      <td> 0</td>
      <td> 0</td>
      <td> 0</td>
      <td> 0</td>
      <td> 0</td>
      <td> 0</td>
      <td> 0</td>
      <td> 0</td>
      <td> 0</td>
      <td> 0</td>
      <td> 0</td>
      <td> 0</td>
      <td> 0</td>
      <td> 0</td>
      <td> 0</td>
      <td> 0</td>
      <td> 0</td>
      <td> 0</td>
      <td> 0</td>
      <td> 0</td>
      <td> 0</td>
      <td> 0</td>
      <td> 0</td>
      <td> 0</td>
      <td>    0</td>
      <td> 0</td>
      <td> 0</td>
      <td> 0</td>
      <td> 0</td>
      <td> 0</td>
      <td> 0</td>
      <td> 0</td>
      <td> 0</td>
      <td> 0</td>
      <td> 0</td>
      <td> 3172</td>
      <td> 0</td>
      <td> 0</td>
      <td> 292</td>
      <td> 4454.0</td>
      <td> 4230.17</td>
      <td> 4777.50</td>
    </tr>
  </tbody>
</table>
</div>



#Using terminal convert the iPython Notebook to a Markdown file

	ipython nbconvert iPythonTest.ipynb --to markdown


    
