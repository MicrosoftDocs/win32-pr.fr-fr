---
title: Élément Server (sendEmailType)
description: Contient le serveur de messagerie utilisé pour envoyer le message électronique.
ms.assetid: 4c6084d1-70c5-4d8b-8fcb-ab4cd8aab441
keywords:
- Planificateur de tâches de l’élément serveur
topic_type:
- apiref
api_name:
- Server
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: d6052ebb5e648c040c321a311a6ba18313244ab20340d5a7f6c4185e3d35f5df
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119002247"
---
# <a name="server-sendemailtype-element"></a>Élément Server (sendEmailType)

Contient le serveur de messagerie utilisé pour envoyer le message électronique.

``` syntax
<xs:element name="Server"
    type="nonEmptyString"
 />
```

L’élément **Server** est défini par le type complexe [**sendEmailType**](taskschedulerschema-sendemailtype-complextype.md) .

## <a name="parent-element"></a>Élément parent



| Élément                                                                              | Dérivé de                                                           | Description                                                  |
|--------------------------------------------------------------------------------------|------------------------------------------------------------------------|--------------------------------------------------------------|
| [**SendEmail (actionGroup)**](taskschedulerschema-sendemail-actiongroup-element.md) | [**sendEMailType**](taskschedulerschema-sendemailtype-complextype.md) | Représente une action qui envoie un message électronique.<br/> |



## <a name="remarks"></a>Remarques

Pour le développement C++, consultez [**propriété de serveur de IEmailAction**](/windows/desktop/api/taskschd/nf-taskschd-iemailaction-get_server).

Pour le développement de scripts, consultez [**EmailAction. Server**](emailaction-server.md).

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows \[Applications de bureau Vista uniquement\]<br/>       |
| Serveur minimal pris en charge<br/> | Windows Serveur 2008 \[ applications de bureau uniquement\]<br/> |



 

 





