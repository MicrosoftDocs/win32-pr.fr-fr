---
description: Montre comment utiliser les méthodes de l’interface IFileOperationProgressSink pour analyser les détails des actions de l’interface IFileOperation.
title: Récepteur de progression d’opération sur les fichiers
ms.topic: article
ms.date: 05/31/2018
ms.assetid: 196ABB75-1FE0-44f5-9060-59AAB4231567
api_name: ''
api_type: ''
api_location: ''
topic_type:
- kbArticle
ms.openlocfilehash: 60e3bde90da36a6122608b463b28df670f0d2a8e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104034677"
---
# <a name="file-operation-progress-sink"></a>Récepteur de progression d’opération sur les fichiers

Montre comment utiliser les méthodes de l’interface [**IFileOperationProgressSink**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ifileoperationprogresssink) pour analyser les détails des actions de l’interface [**IFileOperation**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ifileoperation) .

Cette rubrique contient les sections suivantes.

-   [Configuration requise](#requirements)
-   [Téléchargement de l’exemple](#downloading-the-sample)
-   [Génération de l'exemple](#building-the-sample)
-   [Exécution de l’exemple](#running-the-sample)

## <a name="requirements"></a>Spécifications



| Produit                                | Version minimale du produit |
|----------------------------------------|-------------------------|
| Windows                                | Windows Vista           |
| Kit de développement logiciel Windows | 6.1                     |



 

## <a name="downloading-the-sample"></a>Téléchargement de l’exemple

| Emplacement      | URL du chemin                                                                                             |
|---------------|------------------------------------------------------------------------------------------------------|
| GitHub  | [Exemple FileOperationProgressSink](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/winui/shell/appplatform/FileOperationProgressSink) |

## <a name="building-the-sample"></a>Génération de l'exemple

Pour générer l’exemple à partir de la fenêtre d’invite de commandes :

1.  Ouvrez la fenêtre d’invite de commandes et accédez au répertoire du projet **FileOperationProgressSink** .
2.  Entrez `msbuild FileOperationProgressSinkSample.sln`.

Pour générer l’exemple à l’aide de Microsoft Visual Studio (par défaut) :

1.  Ouvrez l’Explorateur Windows et accédez au répertoire du projet **FilesInUse** . Par exemple, le chemin d’installation complet par défaut est `C:\Program Files\Microsoft SDKs\Windows\v7.0\Samples\WinUI\Shell\AppPlatform\FileOperationProgressSinkSample` .
2.  Double-cliquez sur l’icône du fichier FileOperationProgressSinkSample. sln pour ouvrir le projet dans Visual Studio.
    > [!Note]  
    > L’extension de nom de fichier. sln n’est pas affichée sous paramètres de dossier par défaut. Dans ce cas, il peut être identifié par son icône unique ou par sa description de type, « Microsoft Visual Studio solution ».

     

3.  Dans le menu **générer** , sélectionnez **générer la solution**.

## <a name="running-the-sample"></a>Exécution de l'exemple

1.  Accédez au répertoire qui contient le nouveau fichier exécutable à l’aide de la fenêtre d’invite de commandes ou de l’Explorateur Windows.
2.  À l’invite de commandes, entrez `FileOperationProgressSinkSample.exe` , ou à partir de l’Explorateur Windows, double-cliquez sur l’icône de FileOperationProgressSinkSample.exe.

 

 



