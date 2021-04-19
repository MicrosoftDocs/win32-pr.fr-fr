---
description: La fonction ValidateBitmapInfoHeader vérifie une structure BITMAPINFOHEADER pour certaines erreurs courantes qui peuvent provoquer des dépassements de mémoire tampon ou des débordements d’entiers.
ms.assetid: a797c286-ed77-437f-9ec1-1ef3a189bf62
title: ValidateBitmapInfoHeader, fonction (Checkbmi. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ValidateBitmapInfoHeader
api_type:
- HeaderDef
api_location:
- checkbmi.h
ms.openlocfilehash: c7242778a2ff16414b07f887dc1e71a1547a88e0
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106530030"
---
# <a name="validatebitmapinfoheader-function"></a>ValidateBitmapInfoHeader fonction)

La `ValidateBitmapInfoHeader` fonction vérifie une structure [**BITMAPINFOHEADER**](/windows/win32/api/wingdi/ns-wingdi-bitmapinfoheader) pour certaines erreurs courantes qui peuvent provoquer des dépassements de mémoire tampon ou des débordements d’entiers.

> [!Note]  
> Cette fonction ne garantit pas que la structure [**BITMAPINFOHEADER**](/windows/win32/api/wingdi/ns-wingdi-bitmapinfoheader) est valide ou que le code qui utilise la structure est sécurisé.

 

## <a name="syntax"></a>Syntaxe


```C++
BOOL ValidateBitmapInfoHeader(
   const BITMAPINFOHEADER *pbmi,
         DWORD            cbSize
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*pbmi* 
</dt> <dd>

Pointeur vers la structure [**BITMAPINFOHEADER**](/windows/win32/api/wingdi/ns-wingdi-bitmapinfoheader) à valider.

</dd> <dt>

*cbSize* 
</dt> <dd>

Taille du bloc de mémoire qui contient la structure, en octets.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Retourne une valeur booléenne. Si la valeur est **false**, la structure [**BITMAPINFOHEADER**](/windows/win32/api/wingdi/ns-wingdi-bitmapinfoheader) n’est pas valide.

## <a name="remarks"></a>Notes

Cette fonction protège contre les erreurs suivantes :

-   Débordement arithmétique dans la taille de la structure ou taille de structure non valide.
-   Valeur non valide pour le membre **biClrUsed** .
-   Débordement arithmétique dans la taille de l’image (**biSizeImage**).
-   Valeurs non valides pour la taille de l’image (**biSizeImage**) pour les formats RVB.

La fonction ne vérifie pas si la structure décrit un format vidéo valide.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------|---------------------------------------------------------------------------------------|
| En-tête<br/> | <dl> <dt>Checkbmi. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Fonctions vidéo et image](video-and-image-functions.md)
</dt> </dl>

 

 




