---
description: Génère des déclarations d’implémentation pour les fonctions proxy d’abonnement/annulation d’abonnement pour les opérations de notification de type de port.
ms.assetid: 0e5b2232-c9bf-4741-921d-bb3bce4ee293
title: élément subscriptionFunctionDeclarations
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fb7389b30ef7da17f9466fa8aefd24fa04f4c99f
ms.sourcegitcommit: b6fe9acffad983c14864b8fe0296f6025cb1f961
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/26/2021
ms.locfileid: "107995456"
---
# <a name="subscriptionfunctiondeclarations-element"></a>élément subscriptionFunctionDeclarations

Génère des déclarations d’implémentation pour les fonctions proxy d’abonnement/annulation d’abonnement pour les opérations de notification de type de port.

## <a name="usage"></a>Usage

``` syntax
<subscriptionFunctionDeclarations
  extensible = "boolean">
  child elements
</subscriptionFunctionDeclarations>
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
| [**txt**](file.md)<br/> | Génère un fichier à partir du générateur de code.<br/> <br/> |



## <a name="element-information"></a>Informations sur les éléments



| Étiquette | Value |
|-------------------------------------|---------------|
| Système minimal pris en charge<br/> | Windows Vista |
| Peut être vide                        | Oui           |



 

 




