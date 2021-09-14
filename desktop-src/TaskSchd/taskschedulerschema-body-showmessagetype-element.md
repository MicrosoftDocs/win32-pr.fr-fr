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
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127324679"
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

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|-------------------------------------|------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows \[Applications de bureau Vista uniquement\]<br/>       |
| Serveur minimal pris en charge<br/> | Windows Serveur 2008 \[ applications de bureau uniquement\]<br/> |



 

 





