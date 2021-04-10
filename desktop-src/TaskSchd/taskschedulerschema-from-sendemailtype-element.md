---
title: Élément from (sendEmailType)
description: Contient l’adresse e-mail de l’expéditeur de l’e-mail.
ms.assetid: b80733de-e050-4026-a2fe-f63833ec2660
keywords:
- À partir de l’élément Planificateur de tâches
topic_type:
- apiref
api_name:
- From
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 9f50704212fe6a4fec7ce0fc21bacd7ea33e402c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104032646"
---
# <a name="from-sendemailtype-element"></a>Élément from (sendEmailType)

Contient l’adresse e-mail de l’expéditeur de l’e-mail.

``` syntax
<xs:element name="From"
    type="string"
 />
```

L’élément **from** est défini par le type complexe [**sendEmailType**](taskschedulerschema-sendemailtype-complextype.md) .

## <a name="parent-element"></a>Élément parent



| Élément                                                                              | Dérivé de                                                           | Description                                                  |
|--------------------------------------------------------------------------------------|------------------------------------------------------------------------|--------------------------------------------------------------|
| [**SendEmail (actionGroup)**](taskschedulerschema-sendemail-actiongroup-element.md) | [**sendEMailType**](taskschedulerschema-sendemailtype-complextype.md) | Représente une action qui envoie un message électronique.<br/> |



## <a name="remarks"></a>Notes

Pour le développement C++, consultez [**from property of IEmailAction**](/windows/desktop/api/taskschd/nf-taskschd-iemailaction-get_from).

Pour le développement de scripts, consultez [**EmailAction. from**](emailaction-from.md).

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|------------------------------------------------------|
| Client minimal pris en charge<br/> | Applications de \[ Bureau Windows Vista uniquement\]<br/>       |
| Serveur minimal pris en charge<br/> | Applications de bureau Windows Server 2008 \[ uniquement\]<br/> |



 

 





