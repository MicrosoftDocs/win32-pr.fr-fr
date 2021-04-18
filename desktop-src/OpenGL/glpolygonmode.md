---
title: fonction glPolygonMode (GL. h)
description: La fonction glPolygonMode sélectionne un mode de pixellisation de polygone.
ms.assetid: d8781bae-e78c-40fb-9f33-c742c70ebda1
keywords:
- glPolygonMode fonction OpenGL
topic_type:
- apiref
api_name:
- glPolygonMode
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 23d133243c1655432842a939b8da0f3a981fdffd
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "106512211"
---
# <a name="glpolygonmode-function"></a>glPolygonMode fonction)

La fonction **glPolygonMode** sélectionne un mode de pixellisation de polygone.

## <a name="syntax"></a>Syntaxe


```C++
void WINAPI glPolygonMode(
   GLenum face,
   GLenum mode
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*se* 
</dt> <dd>

Polygones auxquels ce *mode* s’applique. Doit être \_ de premier plan pour les polygones frontaux, le GL \_ de retour pour les polygones d’arrière-plan, ou le \_ recto \_ et l’arrière GL \_ pour les polygones frontaux et dorsaux.

</dd> <dt>

*mode* 
</dt> <dd>

Façon dont les polygones seront pixellisés. Les modes suivants sont définis et peuvent être spécifiés en *mode*. La valeur par défaut est \_ remplissage GL pour les polygones avant et arrière.



| Valeur                                                                                                                                          | Signification                                                                                                                                                                                                                                                                                                                                                                                                                                   |
|------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="GL_POINT"></span><span id="gl_point"></span><dl> <dt>**\_point GL**</dt> </dl> | Les sommets de polygone marqués comme point de départ d’un bord de limite sont dessinés en tant que points. Les attributs de point tels \_ que \_ la taille du point GL et \_ le point de contrôle de l’état du GL \_ déterminent la pixellisation des points. Les attributs de pixellisation de polygone autres que le \_ mode polygone GL n' \_ ont aucun effet.<br/>                                                                                                                                                    |
| <span id="GL_LINE"></span><span id="gl_line"></span><dl> <dt>**\_ligne GL**</dt> </dl>    | Les bords limites du polygone sont dessinés sous forme de segments de ligne. Ils sont traités comme des segments de ligne connectés pour la ligne stippling ; le compteur et le modèle de ligne stipple ne sont pas réinitialisés entre les segments (voir [**glLineStipple**](gllinestipple.md)). Les attributs de ligne tels \_ que \_ la largeur de ligne GL et \_ \_ le contrôle de ligne GL lissent la pixellisation des lignes. Les attributs de pixellisation de polygone autres que le \_ mode polygone GL n' \_ ont aucun effet.<br/> |
| <span id="GL_FILL"></span><span id="gl_fill"></span><dl> <dt>**remplissage du GL \_**</dt> </dl>    | L’intérieur du polygone est rempli. Les attributs Polygon tels que GL \_ Polygon \_ STIPPLE et GL \_ Polygon \_ lisse contrôlent la pixellisation du polygone.<br/>                                                                                                                                                                                                                                                                       |



 

</dd> </dl>

## <a name="return-value"></a>Valeur renvoyée

Cette fonction ne retourne pas de valeur.

## <a name="error-codes"></a>Codes d’erreur

Les codes d’erreur suivants peuvent être récupérés par la fonction [**glGetError**](glgeterror.md) .



| Nom                                                                                                  | Signification                                                                                                                               |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**\_enum GL non valide \_**</dt> </dl>      | La *face* ou le *mode* n’était pas une valeur acceptée.<br/>                                                                         |
| <dl> <dt>**\_opération non valide du GL \_**</dt> </dl> | La fonction a été appelée entre un appel à [**glBegin**](glbegin.md) et l’appel correspondant à [**glEnd**](glend.md).<br/> |



## <a name="remarks"></a>Notes

La fonction **glPolygonMode** contrôle l’interprétation des polygones pour la pixellisation. Le paramètre *face* décrit quel *mode* Polygon s’applique à : les polygones frontaux (GL \_ frontal), les polygones d’arrière-plan (GL \_ Back) ou les deux ( \_ recto \_ et verso GL \_ ). Le mode polygone affecte uniquement la pixellisation finale des polygones. En particulier, les vertex d’un polygone sont allumés et le polygone est coupé et éventuellement Culling avant l’application de ces modes.

Pour dessiner une surface avec des polygones retournés vers l’avant et des polygones prédéfinis, appelez

**glPolygonMode**(GL \_ frontal, \_ ligne GL);

Les sommets sont marqués comme limites ou non liés par un indicateur de bord. Les indicateurs de périphérie sont générés en interne par OpenGL lorsqu’ils décomposent des polygones, et ils peuvent être définis explicitement à l’aide de [**glEdgeFlag**](gledgeflag-functions.md).

La fonction suivante récupère des informations relatives à **glPolygonMode**:

[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) avec argument GL \_ polygone \_ mode

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

[**glEdgeFlag**](gledgeflag-functions.md)
</dt> <dt>

[**glEnd**](glend.md)
</dt> <dt>

[**glLineStipple**](gllinestipple.md)
</dt> <dt>

[**glLineWidth**](gllinewidth.md)
</dt> <dt>

[**glPointSize**](glpointsize.md)
</dt> <dt>

[**glPolygonStipple**](glpolygonstipple.md)
</dt> </dl>

 

 





