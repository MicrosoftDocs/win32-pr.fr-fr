---
description: ICE13 vérifie que les boîtes de dialogue des tables de séquences s’affichent dans les tables AdminUISequence ou InstallUISequence. Les boîtes de dialogue ne doivent pas figurer dans les tables InstallExecuteSequence, AdminExecuteSequence ou AdvtExecuteSequence.
ms.assetid: 51542a8f-2fb6-4021-b52d-6f7a2b0294d6
title: ICE13
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8fdc11f8254c721d404a65e63fc897aa6e55bc61364c768b48f2d5aded4348d8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118946633"
---
# <a name="ice13"></a>ICE13

ICE13 vérifie que les boîtes de dialogue des tables de séquences s’affichent dans les tables [AdminUISequence](adminuisequence-table.md)ou [InstallUISequence](installuisequence-table.md) . Les boîtes de dialogue ne doivent pas figurer dans les tables [InstallExecuteSequence](installexecutesequence-table.md), [AdminExecuteSequence](adminexecutesequence-table.md)ou [AdvtExecuteSequence](advtexecutesequence-table.md) .

## <a name="result"></a>Résultat

ICE13 publie un message d’erreur si une boîte de dialogue s’affiche dans une table de séquence d’exécution.

## <a name="example"></a>Exemple

Dans l’exemple suivant, ICE13 publie un message d’erreur indiquant que « WelcomeDialog » ne peut pas être listé dans la table « InstallExecuteSequence ».

[Table InstallExecuteSequence](installexecutesequence-table.md) (partielle)



| Action          |
|-----------------|
| InstallFinalize |
| CostFinalize    |
| WelcomeDialog   |



 

[Table InstallUISequence](installuisequence-table.md) (partielle)



| Action         |
|----------------|
| CostFinalize   |
| CostInitialize |
| BrowseDialog   |



 

[Table de boîtes de dialogue](dialog-table.md) (partielle)



| Boîte de dialogue        |
|---------------|
| BrowseDialog  |
| WelcomeDialog |



 

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Référence ICE](ice-reference.md)
</dt> </dl>

 

 



