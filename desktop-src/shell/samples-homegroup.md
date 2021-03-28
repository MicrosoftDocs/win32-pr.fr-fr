---
description: Montre comment déterminer l’état de l’appartenance à un groupe résidentiel, comment énumérer les éléments de niveau supérieur dans le dossier de Shell du groupe résidentiel et comment lancer l’Assistant partage du groupe résidentiel.
title: HomeGroup, exemple
ms.topic: article
ms.date: 05/31/2018
ms.assetid: FDEFF261-BF86-4fbb-8567-892F79F23D92
api_name: ''
api_type: ''
api_location: ''
topic_type:
- kbArticle
ms.openlocfilehash: c22ea84431f464ef8fcae6bfad0d90a45ba310d7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104034676"
---
# <a name="homegroup-sample"></a>HomeGroup, exemple

Montre comment déterminer l’état de l’appartenance à un groupe résidentiel, comment énumérer les éléments de niveau supérieur dans le dossier de Shell du **groupe résidentiel** et comment lancer l' **Assistant partage du groupe résidentiel**.

Cette rubrique contient les sections suivantes.

-   [Configuration requise](#requirements)
-   [Téléchargement de l’exemple](#downloading-the-sample)
-   [Génération de l'exemple](#building-the-sample)
-   [Exécution de l’exemple](#running-the-sample)
-   [Rubriques connexes](#related-topics)

## <a name="requirements"></a>Spécifications



| Produit                                | Version minimale du produit |
|----------------------------------------|-------------------------|
| Windows                                | Windows 7               |
| Kit de développement logiciel Windows | 7.0                     |



 

## <a name="downloading-the-sample"></a>Téléchargement de l’exemple

| Emplacement      | URL du chemin                                                                                             |
|---------------|------------------------------------------------------------------------------------------------------|
| GitHub  | [Exemple de groupe résidentiel](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/winui/shell/appshellintegration/HomeGroup) |

## <a name="building-the-sample"></a>Génération de l'exemple

Pour générer l’exemple à partir de l’invite de commandes :

1.  Ouvrez la fenêtre d’invite de commandes et accédez au répertoire du projet de **groupe résidentiel** .
2.  Entrez `msbuild HomeGroup.sln`.

Pour générer l’exemple à l’aide de Microsoft Visual Studio (par défaut) :

1.  Ouvrez l’Explorateur Windows et accédez au répertoire du projet de **groupe résidentiel** .
2.  Double-cliquez sur l’icône du fichier de groupe résidentiel. sln pour ouvrir le projet dans Visual Studio.
3.  Dans le menu **générer** , sélectionnez **générer la solution**.

## <a name="running-the-sample"></a>Exécution de l'exemple

1.  Accédez au répertoire qui contient le nouveau fichier exécutable à l’aide de l’invite de commandes ou de l’Explorateur Windows.
2.  Sur la ligne de commande, entrez `HomeGroup.exe` . Vous pouvez également, à partir de l’Explorateur Windows, double-cliquer sur l’icône de HomeGroup.exe.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[**IHomeGroup**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ihomegroup)
</dt> <dt>

[**KNOWNFOLDERID**](knownfolderid.md)
</dt> </dl>

 

 



