#Apêndice A

Tabela 1 - coordenadas de cada ponto
| Ponto | x | y | z |
| --- | ---: | ---: | ---: |
| $P_0$ | 0 | 0 | 0 |
| $P_1$ | 2 | 2 | 0 |
| $P_2$ | -2 | 2 | 0 |
| $P_3$ | 1.5 | 2.5 | 0 |
| $P_4$ | -1.5 | 2.5 | 0 |
| $P_5$ | -2 | -2 | 0 |
| $P_6$ | 2 | -2 | 0 |

---------------------------------------------------------------------------------------------------------------------------------------------------
# 1. Equações do arco na boca do copo
$\vec{A}_{Boca}X(t)$ = $X_0 + Rcos((\frac{απ}{180}) + (\frac{βπt}{180})$ = $0 + 4cos((\frac{45π}{180})+(\frac{90πt}{180}))$

$\vec{A}_{Boca}Y(t)$ = $Y_0 + Rsen((\frac{απ}{180}) + (\frac{βπt}{180})$ = $0 + 4sen((\frac{45π}{180})+(\frac{90πt}{180}))$

$\vec{A}_{Boca}Z(t)$ = $Z_0 + 12$ =12

---------------------------------------------------------------------------------------------------------------------------------------------------
# 2. Equações da base do copo
## 2.1. Curva inicial
$\vec{B}_{Base1}X(t)$ = $X_1 * t^3 + 3 * X_3 * t^2 * (1 - t) + 3 * X_4 * t * (1 - t)^2 + X_2 * (1 - t)^3$ = $2 * t^3 + 3 * 1.5t^2 * (1-t) + 3 * (-1.5) * t * (1-t)^2 + (-2) * (1-t)^3$

$\vec{B}_{Base1}Y(t)$ = $Y_1 * t^3 + 3 * Y_3 * t^2 * (1 - t) + 3 * Y_4 * t * (1 - t)^2 + Y_2 * (1 - t)^3$ = $2 * t^3 + 3 * 2.5 * t^2 * (1-t) + 3 * 2.5 * t * (1-t)^2 + 2 * (1-t)^3$

$\vec{B}_{Base1}Z(t)$ = $Z_1 * t^3 + 3 * Z_3 * t^2 * (1 - t) + 3 * Z_4 * t * (1 - t)^2 + Z_2 * (1 - t)^3$ = $0 * t^3 + 3 * 0 * t^2 * (1-t) + 3 * 0 * t * (1-t)^2 + 0 * (1-t)^3$ = 0

## 2.2. Curvas criadas por transformações geométricas

### 2.2.1. Rotação

$\vec{B}_{Base2}X(t)$ = $cos(\frac{90π}{180}) * \vec{B} _{Base1}X(t) - sen(\frac{90π}{180}) * \vec{B} _{Base1}Y(t)$ 

$\vec{B}_{Base2}Y(t)$ = $sen(\frac{90π}{180}) * \vec{B} _{Base1}X(t) + cos(\frac{90π}{180}) * \vec{B} _{Base1}Y(t)$

$\vec{B}_{Base2}Z(t)$ = $\vec{B} _{Base1}Z(t)$

### 2.2.2. Espelhamento

$\vec{B}_{Base3}X(t)$ = $\vec{B} _{Base1} * X(t)$ 

$\vec{B}_{Base3}Y(t)$ = $\vec{B} _{Base1}Y(t) * (-1)$

$\vec{B}_{Base3}Z(t)$ = $\vec{B} _{Base1}Z(t)$

### 2.2.3. Rotação + Espelhamento

$\vec{B}_{Base4}X(t)$ = $\vec{B} _{Base2}X(t) * (-1)$ 

$\vec{B}_{Base4}Y(t)$ = $\vec{B} _{Base2}Y(t)$

$\vec{B}_{Base4}Z(t)$ = $\vec{B} _{Base1}Z(t)$

## 2.3. Limite da superfície

$\vec{B}_{LimBase1}X(t)$ = $X_5 * t + X_2 * (1 - t)$ = $-2 * t - 2 * (1 - t)$

$\vec{B}_{LimBase1}Y(t)$ = $Y_5 * t + Y_2 * (1 - t)$ = $-2 * t + 2 * (1 - t)$

---------------------------------------------------------------------------------------------------------------------------------------------------
# 3. Funções de várias variáveis
## 3.1. Funções para a base 1

$\vec{P}_{SupBase1}X(t,u)$ = $(1 - u) * \vec{B} _{Base3}X(t) + u * \vec{B} _{Base1}X(t)$

$\vec{P}_{SupBase1}Y(t,u)$ = $(1 - u) * \vec{B} _{Base3}Y(t) + u * \vec{B} _{Base1}Y(t)$

$\vec{P}_{SupBase1}Z(t,u)$ = $(1 - u) * \vec{B} _{Base3}Z(t) + u * \vec{B} _{Base1}Z(t)$

## 3.2. Funções para a base 2
$\vec{P}_{SupBase2}X(t,u)$ = $(1 - u) * \vec{B} _{Base2}X(t) + u * \vec{B} _{LimBase1}X(t)$

$\vec{P}_{SupBase2}Y(t,u)$ = $(1 - u) * \vec{B} _{Base2}Y(t) + u * \vec{B} _{Base4}Y(t)$

$\vec{P}_{SupBase2}Z(t,u)$ = $(1 - u) * \vec{B} _{Base2}Z(t) + u * \vec{B} _{Base4}Z(t)$

## 3.3. Funções para a base 3
$\vec{P}_{SupBase3}X(t,u)$ = $(1 - u) * (- \vec{B} _{LimBase1}X(t)) + u * \vec{B} _{Base4}X(t)$

$\vec{P}_{SupBase3}Y(t,u)$ = $(1 - u) * (- \vec{B} _{LimBase1}Y(t)) + u * \vec{B} _{Base4}Y(t)$

## 3.4. Funções para superfície do copo
$\vec{P}_{SupCorp}X(t,u)$ = $(1 - u) * \vec{A} _{Boca}X(t) - u * \vec{B} _{Base1}X(t)$

$\vec{P}_{SupCorp}Y(t,u)$ = $(1 - u) * \vec{A} _{Boca}Y(t) + u * \vec{B} _{Base1}Y(t)$

$\vec{P}_{SupCorp}Z(t,u)$ = $(1 - u) * \vec{A} _{Boca}Z(t) + u * \vec{B} _{Base1}Z(t)$

---------------------------------------------------------------------------------------------------------------------------------------------------
# 4. Criação das superfícies
## 4.1. Superfícies da base
$\vec{P}_{BaseExt1}(u,v)$ = $Superfície(\vec{B} _{Base1}X(t,u), \vec{B} _{Base1}Y(t,u), \vec{B} _{Base1}Z(t,u), u, 0, 1, v, 0, 1)$

$\vec{P}_{BaseExt2}(u,v)$ = $Superfície(\vec{B} _{Base2}X(t,u), \vec{B} _{Base2}Y(t,u), \vec{B} _{Base2}Z(t,u), u, 0, 1, v, 0, 1)$

$\vec{P}_{BaseExt3}(u,v)$ = $Superfície(\vec{B} _{Base3}X(t,u), \vec{B} _{Base3}Y(t,u), \vec{B} _{Base3}Z(t,u), u, 0, 1, v, 0, 1)$

## 4.2. Superfície do corpo

### 4.2.1. Superfície do corpo inicial

$\vec{P}_{CorpoExt1}(t,u)$ = $Superfície(\vec{B} _{Sup}X(t,u),\vec{B} _{Sup}Y(t,u), \vec{B} _{Sup}Z(t,u), t,0,1,u,0,1)$

### 4.2.2. Superfícies do corpo por transformações geométricas

#### Espelhamento

$\vec{P}_{CorpoExt2}(t,u)$ = $Superfície(\vec{B} _{Sup}X(t,u),\vec{B} _{Sup}Y(t,u) * (-1), \vec{B} _{Sup}Z(t,u), t,0,1,u,0,1)$

#### Rotação

$\vec{P}_{CorpoExt3}(t,u)$ = $Superfície(cos(\frac{90π}{180}) * \vec{B} _{Sup}X(t,u) - sen(\frac{90π}{180}) * \vec{B} _{Sup}Y(t,u),sen(\frac{90π}{180}) * \vec{B} _{Sup}X(t,u) + cos(\frac{90π}{180}) * \vec{B} _{Sup}Y(t,u), \vec{B} _{Sup}Z(t,u), t,0,1,u,0,1)$

#### Espelhamento + Rotação

$\vec{P}_{CorpoExt4}(t,u)$ = $Superfície((cos(\frac{90π}{180}) * \vec{B} _{Sup}X(t,u) - sen(\frac{90π}{180}) * \vec{B} _{Sup}Y(t,u)) * (-1), sen(\frac{90π}{180}) * \vec{B} _{Sup}X(t,u) + cos(\frac{90π}{180}) * \vec{B} _{Sup}Y(t,u), \vec{B} _{Sup}Z(t,u), t,0,1,u,0,1)$
