---
title: Élément Subject (sendEmailType)
description: Contient l’objet du message électronique.
ms.assetid: 2ccaa983-4dca-4e45-ba8d-2a93e23f7e8c
keywords:
- Élément subject Planificateur de tâches
topic_type:
- apiref
api_name:
- Subject
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: b3b4871f8d61603ea77c7699a9993d29e2fc0187
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104519121"
---
# <a name="subject-sendemailtype-element"></a>Élément Subject (sendEmailType)

Contient l’objet du message électronique.

``` syntax
<xs:element name="Subject"
    type="string"
 />
```

L’élément **Subject** est défini par le type complexe [**sendEmailType**](taskschedulerschema-sendemailtype-complextype.md) .

## <a name="parent-element"></a>Élément parent



| Élément                                                                              | Dérivé de                                                           | Description                                                  |
|--------------------------------------------------------------------------------------|------------------------------------------------------------------------|--------------------------------------------------------------|
| [**SendEmail (actionGroup)**](taskschedulerschema-sendemail-actiongroup-element.md) | [**sendEMailType**](taskschedulerschema-sendemailtype-complextype.md) | Représente une action qui envoie un message électronique.<br/> |



## <a name="remarks"></a>Notes

Pour le développement C++, consultez la [**propriété Subject de IEmailAction**](/windows/desktop/api/taskschd/nf-taskschd-iemailaction-get_subject).

Pour le développement de scripts, consultez [**EmailAction. Subject**](emailaction-subject.md).

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|------------------------------------------------------|
| Client minimal pris en charge<br/> | Applications de \[ Bureau Windows Vista uniquement\]<br/>       |
| Serveur minimal pris en charge<br/> | Applications de bureau Windows Server 2008 \[ uniquement\]<br/> |



 

 





