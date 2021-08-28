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
ms.openlocfilehash: 2af801385c74fa26221556b713faf8db915037ef4cf7439d71a2e2d4004193d8
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120100029"
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



## <a name="remarks"></a>Remarques

Pour le développement C++, consultez la [**propriété HeaderFields de IEmailAction**](/windows/desktop/api/taskschd/nf-taskschd-iemailaction-get_headerfields).

Pour le développement de scripts, consultez [**EmailAction. HeaderFields**](emailaction-headerfields.md).

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows \[Applications de bureau Vista uniquement\]<br/>       |
| Serveur minimal pris en charge<br/> | Windows Serveur 2008 \[ applications de bureau uniquement\]<br/> |



 

 





