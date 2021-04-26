---
description: Génère des implémentations pour les fonctions proxy pour les opérations de type de port.
ms.assetid: 9505ee5f-fdb9-41b8-9537-0c5d29f90168
title: élément proxyFunctionImplementations
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3e9f03834ca59ede41f2f3c3dff00d7dacdd54db
ms.sourcegitcommit: b6fe9acffad983c14864b8fe0296f6025cb1f961
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/26/2021
ms.locfileid: "107995756"
---
# <a name="proxyfunctionimplementations-element"></a>élément proxyFunctionImplementations

Génère des implémentations pour les fonctions proxy pour les opérations de type de port.

## <a name="usage"></a>Usage

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
| [**txt**](file.md)<br/> | Génère un fichier à partir du générateur de code.<br/> <br/> |



## <a name="element-information"></a>Informations sur les éléments



| Étiquette | Value |
|-------------------------------------|---------------|
| Système minimal pris en charge<br/> | Windows Vista |
| Peut être vide                        | Oui           |



 

 




