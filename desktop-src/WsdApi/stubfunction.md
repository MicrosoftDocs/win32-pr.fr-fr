---
description: Spécifie si les références de fonction stub doivent être incluses dans les structures d’opération dans les définitions de type de port pour les opérations unidirectionnelles et bidirectionnelles.
ms.assetid: 2547f71d-8a30-4df8-ba38-6707c415708e
title: élément stubFunction
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dc9304aa33bd193edc631949a93e1d770a1fade3d0c5726a9f2d897ea1862476
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118552410"
---
# <a name="stubfunction-element"></a>élément stubFunction

Spécifie si les références de fonction stub doivent être incluses dans les structures d’opération dans les définitions de type de port pour les opérations unidirectionnelles et bidirectionnelles.

## <a name="usage"></a>Usage

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



## <a name="remarks"></a>Remarques

Les références de fonction stub sont utilisées dans les scénarios d’hébergement pour les opérations unidirectionnelles et bidirectionnelles.

Les valeurs valides pour cet élément sont 1 (TRUE/stub Function References incluses) et 0 (FALSe/aucune référence à la fonction stub incluse).

## <a name="element-information"></a>Informations sur les éléments



| Étiquette | Valeur |
|-------------------------------------|---------------|
| Système minimal pris en charge<br/> | Windows Vista |
| Peut être vide                        | Oui           |



 

 




