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
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103743317"
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

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|------------------------------------------------------|
| Client minimal pris en charge<br/> | Applications de \[ Bureau Windows Vista uniquement\]<br/>       |
| Serveur minimal pris en charge<br/> | Applications de bureau Windows Server 2008 \[ uniquement\]<br/> |



 

 





