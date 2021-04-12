---
description: Spécifie si les paramètres utilisés pour passer les informations d’erreur sont inclus dans les fonctions générées.
ms.assetid: aba78d50-f884-416a-b022-bb03416aad11
title: élément faultInfo
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0f0fd65a7214f61a0b2fa6bb8f44d9a8cadbef07
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104203351"
---
# <a name="faultinfo-element"></a>élément faultInfo

Spécifie si les paramètres utilisés pour passer les informations d’erreur sont inclus dans les fonctions générées.

## <a name="usage"></a>Utilisation

``` syntax
<faultInfo/>
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
| [**stubDefinitions**](stubdefinitions.md)<br/>                           | Génère des implémentations pour les fonctions stub pour les opérations de type de port.<br/> <br/>              |



## <a name="remarks"></a>Notes

Les valeurs possibles sont 1 (paramètres d’erreur inclus) et 0 (paramètres d’erreur exclus). Par défaut, les paramètres d’erreur sont exclus.

## <a name="element-information"></a>Informations sur les éléments



|                                     |               |
|-------------------------------------|---------------|
| Système minimal pris en charge<br/> | Windows Vista |
| Peut être vide                        | Oui           |



 

 




