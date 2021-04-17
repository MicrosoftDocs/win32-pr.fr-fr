---
description: En savoir plus sur les macros de l’API cab
ms.assetid: 85fade43-9fcb-4100-a734-8b36d132b2c0
title: Macros de l’API Cabinet
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 390fa42e0293e5d47c405e8e99986538b8f26254
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104522868"
---
# <a name="cabinet-api-macros"></a><span data-ttu-id="181a8-103">Macros de l’API Cabinet</span><span class="sxs-lookup"><span data-stu-id="181a8-103">Cabinet API Macros</span></span>

<span data-ttu-id="181a8-104">Cette section détaille les macros utilisées par l’API CAB :</span><span class="sxs-lookup"><span data-stu-id="181a8-104">This section details the macros used by the Cabinet API:</span></span>

## <a name="fci-macros"></a><span data-ttu-id="181a8-105">FCI, macros</span><span class="sxs-lookup"><span data-stu-id="181a8-105">FCI Macros</span></span>

<span data-ttu-id="181a8-106">Les macros suivantes sont utilisées par FCI :</span><span class="sxs-lookup"><span data-stu-id="181a8-106">The following macros are used by FCI:</span></span>



| <span data-ttu-id="181a8-107">Macro</span><span class="sxs-lookup"><span data-stu-id="181a8-107">Macro</span></span>                                              | <span data-ttu-id="181a8-108">Description</span><span class="sxs-lookup"><span data-stu-id="181a8-108">Description</span></span>                                                                                    |
|----------------------------------------------------|------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="181a8-109">**FNFCIALLOC**</span><span class="sxs-lookup"><span data-stu-id="181a8-109">**FNFCIALLOC**</span></span>](/windows/desktop/api/fci/nf-fci-fnfcialloc)                   | <span data-ttu-id="181a8-110">Utilisé pour allouer de la mémoire dans un contexte FCI.</span><span class="sxs-lookup"><span data-stu-id="181a8-110">Used to allocate memory in an FCI context.</span></span><br/>                                          |
| [<span data-ttu-id="181a8-111">**FNFCICLOSE**</span><span class="sxs-lookup"><span data-stu-id="181a8-111">**FNFCICLOSE**</span></span>](/windows/desktop/api/fci/nf-fci-fnfciclose)                   | <span data-ttu-id="181a8-112">Utilisé pour fermer un fichier.</span><span class="sxs-lookup"><span data-stu-id="181a8-112">Used to close a file.</span></span><br/>                                                               |
| [<span data-ttu-id="181a8-113">**FNFCIDELETE**</span><span class="sxs-lookup"><span data-stu-id="181a8-113">**FNFCIDELETE**</span></span>](/windows/desktop/api/fci/nf-fci-fnfcidelete)                 | <span data-ttu-id="181a8-114">Utilisé pour supprimer un fichier.</span><span class="sxs-lookup"><span data-stu-id="181a8-114">Used to delete a file.</span></span><br/>                                                              |
| [<span data-ttu-id="181a8-115">**FNFCIFILEPLACED**</span><span class="sxs-lookup"><span data-stu-id="181a8-115">**FNFCIFILEPLACED**</span></span>](/windows/desktop/api/fci/nf-fci-fnfcifileplaced)         | <span data-ttu-id="181a8-116">Utilisé pour notifier quand un fichier est placé dans le fichier CAB.</span><span class="sxs-lookup"><span data-stu-id="181a8-116">Used to notify when a file is placed in the cabinet.</span></span><br/>                                |
| [<span data-ttu-id="181a8-117">**FNFCIFREE**</span><span class="sxs-lookup"><span data-stu-id="181a8-117">**FNFCIFREE**</span></span>](/windows/desktop/api/fci/nf-fci-fnfcifree)                     | <span data-ttu-id="181a8-118">Utilisé pour libérer de la mémoire précédemment allouée dans un contexte FCI.</span><span class="sxs-lookup"><span data-stu-id="181a8-118">Used to free previously allocated memory in an FCI context.</span></span><br/>                         |
| [<span data-ttu-id="181a8-119">**FNFCIGETNEXTCABINET**</span><span class="sxs-lookup"><span data-stu-id="181a8-119">**FNFCIGETNEXTCABINET**</span></span>](/windows/desktop/api/fci/nf-fci-fnfcigetnextcabinet) | <span data-ttu-id="181a8-120">Utilisé pour demander des informations pour le prochain Cabinet.</span><span class="sxs-lookup"><span data-stu-id="181a8-120">Used to request information for the next cabinet.</span></span><br/>                                   |
| [<span data-ttu-id="181a8-121">**FNFCIGETOPENINFO**</span><span class="sxs-lookup"><span data-stu-id="181a8-121">**FNFCIGETOPENINFO**</span></span>](/windows/desktop/api/fci/nf-fci-fnfcigetopeninfo)       | <span data-ttu-id="181a8-122">Permet d’ouvrir un fichier et de récupérer la date, l’heure et les attributs d’un fichier.</span><span class="sxs-lookup"><span data-stu-id="181a8-122">Used to open a file and retrieve file date, time, and attributes.</span></span><br/>                   |
| [<span data-ttu-id="181a8-123">**FNFCIGETTEMPFILE**</span><span class="sxs-lookup"><span data-stu-id="181a8-123">**FNFCIGETTEMPFILE**</span></span>](/windows/desktop/api/fci/nf-fci-fnfcigettempfile)       | <span data-ttu-id="181a8-124">Utilisé pour obtenir un nom de fichier temporaire.</span><span class="sxs-lookup"><span data-stu-id="181a8-124">Used to obtain a temporary file name.</span></span><br/>                                               |
| [<span data-ttu-id="181a8-125">**FNFCIOPEN**</span><span class="sxs-lookup"><span data-stu-id="181a8-125">**FNFCIOPEN**</span></span>](/windows/desktop/api/fci/nf-fci-fnfciopen)                     | <span data-ttu-id="181a8-126">Utilisé pour ouvrir un fichier dans un contexte FCI.</span><span class="sxs-lookup"><span data-stu-id="181a8-126">Used to open a file in an FCI context.</span></span><br/>                                              |
| [<span data-ttu-id="181a8-127">**FNFCIREAD**</span><span class="sxs-lookup"><span data-stu-id="181a8-127">**FNFCIREAD**</span></span>](/windows/desktop/api/fci/nf-fci-fnfciread)                     | <span data-ttu-id="181a8-128">Utilisé pour lire les données d’un fichier.</span><span class="sxs-lookup"><span data-stu-id="181a8-128">Used to read data from a file.</span></span><br/>                                                      |
| [<span data-ttu-id="181a8-129">**FNFCISEEK**</span><span class="sxs-lookup"><span data-stu-id="181a8-129">**FNFCISEEK**</span></span>](/windows/desktop/api/fci/nf-fci-fnfciseek)                     | <span data-ttu-id="181a8-130">Utilisé pour déplacer un pointeur de fichier vers un emplacement spécifié.</span><span class="sxs-lookup"><span data-stu-id="181a8-130">Used to move a file pointer to a specified location.</span></span><br/>                                |
| [<span data-ttu-id="181a8-131">**FNFCISTATUS**</span><span class="sxs-lookup"><span data-stu-id="181a8-131">**FNFCISTATUS**</span></span>](/windows/desktop/api/fci/nf-fci-fnfcistatus)                 | <span data-ttu-id="181a8-132">Utilisé pour mettre à jour l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="181a8-132">Used to update the user.</span></span><br/>                                                            |
| [<span data-ttu-id="181a8-133">**FNFCIWRITE**</span><span class="sxs-lookup"><span data-stu-id="181a8-133">**FNFCIWRITE**</span></span>](/windows/desktop/api/fci/nf-fci-fnfciwrite)                   | <span data-ttu-id="181a8-134">Utilisé pour écrire des données dans un fichier.</span><span class="sxs-lookup"><span data-stu-id="181a8-134">Used to write data to a file.</span></span><br/>                                                       |
| [<span data-ttu-id="181a8-135">**TCOMPfromLZXWindow**</span><span class="sxs-lookup"><span data-stu-id="181a8-135">**TCOMPfromLZXWindow**</span></span>](/windows/desktop/api/fdi_fci_types/nf-fdi_fci_types-tcompfromlzxwindow)   | <span data-ttu-id="181a8-136">Convertit la taille Windows en valeur LXZ TCOMP pour [**FCIAddFile**](/windows/desktop/api/Fci/nf-fci-fciaddfile).</span><span class="sxs-lookup"><span data-stu-id="181a8-136">Converts windows size into an LXZ TCOMP value for [**FCIAddFile**](/windows/desktop/api/Fci/nf-fci-fciaddfile).</span></span><br/> |



 

## <a name="fdi-macros"></a><span data-ttu-id="181a8-137">FDI, macros</span><span class="sxs-lookup"><span data-stu-id="181a8-137">FDI Macros</span></span>

<span data-ttu-id="181a8-138">Les macros suivantes sont utilisées par FDI :</span><span class="sxs-lookup"><span data-stu-id="181a8-138">The following macros are used by FDI:</span></span>



| <span data-ttu-id="181a8-139">Macro</span><span class="sxs-lookup"><span data-stu-id="181a8-139">Macro</span></span>                              | <span data-ttu-id="181a8-140">Description</span><span class="sxs-lookup"><span data-stu-id="181a8-140">Description</span></span>                                                                         |
|------------------------------------|-------------------------------------------------------------------------------------|
| [<span data-ttu-id="181a8-141">**FNALLOC**</span><span class="sxs-lookup"><span data-stu-id="181a8-141">**FNALLOC**</span></span>](/windows/desktop/api/fdi/nf-fdi-fnalloc)         | <span data-ttu-id="181a8-142">Utilisé pour allouer de la mémoire dans un contexte FDI.</span><span class="sxs-lookup"><span data-stu-id="181a8-142">Used to allocate memory in an FDI context.</span></span><br/>                               |
| [<span data-ttu-id="181a8-143">**FNCLOSE**</span><span class="sxs-lookup"><span data-stu-id="181a8-143">**FNCLOSE**</span></span>](/windows/desktop/api/fdi/nf-fdi-fnclose)         | <span data-ttu-id="181a8-144">Utilisé pour fermer un fichier dans un contexte FDI.</span><span class="sxs-lookup"><span data-stu-id="181a8-144">Used to close a file in an FDI context.</span></span><br/>                                  |
| [<span data-ttu-id="181a8-145">**FNFDINOTIFY**</span><span class="sxs-lookup"><span data-stu-id="181a8-145">**FNFDINOTIFY**</span></span>](/windows/desktop/api/fdi/nf-fdi-fnfdinotify) | <span data-ttu-id="181a8-146">Utilisé pour mettre à jour l’application sur l’état du décodeur.</span><span class="sxs-lookup"><span data-stu-id="181a8-146">Used to update the application on the status of the decoder.</span></span><br/>             |
| [<span data-ttu-id="181a8-147">**FNFREE**</span><span class="sxs-lookup"><span data-stu-id="181a8-147">**FNFREE**</span></span>](/windows/desktop/api/fdi/nf-fdi-fnfree)           | <span data-ttu-id="181a8-148">Utilisé pour libérer de la mémoire précédemment allouée dans un contexte FDI.</span><span class="sxs-lookup"><span data-stu-id="181a8-148">Used to free previously allocated memory in an FDI context.</span></span><br/>              |
| [<span data-ttu-id="181a8-149">**FNOPEN**</span><span class="sxs-lookup"><span data-stu-id="181a8-149">**FNOPEN**</span></span>](/windows/desktop/api/fdi/nf-fdi-fnopen)           | <span data-ttu-id="181a8-150">Utilisé pour ouvrir un fichier dans un contexte FDI.</span><span class="sxs-lookup"><span data-stu-id="181a8-150">Used to open a file in an FDI context.</span></span><br/>                                   |
| [<span data-ttu-id="181a8-151">**FNREAD**</span><span class="sxs-lookup"><span data-stu-id="181a8-151">**FNREAD**</span></span>](/windows/desktop/api/fdi/nf-fdi-fnread)           | <span data-ttu-id="181a8-152">Utilisé pour lire les données d’un fichier dans un contexte FDI.</span><span class="sxs-lookup"><span data-stu-id="181a8-152">Used to read data from a file in an FDI context.</span></span><br/>                         |
| [<span data-ttu-id="181a8-153">**FNSEEK**</span><span class="sxs-lookup"><span data-stu-id="181a8-153">**FNSEEK**</span></span>](/windows/desktop/api/fdi/nf-fdi-fnseek)           | <span data-ttu-id="181a8-154">Utilisé pour déplacer un pointeur de fichier vers l’emplacement spécifié dans un contexte FDI.</span><span class="sxs-lookup"><span data-stu-id="181a8-154">Used to move a file pointer to the specified location in an FDI context.</span></span><br/> |
| [<span data-ttu-id="181a8-155">**FNWRITE**</span><span class="sxs-lookup"><span data-stu-id="181a8-155">**FNWRITE**</span></span>](/windows/desktop/api/fdi/nf-fdi-fnwrite)         | <span data-ttu-id="181a8-156">Utilisé pour écrire des données dans un fichier dans un contexte FDI.</span><span class="sxs-lookup"><span data-stu-id="181a8-156">Used to write data to a file in an FDI context.</span></span><br/>                          |



 

## <a name="related-topics"></a><span data-ttu-id="181a8-157">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="181a8-157">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="181a8-158">Référence de l’API cab</span><span class="sxs-lookup"><span data-stu-id="181a8-158">Cabinet API Reference</span></span>](cabinet-api-reference.md)
</dt> <dt>

[<span data-ttu-id="181a8-159">Utilisation de l’API Cabinet</span><span class="sxs-lookup"><span data-stu-id="181a8-159">Using the Cabinet API</span></span>](using-the-cabinet-api.md)
</dt> </dl>

 

 




