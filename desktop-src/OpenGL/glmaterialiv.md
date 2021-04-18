---
title: fonction glMaterialiv (GL. h)
description: La fonction glMaterialiv spécifie les paramètres de matériau pour le modèle d’éclairage.
ms.assetid: 9d045202-e565-4cf7-946a-60299e1bc1b1
keywords:
- glMaterialfv fonction OpenGL
topic_type:
- apiref
api_name:
- glMaterialfv
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 95f12a5d34357a3436ffd6725ad2f1d56901e700
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104384467"
---
# <a name="glmaterialiv-function"></a>glMaterialiv fonction)

La fonction **glMaterialiv** spécifie les paramètres de matériau pour le modèle d’éclairage.

## <a name="syntax"></a>Syntaxe


```C++
void WINAPI glMaterialfv(
         GLenum face,
         GLenum pname,
   const GLint  *params
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*se* 
</dt> <dd>

Face ou faces mises à jour. Il doit s’agir de l’une des valeurs suivantes : recto GL, arrière-plan GL, arrière- \_ \_ plan GL \_ et GL \_ .

</dd> <dt>

*pname* 
</dt> <dd>

Paramètre Material de la face ou des visages en cours de mise à jour. Les paramètres qui peuvent être spécifiés à l’aide de [**glMaterialiv**](glmaterialfv.md)et leurs interprétations par l’équation d’éclairage sont les suivants.



| Valeur                                                                                                                                                                                      | Signification                                                                                                                                                                                                                                                                                                                                                                                                                                                                                        |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="GL_AMBIENT"></span><span id="gl_ambient"></span><dl> <dt>**ambiant du GL \_**</dt> </dl>                                       | Le paramètre params contient quatre valeurs entières qui spécifient la réflectivité RVBA ambiante du matériau. Les valeurs entières sont mappées de façon linéaire de telle sorte que la valeur représentable la plus positive corresponde à 1,0, et la valeur représentable la plus négative correspond à-1,0. Les valeurs à virgule flottante sont mappées directement. Les valeurs entières et à virgule flottante ne sont pas ancrées. La réflectivité ambiante par défaut pour les matériaux frontaux et à face arrière est (0,2, 0,2, 0,2, 1,0). <br/>    |
| <span id="GL_DIFFUSE"></span><span id="gl_diffuse"></span><dl> <dt>**\_diffusion GL**</dt> </dl>                                       | Le paramètre params contient quatre valeurs entières qui spécifient la réflexion RVBA diffuse du matériau. Les valeurs entières sont mappées de façon linéaire de telle sorte que la valeur représentable la plus positive corresponde à 1,0, et la valeur représentable la plus négative correspond à-1,0. Les valeurs à virgule flottante sont mappées directement. Les valeurs entières et à virgule flottante ne sont pas ancrées. La réflectivité diffuse par défaut pour les matériaux avant et arrière est (0,8, 0,8, 0,8, 1,0). <br/>    |
| <span id="GL_SPECULAR"></span><span id="gl_specular"></span><dl> <dt>**\_spéculaire GL**</dt> </dl>                                    | Le paramètre params contient quatre valeurs entières qui spécifient la réflexion RVBA spéculaire du matériau. Les valeurs entières sont mappées de façon linéaire de telle sorte que la valeur représentable la plus positive corresponde à 1,0, et la valeur représentable la plus négative correspond à-1,0. Les valeurs à virgule flottante sont mappées directement. Les valeurs entières et à virgule flottante ne sont pas ancrées. La réflectivité spéculaire par défaut pour les matériaux avant et arrière est (0,0, 0,0, 0,0, 1,0). <br/>  |
| <span id="GL_EMISSION"></span><span id="gl_emission"></span><dl> <dt>**\_émission GL**</dt> </dl>                                    | Le paramètre params contient quatre valeurs entières qui spécifient l’intensité de la lumière émise par le RVBA du matériau. Les valeurs entières sont mappées de façon linéaire de telle sorte que la valeur représentable la plus positive corresponde à 1,0, et la valeur représentable la plus négative correspond à-1,0. Les valeurs à virgule flottante sont mappées directement. Les valeurs entières et à virgule flottante ne sont pas ancrées. L’intensité d’émission par défaut pour les matériaux frontaux et à face arrière est (0,0, 0,0, 0,0, 1,0). <br/> |
| <span id="GL_SHININESS"></span><span id="gl_shininess"></span><dl> <dt>**\_éclat GL**</dt> </dl>                                 | Le paramètre *param* est un entier unique qui spécifie l’exposant spéculaire RVBA du matériau. Les valeurs entières sont mappées directement. Seules les valeurs de la plage \[ 0, 128 \] sont acceptées. L’exposant spéculaire par défaut pour les matériaux frontaux et à face arrière est 0. <br/>                                                                                                                                                                                                     |
| <span id="GL_AMBIENT_AND_DIFFUSE"></span><span id="gl_ambient_and_diffuse"></span><dl> <dt>**\_ambiants \_ et \_ DIFFUSes du GL**</dt> </dl> | Équivalent à l’appel de [**glMaterial**](glmaterial-functions.md) à deux reprises avec les mêmes valeurs de paramètres, une fois avec le GL \_ ambiant et une fois avec la \_ diffusion GL. <br/>                                                                                                                                                                                                                                                                                                                            |
| <span id="GL_COLOR_INDEXES"></span><span id="gl_color_indexes"></span><dl> <dt>**\_index de couleurs GL \_**</dt> </dl>                    | Le paramètre params contient trois valeurs entières spécifiant les index de couleurs pour l’éclairage ambiant, diffus et spéculaire. Ces trois valeurs, et la \_ brillance GL, sont les seules valeurs de matériau utilisées par l’équation d’éclairage du mode d’index des couleurs. Reportez-vous à [**glLightModel**](gllightmodel-functions.md) pour une discussion sur l’éclairage d’index de couleurs.<br/>                                                                                                                                  |



 

</dd> <dt>

*params* 
</dt> <dd>

Valeur à laquelle définir la brillance du GL de paramètres \_ .

</dd> </dl>

## <a name="return-value"></a>Valeur renvoyée

Cette fonction ne retourne pas de valeur.

## <a name="error-codes"></a>Codes d’erreur

Les codes d’erreur suivants peuvent être récupérés par la fonction [**glGetError**](glgeterror.md) .



| Nom                                                                                              | Signification                                                                       |
|---------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------|
| <dl> <dt>**\_enum GL non valide \_**</dt> </dl>  | L’une des *visages* ou l' *pname* n’était pas une valeur acceptée.<br/>                |
| <dl> <dt>**\_valeur non valide du GL \_**</dt> </dl> | Un exposant spéculaire en dehors de la plage comprise entre \[ 0 et 128 \] a été spécifié.<br/> |



## <a name="remarks"></a>Notes

La fonction [**glMaterialiv**](glmaterialf.md) affecte des valeurs aux paramètres de la documentation. Il existe deux ensembles de paramètres de matériau correspondants. L’un, le jeu de face *avant* , est utilisé pour ombrer des points, des lignes, des bitmaps et tous les polygones (lorsque l’éclairage à deux côtés est désactivé), ou simplement des polygones frontaux (lorsque l’éclairage à deux côtés est activé). L’autre jeu, *arrière-plan*, est utilisé pour ombrer les polygones de l’arrière-plan uniquement lorsque l’éclairage à deux côtés est activé. Reportez-vous à [**glLightModel**](gllightmodel-functions.md) pour plus d’informations sur les calculs d’éclairage unilatéraux et à deux côtés.

La fonction [**glMaterialiv**](glmaterialf.md) accepte trois arguments. La première, *face*, spécifie si les documents \_ frontaux, les \_ documents de retour GL, ou \_ les \_ documents frontaux et Back GL \_ sont modifiés. Le deuxième, *pname*, spécifie quels paramètres dans un ou les deux jeux seront modifiés. Le troisième, *param*, spécifie la valeur qui sera assignée au paramètre spécifié.

Les paramètres de matériau sont utilisés dans l’équation d’éclairage qui est éventuellement appliquée à chaque vertex. L’équation est présentée dans [**glLightModel**](gllightmodel-functions.md).

Les paramètres de matériau peuvent être mis à jour à tout moment. En particulier, [**glMaterialiv**](glmaterialf.md) peut être appelé entre un appel à [**glBegin**](glbegin.md) et l’appel correspondant à [**glEnd**](glend.md). Toutefois, si un seul paramètre de matériau doit être modifié par vertex, [**glColorMaterial**](glcolormaterial.md) est préférable à **glMaterialiv**.

La fonction suivante récupère des informations relatives à [**glMaterialiv**](glmaterialf.md):

[**glGetMaterial**](glgetmaterial.md)

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

[**glColorMaterial**](glcolormaterial.md)
</dt> <dt>

[**glLight**](gllight-functions.md)
</dt> <dt>

[**glLightModel**](gllightmodel-functions.md)
</dt> </dl>

 

 





