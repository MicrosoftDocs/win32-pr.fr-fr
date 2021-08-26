---
title: fonction glVertex4f (GL. h)
description: Spécifie un sommet. | fonction glVertex4f (GL. h)
ms.assetid: 877fce8c-095e-4ae4-8633-7c84659ee8a6
keywords:
- glVertex4f fonction OpenGL
topic_type:
- apiref
api_name:
- glVertex4f
api_location:
- Opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5140d7e69da06ba36c6b07b8c92f9aacdd90c49777ac5dc479dc17c5a77915ac
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120035679"
---
# <a name="glvertex4f-function"></a>glVertex4f fonction)

Spécifie un sommet.

## <a name="syntax"></a>Syntaxe


```C++
void WINAPI glVertex4f(
   GLfloat x,
   GLfloat y,
   GLfloat z,
   GLfloat w
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*x* 
</dt> <dd>

Spécifie la coordonnée x d’un vertex.

</dd> <dt>

*y* 
</dt> <dd>

Spécifie la coordonnée y d’un vertex.

</dd> <dt>

*Lettre* 
</dt> <dd>

Spécifie la coordonnée z d’un vertex.

</dd> <dt>

*w* 
</dt> <dd>

Spécifie la coordonnée w d’un vertex.

</dd> </dl>

## <a name="return-value"></a>Valeur renvoyée

Cette fonction ne retourne pas de valeur.

## <a name="remarks"></a>Remarques

Les commandes de fonction glVertex sont utilisées dans les paires [**glBegin**](glbegin.md) / [**glEnd**](glend.md) pour spécifier les sommets de points, de lignes et de polygones. Les coordonnées de couleur actuelle, normale et de texture sont associées au vertex lorsque glVertex est appelé. Si seuls *x* et *y* sont spécifiés, *z* a pour valeur par défaut 0,0 et *w* a la valeur par défaut 1,0. Lorsque *x*, *y* et *z* sont spécifiés, *w* a pour valeur par défaut 1,0. L’appel de glVertex en dehors d’une paire de / **glEnd** glBegin entraîne un comportement indéfini.

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

 

 





