---
description: ICE72 vérifie que les actions personnalisées non intégrées ne sont pas utilisées dans la table AdvtExecuteSequence.
ms.assetid: b04227d5-5bd6-434a-860c-498d787a1f0a
title: ICE72
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7d9d8e1859ffd8123cc7aa3dc801c5484d28ccb2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106529378"
---
# <a name="ice72"></a>ICE72

ICE72 vérifie que les actions personnalisées non intégrées ne sont pas utilisées dans la [table AdvtExecuteSequence](advtexecutesequence-table.md). Plus précisément, seules les actions personnalisées de type 19, de type 35 et de type 51 sont autorisées dans la table AdvtExecuteSequence. Si d’autres actions personnalisées sont utilisées, la publication peut ne pas se comporter comme prévu.

## <a name="result"></a>Résultats

ICE72 retourne une erreur si la table AdvExecuteSequence utilise des actions personnalisées autres que le type 35, le type 51 et le type 19.

## <a name="example"></a>Exemple

ICE72 signale l’erreur suivante pour l’exemple ci-dessous :

``` syntax
Custom Action 'CA1' in the AdvtExecuteSequence table is not allowed. Only built-in custom actions are allowed.
```

Pour corriger l’erreur, supprimez « CA1 » de la table AdvtExecuteSequence.

[Table AdvtExecuteSequence](advtexecutesequence-table.md) (partielle)



| Action |
|--------|
| AC1    |
| CA35   |



 

[Table CustomAction](customaction-table.md) (partielle)



| Action | Type |
|--------|------|
| AC1    | 1    |
| CA35   | 35   |



 

## <a name="tables-used-during-execution"></a>Tables utilisées lors de l’exécution

[Table AdvtExecuteSequence](advtexecutesequence-table.md)

[Table CustomAction](customaction-table.md)

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Type d’action personnalisée 19](custom-action-type-19.md)
</dt> <dt>

[Type d’action personnalisé 35](custom-action-type-35.md)
</dt> <dt>

[Type d’action personnalisé 51](custom-action-type-51.md)
</dt> <dt>

[Référence ICE](ice-reference.md)
</dt> </dl>

 

 



