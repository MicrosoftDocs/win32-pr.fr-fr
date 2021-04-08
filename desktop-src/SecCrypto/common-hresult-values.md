---
description: Les valeurs HRESULT suivantes sont les plus courantes. D’autres valeurs sont contenues dans le fichier d’en-tête winerror. h.
ms.assetid: ce52efc3-92c7-40e4-ac49-0c54049e169f
title: Valeurs HRESULT communes
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1a64d042d9531d026cda548b2a699ed60c0bebd3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103863865"
---
# <a name="common-hresult-values"></a><span data-ttu-id="71047-104">Valeurs HRESULT communes</span><span class="sxs-lookup"><span data-stu-id="71047-104">Common HRESULT Values</span></span>

<span data-ttu-id="71047-105">Les valeurs HRESULT suivantes sont les plus courantes.</span><span class="sxs-lookup"><span data-stu-id="71047-105">The following HRESULT values are the most common.</span></span> <span data-ttu-id="71047-106">D’autres valeurs sont contenues dans le fichier d’en-tête winerror. h.</span><span class="sxs-lookup"><span data-stu-id="71047-106">More values are contained in the header file Winerror.h.</span></span>

<span data-ttu-id="71047-107">Voici les valeurs répertoriées par ordre alphabétique par nom.</span><span class="sxs-lookup"><span data-stu-id="71047-107">Here are the values listed alphabetically by name.</span></span>



| <span data-ttu-id="71047-108">Nom</span><span class="sxs-lookup"><span data-stu-id="71047-108">Name</span></span>            | <span data-ttu-id="71047-109">Description</span><span class="sxs-lookup"><span data-stu-id="71047-109">Description</span></span>                         | <span data-ttu-id="71047-110">Valeur</span><span class="sxs-lookup"><span data-stu-id="71047-110">Value</span></span>      |
|-----------------|-------------------------------------|------------|
| <span data-ttu-id="71047-111">\_OK</span><span class="sxs-lookup"><span data-stu-id="71047-111">S\_OK</span></span>           | <span data-ttu-id="71047-112">L’opération a réussi</span><span class="sxs-lookup"><span data-stu-id="71047-112">Operation successful</span></span>                | <span data-ttu-id="71047-113">0x00000000</span><span class="sxs-lookup"><span data-stu-id="71047-113">0x00000000</span></span> |
| <span data-ttu-id="71047-114">E \_ Abort</span><span class="sxs-lookup"><span data-stu-id="71047-114">E\_ABORT</span></span>        | <span data-ttu-id="71047-115">Opération abandonnée</span><span class="sxs-lookup"><span data-stu-id="71047-115">Operation aborted</span></span>                   | <span data-ttu-id="71047-116">0x80004004</span><span class="sxs-lookup"><span data-stu-id="71047-116">0x80004004</span></span> |
| <span data-ttu-id="71047-117">\_ACCESSDENIED E</span><span class="sxs-lookup"><span data-stu-id="71047-117">E\_ACCESSDENIED</span></span> | <span data-ttu-id="71047-118">Erreur d’accès général refusé</span><span class="sxs-lookup"><span data-stu-id="71047-118">General access denied error</span></span>         | <span data-ttu-id="71047-119">0x80070005</span><span class="sxs-lookup"><span data-stu-id="71047-119">0x80070005</span></span> |
| <span data-ttu-id="71047-120">E \_ échec</span><span class="sxs-lookup"><span data-stu-id="71047-120">E\_FAIL</span></span>         | <span data-ttu-id="71047-121">Échec non spécifié</span><span class="sxs-lookup"><span data-stu-id="71047-121">Unspecified failure</span></span>                 | <span data-ttu-id="71047-122">0x80004005</span><span class="sxs-lookup"><span data-stu-id="71047-122">0x80004005</span></span> |
| <span data-ttu-id="71047-123">\_handle E</span><span class="sxs-lookup"><span data-stu-id="71047-123">E\_HANDLE</span></span>       | <span data-ttu-id="71047-124">Handle non valide</span><span class="sxs-lookup"><span data-stu-id="71047-124">Handle that is not valid</span></span>            | <span data-ttu-id="71047-125">0x80070006</span><span class="sxs-lookup"><span data-stu-id="71047-125">0x80070006</span></span> |
| <span data-ttu-id="71047-126">E \_ INVALIDARG</span><span class="sxs-lookup"><span data-stu-id="71047-126">E\_INVALIDARG</span></span>   | <span data-ttu-id="71047-127">Un ou plusieurs arguments ne sont pas valides</span><span class="sxs-lookup"><span data-stu-id="71047-127">One or more arguments are not valid</span></span> | <span data-ttu-id="71047-128">0x80070057</span><span class="sxs-lookup"><span data-stu-id="71047-128">0x80070057</span></span> |
| <span data-ttu-id="71047-129">E \_ NOinterface</span><span class="sxs-lookup"><span data-stu-id="71047-129">E\_NOINTERFACE</span></span>  | <span data-ttu-id="71047-130">Interface non prise en charge</span><span class="sxs-lookup"><span data-stu-id="71047-130">No such interface supported</span></span>         | <span data-ttu-id="71047-131">0x80004002</span><span class="sxs-lookup"><span data-stu-id="71047-131">0x80004002</span></span> |
| <span data-ttu-id="71047-132">\_NOTIMPL E</span><span class="sxs-lookup"><span data-stu-id="71047-132">E\_NOTIMPL</span></span>      | <span data-ttu-id="71047-133">Non implémenté</span><span class="sxs-lookup"><span data-stu-id="71047-133">Not implemented</span></span>                     | <span data-ttu-id="71047-134">0x80004001</span><span class="sxs-lookup"><span data-stu-id="71047-134">0x80004001</span></span> |
| <span data-ttu-id="71047-135">\_OUTOFMEMORY E</span><span class="sxs-lookup"><span data-stu-id="71047-135">E\_OUTOFMEMORY</span></span>  | <span data-ttu-id="71047-136">Échec de l’allocation de mémoire nécessaire</span><span class="sxs-lookup"><span data-stu-id="71047-136">Failed to allocate necessary memory</span></span> | <span data-ttu-id="71047-137">0x8007000E</span><span class="sxs-lookup"><span data-stu-id="71047-137">0x8007000E</span></span> |
| <span data-ttu-id="71047-138">\_pointeur E</span><span class="sxs-lookup"><span data-stu-id="71047-138">E\_POINTER</span></span>      | <span data-ttu-id="71047-139">Pointeur non valide</span><span class="sxs-lookup"><span data-stu-id="71047-139">Pointer that is not valid</span></span>           | <span data-ttu-id="71047-140">0x80004003</span><span class="sxs-lookup"><span data-stu-id="71047-140">0x80004003</span></span> |
| <span data-ttu-id="71047-141">E \_ inattendu</span><span class="sxs-lookup"><span data-stu-id="71047-141">E\_UNEXPECTED</span></span>   | <span data-ttu-id="71047-142">Défaillance inattendue</span><span class="sxs-lookup"><span data-stu-id="71047-142">Unexpected failure</span></span>                  | <span data-ttu-id="71047-143">0x8000FFFF</span><span class="sxs-lookup"><span data-stu-id="71047-143">0x8000FFFF</span></span> |



 

<span data-ttu-id="71047-144">Voici les valeurs répertoriées par valeur d’ordre numérique.</span><span class="sxs-lookup"><span data-stu-id="71047-144">Here are the values listed in numeric order by value.</span></span>



| <span data-ttu-id="71047-145">Valeur</span><span class="sxs-lookup"><span data-stu-id="71047-145">Value</span></span>      | <span data-ttu-id="71047-146">Nom</span><span class="sxs-lookup"><span data-stu-id="71047-146">Name</span></span>            | <span data-ttu-id="71047-147">Description</span><span class="sxs-lookup"><span data-stu-id="71047-147">Description</span></span>                         |
|------------|-----------------|-------------------------------------|
| <span data-ttu-id="71047-148">0x00000000</span><span class="sxs-lookup"><span data-stu-id="71047-148">0x00000000</span></span> | <span data-ttu-id="71047-149">\_OK</span><span class="sxs-lookup"><span data-stu-id="71047-149">S\_OK</span></span>           | <span data-ttu-id="71047-150">L’opération a réussi</span><span class="sxs-lookup"><span data-stu-id="71047-150">Operation successful</span></span>                |
| <span data-ttu-id="71047-151">0x80004001</span><span class="sxs-lookup"><span data-stu-id="71047-151">0x80004001</span></span> | <span data-ttu-id="71047-152">\_NOTIMPL E</span><span class="sxs-lookup"><span data-stu-id="71047-152">E\_NOTIMPL</span></span>      | <span data-ttu-id="71047-153">Non implémenté</span><span class="sxs-lookup"><span data-stu-id="71047-153">Not implemented</span></span>                     |
| <span data-ttu-id="71047-154">0x80004002</span><span class="sxs-lookup"><span data-stu-id="71047-154">0x80004002</span></span> | <span data-ttu-id="71047-155">E \_ NOinterface</span><span class="sxs-lookup"><span data-stu-id="71047-155">E\_NOINTERFACE</span></span>  | <span data-ttu-id="71047-156">Interface non prise en charge</span><span class="sxs-lookup"><span data-stu-id="71047-156">No such interface supported</span></span>         |
| <span data-ttu-id="71047-157">0x80004003</span><span class="sxs-lookup"><span data-stu-id="71047-157">0x80004003</span></span> | <span data-ttu-id="71047-158">\_pointeur E</span><span class="sxs-lookup"><span data-stu-id="71047-158">E\_POINTER</span></span>      | <span data-ttu-id="71047-159">Pointeur non valide</span><span class="sxs-lookup"><span data-stu-id="71047-159">Pointer that is not valid</span></span>           |
| <span data-ttu-id="71047-160">0x80004004</span><span class="sxs-lookup"><span data-stu-id="71047-160">0x80004004</span></span> | <span data-ttu-id="71047-161">E \_ Abort</span><span class="sxs-lookup"><span data-stu-id="71047-161">E\_ABORT</span></span>        | <span data-ttu-id="71047-162">Opération abandonnée</span><span class="sxs-lookup"><span data-stu-id="71047-162">Operation aborted</span></span>                   |
| <span data-ttu-id="71047-163">0x80004005</span><span class="sxs-lookup"><span data-stu-id="71047-163">0x80004005</span></span> | <span data-ttu-id="71047-164">E \_ échec</span><span class="sxs-lookup"><span data-stu-id="71047-164">E\_FAIL</span></span>         | <span data-ttu-id="71047-165">Échec non spécifié</span><span class="sxs-lookup"><span data-stu-id="71047-165">Unspecified failure</span></span>                 |
| <span data-ttu-id="71047-166">0x8000FFFF</span><span class="sxs-lookup"><span data-stu-id="71047-166">0x8000FFFF</span></span> | <span data-ttu-id="71047-167">E \_ inattendu</span><span class="sxs-lookup"><span data-stu-id="71047-167">E\_UNEXPECTED</span></span>   | <span data-ttu-id="71047-168">Défaillance inattendue</span><span class="sxs-lookup"><span data-stu-id="71047-168">Unexpected failure</span></span>                  |
| <span data-ttu-id="71047-169">0x80070005</span><span class="sxs-lookup"><span data-stu-id="71047-169">0x80070005</span></span> | <span data-ttu-id="71047-170">\_ACCESSDENIED E</span><span class="sxs-lookup"><span data-stu-id="71047-170">E\_ACCESSDENIED</span></span> | <span data-ttu-id="71047-171">Erreur d’accès général refusé</span><span class="sxs-lookup"><span data-stu-id="71047-171">General access denied error</span></span>         |
| <span data-ttu-id="71047-172">0x80070006</span><span class="sxs-lookup"><span data-stu-id="71047-172">0x80070006</span></span> | <span data-ttu-id="71047-173">\_handle E</span><span class="sxs-lookup"><span data-stu-id="71047-173">E\_HANDLE</span></span>       | <span data-ttu-id="71047-174">Handle non valide</span><span class="sxs-lookup"><span data-stu-id="71047-174">Handle that is not valid</span></span>            |
| <span data-ttu-id="71047-175">0x8007000E</span><span class="sxs-lookup"><span data-stu-id="71047-175">0x8007000E</span></span> | <span data-ttu-id="71047-176">\_OUTOFMEMORY E</span><span class="sxs-lookup"><span data-stu-id="71047-176">E\_OUTOFMEMORY</span></span>  | <span data-ttu-id="71047-177">Échec de l’allocation de mémoire nécessaire</span><span class="sxs-lookup"><span data-stu-id="71047-177">Failed to allocate necessary memory</span></span> |
| <span data-ttu-id="71047-178">0x80070057</span><span class="sxs-lookup"><span data-stu-id="71047-178">0x80070057</span></span> | <span data-ttu-id="71047-179">E \_ INVALIDARG</span><span class="sxs-lookup"><span data-stu-id="71047-179">E\_INVALIDARG</span></span>   | <span data-ttu-id="71047-180">Un ou plusieurs arguments ne sont pas valides</span><span class="sxs-lookup"><span data-stu-id="71047-180">One or more arguments are not valid</span></span> |



 

 

 



