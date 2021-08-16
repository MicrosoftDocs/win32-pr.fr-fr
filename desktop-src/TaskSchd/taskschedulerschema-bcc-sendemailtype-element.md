---
title: Élément BCC (sendEmailType)
description: Contient les adresses de messagerie utilisées sur la ligne CCI d’un message électronique.
ms.assetid: c80407d0-3b3f-4efe-91de-7a3a7abc996f
keywords:
- Élément BCC Planificateur de tâches
topic_type:
- apiref
api_name:
- Bcc
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 1409d50a0317758534724b9e2c3a9796c4dd0cb40e666f58fc65ca0771da9762
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119659039"
---
# <a name="bcc-sendemailtype-element"></a>Élément BCC (sendEmailType)

Contient les adresses de messagerie utilisées sur la ligne CCI d’un message électronique.

``` syntax
<xs:element name="Bcc"
    type="string"
 />
```

L’élément **BCC** est défini par le type complexe [**sendEmailType**](taskschedulerschema-sendemailtype-complextype.md) .

## <a name="parent-element"></a>Élément parent



| Élément                                                                              | Dérivé de                                                           | Description                                                  |
|--------------------------------------------------------------------------------------|------------------------------------------------------------------------|--------------------------------------------------------------|
| [**SendEmail (actionGroup)**](taskschedulerschema-sendemail-actiongroup-element.md) | [**sendEMailType**](taskschedulerschema-sendemailtype-complextype.md) | Représente une action qui envoie un message électronique.<br/> |



## <a name="remarks"></a>Remarques

Pour le développement C++, consultez la [**propriété BCC de IEmailAction**](/windows/desktop/api/taskschd/nf-taskschd-iemailaction-get_bcc).

Pour le développement de scripts, consultez [**EmailAction. CCI**](emailaction-bcc.md).

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows \[Applications de bureau Vista uniquement\]<br/>       |
| Serveur minimal pris en charge<br/> | Windows Serveur 2008 \[ applications de bureau uniquement\]<br/> |



 

 





