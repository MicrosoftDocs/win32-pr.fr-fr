---
title: Générer un droit étendu de planification RSoP
description: L’utilisateur qui dispose des droits sur une unité d’organisation ou un domaine est en mesure de générer des données RSoP en mode de planification pour les utilisateurs ou les ordinateurs au sein de l’unité d’organisation.
ms.assetid: 4a874e47-c88b-4945-912b-7d4a2dd799df
ms.tgt_platform: multiple
keywords:
- Générer un schéma AD droit étendu de planification RSoP
topic_type:
- apiref
api_name:
- Generate-RSoP-Planning
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f20b7d3a6431dcc19e83f95c594fd0332e35eb2b
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/14/2020
ms.locfileid: "106516532"
---
# <a name="generate-rsop-planning-extended-right"></a><span data-ttu-id="2cd1d-104">Générer un droit étendu de planification RSoP</span><span class="sxs-lookup"><span data-stu-id="2cd1d-104">Generate-RSoP-Planning extended right</span></span>

<span data-ttu-id="2cd1d-105">L’utilisateur qui dispose des droits sur une unité d’organisation ou un domaine est en mesure de générer des données RSoP en mode de planification pour les utilisateurs ou les ordinateurs au sein de l’unité d’organisation.</span><span class="sxs-lookup"><span data-stu-id="2cd1d-105">The user who has the rights on an OU or Domain will be able to generate planning mode RSoP data for the users or computers within the OU.</span></span>



| <span data-ttu-id="2cd1d-106">Entrée</span><span class="sxs-lookup"><span data-stu-id="2cd1d-106">Entry</span></span> | <span data-ttu-id="2cd1d-107">Valeur</span><span class="sxs-lookup"><span data-stu-id="2cd1d-107">Value</span></span> |
|--------------|---------------------------------------------|
| <span data-ttu-id="2cd1d-108">CN</span><span class="sxs-lookup"><span data-stu-id="2cd1d-108">CN</span></span>           | <span data-ttu-id="2cd1d-109">Générer-stratégie RSoP-planification</span><span class="sxs-lookup"><span data-stu-id="2cd1d-109">Generate-RSoP-Planning</span></span>                      |
| <span data-ttu-id="2cd1d-110">Display-Name</span><span class="sxs-lookup"><span data-stu-id="2cd1d-110">Display-Name</span></span> | <span data-ttu-id="2cd1d-111">Générer le Jeu de stratégie résultant (Planification)</span><span class="sxs-lookup"><span data-stu-id="2cd1d-111">Generate Resultant Set of Policy (Planning)</span></span> |
| <span data-ttu-id="2cd1d-112">Rights-GUID</span><span class="sxs-lookup"><span data-stu-id="2cd1d-112">Rights-GUID</span></span>  | <span data-ttu-id="2cd1d-113">b7b1b3dd-ab09-4242-9e30-9980e5d322f7</span><span class="sxs-lookup"><span data-stu-id="2cd1d-113">b7b1b3dd-ab09-4242-9e30-9980e5d322f7</span></span>        |



## <a name="implementations"></a><span data-ttu-id="2cd1d-114">Implémentations</span><span class="sxs-lookup"><span data-stu-id="2cd1d-114">Implementations</span></span>

-   [<span data-ttu-id="2cd1d-115">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="2cd1d-115">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="2cd1d-116">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="2cd1d-116">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="2cd1d-117">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="2cd1d-117">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="2cd1d-118">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="2cd1d-118">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="2cd1d-119">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="2cd1d-119">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-server-2003"></a><span data-ttu-id="2cd1d-120">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="2cd1d-120">Windows Server 2003</span></span>



| <span data-ttu-id="2cd1d-121">Entrée</span><span class="sxs-lookup"><span data-stu-id="2cd1d-121">Entry</span></span> | <span data-ttu-id="2cd1d-122">Valeur</span><span class="sxs-lookup"><span data-stu-id="2cd1d-122">Value</span></span> |
|-------------------------|-------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2cd1d-123">Applies-To</span><span class="sxs-lookup"><span data-stu-id="2cd1d-123">Applies-To</span></span>              | [<span data-ttu-id="2cd1d-124">**Unité d’organisation**</span><span class="sxs-lookup"><span data-stu-id="2cd1d-124">**Organizational-Unit**</span></span>](c-organizationalunit.md)<br/> [<span data-ttu-id="2cd1d-125">**Domain-DNS**</span><span class="sxs-lookup"><span data-stu-id="2cd1d-125">**Domain-DNS**</span></span>](c-domaindns.md)<br/> |
| <span data-ttu-id="2cd1d-126">Localisation-Display-ID</span><span class="sxs-lookup"><span data-stu-id="2cd1d-126">Localization-Display-ID</span></span> | <span data-ttu-id="2cd1d-127">55</span><span class="sxs-lookup"><span data-stu-id="2cd1d-127">55</span></span>                                                                                                          |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="2cd1d-128">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="2cd1d-128">Windows Server 2003 R2</span></span>



| <span data-ttu-id="2cd1d-129">Entrée</span><span class="sxs-lookup"><span data-stu-id="2cd1d-129">Entry</span></span> | <span data-ttu-id="2cd1d-130">Valeur</span><span class="sxs-lookup"><span data-stu-id="2cd1d-130">Value</span></span> |
|-------------------------|-------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2cd1d-131">Applies-To</span><span class="sxs-lookup"><span data-stu-id="2cd1d-131">Applies-To</span></span>              | [<span data-ttu-id="2cd1d-132">**Unité d’organisation**</span><span class="sxs-lookup"><span data-stu-id="2cd1d-132">**Organizational-Unit**</span></span>](c-organizationalunit.md)<br/> [<span data-ttu-id="2cd1d-133">**Domain-DNS**</span><span class="sxs-lookup"><span data-stu-id="2cd1d-133">**Domain-DNS**</span></span>](c-domaindns.md)<br/> |
| <span data-ttu-id="2cd1d-134">Localisation-Display-ID</span><span class="sxs-lookup"><span data-stu-id="2cd1d-134">Localization-Display-ID</span></span> | <span data-ttu-id="2cd1d-135">55</span><span class="sxs-lookup"><span data-stu-id="2cd1d-135">55</span></span>                                                                                                          |



## <a name="windows-server-2008"></a><span data-ttu-id="2cd1d-136">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="2cd1d-136">Windows Server 2008</span></span>



| <span data-ttu-id="2cd1d-137">Entrée</span><span class="sxs-lookup"><span data-stu-id="2cd1d-137">Entry</span></span> | <span data-ttu-id="2cd1d-138">Valeur</span><span class="sxs-lookup"><span data-stu-id="2cd1d-138">Value</span></span> |
|-------------------------|-------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2cd1d-139">Applies-To</span><span class="sxs-lookup"><span data-stu-id="2cd1d-139">Applies-To</span></span>              | [<span data-ttu-id="2cd1d-140">**Unité d’organisation**</span><span class="sxs-lookup"><span data-stu-id="2cd1d-140">**Organizational-Unit**</span></span>](c-organizationalunit.md)<br/> [<span data-ttu-id="2cd1d-141">**Domain-DNS**</span><span class="sxs-lookup"><span data-stu-id="2cd1d-141">**Domain-DNS**</span></span>](c-domaindns.md)<br/> |
| <span data-ttu-id="2cd1d-142">Localisation-Display-ID</span><span class="sxs-lookup"><span data-stu-id="2cd1d-142">Localization-Display-ID</span></span> | <span data-ttu-id="2cd1d-143">55</span><span class="sxs-lookup"><span data-stu-id="2cd1d-143">55</span></span>                                                                                                          |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="2cd1d-144">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="2cd1d-144">Windows Server 2008 R2</span></span>



| <span data-ttu-id="2cd1d-145">Entrée</span><span class="sxs-lookup"><span data-stu-id="2cd1d-145">Entry</span></span> | <span data-ttu-id="2cd1d-146">Valeur</span><span class="sxs-lookup"><span data-stu-id="2cd1d-146">Value</span></span> |
|-------------------------|-------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2cd1d-147">Applies-To</span><span class="sxs-lookup"><span data-stu-id="2cd1d-147">Applies-To</span></span>              | [<span data-ttu-id="2cd1d-148">**Unité d’organisation**</span><span class="sxs-lookup"><span data-stu-id="2cd1d-148">**Organizational-Unit**</span></span>](c-organizationalunit.md)<br/> [<span data-ttu-id="2cd1d-149">**Domain-DNS**</span><span class="sxs-lookup"><span data-stu-id="2cd1d-149">**Domain-DNS**</span></span>](c-domaindns.md)<br/> |
| <span data-ttu-id="2cd1d-150">Localisation-Display-ID</span><span class="sxs-lookup"><span data-stu-id="2cd1d-150">Localization-Display-ID</span></span> | <span data-ttu-id="2cd1d-151">55</span><span class="sxs-lookup"><span data-stu-id="2cd1d-151">55</span></span>                                                                                                          |



## <a name="windows-server-2012"></a><span data-ttu-id="2cd1d-152">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="2cd1d-152">Windows Server 2012</span></span>



| <span data-ttu-id="2cd1d-153">Entrée</span><span class="sxs-lookup"><span data-stu-id="2cd1d-153">Entry</span></span> | <span data-ttu-id="2cd1d-154">Valeur</span><span class="sxs-lookup"><span data-stu-id="2cd1d-154">Value</span></span> |
|-------------------------|-------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2cd1d-155">Applies-To</span><span class="sxs-lookup"><span data-stu-id="2cd1d-155">Applies-To</span></span>              | [<span data-ttu-id="2cd1d-156">**Unité d’organisation**</span><span class="sxs-lookup"><span data-stu-id="2cd1d-156">**Organizational-Unit**</span></span>](c-organizationalunit.md)<br/> [<span data-ttu-id="2cd1d-157">**Domain-DNS**</span><span class="sxs-lookup"><span data-stu-id="2cd1d-157">**Domain-DNS**</span></span>](c-domaindns.md)<br/> |
| <span data-ttu-id="2cd1d-158">Localisation-Display-ID</span><span class="sxs-lookup"><span data-stu-id="2cd1d-158">Localization-Display-ID</span></span> | <span data-ttu-id="2cd1d-159">55</span><span class="sxs-lookup"><span data-stu-id="2cd1d-159">55</span></span>                                                                                                          |



 

 





