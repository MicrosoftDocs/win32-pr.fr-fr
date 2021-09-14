---
description: ICE63 vérifie le séquencement approprié de l’action RemoveExistingProducts.
ms.assetid: 4dd67bb0-c08a-4a44-b687-0394a3afc2c4
title: ICE63
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d5faa6f2ddbcb95cdf12966c2887fe9438a5d610
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127021518"
---
# <a name="ice63"></a>ICE63

ICE63 vérifie le séquencement approprié de l' [action RemoveExistingProducts](removeexistingproducts-action.md). L’action RemoveExistingProducts peut être placée :

1.  Entre InstallValidate et InstallInitialize
2.  Immédiatement après InstallInitialize, ou après InstallInitialize si les actions entre InstallInitialize et RemoveExistingProducts ne génèrent pas d’actions de script.
3.  Immédiatement après InstallExecute ou InstallExecuteAgain et avant InstallFinalize (la même restriction que ci-dessus s’applique).
4.  Après InstallFinalize.

L’échec de la résolution d’un avertissement ou d’une erreur signalée par ICE63 provoque l’échec de la mise à niveau.

## <a name="result"></a>Résultats

ICE63 publie un avertissement ou une erreur si le séquencement de l’action RemoveExistingProducts n’est pas correct.

## <a name="example"></a>Exemple

ICE63 signale l’erreur suivante pour l’exemple indiqué.

``` syntax
WARNING: Some action falls between InstallInitialize and RemoveExistingProducts.
```

L’action « MyCustomAction » se produit entre InstallInitialize et RemoveExistingProducts. Si MyCustomAction génère des actions dans le script, cela provoque des problèmes lors de l’installation.

Pour corriger cette erreur, vérifiez que MyCustomAction ne génère pas d’actions de script ou reséquencez les actions.

[Table InstallExecuteSequence](installexecutesequence-table.md)



| Action                 | Condition | Séquence |
|------------------------|-----------|----------|
| InstallInitialize      |           | 1 000     |
| MyCustomAction         |           | 1010     |
| RemoveExistingProducts |           | 1020     |



 

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Référence ICE](ice-reference.md)
</dt> </dl>

 

 



