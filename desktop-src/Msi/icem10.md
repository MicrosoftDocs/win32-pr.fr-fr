---
description: ICEM10 vérifie qu’un module de fusion contient uniquement des propriétés qui sont autorisées dans la table de propriétés.
ms.assetid: 9ac7a724-ea0e-4caa-bb4f-846bfb802037
title: ICEM10
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 80263e5033ec14bd669c5d046c7f3842d58e332f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106533986"
---
# <a name="icem10"></a>ICEM10

ICEM10 vérifie qu’un module de fusion contient uniquement des propriétés qui sont autorisées dans la [table de propriétés](property-table.md). Les propriétés spécifiques au produit suivantes ne sont pas autorisées dans la table de propriétés :

-   [**Propriété ProductLanguage**](productlanguage.md)
-   [**Propriété ProductCode**](productcode.md)
-   [**Propriété ProductVersion**](productversion.md)
-   [**Propriété ProductName**](productname.md)
-   [**Propriété Manufacturer**](manufacturer.md)

## <a name="result"></a>Résultats

ICEM10 publie une erreur lorsqu’un module de fusion contient une propriété qui n’est pas autorisée dans la [table de propriétés](property-table.md).

## <a name="example"></a>Exemple

ICEM10 publie les messages d’erreur suivants pour un module qui contient les entrées de base de données affichées.

``` syntax
The property 'ProductLanguage' is not allowed in a merge module.

The property 'Manufacturer' is not allowed in a merge module.
```

Le tableau suivant présente une table de [Propriétés](property-table.md)partielle.



| Propriété                                   | Valeurs    |
|--------------------------------------------|-----------|
| Couleur                                      | Rouge       |
| [**Fabricant**](manufacturer.md)       | Microsoft |
| [**ProductLanguage**](productlanguage.md) | 1033      |



 

La procédure suivante vous montre comment corriger les erreurs.

**Pour corriger les erreurs**

1.  Supprimez la propriété'[**Manufacturer**](manufacturer.md)'de la [table de propriétés](property-table.md).
2.  Supprimez la propriété'[**ProductLanguage**](productlanguage.md)'de la [table de propriétés](property-table.md).

## <a name="table-used-during-execution"></a>Table utilisée pendant l’exécution

La [table de propriétés](property-table.md) est utilisée lors de l’exécution.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Référence ICE du module de fusion](merge-module-ice-reference.md)
</dt> </dl>

 

 



