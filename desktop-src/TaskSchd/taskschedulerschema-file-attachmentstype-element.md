---
title: Élément file (attachmentsType)
description: Contient le chemin d’accès à un fichier envoyé sous forme de pièce jointe dans un message électronique.
ms.assetid: a53f591b-ac59-43b4-8cc2-661e76d307cc
keywords:
- Élément file Planificateur de tâches
topic_type:
- apiref
api_name:
- File
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: ed07d4b31f9054f6caefcff0585d9683faa90c7f
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127228840"
---
# <a name="file-attachmentstype-element"></a>Élément file (attachmentsType)

Contient le chemin d’accès à un fichier envoyé sous forme de pièce jointe dans un message électronique.

``` syntax
<xs:element name="File"
    type="nonEmptyString"
 />
```

L’élément **file** est défini par le type complexe [**attachmentsType**](taskschedulerschema-attachmentstype-complextype.md) .

## <a name="parent-element"></a>Élément parent



| Élément                                                                                      | Dérivé de                                                               | Description                                                     |
|----------------------------------------------------------------------------------------------|----------------------------------------------------------------------------|-----------------------------------------------------------------|
| [**Pièces jointes (sendEmailType)**](taskschedulerschema-attachments-sendemailtype-element.md) | [**attachmentsType**](taskschedulerschema-attachmentstype-complextype.md) | Contient une liste de pièces jointes dans le message électronique.<br/> |



## <a name="remarks"></a>Notes

Pour le développement C++, consultez la [**propriété Attachments de IEmailAction**](/windows/desktop/api/taskschd/nf-taskschd-iemailaction-get_attachments).

Pour le développement de scripts, consultez [**EmailAction. Attachments**](emailaction-attachments.md).

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|-------------------------------------|------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows \[Applications de bureau Vista uniquement\]<br/>       |
| Serveur minimal pris en charge<br/> | Windows Serveur 2008 \[ applications de bureau uniquement\]<br/> |



 

 





