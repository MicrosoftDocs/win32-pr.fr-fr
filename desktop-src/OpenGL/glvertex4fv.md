---
title: fonction glVertex4fv (GL. h)
description: Spécifie un sommet. | fonction glVertex4fv (GL. h)
ms.assetid: c2a766fd-3ad8-463b-8f09-36d0673e6716
keywords:
- glVertex4fv fonction OpenGL
topic_type:
- apiref
api_name:
- glVertex4fv
api_location:
- Opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 31f840c6d3e69e809fe4ae504cb322d0d0a6b3bbc28b495df9a17df94f891836
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120035609"
---
# <a name="glvertex4fv-function"></a>glVertex4fv fonction)

Spécifie un sommet.

## <a name="syntax"></a>Syntaxe


```C++
void WINAPI glVertex4fv(
   const GLfloat *v
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*v* 
</dt> <dd>

Pointeur vers un tableau de quatre éléments. Les éléments sont les coordonnées x, y, z et w d’un vertex.

</dd> </dl>

## <a name="return-value"></a>Valeur renvoyée

Cette fonction ne retourne pas de valeur.

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

[**glCallList**](glcalllist.md)
</dt> <dt>

[**glColor**](glcolor-functions.md)
</dt> <dt>

[**glEdgeFlag**](gledgeflag-functions.md)
</dt> <dt>

[**glEnd**](glend.md)
</dt> <dt>

[**glEvalCoord**](glevalcoord-functions.md)
</dt> <dt>

[**glIndex**](glindex-functions.md)
</dt> <dt>

[**glMaterial**](glmaterial-functions.md)
</dt> <dt>

[**glNormal**](glnormal-functions.md)
</dt> <dt>

[**glRect**](glrect-functions.md)
</dt> <dt>

[**glTexCoord**](gltexcoord-functions.md)
</dt> </dl>

 

 





