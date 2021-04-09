---
description: 'En savoir plus sur : fonctions de l’API cab'
ms.assetid: 43afef50-8fd2-49ec-9fb4-dafd8ebc009e
title: Fonctions de l’API Cabinet
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 327490332d2fe0cb9384eeaaad11215d551f4f0c
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103860910"
---
# <a name="cabinet-api-functions"></a><span data-ttu-id="93187-103">Fonctions de l’API Cabinet</span><span class="sxs-lookup"><span data-stu-id="93187-103">Cabinet API Functions</span></span>

<span data-ttu-id="93187-104">Cette section décrit les fonctions suivantes de l’API CAB :</span><span class="sxs-lookup"><span data-stu-id="93187-104">This section describes the following Cabinet API functions:</span></span>

## <a name="fci-functions"></a><span data-ttu-id="93187-105">FCI, fonctions</span><span class="sxs-lookup"><span data-stu-id="93187-105">FCI Functions</span></span>

<span data-ttu-id="93187-106">La bibliothèque FCI (file compression interface) offre la possibilité de créer des armoires (également appelées « fichiers CAB »).</span><span class="sxs-lookup"><span data-stu-id="93187-106">The FCI (File Compression Interface) library provides the ability to create cabinets (also known as "CAB files").</span></span> <span data-ttu-id="93187-107">En outre, la bibliothèque fournit la compression pour réduire la taille des données de fichier stockées dans les armoires.</span><span class="sxs-lookup"><span data-stu-id="93187-107">Additionally, the library provides compression to reduce the size of the file data stored in cabinets.</span></span>



| <span data-ttu-id="93187-108">Fonction</span><span class="sxs-lookup"><span data-stu-id="93187-108">Function</span></span>                                   | <span data-ttu-id="93187-109">Description</span><span class="sxs-lookup"><span data-stu-id="93187-109">Description</span></span>                                                                                                 |
|--------------------------------------------|-------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="93187-110">**FCIAddFile**</span><span class="sxs-lookup"><span data-stu-id="93187-110">**FCIAddFile**</span></span>](/windows/desktop/api/Fci/nf-fci-fciaddfile)           | <span data-ttu-id="93187-111">Ajoute un fichier au fichier CAB actuellement construit.</span><span class="sxs-lookup"><span data-stu-id="93187-111">Adds a file to the cabinet currently being contructed.</span></span><br/>                                           |
| [<span data-ttu-id="93187-112">**FCICreate**</span><span class="sxs-lookup"><span data-stu-id="93187-112">**FCICreate**</span></span>](/windows/desktop/api/Fci/nf-fci-fcicreate)             | <span data-ttu-id="93187-113">Crée un contexte FCI.</span><span class="sxs-lookup"><span data-stu-id="93187-113">Creates an FCI context.</span></span><br/>                                                                          |
| [<span data-ttu-id="93187-114">**FCIDestroy**</span><span class="sxs-lookup"><span data-stu-id="93187-114">**FCIDestroy**</span></span>](/windows/desktop/api/Fci/nf-fci-fcidestroy)           | <span data-ttu-id="93187-115">Supprime un contexte FCI ouvert, libérant de la mémoire et des fichiers temporaires associés au contexte.</span><span class="sxs-lookup"><span data-stu-id="93187-115">Deletes an open FCI context, freeing any memory and temporary files associated with the context.</span></span><br/> |
| [<span data-ttu-id="93187-116">**FCIFlushCabinet**</span><span class="sxs-lookup"><span data-stu-id="93187-116">**FCIFlushCabinet**</span></span>](/windows/desktop/api/Fci/nf-fci-fciflushcabinet) | <span data-ttu-id="93187-117">Termine le fichier CAB actuel.</span><span class="sxs-lookup"><span data-stu-id="93187-117">Completes the current cabinet.</span></span><br/>                                                                   |
| [<span data-ttu-id="93187-118">**FCIFlushFolder**</span><span class="sxs-lookup"><span data-stu-id="93187-118">**FCIFlushFolder**</span></span>](/windows/desktop/api/Fci/nf-fci-fciflushfolder)   | <span data-ttu-id="93187-119">Force l’exécution immédiate du dossier actif en cours de construction.</span><span class="sxs-lookup"><span data-stu-id="93187-119">Forces the current folder under construction to be completed immediately.</span></span><br/>                        |



 

## <a name="fdi-functions"></a><span data-ttu-id="93187-120">Fonctions FDI</span><span class="sxs-lookup"><span data-stu-id="93187-120">FDI Functions</span></span>

<span data-ttu-id="93187-121">La bibliothèque FDI (file Decompression interface) offre la possibilité d’extraire des fichiers des armoires.</span><span class="sxs-lookup"><span data-stu-id="93187-121">The FDI (File Decompression Interface) library provides the ability to extract files from cabinets.</span></span>



| <span data-ttu-id="93187-122">Fonction</span><span class="sxs-lookup"><span data-stu-id="93187-122">Function</span></span>                                         | <span data-ttu-id="93187-123">Description</span><span class="sxs-lookup"><span data-stu-id="93187-123">Description</span></span>                                                                                       |
|--------------------------------------------------|---------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="93187-124">**FDICopy**</span><span class="sxs-lookup"><span data-stu-id="93187-124">**FDICopy**</span></span>](/windows/desktop/api/Fdi/nf-fdi-fdicopy)                       | <span data-ttu-id="93187-125">Extrait des fichiers des armoires.</span><span class="sxs-lookup"><span data-stu-id="93187-125">Extracts files from cabinets.</span></span><br/>                                                          |
| [<span data-ttu-id="93187-126">**FDICreate**</span><span class="sxs-lookup"><span data-stu-id="93187-126">**FDICreate**</span></span>](/windows/desktop/api/Fdi/nf-fdi-fdicreate)                   | <span data-ttu-id="93187-127">Crée un contexte FDI.</span><span class="sxs-lookup"><span data-stu-id="93187-127">Creates an FDI context.</span></span><br/>                                                                |
| [<span data-ttu-id="93187-128">**FDIDestroy**</span><span class="sxs-lookup"><span data-stu-id="93187-128">**FDIDestroy**</span></span>](/windows/desktop/api/Fdi/nf-fdi-fdidestroy)                 | <span data-ttu-id="93187-129">Supprime un contexte FDI ouvert.</span><span class="sxs-lookup"><span data-stu-id="93187-129">Deletes an open FDI context.</span></span><br/>                                                           |
| [<span data-ttu-id="93187-130">**FDIIsCabinet**</span><span class="sxs-lookup"><span data-stu-id="93187-130">**FDIIsCabinet**</span></span>](/windows/desktop/api/Fdi/nf-fdi-fdiiscabinet)             | <span data-ttu-id="93187-131">Détermine si un fichier est un fichier CAB et, si c’est le cas, retourne des informations descriptives.</span><span class="sxs-lookup"><span data-stu-id="93187-131">Determines whether a file is a cabinet and, if it is, returns descriptive information.</span></span><br/> |
| [<span data-ttu-id="93187-132">**FDITruncateCabinet**</span><span class="sxs-lookup"><span data-stu-id="93187-132">**FDITruncateCabinet**</span></span>](/windows/desktop/api/Fdi/nf-fdi-fditruncatecabinet) | <span data-ttu-id="93187-133">Tronque un fichier CAB en commençant au numéro de dossier spécifié.</span><span class="sxs-lookup"><span data-stu-id="93187-133">Truncates a cabinet file starting at the specified folder number.</span></span><br/>                      |



 

## <a name="deprecated-functions"></a><span data-ttu-id="93187-134">Fonctions dépréciées</span><span class="sxs-lookup"><span data-stu-id="93187-134">Deprecated Functions</span></span>

-   [<span data-ttu-id="93187-135">**DeleteExtractedFiles**</span><span class="sxs-lookup"><span data-stu-id="93187-135">**DeleteExtractedFiles**</span></span>](deleteextractedfiles.md)
-   [<span data-ttu-id="93187-136">**DllGetVersion**</span><span class="sxs-lookup"><span data-stu-id="93187-136">**DllGetVersion**</span></span>](dllgetversion.md)
-   [<span data-ttu-id="93187-137">**Extraction**</span><span class="sxs-lookup"><span data-stu-id="93187-137">**Extract**</span></span>](extract.md)
-   [<span data-ttu-id="93187-138">**GetDllVersion**</span><span class="sxs-lookup"><span data-stu-id="93187-138">**GetDllVersion**</span></span>](getdllversion.md)

## <a name="related-topics"></a><span data-ttu-id="93187-139">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="93187-139">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="93187-140">Référence de l’API cab</span><span class="sxs-lookup"><span data-stu-id="93187-140">Cabinet API Reference</span></span>](cabinet-api-reference.md)
</dt> <dt>

[<span data-ttu-id="93187-141">Utilisation de l’API Cabinet</span><span class="sxs-lookup"><span data-stu-id="93187-141">Using the Cabinet API</span></span>](using-the-cabinet-api.md)
</dt> </dl>

 

 




