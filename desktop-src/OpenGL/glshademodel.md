---
title: fonction glShadeModel (GL. h)
description: La fonction glShadeModel sélectionne un ombrage plat ou lisse.
ms.assetid: 52985ad7-1d6c-48fc-8f1e-4eb2c0324c8e
keywords:
- glShadeModel fonction OpenGL
topic_type:
- apiref
api_name:
- glShadeModel
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 142ac518c91c6378f1606235e25502be8c06dd6a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "106510315"
---
# <a name="glshademodel-function"></a>glShadeModel fonction)

La fonction **glShadeModel** sélectionne un ombrage plat ou lisse.

## <a name="syntax"></a>Syntaxe


```C++
void WINAPI glShadeModel(
   GLenum mode
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*mode* 
</dt> <dd>

Valeur symbolique représentant une technique d’ombrage. Les valeurs acceptées sont \_ Flat GL et GL \_ Smooth. La valeur par défaut est lisse du GL \_ .

</dd> </dl>

## <a name="return-value"></a>Valeur renvoyée

Cette fonction ne retourne pas de valeur.

## <a name="error-codes"></a>Codes d’erreur

Les codes d’erreur suivants peuvent être récupérés par la fonction [**glGetError**](glgeterror.md) .



| Nom                                                                                                  | Signification                                                                                                                               |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**\_enum GL non valide \_**</dt> </dl>      | le *mode* est une valeur autre que GL \_ glat ou GL \_ Smooth.<br/>                                                                      |
| <dl> <dt>**\_opération non valide du GL \_**</dt> </dl> | La fonction a été appelée entre un appel à [**glBegin**](glbegin.md) et l’appel correspondant à [**glEnd**](glend.md).<br/> |



## <a name="remarks"></a>Notes

Les primitives OpenGL peuvent avoir un ombrage plat ou lissé. L’ombrage lissé, par défaut, entraîne l’interpolation des couleurs calculées des vertex lorsque la primitive est pixellisée, en affectant généralement des couleurs différentes à chaque fragment de pixel résultant. L’ombrage plat sélectionne la couleur calculée d’un seul vertex et l’attribue à tous les fragments de pixel générés par la pixellisation d’une seule primitive. Dans les deux cas, la couleur calculée d’un vertex est le résultat de l’éclairage, si l’éclairage est activé ou s’il s’agit de la couleur actuelle au moment de la spécification du vertex, si l’éclairage est désactivé.

L’ombrage plat et lisse ne peuvent pas être différenciés pour les points. En comptant les vertex et les primitives à partir d’un, en commençant à la sortie de [**glBegin**](glbegin.md) , *chaque segment de* ligne à ombrage plat reçoit la couleur calculée du sommet *i* + 1, son deuxième vertex. En comptant de la même manière, chaque polygone à ombrage constant reçoit la couleur calculée du vertex indiqué dans le tableau suivant. Il s’agit du dernier vertex pour spécifier le polygone dans tous les cas, à l’exception des polygones simples, où le premier vertex spécifie la couleur ombrée plate.



| Type primitif de polygone i | Sommet   |
|-----------------------------|----------|
| Polygone simple (*I*= 1)      | 1        |
| Bande triangulaire              | *i* + 2  |
| Ventilateur triangulaire                | *i* + 2  |
| Triangle indépendant        | 3 *I*     |
| Quadruple bande                  | 2 *i* + 2 |
| Quad indépendant            | 4 *I*     |



 

Les ombrages plats et lisses sont spécifiés par **glShadeModel** avec le *mode* défini sur GL \_ Flat et GL \_ Smooth, respectivement.

La fonction suivante récupère des informations relatives à **glShadeModel**:

[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) avec argument GL \_ Shade Shader \_ Model

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

[**glColor**](glcolor-functions.md)
</dt> <dt>

[**glEnd**](glend.md)
</dt> <dt>

[**glLight**](gllight-functions.md)
</dt> <dt>

[**glLightModel**](gllightmodel-functions.md)
</dt> </dl>

 

 





