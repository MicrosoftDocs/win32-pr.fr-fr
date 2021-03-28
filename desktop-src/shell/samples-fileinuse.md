---
description: Montre comment personnaliser le fichier dans la boîte de dialogue d’utilisation de pour afficher des informations et des options supplémentaires pour les fichiers qui sont actuellement ouverts dans l’application.
title: Fichier en cours d’utilisation, exemple
ms.topic: article
ms.date: 05/31/2018
ms.assetid: 22EFE7CC-D223-46b3-BD6B-293E3FA0BA01
api_name: ''
api_type: ''
api_location: ''
topic_type:
- kbArticle
ms.openlocfilehash: 223e0addf201f3526654a17346963b4639e0d215
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104319346"
---
# <a name="file-is-in-use-sample"></a>Fichier en cours d’utilisation, exemple

Montre comment personnaliser le **fichier dans** la boîte de dialogue d’utilisation de pour afficher des informations et des options supplémentaires pour les fichiers qui sont actuellement ouverts dans l’application.

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



 

Pour obtenir des spécifications supplémentaires, consultez le \_ fichier IFileIsInUsesample.docx inclus avec l’exemple.

## <a name="downloading-the-sample"></a>Téléchargement de l’exemple

| Emplacement      | URL du chemin                                                                                             |
|---------------|------------------------------------------------------------------------------------------------------|
| GitHub  | [Exemple FileIsInUse](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/winui/shell/appplatform/fileisinuse) |

## <a name="building-the-sample"></a>Génération de l'exemple

Pour générer l’exemple à partir de la fenêtre d’invite de commandes :

1.  Ouvrez la fenêtre d’invite de commandes et accédez au répertoire du projet **FileIsInUse** .
2.  Entrez `msbuild FileIsInUse.sln`.

Pour générer l’exemple à l’aide de Microsoft Visual Studio (par défaut) :

1.  Ouvrez l’Explorateur Windows et accédez au répertoire du projet **FilesInUse** . Par exemple, le chemin d’installation complet par défaut est `C:\Program Files\Microsoft SDKs\Windows\v7.0\Samples\WinUI\Shell\AppPlatform\FileIsInUse` .
2.  Double-cliquez sur l’icône du fichier FileIsInUseSample. sln pour ouvrir le projet dans Visual Studio.
    > [!Note]  
    > L’extension de nom de fichier. sln n’est pas affichée sous paramètres de dossier par défaut. Dans ce cas, il peut être identifié par son icône unique ou par sa description de type, « Microsoft Visual Studio solution ».

     

3.  Dans le menu **générer** , sélectionnez **générer la solution**.

## <a name="running-the-sample"></a>Exécution de l'exemple

1.  Accédez au répertoire qui contient le nouveau fichier exécutable à l’aide de la fenêtre d’invite de commandes ou de l’Explorateur Windows.
2.  À l’invite de commandes, entrez `FileIsInUseSample.exe` , ou à partir de l’Explorateur Windows, double-cliquez sur l’icône de FileIsInUseSample.exe.

Pour plus d’informations sur cet exemple de code, consultez le \_ fichier IFileIsInUsesample.docx inclus dans l’exemple.

 

 



