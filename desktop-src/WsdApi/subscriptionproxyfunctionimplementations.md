---
description: Génère des implémentations pour les fonctions proxy d’abonnement/annulation d’abonnement pour les opérations de notification de type de port.
ms.assetid: aa26a3f1-df1e-4caa-9ada-6f4a6627b6b8
title: élément subscriptionProxyFunctionImplementations
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bf0abc98e0e9bebd4ff2185d669402c0dae025c07bc4af84be3116dda97b6657
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118991569"
---
# <a name="subscriptionproxyfunctionimplementations-element"></a>élément subscriptionProxyFunctionImplementations

Génère des implémentations pour les fonctions proxy d’abonnement/annulation d’abonnement pour les opérations de notification de type de port.

## <a name="usage"></a>Usage

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
| [**operation**](operation.md)<br/>                         | Spécifie une opération pour laquelle du code doit être généré.<br/> <br/>                       |
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
| [**txt**](file.md)<br/> | Génère un fichier à partir du générateur de code.<br/> <br/> |



## <a name="element-information"></a>Informations sur les éléments



| Étiquette | Valeur |
|-------------------------------------|---------------|
| Système minimal pris en charge<br/> | Windows Vista |
| Peut être vide                        | Oui           |



 

 




