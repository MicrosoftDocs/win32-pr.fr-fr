---
description: Génère des implémentations pour les fonctions proxy pour les opérations de type de port.
ms.assetid: 9505ee5f-fdb9-41b8-9537-0c5d29f90168
title: élément proxyFunctionImplementations
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 53a27e217cfa3d0a9efd204a1b18c7b2f0ca16f9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103867345"
---
# <a name="proxyfunctionimplementations-element"></a>élément proxyFunctionImplementations

Génère des implémentations pour les fonctions proxy pour les opérations de type de port.

## <a name="usage"></a>Utilisation

``` syntax
<proxyFunctionImplementations>
  child elements
</proxyFunctionImplementations>
```

## <a name="attributes"></a>Attributs

Il n’y a pas d’attributs.

## <a name="child-elements"></a>Éléments enfants



| Élément                                     | Description                                                                                                             |
|---------------------------------------------|-------------------------------------------------------------------------------------------------------------------------|
| [**async**](async.md)<br/>           | Spécifie si les opérations asynchrones sont incluses dans les fonctions proxy générées.<br/> <br/>         |
| [**événements**](events.md)<br/>         | Spécifie si les événements connexes sont inclus dans les fonctions générées.<br/> <br/>                        |
| [**faultInfo**](faultinfo.md)<br/>   | Spécifie si les paramètres utilisés pour passer les informations d’erreur sont inclus dans les fonctions générées.<br/> <br/> |
| [**opération**](operation.md)<br/>   | Spécifie une opération pour laquelle du code doit être généré.<br/> <br/>                                        |
| [**portType**](porttype.md)<br/>     | Spécifie le type de port pour lequel le code doit être généré.<br/> <br/>                                       |
| [**proxyClass**](proxyclass.md)<br/> | Spécifie le nom de la classe de proxy côté client.<br/> <br/>                                               |



### <a name="child-element-sequence"></a>Séquence d’éléments enfants

``` syntax
(
  portType?, 
  operation*, 
  proxyClass?, 
  events?, 
  async?, 
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
| Peut être vide                        | Oui           |



 

 




