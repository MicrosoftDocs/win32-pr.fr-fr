---
description: GUID de la partition de l’abonné.
ms.assetid: 0b2411d3-cdc1-492c-a54f-ca3d3bd8b953
title: 'IEventSubscription3 :: SubscriberPartitionID, propriété'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IEventSubscription3.SubscriberPartitionID
- IEventSubscription3.get_SubscriberPartitionID
- IEventSubscription3.put_SubscriberPartitionID
api_type:
- COM
api_location: ''
ms.openlocfilehash: b09c41ac1b3a90c3275daf7afa0cd90fe2bb905c
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "126916816"
---
# <a name="ieventsubscription3subscriberpartitionid-property"></a>IEventSubscription3 :: SubscriberPartitionID, propriété

GUID de la partition de l’abonné.

Cette propriété est en lecture/écriture.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT put_SubscriberPartitionID(
  [in]          BSTR bstrSubscriberPartitionID
);

HRESULT get_SubscriberPartitionID(
  [out, retval] BSTR *pbstrSubscriberPartitionID
);
```



## <a name="property-value"></a>Valeur de la propriété

Chaîne contenant le GUID de la partition de l’abonné.

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

 

 




