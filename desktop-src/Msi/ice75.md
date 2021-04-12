---
description: ICE75 vérifie que toutes les actions personnalisées de type d’action personnalisé 17 (DLL), de type d’action personnalisée 18 (EXE), de type d’action personnalisée 21 (JScript) et de type d’action personnalisée 22 (VBScript) sont séquencées après l’action CostFinalize.
ms.assetid: 831de042-bea6-42da-90a0-3847bb447414
title: ICE75
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 23d708552b3ed2d397e29d37abdf0ceed01093fd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104319918"
---
# <a name="ice75"></a>ICE75

ICE75 vérifie que toutes les actions personnalisées de type d' [action personnalisé 17](custom-action-type-17.md) (dll), de [type d’action personnalisée 18](custom-action-type-18.md) (exe), de [type d’action personnalisée 21](custom-action-type-21.md) (JScript) et de [type d’action personnalisée 22](custom-action-type-22.md) (VBScript) sont séquencées après l' [action CostFinalize](costfinalize-action.md). Ces types d’actions personnalisées utilisent un fichier installé comme source. ICE75 vérifie la table [InstallUISequence](installuisequence-table.md), la table [InstallExecuteSequence](installexecutesequence-table.md), la table [AdminUISequence](adminuisequence-table.md)et la [table AdminExecuteSequence](adminexecutesequence-table.md). Notez que l’action CostFinalize est requise dans ces tables de séquence.

## <a name="result"></a>Résultats

ICE75 publie une erreur s’il trouve une action personnalisée à l’aide d’un fichier installé comme fichier source qui n’est pas séquencé après l’action CostFinalize.

## <a name="example"></a>Exemple

ICE75 signale les erreurs suivantes pour l’exemple illustré :

``` syntax
CostFinalize is missing from 'AdminUISequence'. CA_FileExe is a custom
 action whose source is an installed file. It must be sequenced after 
the CostFinalize action.
 
CA_FileDLL is a custom action whose source is an installed file.  It 
must be sequenced after the CostFinalize action in the 
AdminExecuteSequence table
```

[Table CustomAction](customaction-table.md) (partielle)



| Action      | Type | Source  |
|-------------|------|---------|
| \_FILEEXE ca | 18   | FileExe |
| \_FILEDLL ca | 17   | FileDLL |



 

[Table AdminUISequence](adminuisequence-table.md) (partielle)



| Action      | Séquence |
|-------------|----------|
| \_FILEEXE ca | 1100     |



 

[Table AdminExecuteSequence](adminexecutesequence-table.md) (partielle)



| Action       | Séquence |
|--------------|----------|
| \_FILEDLL ca  | 800      |
| CostFinalize | 1 000     |



 

Pour corriger les erreurs, séquencez les actions personnalisées après l’action CostFinalize.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Référence ICE](ice-reference.md)
</dt> </dl>

 

 



