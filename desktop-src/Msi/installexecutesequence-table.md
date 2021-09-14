---
description: Le tableau InstallExecuteSequence répertorie les actions qui sont exécutées lors de l’exécution de l’action d’installation de niveau supérieur.
ms.assetid: 995d4159-bfc9-48b2-8328-3ae8251d785d
title: Table InstallExecuteSequence
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d7d110debacab19739c3da69abf3948d11bb7aa6
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127012076"
---
# <a name="installexecutesequence-table"></a>Table InstallExecuteSequence

Le tableau InstallExecuteSequence répertorie les actions qui sont exécutées lors de l’exécution de l' [action d’installation](install-action.md) de niveau supérieur.

Les actions de la séquence d’installation jusqu’à l' [action InstallValidate](installvalidate-action.md)et toutes les boîtes de dialogue de sortie sont situées dans la [table InstallUISequence](installuisequence-table.md). Toutes les actions du InstallValidate jusqu’à la fin de la séquence d’installation se trouvent dans la table InstallExecuteSequence. Étant donné que la table InstallExecuteSequence doit être autonome, elle comporte toutes les actions d’initialisation nécessaires, telles que les actions [LaunchConditions](launchconditions-action.md), [CostInitialize](costinitialize-action.md), [FileCost](filecost-action.md)et [CostFinalize](costfinalize-action.md) .

Les [actions personnalisées](custom-actions.md) nécessitant une interface utilisateur doivent utiliser [**MsiProcessMessage**](/windows/desktop/api/Msiquery/nf-msiquery-msiprocessmessage) au lieu de boîtes de dialogue créées créées à l’aide de la table de [boîtes de dialogue](dialog-table.md).

La table InstallExecuteSequence contient les colonnes suivantes.



| Colonne    | Type                         | Clé | Nullable |
|-----------|------------------------------|-----|----------|
| Action    | [Identificateur](identifier.md) | O   | N        |
| Condition | [Condition](condition.md)   | N   | O        |
| Séquence  | [Integer](integer.md)       | N   | O        |



 

## <a name="columns"></a>Colonnes

<dl> <dt>

<span id="Action"></span><span id="action"></span><span id="ACTION"></span>Transactionnel
</dt> <dd>

Nom de l’action à exécuter. Il s’agit d’une action intégrée ou d’une action personnalisée.

Clé de table primaire.

</dd> <dt>

<span id="Condition"></span><span id="condition"></span><span id="CONDITION"></span>Etat
</dt> <dd>

Ce champ contient une expression conditionnelle. Si l’expression prend la valeur false, l’action est ignorée. Si la syntaxe de l’expression n’est pas valide, la séquence se termine et retourne iesBadActionData. Pour plus d’informations sur la syntaxe des instructions conditionnelles, consultez [syntaxe d’instruction conditionnelle](conditional-statement-syntax.md).

</dd> <dt>

<span id="Sequence"></span><span id="sequence"></span><span id="SEQUENCE"></span>Séquence
</dt> <dd>

Nombre qui détermine la position de la séquence dans laquelle cette action doit être exécutée.

Une valeur positive représente la position de la séquence. Une valeur null indique que l’action n’est pas exécutée. Les valeurs négatives suivantes indiquent que cette action doit être exécutée si le programme d’installation retourne l’indicateur d’arrêt associé. Chaque indicateur de fin (valeur négative) peut être utilisé avec une seule action. Plusieurs actions peuvent avoir des indicateurs d’arrêt, mais elles doivent être des indicateurs différents. Les indicateurs de fin (valeurs négatives) sont généralement utilisés avec les [boîtes de dialogue](dialog-boxes.md).



| Indicateur de fin          | Valeur | Description                                                                          |
|---------------------------|-------|--------------------------------------------------------------------------------------|
| msiDoActionStatusSuccess  | -1    | Achèvement réussi. Utilisé avec les boîtes de dialogue [quitter](exit-dialog.md) .               |
| msiDoActionStatusUserExit | -2    | L’utilisateur termine l’installation. Utilisé avec les boîtes de dialogue [UserExit](userexit-dialog.md) .     |
| msiDoActionStatusFailure  | -3    | La sortie irrécupérable s’arrête. Utilisé avec les boîtes de dialogue [FatalError](fatalerror-dialog.md) . |
| msiDoActionStatusSuspend  | -4    | L’installation est suspendue.                                                                |



 

Zéro, tous les autres nombres négatifs ou une valeur null indique que l’action n’est jamais exécutée.

</dd> </dl>

## <a name="remarks"></a>Notes

Le texte localisé pour l’affichage ou la journalisation de la progression est spécifié dans la [table ActionText](actiontext-table.md).

Pour obtenir un exemple de table de séquences, consultez [utilisation d’une table de séquences](using-a-sequence-table.md).

## <a name="validation"></a>Validation

<dl>

[ICE03](ice03.md)  
[ICE06](ice06.md)  
[ICE12](ice12.md)  
[ICE13](ice13.md)  
[ICE26](ice26.md)  
[ICE27](ice27.md)  
[ICE28](ice28.md)  
[ICE46](ice46.md)  
[ICE63](ice63.md)  
[ICE75](ice75.md)  
[ICE77](ice77.md)  
[ICE79](ice79.md)  
[ICE82](ice82.md)  
[ICE83](ice83.md)  
[ICE84](ice84.md)  
[ICE86](ice86.md)  
</dl>

 

 



