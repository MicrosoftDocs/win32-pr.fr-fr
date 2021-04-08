---
description: ICE27 valide les tables de séquence d’un package d’installation pour les actions valides, les restrictions de séquence d’action et l’organisation dans les sections de recherche, d’évaluation des coûts, de sélection et d’exécution.
ms.assetid: c5292a3c-57bb-4203-96a1-6d747f554178
title: ICE27
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4eb4b90b313f5f78874fb93ce9d32c3650b97064
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103864094"
---
# <a name="ice27"></a>ICE27

ICE27 valide les [*tables de séquence*](s-gly.md) d’un package d’installation pour les actions valides, les restrictions de séquence d’action et l’organisation dans les sections de recherche, d’évaluation des coûts, de sélection et d’exécution.

L’action personnalisée ICE27 valide les éléments suivants :

-   Que les actions répertoriées dans la colonne action des tables de séquence sont des [actions standard](standard-actions.md), une action personnalisée répertoriée dans la [table CustomAction](customaction-table.md)ou une boîte de dialogue répertoriée dans la [table boîte de dialogue](dialog-table.md).
-   Les actions soumises aux restrictions de séquencement sont dans l’ordre relatif approprié dans la séquence d’action. Les restrictions de séquencement sont générées lorsqu’une action est dépendante d’une autre.
-   Les actions limitées à une section particulière de la séquence se trouvent là où elles appartiennent. ICE27 valide l’organisation suivante des tables de séquences. Notez que chaque table de séquence n’a pas toutes les sections. Consultez les tables de séquence suggérées dans [à l’aide d’une table de séquences](using-a-sequence-table.md).



| Section table de séquence | Plage dans la séquence d’action                                                                       | Actions appartenant à la section                                                                                                                                                                                                                     |
|------------------------|------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Recherche                 | {Start} à [CostInitialize](costinitialize-action.md)                                         | Actions qui recherchent des applications existantes. [AppSearch](appsearch-action.md)<br/> [CCPSearch](ccpsearch-action.md)<br/>                                                                                                         |
| Coûts                | Action [CostInitialize](costinitialize-action.md) à [CostFinalize](costfinalize-action.md)  | Actions qui effectuent des [coûts de fichier](file-costing.md). [CostInitialize](costinitialize-action.md)<br/> [FileCost](filecost-action.md)<br/> [CostFinalize](costfinalize-action.md)<br/>                                           |
| Sélection              | [CostFinalize](costfinalize-action.md) à [InstallValidate](installvalidate-action.md)       | Actions qui définissent des dossiers ou des États de fonctionnalités. [Action SetODBCFolders](setodbcfolders-action.md)<br/>                                                                                                                                        |
| Exécution              | [InstallValidate](installvalidate-action.md) à [InstallFinalize](installfinalize-action.md) | Actions de script, telles que l’inscription, la publication, l’installation (où vous copiez des fichiers). Notez que l' [action InstallFinalize](installfinalize-action.md) doit se trouver dans la table si et seulement s’il existe des actions dans la section exécution.<br/> |
| PostExecution          | [InstallFinalize](installfinalize-action.md) à {end}                                         | [RemoveExistingProducts](removeexistingproducts-action.md)                                                                                                                                                                                      |



 

ICE27 valide les tables suivantes :

-   [AdvtExecuteSequence](advtexecutesequence-table.md)
-   [AdminUISequence](adminuisequence-table.md)
-   [AdminExecuteSequence](adminexecutesequence-table.md)
-   [InstallUISequence](installuisequence-table.md)
-   [InstallExecuteSequence](installexecutesequence-table.md)

## <a name="result"></a>Résultats

ICE27 publie un message d’erreur s’il existe des tables de séquence dans le package avec une organisation ou un séquençage d’action non valide.

## <a name="example"></a>Exemple



| Erreur ICE27                                                                                                                         | Description                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                         |
|-------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Action inconnue : 'action1 'de la table InstallExecuteSequnence. Action non standard introuvable dans les tables CustomAction ou Dialog    | Une action est indiquée dans le tableau des séquences, car il ne s’agit pas d' [actions standard](standard-actions.md), d’une action personnalisée figurant dans la [table CustomAction](customaction-table.md)ou d’une boîte de dialogue figurant dans la [table de boîte de dialogue](dialog-table.md).                                                                                                                                                                                                                                                                       |
| « Action2 » dans la table InstallExecute n’est pas au bon endroit. Actuel : recherche, corriger : coût                                                 | Il existe une action dans une table de séquences qui est placée de manière incorrecte par rapport au numéro de séquence dans la colonne de séquence. « Current » indique la position actuelle de l’action dans les sections de recherche, d’évaluation des coûts, de sélection ou d’exécution de la table de séquences indiquée.<br/> « Correct » indique dans quelle section appartient l’action.<br/> Pour corriger cette erreur, remplacez le numéro de séquence de l’action par l’intérieur de la section appropriée. Notez qu’une action peut être localisée dans plusieurs sections.<br/> |
| L’action’InstallFinalize’dans la table InstallExecuteSequence ne peut être appelée que lorsque des opérations de script sont exécutées             | Il existe une [action InstallFinalize](installfinalize-action.md) dans une table de séquences qui ne contient aucune opération de script dans la section exécution de la table. Ajoutez des actions à la section exécution ou supprimez l’action InstallFinalize de la table.<br/>                                                                                                                                                                                                                                                        |
| InstallFinalize doit être appelé dans la table InstallExecuteSequence, car il existe des opérations de script à exécuter                            | Il existe une table de séquences contenant des actions dans la section d’exécution qui n’inclut pas l' [action InstallFinalize](installfinalize-action.md). Ajoutez l’action InstallFinalize à cette table de séquences et donnez-lui le plus grand numéro de séquence pour la placer en dernier dans la séquence d’action.<br/>                                                                                                                                                                                                                            |
| Action : « Action3 » dans la table InstallExecuteSequence doit précéder l’action « action5 ». Seq en cours \# : 1200. Seq dépendante \# : 1100 | Il existe une action dans la table de séquences indiquée qui est séquencée après une action dépendante. Modifiez le numéro de séquence de l’action dépendante afin qu’elle précède l’action.<br/>                                                                                                                                                                                                                                                                                                                                    |
| Action : « Action4 » dans la table InstallExecuteSequence doit venir après l’action « action6 ».                                             | Il existe une action dans la table de séquences indiquée qui est séquencée avant une action dont elle dépend. Modifiez le numéro de séquence de l’action afin qu’il se trouve après l’action qui en dépend.<br/>                                                                                                                                                                                                                                                                                                                   |



 

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Référence ICE](ice-reference.md)
</dt> </dl>

 

 




