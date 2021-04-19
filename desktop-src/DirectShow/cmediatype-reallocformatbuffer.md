---
description: La méthode ReallocFormatBuffer réaffecte le bloc de format à une nouvelle taille.
ms.assetid: 49bec677-09cc-4e1a-994a-13e873e61713
title: Méthode CMediaType. ReallocFormatBuffer (mtype. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CMediaType.ReallocFormatBuffer
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 22e861c61f01a7594d720833e2b3a4b923a1e183
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106532203"
---
# <a name="cmediatypereallocformatbuffer-method"></a>Méthode CMediaType. ReallocFormatBuffer

La `ReallocFormatBuffer` méthode réaffecte le bloc de format à une nouvelle taille.

## <a name="syntax"></a>Syntaxe


```C++
BYTE* ReallocFormatBuffer(
   ULONG length
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*length* 
</dt> <dd>

Nouvelle taille requise pour le bloc de format, en octets. Doit être supérieur à zéro.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Retourne un pointeur vers le nouveau bloc en cas de réussite. Sinon, retourne un pointeur vers l’ancien bloc de format ou la **valeur null**.

## <a name="remarks"></a>Notes

Cette méthode alloue un nouveau bloc de format. Il copie la plus grande partie du bloc de format existant dans le nouveau bloc de format. Si le nouveau bloc est plus petit que le bloc existant, le bloc de format existant est tronqué. Si le nouveau bloc est plus grand, le contenu de l’espace supplémentaire n’est pas défini. Ils ne sont pas explicitement définis sur zéro.

La méthode met à jour les membres **cbFormat** et **pbFormat** de la structure du **\_ \_ type de média am** .

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>Mtype. h (include streams. h)</dt> </dl>                                                                                     |
| Bibliothèque<br/> | <dl> <dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**CMediaType, classe**](cmediatype.md)
</dt> </dl>

 

 




