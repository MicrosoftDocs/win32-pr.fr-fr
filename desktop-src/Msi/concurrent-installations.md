---
description: les installations simultanées, également appelées installations imbriquées, constituent une fonctionnalité dépréciée du Windows Installer.
ms.assetid: 579ae4ee-47a0-440e-81ca-ea8bf60c5349
title: Installations simultanées
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d89f2ef4af062c8151935fefab471603f79d7633
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127092066"
---
# <a name="concurrent-installations"></a>Installations simultanées

les installations simultanées, également appelées installations imbriquées, constituent une fonctionnalité dépréciée du Windows Installer. Les applications installées avec des installations simultanées peuvent échouer, car elles sont difficiles à traiter correctement pour les clients. N’utilisez pas d’installations simultanées pour installer des produits destinés à être diffusés au public. Les installations simultanées peuvent avoir une applicabilité limitée dans les environnements d’entreprise contrôlés lorsqu’ils sont utilisés pour installer des applications qui ne sont pas destinées à une version publique. La documentation sur les installations simultanées est fournie pour les auteurs de packages qui souhaitent utiliser des installations simultanées avec des applications qui ne sont pas destinées à la distribution publique.

une action d’installation simultanée installe un autre package de Windows Installer lors de l’installation en cours. Une installation simultanée est ajoutée à un package en créant une action d’installation simultanée dans la [table CustomAction](customaction-table.md) et en planifiant cette action personnalisée dans les tables de séquence. Le champ cible de la table CustomAction contient une chaîne de paramètres de propriété publique utilisée par l’installation simultanée. Le champ source de la table CustomAction identifie le package simultané. Une action d’installation simultanée peut uniquement réinstaller ou supprimer une application qui a été installée par le package d’installation de l’application actuelle.

Le type d’action d’installation simultanée est spécifié dans le champ type de la table CustomAction. Selon le type d’action personnalisé, le package de l’application simultanée peut résider dans un sous-stockage du package principal, sous la forme d’un fichier à un emplacement spécifié par une propriété, ou sous la forme d’une application publiée sur l’ordinateur de l’utilisateur. Les types d’actions personnalisées suivants effectuent une installation simultanée.



| Type d’action personnalisé                                 | Description                                                                     |
|----------------------------------------------------|---------------------------------------------------------------------------------|
| [Type d’action personnalisé 7](custom-action-type-7.md)   | Installation simultanée d’un produit résidant dans le package d’installation.      |
| [Type d’action personnalisé 23](custom-action-type-23.md) | Installation simultanée d’un package d’installation dans l’arborescence source actuelle. |
| [Type d’action personnalisé 39](custom-action-type-39.md) | Installation simultanée d’un package d’installation publié.                     |



 

Une installation simultanée partage les mêmes paramètres d’interface utilisateur et de journalisation que l’installation principale.

Les actions d’installation simultanée doivent être placées entre l’action [InstallInitialize](installinitialize-action.md) et l' [action InstallFinalize](installfinalize-action.md) de la séquence d’action de l’installation principale. Lors de la restauration de l’installation principale, le programme d’installation annule également l’installation simultanée. L’utilisation d’une [exécution différée](deferred-execution-custom-actions.md) avec des actions d’installation simultanées est inutile, car le programme d’installation combine les informations de restauration des installations simultanées et principales. Toutes les modifications sont annulées lors de l’installation d’une restauration.

Les valeurs de retour pour les actions d’installation simultanées sont les mêmes que pour d’autres actions personnalisées. Consultez [valeurs de retour de l’action personnalisée](custom-action-return-values.md).

Les actions standard ou personnalisées qui spécifient un redémarrage automatique du système ou demandent à l’utilisateur de redémarrer, peuvent également effectuer un redémarrage ou une demande à partir d’une installation simultanée.

Une fois que le programme d’installation a lancé une installation simultanée, il verrouille toutes les autres installations jusqu’à ce que l’installation simultanée soit terminée et avant de poursuivre l’installation principale. Le programme d’installation peut uniquement exécuter des installations simultanées en tant qu’actions personnalisées synchrones. Consultez [actions personnalisées synchrones et asynchrones](synchronous-and-asynchronous-custom-actions.md). Les indicateurs d’option décrits dans [options de traitement des retours d’actions personnalisées](custom-action-return-processing-options.md) doivent être définis sur aucun (+ 0) ou **msidbCustomActionTypeContinue** (+ 64).

Une action d’installation simultanée peut installer une application pour qu’elle soit exécutée localement, pour être exécutée à partir de la source, pour être réinstallée ou supprimée de la même façon que lors de l’utilisation de [**MsiInstallProduct**](/windows/desktop/api/Msi/nf-msi-msiinstallproducta) pour une installation normale. Pour spécifier le type d’installation, transmettez la propriété [**addlocal**](addlocal.md), [**addsource**](addsource.md), [**REINSTALL**](reinstall.md)ou [**Remove**](remove.md) à l’action d’installation simultanée.

Les actions d’installation simultanée peuvent être créées par paires, une action utilisée pour installer et l’autre action utilisée pour supprimer l’installation simultanée. Un [type d’action personnalisé 7](custom-action-type-7.md) ou un [type d’action personnalisé 23](custom-action-type-23.md) est généralement utilisé pour installer. Un [type d’action personnalisé 39](custom-action-type-39.md) est généralement utilisé pour supprimer l’installation simultanée lorsque le produit parent est désinstallé. L’enregistrement de l’action personnalisée de suppression dans la [table CustomAction](customaction-table.md) peut avoir le GUID du code du produit dans le champ source et « Remove = All » dans le champ cible. Les deux actions personnalisées doivent être créées dans la table de séquence d’action avec des conditions qui s’excluent mutuellement. Par exemple, l’action personnalisée qui installe le produit peut avoir « non installé » dans son champ condition et l’action personnalisée supprimer l’installation simultanée peut avoir REMOVE = « ALL » dans son champ condition.

Il n’existe aucune méthode pour interroger un package à son coût. Cela complique le coût d’installations simultanées. Des lignes doivent être ajoutées à la [table ReserveCost](reservecost-table.md) pour indiquer les dossiers et les pires coûts du composant associé à l’installation simultanée.

Les seules [options de traitement de retour d’action personnalisées](custom-action-return-processing-options.md) disponibles avec des actions d’installation simultanées sont None (+ 0) ou **msidbCustomActionTypeContinue** (+ 64).

Notez qu’une installation parente ne peut pas appeler son propre package en tant qu’action d’installation simultanée.

Notez que si une installation par ordinateur tente d’exécuter une installation simultanée par utilisateur, le programme d’installation inscrit l’installation parente en tant qu’utilisateur par défaut. Cela peut entraîner la suppression incorrecte de l’application par le programme d’installation, car le programme d’installation tente de désinstaller l’application par ordinateur lorsqu’elle est inscrite en tant qu’utilisateur par utilisateur. Pour forcer l’état d’une installation simultanée à suivre l’état de son installation parente, entrez ALLUSERS = " \[ ALLUSERS \] " dans la colonne cible de la [table CustomAction](customaction-table.md). Dans ce cas, l’installation simultanée est par machine si le parent est par ordinateur, et si l’installation simultanée est par utilisateur si le parent est par utilisateur.

Les développeurs doivent noter les avertissements suivants lors de la création d’installations simultanées.

-   Les installations simultanées ne peuvent pas partager des composants.
-   Une installation d’administration ne peut pas également contenir une installation simultanée.
-   L’application de correctifs et la mise à niveau peuvent ne pas fonctionner avec des installations simultanées.
-   Le programme d’installation peut ne pas coûter correctement une installation simultanée.
-   Les ProgressBars intégrés ne peuvent pas être utilisés avec des installations simultanées.
-   Les ressources qui doivent être publiées ne peuvent pas être installées par l’installation simultanée.
-   Un package qui effectue une installation simultanée d’une application doit également désinstaller l’application simultanée lorsque le produit parent est désinstallé.

Pour empêcher l’installation d’un package en tant qu’installation simultanée, ajoutez l’une des instructions conditionnelles suivantes à la table [LaunchCondition](launchcondition-table.md) . Cela évite que le package ne soit installé par une action d’installation simultanée exécutée par une autre installation. Cela n’empêche pas le package d’être supprimé par l’action [RemoveExistingProducts](removeexistingproducts-action.md) . Consultez également la propriété [**ParentOriginalDatabase**](parentoriginaldatabase.md) et la propriété [**ParentProductCode**](parentproductcode.md) .

``` syntax
"Not ParentProductCode"
```

``` syntax
"Not ParentOriginalDatabase"
```

 

 



