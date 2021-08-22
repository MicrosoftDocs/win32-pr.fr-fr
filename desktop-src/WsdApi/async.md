---
description: Spécifie si les opérations asynchrones sont incluses dans les fonctions proxy générées.
ms.assetid: 7b57d5c6-589b-4e03-bfcf-1faa671ebd77
title: élément Async
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2597e0ed22fe9ccefa053891c0bd67ee76fae567847925de74faa1513de5faf1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119049717"
---
# <a name="async-element"></a>élément Async

Spécifie si les opérations asynchrones sont incluses dans les fonctions proxy générées.

## <a name="usage"></a>Usage

``` syntax
<async/>
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



## <a name="remarks"></a>Remarques

Les valeurs possibles sont 1 (opérations asynchrones incluses) et 0 (opérations asynchrones par défaut exclues).

Un proxy peut avoir des versions asynchrones et synchrones des mêmes opérations.

## <a name="element-information"></a>Informations sur les éléments



| Étiquette | Valeur |
|-------------------------------------|---------------|
| Système minimal pris en charge<br/> | Windows Vista |
| Peut être vide                        | Oui           |



 

 




