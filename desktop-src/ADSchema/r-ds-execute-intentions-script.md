---
title: DS-Execute-intentions-script étendu à droite
description: Droit de contrôle d’accès, qui doit être accordé au conteneur partitions, qui autorise l’utilisation de l' Rendom.exe ou de l’opération de préparation dans un changement de nom de domaine.
ms.assetid: 39e9e76c-55c5-4514-ad4d-102844bcbc5a
ms.tgt_platform: multiple
keywords:
- DS-Execute-intentions-écrire un schéma AD droit étendu
topic_type:
- apiref
api_name:
- DS-Execute-Intentions-Script
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b34765db2063688ccc8fced0a1e25cac23b98ded
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/14/2020
ms.locfileid: "104108250"
---
# <a name="ds-execute-intentions-script-extended-right"></a><span data-ttu-id="c1d7c-104">DS-Execute-intentions-script étendu à droite</span><span class="sxs-lookup"><span data-stu-id="c1d7c-104">DS-Execute-Intentions-Script extended right</span></span>

<span data-ttu-id="c1d7c-105">Droit de contrôle d’accès, qui doit être accordé au conteneur partitions, qui autorise l’utilisation de l' Rendom.exe ou de l’opération de préparation dans un changement de nom de domaine.</span><span class="sxs-lookup"><span data-stu-id="c1d7c-105">Control access right, which should be granted to the partitions container, that allows the Rendom.exe or prepare operation to be used in a domain rename.</span></span> <span data-ttu-id="c1d7c-106">Ce droit d’accès au contrôle apparaît également comme un droit d’audit uniquement lorsque l’opération d' Rendom.exe ou d’exécution de l’étape est effectuée.</span><span class="sxs-lookup"><span data-stu-id="c1d7c-106">This control access right also appears as an audit-only right when the Rendom.exe or execute step operation is performed.</span></span>



| <span data-ttu-id="c1d7c-107">Entrée</span><span class="sxs-lookup"><span data-stu-id="c1d7c-107">Entry</span></span> | <span data-ttu-id="c1d7c-108">Valeur</span><span class="sxs-lookup"><span data-stu-id="c1d7c-108">Value</span></span> |
|--------------|--------------------------------------|
| <span data-ttu-id="c1d7c-109">CN</span><span class="sxs-lookup"><span data-stu-id="c1d7c-109">CN</span></span>           | <span data-ttu-id="c1d7c-110">DS-Execute-intentions-script</span><span class="sxs-lookup"><span data-stu-id="c1d7c-110">DS-Execute-Intentions-Script</span></span>         |
| <span data-ttu-id="c1d7c-111">Display-Name</span><span class="sxs-lookup"><span data-stu-id="c1d7c-111">Display-Name</span></span> | <span data-ttu-id="c1d7c-112">Exécuter le script de mise à jour de forêt</span><span class="sxs-lookup"><span data-stu-id="c1d7c-112">Execute Forest Update Script</span></span>         |
| <span data-ttu-id="c1d7c-113">Rights-GUID</span><span class="sxs-lookup"><span data-stu-id="c1d7c-113">Rights-GUID</span></span>  | <span data-ttu-id="c1d7c-114">2f16c4a5-b98e-432c-952a-cb388ba33f2e</span><span class="sxs-lookup"><span data-stu-id="c1d7c-114">2f16c4a5-b98e-432c-952a-cb388ba33f2e</span></span> |



## <a name="implementations"></a><span data-ttu-id="c1d7c-115">Implémentations</span><span class="sxs-lookup"><span data-stu-id="c1d7c-115">Implementations</span></span>

-   [<span data-ttu-id="c1d7c-116">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="c1d7c-116">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="c1d7c-117">**ADAM**</span><span class="sxs-lookup"><span data-stu-id="c1d7c-117">**ADAM**</span></span>](#adam)
-   [<span data-ttu-id="c1d7c-118">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="c1d7c-118">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="c1d7c-119">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="c1d7c-119">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="c1d7c-120">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="c1d7c-120">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="c1d7c-121">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="c1d7c-121">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-server-2003"></a><span data-ttu-id="c1d7c-122">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="c1d7c-122">Windows Server 2003</span></span>



| <span data-ttu-id="c1d7c-123">Entrée</span><span class="sxs-lookup"><span data-stu-id="c1d7c-123">Entry</span></span> | <span data-ttu-id="c1d7c-124">Valeur</span><span class="sxs-lookup"><span data-stu-id="c1d7c-124">Value</span></span> |
|-------------------------|---------------------------------------------------------------|
| <span data-ttu-id="c1d7c-125">Applies-To</span><span class="sxs-lookup"><span data-stu-id="c1d7c-125">Applies-To</span></span>              | [<span data-ttu-id="c1d7c-126">**Cross-Ref-Container**</span><span class="sxs-lookup"><span data-stu-id="c1d7c-126">**Cross-Ref-Container**</span></span>](c-crossrefcontainer.md)<br/> |
| <span data-ttu-id="c1d7c-127">Localisation-Display-ID</span><span class="sxs-lookup"><span data-stu-id="c1d7c-127">Localization-Display-ID</span></span> | <span data-ttu-id="c1d7c-128">66</span><span class="sxs-lookup"><span data-stu-id="c1d7c-128">66</span></span>                                                            |



## <a name="adam"></a><span data-ttu-id="c1d7c-129">ADAM</span><span class="sxs-lookup"><span data-stu-id="c1d7c-129">ADAM</span></span>



| <span data-ttu-id="c1d7c-130">Entrée</span><span class="sxs-lookup"><span data-stu-id="c1d7c-130">Entry</span></span> | <span data-ttu-id="c1d7c-131">Valeur</span><span class="sxs-lookup"><span data-stu-id="c1d7c-131">Value</span></span> |
|-------------------------|---------------------------------------------------------------|
| <span data-ttu-id="c1d7c-132">Applies-To</span><span class="sxs-lookup"><span data-stu-id="c1d7c-132">Applies-To</span></span>              | [<span data-ttu-id="c1d7c-133">**Cross-Ref-Container**</span><span class="sxs-lookup"><span data-stu-id="c1d7c-133">**Cross-Ref-Container**</span></span>](c-crossrefcontainer.md)<br/> |
| <span data-ttu-id="c1d7c-134">Localisation-Display-ID</span><span class="sxs-lookup"><span data-stu-id="c1d7c-134">Localization-Display-ID</span></span> | <span data-ttu-id="c1d7c-135">66</span><span class="sxs-lookup"><span data-stu-id="c1d7c-135">66</span></span>                                                            |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="c1d7c-136">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="c1d7c-136">Windows Server 2003 R2</span></span>



| <span data-ttu-id="c1d7c-137">Entrée</span><span class="sxs-lookup"><span data-stu-id="c1d7c-137">Entry</span></span> | <span data-ttu-id="c1d7c-138">Valeur</span><span class="sxs-lookup"><span data-stu-id="c1d7c-138">Value</span></span> |
|-------------------------|---------------------------------------------------------------|
| <span data-ttu-id="c1d7c-139">Applies-To</span><span class="sxs-lookup"><span data-stu-id="c1d7c-139">Applies-To</span></span>              | [<span data-ttu-id="c1d7c-140">**Cross-Ref-Container**</span><span class="sxs-lookup"><span data-stu-id="c1d7c-140">**Cross-Ref-Container**</span></span>](c-crossrefcontainer.md)<br/> |
| <span data-ttu-id="c1d7c-141">Localisation-Display-ID</span><span class="sxs-lookup"><span data-stu-id="c1d7c-141">Localization-Display-ID</span></span> | <span data-ttu-id="c1d7c-142">66</span><span class="sxs-lookup"><span data-stu-id="c1d7c-142">66</span></span>                                                            |



## <a name="windows-server-2008"></a><span data-ttu-id="c1d7c-143">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="c1d7c-143">Windows Server 2008</span></span>



| <span data-ttu-id="c1d7c-144">Entrée</span><span class="sxs-lookup"><span data-stu-id="c1d7c-144">Entry</span></span> | <span data-ttu-id="c1d7c-145">Valeur</span><span class="sxs-lookup"><span data-stu-id="c1d7c-145">Value</span></span> |
|-------------------------|---------------------------------------------------------------|
| <span data-ttu-id="c1d7c-146">Applies-To</span><span class="sxs-lookup"><span data-stu-id="c1d7c-146">Applies-To</span></span>              | [<span data-ttu-id="c1d7c-147">**Cross-Ref-Container**</span><span class="sxs-lookup"><span data-stu-id="c1d7c-147">**Cross-Ref-Container**</span></span>](c-crossrefcontainer.md)<br/> |
| <span data-ttu-id="c1d7c-148">Localisation-Display-ID</span><span class="sxs-lookup"><span data-stu-id="c1d7c-148">Localization-Display-ID</span></span> | <span data-ttu-id="c1d7c-149">66</span><span class="sxs-lookup"><span data-stu-id="c1d7c-149">66</span></span>                                                            |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="c1d7c-150">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="c1d7c-150">Windows Server 2008 R2</span></span>



| <span data-ttu-id="c1d7c-151">Entrée</span><span class="sxs-lookup"><span data-stu-id="c1d7c-151">Entry</span></span> | <span data-ttu-id="c1d7c-152">Valeur</span><span class="sxs-lookup"><span data-stu-id="c1d7c-152">Value</span></span> |
|-------------------------|---------------------------------------------------------------|
| <span data-ttu-id="c1d7c-153">Applies-To</span><span class="sxs-lookup"><span data-stu-id="c1d7c-153">Applies-To</span></span>              | [<span data-ttu-id="c1d7c-154">**Cross-Ref-Container**</span><span class="sxs-lookup"><span data-stu-id="c1d7c-154">**Cross-Ref-Container**</span></span>](c-crossrefcontainer.md)<br/> |
| <span data-ttu-id="c1d7c-155">Localisation-Display-ID</span><span class="sxs-lookup"><span data-stu-id="c1d7c-155">Localization-Display-ID</span></span> | <span data-ttu-id="c1d7c-156">66</span><span class="sxs-lookup"><span data-stu-id="c1d7c-156">66</span></span>                                                            |



## <a name="windows-server-2012"></a><span data-ttu-id="c1d7c-157">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="c1d7c-157">Windows Server 2012</span></span>



| <span data-ttu-id="c1d7c-158">Entrée</span><span class="sxs-lookup"><span data-stu-id="c1d7c-158">Entry</span></span> | <span data-ttu-id="c1d7c-159">Valeur</span><span class="sxs-lookup"><span data-stu-id="c1d7c-159">Value</span></span> |
|-------------------------|---------------------------------------------------------------|
| <span data-ttu-id="c1d7c-160">Applies-To</span><span class="sxs-lookup"><span data-stu-id="c1d7c-160">Applies-To</span></span>              | [<span data-ttu-id="c1d7c-161">**Cross-Ref-Container**</span><span class="sxs-lookup"><span data-stu-id="c1d7c-161">**Cross-Ref-Container**</span></span>](c-crossrefcontainer.md)<br/> |
| <span data-ttu-id="c1d7c-162">Localisation-Display-ID</span><span class="sxs-lookup"><span data-stu-id="c1d7c-162">Localization-Display-ID</span></span> | <span data-ttu-id="c1d7c-163">66</span><span class="sxs-lookup"><span data-stu-id="c1d7c-163">66</span></span>                                                            |



 

 





