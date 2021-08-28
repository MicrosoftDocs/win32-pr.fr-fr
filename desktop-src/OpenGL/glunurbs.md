---
title: gluNurbsCallback, fonction (Glu. h)
description: La fonction gluNurbsCallback définit un rappel pour un objet NURBS B-spline (NURBS) non uniforme.
ms.assetid: 1e9afc00-57c6-459e-a9fc-463f45df2084
keywords:
- gluNurbsCallback fonction OpenGL
topic_type:
- apiref
api_name:
- gluNurbsCallback
api_location:
- Glu32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d1da7ebc999d44911cb345b051213a12865e608db7b7fe66e33eb1bb567ef7a7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119519499"
---
# <a name="glunurbscallback-function"></a>gluNurbsCallback fonction)

La fonction **gluNurbsCallback** définit un rappel pour un objet NURBS B-spline ([NURBS](using-nurbs-curves-and-surfaces.md)) non uniforme.

## <a name="syntax"></a>Syntaxe


```C++
void WINAPI gluNurbsCallback(
   GLUnurbs *nobj,
   GLenum   which,
   void (CALLBACK *fn)()
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*nobj* 
</dt> <dd>

Objet NURBS (créé avec [**gluNewNurbsRenderer**](glunewnurbsrenderer.md)).

</dd> <dt>

*et* 
</dt> <dd>

Rappel en cours de définition. La seule valeur valide est GLU \_ Error. La signification de l' \_ erreur Glu signifie que la fonction d’erreur est appelée lorsqu’une erreur est rencontrée. Son argument unique est de type **GLenum** et indique l’erreur spécifique qui s’est produite. Il y a 37 erreurs propres à NURBS, nommées GLU \_ NURBS \_ ERROR1 à Glu \_ NURBS \_ ERROR37. Les chaînes de caractères décrivant ces erreurs peuvent être récupérées avec [**gluErrorString**](gluerrorstring.md).

</dd> <dt>

*FN* 
</dt> <dd>

Pointeur vers la fonction de rappel.

</dd> </dl>

## <a name="return-value"></a>Valeur renvoyée

Cette fonction ne retourne pas de valeur.

## <a name="remarks"></a>Remarques

Utilisez **gluNurbsCallback** pour définir un rappel devant être utilisé par un objet NURBS. Si le rappel spécifié est déjà défini, il est remplacé. Si *FN* a la **valeur null**, tout rappel existant est effacé.

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

[**gluErrorString**](gluerrorstring.md)
</dt> <dt>

[**gluNewNurbsRenderer**](glunewnurbsrenderer.md)
</dt> </dl>

 

 





