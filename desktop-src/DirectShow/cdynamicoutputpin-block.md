---
description: 'La méthode Block bloque ou débloque le workflow de données à partir du code confidentiel. Cette méthode implémente la méthode IPinFlowControl :: Block.'
ms.assetid: 8281cd8c-7543-42b5-9a4a-11bdfcb659e3
title: Méthode CDynamicOutputPin. Block (Amfilter. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CDynamicOutputPin.Block
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 6b10e9dfd43f3ad98adf8f6abb0eb7c2223d5970
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "126999247"
---
# <a name="cdynamicoutputpinblock-method"></a>CDynamicOutputPin. Block, méthode

La `Block` méthode bloque ou débloque le workflow de données à partir du code confidentiel. Cette méthode implémente la méthode [**IPinFlowControl :: Block**](/windows/desktop/api/Strmif/nf-strmif-ipinflowcontrol-block) .

## <a name="syntax"></a>Syntaxe


```C++
HRESULT Block(
   DWORD  dwBlockFlags,
   HANDLE hEvent
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*dwBlockFlags* 
</dt> <dd>

Indicateur qui spécifie s’il faut bloquer ou débloquer le code confidentiel. Il doit s’agir de l’une des valeurs suivantes : 

Zéro : débloquer le workflow de données à partir du code confidentiel.

\_ \_ \_ Bloc de contrôle de workflow am pin \_ : bloquer le workflow de données à partir du code confidentiel.

</dd> <dt>

*hEvent* 
</dt> <dd>

Handle vers un objet d’événement, ou **null**.

</dd> </dl>

## <a name="return-value"></a>Valeur de retour

Retourne une valeur **HRESULT** . Les valeurs possibles sont les suivantes :



| Code de retour                                                                                                                    | Description                                              |
|--------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------|
| <dl> <dt>**S \_ false**</dt> </dl>                                        | Le code PIN est déjà débloqué.<br/>                     |
| <dl> <dt>**\_OK**</dt> </dl>                                           | Réussite.<br/>                                      |
| <dl> <dt>**E \_ INVALIDARG**</dt> </dl>                                   | Argument non valide.<br/>                             |
| <dl> <dt>**\_code PIN de VFW E \_ \_ déjà \_ bloqué**</dt> </dl>                   | Le code PIN est déjà bloqué sur un autre thread.<br/>     |
| <dl> <dt>**\_ \_ code PIN de VFW E \_ déjà \_ bloqué \_ sur \_ ce \_ thread**</dt> </dl> | Le code PIN est déjà bloqué sur le thread appelant.<br/> |



 

## <a name="remarks"></a>Notes

Pour plus d’informations sur cette méthode, consultez [**IPinFlowControl :: Block**](/windows/desktop/api/Strmif/nf-strmif-ipinflowcontrol-block). En interne, cette méthode appelle l’une des méthodes protégées suivantes :

-   Block (asynchrone) : [ **CDynamicOutputPin :: AsynchronousBlockOutputPin**](cdynamicoutputpin-asynchronousblockoutputpin.md)
-   Bloquer (synchrone) : [ **CDynamicOutputPin :: SynchronousBlockOutputPin**](cdynamicoutputpin-synchronousblockoutputpin.md)
-   Unblock : [ **CDynamicOutputPin :: UnblockOutputPin**](cdynamicoutputpin-unblockoutputpin.md)

Le déblocage est toujours effectué de façon synchrone.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>Amfilter. h (inclure Flux. h)</dt> </dl>                                                                                  |
| Bibliothèque<br/> | <dl> <dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**CDynamicOutputPin, classe**](cdynamicoutputpin.md)
</dt> </dl>

 

 




