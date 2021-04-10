---
title: fonction glNormal3b (GL. h)
description: Définit le vecteur normal actuel. | fonction glNormal3b (GL. h)
ms.assetid: b6976143-bc9a-4766-9f7e-5380c3a24173
keywords:
- glNormal3b fonction OpenGL
topic_type:
- apiref
api_name:
- glNormal3b
api_location:
- Opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3a09a92b718881670ed5625fd5aa94a23193cdd6
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/09/2021
ms.locfileid: "103869709"
---
# <a name="glnormal3b-function"></a>glNormal3b fonction)

Définit le vecteur normal actuel.

## <a name="syntax"></a>Syntaxe


```C++
void WINAPI glNormal3b(
   GLbyte nx,
   GLbyte ny,
   GLbyte nz
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

## <a name="remarks"></a>Notes

La normale actuelle est définie sur les coordonnées données chaque fois que vous appelez la fonction **glNormal3b** .

Les arguments Byte, short ou Integer sont convertis en format à virgule flottante à l’aide d’un mappage linéaire qui mappe la valeur entière représentable la plus positive à 1,0, et la valeur entière la plus négative à-1,0.

Les normales spécifiées avec **glNormal3b** n’ont pas besoin d’avoir une longueur d’unité. Si la normalisation est activée, les normales spécifiées avec **glNormal3b** sont normalisées après la transformation. Vous pouvez contrôler la normalisation à l’aide de [**glEnable**](glenable.md) et [**glDisable**](gldisable.md) avec l’argument GL \_ Normalize. Par défaut, la normalisation est désactivée. Vous pouvez mettre à jour la normale actuelle à tout moment. En particulier, vous pouvez appeler **glNormal3b** entre un appel à [**glBegin**](glbegin.md) et l’appel correspondant à [**glEnd**](glend.md). Les fonctions suivantes récupèrent les informations relatives à **glNormal3b**:

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

 

 





