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
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "126920252"
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

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|-------------------------------------|------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows \[Applications de bureau Vista uniquement\]<br/>       |
| Serveur minimal pris en charge<br/> | Windows Serveur 2008 \[ applications de bureau uniquement\]<br/> |



 

 





