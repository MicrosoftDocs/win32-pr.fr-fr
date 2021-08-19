---
description: La classe CAutoUsingOutputPin obtient et libère l’accès à un objet CDynamicOutputPin.
ms.assetid: 4ded5d18-4b14-4574-ad1f-73b886a51fac
title: CAutoUsingOutputPin, classe (Amfilter. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CAutoUsingOutputPin
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 141c65507a0d983a2b4531b93617ed741e7403b8b2a5ead9c196f78dcf61acdf
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118955378"
---
# <a name="cautousingoutputpin-class"></a>CAutoUsingOutputPin, classe

La classe **CAutoUsingOutputPin** obtient et libère l’accès à un objet [**CDynamicOutputPin**](cdynamicoutputpin.md) .

**CAutoUsingOutputPin** possède les types de membres suivants :



| M&#233;thodes publiques                                                           | Description                                              |
|--------------------------------------------------------------------------|----------------------------------------------------------|
| [**CAutoUsingOutputPin**](cautousingoutputpin-cautousingoutputpin.md)   | Méthode de constructeur. Obtient l’accès au code confidentiel spécifié. |
| [**~ CAutoUsingOutputPin**](cautousingoutputpin--cautousingoutputpin.md) | Méthode de destructeur. Obtient l’accès au code confidentiel spécifié.  |



 

## <a name="remarks"></a>Remarques

Lorsque certaines méthodes sont appelées sur [**CDynamicOutputPin**](cdynamicoutputpin.md), l’appelant doit obtenir l’accès au code confidentiel, puis libérer cet accès. Pour obtenir l’accès, l’appelant utilise la méthode [**CDynamicOutputPin :: StartUsingOutputPin**](cdynamicoutputpin-startusingoutputpin.md) . Pour libérer l’accès, elle appelle la méthode [**CDynamicOutputPin :: StopUsingOutputPin**](cdynamicoutputpin-stopusingoutputpin.md) . La classe **CAutoUsingOutputPin** est une classe d’assistance qui gère ces tâches dans ses méthodes de constructeur et de destructeur. L’exemple de code suivant montre comment utiliser cette classe :


```
CDynamicOutputPin *pPin;
HRESULT hr = S_OK;  // Important! Initialize to S_OK.

// TODO: Obtain a pointer to the pin (not shown).

// Scope for lock.
{
    // Hold lock on pin.
    CAutoUsingOutputPin UsingPin(pPin, &hr)

    if (SUCCEEDED(hr)) 
    {

        // Safe to use the pin.
        hr = pPin->Deliver(pSample);

    }

} // Object goes out of scope here.

// No longer safe to use the pin.
```



## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>Amfilter. h (inclure Flux. h)</dt> </dl>                                                                                  |
| Bibliothèque<br/> | <dl> <dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Référence de classe de base](base-class-reference.md)
</dt> </dl>

 

 




