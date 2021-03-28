---
description: Montre comment implémenter un verbe de Shell à l’aide de la méthode DropTarget.
title: DropTarget, exemple de verbe
ms.topic: article
ms.date: 05/31/2018
ms.assetid: BEAD20C9-B01A-48aa-A85A-B7171383FBDF
api_name: ''
api_type: ''
api_location: ''
topic_type:
- kbArticle
ms.openlocfilehash: 1f737c951c5bd588760dbb716859c04c0dc062fc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104973339"
---
# <a name="droptarget-verb-sample"></a>DropTarget, exemple de verbe

Montre comment implémenter un verbe de Shell à l’aide de la méthode DropTarget.

Cette rubrique contient les sections suivantes.

-   [Description](#description)
-   [Configuration requise](#requirements)
-   [Téléchargement de l’exemple](#downloading-the-sample)
-   [Génération de l'exemple](#building-the-sample)
-   [Exécution de l’exemple](#running-the-sample)

## <a name="description"></a>Description

Cet exemple montre comment implémenter un verbe de Shell à l’aide de la méthode DropTarget. Cette méthode est recommandée pour les implémentations de verbe qui doivent fonctionner sur Windows XP. Cet exemple implémente un objet COM (Component Object Model) du serveur local autonome, mais il est supposé que l’implémentation du verbe sera intégrée aux applications existantes. Pour ce faire, votre objet d’application principal inscrit une fabrique de classe pour elle-même. Cet objet implémente [**IDropTarget**](/windows/win32/api/oleidl/nn-oleidl-idroptarget) pour les verbes de votre application. Notez que COM lance votre application si elle n’est pas déjà en cours d’exécution, mais se connecte à une instance en cours d’exécution de votre application, le cas échéant.

## <a name="requirements"></a>Spécifications



| Produit                                | Version minimale du produit |
|----------------------------------------|-------------------------|
| Windows                                | Windows Vista           |
| Kit de développement logiciel Windows | 7.0                     |



 

## <a name="downloading-the-sample"></a>Téléchargement de l’exemple

| Emplacement      | URL du chemin                                                                                             |
|---------------|------------------------------------------------------------------------------------------------------|
| GitHub  | [Exemple DropTargetVerb](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/winui/shell/appshellintegration/DropTargetVerb) |

## <a name="building-the-sample"></a>Génération de l'exemple

Pour générer l’exemple à partir de l’invite de commandes :

1.  Ouvrez la fenêtre d’invite de commandes et accédez au répertoire du projet **DropTargetVerb** .
2.  Entrez `msbuild DropTargetVerb.sln`.

Pour générer l’exemple à l’aide de Microsoft Visual Studio (par défaut) :

1.  Ouvrez l’Explorateur Windows et accédez au répertoire du projet **DropTargetVerb** .
2.  Double-cliquez sur l’icône du fichier DropTargetVerb. sln pour ouvrir le projet dans Visual Studio.
3.  Dans le menu **générer** , sélectionnez **générer la solution**.

## <a name="running-the-sample"></a>Exécution de l'exemple

1.  Accédez au répertoire qui contient le nouveau fichier exécutable à l’aide de l’invite de commandes ou de l’Explorateur Windows.
2.  Sur la ligne de commande, entrez `DropTargetVerb.exe` . Vous pouvez également, à partir de l’Explorateur Windows, double-cliquer sur l’icône de DropTargetVerb.exe.
3.  Suivez les instructions de la boîte de dialogue qui s’affiche

 

 
