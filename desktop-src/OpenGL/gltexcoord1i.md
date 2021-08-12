---
title: fonction glTexCoord1i (GL. h)
description: Définit les coordonnées de texture actuelles. | fonction glTexCoord1i (GL. h)
ms.assetid: 910e5908-8c19-4c79-9744-a534bce03b20
keywords:
- glTexCoord1i fonction OpenGL
topic_type:
- apiref
api_name:
- glTexCoord1i
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6f0b47f10ff0d47333c4aebf05dbe39371ad3e79e8572692fc774a5607e4e20f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118614003"
---
# <a name="gltexcoord1i-function"></a>glTexCoord1i fonction)

Définit les coordonnées de texture actuelles.

## <a name="syntax"></a>Syntaxe


```C++
void WINAPI glTexCoord1i(
   GLint s
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*s* 
</dt> <dd>

Coordonnée de texture s.

</dd> </dl>

## <a name="return-value"></a>Valeur renvoyée

Cette fonction ne retourne pas de valeur.

## <a name="remarks"></a>Remarques

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

 

 





