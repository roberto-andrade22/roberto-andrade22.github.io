[Back to Portfolio](index)

---
## **Predicting the next items in a grocery ordering & delivering app: Instacart Market Basket Analysis**

### Summary

Given Instacart's open source dataset, 3 million Instacart Orders, in which there is information of millions of sales transactions that have been made through the app, it is of interest to try to determine if there are certain hidden patterns regarding consumer decisiones within the data.

This is how the data looks:




<div>
<table border="1" class="dataframe">
  <thead>
    <tr style="text-align: right;">
      <th></th>
      <th>order_id</th>
      <th>product_id</th>
      <th>add_to_cart_order</th>
      <th>product_name</th>
      <th>aisle_id</th>
      <th>department_id</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>0</th>
      <td>2</td>
      <td>33120</td>
      <td>1</td>
      <td>Organic Egg Whites</td>
      <td>86</td>
      <td>16</td>
    </tr>
    <tr>
      <th>1</th>
      <td>26</td>
      <td>33120</td>
      <td>5</td>
      <td>Organic Egg Whites</td>
      <td>86</td>
      <td>16</td>
    </tr>
    <tr>
      <th>2</th>
      <td>120</td>
      <td>33120</td>
      <td>13</td>
      <td>Organic Egg Whites</td>
      <td>86</td>
      <td>16</td>
    </tr>
    <tr>
      <th>3</th>
      <td>327</td>
      <td>33120</td>
      <td>5</td>
      <td>Organic Egg Whites</td>
      <td>86</td>
      <td>16</td>
    </tr>
    <tr>
      <th>4</th>
      <td>390</td>
      <td>33120</td>
      <td>28</td>
      <td>Organic Egg Whites</td>
      <td>86</td>
      <td>16</td>
    </tr>
  </tbody>
</table>
</div>



The project focused on <u>*association rules*</u> for departments. The objective was to deliver a set of rules such as if the client just added a product from the Dairy department, it's likely the next product will be from Bakery, for example. Making these suggestions would improve customer experience and increase sales.

This is how the recommendations would look:




<div>
<table border="1" class="dataframe">
  <thead>
    <tr style="text-align: right;">
      <th></th>
      <th>lift</th>
      <th>antecedents_name</th>
      <th>consequents_name</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>163</th>
      <td>1.601961</td>
      <td>[dairy eggs, deli]</td>
      <td>[snacks, produce]</td>
    </tr>
    <tr>
      <th>165</th>
      <td>1.569408</td>
      <td>[deli, produce]</td>
      <td>[dairy eggs, snacks]</td>
    </tr>
    <tr>
      <th>107</th>
      <td>1.490181</td>
      <td>[deli]</td>
      <td>[snacks, produce]</td>
    </tr>
    <tr>
      <th>145</th>
      <td>1.486045</td>
      <td>[dairy eggs, bakery]</td>
      <td>[snacks, produce]</td>
    </tr>
    <tr>
      <th>27</th>
      <td>1.476974</td>
      <td>[canned goods]</td>
      <td>[pantry]</td>
    </tr>
    <tr>
      <th>122</th>
      <td>1.418792</td>
      <td>[dairy eggs, bakery, produce]</td>
      <td>[frozen]</td>
    </tr>
    <tr>
      <th>135</th>
      <td>1.409875</td>
      <td>[dairy eggs, snacks, produce]</td>
      <td>[frozen]</td>
    </tr>
    <tr>
      <th>58</th>
      <td>1.407305</td>
      <td>[dairy eggs, deli]</td>
      <td>[frozen]</td>
    </tr>
    <tr>
      <th>161</th>
      <td>1.402527</td>
      <td>[dairy eggs, deli, produce]</td>
      <td>[snacks]</td>
    </tr>
  </tbody>
</table>
</div>



### References

* [Data](https://www.kaggle.com/competitions/instacart-market-basket-analysis/data)
* [Apriori Algorithm](https://www.vldb.org/conf/1994/P487.PDF)
* [Full Project](https://github.com/roberto-andrade22/instacart_basket)

---

[Back to Portfolio](index)
