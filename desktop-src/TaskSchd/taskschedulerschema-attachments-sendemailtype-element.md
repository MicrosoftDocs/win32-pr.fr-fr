---
title: Élément Attachments (sendEmailType)
description: Contient une liste de pièces jointes dans le message électronique.
ms.assetid: 5ae22481-af70-42eb-a964-e63d800be17d
keywords:
- Élément Attachments Planificateur de tâches
topic_type:
- apiref
api_name:
- Attachments
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 67eed8f82f0caa27f44070bd109d4fa4560472eb
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103742772"
---
# <a name="attachments-sendemailtype-element"></a>Élément Attachments (sendEmailType)

Contient une liste de pièces jointes dans le message électronique.

``` syntax
<xs:element name="Attachments"
    type="attachmentsType"
 />
```

L’élément **Attachments** est défini par le type complexe [**sendEmailType**](taskschedulerschema-sendemailtype-complextype.md) .

## <a name="parent-element"></a>Élément parent



| Élément                                                                              | Dérivé de                                                           | Description                                                  |
|--------------------------------------------------------------------------------------|------------------------------------------------------------------------|--------------------------------------------------------------|
| [**SendEmail (actionGroup)**](taskschedulerschema-sendemail-actiongroup-element.md) | [**sendEMailType**](taskschedulerschema-sendemailtype-complextype.md) | Représente une action qui envoie un message électronique.<br/> |



## <a name="child-elements"></a>Éléments enfants



| Élément                                                          | Type                                                                    | Description                                                                                |
|------------------------------------------------------------------|-------------------------------------------------------------------------|--------------------------------------------------------------------------------------------|
| [**Fichier**](taskschedulerschema-file-attachmentstype-element.md) | [**nonEmptyString**](taskschedulerschema-nonemptystring-simpletype.md) | Spécifie le chemin d’accès à un fichier qui est envoyé en tant que pièce jointe dans un message électronique.<br/> |



## <a name="remarks"></a>Notes

Pour le développement C++, consultez la [**propriété Attachments de IEmailAction**](/windows/desktop/api/taskschd/nf-taskschd-iemailaction-get_attachments).

Pour le développement de scripts, consultez [**EmailAction. Attachments**](emailaction-attachments.md).

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|------------------------------------------------------|
| Client minimal pris en charge<br/> | Applications de \[ Bureau Windows Vista uniquement\]<br/>       |
| Serveur minimal pris en charge<br/> | Applications de bureau Windows Server 2008 \[ uniquement\]<br/> |



 

 





