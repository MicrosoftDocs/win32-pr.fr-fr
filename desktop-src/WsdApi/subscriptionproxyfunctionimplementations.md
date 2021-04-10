---
description: Génère des implémentations pour les fonctions proxy d’abonnement/annulation d’abonnement pour les opérations de notification de type de port.
ms.assetid: aa26a3f1-df1e-4caa-9ada-6f4a6627b6b8
title: élément subscriptionProxyFunctionImplementations
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fb57fa21910f9b39440257bc72918519b35c6a57
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104112983"
---
# <a name="subscriptionproxyfunctionimplementations-element"></a>élément subscriptionProxyFunctionImplementations

Génère des implémentations pour les fonctions proxy d’abonnement/annulation d’abonnement pour les opérations de notification de type de port.

## <a name="usage"></a>Utilisation

``` syntax
<subscriptionProxyFunctionImplementations
  extensible = "boolean">
  child elements
</subscriptionProxyFunctionImplementations>
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
| [**proxyClass**](proxyclass.md)<br/>                       | Spécifie le nom de la classe de proxy côté client.<br/> <br/>                              |



### <a name="child-element-sequence"></a>Séquence d’éléments enfants

``` syntax
(
  portType?, 
  operation*, 
  proxyClass?, 
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



 

 




