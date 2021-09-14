---
description: montre comment écrire un gestionnaire utilisé pour afficher un aperçu de fichier dans le volet de visualisation de l’explorateur de Windows ou d’autres hôtes du gestionnaire d’aperçus.
title: Gestionnaire de préversion de recette, exemple
ms.topic: article
ms.date: 05/31/2018
ms.assetid: 2C926922-48C0-46f5-8928-67007C6FF957
api_name: ''
api_type: ''
api_location: ''
topic_type:
- kbArticle
ms.openlocfilehash: 05208010c90c7185a777bb75f5de1e67bdb5bc14
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127235188"
---
# <a name="recipe-preview-handler-sample"></a>Gestionnaire de préversion de recette, exemple

montre comment écrire un gestionnaire utilisé pour afficher un aperçu de fichier dans le volet de visualisation de l’explorateur de Windows ou d’autres hôtes du gestionnaire d’aperçus.

Cette rubrique contient les sections suivantes :

-   [Configuration requise](#requirements)
-   [Téléchargement de l’exemple](#downloading-the-sample)
-   [Génération de l'exemple](#building-the-sample)
-   [Exécution de l’exemple](#running-the-sample)
-   [Annulation de l’inscription de l’exemple de DLL du gestionnaire d’aperçus](#unregistering-the-sample-preview-handler-dll)
-   [Rubriques connexes](#related-topics)

## <a name="requirements"></a>Spécifications



| Produit                                | Version minimale du produit |
|----------------------------------------|-------------------------|
| Windows                                | Windows Vista           |
| Kit de développement logiciel Windows | 7.0                     |



 

## <a name="downloading-the-sample"></a>Téléchargement de l’exemple

| Emplacement      | URL du chemin                                                                                             |
|---------------|------------------------------------------------------------------------------------------------------|
| GitHub  | [Exemple RecipePreviewHandler](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/winui/shell/appshellintegration/RecipePreviewHandler) |

## <a name="building-the-sample"></a>Génération de l'exemple

Pour générer l’exemple à partir de l’invite de commandes :

1.  Ouvrez la fenêtre d’invite de commandes et accédez au répertoire du projet **RecipePreviewHandler** . Par exemple : `C:\Program Files\MicrosoftSDKs\Windows\v7.0\Samples\WinUI\Shell\AppShellIntegration\RecipePreviewHandler`.
2.  Entrez `msbuild PreviewHandlerSDKSample.sln`.

pour générer l’exemple à l’aide de Microsoft Visual Studio (par défaut) :

1.  ouvrez Windows Explorer et accédez au répertoire du projet **RecipePreviewHandler** .
2.  Double-cliquez sur l’icône du fichier PreviewHandlerSDKSample. sln pour ouvrir le projet dans Visual Studio.
    > [!Note]  
    > L’extension de nom de fichier. sln n’est pas affichée sous paramètres de dossier par défaut. dans ce cas, il peut être identifié par son icône unique ou par sa description de type « Microsoft Visual Studio Solution ».

     

3.  Dans le menu **Générer**, sélectionnez **Générer la solution**.

> [!Note]  
> Si le système cible est 64 bits (x64), cet exemple de gestionnaire d’aperçus doit être généré sous la forme d’une application 64 bits.

 

## <a name="running-the-sample"></a>Exécution de l'exemple

1.  Ouvrez la fenêtre d’invite de commandes et accédez au répertoire du projet **RecipePreviewHandler** généré. Par exemple : `C:\Program Files\MicrosoftSDKs\Windows\v7.0\Samples\WinUI\Shell\AppShellIntegration\RecipePreviewHandler\RecipePreviewHandler`. Entrez `regsvr32.exe PreviewHandlerSDKSample.dll` pour inscrire le gestionnaire.
2.  ouvrez Windows Explorer et affichez le volet de visualisation s’il n’est pas déjà affiché.
    -   **Windows 7**: cliquez sur le bouton volet de visualisation.
    -   **Windows Vista**: cliquez sur le menu **organiser** , accédez au sous-menu **disposition** et sélectionnez **volet de visualisation**.
3.  utilisez Windows Explorer pour accéder au répertoire du projet **RecipePreviewHandler** .
4.  Sélectionnez le fichier example. recette.

pour que la sortie 32 bits (x86) et 64 bits (x64) fonctionne sur une version 64 bits de Windows, définissez la valeur **AppId** sur l’hôte de substitution WOW64 `{534A1E02-D58F-44f0-B58B-36CBED287C7C}` , comme indiqué dans le code suivant.


```
{HKEY_CURRENT_USER,   
 L"Software\\Classes\\CLSID\\" SZ_CLSID_RecipePreviewHandler,
 L"AppID",
 L"{534A1E02-D58F-44f0-B58B-36CBED287C7C}"}
```



## <a name="unregistering-the-sample-preview-handler-dll"></a>Annulation de l’inscription de l’exemple de DLL du gestionnaire d’aperçus

-   Ouvrez la fenêtre d’invite de commandes et entrez `regsvr32.exe /u PreviewHandlerSDKSample.dll` pour annuler l’inscription du gestionnaire.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[**IPreviewHandler**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ipreviewhandler)
</dt> <dt>

[**IPreviewHandlerFrame**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ipreviewhandlerframe)
</dt> <dt>

[ID de modèle d’utilisateur d’application (AppUserModelIDs)](appids.md)
</dt> </dl>

 

 
