---
title: Élément CC (sendEmailType)
description: Contient les adresses de messagerie utilisées sur la ligne CC d’un message électronique.
ms.assetid: cb8bc5b3-c352-43e3-bf28-d2090a519c7f
keywords:
- Élément CC Planificateur de tâches
topic_type:
- apiref
api_name:
- Cc
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 0bc49f2d7eebc2fbb1b5818fee2efa0e54f579a8
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104466026"
---
# <a name="cc-sendemailtype-element"></a>Élément CC (sendEmailType)

Contient les adresses de messagerie utilisées sur la ligne CC d’un message électronique.

``` syntax
<xs:element name="Cc"
    type="string"
 />
```

L’élément **CC** est défini par le type complexe [**sendEmailType**](taskschedulerschema-sendemailtype-complextype.md) .

## <a name="parent-element"></a>Élément parent



| Élément                                                                              | Dérivé de                                                           | Description                                                  |
|--------------------------------------------------------------------------------------|------------------------------------------------------------------------|--------------------------------------------------------------|
| [**SendEmail (actionGroup)**](taskschedulerschema-sendemail-actiongroup-element.md) | [**sendEMailType**](taskschedulerschema-sendemailtype-complextype.md) | Représente une action qui envoie un message électronique.<br/> |



## <a name="remarks"></a>Notes

Pour le développement C++, consultez la [**propriété CC de IEmailAction**](/windows/desktop/api/taskschd/nf-taskschd-iemailaction-get_cc).

Pour le développement de scripts, consultez [**EmailAction.cc**](emailaction-cc.md).

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|------------------------------------------------------|
| Client minimal pris en charge<br/> | Applications de \[ Bureau Windows Vista uniquement\]<br/>       |
| Serveur minimal pris en charge<br/> | Applications de bureau Windows Server 2008 \[ uniquement\]<br/> |



 

 





