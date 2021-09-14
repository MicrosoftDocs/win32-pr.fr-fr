---
description: La méthode UpdateColourTable met à jour la table des couleurs avec une nouvelle palette.
ms.assetid: 61ad98c6-a526-4aac-ad68-d44fadc668de
title: Méthode CDrawImage. UpdateColourTable (Winutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CDrawImage.UpdateColourTable
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: fcffdf9e7deaaac5a01f6559ee557c978fcda88f
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "126999257"
---
# <a name="cdrawimageupdatecolourtable-method"></a>Méthode CDrawImage. UpdateColourTable

La `UpdateColourTable` méthode met à jour la table des couleurs avec une nouvelle palette.

## <a name="syntax"></a>Syntaxe


```C++
void UpdateColourTable(
   HDC              hdc,
   BITMAPINFOHEADER *pbmi
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*HDC* 
</dt> <dd>

Contexte de périphérique contenant l’image.

</dd> <dt>

*pbmi* 
</dt> <dd>

Pointeur vers une structure [**BITMAPINFOHEADER**](/windows/win32/api/wingdi/ns-wingdi-bitmapinfoheader) contenant la nouvelle palette.

</dd> </dl>

## <a name="return-value"></a>Valeur de retour

Cette méthode ne retourne pas de valeur.

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>Winutil. h (inclure Flux. h)</dt> </dl>                                                                                   |
| Bibliothèque<br/> | <dl> <dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**CDrawImage, classe**](cdrawimage.md)
</dt> </dl>

 

 




