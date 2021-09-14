---
description: GUID de l’application de l’abonné.
ms.assetid: 46c91cae-ca31-4eac-baa8-d36910917f0f
title: 'IEventSubscription3 :: SubscriberApplicationID, propriété'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IEventSubscription3.SubscriberApplicationID
- IEventSubscription3.get_SubscriberApplicationID
- IEventSubscription3.put_SubscriberApplicationID
api_type:
- COM
api_location: ''
ms.openlocfilehash: c2e726d97821a7a7143f4971a4918227235adb9c
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "126855405"
---
# <a name="ieventsubscription3subscriberapplicationid-property"></a>IEventSubscription3 :: SubscriberApplicationID, propriété

GUID de l’application de l’abonné.

Cette propriété est en lecture/écriture.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT put_SubscriberApplicationID(
  [in]          BSTR bstrSubscriberApplicationID
);

HRESULT get_SubscriberApplicationID(
  [out, retval] BSTR *pbstrSubscriberApplicationID
);
```



## <a name="property-value"></a>Valeur de la propriété

Chaîne contenant le GUID de l’application de l’abonné.

## <a name="error-codes"></a>Codes d’erreur

Cette méthode peut retourner les valeurs de retour standard E \_ INVALIDARG, e \_ OUTOFMEMORY, e \_ inattendue, e \_ Fail et S \_ OK.

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|-------------------------------------|------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows 2000 Professionnel - \[Applications de bureau uniquement\]<br/> |
| Serveur minimal pris en charge<br/> | Windows 2000 Server - \[Applications de bureau uniquement\]<br/>       |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**IEventSubscription3**](ieventsubscription3.md)
</dt> </dl>

 

 




