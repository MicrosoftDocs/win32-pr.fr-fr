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
ms.openlocfilehash: 793b23bc6b9d75ac809c42063fa9c300542705b718cd22253f6f2d3a1a76caa8
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120125849"
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



## <a name="remarks"></a>Remarques

Pour le développement C++, consultez la [**propriété Attachments de IEmailAction**](/windows/desktop/api/taskschd/nf-taskschd-iemailaction-get_attachments).

Pour le développement de scripts, consultez [**EmailAction. Attachments**](emailaction-attachments.md).

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows \[Applications de bureau Vista uniquement\]<br/>       |
| Serveur minimal pris en charge<br/> | Windows Serveur 2008 \[ applications de bureau uniquement\]<br/> |



 

 





