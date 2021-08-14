---
description: Le tableau AdvtExecuteSequence répertorie les actions que le programme d’installation appelle lorsque l’action de publication de niveau supérieur est exécutée.
ms.assetid: 8873c161-a709-48b8-a66f-fe2ee9be859f
title: Table AdvtExecuteSequence
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fed9a566b721be1065e825cbf7cd6650a52c83ace653dc2730f1fcf7785d125c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118381588"
---
# <a name="advtexecutesequence-table"></a>Table AdvtExecuteSequence

Le tableau AdvtExecuteSequence répertorie les actions que le programme d’installation appelle lorsque l' [action de publication](advertise-action.md) de niveau supérieur est exécutée.

Seules les actions suivantes peuvent être utilisées dans la table AdvtExecuteSequence. Les actions personnalisées ne peuvent pas être utilisées dans cette table.

[CostFinalize](costfinalize-action.md)

[CostInitialize](costinitialize-action.md)

[CreateShortcuts](createshortcuts-action.md)

[InstallFinalize](installfinalize-action.md)

[InstallInitialize](installinitialize-action.md)

[InstallValidate](installvalidate-action.md)

[MsiPublishAssemblies](msipublishassemblies-action.md)

[PublishComponents](publishcomponents-action.md)

[PublishFeatures](publishfeatures-action.md)

[PublishProduct](publishproduct-action.md)

[RegisterClassInfo](registerclassinfo-action.md)

[RegisterExtensionInfo](registerextensioninfo-action.md)

[RegisterMIMEInfo](registermimeinfo-action.md)

[RegisterProgIdInfo](registerprogidinfo-action.md)

Les colonnes sont identiques à celles de la [table InstallExecuteSequence](installexecutesequence-table.md). La table AdvtExecuteSequence contient les colonnes suivantes.



| Colonne    | Type                         | Clé | Nullable |
|-----------|------------------------------|-----|----------|
| Action    | [Identificateur](identifier.md) | O   | N        |
| Condition | [Condition](condition.md)   | N   | O        |
| Séquence  | [Integer](integer.md)       | N   | O        |



 

## <a name="columns"></a>Colonnes

<dl> <dt>

<span id="Action"></span><span id="action"></span><span id="ACTION"></span>Transactionnel
</dt> <dd>

Nom de l' [action standard](standard-actions.md) que le programme d’installation doit exécuter. Il s’agit de la clé primaire de la table.

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
[ICE27](ice27.md)  
[ICE46](ice46.md)  
[ICE72](ice72.md)  
[ICE79](ice79.md)  
[ICE82](ice82.md)  
[ICE83](ice83.md)  
[ICE84](ice84.md)  
[ICE86](ice86.md)  
[ICEM04](icem04.md)  
</dl>

 

 



