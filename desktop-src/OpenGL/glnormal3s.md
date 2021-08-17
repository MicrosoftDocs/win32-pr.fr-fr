---
title: fonction glNormal3s (GL. h)
description: Définit le vecteur normal actuel. | fonction glNormal3s (GL. h)
ms.assetid: 4fd98ad5-266d-4ef1-9c1f-2b5166ee65d7
keywords:
- glNormal3s fonction OpenGL
topic_type:
- apiref
api_name:
- glNormal3s
api_location:
- Opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0a21ce2ff4c780e19e0849730db5fb7831343a32961e0e673b355124f799c61c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117795252"
---
# <a name="glnormal3s-function"></a>glNormal3s fonction)

Définit le vecteur normal actuel.

## <a name="syntax"></a>Syntaxe


```C++
void WINAPI glNormal3s(
   GLshort nx,
   GLshort ny,
   GLshort nz
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*NX* 
</dt> <dd>

Spécifie la coordonnée x du nouveau vecteur normal actuel.

</dd> <dt>

*NY* 
</dt> <dd>

Spécifie la coordonnée y du nouveau vecteur normal actuel.

</dd> <dt>

*NZ* 
</dt> <dd>

Spécifie la coordonnée z du nouveau vecteur normal actuel.

</dd> </dl>

## <a name="return-value"></a>Valeur renvoyée

Cette fonction ne retourne pas de valeur.

## <a name="remarks"></a>Remarques

La normale actuelle est définie sur les coordonnées données chaque fois que vous appelez la fonction **glNormal3s**.

Les arguments Byte, short ou Integer sont convertis en format à virgule flottante avec un mappage linéaire qui mappe la valeur entière représentable la plus positive à 1,0, et la valeur entière représentable la plus négative à-1,0.

Les normales spécifiées à l’aide de **glNormal3s** n’ont pas besoin d’avoir une longueur d’unité. Si la normalisation est activée, les normales spécifiées avec **glNormal3s** sont normalisées après la transformation. Vous pouvez contrôler normalizationby à l’aide de [**glEnable**](glenable.md) et [**glDisable**](gldisable.md) avec l’argument GL \_ Normalize. Par défaut, la normalisation est désactivée. Vous pouvez mettre à jour la normale actuelle à tout moment. En particulier, vous pouvez appeler **glNormal3s** entre un appel à [**glBegin**](glbegin.md) et l’appel correspondant à [**glEnd**](glend.md). Les fonctions suivantes récupèrent les informations relatives à **glNormal3s**:

[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) avec argument GL \_ actuel \_ normal

[**glIsEnable**](glisenabled.md) avec argument GL \_ Normalize

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

[**glIndex**](glindex-functions.md)
</dt> <dt>

[**glTexCoord**](gltexcoord-functions.md)
</dt> <dt>

[**glVertex**](glvertex-functions.md)
</dt> </dl>

 

 





