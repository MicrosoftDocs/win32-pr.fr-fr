---
description: ICEM04 vérifie que les tables vides requises du module de fusion sont vides. Si vous ne corrigez pas une erreur signalant que les rapports ICEM04 peuvent entraîner une fusion incorrecte du module de fusion.
ms.assetid: c6f64f5e-be65-485b-8831-e377535bd335
title: ICEM04
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f2ef993690ae690e0651db1538196998c4dd28c7
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127021437"
---
# <a name="icem04"></a>ICEM04

ICEM04 vérifie que les tables vides requises du module de fusion sont vides. Si vous ne corrigez pas une erreur signalant que les rapports ICEM04 peuvent entraîner une fusion incorrecte du module de fusion.

## <a name="result"></a>Résultats

ICEM04 publie une erreur lorsque les tables vides requises du module de fusion ne sont pas vides.

## <a name="example"></a>Exemple

ICEM04 publie les messages d’erreur suivants pour un module qui contient les entrées de base de données affichées.

``` syntax
An empty FeatureComponents table is required in a Merge Module.

The Merge Module contains the 'ModuleInstallExecuteSequence' table. It 
must therefore have an empty 'InstallExecuteSequence' table.

Action 'CostInitialize' found in the AdvtExecuteSequence table. This 
table must be empty in a Merge Module
```

Le tableau suivant présente une [table AdvtExecuteSequence](advtexecutesequence-table.md)partielle.



| Action         | Séquence |
|----------------|----------|
| CostInitialize | 1        |



 

La liste suivante affiche le contenu partiel de MergeModule :

-   ModuleInstallExecuteSequence
-   ModuleAdvtExecuteSequence
-   InstallUISequence

L’exemple suivant montre une autre erreur possible.

``` syntax
Feature-Component '[1].[2]' found in the FeatureComponents table. The 
FeatureComponents table must be empty in a Merge Module.
```

Si un module de fusion contient une table de séquence de module, il doit contenir la table de séquences vide correspondante, que la table de séquence de module soit vide ou non. Par exemple, si le module de fusion contient la [table ModuleAdminExecuteSequence](moduleadminexecutesequence-table.md), il doit également contenir une table AdminExecuteSequence vide.

La [table FeatureComponents](featurecomponents-table.md) est requise dans tous les modules de fusion et doit être vide.

La procédure suivante vous montre comment corriger les erreurs.

**Pour résoudre les erreurs**

1.  Ajoutez une [table FeatureComponents](featurecomponents-table.md) vide au module de fusion.
2.  Ajoutez une [table InstallExecuteSequence](installexecutesequence-table.md) vide au module de fusion.
3.  Supprimez l’action « CostInitialize » de la [table AdvtExecuteSequence](advtexecutesequence-table.md).
    > [!Note]  
    > Cette table doit être vide dans un module de fusion. Les actions doivent apparaître uniquement dans la table ModuleAdvtExecuteSequence.

     

## <a name="tables-used-during-execution"></a>Tables utilisées lors de l’exécution

La liste suivante identifie les tables utilisées lors de l’exécution :

-   [Table FeatureComponents](featurecomponents-table.md)
-   \*Tables de séquence de module et tables de séquence correspondantes \* .

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[À propos des modules de fusion](about-merge-modules.md)
</dt> <dt>

[Référence ICE du module de fusion](merge-module-ice-reference.md)
</dt> </dl>

 

 



