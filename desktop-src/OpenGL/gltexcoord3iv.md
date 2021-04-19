---
title: fonction glTexCoord3iv (GL. h)
description: Définit les coordonnées de texture actuelles. | fonction glTexCoord3iv (GL. h)
ms.assetid: 1d2f551a-d920-4020-bd51-bff28af83d44
keywords:
- glTexCoord3iv fonction OpenGL
topic_type:
- apiref
api_name:
- glTexCoord3iv
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: eef681a41b39ad1cafff1b4a23e4b814dfaab8a7
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/09/2021
ms.locfileid: "106536433"
---
# <a name="gltexcoord3iv-function"></a>glTexCoord3iv fonction)

Définit les coordonnées de texture actuelles.

## <a name="syntax"></a>Syntaxe


```C++
void WINAPI glTexCoord3iv(
   const GLint *v
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*v* 
</dt> <dd>

Pointeur vers un tableau de trois éléments, qui à son tour spécifie les coordonnées de texture s, t et r.

</dd> </dl>

## <a name="return-value"></a>Valeur renvoyée

Cette fonction ne retourne pas de valeur.

## <a name="remarks"></a>Notes

La fonction [**glTexCoord**](gltexcoord-functions.md) définit les coordonnées de texture actuelles qui font partie des données associées aux sommets de polygone. La fonction **glTexCoord** spécifie des coordonnées de texture en une, deux, trois ou quatre dimensions. La fonction glTexCoord1 définit les coordonnées de texture actuelles sur (s, 0, 0, 1); un appel à glTexCoord2 les affecte à la valeur (s, t, 0, 1). De même, glTexCoord3 spécifie les coordonnées de la texture comme (s, t, r, 1) et glTexCoord4 définit les quatre composants explicitement comme (s, t, r, q). Vous pouvez mettre à jour les coordonnées de texture actuelles à tout moment. En particulier, vous pouvez appeler glTexCoord entre un appel à [**glBegin**](glbegin.md) et l’appel correspondant à [**glEnd**](glend.md). La fonction suivante récupère des informations relatives à **glTexCoord**:

[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) avec argument de \_ la \_ texture actuelle de la comptabilité \_

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

[glVertex](glvertex-functions.md)
</dt> </dl>

 

 





