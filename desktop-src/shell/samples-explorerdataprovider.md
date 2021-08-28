---
description: Montre comment implémenter une extension d’espace de noms Shell, y compris le comportement de menu contextuel et des tâches personnalisées dans le navigateur.
title: Fournisseur de données de l’Explorateur, exemple
ms.topic: article
ms.date: 05/31/2018
ms.assetid: B1B20AF8-3DDE-467b-A49E-A77849CF9F1B
api_name: ''
api_type: ''
api_location: ''
topic_type:
- kbArticle
ms.openlocfilehash: b30a1c6cb31038d69c9feb85f0382fd5f4bb89bf
ms.sourcegitcommit: 4e94fc75fad7b2a0f3c92a26f97e89924e59b7a9
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/24/2021
ms.locfileid: "122786705"
---
# <a name="explorer-data-provider-sample"></a>Fournisseur de données de l’Explorateur, exemple

Montre comment implémenter une extension d’espace de noms Shell, y compris le comportement de menu contextuel et des tâches personnalisées dans le navigateur.

Cette rubrique contient les sections suivantes.

-   [Configuration requise](#requirements)
-   [Téléchargement de l’exemple](#downloading-the-sample)
-   [Génération de l'exemple](#building-the-sample)
-   [Exécution de l’exemple](#running-the-sample)

## <a name="requirements"></a>Configuration requise



| Produit                                | Version minimale du produit |
|----------------------------------------|-------------------------|
| Windows                                | Windows Vista           |
| Kit de développement logiciel Windows | 6.1                     |



 

## <a name="downloading-the-sample"></a>Téléchargement de l’exemple

| Emplacement      | URL du chemin                                                                                             |
|---------------|------------------------------------------------------------------------------------------------------|
| GitHub  | [Exemple ExplorerDataProvider](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/winui/shell/shellextensibility/explorerdataprovider) |

## <a name="building-the-sample"></a>Génération de l'exemple

Pour générer l’exemple à partir de l’invite de commandes :

1.  Ouvrez la fenêtre d’invite de commandes et accédez au répertoire du projet **ExplorerDataProvider** .
2.  Entrez `msbuild ExplorerDataProvider.sln`.

pour générer l’exemple à l’aide de Microsoft Visual Studio (par défaut) :

1.  ouvrez Windows Explorer et accédez au répertoire du projet **ExplorerDataProvider** .
2.  Double-cliquez sur l’icône du fichier ExplorerDataProvider. sln pour ouvrir le projet dans Visual Studio.
3.  Dans le menu **Générer**, sélectionnez **Générer la solution**. La DLL sera générée dans le répertoire de \\ débogage ou de version par défaut \\ .

> [!Note]  
> dans la version de cet exemple incluse dans le SDK Windows, la configuration de la version 64 bits n’inclut pas le fichier ExplorerDataProvider. def dans l’option de **fichier de définition de Module** de l’éditeur de liens. Vous devez spécifier ce fichier vous-même avant de générer dans un environnement 64 bits. Ajoutez la ligne `ModuleDefinitionFile="ExplorerDataProvider.def"` à la section VCLinkerTool (commence à la ligne 329) du fichier ExplorerDataProvider. vcproj comme indiqué ici :
>
> 
>
> 
| | | <pre><code>LinkIncremental="1"&gt; AdditionalLibraryDirectories=""c:\Program Files\Microsoft SDKs\Windows\v6.0\Lib\x64""&gt; ModuleDefinitionFile="ExplorerDataProvider.def"&gt; GenerateDebugInformation="true"</code></pre> | 

>
> 
>
> La version de cet exemple téléchargeable à partir de la Galerie de code a été corrigée pour ce problème et aucune action supplémentaire n’est requise de votre part.
>
>  
>
> ## <a name="running-the-sample"></a>Exécution de l'exemple
>
> 1.  accédez au répertoire qui contient les nouveaux .dll et le fichier. propdesc à l’aide de l’invite de commandes ou de l’explorateur de Windows.
> 2.  Sur la ligne de commande, tapez `regsvr32.exe` .
>     > [!Note]  
>     > Si vous exécutez cette commande à partir d’une invite de commandes avec élévation de privilèges, l’inscription automatique inscrira également le fichier. propDesc automatiquement. S’il est exécuté à partir d’une invite de commandes non élevée, l’extension de l’espace de noms fonctionne, mais sans fonctionnalité de propriété personnalisée.
>
>      
>
> 3.  Ouvrez le dossier **poste de travail** et parcourez l’extension de l’espace de noms qui s’y trouve.
>
>  
>
>  
>


