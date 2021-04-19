---
description: La table AdminUISequence répertorie les actions que le programme d’installation appelle en séquence lorsque l’action d’administration de niveau supérieur est exécutée et que le niveau de l’interface utilisateur interne est défini sur interface utilisateur complète ou interface utilisateur réduite.
ms.assetid: 7227846d-b755-4af9-acc3-e27742a5097a
title: Table AdminUISequence
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f8fb460f65d223e75ebd50a7587f5b3f4adeced8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106534222"
---
# <a name="adminuisequence-table"></a>Table AdminUISequence

La table AdminUISequence répertorie les actions que le programme d’installation appelle en séquence lorsque l' [action d’administration](admin-action.md) de niveau supérieur est exécutée et que le niveau de l’interface utilisateur interne est défini sur interface utilisateur complète ou interface utilisateur réduite. Le programme d’installation ignore les actions dans ce tableau si le niveau de l’interface utilisateur est défini sur interface utilisateur de base ou aucune interface utilisateur. Consultez [à propos de l’interface utilisateur](about-the-user-interface.md).

Les actions d’administration dans la séquence d’installation jusqu’à l' [action InstallValidate](installvalidate-action.md)et toutes les boîtes de dialogue de sortie sont situées dans la table AdminUISequence. Toutes les actions du InstallValidate jusqu’à la fin de la séquence d’installation se trouvent dans la [table AdminExecuteSequence](adminexecutesequence-table.md). Étant donné que la table AdminExecuteSequence doit être autonome, elle contient également toutes les actions d’initialisation nécessaires, telles que [LaunchConditions](launchconditions-action.md), [CostInitialize](costinitialize-action.md), [FileCost](filecost-action.md)et [CostFinalize](costfinalize-action.md). Elle a également l' [action ExecuteAction](executeaction-action.md).

Les colonnes sont identiques à celles de la [table InstallUISequence](installuisequence-table.md). La table AdminUISequence contient les colonnes suivantes.



| Colonne    | Type                         | Clé | Nullable |
|-----------|------------------------------|-----|----------|
| Action    | [Identificateur](identifier.md) | O   | N        |
| Condition | [Condition](condition.md)   | N   | O        |
| Séquence  | [Integer](integer.md)       | N   | O        |



 

## <a name="columns"></a>Colonnes

<dl> <dt>

<span id="Action"></span><span id="action"></span><span id="ACTION"></span>Transactionnel
</dt> <dd>

Nom de l’action à exécuter. Il s’agit d’une action standard, d’un assistant d’interface utilisateur ou d’une action personnalisée indiquée dans la [table CustomAction](customaction-table.md).

Clé de table primaire.

</dd> <dt>

<span id="Condition"></span><span id="condition"></span><span id="CONDITION"></span>Etat
</dt> <dd>

Expression logique. Si l’expression prend la valeur false, l’action est ignorée. Si la syntaxe de l’expression n’est pas valide, la séquence se termine et retourne iesBadActionData. Pour plus d’informations sur la syntaxe des instructions conditionnelles, consultez [syntaxe d’instruction conditionnelle](conditional-statement-syntax.md).

</dd> <dt>

<span id="Sequence"></span><span id="sequence"></span><span id="SEQUENCE"></span>Séquence
</dt> <dd>

Une valeur positive indique la position de séquence de l’action. Les valeurs négatives suivantes indiquent que l’action est appelée si le programme d’installation retourne l’indicateur d’arrêt. Chaque indicateur de fin (valeur négative) peut être utilisé avec une seule action. Plusieurs actions peuvent avoir des indicateurs d’arrêt, mais elles doivent être des indicateurs différents. Les indicateurs de fin (valeurs négatives) sont généralement utilisés avec les [boîtes de dialogue](dialog-boxes.md).



| Indicateur de fin          | Valeur | Description                                                                          |
|---------------------------|-------|--------------------------------------------------------------------------------------|
| msiDoActionStatusSuccess  | -1    | Achèvement réussi. Utilisé avec les boîtes de dialogue [quitter](exit-dialog.md) .               |
| msiDoActionStatusUserExit | -2    | L’utilisateur termine l’installation. Utilisé avec les boîtes de dialogue [UserExit](userexit-dialog.md) .     |
| msiDoActionStatusFailure  | -3    | La sortie irrécupérable s’arrête. Utilisé avec les boîtes de dialogue [FatalError](fatalerror-dialog.md) . |
| msiDoActionStatusSuspend  | -4    | L’installation est suspendue.                                                                |



 

Zéro, tous les autres nombres négatifs ou une valeur null indique que l’action n’est jamais appelée.

</dd> </dl>

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
[ICE84](ice84.md)  
[ICE86](ice86.md)  
[ICE96](ice96.md)  
[ICEM04](icem04.md)  
</dl>

 

 



