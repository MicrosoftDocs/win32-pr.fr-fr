---
title: Typage fort
description: C est un langage faiblement typé, autrement dit, le compilateur autorise des opérations telles que l’assignation et la comparaison entre les variables de types différents.
ms.assetid: 5f52adcc-22b9-4b4f-b921-5996d278b10e
keywords:
- Appel de procédure distante RPC, description, saisie de données
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ea859e2d5c160048d79e3c371b47af2bc55e0a65
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127413490"
---
# <a name="strong-typing"></a>Typage fort

C est un langage faiblement typé, autrement dit, le compilateur autorise des opérations telles que l’assignation et la comparaison entre les variables de types différents. Par exemple, C permet d’effectuer un cast de la valeur d’une variable en un autre type. La possibilité d’utiliser des variables de types différents dans la même expression favorise la flexibilité et l’efficacité.

Un langage fortement typé impose des restrictions sur les opérations parmi les variables de types différents. Dans ce cas, le compilateur émet une erreur qui interdit l’opération. Ces recommandations strictes en matière de types de données sont conçues pour éviter les erreurs potentielles.

La difficulté avec l’utilisation d’un langage faiblement typé comme C pour les appels de procédure distante est que les applications distribuées peuvent s’exécuter sur plusieurs ordinateurs différents avec des compilateurs C et des architectures différentes. Quand une application s’exécute sur un seul ordinateur, vous n’avez pas à vous préoccuper du format de données interne, car les données sont gérées de manière cohérente. Toutefois, dans un environnement informatique distribué, différents ordinateurs peuvent utiliser des définitions différentes pour leurs types de données de base. Par exemple, certains ordinateurs définissent le type **int** , donc sa représentation interne est de 16 bits, tandis que les autres ordinateurs utilisent 32 bits. Une architecture d’ordinateur, appelée « Little endian », attribue l’octet de données le moins significatif à l’adresse mémoire la plus basse et l’octet le plus significatif à l’adresse la plus élevée. Une autre architecture, appelée « Big endian », attribue l’octet le moins significatif à l’adresse mémoire la plus élevée associée à ces données.

Les appels de procédure distante nécessitent un contrôle strict sur les types de paramètres. Pour gérer la transmission et la conversion des données sur le réseau, MIDL applique strictement les restrictions de type pour les données transférées sur le réseau. Pour cette raison, MIDL comprend un ensemble de [types de base](base-types.md)bien définis. MIDL applique un typage fort en exigeant l’utilisation de mots clés qui définissent de manière non ambiguë la taille et le type de données. L’effet le plus visible du typage fort est que MIDL n’autorise pas les variables de **type \* void**.

Dans les rubriques suivantes, cette section traite des fonctionnalités de langage MIDL qui garantissent un typage fort des données :

-   [Types de base](base-types.md)
-   [Types signés et non signés](signed-and-unsigned-types.md)
-   [Types à caractères larges](wide-character-types.md)
-   [Structures](structures.md)
-   [Unions](unions.md)
-   [Types énumérés](enumerated-types.md)
-   [Tableaux](arrays.md)
-   [Attributs de fonction](function-attributes.md)
-   [Attributs de champ](field-attributes.md)
-   [Trois types pointeur](three-pointer-types.md)
-   [Attributs de type](type-attributes.md)

 

 




