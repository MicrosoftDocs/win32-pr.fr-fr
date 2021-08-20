---
description: ICE63 vérifie le séquencement approprié de l’action RemoveExistingProducts.
ms.assetid: 4dd67bb0-c08a-4a44-b687-0394a3afc2c4
title: ICE63
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4f0de847a3b79c87b8ddc7dbaf3be64f88b9ef34df80d92737b6d9005ffdad24
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118142493"
---
# <a name="ice63"></a>ICE63

ICE63 vérifie le séquencement approprié de l' [action RemoveExistingProducts](removeexistingproducts-action.md). L’action RemoveExistingProducts peut être placée :

1.  Entre InstallValidate et InstallInitialize
2.  Immédiatement après InstallInitialize, ou après InstallInitialize si les actions entre InstallInitialize et RemoveExistingProducts ne génèrent pas d’actions de script.
3.  Immédiatement après InstallExecute ou InstallExecuteAgain et avant InstallFinalize (la même restriction que ci-dessus s’applique).
4.  Après InstallFinalize.

L’échec de la résolution d’un avertissement ou d’une erreur signalée par ICE63 provoque l’échec de la mise à niveau.

## <a name="result"></a>Résultat

ICE63 publie un avertissement ou une erreur si le séquencement de l’action RemoveExistingProducts n’est pas correct.

## <a name="example"></a>Exemples

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

 

 



