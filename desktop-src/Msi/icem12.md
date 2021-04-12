---
description: ICEM12 vérifie que dans une table ModuleSequence, les actions standard ont des numéros de séquence et les actions personnalisées ont des valeurs BaseAction et after.
ms.assetid: 1a168629-9865-4412-8317-8af8b9a7b8bd
title: ICEM12
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7b37cbff2e29a85dd50ef1f044a43fdb8e48ffdd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104034122"
---
# <a name="icem12"></a>ICEM12

ICEM12 vérifie que dans une table ModuleSequence, les actions standard ont des numéros de séquence et les actions personnalisées ont des valeurs BaseAction et after.

Ce ICEM est disponible dans le fichier Mergemod. CUB fourni dans le kit de développement logiciel (SDK) Windows Installer 2,0 et versions ultérieures. Pour plus d’informations, consultez [SDK Windows Components for Windows Installer Developers](platform-sdk-components-for-windows-installer-developers.md).

## <a name="result"></a>Résultats

ICEM12 publie une erreur dans les cas suivants :

-   Il trouve que le module contient une [action standard](standard-actions.md) sans numéro de séquence.
-   Elle constate qu’une action standard a des valeurs entrées dans les champs BaseAction ou after de la table [ModuleAdminUISequence](moduleadminuisequence-table.md), de la table [ModuleAdminExecuteSequence](moduleadminexecutesequence-table.md), de la table [ModuleAdvtExecuteSequence](moduleadvtexecutesequence-table.md), de la [table ModuleInstallUISequence](moduleinstalluisequence-table.md)ou de la [table ModuleInstallExecuteSequence](moduleinstallexecutesequence-table.md).
-   Il trouve que le module contient une [action personnalisée](custom-actions.md) sans aucune valeur entrée dans les champs Sequence, BaseAction ou after de la table [ModuleAdminUISequence](moduleadminuisequence-table.md), de la table [ModuleAdminExecuteSequence](moduleadminexecutesequence-table.md), de la table [ModuleAdvtExecuteSequence](moduleadvtexecutesequence-table.md), de la [table ModuleInstallUISequence](moduleinstalluisequence-table.md)ou de la [table ModuleInstallExecuteSequence](moduleinstallexecutesequence-table.md).

ICEM12 publie un avertissement s’il trouve une action personnalisée qui a un numéro de séquence spécifié, mais aucune valeur dans les champs BaseAction ou after.

Notez que toutes les actions trouvées dans la [table CustomAction](customaction-table.md) sont considérées comme des actions personnalisées. Toutes les autres actions sont considérées comme des actions standard.

## <a name="example"></a>Exemple

ICEM12 publie les messages d’erreur et d’avertissement suivants pour un module qui contient les entrées de la base de données, comme indiqué ci-dessous :

``` syntax
Error. Custom actions should use the BaseAction and After fields and not use the 
Sequence field in the Module Sequence tables. The custom action 'Action1' uses the Sequence field 
and does not use the BaseAction and After fields in the ModuleInstallExecuteSequence table. 
    
Error. Custom actions should not leave the Sequence, BaseAction, and After fields 
of the Module Sequence tables all empty. The custom action 'Action3' leaves the Sequence, 
BaseAction, and After fields empty in the ModuleAdminExecuteSequence table.

Error. Standard actions should not use the BaseAction and After fields in Module 
Sequence tables. The standard action 'Action2' has a values entered in the BaseAction 
or After fields of the ModuleAdminExecuteSequence table.

Error. Standard actions must have a entry in the Sequence field of Module Sequence 
tables. The standard action 'Action2' does not have a Sequence value in the 
ModuleExecuteSequence table.
```

[CustomAction](customaction-table.md)



| Action  | Type | Source  | Cible  |
|---------|------|---------|---------|
| Action1 | 30   | source1 | target1 |
| Action3 | 30   | source3 | target3 |



 

[ModuleAdminExecuteSequence](moduleadminexecutesequence-table.md)



| Action  | Séquence | BaseAction | After | Condition |
|---------|----------|------------|-------|-----------|
| Action2 |          | Action1    | 1     | true      |
| Action3 |          |            |       | true      |



 

[ModuleInstallExecuteSequence](moduleinstallexecutesequence-table.md)



| Action  | Séquence | BaseAction | After | Condition |
|---------|----------|------------|-------|-----------|
| Action1 | 1        |            |       | true      |



 

Pour corriger ces erreurs, essayez ce qui suit :

-   Supprimez le numéro de séquence de l’action personnalisée action1 et utilisez à la place les champs BaseAction et after.
-   Entrez les valeurs dans les champs Sequence, BaseAction ou after pour l’action personnalisée Action3. Laissez les champs BaseAction et after vides pour l’action standard action2.
-   Ne laissez pas le champ séquence vide pour l’action standard action2.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Référence ICE du module de fusion](merge-module-ice-reference.md)
</dt> </dl>

 

 



