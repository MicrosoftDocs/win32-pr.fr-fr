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
ms.openlocfilehash: fda15342b246ba979bdbe60184eeb632368f36b4
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/25/2019
ms.locfileid: "103841158"
---
# <a name="pixel-operations"></a><span data-ttu-id="0acd5-104">Opérations de pixel</span><span class="sxs-lookup"><span data-stu-id="0acd5-104">Pixel Operations</span></span>

<dl> <span data-ttu-id="0acd5-105"><dt><span id="GL_SCISSOR_TEST"></span><span id="gl_scissor_test"></span>\_test de ciseaux du GL \_</dt> </span><span class="sxs-lookup"><span data-stu-id="0acd5-105"><dt><span id="GL_SCISSOR_TEST"></span><span id="gl_scissor_test"></span>GL\_SCISSOR\_TEST</dt> </span></span><dd> 

|                  |                                    |
|------------------|------------------------------------|
| <span data-ttu-id="0acd5-106">Description :</span><span class="sxs-lookup"><span data-stu-id="0acd5-106">Description:</span></span>     | <span data-ttu-id="0acd5-107">Ciseaux activé</span><span class="sxs-lookup"><span data-stu-id="0acd5-107">Scissoring enabled</span></span>                 |
| <span data-ttu-id="0acd5-108">Groupe d’attributs :</span><span class="sxs-lookup"><span data-stu-id="0acd5-108">Attribute group:</span></span> | <span data-ttu-id="0acd5-109">ciseaux/activer</span><span class="sxs-lookup"><span data-stu-id="0acd5-109">scissor/enable</span></span>                     |
| <span data-ttu-id="0acd5-110">Valeur initiale :</span><span class="sxs-lookup"><span data-stu-id="0acd5-110">Initial value:</span></span>   | <span data-ttu-id="0acd5-111">GL- \_ faux</span><span class="sxs-lookup"><span data-stu-id="0acd5-111">GL\_FALSE</span></span>                          |
| <span data-ttu-id="0acd5-112">Commande d’extraction :</span><span class="sxs-lookup"><span data-stu-id="0acd5-112">Get command:</span></span>     | [<span data-ttu-id="0acd5-113">**glIsEnabled**</span><span class="sxs-lookup"><span data-stu-id="0acd5-113">**glIsEnabled**</span></span>](glisenabled.md) |



 

<span data-ttu-id="0acd5-114"></dd> <dt><span id="GL_SCISSOR_BOX"></span><span id="gl_scissor_box"></span>\_zone de ciseaux du GL \_</dt> </span><span class="sxs-lookup"><span data-stu-id="0acd5-114"></dd> <dt><span id="GL_SCISSOR_BOX"></span><span id="gl_scissor_box"></span>GL\_SCISSOR\_BOX</dt> </span></span><dd> 

|                  |                                                                                  |
|------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="0acd5-115">Description :</span><span class="sxs-lookup"><span data-stu-id="0acd5-115">Description:</span></span>     | <span data-ttu-id="0acd5-116">Zone de ciseaux</span><span class="sxs-lookup"><span data-stu-id="0acd5-116">Scissor box</span></span>                                                                      |
| <span data-ttu-id="0acd5-117">Groupe d’attributs :</span><span class="sxs-lookup"><span data-stu-id="0acd5-117">Attribute group:</span></span> | <span data-ttu-id="0acd5-118">ciseaux</span><span class="sxs-lookup"><span data-stu-id="0acd5-118">scissor</span></span>                                                                          |
| <span data-ttu-id="0acd5-119">Valeur initiale :</span><span class="sxs-lookup"><span data-stu-id="0acd5-119">Initial value:</span></span>   |                                                                                  |
| <span data-ttu-id="0acd5-120">Commande d’extraction :</span><span class="sxs-lookup"><span data-stu-id="0acd5-120">Get command:</span></span>     | [<span data-ttu-id="0acd5-121">**glGetIntegerv**</span><span class="sxs-lookup"><span data-stu-id="0acd5-121">**glGetIntegerv**</span></span>](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) |



 

<span data-ttu-id="0acd5-122"></dd> <dt><span id="GL_STENCIL_TEST"></span><span id="gl_stencil_test"></span>\_test du stencil du GL \_</dt> </span><span class="sxs-lookup"><span data-stu-id="0acd5-122"></dd> <dt><span id="GL_STENCIL_TEST"></span><span id="gl_stencil_test"></span>GL\_STENCIL\_TEST</dt> </span></span><dd> 

|                  |                                    |
|------------------|------------------------------------|
| <span data-ttu-id="0acd5-123">Description :</span><span class="sxs-lookup"><span data-stu-id="0acd5-123">Description:</span></span>     | <span data-ttu-id="0acd5-124">Stencil activé</span><span class="sxs-lookup"><span data-stu-id="0acd5-124">Stenciling enabled</span></span>                 |
| <span data-ttu-id="0acd5-125">Groupe d’attributs :</span><span class="sxs-lookup"><span data-stu-id="0acd5-125">Attribute group:</span></span> | <span data-ttu-id="0acd5-126">stencil-tampon/activer</span><span class="sxs-lookup"><span data-stu-id="0acd5-126">stencil-buffer/enable</span></span>              |
| <span data-ttu-id="0acd5-127">Valeur initiale :</span><span class="sxs-lookup"><span data-stu-id="0acd5-127">Initial value:</span></span>   | <span data-ttu-id="0acd5-128">GL- \_ faux</span><span class="sxs-lookup"><span data-stu-id="0acd5-128">GL\_FALSE</span></span>                          |
| <span data-ttu-id="0acd5-129">Commande d’extraction :</span><span class="sxs-lookup"><span data-stu-id="0acd5-129">Get command:</span></span>     | [<span data-ttu-id="0acd5-130">**glIsEnabled**</span><span class="sxs-lookup"><span data-stu-id="0acd5-130">**glIsEnabled**</span></span>](glisenabled.md) |



 

<span data-ttu-id="0acd5-131"></dd> <dt><span id="GL_STENCIL_FUNC"></span><span id="gl_stencil_func"></span>\_Func de gabarit GL \_</dt> </span><span class="sxs-lookup"><span data-stu-id="0acd5-131"></dd> <dt><span id="GL_STENCIL_FUNC"></span><span id="gl_stencil_func"></span>GL\_STENCIL\_FUNC</dt> </span></span><dd> 

|                  |                                                                                  |
|------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="0acd5-132">Description :</span><span class="sxs-lookup"><span data-stu-id="0acd5-132">Description:</span></span>     | <span data-ttu-id="0acd5-133">Fonction de stencil</span><span class="sxs-lookup"><span data-stu-id="0acd5-133">Stencil function</span></span>                                                                 |
| <span data-ttu-id="0acd5-134">Groupe d’attributs :</span><span class="sxs-lookup"><span data-stu-id="0acd5-134">Attribute group:</span></span> | <span data-ttu-id="0acd5-135">stencil-tampon</span><span class="sxs-lookup"><span data-stu-id="0acd5-135">stencil-buffer</span></span>                                                                   |
| <span data-ttu-id="0acd5-136">Valeur initiale :</span><span class="sxs-lookup"><span data-stu-id="0acd5-136">Initial value:</span></span>   | <span data-ttu-id="0acd5-137">\_toujours GL</span><span class="sxs-lookup"><span data-stu-id="0acd5-137">GL\_ALWAYS</span></span>                                                                       |
| <span data-ttu-id="0acd5-138">Commande d’extraction :</span><span class="sxs-lookup"><span data-stu-id="0acd5-138">Get command:</span></span>     | [<span data-ttu-id="0acd5-139">**glGetIntegerv**</span><span class="sxs-lookup"><span data-stu-id="0acd5-139">**glGetIntegerv**</span></span>](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) |



 

<span data-ttu-id="0acd5-140"></dd> <dt><span id="GL_STENCIL_VALUE_MASK"></span><span id="gl_stencil_value_mask"></span>\_masque de \_ valeur du stencil du GL \_</dt> </span><span class="sxs-lookup"><span data-stu-id="0acd5-140"></dd> <dt><span id="GL_STENCIL_VALUE_MASK"></span><span id="gl_stencil_value_mask"></span>GL\_STENCIL\_VALUE\_MASK</dt> </span></span><dd> 

|                  |                                                                                  |
|------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="0acd5-141">Description :</span><span class="sxs-lookup"><span data-stu-id="0acd5-141">Description:</span></span>     | <span data-ttu-id="0acd5-142">Masque du gabarit</span><span class="sxs-lookup"><span data-stu-id="0acd5-142">Stencil mask</span></span>                                                                     |
| <span data-ttu-id="0acd5-143">Groupe d’attributs :</span><span class="sxs-lookup"><span data-stu-id="0acd5-143">Attribute group:</span></span> | <span data-ttu-id="0acd5-144">stencil-tampon</span><span class="sxs-lookup"><span data-stu-id="0acd5-144">stencil-buffer</span></span>                                                                   |
| <span data-ttu-id="0acd5-145">Valeur initiale :</span><span class="sxs-lookup"><span data-stu-id="0acd5-145">Initial value:</span></span>   | <span data-ttu-id="0acd5-146">du 1</span><span class="sxs-lookup"><span data-stu-id="0acd5-146">1's</span></span>                                                                              |
| <span data-ttu-id="0acd5-147">Commande d’extraction :</span><span class="sxs-lookup"><span data-stu-id="0acd5-147">Get command:</span></span>     | [<span data-ttu-id="0acd5-148">**glGetIntegerv**</span><span class="sxs-lookup"><span data-stu-id="0acd5-148">**glGetIntegerv**</span></span>](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) |



 

<span data-ttu-id="0acd5-149"></dd> <dt><span id="GL_STENCIL_REF"></span><span id="gl_stencil_ref"></span>Réf. du \_ stencil GL \_</dt> </span><span class="sxs-lookup"><span data-stu-id="0acd5-149"></dd> <dt><span id="GL_STENCIL_REF"></span><span id="gl_stencil_ref"></span>GL\_STENCIL\_REF</dt> </span></span><dd> 

|                  |                                                                                  |
|------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="0acd5-150">Description :</span><span class="sxs-lookup"><span data-stu-id="0acd5-150">Description:</span></span>     | <span data-ttu-id="0acd5-151">Valeur de référence du stencil</span><span class="sxs-lookup"><span data-stu-id="0acd5-151">Stencil reference value</span></span>                                                          |
| <span data-ttu-id="0acd5-152">Groupe d’attributs :</span><span class="sxs-lookup"><span data-stu-id="0acd5-152">Attribute group:</span></span> | <span data-ttu-id="0acd5-153">stencil-tampon</span><span class="sxs-lookup"><span data-stu-id="0acd5-153">stencil-buffer</span></span>                                                                   |
| <span data-ttu-id="0acd5-154">Valeur initiale :</span><span class="sxs-lookup"><span data-stu-id="0acd5-154">Initial value:</span></span>   | <span data-ttu-id="0acd5-155">0</span><span class="sxs-lookup"><span data-stu-id="0acd5-155">0</span></span>                                                                                |
| <span data-ttu-id="0acd5-156">Commande d’extraction :</span><span class="sxs-lookup"><span data-stu-id="0acd5-156">Get command:</span></span>     | [<span data-ttu-id="0acd5-157">**glGetIntegerv**</span><span class="sxs-lookup"><span data-stu-id="0acd5-157">**glGetIntegerv**</span></span>](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) |



 

<span data-ttu-id="0acd5-158"></dd> <dt><span id="GL_STENCIL_FAIL"></span><span id="gl_stencil_fail"></span>\_échec du stencil du GL \_</dt> </span><span class="sxs-lookup"><span data-stu-id="0acd5-158"></dd> <dt><span id="GL_STENCIL_FAIL"></span><span id="gl_stencil_fail"></span>GL\_STENCIL\_FAIL</dt> </span></span><dd> 

|                  |                                                                                  |
|------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="0acd5-159">Description :</span><span class="sxs-lookup"><span data-stu-id="0acd5-159">Description:</span></span>     | <span data-ttu-id="0acd5-160">Action d’échec du stencil</span><span class="sxs-lookup"><span data-stu-id="0acd5-160">Stencil fail action</span></span>                                                              |
| <span data-ttu-id="0acd5-161">Groupe d’attributs :</span><span class="sxs-lookup"><span data-stu-id="0acd5-161">Attribute group:</span></span> | <span data-ttu-id="0acd5-162">stencil-tampon</span><span class="sxs-lookup"><span data-stu-id="0acd5-162">stencil-buffer</span></span>                                                                   |
| <span data-ttu-id="0acd5-163">Valeur initiale :</span><span class="sxs-lookup"><span data-stu-id="0acd5-163">Initial value:</span></span>   | <span data-ttu-id="0acd5-164">conserver le GL \_</span><span class="sxs-lookup"><span data-stu-id="0acd5-164">GL\_KEEP</span></span>                                                                         |
| <span data-ttu-id="0acd5-165">Commande d’extraction :</span><span class="sxs-lookup"><span data-stu-id="0acd5-165">Get command:</span></span>     | [<span data-ttu-id="0acd5-166">**glGetIntegerv**</span><span class="sxs-lookup"><span data-stu-id="0acd5-166">**glGetIntegerv**</span></span>](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) |



 

<span data-ttu-id="0acd5-167"></dd> <dt><span id="GL_STENCIL_PASS_DEPTH_FAIL"></span><span id="gl_stencil_pass_depth_fail"></span>échec de la profondeur du test de \_ stencil du GL \_ \_ \_</dt> </span><span class="sxs-lookup"><span data-stu-id="0acd5-167"></dd> <dt><span id="GL_STENCIL_PASS_DEPTH_FAIL"></span><span id="gl_stencil_pass_depth_fail"></span>GL\_STENCIL\_PASS\_DEPTH\_FAIL</dt> </span></span><dd> 

|                  |                                                                                  |
|------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="0acd5-168">Description :</span><span class="sxs-lookup"><span data-stu-id="0acd5-168">Description:</span></span>     | <span data-ttu-id="0acd5-169">Action en cas d’échec du tampon de profondeur du stencil</span><span class="sxs-lookup"><span data-stu-id="0acd5-169">Stencil depth buffer fail action</span></span>                                                 |
| <span data-ttu-id="0acd5-170">Groupe d’attributs :</span><span class="sxs-lookup"><span data-stu-id="0acd5-170">Attribute group:</span></span> | <span data-ttu-id="0acd5-171">stencil-tampon</span><span class="sxs-lookup"><span data-stu-id="0acd5-171">stencil-buffer</span></span>                                                                   |
| <span data-ttu-id="0acd5-172">Valeur initiale :</span><span class="sxs-lookup"><span data-stu-id="0acd5-172">Initial value:</span></span>   | <span data-ttu-id="0acd5-173">conserver le GL \_</span><span class="sxs-lookup"><span data-stu-id="0acd5-173">GL\_KEEP</span></span>                                                                         |
| <span data-ttu-id="0acd5-174">Commande d’extraction :</span><span class="sxs-lookup"><span data-stu-id="0acd5-174">Get command:</span></span>     | [<span data-ttu-id="0acd5-175">**glGetIntegerv**</span><span class="sxs-lookup"><span data-stu-id="0acd5-175">**glGetIntegerv**</span></span>](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) |



 

<span data-ttu-id="0acd5-176"></dd> <dt><span id="GL_STENCIL_PASS_DEPTH_PASS"></span><span id="gl_stencil_pass_depth_pass"></span>passe de profondeur du test de la \_ passe du gabarit GL \_ \_ \_</dt> </span><span class="sxs-lookup"><span data-stu-id="0acd5-176"></dd> <dt><span id="GL_STENCIL_PASS_DEPTH_PASS"></span><span id="gl_stencil_pass_depth_pass"></span>GL\_STENCIL\_PASS\_DEPTH\_PASS</dt> </span></span><dd> 

|                  |                                                                                  |
|------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="0acd5-177">Description :</span><span class="sxs-lookup"><span data-stu-id="0acd5-177">Description:</span></span>     | <span data-ttu-id="0acd5-178">Action de passe de tampon de profondeur du stencil</span><span class="sxs-lookup"><span data-stu-id="0acd5-178">Stencil depth buffer pass action</span></span>                                                 |
| <span data-ttu-id="0acd5-179">Groupe d’attributs :</span><span class="sxs-lookup"><span data-stu-id="0acd5-179">Attribute group:</span></span> | <span data-ttu-id="0acd5-180">stencil-tampon</span><span class="sxs-lookup"><span data-stu-id="0acd5-180">stencil-buffer</span></span>                                                                   |
| <span data-ttu-id="0acd5-181">Valeur initiale :</span><span class="sxs-lookup"><span data-stu-id="0acd5-181">Initial value:</span></span>   | <span data-ttu-id="0acd5-182">conserver le GL \_</span><span class="sxs-lookup"><span data-stu-id="0acd5-182">GL\_KEEP</span></span>                                                                         |
| <span data-ttu-id="0acd5-183">Commande d’extraction :</span><span class="sxs-lookup"><span data-stu-id="0acd5-183">Get command:</span></span>     | [<span data-ttu-id="0acd5-184">**glGetIntegerv**</span><span class="sxs-lookup"><span data-stu-id="0acd5-184">**glGetIntegerv**</span></span>](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) |



 

<span data-ttu-id="0acd5-185"></dd> <dt><span id="GL_ALPHA_TEST"></span><span id="gl_alpha_test"></span>TEST du GL \_ alpha \_</dt> </span><span class="sxs-lookup"><span data-stu-id="0acd5-185"></dd> <dt><span id="GL_ALPHA_TEST"></span><span id="gl_alpha_test"></span>GL\_ALPHA\_TEST</dt> </span></span><dd> 

|                  |                                    |
|------------------|------------------------------------|
| <span data-ttu-id="0acd5-186">Description :</span><span class="sxs-lookup"><span data-stu-id="0acd5-186">Description:</span></span>     | <span data-ttu-id="0acd5-187">Test alpha activé</span><span class="sxs-lookup"><span data-stu-id="0acd5-187">Alpha test enabled</span></span>                 |
| <span data-ttu-id="0acd5-188">Groupe d’attributs :</span><span class="sxs-lookup"><span data-stu-id="0acd5-188">Attribute group:</span></span> | <span data-ttu-id="0acd5-189">mémoire tampon de couleur/activation</span><span class="sxs-lookup"><span data-stu-id="0acd5-189">color-buffer/enable</span></span>                |
| <span data-ttu-id="0acd5-190">Valeur initiale :</span><span class="sxs-lookup"><span data-stu-id="0acd5-190">Initial value:</span></span>   | <span data-ttu-id="0acd5-191">GL- \_ faux</span><span class="sxs-lookup"><span data-stu-id="0acd5-191">GL\_FALSE</span></span>                          |
| <span data-ttu-id="0acd5-192">Commande d’extraction :</span><span class="sxs-lookup"><span data-stu-id="0acd5-192">Get command:</span></span>     | [<span data-ttu-id="0acd5-193">**glIsEnabled**</span><span class="sxs-lookup"><span data-stu-id="0acd5-193">**glIsEnabled**</span></span>](glisenabled.md) |



 

<span data-ttu-id="0acd5-194"></dd> <dt><span id="GL_ALPHA_TEST_FUNC"></span><span id="gl_alpha_test_func"></span>\_Func alpha de \_ test \_ GL</dt> </span><span class="sxs-lookup"><span data-stu-id="0acd5-194"></dd> <dt><span id="GL_ALPHA_TEST_FUNC"></span><span id="gl_alpha_test_func"></span>GL\_ALPHA\_TEST\_FUNC</dt> </span></span><dd> 

|                  |                                                                                  |
|------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="0acd5-195">Description :</span><span class="sxs-lookup"><span data-stu-id="0acd5-195">Description:</span></span>     | <span data-ttu-id="0acd5-196">Fonction de test alpha</span><span class="sxs-lookup"><span data-stu-id="0acd5-196">Alpha test function</span></span>                                                              |
| <span data-ttu-id="0acd5-197">Groupe d’attributs :</span><span class="sxs-lookup"><span data-stu-id="0acd5-197">Attribute group:</span></span> | <span data-ttu-id="0acd5-198">mémoire tampon de couleur</span><span class="sxs-lookup"><span data-stu-id="0acd5-198">color-buffer</span></span>                                                                     |
| <span data-ttu-id="0acd5-199">Valeur initiale :</span><span class="sxs-lookup"><span data-stu-id="0acd5-199">Initial value:</span></span>   | <span data-ttu-id="0acd5-200">\_toujours GL</span><span class="sxs-lookup"><span data-stu-id="0acd5-200">GL\_ALWAYS</span></span>                                                                       |
| <span data-ttu-id="0acd5-201">Commande d’extraction :</span><span class="sxs-lookup"><span data-stu-id="0acd5-201">Get command:</span></span>     | [<span data-ttu-id="0acd5-202">**glGetIntegerv**</span><span class="sxs-lookup"><span data-stu-id="0acd5-202">**glGetIntegerv**</span></span>](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) |



 

<span data-ttu-id="0acd5-203"></dd> <dt><span id="GL_ALPHA_TEST_REF"></span><span id="gl_alpha_test_ref"></span>Référence de test du GL \_ alpha \_ \_</dt> </span><span class="sxs-lookup"><span data-stu-id="0acd5-203"></dd> <dt><span id="GL_ALPHA_TEST_REF"></span><span id="gl_alpha_test_ref"></span>GL\_ALPHA\_TEST\_REF</dt> </span></span><dd> 

|                  |                                                                                  |
|------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="0acd5-204">Description :</span><span class="sxs-lookup"><span data-stu-id="0acd5-204">Description:</span></span>     | <span data-ttu-id="0acd5-205">Valeur de référence de test alpha</span><span class="sxs-lookup"><span data-stu-id="0acd5-205">Alpha test reference value</span></span>                                                       |
| <span data-ttu-id="0acd5-206">Groupe d’attributs :</span><span class="sxs-lookup"><span data-stu-id="0acd5-206">Attribute group:</span></span> | <span data-ttu-id="0acd5-207">mémoire tampon de couleur</span><span class="sxs-lookup"><span data-stu-id="0acd5-207">color-buffer</span></span>                                                                     |
| <span data-ttu-id="0acd5-208">Valeur initiale :</span><span class="sxs-lookup"><span data-stu-id="0acd5-208">Initial value:</span></span>   | <span data-ttu-id="0acd5-209">0</span><span class="sxs-lookup"><span data-stu-id="0acd5-209">0</span></span>                                                                                |
| <span data-ttu-id="0acd5-210">Commande d’extraction :</span><span class="sxs-lookup"><span data-stu-id="0acd5-210">Get command:</span></span>     | [<span data-ttu-id="0acd5-211">**glGetIntegerv**</span><span class="sxs-lookup"><span data-stu-id="0acd5-211">**glGetIntegerv**</span></span>](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) |



 

<span data-ttu-id="0acd5-212"></dd> <dt><span id="GL_DEPTH_TEST"></span><span id="gl_depth_test"></span>\_test de profondeur du GL \_</dt> </span><span class="sxs-lookup"><span data-stu-id="0acd5-212"></dd> <dt><span id="GL_DEPTH_TEST"></span><span id="gl_depth_test"></span>GL\_DEPTH\_TEST</dt> </span></span><dd> 

|                  |                                    |
|------------------|------------------------------------|
| <span data-ttu-id="0acd5-213">Description :</span><span class="sxs-lookup"><span data-stu-id="0acd5-213">Description:</span></span>     | <span data-ttu-id="0acd5-214">Mémoire tampon de profondeur activée</span><span class="sxs-lookup"><span data-stu-id="0acd5-214">Depth buffer enabled</span></span>               |
| <span data-ttu-id="0acd5-215">Groupe d’attributs :</span><span class="sxs-lookup"><span data-stu-id="0acd5-215">Attribute group:</span></span> | <span data-ttu-id="0acd5-216">cache de profondeur/activer</span><span class="sxs-lookup"><span data-stu-id="0acd5-216">depth-buffer/enable</span></span>                |
| <span data-ttu-id="0acd5-217">Valeur initiale :</span><span class="sxs-lookup"><span data-stu-id="0acd5-217">Initial value:</span></span>   | <span data-ttu-id="0acd5-218">GL- \_ faux</span><span class="sxs-lookup"><span data-stu-id="0acd5-218">GL\_FALSE</span></span>                          |
| <span data-ttu-id="0acd5-219">Commande d’extraction :</span><span class="sxs-lookup"><span data-stu-id="0acd5-219">Get command:</span></span>     | [<span data-ttu-id="0acd5-220">**glIsEnabled**</span><span class="sxs-lookup"><span data-stu-id="0acd5-220">**glIsEnabled**</span></span>](glisenabled.md) |



 

<span data-ttu-id="0acd5-221"></dd> <dt><span id="GL_DEPTH_FUNC"></span><span id="gl_depth_func"></span>\_Func de profondeur GL \_</dt> </span><span class="sxs-lookup"><span data-stu-id="0acd5-221"></dd> <dt><span id="GL_DEPTH_FUNC"></span><span id="gl_depth_func"></span>GL\_DEPTH\_FUNC</dt> </span></span><dd> 

|                  |                                                                                  |
|------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="0acd5-222">Description :</span><span class="sxs-lookup"><span data-stu-id="0acd5-222">Description:</span></span>     | <span data-ttu-id="0acd5-223">Fonction de test de la mémoire tampon de profondeur</span><span class="sxs-lookup"><span data-stu-id="0acd5-223">Depth buffer test function</span></span>                                                       |
| <span data-ttu-id="0acd5-224">Groupe d’attributs :</span><span class="sxs-lookup"><span data-stu-id="0acd5-224">Attribute group:</span></span> | <span data-ttu-id="0acd5-225">mémoire tampon de profondeur</span><span class="sxs-lookup"><span data-stu-id="0acd5-225">depth-buffer</span></span>                                                                     |
| <span data-ttu-id="0acd5-226">Valeur initiale :</span><span class="sxs-lookup"><span data-stu-id="0acd5-226">Initial value:</span></span>   | <span data-ttu-id="0acd5-227">GL \_ moins</span><span class="sxs-lookup"><span data-stu-id="0acd5-227">GL\_LESS</span></span>                                                                         |
| <span data-ttu-id="0acd5-228">Commande d’extraction :</span><span class="sxs-lookup"><span data-stu-id="0acd5-228">Get command:</span></span>     | [<span data-ttu-id="0acd5-229">**glGetIntegerv**</span><span class="sxs-lookup"><span data-stu-id="0acd5-229">**glGetIntegerv**</span></span>](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) |



 

<span data-ttu-id="0acd5-230"></dd> <dt><span id="GL_BLEND"></span><span id="gl_blend"></span>fusion du GL \_</dt> </span><span class="sxs-lookup"><span data-stu-id="0acd5-230"></dd> <dt><span id="GL_BLEND"></span><span id="gl_blend"></span>GL\_BLEND</dt> </span></span><dd> 

|                  |                                    |
|------------------|------------------------------------|
| <span data-ttu-id="0acd5-231">Description :</span><span class="sxs-lookup"><span data-stu-id="0acd5-231">Description:</span></span>     | <span data-ttu-id="0acd5-232">Fusion activée</span><span class="sxs-lookup"><span data-stu-id="0acd5-232">Blending enabled</span></span>                   |
| <span data-ttu-id="0acd5-233">Groupe d’attributs :</span><span class="sxs-lookup"><span data-stu-id="0acd5-233">Attribute group:</span></span> | <span data-ttu-id="0acd5-234">mémoire tampon de couleur/activation</span><span class="sxs-lookup"><span data-stu-id="0acd5-234">color-buffer/enable</span></span>                |
| <span data-ttu-id="0acd5-235">Valeur initiale :</span><span class="sxs-lookup"><span data-stu-id="0acd5-235">Initial value:</span></span>   | <span data-ttu-id="0acd5-236">GL- \_ faux</span><span class="sxs-lookup"><span data-stu-id="0acd5-236">GL\_FALSE</span></span>                          |
| <span data-ttu-id="0acd5-237">Commande d’extraction :</span><span class="sxs-lookup"><span data-stu-id="0acd5-237">Get command:</span></span>     | [<span data-ttu-id="0acd5-238">**glIsEnabled**</span><span class="sxs-lookup"><span data-stu-id="0acd5-238">**glIsEnabled**</span></span>](glisenabled.md) |



 

<span data-ttu-id="0acd5-239"></dd> <dt><span id="GL_BLENC_SRC"></span><span id="gl_blenc_src"></span>\_BLENC \_ source GL</dt> </span><span class="sxs-lookup"><span data-stu-id="0acd5-239"></dd> <dt><span id="GL_BLENC_SRC"></span><span id="gl_blenc_src"></span>GL\_BLENC\_SRC</dt> </span></span><dd> 

|                  |                                                                                  |
|------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="0acd5-240">Description :</span><span class="sxs-lookup"><span data-stu-id="0acd5-240">Description:</span></span>     | <span data-ttu-id="0acd5-241">Fusion de la fonction source</span><span class="sxs-lookup"><span data-stu-id="0acd5-241">Blending source function</span></span>                                                         |
| <span data-ttu-id="0acd5-242">Groupe d’attributs :</span><span class="sxs-lookup"><span data-stu-id="0acd5-242">Attribute group:</span></span> | <span data-ttu-id="0acd5-243">mémoire tampon de couleur</span><span class="sxs-lookup"><span data-stu-id="0acd5-243">color-buffer</span></span>                                                                     |
| <span data-ttu-id="0acd5-244">Valeur initiale :</span><span class="sxs-lookup"><span data-stu-id="0acd5-244">Initial value:</span></span>   | <span data-ttu-id="0acd5-245">GL \_ 1</span><span class="sxs-lookup"><span data-stu-id="0acd5-245">GL\_ONE</span></span>                                                                          |
| <span data-ttu-id="0acd5-246">Commande d’extraction :</span><span class="sxs-lookup"><span data-stu-id="0acd5-246">Get command:</span></span>     | [<span data-ttu-id="0acd5-247">**glGetIntegerv**</span><span class="sxs-lookup"><span data-stu-id="0acd5-247">**glGetIntegerv**</span></span>](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) |



 

<span data-ttu-id="0acd5-248"></dd> <dt><span id="GL_BLEND_DST"></span><span id="gl_blend_dst"></span>heure d’été du GL de \_ fusion \_</dt> </span><span class="sxs-lookup"><span data-stu-id="0acd5-248"></dd> <dt><span id="GL_BLEND_DST"></span><span id="gl_blend_dst"></span>GL\_BLEND\_DST</dt> </span></span><dd> 

|                  |                                                                                  |
|------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="0acd5-249">Description :</span><span class="sxs-lookup"><span data-stu-id="0acd5-249">Description:</span></span>     | <span data-ttu-id="0acd5-250">Fusion de la fonction destination</span><span class="sxs-lookup"><span data-stu-id="0acd5-250">Blending destination function</span></span>                                                    |
| <span data-ttu-id="0acd5-251">Groupe d’attributs :</span><span class="sxs-lookup"><span data-stu-id="0acd5-251">Attribute group:</span></span> | <span data-ttu-id="0acd5-252">mémoire tampon de couleur</span><span class="sxs-lookup"><span data-stu-id="0acd5-252">color-buffer</span></span>                                                                     |
| <span data-ttu-id="0acd5-253">Valeur initiale :</span><span class="sxs-lookup"><span data-stu-id="0acd5-253">Initial value:</span></span>   | <span data-ttu-id="0acd5-254">\_zéro GL</span><span class="sxs-lookup"><span data-stu-id="0acd5-254">GL\_ZERO</span></span>                                                                         |
| <span data-ttu-id="0acd5-255">Commande d’extraction :</span><span class="sxs-lookup"><span data-stu-id="0acd5-255">Get command:</span></span>     | [<span data-ttu-id="0acd5-256">**glGetIntegerv**</span><span class="sxs-lookup"><span data-stu-id="0acd5-256">**glGetIntegerv**</span></span>](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) |



 

<span data-ttu-id="0acd5-257"></dd> <dt><span id="GL_DITHER"></span><span id="gl_dither"></span>\_tramage GL</dt> </span><span class="sxs-lookup"><span data-stu-id="0acd5-257"></dd> <dt><span id="GL_DITHER"></span><span id="gl_dither"></span>GL\_DITHER</dt> </span></span><dd> 

|                  |                                    |
|------------------|------------------------------------|
| <span data-ttu-id="0acd5-258">Description :</span><span class="sxs-lookup"><span data-stu-id="0acd5-258">Description:</span></span>     | <span data-ttu-id="0acd5-259">Tramage activé</span><span class="sxs-lookup"><span data-stu-id="0acd5-259">Dithering enabled</span></span>                  |
| <span data-ttu-id="0acd5-260">Groupe d’attributs :</span><span class="sxs-lookup"><span data-stu-id="0acd5-260">Attribute group:</span></span> | <span data-ttu-id="0acd5-261">mémoire tampon de couleur/activation</span><span class="sxs-lookup"><span data-stu-id="0acd5-261">color-buffer/enable</span></span>                |
| <span data-ttu-id="0acd5-262">Valeur initiale :</span><span class="sxs-lookup"><span data-stu-id="0acd5-262">Initial value:</span></span>   | <span data-ttu-id="0acd5-263">GL \_ true</span><span class="sxs-lookup"><span data-stu-id="0acd5-263">GL\_TRUE</span></span>                           |
| <span data-ttu-id="0acd5-264">Commande d’extraction :</span><span class="sxs-lookup"><span data-stu-id="0acd5-264">Get command:</span></span>     | [<span data-ttu-id="0acd5-265">**glIsEnabled**</span><span class="sxs-lookup"><span data-stu-id="0acd5-265">**glIsEnabled**</span></span>](glisenabled.md) |



 

<span data-ttu-id="0acd5-266"></dd> <dt><span id="GL_LOGIC_OP"></span><span id="gl_logic_op"></span>GL \_ logique \_ op</dt> </span><span class="sxs-lookup"><span data-stu-id="0acd5-266"></dd> <dt><span id="GL_LOGIC_OP"></span><span id="gl_logic_op"></span>GL\_LOGIC\_OP</dt> </span></span><dd> 

|                  |                                    |
|------------------|------------------------------------|
| <span data-ttu-id="0acd5-267">Description :</span><span class="sxs-lookup"><span data-stu-id="0acd5-267">Description:</span></span>     | <span data-ttu-id="0acd5-268">Opération logique activée</span><span class="sxs-lookup"><span data-stu-id="0acd5-268">Logical operation enabled</span></span>          |
| <span data-ttu-id="0acd5-269">Groupe d’attributs :</span><span class="sxs-lookup"><span data-stu-id="0acd5-269">Attribute group:</span></span> | <span data-ttu-id="0acd5-270">mémoire tampon de couleur/activation</span><span class="sxs-lookup"><span data-stu-id="0acd5-270">color-buffer/enable</span></span>                |
| <span data-ttu-id="0acd5-271">Valeur initiale :</span><span class="sxs-lookup"><span data-stu-id="0acd5-271">Initial value:</span></span>   | <span data-ttu-id="0acd5-272">GL- \_ faux</span><span class="sxs-lookup"><span data-stu-id="0acd5-272">GL\_FALSE</span></span>                          |
| <span data-ttu-id="0acd5-273">Commande d’extraction :</span><span class="sxs-lookup"><span data-stu-id="0acd5-273">Get command:</span></span>     | [<span data-ttu-id="0acd5-274">**glIsEnabled**</span><span class="sxs-lookup"><span data-stu-id="0acd5-274">**glIsEnabled**</span></span>](glisenabled.md) |



 

<span data-ttu-id="0acd5-275"></dd> <dt><span id="GL_LOGIC_OP_MODE"></span><span id="gl_logic_op_mode"></span>\_mode logique \_ du \_ GL</dt> </span><span class="sxs-lookup"><span data-stu-id="0acd5-275"></dd> <dt><span id="GL_LOGIC_OP_MODE"></span><span id="gl_logic_op_mode"></span>GL\_LOGIC\_OP\_MODE</dt> </span></span><dd> 

|                  |                                                                                  |
|------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="0acd5-276">Description :</span><span class="sxs-lookup"><span data-stu-id="0acd5-276">Description:</span></span>     | <span data-ttu-id="0acd5-277">Fonction d’opération logique</span><span class="sxs-lookup"><span data-stu-id="0acd5-277">Logical operation function</span></span>                                                       |
| <span data-ttu-id="0acd5-278">Groupe d’attributs :</span><span class="sxs-lookup"><span data-stu-id="0acd5-278">Attribute group:</span></span> | <span data-ttu-id="0acd5-279">mémoire tampon de couleur</span><span class="sxs-lookup"><span data-stu-id="0acd5-279">color-buffer</span></span>                                                                     |
| <span data-ttu-id="0acd5-280">Valeur initiale :</span><span class="sxs-lookup"><span data-stu-id="0acd5-280">Initial value:</span></span>   | <span data-ttu-id="0acd5-281">\_copie GL</span><span class="sxs-lookup"><span data-stu-id="0acd5-281">GL\_COPY</span></span>                                                                         |
| <span data-ttu-id="0acd5-282">Commande d’extraction :</span><span class="sxs-lookup"><span data-stu-id="0acd5-282">Get command:</span></span>     | [<span data-ttu-id="0acd5-283">**glGetIntegerv**</span><span class="sxs-lookup"><span data-stu-id="0acd5-283">**glGetIntegerv**</span></span>](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) |



 

</dd> </dl>

 

 




