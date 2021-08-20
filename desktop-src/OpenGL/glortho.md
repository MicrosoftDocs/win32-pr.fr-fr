---
title: fonction glOrtho (GL. h)
description: La fonction glOrtho multiplie la matrice actuelle par une matrice orthographique.
ms.assetid: 5c70819f-e9b6-49e2-add5-9f6e6aba26ee
keywords:
- glOrtho fonction OpenGL
topic_type:
- apiref
api_name:
- glOrtho
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b1e06c1740e908c34652a6d39bc7a2334763199d222ff9d1dc00ae733803ada0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117795220"
---
# <a name="glortho-function"></a>glOrtho fonction)

La fonction **glOrtho** multiplie la matrice actuelle par une matrice orthographique.

## <a name="syntax"></a>Syntaxe


```C++
void WINAPI glOrtho(
   GLdouble left,
   GLdouble right,
   GLdouble bottom,
   GLdouble top,
   GLdouble zNear,
   GLdouble zFar
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*gauche* 
</dt> <dd>

Coordonnées du plan de découpage vertical gauche.

</dd> <dt>

*Oui* 
</dt> <dd>

Coordonnées du plan de découpage vertical theright.

</dd> <dt>

*ballon* 
</dt> <dd>

Coordonnées du plan de découpage horizontal inférieur.

</dd> <dt>

*top* 
</dt> <dd>

Coordonnées des plans de découpage horizontal supérieurs.

</dd> <dt>

*zNear* 
</dt> <dd>

Distances avec le plan de découpage de profondeur le plus proche. Cette distance est négative si le plan doit être placé derrière la visionneuse.

</dd> <dt>

*zFar* 
</dt> <dd>

Distances avec le plan de découpage de profondeur le plus éloigné. Cette distance est négative si le plan doit être placé derrière la visionneuse.

</dd> </dl>

## <a name="return-value"></a>Valeur renvoyée

Cette fonction ne retourne pas de valeur.

## <a name="error-codes"></a>Codes d’erreur

Le code d’erreur suivant peut être récupéré par la fonction [**glGetError**](glgeterror.md) .



| Nom                                                                                                  | Signification                                                                                                                               |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**\_opération non valide du GL \_**</dt> </dl> | La fonction a été appelée entre un appel à [**glBegin**](glbegin.md) et l’appel correspondant à [**glEnd**](glend.md).<br/> |



## <a name="remarks"></a>Remarques

La fonction **glOrtho** décrit une matrice de perspective qui produit une projection parallèle. Les paramètres (*gauche*, *bas*, *proche*) et (*droite*, *haut*, *near*) spécifient les points sur le plan de découpage proche qui sont mappés aux angles inférieur gauche et supérieur droit de la fenêtre, respectivement, en supposant que l’œil se trouve à (0, 0,0). Le paramètre *Far* spécifie l’emplacement du plan de découpage Far. *ZNear* et *zFar* peuvent être positifs ou négatifs. La matrice correspondante est présentée dans l’image suivante.

![Diagramme montrant la matrice de perspective décrite par la fonction glOrtho.](images/ortho1.png)

where

![Équations décrivant la matrice de perspective.](images/ortho2.png)

La matrice actuelle est multipliée par cette matrice avec le résultat qui remplace la matrice actuelle. Autrement dit, si M est la matrice active et O est la matrice ortho, M est remplacé par M O.

Utilisez [**glPushMatrix**](glpushmatrix.md) et **glPopMatrix** pour enregistrer et restaurer la pile de matrice actuelle. Utilisez [**glMatrixMode**](glmatrixmode.md) pour définir la matrice actuelle.

Les fonctions suivantes récupèrent les informations relatives à **glOrtho**:

[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) avec l’argument \_ mode de matrice GL \_

**glGet** avec argument GL \_ MODELVIEW \_ Matrix

**glGet** avec argument \_ matrice de projection de la comptabilité \_

matrice de texture **glGet** avec argument GL \_ \_

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

[**glFrustum**](glfrustum.md)
</dt> <dt>

[**glMatrixMode**](glmatrixmode.md)
</dt> <dt>

[**glMultMatrix**](glmultmatrix.md)
</dt> <dt>

[**glPushMatrix**](glpushmatrix.md)
</dt> <dt>

[**glViewport**](glviewport.md)
</dt> </dl>

 

 





