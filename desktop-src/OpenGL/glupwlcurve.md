---
title: gluPwlCurve, fonction (Glu. h)
description: La fonction gluPwlCurve décrit une courbe de découpage NURBS B-spline (NURBS) par morceaux linéaire non uniforme.
ms.assetid: 3d08e7e8-dfdf-447c-9795-bd73299412b5
keywords:
- gluPwlCurve fonction OpenGL
topic_type:
- apiref
api_name:
- gluPwlCurve
api_location:
- glu32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d15c532659811c7e499369e7798c4b1ceaf842bc
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127194371"
---
# <a name="glupwlcurve-function"></a>gluPwlCurve fonction)

La fonction **gluPwlCurve** décrit une courbe de découpage NURBS B-spline ([NURBS](using-nurbs-curves-and-surfaces.md)) par morceaux linéaire non uniforme.

## <a name="syntax"></a>Syntaxe


```C++
void WINAPI gluPwlCurve(
   GLUnurbs *nobj,
   GLint    count,
   GLfloat  *array,
   GLint    stride,
   GLenum   type
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*nobj* 
</dt> <dd>

Objet NURBS (créé avec [**gluNewNurbsRenderer**](glunewnurbsrenderer.md)).

</dd> <dt>

*count* 
</dt> <dd>

Nombre de points sur la courbe.

</dd> <dt>

*array* 
</dt> <dd>

Tableau contenant les points de courbe.

</dd> <dt>

*progrès* 
</dt> <dd>

Décalage (nombre de valeurs à virgule flottante simple précision) entre des points sur la courbe.

</dd> <dt>

*type* 
</dt> <dd>

Type de courbe. Il doit s’agir \_ de Glu Map1 \_ Trim \_ 2 ou de Glu \_ Map1 \_ Trim \_ 3.

</dd> </dl>

## <a name="return-value"></a>Valeur renvoyée

Cette fonction ne retourne pas de valeur.

## <a name="remarks"></a>Notes

La fonction **gluPwlCurve** décrit une courbe de rognage linéaire par morceaux pour une surface NURBS. Une courbe linéaire par morceaux se compose d’une liste de coordonnées de points dans l’espace de paramètres pour la surface NURBS à tronquer. Ces points sont reliés par des segments de ligne pour former une courbe. Si la courbe est une approximation d’une courbe réelle, les points doivent être suffisamment proches pour que le tracé résultant apparaisse courbé au niveau de la résolution utilisée dans l’application.

Si le *type* est Glu \_ Map1 \_ Trim \_ 2, il décrit une courbe dans l’espace de paramètres à deux dimensions (*u* et *v*). S’il s’agit \_ de Glu Map1 \_ Trim \_ 3, il décrit une courbe dans un espace de paramètre homogène à deux dimensions (*u*, *v* et *w*). Pour plus d’informations sur les courbes de suppression, consultez [**gluBeginTrim**](glubegintrim.md).

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows 2000 Professionnel - \[Applications de bureau uniquement\]<br/>                           |
| Serveur minimal pris en charge<br/> | Windows 2000 Server - \[Applications de bureau uniquement\]<br/>                                 |
| En-tête<br/>                   | <dl> <dt>Glu. h</dt> </dl>     |
| Bibliothèque<br/>                  | <dl> <dt>Glu32. lib</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Glu32.dll</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**gluBeginCurve**](glubegincurve.md)
</dt> <dt>

[**gluBeginTrim**](glubegintrim.md)
</dt> <dt>

[**gluNewNurbsRenderer**](glunewnurbsrenderer.md)
</dt> <dt>

[**gluNurbsCurve**](glunurbscurve.md)
</dt> </dl>

 

 





