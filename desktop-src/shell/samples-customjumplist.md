---
description: Montre comment créer une liste de raccourcis personnalisée pour une application, y compris l’ajout d’une catégorie et de tâches personnalisées.
title: Liste de raccourcis personnalisée, exemple
ms.topic: article
ms.date: 05/31/2018
ms.assetid: 60DEDB01-8F8F-4c25-8FCC-8EAC461A99B7
api_name: ''
api_type: ''
api_location: ''
topic_type:
- kbArticle
ms.openlocfilehash: 3eb6f5db0b9576f360abcbaacb8a8a5a291d3dbe07754281954ea585d3ebe965
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118968828"
---
# <a name="custom-jump-list-sample"></a>Liste de raccourcis personnalisée, exemple

Montre comment créer une liste de raccourcis personnalisée pour une application, y compris l’ajout d’une catégorie et de tâches personnalisées.

Cette rubrique contient les sections suivantes.

-   [Requirements](#requirements)
-   [Téléchargement de l’exemple](#downloading-the-sample)
-   [Génération de l'exemple](#building-the-sample)
-   [Exécution de l’exemple](#running-the-sample)
-   [Rubriques connexes](#related-topics)

## <a name="requirements"></a>Configuration requise



| Produit                                | Version minimale du produit |
|----------------------------------------|-------------------------|
| Windows                                | Windows 7               |
| Kit de développement logiciel Windows | 7.0                     |



 

## <a name="downloading-the-sample"></a>Téléchargement de l’exemple

| Emplacement      | URL du chemin                                                                                             |
|---------------|------------------------------------------------------------------------------------------------------|
| GitHub  | [Exemple CustomJumpList](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/winui/shell/appshellintegration/CustomJumpList) |

## <a name="building-the-sample"></a>Génération de l'exemple

Pour générer l’exemple à partir de l’invite de commandes :

1.  Ouvrez la fenêtre d’invite de commandes et accédez au répertoire du projet **CustomJumpList** .
2.  Entrez `msbuild CustomJumpListSample.sln`.

pour générer l’exemple à l’aide de Microsoft Visual Studio (par défaut) :

1.  ouvrez Windows Explorer et accédez au répertoire du projet **CustomJumpList** .
2.  Double-cliquez sur l’icône du fichier CustomJumpListSample. sln pour ouvrir le projet dans Visual Studio.
3.  Dans le menu **Générer**, sélectionnez **Générer la solution**.

## <a name="running-the-sample"></a>Exécution de l'exemple

1.  accédez au répertoire qui contient le nouveau fichier exécutable à l’aide de l’invite de commandes ou de l’explorateur de Windows.
2.  Sur la ligne de commande, entrez `CustomJumpListSample.exe` . vous pouvez également, à partir de Windows Explorer, double-cliquer sur l’icône de CustomJumpListSample.exe.
3.  Cet exemple doit être exécuté en tant qu’administrateur la première fois qu’il est exécuté afin de pouvoir installer les inscriptions de types de fichiers nécessaires. Une fois les types de fichiers enregistrés, l’exemple peut s’exécuter en tant qu’utilisateur standard.
4.  Sélectionnez des options dans le menu de l’exemple d’application pour voir comment elles affectent la liste de raccourcis de l’application dans la barre des tâches.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[ID de modèle d’utilisateur d’application (AppUserModelIDs)](appids.md)
</dt> </dl>

 

 



