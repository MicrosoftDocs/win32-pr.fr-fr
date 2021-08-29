---
title: Windows Types de données du collecteur d’événements (Evcoll. h)
description: les types de données du collecteur d’événements Windows sont utilisés en tant que types de variables objet d’abonnement d’événement, types de paramètres de fonction et types de retour de fonction.
ms.assetid: b78bdaf8-e034-40fe-acf8-632313e4fd94
ms.tgt_platform: multiple
keywords:
- EC_HANDLE
- EC_OBJECT_ARRAY_PROPERTY_HANDLE
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a8d0a3a0887fccebbd5cfb45042eaa59895febfa1001af93eed1161e9d33f8b0
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119620569"
---
# <a name="windows-event-collector-data-types"></a>Windows Types de données du collecteur d’événements

les types de données du collecteur d’événements Windows sont utilisés en tant que types de variables objet d’abonnement d’événement, types de paramètres de fonction et types de retour de fonction.


```C++
typedef HANDLE EC_HANDLE;
typedef HANDLE EC_OBJECT_ARRAY_PROPERTY_HANDLE;
```



<dl> <dt>

**\_handle EC**
</dt> <dd>

Handle vers un objet d’abonnement. Utilisé pour représenter un abonnement au collecteur d’événements.

</dd> <dt>

**\_handle de \_ propriété du tableau d’objets EC \_ \_**
</dt> <dd>

Handle vers un tableau de valeurs de propriété pour les sources d’événements d’un abonnement. Le descripteur de tableau est retourné par la méthode [**EcGetSubscriptionProperty**](/windows/desktop/api/Evcoll/nf-evcoll-ecgetsubscriptionproperty) lorsque la valeur **EcSubscriptionEventSources** est passée dans le paramètre *PropertyId* .

</dd> </dl>

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows Vista<br/>                                                            |
| Serveur minimal pris en charge<br/> | Windows Server 2008<br/>                                                      |
| En-tête<br/>                   | <dl> <dt>Evcoll. h</dt> </dl> |



 

 





