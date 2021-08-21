---
description: La création de tables de séquences est un élément essentiel du développement d’un package d’installation, car ces tables spécifient l’ordre d’exécution des actions standard qui contrôlent le processus d’installation et affichent les boîtes de dialogue de l’interface utilisateur.
ms.assetid: db9a9cae-2a66-4e0d-a981-8de66d7c2a13
title: Utilisation d’une table de séquences
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 16adf47a554bf70298b0efc893847f84eafd6e97313b09ba9ea3182398cdd97d
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119809009"
---
# <a name="using-a-sequence-table"></a>Utilisation d’une table de séquences

La création de tables de séquences est un élément essentiel du développement d’un package d’installation, car ces tables spécifient l’ordre d’exécution des [actions standard](standard-actions.md) qui contrôlent le processus d’installation et affichent les boîtes de dialogue de l’interface utilisateur.

Il existe trois modes d’installation et deux types de tables de séquences pour chaque mode.

Les trois modes d’installation distincts actuellement pris en charge par le programme d’installation sont les suivants :

-   Installation simple
-   Installation administrative
-   Installation d’une publication

Les tables de séquences ont chacune trois champs : action, condition et séquence. Le champ action nomme une action standard ou personnalisée, ou une boîte de dialogue définie par l’utilisateur ou une séquence que le programme d’installation exécute. Le champ condition permet à l’auteur de spécifier une expression logique qui contrôle si une action ou une boîte de dialogue définie par l’utilisateur est exécutée ou affichée. Si le champ condition est vide ou contient une expression qui prend la valeur true, l’action ou la boîte de dialogue est exécutée ou affichée. L’action ou la boîte de dialogue est ignorée si l’expression prend la valeur false. Le champ séquence spécifie l’ordre d’exécution de chaque action ou boîte de dialogue définie par l’utilisateur dans la table.

Chacun de ces modes d’installation traite les tables de séquence de l’interface utilisateur et les tables de séquence d’exécution. Les tables de séquences de l’interface utilisateur sont traitées uniquement si le programme d’installation a été initialisé avec le niveau d’affichage de l’interface utilisateur défini sur réduit ou complet. Pour plus d’informations sur les niveaux d’affichage de l’interface utilisateur, consultez la référence [**MsiSetInternalUI**](/windows/desktop/api/Msi/nf-msi-msisetinternalui) .

Les tables de séquences de l’interface utilisateur contiennent généralement des actions standard liées à la collecte des informations système affichées à l’utilisateur par le biais de l’interface utilisateur. L’interface utilisateur s’affiche en enregistrant les clés étrangères dans les noms des boîtes de dialogue de la [table boîte de dialogue](dialog-table.md) dans le champ action de la table séquence de l’interface utilisateur. L’utilisateur a ensuite la possibilité de modifier ou d’accepter les informations système et de commencer l’installation, ce qui se produit lors du traitement de la table de séquences d’exécution.

Au cours d’une installation simple, l’action [installer](install-action.md) le plus haut niveau est exécutée, qui à son tour traite la [table InstallUISequence](installuisequence-table.md) et la [table InstallExecuteSequence](installexecutesequence-table.md).

Une installation administrative est généralement initiée par un administrateur réseau pour affecter et installer des applications pour des utilisateurs individuels et des groupes d’utilisateurs. Pendant ce type d’installation, l’action de niveau supérieur de l' [administrateur](admin-action.md) est exécutée, qui traite la [table AdminUISequence](adminuisequence-table.md) et la [table AdminExecuteSequence](adminexecutesequence-table.md).

Pour [publier](advertisement.md) une application ou une fonctionnalité, le programme d’installation doit être lancé avec l’action [publier](advertise-action.md) . Pendant ce type d’installation, la [table AdvtExecuteSequence](advtexecutesequence-table.md) est traitée.

Lors de la création d’une table de séquences, il est recommandé d’utiliser le numéro de séquence pour les actions standard à partir des séquences suggérées dans les rubriques ci-dessous. Pour les actions standard qui n’ont pas de position standard dans la table de séquences comme [ForceReboot](forcereboot-action.md), [ValidateProductID](validateproductid-action.md)et [InstallExecute](installexecute-action.md), utilisez un numéro de séquence qui est un multiple de dix pour identifier l’action en tant qu’action standard. Pour les actions personnalisées, utilisez un numéro de séquence qui n’est pas un multiple de dix pour le différencier des actions standard dans la table de séquences.

Pour les séquences d’actions suggérées pour chaque table de séquences, consultez les rubriques suivantes :

-   [InstallUISequence suggéré](suggested-installuisequence.md)
-   [InstallExecuteSequence suggéré](suggested-installexecutesequence.md)
-   [AdminUISequence suggéré](suggested-adminuisequence.md)
-   [AdminExecuteSequence suggéré](suggested-adminexecutesequence.md)
-   [AdvtUISequence suggéré](suggested-advtuisequence.md)
-   [AdvtExecuteSequence suggéré](suggested-advtexecutesequence.md)

Pour obtenir une description détaillée des tables de séquence et de la façon dont les actions standard sont exécutées, consultez l' [exemple de table de séquence détaillé](sequence-table-detailed-example.md).

* * Windows Installer 3,0 et versions ultérieures : * *

à partir de Windows Installer 3,0, un package de correctifs peut contenir la [table MsiPatchSequence](msipatchsequence-table.md). Ce tableau contient toutes les informations requises par le programme d’installation pour déterminer la séquence de l’application d’un correctif logiciel de petite mise à jour par rapport à tous les autres correctifs. Pour plus d’informations, consultez [mise à jour corrective et mises à niveau](patching-and-upgrades.md).

> [!Note]
>
> Les [modules de fusion](merge-modules.md) peuvent contenir des [tables de base de données de module de fusion](merge-module-database-tables.md) qui modifient les tables de séquences d’action du fichier de .msi cible. La fusion du module dans une base de données peut modifier les informations de la table Sequence, mais n’ajoute pas ces tables au fichier .msi. Pour plus d’informations, consultez [création de tables de séquence de module de fusion](authoring-merge-module-sequence-tables.md).

 

 

 



