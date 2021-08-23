---
title: fonction glTexCoord3d (GL. h)
description: Définit les coordonnées de texture actuelles. | fonction glTexCoord3d (GL. h)
ms.assetid: 41b8aa69-c069-493f-a1e3-51cf6a01209e
keywords:
- glTexCoord3d fonction OpenGL
topic_type:
- apiref
api_name:
- glTexCoord3d
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 15591d2cf8e62e6d016818001ee7d39ad3cc8ed0fc1bf8d4aacaec56b51d6189
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119491129"
---
# <a name="gltexcoord3d-function"></a>glTexCoord3d fonction)

Définit les coordonnées de texture actuelles.

## <a name="syntax"></a>Syntaxe


```C++
void WINAPI glTexCoord3d(
   GLdouble s,
   GLdouble t,
   GLdouble r
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*s* 
</dt> <dd>

Coordonnée de texture s.

</dd> <dt>

*t* 
</dt> <dd>

Coordonnée de la texture t.

</dd> <dt>

*r* 
</dt> <dd>

Coordonnée de texture r.

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

 

 





