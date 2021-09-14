---
description: ICE28 est couramment utilisé pour confirmer que l’action ForceReboot est placée avant ou après, et jamais dans, un groupe spécifique d’actions dans les tables de séquences d’actions. Consultez la rubrique d’action ForceReboot pour déterminer les actions qui composent ce groupe.
ms.assetid: 746d907a-33e1-479a-bcb0-93e7fd5dd975
title: ICE28
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bc65878bdc3db4f9b79ba95b4a170b694a4728ff
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127021583"
---
# <a name="ice28"></a>ICE28

ICE28 est couramment utilisé pour confirmer que l’action ForceReboot est placée avant ou après, et jamais dans, un groupe spécifique d’actions dans les tables de séquences d’actions. Consultez la rubrique d' [action ForceReboot](forcereboot-action.md) pour déterminer les actions qui composent ce groupe.

ICE28 valide les actions dans les tableaux de séquence suivants :

[Table AdminUISequence](adminuisequence-table.md)

[Table AdminExecuteSequence](adminexecutesequence-table.md)

[Table InstallUISequence](installuisequence-table.md)

[Table InstallExecuteSequence](installexecutesequence-table.md)

## <a name="result"></a>Résultats

ICE28 publie un message d’erreur si ForceReboot est séquencé dans le groupe d’actions spécifié.

## <a name="example"></a>Exemple

Pour l’exemple illustré, ICE28 publie le message d’erreur suivant :

``` syntax
Action: 'ForceReboot' of table InstallExecuteSequence is not permitted in the range 5 to 15 because it cannot separate a set of actions contained in this range.
```

[Table InstallExecuteSequence](installexecutesequence-table.md)



| Action             | Séquence |
|--------------------|----------|
| ForceReboot        | 10       |
| RegisterMIMEInfo   |   5      |
| RegisterProgIdInfo | 15       |



 

Le numéro de séquence 10 donné aux arrêts ForceReboot génère l’erreur, car il est compris entre les numéros de séquence de RegisterMIMEInfo et de RegisterProgIdInfo.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Référence ICE](ice-reference.md)
</dt> </dl>

 

 



