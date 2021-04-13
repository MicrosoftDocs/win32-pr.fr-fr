---
title: Élément Body (showMessageType)
description: Contient le texte à afficher dans le corps de la boîte de message.
ms.assetid: 69ea872a-7ca1-4464-9380-b35f74c9cb8e
keywords:
- Élément Body Planificateur de tâches
topic_type:
- apiref
api_name:
- Body
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 3486601153f8e9dd7dac14f83800dae00a79a9f8
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104465810"
---
# <a name="body-showmessagetype-element"></a>Élément Body (showMessageType)

Contient le texte à afficher dans le corps de la boîte de message.

``` syntax
<xs:element name="Body"
    type="nonEmptyString"
 />
```

L’élément **Body** est défini par le type complexe [**showMessageType**](taskschedulerschema-showmessagetype-complextype.md) .

## <a name="parent-element"></a>Élément parent



| Élément                                                                                  | Dérivé de                                                               | Description                                               |
|------------------------------------------------------------------------------------------|----------------------------------------------------------------------------|-----------------------------------------------------------|
| [**ShowMessage (actionGroup)**](taskschedulerschema-showmessage-actiongroup-element.md) | [**showMessageType**](taskschedulerschema-showmessagetype-complextype.md) | Représente une action qui affiche une boîte de message.<br/> |



## <a name="remarks"></a>Notes

Pour le développement C++, consultez la [**propriété MessageBody de IShowMessageAction**](/windows/desktop/api/taskschd/nf-taskschd-ishowmessageaction-get_messagebody).

Pour le développement de scripts, consultez [**ShowMessageAction. MessageBody**](showmessageaction-messagebody.md).

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|------------------------------------------------------|
| Client minimal pris en charge<br/> | Applications de \[ Bureau Windows Vista uniquement\]<br/>       |
| Serveur minimal pris en charge<br/> | Applications de bureau Windows Server 2008 \[ uniquement\]<br/> |



 

 





