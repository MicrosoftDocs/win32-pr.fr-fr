---
title: Opérations de pixel
description: Opérations de pixel
ms.assetid: e60cc45b-867c-441a-b579-8c7dbd46ecd9
keywords:
- Opérations de pixel OpenGL
topic_type:
- apiref
api_name:
- Pixel Operations
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 45d36fc22ace4ee18303ce0eb16c5a10f901510f
ms.sourcegitcommit: 63753fcfb0afbbe5ec283fb8316e62c2dc950f66
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/22/2021
ms.locfileid: "107908877"
---
# <a name="pixel-operations"></a><span data-ttu-id="e1a3f-104">Opérations de pixel</span><span class="sxs-lookup"><span data-stu-id="e1a3f-104">Pixel Operations</span></span>

<dl> <span data-ttu-id="e1a3f-105"><dt><span id="GL_SCISSOR_TEST"></span><span id="gl_scissor_test"></span>\_test de ciseaux du GL \_</dt> </span><span class="sxs-lookup"><span data-stu-id="e1a3f-105"><dt><span id="GL_SCISSOR_TEST"></span><span id="gl_scissor_test"></span>GL\_SCISSOR\_TEST</dt> </span></span><dd> 

| <span data-ttu-id="e1a3f-106">Propriété</span><span class="sxs-lookup"><span data-stu-id="e1a3f-106">Property</span></span> | <span data-ttu-id="e1a3f-107">Valeur</span><span class="sxs-lookup"><span data-stu-id="e1a3f-107">Value</span></span> |
|------------------|------------------------------------|
| <span data-ttu-id="e1a3f-108">Description :</span><span class="sxs-lookup"><span data-stu-id="e1a3f-108">Description:</span></span>     | <span data-ttu-id="e1a3f-109">Ciseaux activé</span><span class="sxs-lookup"><span data-stu-id="e1a3f-109">Scissoring enabled</span></span>                 |
| <span data-ttu-id="e1a3f-110">Groupe d’attributs :</span><span class="sxs-lookup"><span data-stu-id="e1a3f-110">Attribute group:</span></span> | <span data-ttu-id="e1a3f-111">ciseaux/activer</span><span class="sxs-lookup"><span data-stu-id="e1a3f-111">scissor/enable</span></span>                     |
| <span data-ttu-id="e1a3f-112">Valeur initiale :</span><span class="sxs-lookup"><span data-stu-id="e1a3f-112">Initial value:</span></span>   | <span data-ttu-id="e1a3f-113">GL- \_ faux</span><span class="sxs-lookup"><span data-stu-id="e1a3f-113">GL\_FALSE</span></span>                          |
| <span data-ttu-id="e1a3f-114">Commande d’extraction :</span><span class="sxs-lookup"><span data-stu-id="e1a3f-114">Get command:</span></span>     | [<span data-ttu-id="e1a3f-115">**glIsEnabled**</span><span class="sxs-lookup"><span data-stu-id="e1a3f-115">**glIsEnabled**</span></span>](glisenabled.md) |



 

<span data-ttu-id="e1a3f-116"></dd> <dt><span id="GL_SCISSOR_BOX"></span><span id="gl_scissor_box"></span>\_zone de ciseaux du GL \_</dt> </span><span class="sxs-lookup"><span data-stu-id="e1a3f-116"></dd> <dt><span id="GL_SCISSOR_BOX"></span><span id="gl_scissor_box"></span>GL\_SCISSOR\_BOX</dt> </span></span><dd> 

| <span data-ttu-id="e1a3f-117">Propriété</span><span class="sxs-lookup"><span data-stu-id="e1a3f-117">Property</span></span> | <span data-ttu-id="e1a3f-118">Valeur</span><span class="sxs-lookup"><span data-stu-id="e1a3f-118">Value</span></span> |
|------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="e1a3f-119">Description :</span><span class="sxs-lookup"><span data-stu-id="e1a3f-119">Description:</span></span>     | <span data-ttu-id="e1a3f-120">Zone de ciseaux</span><span class="sxs-lookup"><span data-stu-id="e1a3f-120">Scissor box</span></span>                                                                      |
| <span data-ttu-id="e1a3f-121">Groupe d’attributs :</span><span class="sxs-lookup"><span data-stu-id="e1a3f-121">Attribute group:</span></span> | <span data-ttu-id="e1a3f-122">ciseaux</span><span class="sxs-lookup"><span data-stu-id="e1a3f-122">scissor</span></span>                                                                          |
| <span data-ttu-id="e1a3f-123">Valeur initiale :</span><span class="sxs-lookup"><span data-stu-id="e1a3f-123">Initial value:</span></span>   |                                                                                  |
| <span data-ttu-id="e1a3f-124">Commande d’extraction :</span><span class="sxs-lookup"><span data-stu-id="e1a3f-124">Get command:</span></span>     | [<span data-ttu-id="e1a3f-125">**glGetIntegerv**</span><span class="sxs-lookup"><span data-stu-id="e1a3f-125">**glGetIntegerv**</span></span>](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) |



 

<span data-ttu-id="e1a3f-126"></dd> <dt><span id="GL_STENCIL_TEST"></span><span id="gl_stencil_test"></span>\_test du stencil du GL \_</dt> </span><span class="sxs-lookup"><span data-stu-id="e1a3f-126"></dd> <dt><span id="GL_STENCIL_TEST"></span><span id="gl_stencil_test"></span>GL\_STENCIL\_TEST</dt> </span></span><dd> 

| <span data-ttu-id="e1a3f-127">Propriété</span><span class="sxs-lookup"><span data-stu-id="e1a3f-127">Property</span></span> | <span data-ttu-id="e1a3f-128">Valeur</span><span class="sxs-lookup"><span data-stu-id="e1a3f-128">Value</span></span> |
|------------------|------------------------------------|
| <span data-ttu-id="e1a3f-129">Description :</span><span class="sxs-lookup"><span data-stu-id="e1a3f-129">Description:</span></span>     | <span data-ttu-id="e1a3f-130">Stencil activé</span><span class="sxs-lookup"><span data-stu-id="e1a3f-130">Stenciling enabled</span></span>                 |
| <span data-ttu-id="e1a3f-131">Groupe d’attributs :</span><span class="sxs-lookup"><span data-stu-id="e1a3f-131">Attribute group:</span></span> | <span data-ttu-id="e1a3f-132">stencil-tampon/activer</span><span class="sxs-lookup"><span data-stu-id="e1a3f-132">stencil-buffer/enable</span></span>              |
| <span data-ttu-id="e1a3f-133">Valeur initiale :</span><span class="sxs-lookup"><span data-stu-id="e1a3f-133">Initial value:</span></span>   | <span data-ttu-id="e1a3f-134">GL- \_ faux</span><span class="sxs-lookup"><span data-stu-id="e1a3f-134">GL\_FALSE</span></span>                          |
| <span data-ttu-id="e1a3f-135">Commande d’extraction :</span><span class="sxs-lookup"><span data-stu-id="e1a3f-135">Get command:</span></span>     | [<span data-ttu-id="e1a3f-136">**glIsEnabled**</span><span class="sxs-lookup"><span data-stu-id="e1a3f-136">**glIsEnabled**</span></span>](glisenabled.md) |



 

<span data-ttu-id="e1a3f-137"></dd> <dt><span id="GL_STENCIL_FUNC"></span><span id="gl_stencil_func"></span>\_Func de gabarit GL \_</dt> </span><span class="sxs-lookup"><span data-stu-id="e1a3f-137"></dd> <dt><span id="GL_STENCIL_FUNC"></span><span id="gl_stencil_func"></span>GL\_STENCIL\_FUNC</dt> </span></span><dd> 

| <span data-ttu-id="e1a3f-138">Propriété</span><span class="sxs-lookup"><span data-stu-id="e1a3f-138">Property</span></span> | <span data-ttu-id="e1a3f-139">Valeur</span><span class="sxs-lookup"><span data-stu-id="e1a3f-139">Value</span></span> |
|------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="e1a3f-140">Description :</span><span class="sxs-lookup"><span data-stu-id="e1a3f-140">Description:</span></span>     | <span data-ttu-id="e1a3f-141">Fonction de stencil</span><span class="sxs-lookup"><span data-stu-id="e1a3f-141">Stencil function</span></span>                                                                 |
| <span data-ttu-id="e1a3f-142">Groupe d’attributs :</span><span class="sxs-lookup"><span data-stu-id="e1a3f-142">Attribute group:</span></span> | <span data-ttu-id="e1a3f-143">stencil-tampon</span><span class="sxs-lookup"><span data-stu-id="e1a3f-143">stencil-buffer</span></span>                                                                   |
| <span data-ttu-id="e1a3f-144">Valeur initiale :</span><span class="sxs-lookup"><span data-stu-id="e1a3f-144">Initial value:</span></span>   | <span data-ttu-id="e1a3f-145">\_toujours GL</span><span class="sxs-lookup"><span data-stu-id="e1a3f-145">GL\_ALWAYS</span></span>                                                                       |
| <span data-ttu-id="e1a3f-146">Commande d’extraction :</span><span class="sxs-lookup"><span data-stu-id="e1a3f-146">Get command:</span></span>     | [<span data-ttu-id="e1a3f-147">**glGetIntegerv**</span><span class="sxs-lookup"><span data-stu-id="e1a3f-147">**glGetIntegerv**</span></span>](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) |



 

<span data-ttu-id="e1a3f-148"></dd> <dt><span id="GL_STENCIL_VALUE_MASK"></span><span id="gl_stencil_value_mask"></span>\_masque de \_ valeur du stencil du GL \_</dt> </span><span class="sxs-lookup"><span data-stu-id="e1a3f-148"></dd> <dt><span id="GL_STENCIL_VALUE_MASK"></span><span id="gl_stencil_value_mask"></span>GL\_STENCIL\_VALUE\_MASK</dt> </span></span><dd> 

| <span data-ttu-id="e1a3f-149">Propriété</span><span class="sxs-lookup"><span data-stu-id="e1a3f-149">Property</span></span> | <span data-ttu-id="e1a3f-150">Valeur</span><span class="sxs-lookup"><span data-stu-id="e1a3f-150">Value</span></span> |
|------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="e1a3f-151">Description :</span><span class="sxs-lookup"><span data-stu-id="e1a3f-151">Description:</span></span>     | <span data-ttu-id="e1a3f-152">Masque du gabarit</span><span class="sxs-lookup"><span data-stu-id="e1a3f-152">Stencil mask</span></span>                                                                     |
| <span data-ttu-id="e1a3f-153">Groupe d’attributs :</span><span class="sxs-lookup"><span data-stu-id="e1a3f-153">Attribute group:</span></span> | <span data-ttu-id="e1a3f-154">stencil-tampon</span><span class="sxs-lookup"><span data-stu-id="e1a3f-154">stencil-buffer</span></span>                                                                   |
| <span data-ttu-id="e1a3f-155">Valeur initiale :</span><span class="sxs-lookup"><span data-stu-id="e1a3f-155">Initial value:</span></span>   | <span data-ttu-id="e1a3f-156">du 1</span><span class="sxs-lookup"><span data-stu-id="e1a3f-156">1's</span></span>                                                                              |
| <span data-ttu-id="e1a3f-157">Commande d’extraction :</span><span class="sxs-lookup"><span data-stu-id="e1a3f-157">Get command:</span></span>     | [<span data-ttu-id="e1a3f-158">**glGetIntegerv**</span><span class="sxs-lookup"><span data-stu-id="e1a3f-158">**glGetIntegerv**</span></span>](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) |



 

<span data-ttu-id="e1a3f-159"></dd> <dt><span id="GL_STENCIL_REF"></span><span id="gl_stencil_ref"></span>Réf. du \_ stencil GL \_</dt> </span><span class="sxs-lookup"><span data-stu-id="e1a3f-159"></dd> <dt><span id="GL_STENCIL_REF"></span><span id="gl_stencil_ref"></span>GL\_STENCIL\_REF</dt> </span></span><dd> 

| <span data-ttu-id="e1a3f-160">Propriété</span><span class="sxs-lookup"><span data-stu-id="e1a3f-160">Property</span></span> | <span data-ttu-id="e1a3f-161">Valeur</span><span class="sxs-lookup"><span data-stu-id="e1a3f-161">Value</span></span> |
|------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="e1a3f-162">Description :</span><span class="sxs-lookup"><span data-stu-id="e1a3f-162">Description:</span></span>     | <span data-ttu-id="e1a3f-163">Valeur de référence du stencil</span><span class="sxs-lookup"><span data-stu-id="e1a3f-163">Stencil reference value</span></span>                                                          |
| <span data-ttu-id="e1a3f-164">Groupe d’attributs :</span><span class="sxs-lookup"><span data-stu-id="e1a3f-164">Attribute group:</span></span> | <span data-ttu-id="e1a3f-165">stencil-tampon</span><span class="sxs-lookup"><span data-stu-id="e1a3f-165">stencil-buffer</span></span>                                                                   |
| <span data-ttu-id="e1a3f-166">Valeur initiale :</span><span class="sxs-lookup"><span data-stu-id="e1a3f-166">Initial value:</span></span>   | <span data-ttu-id="e1a3f-167">0</span><span class="sxs-lookup"><span data-stu-id="e1a3f-167">0</span></span>                                                                                |
| <span data-ttu-id="e1a3f-168">Commande d’extraction :</span><span class="sxs-lookup"><span data-stu-id="e1a3f-168">Get command:</span></span>     | [<span data-ttu-id="e1a3f-169">**glGetIntegerv**</span><span class="sxs-lookup"><span data-stu-id="e1a3f-169">**glGetIntegerv**</span></span>](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) |



 

<span data-ttu-id="e1a3f-170"></dd> <dt><span id="GL_STENCIL_FAIL"></span><span id="gl_stencil_fail"></span>\_échec du stencil du GL \_</dt> </span><span class="sxs-lookup"><span data-stu-id="e1a3f-170"></dd> <dt><span id="GL_STENCIL_FAIL"></span><span id="gl_stencil_fail"></span>GL\_STENCIL\_FAIL</dt> </span></span><dd> 

| <span data-ttu-id="e1a3f-171">Propriété</span><span class="sxs-lookup"><span data-stu-id="e1a3f-171">Property</span></span> | <span data-ttu-id="e1a3f-172">Valeur</span><span class="sxs-lookup"><span data-stu-id="e1a3f-172">Value</span></span> |
|------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="e1a3f-173">Description :</span><span class="sxs-lookup"><span data-stu-id="e1a3f-173">Description:</span></span>     | <span data-ttu-id="e1a3f-174">Action d’échec du stencil</span><span class="sxs-lookup"><span data-stu-id="e1a3f-174">Stencil fail action</span></span>                                                              |
| <span data-ttu-id="e1a3f-175">Groupe d’attributs :</span><span class="sxs-lookup"><span data-stu-id="e1a3f-175">Attribute group:</span></span> | <span data-ttu-id="e1a3f-176">stencil-tampon</span><span class="sxs-lookup"><span data-stu-id="e1a3f-176">stencil-buffer</span></span>                                                                   |
| <span data-ttu-id="e1a3f-177">Valeur initiale :</span><span class="sxs-lookup"><span data-stu-id="e1a3f-177">Initial value:</span></span>   | <span data-ttu-id="e1a3f-178">conserver le GL \_</span><span class="sxs-lookup"><span data-stu-id="e1a3f-178">GL\_KEEP</span></span>                                                                         |
| <span data-ttu-id="e1a3f-179">Commande d’extraction :</span><span class="sxs-lookup"><span data-stu-id="e1a3f-179">Get command:</span></span>     | [<span data-ttu-id="e1a3f-180">**glGetIntegerv**</span><span class="sxs-lookup"><span data-stu-id="e1a3f-180">**glGetIntegerv**</span></span>](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) |



 

<span data-ttu-id="e1a3f-181"></dd> <dt><span id="GL_STENCIL_PASS_DEPTH_FAIL"></span><span id="gl_stencil_pass_depth_fail"></span>échec de la profondeur du test de \_ stencil du GL \_ \_ \_</dt> </span><span class="sxs-lookup"><span data-stu-id="e1a3f-181"></dd> <dt><span id="GL_STENCIL_PASS_DEPTH_FAIL"></span><span id="gl_stencil_pass_depth_fail"></span>GL\_STENCIL\_PASS\_DEPTH\_FAIL</dt> </span></span><dd> 

| <span data-ttu-id="e1a3f-182">Propriété</span><span class="sxs-lookup"><span data-stu-id="e1a3f-182">Property</span></span> | <span data-ttu-id="e1a3f-183">Valeur</span><span class="sxs-lookup"><span data-stu-id="e1a3f-183">Value</span></span> |
|------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="e1a3f-184">Description :</span><span class="sxs-lookup"><span data-stu-id="e1a3f-184">Description:</span></span>     | <span data-ttu-id="e1a3f-185">Action en cas d’échec du tampon de profondeur du stencil</span><span class="sxs-lookup"><span data-stu-id="e1a3f-185">Stencil depth buffer fail action</span></span>                                                 |
| <span data-ttu-id="e1a3f-186">Groupe d’attributs :</span><span class="sxs-lookup"><span data-stu-id="e1a3f-186">Attribute group:</span></span> | <span data-ttu-id="e1a3f-187">stencil-tampon</span><span class="sxs-lookup"><span data-stu-id="e1a3f-187">stencil-buffer</span></span>                                                                   |
| <span data-ttu-id="e1a3f-188">Valeur initiale :</span><span class="sxs-lookup"><span data-stu-id="e1a3f-188">Initial value:</span></span>   | <span data-ttu-id="e1a3f-189">conserver le GL \_</span><span class="sxs-lookup"><span data-stu-id="e1a3f-189">GL\_KEEP</span></span>                                                                         |
| <span data-ttu-id="e1a3f-190">Commande d’extraction :</span><span class="sxs-lookup"><span data-stu-id="e1a3f-190">Get command:</span></span>     | [<span data-ttu-id="e1a3f-191">**glGetIntegerv**</span><span class="sxs-lookup"><span data-stu-id="e1a3f-191">**glGetIntegerv**</span></span>](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) |



 

<span data-ttu-id="e1a3f-192"></dd> <dt><span id="GL_STENCIL_PASS_DEPTH_PASS"></span><span id="gl_stencil_pass_depth_pass"></span>passe de profondeur du test de la \_ passe du gabarit GL \_ \_ \_</dt> </span><span class="sxs-lookup"><span data-stu-id="e1a3f-192"></dd> <dt><span id="GL_STENCIL_PASS_DEPTH_PASS"></span><span id="gl_stencil_pass_depth_pass"></span>GL\_STENCIL\_PASS\_DEPTH\_PASS</dt> </span></span><dd> 

| <span data-ttu-id="e1a3f-193">Propriété</span><span class="sxs-lookup"><span data-stu-id="e1a3f-193">Property</span></span> | <span data-ttu-id="e1a3f-194">Valeur</span><span class="sxs-lookup"><span data-stu-id="e1a3f-194">Value</span></span> |
|------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="e1a3f-195">Description :</span><span class="sxs-lookup"><span data-stu-id="e1a3f-195">Description:</span></span>     | <span data-ttu-id="e1a3f-196">Action de passe de tampon de profondeur du stencil</span><span class="sxs-lookup"><span data-stu-id="e1a3f-196">Stencil depth buffer pass action</span></span>                                                 |
| <span data-ttu-id="e1a3f-197">Groupe d’attributs :</span><span class="sxs-lookup"><span data-stu-id="e1a3f-197">Attribute group:</span></span> | <span data-ttu-id="e1a3f-198">stencil-tampon</span><span class="sxs-lookup"><span data-stu-id="e1a3f-198">stencil-buffer</span></span>                                                                   |
| <span data-ttu-id="e1a3f-199">Valeur initiale :</span><span class="sxs-lookup"><span data-stu-id="e1a3f-199">Initial value:</span></span>   | <span data-ttu-id="e1a3f-200">conserver le GL \_</span><span class="sxs-lookup"><span data-stu-id="e1a3f-200">GL\_KEEP</span></span>                                                                         |
| <span data-ttu-id="e1a3f-201">Commande d’extraction :</span><span class="sxs-lookup"><span data-stu-id="e1a3f-201">Get command:</span></span>     | [<span data-ttu-id="e1a3f-202">**glGetIntegerv**</span><span class="sxs-lookup"><span data-stu-id="e1a3f-202">**glGetIntegerv**</span></span>](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) |



 

<span data-ttu-id="e1a3f-203"></dd> <dt><span id="GL_ALPHA_TEST"></span><span id="gl_alpha_test"></span>TEST du GL \_ alpha \_</dt> </span><span class="sxs-lookup"><span data-stu-id="e1a3f-203"></dd> <dt><span id="GL_ALPHA_TEST"></span><span id="gl_alpha_test"></span>GL\_ALPHA\_TEST</dt> </span></span><dd> 

| <span data-ttu-id="e1a3f-204">Propriété</span><span class="sxs-lookup"><span data-stu-id="e1a3f-204">Property</span></span> | <span data-ttu-id="e1a3f-205">Valeur</span><span class="sxs-lookup"><span data-stu-id="e1a3f-205">Value</span></span> |
|------------------|------------------------------------|
| <span data-ttu-id="e1a3f-206">Description :</span><span class="sxs-lookup"><span data-stu-id="e1a3f-206">Description:</span></span>     | <span data-ttu-id="e1a3f-207">Test alpha activé</span><span class="sxs-lookup"><span data-stu-id="e1a3f-207">Alpha test enabled</span></span>                 |
| <span data-ttu-id="e1a3f-208">Groupe d’attributs :</span><span class="sxs-lookup"><span data-stu-id="e1a3f-208">Attribute group:</span></span> | <span data-ttu-id="e1a3f-209">mémoire tampon de couleur/activation</span><span class="sxs-lookup"><span data-stu-id="e1a3f-209">color-buffer/enable</span></span>                |
| <span data-ttu-id="e1a3f-210">Valeur initiale :</span><span class="sxs-lookup"><span data-stu-id="e1a3f-210">Initial value:</span></span>   | <span data-ttu-id="e1a3f-211">GL- \_ faux</span><span class="sxs-lookup"><span data-stu-id="e1a3f-211">GL\_FALSE</span></span>                          |
| <span data-ttu-id="e1a3f-212">Commande d’extraction :</span><span class="sxs-lookup"><span data-stu-id="e1a3f-212">Get command:</span></span>     | [<span data-ttu-id="e1a3f-213">**glIsEnabled**</span><span class="sxs-lookup"><span data-stu-id="e1a3f-213">**glIsEnabled**</span></span>](glisenabled.md) |



 

<span data-ttu-id="e1a3f-214"></dd> <dt><span id="GL_ALPHA_TEST_FUNC"></span><span id="gl_alpha_test_func"></span>\_Func alpha de \_ test \_ GL</dt> </span><span class="sxs-lookup"><span data-stu-id="e1a3f-214"></dd> <dt><span id="GL_ALPHA_TEST_FUNC"></span><span id="gl_alpha_test_func"></span>GL\_ALPHA\_TEST\_FUNC</dt> </span></span><dd> 

| <span data-ttu-id="e1a3f-215">Propriété</span><span class="sxs-lookup"><span data-stu-id="e1a3f-215">Property</span></span> | <span data-ttu-id="e1a3f-216">Valeur</span><span class="sxs-lookup"><span data-stu-id="e1a3f-216">Value</span></span> |
|------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="e1a3f-217">Description :</span><span class="sxs-lookup"><span data-stu-id="e1a3f-217">Description:</span></span>     | <span data-ttu-id="e1a3f-218">Fonction de test alpha</span><span class="sxs-lookup"><span data-stu-id="e1a3f-218">Alpha test function</span></span>                                                              |
| <span data-ttu-id="e1a3f-219">Groupe d’attributs :</span><span class="sxs-lookup"><span data-stu-id="e1a3f-219">Attribute group:</span></span> | <span data-ttu-id="e1a3f-220">mémoire tampon de couleur</span><span class="sxs-lookup"><span data-stu-id="e1a3f-220">color-buffer</span></span>                                                                     |
| <span data-ttu-id="e1a3f-221">Valeur initiale :</span><span class="sxs-lookup"><span data-stu-id="e1a3f-221">Initial value:</span></span>   | <span data-ttu-id="e1a3f-222">\_toujours GL</span><span class="sxs-lookup"><span data-stu-id="e1a3f-222">GL\_ALWAYS</span></span>                                                                       |
| <span data-ttu-id="e1a3f-223">Commande d’extraction :</span><span class="sxs-lookup"><span data-stu-id="e1a3f-223">Get command:</span></span>     | [<span data-ttu-id="e1a3f-224">**glGetIntegerv**</span><span class="sxs-lookup"><span data-stu-id="e1a3f-224">**glGetIntegerv**</span></span>](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) |



 

<span data-ttu-id="e1a3f-225"></dd> <dt><span id="GL_ALPHA_TEST_REF"></span><span id="gl_alpha_test_ref"></span>Référence de test du GL \_ alpha \_ \_</dt> </span><span class="sxs-lookup"><span data-stu-id="e1a3f-225"></dd> <dt><span id="GL_ALPHA_TEST_REF"></span><span id="gl_alpha_test_ref"></span>GL\_ALPHA\_TEST\_REF</dt> </span></span><dd> 

| <span data-ttu-id="e1a3f-226">Propriété</span><span class="sxs-lookup"><span data-stu-id="e1a3f-226">Property</span></span> | <span data-ttu-id="e1a3f-227">Valeur</span><span class="sxs-lookup"><span data-stu-id="e1a3f-227">Value</span></span> |
|------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="e1a3f-228">Description :</span><span class="sxs-lookup"><span data-stu-id="e1a3f-228">Description:</span></span>     | <span data-ttu-id="e1a3f-229">Valeur de référence de test alpha</span><span class="sxs-lookup"><span data-stu-id="e1a3f-229">Alpha test reference value</span></span>                                                       |
| <span data-ttu-id="e1a3f-230">Groupe d’attributs :</span><span class="sxs-lookup"><span data-stu-id="e1a3f-230">Attribute group:</span></span> | <span data-ttu-id="e1a3f-231">mémoire tampon de couleur</span><span class="sxs-lookup"><span data-stu-id="e1a3f-231">color-buffer</span></span>                                                                     |
| <span data-ttu-id="e1a3f-232">Valeur initiale :</span><span class="sxs-lookup"><span data-stu-id="e1a3f-232">Initial value:</span></span>   | <span data-ttu-id="e1a3f-233">0</span><span class="sxs-lookup"><span data-stu-id="e1a3f-233">0</span></span>                                                                                |
| <span data-ttu-id="e1a3f-234">Commande d’extraction :</span><span class="sxs-lookup"><span data-stu-id="e1a3f-234">Get command:</span></span>     | [<span data-ttu-id="e1a3f-235">**glGetIntegerv**</span><span class="sxs-lookup"><span data-stu-id="e1a3f-235">**glGetIntegerv**</span></span>](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) |



 

<span data-ttu-id="e1a3f-236"></dd> <dt><span id="GL_DEPTH_TEST"></span><span id="gl_depth_test"></span>\_test de profondeur du GL \_</dt> </span><span class="sxs-lookup"><span data-stu-id="e1a3f-236"></dd> <dt><span id="GL_DEPTH_TEST"></span><span id="gl_depth_test"></span>GL\_DEPTH\_TEST</dt> </span></span><dd> 

| <span data-ttu-id="e1a3f-237">Propriété</span><span class="sxs-lookup"><span data-stu-id="e1a3f-237">Property</span></span> | <span data-ttu-id="e1a3f-238">Valeur</span><span class="sxs-lookup"><span data-stu-id="e1a3f-238">Value</span></span> |
|------------------|------------------------------------|
| <span data-ttu-id="e1a3f-239">Description :</span><span class="sxs-lookup"><span data-stu-id="e1a3f-239">Description:</span></span>     | <span data-ttu-id="e1a3f-240">Mémoire tampon de profondeur activée</span><span class="sxs-lookup"><span data-stu-id="e1a3f-240">Depth buffer enabled</span></span>               |
| <span data-ttu-id="e1a3f-241">Groupe d’attributs :</span><span class="sxs-lookup"><span data-stu-id="e1a3f-241">Attribute group:</span></span> | <span data-ttu-id="e1a3f-242">cache de profondeur/activer</span><span class="sxs-lookup"><span data-stu-id="e1a3f-242">depth-buffer/enable</span></span>                |
| <span data-ttu-id="e1a3f-243">Valeur initiale :</span><span class="sxs-lookup"><span data-stu-id="e1a3f-243">Initial value:</span></span>   | <span data-ttu-id="e1a3f-244">GL- \_ faux</span><span class="sxs-lookup"><span data-stu-id="e1a3f-244">GL\_FALSE</span></span>                          |
| <span data-ttu-id="e1a3f-245">Commande d’extraction :</span><span class="sxs-lookup"><span data-stu-id="e1a3f-245">Get command:</span></span>     | [<span data-ttu-id="e1a3f-246">**glIsEnabled**</span><span class="sxs-lookup"><span data-stu-id="e1a3f-246">**glIsEnabled**</span></span>](glisenabled.md) |



 

<span data-ttu-id="e1a3f-247"></dd> <dt><span id="GL_DEPTH_FUNC"></span><span id="gl_depth_func"></span>\_Func de profondeur GL \_</dt> </span><span class="sxs-lookup"><span data-stu-id="e1a3f-247"></dd> <dt><span id="GL_DEPTH_FUNC"></span><span id="gl_depth_func"></span>GL\_DEPTH\_FUNC</dt> </span></span><dd> 

| <span data-ttu-id="e1a3f-248">Propriété</span><span class="sxs-lookup"><span data-stu-id="e1a3f-248">Property</span></span> | <span data-ttu-id="e1a3f-249">Valeur</span><span class="sxs-lookup"><span data-stu-id="e1a3f-249">Value</span></span> |
|------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="e1a3f-250">Description :</span><span class="sxs-lookup"><span data-stu-id="e1a3f-250">Description:</span></span>     | <span data-ttu-id="e1a3f-251">Fonction de test de la mémoire tampon de profondeur</span><span class="sxs-lookup"><span data-stu-id="e1a3f-251">Depth buffer test function</span></span>                                                       |
| <span data-ttu-id="e1a3f-252">Groupe d’attributs :</span><span class="sxs-lookup"><span data-stu-id="e1a3f-252">Attribute group:</span></span> | <span data-ttu-id="e1a3f-253">mémoire tampon de profondeur</span><span class="sxs-lookup"><span data-stu-id="e1a3f-253">depth-buffer</span></span>                                                                     |
| <span data-ttu-id="e1a3f-254">Valeur initiale :</span><span class="sxs-lookup"><span data-stu-id="e1a3f-254">Initial value:</span></span>   | <span data-ttu-id="e1a3f-255">GL \_ moins</span><span class="sxs-lookup"><span data-stu-id="e1a3f-255">GL\_LESS</span></span>                                                                         |
| <span data-ttu-id="e1a3f-256">Commande d’extraction :</span><span class="sxs-lookup"><span data-stu-id="e1a3f-256">Get command:</span></span>     | [<span data-ttu-id="e1a3f-257">**glGetIntegerv**</span><span class="sxs-lookup"><span data-stu-id="e1a3f-257">**glGetIntegerv**</span></span>](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) |



 

<span data-ttu-id="e1a3f-258"></dd> <dt><span id="GL_BLEND"></span><span id="gl_blend"></span>fusion du GL \_</dt> </span><span class="sxs-lookup"><span data-stu-id="e1a3f-258"></dd> <dt><span id="GL_BLEND"></span><span id="gl_blend"></span>GL\_BLEND</dt> </span></span><dd> 

| <span data-ttu-id="e1a3f-259">Propriété</span><span class="sxs-lookup"><span data-stu-id="e1a3f-259">Property</span></span> | <span data-ttu-id="e1a3f-260">Valeur</span><span class="sxs-lookup"><span data-stu-id="e1a3f-260">Value</span></span> |
|------------------|------------------------------------|
| <span data-ttu-id="e1a3f-261">Description :</span><span class="sxs-lookup"><span data-stu-id="e1a3f-261">Description:</span></span>     | <span data-ttu-id="e1a3f-262">Fusion activée</span><span class="sxs-lookup"><span data-stu-id="e1a3f-262">Blending enabled</span></span>                   |
| <span data-ttu-id="e1a3f-263">Groupe d’attributs :</span><span class="sxs-lookup"><span data-stu-id="e1a3f-263">Attribute group:</span></span> | <span data-ttu-id="e1a3f-264">mémoire tampon de couleur/activation</span><span class="sxs-lookup"><span data-stu-id="e1a3f-264">color-buffer/enable</span></span>                |
| <span data-ttu-id="e1a3f-265">Valeur initiale :</span><span class="sxs-lookup"><span data-stu-id="e1a3f-265">Initial value:</span></span>   | <span data-ttu-id="e1a3f-266">GL- \_ faux</span><span class="sxs-lookup"><span data-stu-id="e1a3f-266">GL\_FALSE</span></span>                          |
| <span data-ttu-id="e1a3f-267">Commande d’extraction :</span><span class="sxs-lookup"><span data-stu-id="e1a3f-267">Get command:</span></span>     | [<span data-ttu-id="e1a3f-268">**glIsEnabled**</span><span class="sxs-lookup"><span data-stu-id="e1a3f-268">**glIsEnabled**</span></span>](glisenabled.md) |



 

<span data-ttu-id="e1a3f-269"></dd> <dt><span id="GL_BLENC_SRC"></span><span id="gl_blenc_src"></span>\_BLENC \_ source GL</dt> </span><span class="sxs-lookup"><span data-stu-id="e1a3f-269"></dd> <dt><span id="GL_BLENC_SRC"></span><span id="gl_blenc_src"></span>GL\_BLENC\_SRC</dt> </span></span><dd> 

| <span data-ttu-id="e1a3f-270">Propriété</span><span class="sxs-lookup"><span data-stu-id="e1a3f-270">Property</span></span> | <span data-ttu-id="e1a3f-271">Valeur</span><span class="sxs-lookup"><span data-stu-id="e1a3f-271">Value</span></span> |
|------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="e1a3f-272">Description :</span><span class="sxs-lookup"><span data-stu-id="e1a3f-272">Description:</span></span>     | <span data-ttu-id="e1a3f-273">Fusion de la fonction source</span><span class="sxs-lookup"><span data-stu-id="e1a3f-273">Blending source function</span></span>                                                         |
| <span data-ttu-id="e1a3f-274">Groupe d’attributs :</span><span class="sxs-lookup"><span data-stu-id="e1a3f-274">Attribute group:</span></span> | <span data-ttu-id="e1a3f-275">mémoire tampon de couleur</span><span class="sxs-lookup"><span data-stu-id="e1a3f-275">color-buffer</span></span>                                                                     |
| <span data-ttu-id="e1a3f-276">Valeur initiale :</span><span class="sxs-lookup"><span data-stu-id="e1a3f-276">Initial value:</span></span>   | <span data-ttu-id="e1a3f-277">GL \_ 1</span><span class="sxs-lookup"><span data-stu-id="e1a3f-277">GL\_ONE</span></span>                                                                          |
| <span data-ttu-id="e1a3f-278">Commande d’extraction :</span><span class="sxs-lookup"><span data-stu-id="e1a3f-278">Get command:</span></span>     | [<span data-ttu-id="e1a3f-279">**glGetIntegerv**</span><span class="sxs-lookup"><span data-stu-id="e1a3f-279">**glGetIntegerv**</span></span>](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) |



 

<span data-ttu-id="e1a3f-280"></dd> <dt><span id="GL_BLEND_DST"></span><span id="gl_blend_dst"></span>heure d’été du GL de \_ fusion \_</dt> </span><span class="sxs-lookup"><span data-stu-id="e1a3f-280"></dd> <dt><span id="GL_BLEND_DST"></span><span id="gl_blend_dst"></span>GL\_BLEND\_DST</dt> </span></span><dd> 

| <span data-ttu-id="e1a3f-281">Propriété</span><span class="sxs-lookup"><span data-stu-id="e1a3f-281">Property</span></span> | <span data-ttu-id="e1a3f-282">Valeur</span><span class="sxs-lookup"><span data-stu-id="e1a3f-282">Value</span></span> |
|------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="e1a3f-283">Description :</span><span class="sxs-lookup"><span data-stu-id="e1a3f-283">Description:</span></span>     | <span data-ttu-id="e1a3f-284">Fusion de la fonction destination</span><span class="sxs-lookup"><span data-stu-id="e1a3f-284">Blending destination function</span></span>                                                    |
| <span data-ttu-id="e1a3f-285">Groupe d’attributs :</span><span class="sxs-lookup"><span data-stu-id="e1a3f-285">Attribute group:</span></span> | <span data-ttu-id="e1a3f-286">mémoire tampon de couleur</span><span class="sxs-lookup"><span data-stu-id="e1a3f-286">color-buffer</span></span>                                                                     |
| <span data-ttu-id="e1a3f-287">Valeur initiale :</span><span class="sxs-lookup"><span data-stu-id="e1a3f-287">Initial value:</span></span>   | <span data-ttu-id="e1a3f-288">\_zéro GL</span><span class="sxs-lookup"><span data-stu-id="e1a3f-288">GL\_ZERO</span></span>                                                                         |
| <span data-ttu-id="e1a3f-289">Commande d’extraction :</span><span class="sxs-lookup"><span data-stu-id="e1a3f-289">Get command:</span></span>     | [<span data-ttu-id="e1a3f-290">**glGetIntegerv**</span><span class="sxs-lookup"><span data-stu-id="e1a3f-290">**glGetIntegerv**</span></span>](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) |



 

<span data-ttu-id="e1a3f-291"></dd> <dt><span id="GL_DITHER"></span><span id="gl_dither"></span>\_tramage GL</dt> </span><span class="sxs-lookup"><span data-stu-id="e1a3f-291"></dd> <dt><span id="GL_DITHER"></span><span id="gl_dither"></span>GL\_DITHER</dt> </span></span><dd> 

| <span data-ttu-id="e1a3f-292">Propriété</span><span class="sxs-lookup"><span data-stu-id="e1a3f-292">Property</span></span> | <span data-ttu-id="e1a3f-293">Valeur</span><span class="sxs-lookup"><span data-stu-id="e1a3f-293">Value</span></span> |
|------------------|------------------------------------|
| <span data-ttu-id="e1a3f-294">Description :</span><span class="sxs-lookup"><span data-stu-id="e1a3f-294">Description:</span></span>     | <span data-ttu-id="e1a3f-295">Tramage activé</span><span class="sxs-lookup"><span data-stu-id="e1a3f-295">Dithering enabled</span></span>                  |
| <span data-ttu-id="e1a3f-296">Groupe d’attributs :</span><span class="sxs-lookup"><span data-stu-id="e1a3f-296">Attribute group:</span></span> | <span data-ttu-id="e1a3f-297">mémoire tampon de couleur/activation</span><span class="sxs-lookup"><span data-stu-id="e1a3f-297">color-buffer/enable</span></span>                |
| <span data-ttu-id="e1a3f-298">Valeur initiale :</span><span class="sxs-lookup"><span data-stu-id="e1a3f-298">Initial value:</span></span>   | <span data-ttu-id="e1a3f-299">GL \_ true</span><span class="sxs-lookup"><span data-stu-id="e1a3f-299">GL\_TRUE</span></span>                           |
| <span data-ttu-id="e1a3f-300">Commande d’extraction :</span><span class="sxs-lookup"><span data-stu-id="e1a3f-300">Get command:</span></span>     | [<span data-ttu-id="e1a3f-301">**glIsEnabled**</span><span class="sxs-lookup"><span data-stu-id="e1a3f-301">**glIsEnabled**</span></span>](glisenabled.md) |



 

<span data-ttu-id="e1a3f-302"></dd> <dt><span id="GL_LOGIC_OP"></span><span id="gl_logic_op"></span>GL \_ logique \_ op</dt> </span><span class="sxs-lookup"><span data-stu-id="e1a3f-302"></dd> <dt><span id="GL_LOGIC_OP"></span><span id="gl_logic_op"></span>GL\_LOGIC\_OP</dt> </span></span><dd> 

| <span data-ttu-id="e1a3f-303">Propriété</span><span class="sxs-lookup"><span data-stu-id="e1a3f-303">Property</span></span> | <span data-ttu-id="e1a3f-304">Valeur</span><span class="sxs-lookup"><span data-stu-id="e1a3f-304">Value</span></span> |
|------------------|------------------------------------|
| <span data-ttu-id="e1a3f-305">Description :</span><span class="sxs-lookup"><span data-stu-id="e1a3f-305">Description:</span></span>     | <span data-ttu-id="e1a3f-306">Opération logique activée</span><span class="sxs-lookup"><span data-stu-id="e1a3f-306">Logical operation enabled</span></span>          |
| <span data-ttu-id="e1a3f-307">Groupe d’attributs :</span><span class="sxs-lookup"><span data-stu-id="e1a3f-307">Attribute group:</span></span> | <span data-ttu-id="e1a3f-308">mémoire tampon de couleur/activation</span><span class="sxs-lookup"><span data-stu-id="e1a3f-308">color-buffer/enable</span></span>                |
| <span data-ttu-id="e1a3f-309">Valeur initiale :</span><span class="sxs-lookup"><span data-stu-id="e1a3f-309">Initial value:</span></span>   | <span data-ttu-id="e1a3f-310">GL- \_ faux</span><span class="sxs-lookup"><span data-stu-id="e1a3f-310">GL\_FALSE</span></span>                          |
| <span data-ttu-id="e1a3f-311">Commande d’extraction :</span><span class="sxs-lookup"><span data-stu-id="e1a3f-311">Get command:</span></span>     | [<span data-ttu-id="e1a3f-312">**glIsEnabled**</span><span class="sxs-lookup"><span data-stu-id="e1a3f-312">**glIsEnabled**</span></span>](glisenabled.md) |



 

<span data-ttu-id="e1a3f-313"></dd> <dt><span id="GL_LOGIC_OP_MODE"></span><span id="gl_logic_op_mode"></span>\_mode logique \_ du \_ GL</dt> </span><span class="sxs-lookup"><span data-stu-id="e1a3f-313"></dd> <dt><span id="GL_LOGIC_OP_MODE"></span><span id="gl_logic_op_mode"></span>GL\_LOGIC\_OP\_MODE</dt> </span></span><dd> 

| <span data-ttu-id="e1a3f-314">Propriété</span><span class="sxs-lookup"><span data-stu-id="e1a3f-314">Property</span></span> | <span data-ttu-id="e1a3f-315">Valeur</span><span class="sxs-lookup"><span data-stu-id="e1a3f-315">Value</span></span> |
|------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="e1a3f-316">Description :</span><span class="sxs-lookup"><span data-stu-id="e1a3f-316">Description:</span></span>     | <span data-ttu-id="e1a3f-317">Fonction d’opération logique</span><span class="sxs-lookup"><span data-stu-id="e1a3f-317">Logical operation function</span></span>                                                       |
| <span data-ttu-id="e1a3f-318">Groupe d’attributs :</span><span class="sxs-lookup"><span data-stu-id="e1a3f-318">Attribute group:</span></span> | <span data-ttu-id="e1a3f-319">mémoire tampon de couleur</span><span class="sxs-lookup"><span data-stu-id="e1a3f-319">color-buffer</span></span>                                                                     |
| <span data-ttu-id="e1a3f-320">Valeur initiale :</span><span class="sxs-lookup"><span data-stu-id="e1a3f-320">Initial value:</span></span>   | <span data-ttu-id="e1a3f-321">\_copie GL</span><span class="sxs-lookup"><span data-stu-id="e1a3f-321">GL\_COPY</span></span>                                                                         |
| <span data-ttu-id="e1a3f-322">Commande d’extraction :</span><span class="sxs-lookup"><span data-stu-id="e1a3f-322">Get command:</span></span>     | [<span data-ttu-id="e1a3f-323">**glGetIntegerv**</span><span class="sxs-lookup"><span data-stu-id="e1a3f-323">**glGetIntegerv**</span></span>](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) |



 

</dd> </dl>

 

 




