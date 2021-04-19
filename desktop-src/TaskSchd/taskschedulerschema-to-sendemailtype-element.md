---
title: À (sendEmailType) (élément)
description: Contient les adresses de messagerie auxquelles le courrier électronique sera envoyé.
ms.assetid: bf3aa878-967b-4ebd-9397-a2a499686a9f
keywords:
- À l’élément Planificateur de tâches
topic_type:
- apiref
api_name:
- To
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: b9e0643220915ecb1c8f2cd1fe842e0dc3f21d8f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "106510522"
---
# <a name="to-sendemailtype-element"></a>À (sendEmailType) (élément)

Contient les adresses de messagerie auxquelles le courrier électronique sera envoyé.

``` syntax
<xs:element name="To"
    type="string"
 />
```

L’élément **to** est défini par le type complexe [**sendEmailType**](taskschedulerschema-sendemailtype-complextype.md) .

## <a name="parent-element"></a>Élément parent



| Élément                                                                              | Dérivé de                                                           | Description                                                  |
|--------------------------------------------------------------------------------------|------------------------------------------------------------------------|--------------------------------------------------------------|
| [**SendEmail (actionGroup)**](taskschedulerschema-sendemail-actiongroup-element.md) | [**sendEMailType**](taskschedulerschema-sendemailtype-complextype.md) | Représente une action qui envoie un message électronique.<br/> |



## <a name="remarks"></a>Notes

Pour le développement C++, consultez la [**propriété to de IEmailAction**](/windows/desktop/api/taskschd/nf-taskschd-iemailaction-get_to).

Pour le développement de scripts, consultez [**EmailAction.to**](emailaction-to.md).

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|------------------------------------------------------|
| Client minimal pris en charge<br/> | Applications de \[ Bureau Windows Vista uniquement\]<br/>       |
| Serveur minimal pris en charge<br/> | Applications de bureau Windows Server 2008 \[ uniquement\]<br/> |



 

 





