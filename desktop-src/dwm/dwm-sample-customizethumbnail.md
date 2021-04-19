---
title: Personnaliser une miniature d’icône et une image bitmap Live Preview
description: Montre comment personnaliser une miniature sous forme et une image bitmap en mode aperçu instantané (également appelée aperçu de lecture).
ms.assetid: 43fe71e7-4e5c-46fb-876b-e26996071665
ms.topic: article
ms.date: 05/31/2018
ms.custom: project-verbatim
ms.openlocfilehash: 8fceb94727257b51a2e6235cbfcc44b155635343
ms.sourcegitcommit: af120ad5c30da2fc5eb717ca2a1c4c45878efd71
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/20/2021
ms.locfileid: "106538072"
---
# <a name="customize-an-iconic-thumbnail-and-a-live-preview-bitmap"></a><span data-ttu-id="e7dd7-103">Personnaliser une miniature d’icône et une image bitmap Live Preview</span><span class="sxs-lookup"><span data-stu-id="e7dd7-103">Customize an Iconic Thumbnail and a Live Preview Bitmap</span></span>

## <a name="description"></a><span data-ttu-id="e7dd7-104">Description</span><span class="sxs-lookup"><span data-stu-id="e7dd7-104">Description</span></span>

<span data-ttu-id="e7dd7-105">Vous pouvez personnaliser une image bitmap sous forme et une image de l' *aperçu instantané* (ou aperçu de l' *Aperçu*) en utilisant des fonctions et des messages introduits dans les API Windows 7 gestionnaire de fenêtrage (DWM).</span><span class="sxs-lookup"><span data-stu-id="e7dd7-105">You can customize an iconic thumbnail and a *live preview* (or *Peek preview*) bitmap by using functions and messages that are introduced in the Windows 7 Desktop Window Manager (DWM) APIs.</span></span>

<span data-ttu-id="e7dd7-106">Plus précisément, vous utilisez la fonction [**DwmSetIconicThumbnail**](/windows/win32/api/Dwmapi/nf-dwmapi-dwmseticonicthumbnail) et le message [**WM \_ SENDICONICTHUMBNAILBITMAP**](wm-dwmsendiconicthumbnail.md) pour personnaliser une miniature de sous forme.</span><span class="sxs-lookup"><span data-stu-id="e7dd7-106">Specifically, you use the [**DwmSetIconicThumbnail**](/windows/win32/api/Dwmapi/nf-dwmapi-dwmseticonicthumbnail) function and the [**WM\_SENDICONICTHUMBNAILBITMAP**](wm-dwmsendiconicthumbnail.md) message to customize an iconic thumbnail.</span></span> <span data-ttu-id="e7dd7-107">Vous pouvez également utiliser la fonction [**DwmSetIconicLivePreviewBitmap**](/windows/win32/api/Dwmapi/nf-dwmapi-dwmseticoniclivepreviewbitmap) et le message [**WM \_ SENDICONICLIVEPREVIEWBITMAP**](wm-dwmsendiconiclivepreviewbitmap.md) pour définir une image bitmap de l’aperçu instantané de sous forme.</span><span class="sxs-lookup"><span data-stu-id="e7dd7-107">You can also use the [**DwmSetIconicLivePreviewBitmap**](/windows/win32/api/Dwmapi/nf-dwmapi-dwmseticoniclivepreviewbitmap) function and the [**WM\_SENDICONICLIVEPREVIEWBITMAP**](wm-dwmsendiconiclivepreviewbitmap.md) message to set an iconic live preview bitmap.</span></span>

<span data-ttu-id="e7dd7-108">Pour obtenir un exemple d’application qui utilise la fonction **DwmSetIconicThumbnail** , consultez [exemple TabThumbnails](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/winui/shell/appshellintegration/TabThumbnails).</span><span class="sxs-lookup"><span data-stu-id="e7dd7-108">For a sample application that uses the **DwmSetIconicThumbnail** function, see [TabThumbnails sample](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/winui/shell/appshellintegration/TabThumbnails).</span></span>

<span data-ttu-id="e7dd7-109">L’illustration suivante montre une miniature par défaut transformée en miniature personnalisée.</span><span class="sxs-lookup"><span data-stu-id="e7dd7-109">The following illustration shows a default thumbnail transformed into a customized thumbnail.</span></span>

![illustration d’une image miniature d’origine et d’une image miniature modifiée avec une bitmap personnalisée](images/customthumbnail.jpg)

## <a name="requirements"></a><span data-ttu-id="e7dd7-111">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="e7dd7-111">Requirements</span></span>

| <span data-ttu-id="e7dd7-112">Condition requise</span><span class="sxs-lookup"><span data-stu-id="e7dd7-112">Requirement</span></span> | <span data-ttu-id="e7dd7-113">Valeur</span><span class="sxs-lookup"><span data-stu-id="e7dd7-113">Value</span></span> |
|--------------------------|---------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e7dd7-114">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="e7dd7-114">Minimum supported client</span></span> | <span data-ttu-id="e7dd7-115">Windows 7 ou Windows Vista avec Service Pack 2 (SP2) et mise à jour de la plateforme pour Windows Vista</span><span class="sxs-lookup"><span data-stu-id="e7dd7-115">Windows 7 or Windows Vista with Service Pack 2 (SP2) and Platform Update for Windows Vista</span></span>                          |
| <span data-ttu-id="e7dd7-116">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="e7dd7-116">Minimum supported server</span></span> | <span data-ttu-id="e7dd7-117">Windows Server 2008 R2 ou Windows Server 2008 avec Service Pack 2 (SP2) et mise à jour de plateforme pour Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="e7dd7-117">Windows Server 2008 R2 or Windows Server 2008 with Service Pack 2 (SP2) and Platform Update for Windows Server 2008</span></span> |
| <span data-ttu-id="e7dd7-118">SDK Windows minimal</span><span class="sxs-lookup"><span data-stu-id="e7dd7-118">Minimum Windows SDK</span></span>      | [<span data-ttu-id="e7dd7-119">Kit de développement logiciel (SDK) Windows pour Windows 7</span><span class="sxs-lookup"><span data-stu-id="e7dd7-119">Windows Software Development Kit (SDK) for Windows 7</span></span>](https://msdn.microsoft.com/windows/bb980924.aspx)             |

## <a name="building-the-tabthumbnails-sample"></a><span data-ttu-id="e7dd7-120">Génération de l’exemple TabThumbnails</span><span class="sxs-lookup"><span data-stu-id="e7dd7-120">Building the TabThumbnails sample</span></span>

<span data-ttu-id="e7dd7-121">**Pour générer l’exemple à l’aide de Microsoft Visual Studio (méthode recommandée)**</span><span class="sxs-lookup"><span data-stu-id="e7dd7-121">**To build the sample by using Microsoft Visual Studio (preferred method)**</span></span>

1.  <span data-ttu-id="e7dd7-122">Ouvrez l’Explorateur Windows et accédez au dossier où se trouve le fichier TabThumbnails. sln.</span><span class="sxs-lookup"><span data-stu-id="e7dd7-122">Open Windows Explorer and browse to the folder where the TabThumbnails.sln file is located.</span></span>
2.  <span data-ttu-id="e7dd7-123">Double-cliquez sur le fichier solution (. sln) pour ouvrir le fichier dans Microsoft Visual Studio.</span><span class="sxs-lookup"><span data-stu-id="e7dd7-123">Double-click the solution file (.sln) to open the file in Microsoft Visual Studio.</span></span>
3.  <span data-ttu-id="e7dd7-124">Dans le menu **Générer**, cliquez sur **Générer la solution**.</span><span class="sxs-lookup"><span data-stu-id="e7dd7-124">On the **Build** menu, click **Build Solution**.</span></span> <span data-ttu-id="e7dd7-125">L’application est générée dans le \\ Répertoire de débogage ou de version par défaut \\ .</span><span class="sxs-lookup"><span data-stu-id="e7dd7-125">The application is built in the default \\Debug or \\Release directory.</span></span>

<span data-ttu-id="e7dd7-126">**Pour générer l’exemple à l’aide de l’invite de commandes**</span><span class="sxs-lookup"><span data-stu-id="e7dd7-126">**To build the sample by using the command prompt**</span></span>

1.  <span data-ttu-id="e7dd7-127">Ouvrez une fenêtre d’invite de commandes et accédez au répertoire de l’exemple.</span><span class="sxs-lookup"><span data-stu-id="e7dd7-127">Open a Command Prompt window and browse to the sample directory.</span></span>
2.  <span data-ttu-id="e7dd7-128">Entrez `msbuild TabThumbnails.sln`.</span><span class="sxs-lookup"><span data-stu-id="e7dd7-128">Enter `msbuild TabThumbnails.sln`.</span></span>

## <a name="related-topics"></a><span data-ttu-id="e7dd7-129">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="e7dd7-129">Related topics</span></span>

[<span data-ttu-id="e7dd7-130">Gestionnaire de fenêtres du Bureau</span><span class="sxs-lookup"><span data-stu-id="e7dd7-130">Desktop Window Manager</span></span>](dwm-overview.md)

[<span data-ttu-id="e7dd7-131">Développement Windows</span><span class="sxs-lookup"><span data-stu-id="e7dd7-131">Windows Development</span></span>](/windows/desktop/win32-and-com-development)
