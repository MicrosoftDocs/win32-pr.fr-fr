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
ms.openlocfilehash: 223f498f42e33dda09206b1e21a44138fda54e261ec957efb62e55148a014d6e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117677836"
---
# <a name="explorer-data-provider-sample"></a>Fournisseur de données de l’Explorateur, exemple

Montre comment implémenter une extension d’espace de noms Shell, y compris le comportement de menu contextuel et des tâches personnalisées dans le navigateur.

Cette rubrique contient les sections suivantes.

-   [Requirements](#requirements)
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
> <span codelanguage=""></span>
>
> <table>
> <colgroup>
> <col style="width: 100%" />
> </colgroup>
> <tbody>
> <tr class="odd">
> <td><pre><code>LinkIncremental=&quot;1&quot;
> AdditionalLibraryDirectories=&quot;&quot;c:\Program Files\Microsoft SDKs\Windows\v6.0\Lib\x64&quot;&quot;
> ModuleDefinitionFile=&quot;ExplorerDataProvider.def&quot;
> GenerateDebugInformation=&quot;true&quot;</code></pre></td>
> </tr>
> </tbody>
> </table> 
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


