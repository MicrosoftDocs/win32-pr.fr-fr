---
description: Montre comment écrire un gestionnaire utilisé pour afficher un aperçu de fichier dans le volet de visualisation de l’Explorateur Windows ou d’autres hôtes du gestionnaire d’aperçus.
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
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104973495"
---
# <a name="recipe-preview-handler-sample"></a><span data-ttu-id="dfb1d-103">Gestionnaire de préversion de recette, exemple</span><span class="sxs-lookup"><span data-stu-id="dfb1d-103">Recipe Preview Handler Sample</span></span>

<span data-ttu-id="dfb1d-104">Montre comment écrire un gestionnaire utilisé pour afficher un aperçu de fichier dans le volet de visualisation de l’Explorateur Windows ou d’autres hôtes du gestionnaire d’aperçus.</span><span class="sxs-lookup"><span data-stu-id="dfb1d-104">Demonstrates how to write a handler used to display a file preview inside the Windows Explorer preview pane or other preview handler hosts.</span></span>

<span data-ttu-id="dfb1d-105">Cette rubrique contient les sections suivantes :</span><span class="sxs-lookup"><span data-stu-id="dfb1d-105">This topic contains the following sections:</span></span>

-   [<span data-ttu-id="dfb1d-106">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="dfb1d-106">Requirements</span></span>](#requirements)
-   [<span data-ttu-id="dfb1d-107">Téléchargement de l’exemple</span><span class="sxs-lookup"><span data-stu-id="dfb1d-107">Downloading the Sample</span></span>](#downloading-the-sample)
-   [<span data-ttu-id="dfb1d-108">Génération de l'exemple</span><span class="sxs-lookup"><span data-stu-id="dfb1d-108">Building the Sample</span></span>](#building-the-sample)
-   [<span data-ttu-id="dfb1d-109">Exécution de l’exemple</span><span class="sxs-lookup"><span data-stu-id="dfb1d-109">Running the Sample</span></span>](#running-the-sample)
-   [<span data-ttu-id="dfb1d-110">Annulation de l’inscription de l’exemple de DLL du gestionnaire d’aperçus</span><span class="sxs-lookup"><span data-stu-id="dfb1d-110">Unregistering the Sample Preview Handler DLL</span></span>](#unregistering-the-sample-preview-handler-dll)
-   [<span data-ttu-id="dfb1d-111">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="dfb1d-111">Related topics</span></span>](#related-topics)

## <a name="requirements"></a><span data-ttu-id="dfb1d-112">Spécifications</span><span class="sxs-lookup"><span data-stu-id="dfb1d-112">Requirements</span></span>



| <span data-ttu-id="dfb1d-113">Produit</span><span class="sxs-lookup"><span data-stu-id="dfb1d-113">Product</span></span>                                | <span data-ttu-id="dfb1d-114">Version minimale du produit</span><span class="sxs-lookup"><span data-stu-id="dfb1d-114">Minimum Product Version</span></span> |
|----------------------------------------|-------------------------|
| <span data-ttu-id="dfb1d-115">Windows</span><span class="sxs-lookup"><span data-stu-id="dfb1d-115">Windows</span></span>                                | <span data-ttu-id="dfb1d-116">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="dfb1d-116">Windows Vista</span></span>           |
| <span data-ttu-id="dfb1d-117">Kit de développement logiciel Windows</span><span class="sxs-lookup"><span data-stu-id="dfb1d-117">Windows Software Development Kit (SDK)</span></span> | <span data-ttu-id="dfb1d-118">7.0</span><span class="sxs-lookup"><span data-stu-id="dfb1d-118">7.0</span></span>                     |



 

## <a name="downloading-the-sample"></a><span data-ttu-id="dfb1d-119">Téléchargement de l’exemple</span><span class="sxs-lookup"><span data-stu-id="dfb1d-119">Downloading the Sample</span></span>

| <span data-ttu-id="dfb1d-120">Emplacement</span><span class="sxs-lookup"><span data-stu-id="dfb1d-120">Location</span></span>      | <span data-ttu-id="dfb1d-121">URL du chemin</span><span class="sxs-lookup"><span data-stu-id="dfb1d-121">Path URL</span></span>                                                                                             |
|---------------|------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="dfb1d-122">GitHub</span><span class="sxs-lookup"><span data-stu-id="dfb1d-122">GitHub</span></span>  | [<span data-ttu-id="dfb1d-123">Exemple RecipePreviewHandler</span><span class="sxs-lookup"><span data-stu-id="dfb1d-123">RecipePreviewHandler sample</span></span>](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/winui/shell/appshellintegration/RecipePreviewHandler) |

## <a name="building-the-sample"></a><span data-ttu-id="dfb1d-124">Génération de l'exemple</span><span class="sxs-lookup"><span data-stu-id="dfb1d-124">Building the Sample</span></span>

<span data-ttu-id="dfb1d-125">Pour générer l’exemple à partir de l’invite de commandes :</span><span class="sxs-lookup"><span data-stu-id="dfb1d-125">To build the sample from the command prompt:</span></span>

1.  <span data-ttu-id="dfb1d-126">Ouvrez la fenêtre d’invite de commandes et accédez au répertoire du projet **RecipePreviewHandler** .</span><span class="sxs-lookup"><span data-stu-id="dfb1d-126">Open the command prompt window and navigate to the **RecipePreviewHandler** project directory.</span></span> <span data-ttu-id="dfb1d-127">Par exemple : `C:\Program Files\MicrosoftSDKs\Windows\v7.0\Samples\WinUI\Shell\AppShellIntegration\RecipePreviewHandler`.</span><span class="sxs-lookup"><span data-stu-id="dfb1d-127">For example, `C:\Program Files\MicrosoftSDKs\Windows\v7.0\Samples\WinUI\Shell\AppShellIntegration\RecipePreviewHandler`.</span></span>
2.  <span data-ttu-id="dfb1d-128">Entrez `msbuild PreviewHandlerSDKSample.sln`.</span><span class="sxs-lookup"><span data-stu-id="dfb1d-128">Enter `msbuild PreviewHandlerSDKSample.sln`.</span></span>

<span data-ttu-id="dfb1d-129">Pour générer l’exemple à l’aide de Microsoft Visual Studio (par défaut) :</span><span class="sxs-lookup"><span data-stu-id="dfb1d-129">To build the sample using Microsoft Visual Studio (preferred):</span></span>

1.  <span data-ttu-id="dfb1d-130">Ouvrez l’Explorateur Windows et accédez au répertoire du projet **RecipePreviewHandler** .</span><span class="sxs-lookup"><span data-stu-id="dfb1d-130">Open Windows Explorer and navigate to the **RecipePreviewHandler** project directory.</span></span>
2.  <span data-ttu-id="dfb1d-131">Double-cliquez sur l’icône du fichier PreviewHandlerSDKSample. sln pour ouvrir le projet dans Visual Studio.</span><span class="sxs-lookup"><span data-stu-id="dfb1d-131">Double-click the icon for the PreviewHandlerSDKSample.sln file to open the project in Visual Studio.</span></span>
    > [!Note]  
    > <span data-ttu-id="dfb1d-132">L’extension de nom de fichier. sln n’est pas affichée sous paramètres de dossier par défaut.</span><span class="sxs-lookup"><span data-stu-id="dfb1d-132">The .sln file name extension is not shown under default folder settings.</span></span> <span data-ttu-id="dfb1d-133">Dans ce cas, il peut être identifié par son icône unique ou par sa description de type « Microsoft Visual Studio solution ».</span><span class="sxs-lookup"><span data-stu-id="dfb1d-133">In that situation, it can be identified by its unique icon or by its type description "Microsoft Visual Studio Solution".</span></span>

     

3.  <span data-ttu-id="dfb1d-134">Dans le menu **générer** , sélectionnez **générer la solution**.</span><span class="sxs-lookup"><span data-stu-id="dfb1d-134">From the **Build** menu, select **Build Solution**.</span></span>

> [!Note]  
> <span data-ttu-id="dfb1d-135">Si le système cible est 64 bits (x64), cet exemple de gestionnaire d’aperçus doit être généré sous la forme d’une application 64 bits.</span><span class="sxs-lookup"><span data-stu-id="dfb1d-135">If the target system is 64-bit (x64), this sample preview handler must be built as a 64-bit application.</span></span>

 

## <a name="running-the-sample"></a><span data-ttu-id="dfb1d-136">Exécution de l'exemple</span><span class="sxs-lookup"><span data-stu-id="dfb1d-136">Running the Sample</span></span>

1.  <span data-ttu-id="dfb1d-137">Ouvrez la fenêtre d’invite de commandes et accédez au répertoire du projet **RecipePreviewHandler** généré.</span><span class="sxs-lookup"><span data-stu-id="dfb1d-137">Open the command prompt window and navigate to the built **RecipePreviewHandler** project directory.</span></span> <span data-ttu-id="dfb1d-138">Par exemple : `C:\Program Files\MicrosoftSDKs\Windows\v7.0\Samples\WinUI\Shell\AppShellIntegration\RecipePreviewHandler\RecipePreviewHandler`.</span><span class="sxs-lookup"><span data-stu-id="dfb1d-138">For example, `C:\Program Files\MicrosoftSDKs\Windows\v7.0\Samples\WinUI\Shell\AppShellIntegration\RecipePreviewHandler\RecipePreviewHandler`.</span></span> <span data-ttu-id="dfb1d-139">Entrez `regsvr32.exe PreviewHandlerSDKSample.dll` pour inscrire le gestionnaire.</span><span class="sxs-lookup"><span data-stu-id="dfb1d-139">Enter `regsvr32.exe PreviewHandlerSDKSample.dll` to register the handler.</span></span>
2.  <span data-ttu-id="dfb1d-140">Ouvrez l’Explorateur Windows et affichez le volet de visualisation s’il n’est pas déjà affiché.</span><span class="sxs-lookup"><span data-stu-id="dfb1d-140">Open Windows Explorer and show the preview pane if it is not already displayed.</span></span>
    -   <span data-ttu-id="dfb1d-141">**Windows 7**: cliquez sur le bouton volet de visualisation.</span><span class="sxs-lookup"><span data-stu-id="dfb1d-141">**Windows 7**: Click the preview pane button.</span></span>
    -   <span data-ttu-id="dfb1d-142">**Windows Vista**: cliquez sur le menu **organiser** , accédez au sous-menu **disposition** et sélectionnez **volet de visualisation**.</span><span class="sxs-lookup"><span data-stu-id="dfb1d-142">**Windows Vista**: Click the **Organize** menu, go to the **Layout** submenu and select **Preview Pane**.</span></span>
3.  <span data-ttu-id="dfb1d-143">Utilisez l’Explorateur Windows pour accéder au répertoire du projet **RecipePreviewHandler** .</span><span class="sxs-lookup"><span data-stu-id="dfb1d-143">Use Windows Explorer to navigate to the **RecipePreviewHandler** project directory.</span></span>
4.  <span data-ttu-id="dfb1d-144">Sélectionnez le fichier example. recette.</span><span class="sxs-lookup"><span data-stu-id="dfb1d-144">Select the example .recipe file.</span></span>

<span data-ttu-id="dfb1d-145">Pour que la sortie 32 bits (x86) et 64 bits (x64) fonctionne sur une version 64 bits de Windows, définissez la valeur **AppID** sur l’hôte de substitution WOW64 `{534A1E02-D58F-44f0-B58B-36CBED287C7C}` , comme indiqué dans le code suivant.</span><span class="sxs-lookup"><span data-stu-id="dfb1d-145">To make both the 32-bit (x86) and 64-bit (x64) output work on a 64-bit version of Windows, set the **AppId** value to the WOW64 surrogate host `{534A1E02-D58F-44f0-B58B-36CBED287C7C}`, as shown in the following code.</span></span>


```
{HKEY_CURRENT_USER,   
 L"Software\\Classes\\CLSID\\" SZ_CLSID_RecipePreviewHandler,
 L"AppID",
 L"{534A1E02-D58F-44f0-B58B-36CBED287C7C}"}
```



## <a name="unregistering-the-sample-preview-handler-dll"></a><span data-ttu-id="dfb1d-146">Annulation de l’inscription de l’exemple de DLL du gestionnaire d’aperçus</span><span class="sxs-lookup"><span data-stu-id="dfb1d-146">Unregistering the Sample Preview Handler DLL</span></span>

-   <span data-ttu-id="dfb1d-147">Ouvrez la fenêtre d’invite de commandes et entrez `regsvr32.exe /u PreviewHandlerSDKSample.dll` pour annuler l’inscription du gestionnaire.</span><span class="sxs-lookup"><span data-stu-id="dfb1d-147">Open the command prompt window and enter `regsvr32.exe /u PreviewHandlerSDKSample.dll` to unregister the handler.</span></span>

## <a name="related-topics"></a><span data-ttu-id="dfb1d-148">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="dfb1d-148">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="dfb1d-149">**IPreviewHandler**</span><span class="sxs-lookup"><span data-stu-id="dfb1d-149">**IPreviewHandler**</span></span>](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ipreviewhandler)
</dt> <dt>

[<span data-ttu-id="dfb1d-150">**IPreviewHandlerFrame**</span><span class="sxs-lookup"><span data-stu-id="dfb1d-150">**IPreviewHandlerFrame**</span></span>](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ipreviewhandlerframe)
</dt> <dt>

[<span data-ttu-id="dfb1d-151">ID de modèle d’utilisateur d’application (AppUserModelIDs)</span><span class="sxs-lookup"><span data-stu-id="dfb1d-151">Application User Model IDs (AppUserModelIDs)</span></span>](appids.md)
</dt> </dl>

 

 
