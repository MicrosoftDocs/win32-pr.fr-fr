---
title: Title (élément showMessageType)
description: Contient le titre de la boîte de message.
ms.assetid: 089d2043-41ed-4050-b794-af24ab7ac8b9
keywords:
- Élément title Planificateur de tâches
topic_type:
- apiref
api_name:
- Title
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: ca5baa7135579ff673ba9b01a672a126924d1d49
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "126920256"
---
# <a name="title-showmessagetype-element"></a>Title (élément showMessageType)

Contient le titre de la boîte de message.

``` syntax
<xs:element name="Title"
    type="nonEmptyString"
 />
```

L’élément **title** est défini par le type complexe [**showMessageType**](taskschedulerschema-showmessagetype-complextype.md) .

## <a name="parent-element"></a>Élément parent



| Élément                                                                                  | Dérivé de                                                               | Description                                               |
|------------------------------------------------------------------------------------------|----------------------------------------------------------------------------|-----------------------------------------------------------|
| [**ShowMessage (actionGroup)**](taskschedulerschema-showmessage-actiongroup-element.md) | [**showMessageType**](taskschedulerschema-showmessagetype-complextype.md) | Représente une action qui affiche une boîte de message.<br/> |



## <a name="remarks"></a>Notes

Pour le développement C++, consultez [**propriété Title de IShowMessageAction**](/windows/desktop/api/taskschd/nf-taskschd-ishowmessageaction-get_title).

Pour le développement de scripts, consultez [**ShowMessageAction. title**](showmessageaction-title.md).

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|-------------------------------------|------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows \[Applications de bureau Vista uniquement\]<br/>       |
| Serveur minimal pris en charge<br/> | Windows Serveur 2008 \[ applications de bureau uniquement\]<br/> |



 

 





