---
title: gluGetNurbsProperty, fonction (Glu. h)
description: La fonction gluGetNurbsProperty obtient une propriété NURBS B-spline (NURBS) non uniforme.
ms.assetid: 7dbc75a0-d04e-4794-b3dd-a602addf9dfa
keywords:
- gluGetNurbsProperty fonction OpenGL
topic_type:
- apiref
api_name:
- gluGetNurbsProperty
api_location:
- glu32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a68e91fbdaafc2a1857a95e059125bf62347777edfbcc764868ceea0a8fce578
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119519589"
---
# <a name="glugetnurbsproperty-function"></a>gluGetNurbsProperty fonction)

La fonction **gluGetNurbsProperty** obtient une propriété NURBS B-spline ([NURBS](using-nurbs-curves-and-surfaces.md)) non uniforme.

## <a name="syntax"></a>Syntaxe


```C++
void WINAPI gluGetNurbsProperty(
   GLUnurbs *nobj,
   GLenum   property,
   GLfloat  *value
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*nobj* 
</dt> <dd>

Objet NURBS (créé avec [**gluNewNurbsRenderer**](glunewnurbsrenderer.md)).

</dd> <dt>

*property* 
</dt> <dd>

Propriété dont la valeur doit être récupérée. Les valeurs suivantes sont valides : \_ tolérance d’échantillonnage Glu \_ , \_ mode d’affichage Glu \_ , \_ élimination de Glu, \_ matrice de chargement automatique Glu \_ \_ , \_ tolérance paramétrique Glu \_ , méthode d' \_ échantillonnage Glu \_ , \_ étape Glu U \_ et \_ étape Glu V \_ .

</dd> <dt>

*value* 
</dt> <dd>

Pointeur vers l’emplacement dans lequel la valeur de la propriété nommée est écrite.

</dd> </dl>

## <a name="return-value"></a>Valeur renvoyée

Cette fonction ne retourne pas de valeur.

## <a name="remarks"></a>Remarques

Utilisez **gluGetNurbsProperty** pour récupérer les propriétés stockées dans un objet NURBS. Ces propriétés affectent le mode de rendu des courbes et des surfaces NURBS. Pour plus d’informations sur les propriétés NURBS, consultez [**gluNurbsProperty**](glunurbsproperty.md).

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows 2000 Professionnel - \[Applications de bureau uniquement\]<br/>                           |
| Serveur minimal pris en charge<br/> | Windows 2000 Server - \[Applications de bureau uniquement\]<br/>                                 |
| En-tête<br/>                   | <dl> <dt>Glu. h</dt> </dl>     |
| Bibliothèque<br/>                  | <dl> <dt>Glu32. lib</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Glu32.dll</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**gluNewNurbsRenderer**](glunewnurbsrenderer.md)
</dt> <dt>

[**gluNurbsProperty**](glunurbsproperty.md)
</dt> </dl>

 

 





