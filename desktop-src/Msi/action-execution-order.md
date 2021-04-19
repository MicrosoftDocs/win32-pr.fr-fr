---
description: L’ordre d’exécution des actions est déterminé par la séquence d’actions qui ont été créées dans les tables de séquence et par l’ordre dans lequel le programme d’installation exécute les tables de séquence.
ms.assetid: f4666f49-4ea1-42fb-b32d-ce77de79b212
title: Ordre d’exécution des actions
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 954c44f6e2525deb3375cb9ea72d0320df3a5f02
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106527438"
---
# <a name="action-execution-order"></a>Ordre d’exécution des actions

L’ordre d’exécution des actions est déterminé par la séquence d’actions qui ont été créées dans les [*tables de séquence*](s-gly.md) et par l’ordre dans lequel le programme d’installation exécute les tables de séquence. Pour plus d’informations, consultez séquences d’actions suggérées dans [à l’aide d’une table de séquences](using-a-sequence-table.md).

Le programme d’installation exécute des tables de séquence en réponse à une demande d’installation, de [publication](advertisement.md)ou d' [installation administrative](administrative-installation.md). Par exemple, en réponse à l’utilisation des [options de ligne de commande](command-line-options.md)/I,/J ou/a, les actions d' [installation](install-action.md), de [publication](advertise-action.md)et d' [administration](admin-action.md) ne sont pas appelées à partir de la séquence d’action. Ces actions de haut niveau sont passées au programme d’installation lors de l’initialisation du programme d’installation.

Si le programme d’installation reçoit l’action d’installation et que le package d’installation a été créé avec une interface utilisateur, le programme d’installation exécute d’abord les actions dans la [table InstallUISequence](installuisequence-table.md) , puis exécute les actions dans la [table InstallExecuteSequence](installexecutesequence-table.md) dans l’ordre. Si le package n’a pas d’interface utilisateur, le programme d’installation exécute les actions dans la table InstallExecuteSequence dans l’ordre.

Si l’action d’administration est passée au programme d’installation et que le package d’installation a été créé avec une interface utilisateur, le programme d’installation exécute d’abord la [table AdminUISequence](adminuisequence-table.md) , puis exécute la [table AdminExecuteSequence](adminexecutesequence-table.md). Si le package n’a pas d’interface utilisateur, le programme d’installation exécute la table AdminExecute.

Si l’action de publication est passée au programme d’installation, le programme d’installation exécute la table [AdvtExecuteSequence](advtexecutesequence-table.md) .

> [!Note]  
> Le programme d’installation n’utilise pas la table [AdvtUISequence](advtuisequence-table.md) . La table AdvtUISequence ne doit pas exister dans la base de données d’installation ou elle doit être laissée vide.

 

Quand le programme d’installation exécute une table de séquences, il exécute des actions dans l’ordre des numéros de séquence listés dans la colonne séquence. L’ordre des actions est toujours linéaire sans branchement ni boucle. Les développeurs de packages peuvent empêcher de manière conditionnelle une action particulière d’être exécutée en créant une expression logique dans la colonne condition. Le programme d’installation ignore l’action chaque fois que la condition prend la valeur false. Consultez [utilisation d’une table de séquences et d’une syntaxe d'](using-a-sequence-table.md) [instruction conditionnelle](conditional-statement-syntax.md).

Toutes les tables de séquences ont les colonnes suivantes.



| Colonne    | Description                                                                                                                                                                                                                                   |
|-----------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Action    | Clé primaire de la table ; le nom de l’action doit être unique.                                                                                                                                                                                |
| Condition | Expression booléenne utilisée pour déterminer s’il faut exécuter l’action. L’action est exécutée si ce champ est vide ou contient une expression qui prend la valeur true. L’action n’est pas exécutée si l’expression prend la valeur false. |
| Séquence  | Numéro de séquence relatif utilisé pour déterminer l’ordre dans lequel les actions sont exécutées.                                                                                                                                                         |



 

 

 



