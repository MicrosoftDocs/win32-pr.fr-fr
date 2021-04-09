---
title: Exemple de propriété
ms.assetid: 44642d32-2cbc-4dd9-bccc-15924f310539
description: 'En savoir plus sur : exemple de propriété'
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b9c11fda9b133ca6fa3b2f9942d8d48bec3a9e47
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104110151"
---
# <a name="property-sample"></a>Exemple de propriété

Cette rubrique décrit l’exemple de code de propriété. Il contient les sections suivantes :

-   [Description](#description)
-   [Configuration minimale requise](#minimum-requirements)
-   [Téléchargement de l’exemple](#downloading-the-sample)
-   [Génération de l'exemple](#building-the-sample)
-   [Rubriques connexes](#related-topics)

## <a name="description"></a>Description

L’exemple de propriété montre comment implémenter trois styles différents de feuilles de propriétés : modal, non modal et Assistant. Il montre également comment utiliser la fonction [*PropSheetProc*](/windows/desktop/api/Prsht/nc-prsht-pfnpropsheetcallback) pour modifier la boîte de dialogue de la feuille de propriétés avant ou après sa création.

## <a name="minimum-requirements"></a>Configuration minimale requise



| Produit          | Version                              |
|------------------|--------------------------------------|
| DLL              | comctl32.dll version 4,0             |
| Système d’exploitation | Windows 95, Microsoft Windows NT 3,1 |



 

## <a name="downloading-the-sample"></a>Téléchargement de l’exemple

L’exemple de propriété est installé dans le cadre du [Kit de développement logiciel (SDK) Windows](https://msdn.microsoft.com/windows/bb980924.aspx) et est disponible à l’emplacement suivant.



| Emplacement    | Chemin d’accès/URL                                                                                                 |
|-------------|----------------------------------------------------------------------------------------------------------|
| Kit de développement logiciel (SDK) Windows | % Program Files% \\ Microsoft SDK \\ \\ \[ numéro de version Windows exemples d’exemples de \] \\ \\ \\ contrôle WinUI \\ \\ propriété commune |



 

## <a name="building-the-sample"></a>Génération de l'exemple

Pour générer l’exemple à l’aide de l’invite de commandes :

1.  Ouvrez la fenêtre d’invite de commandes et accédez au répertoire du projet.
2.  Entrez `msbuild [project file]`.

Pour générer l’exemple à l’aide de Visual Studio :

1.  Ouvrez l’Explorateur Windows et accédez au répertoire du projet.
2.  Double-cliquez sur l’icône du fichier. vcproj pour ouvrir le projet dans Visual Studio.
3.  Dans le menu **générer** , sélectionnez **générer la solution** pour générer la solution.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[À propos des feuilles de propriétés](property-sheets.md)
</dt> </dl>

 

 




