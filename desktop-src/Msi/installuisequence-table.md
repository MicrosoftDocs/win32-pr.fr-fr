---
description: La table InstallUISequence répertorie les actions qui sont exécutées lorsque l’action d’installation de niveau supérieur est exécutée et que le niveau d’interface utilisateur interne est défini sur interface utilisateur complète ou réduite.
ms.assetid: 076d7c14-e302-4465-aed5-27a4b1f70ac8
title: Table InstallUISequence
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 19a4d8d3033645ac1f414e3aff67be2a26d7a6ab
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106536596"
---
# <a name="installuisequence-table"></a>Table InstallUISequence

La table InstallUISequence répertorie les actions qui sont exécutées lorsque l' [action d’installation](install-action.md) de niveau supérieur est exécutée et que le niveau d’interface utilisateur interne est défini sur interface utilisateur complète ou réduite. Le programme d’installation ignore les actions dans ce tableau si le niveau de l’interface utilisateur est défini sur interface utilisateur de base ou aucune interface utilisateur. Consultez [à propos de l’interface utilisateur](about-the-user-interface.md).

Les actions de la séquence d’installation jusqu’à l' [action InstallValidate](installvalidate-action.md)et les boîtes de dialogue quitter sont situées dans la table InstallUISequence. Toutes les actions du InstallValidate jusqu’à la fin de la séquence d’installation se trouvent dans la [table InstallExecuteSequence](installexecutesequence-table.md). Étant donné que la table InstallExecuteSequence doit être autonome, elle comporte toutes les actions d’initialisation nécessaires, telles que les actions [LaunchConditions](launchconditions-action.md), [CostInitialize](costinitialize-action.md), [FileCost](filecost-action.md), [CostFinalize](costfinalize-action.md)et [ExecuteAction](executeaction-action.md).

La table InstallUISequence contient les colonnes suivantes.



| Colonne    | Type                         | Clé | Nullable |
|-----------|------------------------------|-----|----------|
| Action    | [Identificateur](identifier.md) | O   | N        |
| Condition | [Condition](condition.md)   | N   | O        |
| Séquence  | [Integer](integer.md)       | N   | O        |



 

## <a name="columns"></a>Colonnes

<dl> <dt>

<span id="Action"></span><span id="action"></span><span id="ACTION"></span>Transactionnel
</dt> <dd>

Nom de l’action à exécuter. Il s’agit d’une action intégrée, d’une action personnalisée ou d’un assistant de l’interface utilisateur.

Clé de table primaire.

</dd> <dt>

<span id="Condition"></span><span id="condition"></span><span id="CONDITION"></span>Etat
</dt> <dd>

Ce champ contient une expression conditionnelle. Si l’expression prend la valeur false, l’action est ignorée. Si la syntaxe de l’expression n’est pas valide, la séquence se termine et retourne iesBadActionData. Pour plus d’informations sur la syntaxe des instructions conditionnelles, consultez [syntaxe d’instruction conditionnelle](conditional-statement-syntax.md).

</dd> <dt>

<span id="Sequence"></span><span id="sequence"></span><span id="SEQUENCE"></span>Séquence
</dt> <dd>

Le nombre dans cette colonne détermine la position de la séquence dans laquelle cette action est exécutée.

Une valeur positive représente la position de la séquence. Une valeur null indique que l’action n’est jamais exécutée. Les valeurs négatives suivantes indiquent que cette action est exécutée si le programme d’installation retourne l’indicateur de fin associé. Chaque indicateur de fin (valeur négative) peut être utilisé avec une seule action. Plusieurs actions peuvent avoir des indicateurs d’arrêt, mais elles doivent être des indicateurs différents. Les indicateurs de fin (valeurs négatives) sont généralement utilisés avec les [boîtes de dialogue](dialog-boxes.md).



| Indicateur de fin          | Valeur | Description                                                                          |
|---------------------------|-------|--------------------------------------------------------------------------------------|
| msiDoActionStatusSuccess  | -1    | Achèvement réussi. Utilisé avec les boîtes de dialogue [quitter](exit-dialog.md) .               |
| msiDoActionStatusUserExit | -2    | L’utilisateur termine l’installation. Utilisé avec les boîtes de dialogue [UserExit](userexit-dialog.md) .     |
| msiDoActionStatusFailure  | -3    | La sortie irrécupérable s’arrête. Utilisé avec les boîtes de dialogue [FatalError](fatalerror-dialog.md) . |
| msiDoActionStatusSuspend  | -4    | L’installation est suspendue.                                                                |



 

Zéro, tous les autres nombres négatifs ou une valeur null indique que l’action n’est jamais exécutée.

</dd> </dl>

## <a name="remarks"></a>Notes

Le texte localisé associé à l’affichage de progression ou à la journalisation est spécifié dans la [table ActionText](actiontext-table.md).

Pour obtenir un exemple de table de séquences, consultez [utilisation d’une table de séquences](using-a-sequence-table.md).

## <a name="validation"></a>Validation

<dl>

[ICE03](ice03.md)  
[ICE06](ice06.md)  
[ICE12](ice12.md)  
[ICE13](ice13.md)  
[ICE20](ice20.md)  
[ICE26](ice26.md)  
[ICE27](ice27.md)  
[ICE28](ice28.md)  
[ICE46](ice46.md)  
[ICE75](ice75.md)  
[ICE79](ice79.md)  
[ICE82](ice82.md)  
[ICE86](ice86.md)  
</dl>

 

 



