<h1 align="center">Preparación de los datos</h1>


## Definir el problema: Clasificación o Regresión




## Selección del conjunto de validación




## Preprocesamiento

<table>
  <tr>
    <tD></tD>
    <tD>
      <h4>Tree based models</h4>
      <ul>
        <li>Decission Tree</li>
        <li>Random Forest</li>
        <li>Extra Trees</li>
        <li>Adaboost</li>
        <li>Gradient Boosting</li>
        <li>XGBoost</li>
        <li>LightGBM</li>
        <li>CatBoost</li>
      </ul>
    </tD>
    <td>
      <h4>No-tree based models</h4>
      <ul>
        <li>Linear Models</li>
        <li>Neural Networks</li>
        <li>K-Nearest Neighbors</li>
        <li>Suport Vector Machines</li>
      </ul>
    </td>
  </tr>
  <tr>
    <th>Categorical<br>Ordinal</th>
    <td>
      <ul>
        <li><b>Ordinal encoding</b></li>
        <li>Other: Frequency encoding</li>
      </ul>
    </td>
    <td>
      <ul>
        <li><b>One hot encoding</b></li>
        <li>Other: Embedding</li>
      </ul>
    </td>
  </tr>
  <tr>
    <th>Numerical</th>
    <td><b>Nothing</b></td>
    <td>
      <ul>
        <li>MinMaxScaler</li>
        <li><b>StandarScaler</b></li>
        <li>Skewed?
          <ul>
            <li>np.log(1+x)</li>
            <li>np.sqrt(x+2/3)</li>
            <li>Box-Cox</li>
          </ul>
        </li>
      </ul>
    </td>
  </tr>
</table>



### [Map data to a normal distribution](https://scikit-learn.org/stable/auto_examples/preprocessing/plot_map_data_to_normal.html): Box-Cox
A Box Cox transformation is a generic way to transform non-normal variables into a **normal shape**.

| Lambda value (λ) | Transformed data |
|------------------|------------------|
| -3               | Y⁻³ = 1/Y³       |
| -2               | Y⁻² = 1/Y²       |
| -1               | Y⁻¹ = 1/Y¹       |
| -0.5             | Y⁻⁰·⁵ = 1/√Y      |
| 0                | log(Y)           |
| 0.5              | Y⁰·⁵ = √Y         |
| 1                | Y¹               |
| 2                | Y²               |
| 3                | Y³               |


## Categorical features

| Ordinal Encoding o Label Encoding    | One-Hot Encoding        |
|--------------------------------------|-------------------------|
| ![](img/enc-ord.png)                 | ![](img/enc-onehot.png) |

> ## Target Encoding o Mean Encoding
> ![](img/enc-target.png)

## Models

| Model                 | Comment                              | Library                    | More info |
|:---------------------:|--------------------------------------|----------------------------|-----------|
| **Decission Tree**    | Simple and explicable.               | Sklearn                    |           |
| **Linear models**     | Simple and explicable.               | Sklearn                    |           |
| **Random Forest**     | Good starting point (tree enesemble) | Sklearn                    |           |
| **Gradient Boosting** | Usually the best (tree enesemble)    | XGBoost, LighGBM, Catboost |           |
| **Neural Network**    | Good if lot of data.                 | Fast.ai v2                 | [blog](https://hackernoon.com/gain-state-of-the-art-results-on-tabular-data-with-deep-learning-and-embedding-layers-a-how-to-guide-r17b36k8) |





## Ingeniería de características = CREATIVIDAD + CONOCIMIENTO DEL DOMINIO

- Si tienes el precio de la casa y los metros cuadrados, puedes añadir el precio del metro cuadrado.
- Si tines la distancia en el eje x e y, puedes añadir la distancia directa por pitagoras.
- Si tines precios, puedes añanir la parte fraccionaria pq es muy subjetiva en la gente.
