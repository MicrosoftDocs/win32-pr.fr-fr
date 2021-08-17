---
description: Génère des déclarations IDL pour les fonctions de proxy d’abonnement/annulation d’abonnement pour les opérations de notification de type de port.
ms.assetid: 240ef2b3-ed72-45bb-b653-441c4e5540b5
title: élément subscriptionIdlFunctionDeclarations
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3998103d04250206ef382f822e329210b83471c69dcc51b401fcfbc241460729
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119130611"
---
# <a name="subscriptionidlfunctiondeclarations-element"></a>élément subscriptionIdlFunctionDeclarations

Génère des déclarations IDL pour les fonctions de proxy d’abonnement/annulation d’abonnement pour les opérations de notification de type de port.

## <a name="usage"></a>Usage

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
| [**operation**](operation.md)<br/>                         | Spécifie une opération pour laquelle du code doit être généré.<br/> <br/>                       |
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
| [**txt**](file.md)<br/> | Génère un fichier à partir du générateur de code.<br/> <br/> |



## <a name="element-information"></a>Informations sur les éléments



| Étiquette | Valeur |
|-------------------------------------|---------------|
| Système minimal pris en charge<br/> | Windows Vista |
| Peut être vide                        | Oui           |



 

 




