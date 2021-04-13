---
title: Élément HeaderFields (sendEmailType)
description: Spécifie les champs d’en-tête et leurs valeurs utilisées dans l’en-tête du message électronique.
ms.assetid: 6261f32e-3012-4ce7-b407-699374596333
keywords:
- Élément HeaderFields Planificateur de tâches
topic_type:
- apiref
api_name:
- HeaderFields
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 9d108f1c31b8253046ccdbf09312df4f54c7335d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104508850"
---
# <a name="headerfields-sendemailtype-element"></a>Élément HeaderFields (sendEmailType)

Spécifie les champs d’en-tête et leurs valeurs utilisées dans l’en-tête du message électronique.

``` syntax
<xs:element name="HeaderFields"
    type="headerFieldsType"
 />
```

L’élément **HeaderFields** est défini par le type complexe [**sendEmailType**](taskschedulerschema-sendemailtype-complextype.md) .

## <a name="parent-element"></a>Élément parent



| Élément                                                                              | Dérivé de                                                           | Description                                                  |
|--------------------------------------------------------------------------------------|------------------------------------------------------------------------|--------------------------------------------------------------|
| [**SendEmail (actionGroup)**](taskschedulerschema-sendemail-actiongroup-element.md) | [**sendEMailType**](taskschedulerschema-sendemailtype-complextype.md) | Représente une action qui envoie un message électronique.<br/> |



## <a name="child-elements"></a>Éléments enfants



| Élément                                                                         | Type                                                                       | Description                                                    |
|---------------------------------------------------------------------------------|----------------------------------------------------------------------------|----------------------------------------------------------------|
| [**HeaderField**](taskschedulerschema-headerfield-headerfieldstype-element.md) | [**headerFieldType**](taskschedulerschema-headerfieldtype-complextype.md) | Contient un champ pour un en-tête dans un message électronique. <br/> |



## <a name="remarks"></a>Notes

Pour le développement C++, consultez la [**propriété HeaderFields de IEmailAction**](/windows/desktop/api/taskschd/nf-taskschd-iemailaction-get_headerfields).

Pour le développement de scripts, consultez [**EmailAction. HeaderFields**](emailaction-headerfields.md).

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|------------------------------------------------------|
| Client minimal pris en charge<br/> | Applications de \[ Bureau Windows Vista uniquement\]<br/>       |
| Serveur minimal pris en charge<br/> | Applications de bureau Windows Server 2008 \[ uniquement\]<br/> |



 

 





