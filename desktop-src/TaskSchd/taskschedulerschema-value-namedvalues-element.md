---
title: Élément Value (namedValues)
description: Contient la valeur associée à un nom dans une paire nom-valeur.
ms.assetid: d5582b55-0b9b-4fed-a425-9d15a1a62fb7
keywords:
- Élément Value Planificateur de tâches
topic_type:
- apiref
api_name:
- Value
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 8afa12156a15ff399f3cbc967a5fd9c612df582b
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "126920212"
---
# <a name="value-namedvalues-element"></a>Élément Value (namedValues)

Contient la valeur associée à un nom dans une paire nom-valeur.

``` syntax
<xs:element name="Value"
    type="namedValue"
    minOccurs="1"
    maxOccurs="32"
 />
```

L’élément **value** est défini par le type complexe [**namedValues**](taskschedulerschema-namedvalues-complextype.md) .

## <a name="parent-element"></a>Élément parent



| Élément                                                                                              | Dérivé de                                                       | Description                                                                                                                                                                                                                                                                                                                                                                       |
|------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**ValueQueries (eventTriggerType)**](taskschedulerschema-valuequeries-eventtriggertype-element.md) | [**namedValues**](taskschedulerschema-namedvalues-complextype.md) | Spécifie une collection de requêtes XPath nommées. Chaque requête de la collection est appliquée au dernier fichier XML d’événement correspondant retourné par la requête d’abonnement spécifiée dans l’élément [**subscription**](taskschedulerschema-subscription-eventtriggertype-element.md) . Le nom de la requête peut être utilisé en tant que variable dans le message d’une action ShowMessage.<br/> |



## <a name="remarks"></a>Notes

Pour le développement C++, consultez la [**propriété Value de ITaskNamedValuePair**](/windows/desktop/api/taskschd/nf-taskschd-itasknamedvaluepair-get_value).

Pour le développement de scripts, consultez [**TaskNamedValuePair. Value**](tasknamedvaluepair-value.md).

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|-------------------------------------|------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows \[Applications de bureau Vista uniquement\]<br/>       |
| Serveur minimal pris en charge<br/> | Windows Serveur 2008 \[ applications de bureau uniquement\]<br/> |



 

 





