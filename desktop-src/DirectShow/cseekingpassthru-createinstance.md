---
description: La méthode CreateInstance crée une instance de l’objet. Cette méthode prend en charge la création de l’objet par le biais d’une fabrique de classe. Pour plus d’informations, consultez CFactoryTemplate.
ms.assetid: 88dfa933-6fa1-4b57-8b0d-579233fa960c
title: Méthode CSeekingPassThru. CreateInstance (Seekpt. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CSeekingPassThru.CreateInstance
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 3640cbd6a0a3e582899e7f5cd349ca48498f3532
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127121941"
---
# <a name="cseekingpassthrucreateinstance-method"></a>CSeekingPassThru. CreateInstance, méthode

La `CreateInstance` méthode crée une instance de l’objet. Cette méthode prend en charge la création de l’objet par le biais d’une fabrique de classe. Pour plus d’informations, consultez [**CFactoryTemplate**](cfactorytemplate.md).

## <a name="syntax"></a>Syntaxe


```C++
static CUnknown* CreateInstance(
   LPUNKNOWN pUnk,
   HRESULT   *phr
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*pUnk* 
</dt> <dd>

Pointeur vers le propriétaire de cet objet. Si l’objet est agrégé, passer un pointeur vers l’interface **IUnknown** de l’objet d’agrégation. Sinon, affectez la valeur **null** à ce paramètre.

</dd> <dt>

*phr* 
</dt> <dd>

Pointeur vers une valeur **HRESULT** . Ignoré.

</dd> </dl>

## <a name="return-value"></a>Valeur de retour

Retourne un pointeur vers un nouvel objet **CSeekingPassThru** .

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>Seekpt. h (inclure Flux. h)</dt> </dl>                                                                                    |
| Bibliothèque<br/> | <dl> <dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**CSeekingPassThru, classe**](cseekingpassthru.md)
</dt> </dl>

 

 




