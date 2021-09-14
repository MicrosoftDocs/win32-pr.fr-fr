---
description: ICE13 vérifie que les boîtes de dialogue des tables de séquences s’affichent dans les tables AdminUISequence ou InstallUISequence. Les boîtes de dialogue ne doivent pas figurer dans les tables InstallExecuteSequence, AdminExecuteSequence ou AdvtExecuteSequence.
ms.assetid: 51542a8f-2fb6-4021-b52d-6f7a2b0294d6
title: ICE13
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1fff440217ccffe41d5e4036f4ea0d03d1eabb0b
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127021614"
---
# <a name="ice13"></a>ICE13

ICE13 vérifie que les boîtes de dialogue des tables de séquences s’affichent dans les tables [AdminUISequence](adminuisequence-table.md)ou [InstallUISequence](installuisequence-table.md) . Les boîtes de dialogue ne doivent pas figurer dans les tables [InstallExecuteSequence](installexecutesequence-table.md), [AdminExecuteSequence](adminexecutesequence-table.md)ou [AdvtExecuteSequence](advtexecutesequence-table.md) .

## <a name="result"></a>Résultats

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

 

 



