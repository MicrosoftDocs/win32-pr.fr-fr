---
description: Les répertoires de la table Directory spécifient la disposition d’une installation.
ms.assetid: 59f6ae09-d013-46d7-a1a7-0543f31ac487
title: Utilisation d’une propriété de répertoire dans un chemin d’accès
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2789f6442072f3db6a96c0abb7db301038673f83
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127009587"
---
# <a name="using-a-directory-property-in-a-path"></a>Utilisation d’une propriété de répertoire dans un chemin d’accès

Les répertoires de la [table Directory](directory-table.md) spécifient la disposition d’une installation. lorsque le Windows Installer résout ces répertoires au cours de l' [action CostFinalize](costfinalize-action.md), les clés de la table Directory deviennent des [propriétés](properties.md) définies sur des chemins d’accès aux répertoires. Le programme d’installation définit également toujours un certain nombre de propriétés standard du [dossier système](property-reference.md) pour les chemins d’accès des dossiers système.

Il est garanti que les valeurs des [Propriétés du dossier système](property-reference.md) se terminent dans un séparateur de répertoire. Les valeurs de toutes les autres propriétés entrées dans la [table Directory](directory-table.md) sont garanties uniquement dans un séparateur de répertoire après que le programme d’installation a exécuté l' [action CostFinalize](costfinalize-action.md). Avant la fin de l’évaluation des coûts, les valeurs des propriétés entrées dans la table de répertoires qui ne sont pas des [Propriétés de dossier système](property-reference.md) peuvent ne pas se terminer par un séparateur de répertoire. Par conséquent, si votre installation définit des propriétés de répertoire à l’aide d' [actions personnalisées](custom-actions.md) dans le package, les valeurs de référence peuvent ne pas se terminer par un séparateur de répertoire.

Les propriétés de répertoire se terminant par un séparateur de répertoire peuvent donc être utilisées dans une chaîne de chemin d’accès sans inclure explicitement le séparateur de répertoire. Par exemple, si la valeur de DirectoryProperty se termine par un séparateur de répertoire, la chaîne suivante spécifie correctement le chemin d’accès au *fichier* dans le *sous-répertoire*

``` syntax
[DirectoryProperty]subdirectory\file
```

et la chaîne de chemin d’accès suivante est incorrecte.

``` syntax
[DirectoryProperty]\subdirectory\file
```

 

 



