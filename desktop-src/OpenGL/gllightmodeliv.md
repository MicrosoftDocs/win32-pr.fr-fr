---
title: fonction glLightModeliv (GL. h)
description: La fonction glLightModeliv définit les paramètres du modèle d’éclairage.
ms.assetid: 5998bb7e-d97a-47a0-b612-e6b0046aa5d2
keywords:
- glLightModeliv fonction OpenGL
topic_type:
- apiref
api_name:
- glLightModeliv
api_location:
- Opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: de61d53d3f4ceb9805ca5560c864379b18c65b3b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103743116"
---
# <a name="gllightmodeliv-function"></a>glLightModeliv fonction)

La fonction [**glLightModeliv**](gllightiv.md) définit les paramètres du modèle d’éclairage.

## <a name="syntax"></a>Syntaxe


```C++
void WINAPI glLightModeliv(
         GLenum pname,
   const GLint  *params
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*pname* 
</dt> <dd>

Paramètre de modèle d’éclairage. Les valeurs suivantes sont acceptées.



| Valeur                                                                                                                                                                                                      | Signification                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                 |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="GL_LIGHT_MODEL_AMBIENT"></span><span id="gl_light_model_ambient"></span><dl> <dt>**ambiant (GL \_ Light \_ Model) \_**</dt> </dl>                 | Le paramètre *params* contient quatre valeurs entières qui spécifient l’intensité de la RVBA ambiante de l’ensemble de la scène. Les valeurs entières sont mappées de façon linéaire de telle sorte que la valeur représentable la plus positive corresponde à 1,0, et la valeur représentable la plus négative correspond à-1,0. Les valeurs à virgule flottante sont mappées directement. Les valeurs entières et à virgule flottante ne sont pas ancrées. L’intensité de la scène ambiante par défaut est (0,2, 0,2, 0,2, 1,0). <br/>                                                                                                                                                                                                                                                                                                     |
| <span id="GL_LIGHT_MODEL_LOCAL_VIEWER"></span><span id="gl_light_model_local_viewer"></span><dl> <dt>**\_ \_ visionneuse locale du modèle de lumière \_ GL \_**</dt> </dl> | Le paramètre *params* est une valeur entière unique qui spécifie le mode de calcul des angles de réflexion spéculaire. Si *param* est égal à 0 (ou 0,0), les angles de réflexion spéculaire prennent le sens de la vue comme étant parallèle et dans la direction de l’axe-*z* , indépendamment de l’emplacement du vertex en coordonnées oculaires. Sinon, les réflexions spéculaires sont calculées à partir de l’origine du système de coordonnées oculaires. La valeur par défaut est 0. <br/>                                                                                                                                                                                                                                                                                                                |
| <span id="GL_LIGHT_MODEL_TWO_SIDE"></span><span id="gl_light_model_two_side"></span><dl> <dt>**\_ \_ côté 2 du modèle GL clair \_ \_**</dt> </dl>             | Le paramètre *params* est une valeur entière unique qui spécifie si les polygones doivent effectuer des calculs d’éclairage à un ou deux côtés. Elle n’a aucun effet sur les calculs d’éclairage pour les points, les lignes ou les bitmaps. Si *param* est égal à 0 (ou 0,0), un éclairage à un seul côté est spécifié et seuls les paramètres de matière première sont utilisés dans l’équation d’éclairage. Dans le cas contraire, l’éclairage à deux côtés est spécifié. <br/> Dans ce cas, les sommets des polygones de l’arrière-plan sont allumés à l’aide des paramètres de la matière arrière et les normales sont inversées avant l’évaluation de l’équation d’éclairage. Les sommets des polygones frontaux sont toujours éclaircis à l’aide des paramètres du matériau avant, sans aucune modification de leurs normales. La valeur par défaut est 0.<br/> |



 

</dd> <dt>

*params* 
</dt> <dd>

Pointeur vers la ou les valeurs dans lesquelles les *paramètres* seront définis.

</dd> </dl>

## <a name="return-value"></a>Valeur renvoyée

Cette fonction ne retourne pas de valeur.

## <a name="error-codes"></a>Codes d’erreur

Les codes d’erreur suivants peuvent être récupérés par la fonction [**glGetError**](glgeterror.md) .



| Nom                                                                                                  | Signification                                                                                                                               |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**\_enum GL non valide \_**</dt> </dl>      | *pname* n’est pas une valeur acceptée.<br/>                                                                                         |
| <dl> <dt>**\_opération non valide du GL \_**</dt> </dl> | La fonction a été appelée entre un appel à [**glBegin**](glbegin.md) et l’appel correspondant à [**glEnd**](glend.md).<br/> |



## <a name="remarks"></a>Notes

La fonction **glLightModeliv** définit le paramètre de modèle d’éclairage. Le paramètre *pname* nomme un paramètre et *param* donne la nouvelle valeur. la ou les valeurs des paramètres de la source lumineuse individuelle.

En mode RVBA, la couleur éclaircie d’un vertex est égale à la somme de l’intensité de l’émission du matériau, du produit de la réflectivité ambiante du matériau et de l’intensité ambiante du modèle d’éclairage de la scène, ainsi que de la contribution de chaque source de lumière activée. Chaque source de lumière contribue à la somme de trois termes : ambiant, diffuse et spéculaire.

-   La contribution source de la lumière ambiante est le produit de la réflexion ambiante du matériau et de l’intensité ambiante de la lumière.
-   La contribution à la source de lumière diffuse est le produit de la réflexion diffuse de matériau, l’intensité diffuse de la lumière et le produit scalaire du vertex normal avec le vecteur normalisé du vertex à la source de lumière.
-   La contribution à la source de lumière spéculaire est le produit de la réflexion spéculaire, de l’intensité spéculaire de la lumière et du produit scalaire des vecteurs de vertex à oculaire normalisés et de sommets à la lumière, élevé à la puissance de la brillance du matériau.

Les trois contributions à la source lumineuse sont atténuées de manière égale en fonction de la distance entre le sommet et la source de lumière, et de la direction de la source de lumière, de la répartition de l’exposant et de l’angle de coupure. Tous les produits scalaires sont remplacés par zéro s’ils correspondent à une valeur négative.

Le composant alpha de la couleur éclaircie résultante est défini sur la valeur alpha de la réflexion de diffusion matérielle.

En mode d’index des couleurs, la valeur de l’index clair d’un vertex est comprise entre l’ambiant et les valeurs spéculaires transmises à [**glMaterial**](glmaterial-functions.md) à l’aide d' \_ index de couleur GL \_ . Coefficients diffus et spéculaire, calculés avec une pondération (. 30,. 59, .11) des couleurs de la lumière, la brillance du matériau et les mêmes équations de réflexion et d’atténuation que dans le cas RVBA, déterminez le degré au-dessus de l’index résultant.

Les fonctions suivantes récupèrent les informations relatives à la fonction **glLightModeliv** :

[](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) \_ \_ \_ visionneuse locale glGet avec argument GL Light Model \_

[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) avec argument GL \_ Light \_ Model \_ deux \_ côtés

[**glIsEnabled**](glisenabled.md) avec argument GL \_ Lighting

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows 2000 Professionnel - \[Applications de bureau uniquement\]<br/>                              |
| Serveur minimal pris en charge<br/> | Windows 2000 Server - \[Applications de bureau uniquement\]<br/>                                    |
| En-tête<br/>                   | <dl> <dt>GL. h</dt> </dl>         |
| Bibliothèque<br/>                  | <dl> <dt>Opengl32. lib</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Opengl32.dll</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**glBegin**](glbegin.md)
</dt> <dt>

[**glEnd**](glend.md)
</dt> <dt>

[**glLight**](gllight-functions.md)
</dt> <dt>

[**glMaterial**](glmaterial-functions.md)
</dt> </dl>

 

 





