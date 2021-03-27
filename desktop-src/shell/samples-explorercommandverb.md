---
description: Montre comment implémenter un verbe d’interpréteur de commandes à l’aide des méthodes ExplorerCommand et ExplorerCommandState.
title: ExplorerCommand, exemple de verbe
ms.topic: article
ms.date: 05/31/2018
ms.assetid: 2310A6AA-EAF9-4d7a-A784-04931BDC2089
api_name: ''
api_type: ''
api_location: ''
topic_type:
- kbArticle
ms.openlocfilehash: a35662c3df0e0fcddae049ccfaac2d9e3e265ee3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103868305"
---
# <a name="explorer-command-verb-sample"></a>ExplorerCommand, exemple de verbe

Montre comment implémenter un verbe d’interpréteur de commandes à l’aide des méthodes ExplorerCommand et ExplorerCommandState.

Cette rubrique contient les sections suivantes.

-   [Configuration requise](#requirements)
-   [Téléchargement de l’exemple](#downloading-the-sample)
-   [Génération de l'exemple](#building-the-sample)
-   [Exécution de l’exemple](#running-the-sample)

## <a name="requirements"></a>Spécifications



| Produit                                | Version minimale du produit |
|----------------------------------------|-------------------------|
| Windows                                | Windows Vista           |
| Kit de développement logiciel Windows | 7.0                     |



 

## <a name="downloading-the-sample"></a>Téléchargement de l’exemple

| Emplacement      | URL du chemin                                                                                             |
|---------------|------------------------------------------------------------------------------------------------------|
| GitHub  | [Exemple ExplorerCommandVerb](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/winui/shell/appshellintegration/ExplorerCommandVerb) |

## <a name="building-the-sample"></a>Génération de l'exemple

Pour générer l’exemple à partir de l’invite de commandes :

1.  Ouvrez la fenêtre d’invite de commandes et accédez au répertoire du projet **ExplorerCommandVerb** .
2.  Entrez `msbuild ExplorerCommandVerb.sln`.

Pour générer l’exemple à l’aide de Microsoft Visual Studio (par défaut) :

1.  Ouvrez l’Explorateur Windows et accédez au répertoire du projet **ExplorerCommandVerb** .
2.  Double-cliquez sur l’icône du fichier ExplorerCommandVerb. sln pour ouvrir le projet dans Visual Studio.
3.  Dans le menu **générer** , sélectionnez **générer la solution**.

## <a name="running-the-sample"></a>Exécution de l'exemple

1.  Accédez au répertoire qui contient le ExplorerCommandVerb.dll à l’aide de l’invite de commandes ou de l’Explorateur Windows. Veillez à utiliser le fichier DLL 64 bits sur Windows 64 bits.
2.  Sur la ligne de commande, entrez `regsvr32.exe ExplorerCommandVerb.dll` .
3.  Deux nouveaux verbes s’affichent dans le menu contextuel lorsque vous cliquez avec le bouton droit sur un fichier. txt.

 

 



