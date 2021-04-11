---
description: ICE77 vérifie que les actions personnalisées avec le jeu de bits msidbCustomActionTypeInScript sont séquencées après l’action InstallInitialize et avant l’action InstallFinalize.
ms.assetid: 291cf731-b7e6-44c2-a8ec-78e0e037d1f5
title: ICE77
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 15e072692b76cfd63bf62c5fd23f612a445e5fd7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104113855"
---
# <a name="ice77"></a>ICE77

ICE77 vérifie que les actions personnalisées avec le jeu de bits **msidbCustomActionTypeInScript** sont séquencées après l' [action InstallInitialize](installinitialize-action.md) et avant l' [action InstallFinalize](installfinalize-action.md). ICE77 vérifie la séquence dans la [table InstallExecuteSequence](installexecutesequence-table.md) et la [table AdminExecuteSequence](adminexecutesequence-table.md).

## <a name="result"></a>Résultats

ICE77 publie une erreur si une action personnalisée dans le script est séquencée avant l’action InstallInitialize ou après l’action InstallFinalize.

ICE77 publie une erreur si l’action InstallInitialize ou l’action InstallFinalize est manquante.

## <a name="example"></a>Exemple

ICE77 signale les erreurs suivantes pour l’exemple :

``` syntax
InstallFinalize is missing from 'InstallExecuteSequence'. 
CA_InScriptInstall is a in-script custom action. It must be sequenced 
before the InstallFinalize action.
 
CA_InScriptAdmin is a in-script custom action.  It must be sequenced 
in between the InstallInitialize action and the InstallFinalize action 
in the AdminExecuteSequence Sequence table.
```

[Table CustomAction](customaction-table.md) (partielle)



| Action              | Type |
|---------------------|------|
| \_INSCRIPTINSTALL ca | 1025 |
| \_INSCRIPTADMIN ca   | 1026 |



 

[Table InstallExecuteSequence](installexecutesequence-table.md) (partielle)



| Action              | Séquence |
|---------------------|----------|
| \_INSCRIPTINSTALL ca | 2000     |
| InstallInitialize   | 1500     |



 

[Table AdminExecuteSequence](adminexecutesequence-table.md) (partielle)



| Action            | Séquence |
|-------------------|----------|
| \_INSCRIPTADMIN ca | 1400     |
| InstallInitialize | 1500     |
| InstallFinalize   | 6600     |



 

Pour corriger les erreurs, séquencez les actions personnalisées dans le script après l’action InstallInitialize et avant l’action InstallFinalize. Les actions InstallInitialize et InstallFinalize doivent être présentes dans la table InstallExecuteSequence et la table AdminExecuteSequence.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Référence ICE](ice-reference.md)
</dt> </dl>

 

 



