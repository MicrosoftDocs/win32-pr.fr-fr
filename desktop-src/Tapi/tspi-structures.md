---
description: Les structures de données utilisées par TSPI sont identiques à celles définies dans les structures TAPI, à l’exception de TUISPICREATEDIALOGINSTANCEPARAMS.
ms.assetid: 99d966ea-49b5-4a84-83a1-99dc8465c751
title: Structures TSPI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4e3468171bc160ca03ac9f5501a9eba7fd9221ef
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106519886"
---
# <a name="tspi-structures"></a>Structures TSPI

Les structures de données utilisées par TSPI sont identiques à celles définies dans les [structures TAPI](./tapi-structures.md), à l’exception de [**TUISPICREATEDIALOGINSTANCEPARAMS**](/windows/win32/api/tspi/ns-tspi-tuispicreatedialoginstanceparams).

Dans le cas de la plupart des structures de données les plus volumineuses, la responsabilité de remplir les membres est divisée entre le fournisseur de services et TAPI. Le fournisseur de services doit conserver les valeurs présentes dans les membres appartenant à l’interface TAPI. La description des membres qui doivent être définis par le fournisseur de services et qui doivent être préservés est fournie dans la section Functions dans les fonctions qui font référence à cette structure de données.

Pour chaque structure, la section de référence répertorie les éléments suivants :

-   L’objectif de la structure
-   Description des valeurs ou des champs
-   Description de l’extensibilité de la structure
-   Commentaires facultatifs sur l’utilisation de la structure
-   Références facultatives à d’autres fonctions, messages, constantes ou structures.

La mémoire pour toutes les structures de données dont la représentation est publiée et partagée par TAPI et le fournisseur de services est allouée par TAPI ou une application utilisant TAPI. L’interface TAPI transmet un pointeur vers la fonction TSPI qui retourne les informations. TSPI remplit la structure de données avec les informations demandées. Si l’opération est asynchrone, les informations ne sont pas disponibles tant que le rappel de réponse asynchrone n’indique pas la réussite.

> [!Note]  
> Certaines structures incluent des champs de taille et de décalage pour définir l’emplacement et la longueur des chaînes dans la partie variable de la structure. Si le fournisseur de services est invité à ajouter une chaîne alors qu’aucune chaîne n’est disponible, le fournisseur de services doit indiquer cette condition de l’une des manières suivantes :
>
> -   Affectez la valeur 0 aux champs taille et décalage.
> -   Définissez le champ décalage sur une valeur différente de zéro, mais dimensionnez-la sur 0.
> -   Définissez le champ décalage sur une valeur différente de zéro, la taille sur 1 et l’octet au décalage à 0.

 

 

 
