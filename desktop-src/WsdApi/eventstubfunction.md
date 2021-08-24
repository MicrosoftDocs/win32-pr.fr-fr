---
description: Spécifie si les références de fonction stub doivent être incluses dans les structures d’opération dans les définitions de type de port pour les opérations de notification.
ms.assetid: 8a2fd7b2-e37b-465a-ba83-a68877a2e0c3
title: élément eventStubFunction
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 34e0b42416adc29c75fcafffedabf558bf6455df6cecf2bfebc344f747fff971
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119856718"
---
# <a name="eventstubfunction-element"></a>élément eventStubFunction

Spécifie si les références de fonction stub doivent être incluses dans les structures d’opération dans les définitions de type de port pour les opérations de notification.

## <a name="usage"></a>Usage

``` syntax
<eventStubFunction/>
```

## <a name="attributes"></a>Attributs

Il n’y a pas d’attributs.

## <a name="child-elements"></a>Éléments enfants

Il n’y a pas d’éléments enfants.

## <a name="parent-elements"></a>Éléments parents



| Élément                                                       | Description                                                  |
|---------------------------------------------------------------|--------------------------------------------------------------|
| [**portTypeDefinitions**](porttypedefinitions.md)<br/> | Génère des constantes C pour les types de ports.<br/> <br/> |



## <a name="remarks"></a>Remarques

Les références de fonction stub se trouvent dans des scénarios clients pour les opérations de notification (événements).

Les valeurs valides pour cet élément sont 1 (TRUE/stub Function References incluses) et 0 (FALSe/aucune référence à la fonction stub incluse).

## <a name="element-information"></a>Informations sur les éléments



| Étiquette | Valeur |
|-------------------------------------|---------------|
| Système minimal pris en charge<br/> | Windows Vista |
| Peut être vide                        | Oui           |



 

 




