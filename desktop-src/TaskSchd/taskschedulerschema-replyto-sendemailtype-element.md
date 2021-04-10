---
title: Élément ReplyTo (sendEmailType)
description: Contient les adresses de messagerie auxquelles il est répondu dans le message électronique.
ms.assetid: c09b72f6-de2c-41dc-942c-d6184863e33c
keywords:
- ReplyTo, élément Planificateur de tâches
topic_type:
- apiref
api_name:
- ReplyTo
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 02055539d4557a60f182981f0d9cd7d3e1a63ca4
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104106357"
---
# <a name="replyto-sendemailtype-element"></a>Élément ReplyTo (sendEmailType)

Contient les adresses de messagerie auxquelles il est répondu dans le message électronique.

``` syntax
<xs:element name="ReplyTo"
    type="string"
 />
```

L’élément **ReplyTo** est défini par le type complexe [**sendEmailType**](taskschedulerschema-sendemailtype-complextype.md) .

## <a name="parent-element"></a>Élément parent



| Élément                                                                              | Dérivé de                                                           | Description                                                  |
|--------------------------------------------------------------------------------------|------------------------------------------------------------------------|--------------------------------------------------------------|
| [**SendEmail (actionGroup)**](taskschedulerschema-sendemail-actiongroup-element.md) | [**sendEMailType**](taskschedulerschema-sendemailtype-complextype.md) | Représente une action qui envoie un message électronique.<br/> |



## <a name="remarks"></a>Notes

Pour le développement C++, consultez la [**propriété ReplyTo de IEmailAction**](/windows/desktop/api/taskschd/nf-taskschd-iemailaction-get_replyto).

Pour le développement de scripts, consultez [**EmailAction. ReplyTo**](emailaction-replyto.md).

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|------------------------------------------------------|
| Client minimal pris en charge<br/> | Applications de \[ Bureau Windows Vista uniquement\]<br/>       |
| Serveur minimal pris en charge<br/> | Applications de bureau Windows Server 2008 \[ uniquement\]<br/> |



 

 





