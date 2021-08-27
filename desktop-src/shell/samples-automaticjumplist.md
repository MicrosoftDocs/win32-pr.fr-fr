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
ms.openlocfilehash: 4dcb2146c8db8eda0280b3ff7a34a19faf4ac172036ae7a4e61131b50fde2d0a
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120090189"
---
# <a name="automatic-jump-list-sample"></a>Liste de raccourcis automatique, exemple

Montre comment ajouter des éléments à la liste de raccourcis automatique pour une application, y compris le basculement entre l’affichage des catégories fréquentes et récentes.

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
| GitHub  | [Exemple AutomaticJumpList](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/winui/shell/appshellintegration/AutomaticJumpList) |

## <a name="building-the-sample"></a>Génération de l'exemple

Pour générer l’exemple à partir de l’invite de commandes :

1.  Ouvrez la fenêtre d’invite de commandes et accédez au répertoire du projet **AutomaticJumpList** .
2.  Entrez `msbuild AutomaticJumpListSample.sln`.

pour générer l’exemple à l’aide de Microsoft Visual Studio (par défaut) :

1.  ouvrez Windows Explorer et accédez au répertoire du projet **AutomaticJumpList** .
2.  Double-cliquez sur l’icône du fichier AutomaticJumpListSample. sln pour ouvrir le projet dans Visual Studio.
3.  Dans le menu **Générer**, sélectionnez **Générer la solution**.

## <a name="running-the-sample"></a>Exécution de l'exemple

1.  accédez au répertoire qui contient le nouveau fichier exécutable à l’aide de l’invite de commandes ou de l’explorateur de Windows.
2.  Sur la ligne de commande, entrez `AutomaticJumpListSample.exe` . vous pouvez également, à partir de Windows Explorer, double-cliquer sur l’icône de AutomaticJumpListSample.exe.
3.  Cet exemple doit être exécuté en tant qu’administrateur la première fois qu’il est exécuté afin de pouvoir installer les inscriptions de types de fichiers nécessaires. Une fois les types de fichiers enregistrés, l’exemple peut s’exécuter en tant qu’utilisateur standard.
4.  Sélectionnez des options dans le menu de l’exemple d’application, notamment la sélection de .txt ou .doc documents via la boîte de dialogue **ouvrir** pour voir comment ils affectent la liste de raccourcis de l’application dans la barre des tâches.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[ID de modèle d’utilisateur d’application (AppUserModelIDs)](appids.md)
</dt> </dl>

 

 



