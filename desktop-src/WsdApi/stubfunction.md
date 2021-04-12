---
description: Spécifie si les références de fonction stub doivent être incluses dans les structures d’opération dans les définitions de type de port pour les opérations unidirectionnelles et bidirectionnelles.
ms.assetid: 2547f71d-8a30-4df8-ba38-6707c415708e
title: élément stubFunction
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7282e7280c8d701710094b70b84a65756f7230ad
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104209851"
---
# <a name="stubfunction-element"></a>élément stubFunction

Spécifie si les références de fonction stub doivent être incluses dans les structures d’opération dans les définitions de type de port pour les opérations unidirectionnelles et bidirectionnelles.

## <a name="usage"></a>Utilisation

``` syntax
<stubFunction/>
```

## <a name="attributes"></a>Attributs

Il n’y a pas d’attributs.

## <a name="child-elements"></a>Éléments enfants

Il n’y a pas d’éléments enfants.

## <a name="parent-elements"></a>Éléments parents



| Élément                                                       | Description                                                  |
|---------------------------------------------------------------|--------------------------------------------------------------|
| [**portTypeDefinitions**](porttypedefinitions.md)<br/> | Génère des constantes C pour les types de ports.<br/> <br/> |



## <a name="remarks"></a>Notes

Les références de fonction stub sont utilisées dans les scénarios d’hébergement pour les opérations unidirectionnelles et bidirectionnelles.

Les valeurs valides pour cet élément sont 1 (TRUE/stub Function References incluses) et 0 (FALSe/aucune référence à la fonction stub incluse).

## <a name="element-information"></a>Informations sur les éléments



|                                     |               |
|-------------------------------------|---------------|
| Système minimal pris en charge<br/> | Windows Vista |
| Peut être vide                        | Oui           |



 

 




