---
description: Incluez les tables MergeModuleSequence dans le fichier. msm si le module de fusion doit modifier les tables de séquences d’action du fichier .msi cible. La fusion n’ajoute pas ces tables au fichier .msi. Ces tables se trouvent uniquement dans les modules de fusion.
ms.assetid: 9efb75d2-43f9-404c-8e7f-918d056190cf
title: Création de tables de séquence de module de fusion
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 24b21780601e626c006967cefa0dcff5700bdec4
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127092489"
---
# <a name="authoring-merge-module-sequence-tables"></a>Création de tables de séquence de module de fusion

Incluez les tables MergeModuleSequence dans le fichier. msm si le module de fusion doit modifier les [*tables de séquences*](s-gly.md) d’action du fichier .msi cible. La fusion n’ajoute pas ces tables au fichier .msi. Ces tables se trouvent uniquement dans les modules de fusion.

Si l’une des tables ModuleSequence est présente dans un fichier. msm, une copie vide de la table de séquences du programme d’installation correspondante doit également être créée dans le module de fusion. Par exemple, si un module de fusion contient une table ModuleAdminExecuteSequence, le module de fusion doit également inclure une table AdminExecuteSequence vide. Pendant une fusion, ces tables vides fournissent l’outil de fusion avec les instructions de schéma nécessaires.

Lors de l’utilisation d' [actions standard](standard-actions.md) dans les tables de séquence de module de fusion, la valeur de la colonne Sequence doit être le numéro de séquence d’action recommandé pour l’action standard. Consultez les séquences d’actions suggérées ci-dessous pour connaître les numéros de séquence recommandés dans chaque table de séquences. Si le numéro de séquence dans la table de séquence de module de fusion diffère du numéro de séquence pour la même action dans le fichier .msi, l’outil de fusion utilise le numéro de séquence dans le fichier .msi lors de la fusion.



| Table MergeModuleSequence                                                    | Séquences d’actions recommandées                                             |
|------------------------------------------------------------------------------|--------------------------------------------------------------------------|
| [ModuleAdminUISequence](moduleadminuisequence-table.md)                     | [AdminUISequence suggéré](suggested-adminuisequence.md)               |
| [ModuleAdminExecuteSequence](moduleadminexecutesequence-table.md)           | [AdminExecuteSequence suggéré](suggested-adminexecutesequence.md)     |
| [ModuleAdvtUISequence](moduleadvtuisequence-table.md)                       | [AdvtUISequence suggéré](suggested-advtuisequence.md)                 |
| [ModuleAdvtExecuteSequence](moduleadvtexecutesequence-table.md)             | [AdvtExecuteSequence suggéré](suggested-advtexecutesequence.md)       |
| [ModuleInstallUISequence](moduleinstalluisequence-table.md)                 | [InstallUISequence suggéré](suggested-installuisequence.md)           |
| [Table ModuleInstallExecuteSequence](moduleinstallexecutesequence-table.md) | [InstallExecuteSequence suggéré](suggested-installexecutesequence.md) |



 

Si une [action standard](standard-actions.md) est utilisée dans la colonne action d’une table de séquence de module de fusion, les colonnes BaseAction et after de cet enregistrement doivent avoir la valeur null.

Si une action ou une boîte de dialogue personnalisée est entrée dans la colonne action, la colonne Sequence doit avoir la valeur null.

Si une action qui retourne un indicateur d’arrêt est entrée dans la colonne action, la colonne Sequence doit contenir la valeur négative de cet indicateur et les colonnes BaseAction et after de cet enregistrement doivent avoir la valeur null. Les valeurs négatives suivantes indiquent que l’action est appelée si le programme d’installation retourne l’indicateur d’arrêt.



| Indicateur de fin          | Valeur | Description              |
|---------------------------|-------|--------------------------|
| msiDoActionStatusSuccess  | -1    | Achèvement réussi.   |
| msiDoActionStatusUserExit | -2    | L’utilisateur termine l’installation. |
| msiDoActionStatusFailure  | -3    | La sortie irrécupérable s’arrête.   |
| msiDoActionStatusSuspend  | -4    | L’installation est suspendue.    |



 

La colonne BaseAction peut contenir une action standard, une action personnalisée spécifiée dans la table d’actions personnalisée du module de fusion ou une boîte de dialogue spécifiée dans la table de boîte de dialogue du module. La colonne BaseAction est une clé dans la colonne action de ce tableau. Il ne peut pas s’agir d’une clé étrangère dans une autre table de fusion ou table dans le fichier .msi. Cela signifie que chaque action standard, action personnalisée ou boîte de dialogue figurant dans la colonne BaseAction doit également figurer dans la colonne action d’un autre enregistrement dans ce tableau.

 

 



