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
## 1. Definindo as equações do arco na boca do copo
$\vec{A}_{Boca}X(t)$ =  0 + 4 * $cos((45 * π/180)+(90 * π * t/180))$

$\vec{A}_{Boca}Y(t)$ =  0 + 4 * $sen((45 * π/180)+(90 * π * t/180))$

$\vec{A}_{Boca}Z(t)$ = 12

---------------------------------------------------------------------------------------------------------------------------------------------------
## 2. Definindo as equações da base do copo
## 2.1. Curva 1
$\vec{B}_{Base1}X(t)$ =  $2 * t^3 + 3 * 1.5 * t^2 * (1-t) + 3 * (-1.5) * t * (1-t)^2 + (-2) * (1-t)^3$

$\vec{B}_{Base1}Y(t)$ =  $2 * t^3 + 3 * 2.5 * t^2 * (1-t) + 3 * 2.5 * t * (1-t)^2 + 2 * (1-t)^3$

$\vec{B}_{Base1}Z(t)$ =  $0 * t^3 + 3 * 0 * t^2 * (1-t) + 3 * 0 * t * (1-t)^2 + 0 * (1-t)^3$ = 0

## 2.2. Curva 2

$\vec{B}_{Base2}X(t)$ = $cos(90 * \frac{π}{180}) * \vec{B} _{Base1}X(t) - sen(90 * \frac{π}{180}) * \vec{B} _{Base1}Y(t)$ 

$\vec{B}_{Base2}Y(t)$ = $sen(90 * \frac{π}{180}) * \vec{B} _{Base1}X(t) + cos(90 * \frac{π}{180}) * \vec{B} _{Base1}Y(t)$

$\vec{B}_{Base2}Z(t)$ = $\vec{B} _{Base1}Z(t)$

## 2.3. Curva 3

$\vec{B}_{Base3}X(t)$ = $\vec{B} _{Base1}X(t)$ 

$\vec{B}_{Base3}Y(t)$ = $\vec{B} _{Base1}Y(t) * (-1)$

$\vec{B}_{Base3}Z(t)$ = $\vec{B} _{Base1}Z(t)$

## 2.4. Curva 4

$\vec{B}_{Base4}X(t)$ = $\vec{B} _{Base2}X(t) * (-1)$ 

$\vec{B}_{Base4}Y(t)$ = $\vec{B} _{Base2}Y(t)$

$\vec{B}_{Base4}Z(t)$ = $\vec{B} _{Base1}Z(t)$

## 2.5. Limite da superfície

$\vec{B}_{LimBase1}X(t)$ = $X_5 * t + X_2 * (1 - t)$ = $-2 * t - 2 * (1 - t)$

$\vec{B}_{LimBase1}Y(t)$ = $Y_5 * t + Y_2 * (1 - t)$ = $-2 * t + 2 * (1 - t)$

---------------------------------------------------------------------------------------------------------------------------------------------------
## 3. Funções de várias variáveis
## 3.1. Base 1

$\vec{B}_{Base1}X(u,t)$ = $(1 - u) * \vec{B} _{Base3}X(t) + u * \vec{B} _{Base1}X(t)$

$\vec{B}_{Base1}Y(u,t)$ = $(1 - u) * \vec{B} _{Base3}Y(t) + u * \vec{B} _{Base1}Y(t)$

$\vec{B}_{Base1}Z(u,t)$ = $(1 - u) * \vec{B} _{Base3}Z(t) + u * \vec{B} _{Base1}Z(t)$

## 3.2. Base 2
$\vec{B}_{Base2}X(u,t)$ = $(1 - u) * \vec{B} _{Base2}X(t) + u * \vec{B} _{LimBase1}X(t)$

$\vec{B}_{Base2}Y(u,t)$ = $(1 - u) * \vec{B} _{Base2}Y(t) + u * \vec{B} _{Base4}Y(t)$

$\vec{B}_{Base2}Z(u,t)$ = $(1 - u) * \vec{B} _{Base2}Z(t) + u * \vec{B} _{Base4}Z(t)$

## 3.3. Base 3
$\vec{B}_{Base3}X(u,t)$ = $(1 - u) * (- \vec{B} _{LimBase1}X(t)) + u * \vec{B} _{Base4}X(t)$

$\vec{B}_{Base3}Y(u,t)$ = $(1 - u) * (- \vec{B} _{LimBase1}Y(t)) + u * \vec{B} _{Base4}Y(t)$

## 3.4. Curvas do corpo
$\vec{B}_{Sup}X(u,t)$ = $(1 - u) * \vec{A} _{Boca}X(t) - u * \vec{B} _{Base1}X(t)$

$\vec{B}_{Sup}Y(u,t)$ = $(1 - u) * \vec{A} _{Boca}Y(t) + u * \vec{B} _{Base1}Y(t)$

$\vec{B}_{Sup}Z(u,t)$ = $(1 - u) * \vec{A} _{Boca}Z(t) + u * \vec{B} _{Base1}Z(t)$

---------------------------------------------------------------------------------------------------------------------------------------------------
## 4. Criação das superfícies
$\vec{P}_{BaseExt1}(u,v)$ = $Superfície(\vec{B} _{Base1}X(u,t), \vec{B} _{Base1}Y(u,t), \vec{B} _{Base1}Z(u,t), u, 0, 1, v, 0, 1)$

$\vec{P}_{BaseExt2}(u,v)$ = $Superfície(\vec{B} _{Base2}X(u,t), \vec{B} _{Base2}Y(u,t), \vec{B} _{Base2}Z(u,t), u, 0, 1, v, 0, 1)$

$\vec{P}_{BaseExt3}(u,v)$ = $Superfície(\vec{B} _{Base3}X(u,t), \vec{B} _{Base3}Y(u,t), \vec{B} _{Base3}Z(u,t), u, 0, 1, v, 0, 1)$

$\vec{P}_{CorpoExt1}(u,v)$ = $Superfície(\vec{B} _{Sup}X(u,t),\vec{B} _{Sup}Y(u,t), \vec{B} _{Sup}Z(u,t), t,0,1,u,0,1)$

$\vec{P}_{CorpoExt2}(u,v)$ = $Superfície(\vec{B} _{Sup}X(u,t),\vec{B} _{Sup}Y(u,t) * (-1), \vec{B} _{Sup}Z(u,t), t,0,1,u,0,1)$

$\vec{P}_{CorpoExt3}(u,v)$ = $Superfície(cos(90 * \frac{π}{180}) * \vec{B} _{Sup}X(u,t) - sen(90 * \frac{π}{180}) * \vec{B} _{Sup}Y(u,t),sen(90 * \frac{π}{180}) * \vec{B} _{Sup}X(u,t) + cos(90 * \frac{π}{180}) * \vec{B} _{Sup}Y(u,t), \vec{B} _{Sup}Z(u,t), t,0,1,u,0,1)$

$\vec{P}_{CorpoExt4}(u,v)$ = $Superfície((cos(90 * \frac{π}{180}) * \vec{B} _{Sup}X(u,t) - sen(90 * \frac{π}{180}) * \vec{B} _{Sup}Y(u,t)) * (-1) ,sen(90 * \frac{π}{180}) * \vec{B} _{Sup}X(u,t) + cos(90 * \frac{π}{180}) * \vec{B} _{Sup}Y(u,t), \vec{B} _{Sup}Z(u,t), t,0,1,u,0,1)$
