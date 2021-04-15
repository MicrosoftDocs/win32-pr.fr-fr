---
description: Montre comment ajouter des éléments à la liste de raccourcis automatique pour une application, y compris le basculement entre l’affichage des catégories fréquentes et récentes.
title: Liste de raccourcis automatique, exemple
ms.topic: article
ms.date: 05/31/2018
ms.assetid: C33152FE-1322-42f8-A656-3D5FAF4B612D
api_name: ''
api_type: ''
api_location: ''
topic_type:
- kbArticle
ms.openlocfilehash: ce0b6520163fcb07bb990b7a5a9fe742d976a899
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104485561"
---
# <a name="automatic-jump-list-sample"></a>Liste de raccourcis automatique, exemple

Montre comment ajouter des éléments à la liste de raccourcis automatique pour une application, y compris le basculement entre l’affichage des catégories fréquentes et récentes.

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
| GitHub  | [Exemple AutomaticJumpList](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/winui/shell/appshellintegration/AutomaticJumpList) |

## <a name="building-the-sample"></a>Génération de l'exemple

Pour générer l’exemple à partir de l’invite de commandes :

1.  Ouvrez la fenêtre d’invite de commandes et accédez au répertoire du projet **AutomaticJumpList** .
2.  Entrez `msbuild AutomaticJumpListSample.sln`.

Pour générer l’exemple à l’aide de Microsoft Visual Studio (par défaut) :

1.  Ouvrez l’Explorateur Windows et accédez au répertoire du projet **AutomaticJumpList** .
2.  Double-cliquez sur l’icône du fichier AutomaticJumpListSample. sln pour ouvrir le projet dans Visual Studio.
3.  Dans le menu **générer** , sélectionnez **générer la solution**.

## <a name="running-the-sample"></a>Exécution de l'exemple

1.  Accédez au répertoire qui contient le nouveau fichier exécutable à l’aide de l’invite de commandes ou de l’Explorateur Windows.
2.  Sur la ligne de commande, entrez `AutomaticJumpListSample.exe` . Vous pouvez également, à partir de l’Explorateur Windows, double-cliquer sur l’icône de AutomaticJumpListSample.exe.
3.  Cet exemple doit être exécuté en tant qu’administrateur la première fois qu’il est exécuté afin de pouvoir installer les inscriptions de types de fichiers nécessaires. Une fois les types de fichiers enregistrés, l’exemple peut s’exécuter en tant qu’utilisateur standard.
4.  Sélectionnez des options dans le menu de l’exemple d’application, notamment la sélection des documents. txt ou. doc via la boîte de dialogue **ouvrir** pour voir comment ils affectent la liste de raccourcis de l’application dans la barre des tâches.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[ID de modèle d’utilisateur d’application (AppUserModelIDs)](appids.md)
</dt> </dl>

 

 



