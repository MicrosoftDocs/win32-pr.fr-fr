---
description: Génère des déclarations IDL pour les fonctions de proxy d’abonnement/annulation d’abonnement pour les opérations de notification de type de port.
ms.assetid: 240ef2b3-ed72-45bb-b653-441c4e5540b5
title: élément subscriptionIdlFunctionDeclarations
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8e1eba60e327778efb1589436a09e62d043d2960
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103867602"
---
# <a name="subscriptionidlfunctiondeclarations-element"></a>élément subscriptionIdlFunctionDeclarations

Génère des déclarations IDL pour les fonctions de proxy d’abonnement/annulation d’abonnement pour les opérations de notification de type de port.

## <a name="usage"></a>Utilisation

``` syntax
<subscriptionIdlFunctionDeclarations
  extensible = "boolean">
  child elements
</subscriptionIdlFunctionDeclarations>
```

## <a name="attributes"></a>Attributs



| Attribut                 | Type               | Obligatoire      | Description                                                                                                                   |
|---------------------------|--------------------|---------------|-------------------------------------------------------------------------------------------------------------------------------|
| **EAP**<br/> | boolean<br/> | Non<br/> | La possibilité d’ajouter des points d’extensibilité aux fonctions et aux interfaces. Cette valeur est toujours définie sur true.<br/> <br/> |



## <a name="child-elements"></a>Éléments enfants



| Élément                                                           | Description                                                                                            |
|-------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------|
| [**notificationInterface**](notificationinterface.md)<br/> | Spécifie le nom de l’interface de notification utilisée avec les abonnements aux événements.<br/> <br/> |
| [**opération**](operation.md)<br/>                         | Spécifie une opération pour laquelle du code doit être généré.<br/> <br/>                       |
| [**portType**](porttype.md)<br/>                           | Spécifie le type de port pour lequel le code doit être généré.<br/> <br/>                      |



### <a name="child-element-sequence"></a>Séquence d’éléments enfants

``` syntax
(
  portType?, 
  operation*, 
  notificationInterface?
)
```

## <a name="parent-elements"></a>Éléments parents



| Élément                         | Description                                                    |
|---------------------------------|----------------------------------------------------------------|
| [**fichier**](file.md)<br/> | Génère un fichier à partir du générateur de code.<br/> <br/> |



## <a name="element-information"></a>Informations sur les éléments



|                                     |               |
|-------------------------------------|---------------|
| Système minimal pris en charge<br/> | Windows Vista |
| Peut être vide                        | Oui           |



 

 




