---
description: Méthode constructeur CEnumMediaTypes. CEnumMediaTypes.
ms.assetid: fae2e05c-3f7b-4511-9b9d-5a37ea03f851
title: Constructeur CEnumMediaTypes. CEnumMediaTypes (Amfilter. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CEnumMediaTypes.CEnumMediaTypes
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 2d243ed25cc48c5d30d467f97e2ec20e1f0f2b58
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "126923667"
---
# <a name="cenummediatypescenummediatypes-constructor"></a>Constructeur CEnumMediaTypes. CEnumMediaTypes

Méthode de constructeur.

## <a name="syntax"></a>Syntaxe


```C++
CEnumMediaTypes(
   CBasePin        *pPin,
   CEnumMediaTypes *pEnumMediaTypes
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*pPin* 
</dt> <dd>

Pointeur vers le code confidentiel sur lequel l’énumération doit être exécutée.

</dd> <dt>

*pEnumMediaTypes* 
</dt> <dd>

Pointeur vers l’interface [**IEnumMediaTypes**](/windows/desktop/api/Strmif/nn-strmif-ienummediatypes) d’un énumérateur à cloner, ou **null**.

</dd> </dl>

## <a name="remarks"></a>Notes

Si *pEnumMediaTypes* a la **valeur null**, cette méthode initialise l’énumérateur au début de la séquence d’énumération. Sinon, elle duplique l’état interne de l’énumérateur spécifié par *pEnumMediaTypes*.

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>Amfilter. h (inclure Flux. h)</dt> </dl>                                                                                  |
| Bibliothèque<br/> | <dl> <dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**CEnumMediaTypes, classe**](cenummediatypes.md)
</dt> </dl>

 

 




