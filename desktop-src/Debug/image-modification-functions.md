---
description: Les fonctions de modification d’image vous permettent de modifier l’image exécutable.
ms.assetid: 195959cb-e1ab-4c76-b7f9-f20522feac8c
title: Fonctions de modification d’image ImageHlp
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 06f6be83457738d1237865940463f438d3b73afa
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103747893"
---
# <a name="imagehlp-image-modification-functions"></a><span data-ttu-id="5bc52-103">Fonctions de modification d’image ImageHlp</span><span class="sxs-lookup"><span data-stu-id="5bc52-103">ImageHlp Image Modification Functions</span></span>

<span data-ttu-id="5bc52-104">Les fonctions de modification d’image vous permettent de modifier l’image exécutable.</span><span class="sxs-lookup"><span data-stu-id="5bc52-104">The image modification functions allow you to change the executable image.</span></span> <span data-ttu-id="5bc52-105">Ils sont principalement utilisés par les outils de développement et les programmes d’installation.</span><span class="sxs-lookup"><span data-stu-id="5bc52-105">They are mostly for use by development tools and install programs.</span></span> <span data-ttu-id="5bc52-106">Ils peuvent être utilisés pour lier une image, calculer sa somme de contrôle (ce qui est important pour garantir l’intégrité de l’image), modifier son adresse de chargement et produire des fichiers de symboles.</span><span class="sxs-lookup"><span data-stu-id="5bc52-106">They can be used to bind an image, compute its checksum (which is important for ensuring image integrity), change its load address, and produce symbol files.</span></span>

<span data-ttu-id="5bc52-107">Les fonctions de modification d’image sont les suivantes.</span><span class="sxs-lookup"><span data-stu-id="5bc52-107">The following are the image modification functions.</span></span>

-   [<span data-ttu-id="5bc52-108">**BindImage**</span><span class="sxs-lookup"><span data-stu-id="5bc52-108">**BindImage**</span></span>](/windows/desktop/api/Imagehlp/nf-imagehlp-bindimage)
-   [<span data-ttu-id="5bc52-109">**BindImageEx**</span><span class="sxs-lookup"><span data-stu-id="5bc52-109">**BindImageEx**</span></span>](/windows/desktop/api/Imagehlp/nf-imagehlp-bindimageex)
-   [<span data-ttu-id="5bc52-110">**CheckSumMappedFile**</span><span class="sxs-lookup"><span data-stu-id="5bc52-110">**CheckSumMappedFile**</span></span>](/windows/desktop/api/Imagehlp/nf-imagehlp-checksummappedfile)
-   [<span data-ttu-id="5bc52-111">**MapFileAndCheckSum**</span><span class="sxs-lookup"><span data-stu-id="5bc52-111">**MapFileAndCheckSum**</span></span>](/windows/desktop/api/Imagehlp/nf-imagehlp-mapfileandchecksuma)
-   [<span data-ttu-id="5bc52-112">**ReBaseImage**</span><span class="sxs-lookup"><span data-stu-id="5bc52-112">**ReBaseImage**</span></span>](/windows/desktop/api/Imagehlp/nf-imagehlp-rebaseimage)
-   [<span data-ttu-id="5bc52-113">**SplitSymbols**</span><span class="sxs-lookup"><span data-stu-id="5bc52-113">**SplitSymbols**</span></span>](/windows/desktop/api/Imagehlp/nf-imagehlp-splitsymbols)
-   [<span data-ttu-id="5bc52-114">**StatusRoutine**</span><span class="sxs-lookup"><span data-stu-id="5bc52-114">**StatusRoutine**</span></span>](/windows/desktop/api/Imagehlp/nc-imagehlp-pimagehlp_status_routine)
-   [<span data-ttu-id="5bc52-115">**TouchFileTimes**</span><span class="sxs-lookup"><span data-stu-id="5bc52-115">**TouchFileTimes**</span></span>](/windows/desktop/api/Imagehlp/nf-imagehlp-touchfiletimes)
-   [<span data-ttu-id="5bc52-116">**UpdateDebugInfoFile**</span><span class="sxs-lookup"><span data-stu-id="5bc52-116">**UpdateDebugInfoFile**</span></span>](/windows/desktop/api/Imagehlp/nf-imagehlp-updatedebuginfofile)
-   [<span data-ttu-id="5bc52-117">**UpdateDebugInfoFileEx**</span><span class="sxs-lookup"><span data-stu-id="5bc52-117">**UpdateDebugInfoFileEx**</span></span>](/windows/desktop/api/Imagehlp/nf-imagehlp-updatedebuginfofileex)

 

 



