---
description: Génère des implémentations pour les fonctions stub pour les opérations de type de port.
ms.assetid: 69899302-db54-493b-90de-596750be566f
title: élément stubDefinitions
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c6676cfc6cf55aa9c9961bd614506500d847def0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106519967"
---
# <a name="stubdefinitions-element"></a>élément stubDefinitions

Génère des implémentations pour les fonctions stub pour les opérations de type de port.

## <a name="usage"></a>Utilisation

``` syntax
<stubDefinitions>
  child elements
</stubDefinitions>
```

## <a name="attributes"></a>Attributs

Il n’y a pas d’attributs.

## <a name="child-elements"></a>Éléments enfants



| Élément                                                         | Description                                                                                                             |
|-----------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------|
| [**annulateur**](deallocator.md)<br/>                   | Spécifie le type de annulateur à utiliser par une fonction stub.<br/> <br/>                                 |
| [**eventArg**](eventarg.md)<br/>                         | Spécifie si les arguments d’événement associés sont inclus dans les fonctions générées.<br/> <br/>               |
| [**événements**](events.md)<br/>                             | Spécifie si les événements connexes sont inclus dans les fonctions générées.<br/> <br/>                        |
| [**faultInfo**](faultinfo.md)<br/>                       | Spécifie si les paramètres utilisés pour passer les informations d’erreur sont inclus dans les fonctions générées.<br/> <br/> |
| [**opération**](operation.md)<br/>                       | Spécifie une opération pour laquelle du code doit être généré.<br/> <br/>                                        |
| [**operationDeallocator**](operationdeallocator.md)<br/> | Spécifie le type de annulateur à utiliser par la fonction stub d’une opération.<br/> <br/>                    |
| [**portType**](porttype.md)<br/>                         | Spécifie le type de port pour lequel le code doit être généré.<br/> <br/>                                       |
| [**serverClass**](serverclass.md)<br/>                   | Spécifie le nom de la classe de serveur côté hôte.<br/> <br/>                                                |



### <a name="child-element-sequence"></a>Séquence d’éléments enfants

``` syntax
(
  portType?, 
  operation*, 
  serverClass, 
  eventArg?, 
  events?, 
  operationDeallocator*, 
  deallocator?, 
  faultInfo?
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
| Peut être vide                        | Non            |



 

 




