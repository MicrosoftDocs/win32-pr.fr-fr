---
description: Spécifie si les événements connexes sont inclus dans les fonctions générées.
ms.assetid: 23ca463c-b305-496b-a1e3-58dbb793f17e
title: élément Events
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2571cc8e9820ca38beb649b3c227fb1c01f61c50
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104202271"
---
# <a name="events-element"></a>élément Events

Spécifie si les événements connexes sont inclus dans les fonctions générées.

## <a name="usage"></a>Utilisation

``` syntax
<events/>
```

## <a name="attributes"></a>Attributs

Il n’y a pas d’attributs.

## <a name="child-elements"></a>Éléments enfants

Il n’y a pas d’éléments enfants.

## <a name="parent-elements"></a>Éléments parents



| Élément                                                                         | Description                                                                                                |
|---------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------|
| [**functionDeclarations**](functiondeclarations.md)<br/>                 | Génère des déclarations d’implémentation pour les fonctions de proxy pour les opérations de type de port.<br/> <br/> |
| [**idlFunctionDeclarations**](idlfunctiondeclarations.md)<br/>           | Génère des déclarations IDL pour les fonctions de proxy pour les opérations de type de port.<br/> <br/>            |
| [**proxyFunctionImplementations**](proxyfunctionimplementations.md)<br/> | Génère des implémentations pour les fonctions proxy pour les opérations de type de port.<br/> <br/>             |
| [**stubDeclarations**](stubdeclarations.md)<br/>                         | Génère des déclarations pour les fonctions stub pour les opérations de type de port.<br/> <br/>                 |
| [**stubDefinitions**](stubdefinitions.md)<br/>                           | Génère des implémentations pour les fonctions stub pour les opérations de type de port.<br/> <br/>              |



## <a name="remarks"></a>Notes

Les valeurs possibles sont 1 (événements inclus) et 0 (valeur par défaut, événements exclus).

## <a name="element-information"></a>Informations sur les éléments



|                                     |               |
|-------------------------------------|---------------|
| Système minimal pris en charge<br/> | Windows Vista |
| Peut être vide                        | Oui           |



 

 




