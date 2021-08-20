---
description: ICE06 vérifie chaque table pour valider que toutes les colonnes répertoriées dans le \_ tableau de validation sont présentes dans la table. Si une table n’existe pas, toutes les \_ entrées de validation pour cette table sont ignorées.
ms.assetid: 0c3f21ae-49ea-4cfe-b465-6fdc2b19cbb9
title: ICE06
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: febccd205b78e90d3dac49f88d0750f803c8cd575b6b76b46cab79a684deea90
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118142567"
---
# <a name="ice06"></a>ICE06

ICE06 vérifie chaque table pour valider que toutes les colonnes répertoriées dans le [ \_ tableau de validation](-validation-table.md) sont présentes dans la table. Si une table n’existe pas, toutes les \_ entrées de validation pour cette table sont ignorées.

L’objectif de ICE06 est de détecter les instances dans lesquelles un auteur tente d’utiliser une nouvelle \_ table de validation qui reflète une modification de schéma avec une ancienne base de données qui n’a pas été mise à jour. ICE06 détecte également le cas inverse d’une ancienne \_ table de validation utilisée avec une base de données modifiée.

Notez que la validation interne effectuée par [ICE03](ice03.md) intercepte l’instance d’une colonne de table non définie dans la \_ table de validation qui est indiquée dans le catalogue de colonnes. L’utilisation de ICE03 et ICE06 garantit donc que chaque colonne de la base de données est testée.

## <a name="result"></a>Résultat

ICE06 publie une erreur quand une colonne de table définie dans la table de \_ validation n’est pas listée dans la \_ Table Columns.

## <a name="example"></a>Exemples

Dans l’exemple suivant, ICE06 publie le message

Colonne : version de la table : la ModuleSignature n’est pas définie dans la base de données.

[ \_ Table de validation](-validation-table.md) (partielle)



| Table de charge de travail           | Colonne   |
|-----------------|----------|
| ModuleSignature | ModuleID |
| ModuleSignature | Version  |



 

[ \_ Table Columns](-columns-table.md) (partielle)



| Table           | Nombre | Name     |
|-----------------|--------|----------|
| ModuleSignature | 1      | ModuleID |



 

La colonne version de la table ModuleSignature n’est pas dans la base de données ou n’est pas indiquée dans la \_ Table Columns.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Référence ICE](ice-reference.md)
</dt> </dl>

 

 



