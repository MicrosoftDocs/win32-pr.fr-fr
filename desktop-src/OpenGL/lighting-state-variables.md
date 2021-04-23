---
title: Variables d’état d’éclairage
description: Variables d’état d’éclairage
ms.assetid: a9fb1e22-5e33-4b46-9c3b-2f64de5dd646
keywords:
- Variables d’état d’éclairage OpenGL
topic_type:
- apiref
api_name:
- Lighting State Variables
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3c5a2d029727f4ff4a9eee353230e0843a39f082
ms.sourcegitcommit: 63753fcfb0afbbe5ec283fb8316e62c2dc950f66
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/22/2021
ms.locfileid: "107909847"
---
# <a name="lighting-state-variables"></a><span data-ttu-id="55664-104">Variables d’état d’éclairage</span><span class="sxs-lookup"><span data-stu-id="55664-104">Lighting State Variables</span></span>

<dl> <span data-ttu-id="55664-105"><dt><span id="GL_LIGHTING"></span><span id="gl_lighting"></span>\_éclairage GL</dt> </span><span class="sxs-lookup"><span data-stu-id="55664-105"><dt><span id="GL_LIGHTING"></span><span id="gl_lighting"></span>GL\_LIGHTING</dt> </span></span><dd> 

| <span data-ttu-id="55664-106">Propriété</span><span class="sxs-lookup"><span data-stu-id="55664-106">Property</span></span> | <span data-ttu-id="55664-107">Valeur</span><span class="sxs-lookup"><span data-stu-id="55664-107">Value</span></span> |
|------------------|------------------------------------|
| <span data-ttu-id="55664-108">Description :</span><span class="sxs-lookup"><span data-stu-id="55664-108">Description:</span></span>     | <span data-ttu-id="55664-109">True si l’éclairage est activé</span><span class="sxs-lookup"><span data-stu-id="55664-109">True if lighting is enabled</span></span>        |
| <span data-ttu-id="55664-110">Groupe d’attributs :</span><span class="sxs-lookup"><span data-stu-id="55664-110">Attribute group:</span></span> | <span data-ttu-id="55664-111">éclairage/activation</span><span class="sxs-lookup"><span data-stu-id="55664-111">lighting/enable</span></span>                    |
| <span data-ttu-id="55664-112">Valeur initiale :</span><span class="sxs-lookup"><span data-stu-id="55664-112">Initial value:</span></span>   | <span data-ttu-id="55664-113">GL- \_ faux</span><span class="sxs-lookup"><span data-stu-id="55664-113">GL\_FALSE</span></span>                          |
| <span data-ttu-id="55664-114">Commande d’extraction :</span><span class="sxs-lookup"><span data-stu-id="55664-114">Get command:</span></span>     | [<span data-ttu-id="55664-115">**glIsEnabled**</span><span class="sxs-lookup"><span data-stu-id="55664-115">**glIsEnabled**</span></span>](glisenabled.md) |



 

<span data-ttu-id="55664-116"></dd> <dt><span id="GL_COLOR_MATERIAL"></span><span id="gl_color_material"></span>\_matériau de couleur GL \_</dt> </span><span class="sxs-lookup"><span data-stu-id="55664-116"></dd> <dt><span id="GL_COLOR_MATERIAL"></span><span id="gl_color_material"></span>GL\_COLOR\_MATERIAL</dt> </span></span><dd> 

| <span data-ttu-id="55664-117">Propriété</span><span class="sxs-lookup"><span data-stu-id="55664-117">Property</span></span> | <span data-ttu-id="55664-118">Valeur</span><span class="sxs-lookup"><span data-stu-id="55664-118">Value</span></span> |
|------------------|------------------------------------|
| <span data-ttu-id="55664-119">Description :</span><span class="sxs-lookup"><span data-stu-id="55664-119">Description:</span></span>     | <span data-ttu-id="55664-120">True si le suivi des couleurs est activé</span><span class="sxs-lookup"><span data-stu-id="55664-120">True if color tracking is enabled</span></span>  |
| <span data-ttu-id="55664-121">Groupe d’attributs :</span><span class="sxs-lookup"><span data-stu-id="55664-121">Attribute group:</span></span> | <span data-ttu-id="55664-122">éclairage</span><span class="sxs-lookup"><span data-stu-id="55664-122">lighting</span></span>                           |
| <span data-ttu-id="55664-123">Valeur initiale :</span><span class="sxs-lookup"><span data-stu-id="55664-123">Initial value:</span></span>   | <span data-ttu-id="55664-124">GL- \_ faux</span><span class="sxs-lookup"><span data-stu-id="55664-124">GL\_FALSE</span></span>                          |
| <span data-ttu-id="55664-125">Commande d’extraction :</span><span class="sxs-lookup"><span data-stu-id="55664-125">Get command:</span></span>     | [<span data-ttu-id="55664-126">**glIsEnabled**</span><span class="sxs-lookup"><span data-stu-id="55664-126">**glIsEnabled**</span></span>](glisenabled.md) |



 

<span data-ttu-id="55664-127"></dd> <dt><span id="GL_COLOR_MATERIAL_PARAMETER"></span><span id="gl_color_material_parameter"></span>\_paramètre de \_ matériau de couleur GL \_</dt> </span><span class="sxs-lookup"><span data-stu-id="55664-127"></dd> <dt><span id="GL_COLOR_MATERIAL_PARAMETER"></span><span id="gl_color_material_parameter"></span>GL\_COLOR\_MATERIAL\_PARAMETER</dt> </span></span><dd> 

| <span data-ttu-id="55664-128">Propriété</span><span class="sxs-lookup"><span data-stu-id="55664-128">Property</span></span> | <span data-ttu-id="55664-129">Valeur</span><span class="sxs-lookup"><span data-stu-id="55664-129">Value</span></span> |
|------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="55664-130">Description :</span><span class="sxs-lookup"><span data-stu-id="55664-130">Description:</span></span>     | <span data-ttu-id="55664-131">Couleur actuelle de suivi des propriétés de matériau</span><span class="sxs-lookup"><span data-stu-id="55664-131">Material properties tracking current color</span></span>                                       |
| <span data-ttu-id="55664-132">Groupe d’attributs :</span><span class="sxs-lookup"><span data-stu-id="55664-132">Attribute group:</span></span> | <span data-ttu-id="55664-133">éclairage</span><span class="sxs-lookup"><span data-stu-id="55664-133">lighting</span></span>                                                                         |
| <span data-ttu-id="55664-134">Valeur initiale :</span><span class="sxs-lookup"><span data-stu-id="55664-134">Initial value:</span></span>   | <span data-ttu-id="55664-135">\_ambiants \_ et \_ DIFFUSes du GL</span><span class="sxs-lookup"><span data-stu-id="55664-135">GL\_AMBIENT\_AND\_DIFFUSE</span></span>                                                        |
| <span data-ttu-id="55664-136">Commande d’extraction :</span><span class="sxs-lookup"><span data-stu-id="55664-136">Get command:</span></span>     | [<span data-ttu-id="55664-137">**glGetIntegerv**</span><span class="sxs-lookup"><span data-stu-id="55664-137">**glGetIntegerv**</span></span>](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) |



 

<span data-ttu-id="55664-138"></dd> <dt><span id="GL_COLOR_MATERIAL_FACE"></span><span id="gl_color_material_face"></span>\_ \_ visage matériel de couleur GL \_</dt> </span><span class="sxs-lookup"><span data-stu-id="55664-138"></dd> <dt><span id="GL_COLOR_MATERIAL_FACE"></span><span id="gl_color_material_face"></span>GL\_COLOR\_MATERIAL\_FACE</dt> </span></span><dd> 

| <span data-ttu-id="55664-139">Propriété</span><span class="sxs-lookup"><span data-stu-id="55664-139">Property</span></span> | <span data-ttu-id="55664-140">Valeur</span><span class="sxs-lookup"><span data-stu-id="55664-140">Value</span></span> |
|------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="55664-141">Description :</span><span class="sxs-lookup"><span data-stu-id="55664-141">Description:</span></span>     | <span data-ttu-id="55664-142">Visages affectés par le suivi des couleurs</span><span class="sxs-lookup"><span data-stu-id="55664-142">Faces affected by color tracking</span></span>                                                 |
| <span data-ttu-id="55664-143">Groupe d’attributs :</span><span class="sxs-lookup"><span data-stu-id="55664-143">Attribute group:</span></span> | <span data-ttu-id="55664-144">éclairage</span><span class="sxs-lookup"><span data-stu-id="55664-144">lighting</span></span>                                                                         |
| <span data-ttu-id="55664-145">Valeur initiale :</span><span class="sxs-lookup"><span data-stu-id="55664-145">Initial value:</span></span>   | <span data-ttu-id="55664-146">\_recto \_ et \_ Back GL</span><span class="sxs-lookup"><span data-stu-id="55664-146">GL\_FRONT\_AND\_BACK</span></span>                                                             |
| <span data-ttu-id="55664-147">Commande d’extraction :</span><span class="sxs-lookup"><span data-stu-id="55664-147">Get command:</span></span>     | [<span data-ttu-id="55664-148">**glGetIntegerv**</span><span class="sxs-lookup"><span data-stu-id="55664-148">**glGetIntegerv**</span></span>](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) |



 

<span data-ttu-id="55664-149"></dd> <dt><span id="GL_AMBIENT"></span><span id="gl_ambient"></span>ambiant du GL \_</dt> </span><span class="sxs-lookup"><span data-stu-id="55664-149"></dd> <dt><span id="GL_AMBIENT"></span><span id="gl_ambient"></span>GL\_AMBIENT</dt> </span></span><dd> 

| <span data-ttu-id="55664-150">Propriété</span><span class="sxs-lookup"><span data-stu-id="55664-150">Property</span></span> | <span data-ttu-id="55664-151">Valeur</span><span class="sxs-lookup"><span data-stu-id="55664-151">Value</span></span> |
|------------------|------------------------------------------|
| <span data-ttu-id="55664-152">Description :</span><span class="sxs-lookup"><span data-stu-id="55664-152">Description:</span></span>     | <span data-ttu-id="55664-153">Couleur du matériau ambiant</span><span class="sxs-lookup"><span data-stu-id="55664-153">Ambient material color</span></span>                   |
| <span data-ttu-id="55664-154">Groupe d’attributs :</span><span class="sxs-lookup"><span data-stu-id="55664-154">Attribute group:</span></span> | <span data-ttu-id="55664-155">éclairage</span><span class="sxs-lookup"><span data-stu-id="55664-155">lighting</span></span>                                 |
| <span data-ttu-id="55664-156">Valeur initiale :</span><span class="sxs-lookup"><span data-stu-id="55664-156">Initial value:</span></span>   | <span data-ttu-id="55664-157">(0,2, 0,2, 0,2, 1,0)</span><span class="sxs-lookup"><span data-stu-id="55664-157">(0.2,0.2,0.2,1.0)</span></span>                        |
| <span data-ttu-id="55664-158">Commande d’extraction :</span><span class="sxs-lookup"><span data-stu-id="55664-158">Get command:</span></span>     | [<span data-ttu-id="55664-159">**glGetMaterialfv**</span><span class="sxs-lookup"><span data-stu-id="55664-159">**glGetMaterialfv**</span></span>](glgetmaterial.md) |



 

<span data-ttu-id="55664-160"></dd> <dt><span id="GL_DIFFUSE"></span><span id="gl_diffuse"></span>\_diffusion GL</dt> </span><span class="sxs-lookup"><span data-stu-id="55664-160"></dd> <dt><span id="GL_DIFFUSE"></span><span id="gl_diffuse"></span>GL\_DIFFUSE</dt> </span></span><dd> 

| <span data-ttu-id="55664-161">Propriété</span><span class="sxs-lookup"><span data-stu-id="55664-161">Property</span></span> | <span data-ttu-id="55664-162">Valeur</span><span class="sxs-lookup"><span data-stu-id="55664-162">Value</span></span> |
|------------------|------------------------------------------|
| <span data-ttu-id="55664-163">Description :</span><span class="sxs-lookup"><span data-stu-id="55664-163">Description:</span></span>     | <span data-ttu-id="55664-164">Couleur du matériau diffus</span><span class="sxs-lookup"><span data-stu-id="55664-164">Diffuse material color</span></span>                   |
| <span data-ttu-id="55664-165">Groupe d’attributs :</span><span class="sxs-lookup"><span data-stu-id="55664-165">Attribute group:</span></span> | <span data-ttu-id="55664-166">éclairage</span><span class="sxs-lookup"><span data-stu-id="55664-166">lighting</span></span>                                 |
| <span data-ttu-id="55664-167">Valeur initiale :</span><span class="sxs-lookup"><span data-stu-id="55664-167">Initial value:</span></span>   | <span data-ttu-id="55664-168">(0,8, 0,8, 0,8, 1,0)</span><span class="sxs-lookup"><span data-stu-id="55664-168">(0.8,0.8,0.8,1.0)</span></span>                        |
| <span data-ttu-id="55664-169">Commande d’extraction :</span><span class="sxs-lookup"><span data-stu-id="55664-169">Get command:</span></span>     | [<span data-ttu-id="55664-170">**glGetMaterialfv**</span><span class="sxs-lookup"><span data-stu-id="55664-170">**glGetMaterialfv**</span></span>](glgetmaterial.md) |



 

<span data-ttu-id="55664-171"></dd> <dt><span id="GL_SPECULAR"></span><span id="gl_specular"></span>\_spéculaire GL</dt> </span><span class="sxs-lookup"><span data-stu-id="55664-171"></dd> <dt><span id="GL_SPECULAR"></span><span id="gl_specular"></span>GL\_SPECULAR</dt> </span></span><dd> 

| <span data-ttu-id="55664-172">Propriété</span><span class="sxs-lookup"><span data-stu-id="55664-172">Property</span></span> | <span data-ttu-id="55664-173">Valeur</span><span class="sxs-lookup"><span data-stu-id="55664-173">Value</span></span> |
|------------------|------------------------------------------|
| <span data-ttu-id="55664-174">Description :</span><span class="sxs-lookup"><span data-stu-id="55664-174">Description:</span></span>     | <span data-ttu-id="55664-175">Couleur de matériau spéculaire</span><span class="sxs-lookup"><span data-stu-id="55664-175">Specular material color</span></span>                  |
| <span data-ttu-id="55664-176">Groupe d’attributs :</span><span class="sxs-lookup"><span data-stu-id="55664-176">Attribute group:</span></span> | <span data-ttu-id="55664-177">éclairage</span><span class="sxs-lookup"><span data-stu-id="55664-177">lighting</span></span>                                 |
| <span data-ttu-id="55664-178">Valeur initiale :</span><span class="sxs-lookup"><span data-stu-id="55664-178">Initial value:</span></span>   | <span data-ttu-id="55664-179">(0.0, 0.0, 0.0, 1.0)</span><span class="sxs-lookup"><span data-stu-id="55664-179">(0.0,0.0,0.0,1.0)</span></span>                        |
| <span data-ttu-id="55664-180">Commande d’extraction :</span><span class="sxs-lookup"><span data-stu-id="55664-180">Get command:</span></span>     | [<span data-ttu-id="55664-181">**glGetMaterialfv**</span><span class="sxs-lookup"><span data-stu-id="55664-181">**glGetMaterialfv**</span></span>](glgetmaterial.md) |



 

<span data-ttu-id="55664-182"></dd> <dt><span id="GL_EMISSION"></span><span id="gl_emission"></span>\_émission GL</dt> </span><span class="sxs-lookup"><span data-stu-id="55664-182"></dd> <dt><span id="GL_EMISSION"></span><span id="gl_emission"></span>GL\_EMISSION</dt> </span></span><dd> 

| <span data-ttu-id="55664-183">Propriété</span><span class="sxs-lookup"><span data-stu-id="55664-183">Property</span></span> | <span data-ttu-id="55664-184">Valeur</span><span class="sxs-lookup"><span data-stu-id="55664-184">Value</span></span> |
|------------------|------------------------------------------|
| <span data-ttu-id="55664-185">Description :</span><span class="sxs-lookup"><span data-stu-id="55664-185">Description:</span></span>     | <span data-ttu-id="55664-186">Couleur de matériau émissif</span><span class="sxs-lookup"><span data-stu-id="55664-186">Emissive material color</span></span>                  |
| <span data-ttu-id="55664-187">Groupe d’attributs :</span><span class="sxs-lookup"><span data-stu-id="55664-187">Attribute group:</span></span> | <span data-ttu-id="55664-188">éclairage</span><span class="sxs-lookup"><span data-stu-id="55664-188">lighting</span></span>                                 |
| <span data-ttu-id="55664-189">Valeur initiale :</span><span class="sxs-lookup"><span data-stu-id="55664-189">Initial value:</span></span>   | <span data-ttu-id="55664-190">(0.0, 0.0, 0.0, 1.0)</span><span class="sxs-lookup"><span data-stu-id="55664-190">(0.0,0.0,0.0,1.0)</span></span>                        |
| <span data-ttu-id="55664-191">Commande d’extraction :</span><span class="sxs-lookup"><span data-stu-id="55664-191">Get command:</span></span>     | [<span data-ttu-id="55664-192">**glGetMaterialfv**</span><span class="sxs-lookup"><span data-stu-id="55664-192">**glGetMaterialfv**</span></span>](glgetmaterial.md) |



 

<span data-ttu-id="55664-193"></dd> <dt><span id="GL_SHININESS"></span><span id="gl_shininess"></span>\_éclat GL</dt> </span><span class="sxs-lookup"><span data-stu-id="55664-193"></dd> <dt><span id="GL_SHININESS"></span><span id="gl_shininess"></span>GL\_SHININESS</dt> </span></span><dd> 

| <span data-ttu-id="55664-194">Propriété</span><span class="sxs-lookup"><span data-stu-id="55664-194">Property</span></span> | <span data-ttu-id="55664-195">Valeur</span><span class="sxs-lookup"><span data-stu-id="55664-195">Value</span></span> |
|------------------|------------------------------------------|
| <span data-ttu-id="55664-196">Description :</span><span class="sxs-lookup"><span data-stu-id="55664-196">Description:</span></span>     | <span data-ttu-id="55664-197">Exposant spéculaire du matériau</span><span class="sxs-lookup"><span data-stu-id="55664-197">Specular exponent of material</span></span>            |
| <span data-ttu-id="55664-198">Groupe d’attributs :</span><span class="sxs-lookup"><span data-stu-id="55664-198">Attribute group:</span></span> | <span data-ttu-id="55664-199">éclairage</span><span class="sxs-lookup"><span data-stu-id="55664-199">lighting</span></span>                                 |
| <span data-ttu-id="55664-200">Valeur initiale :</span><span class="sxs-lookup"><span data-stu-id="55664-200">Initial value:</span></span>   | <span data-ttu-id="55664-201">0.0</span><span class="sxs-lookup"><span data-stu-id="55664-201">0.0</span></span>                                      |
| <span data-ttu-id="55664-202">Commande d’extraction :</span><span class="sxs-lookup"><span data-stu-id="55664-202">Get command:</span></span>     | [<span data-ttu-id="55664-203">**glGetMaterialfv**</span><span class="sxs-lookup"><span data-stu-id="55664-203">**glGetMaterialfv**</span></span>](glgetmaterial.md) |



 

<span data-ttu-id="55664-204"></dd> <dt><span id="GL_LIGHT_MODEL_AMBIENT"></span><span id="gl_light_model_ambient"></span>ambiant (GL \_ Light \_ Model) \_</dt> </span><span class="sxs-lookup"><span data-stu-id="55664-204"></dd> <dt><span id="GL_LIGHT_MODEL_AMBIENT"></span><span id="gl_light_model_ambient"></span>GL\_LIGHT\_MODEL\_AMBIENT</dt> </span></span><dd> 

| <span data-ttu-id="55664-205">Propriété</span><span class="sxs-lookup"><span data-stu-id="55664-205">Property</span></span> | <span data-ttu-id="55664-206">Valeur</span><span class="sxs-lookup"><span data-stu-id="55664-206">Value</span></span> |
|------------------|--------------------------------------------------------------------------------|
| <span data-ttu-id="55664-207">Description :</span><span class="sxs-lookup"><span data-stu-id="55664-207">Description:</span></span>     | <span data-ttu-id="55664-208">Couleur de scène ambiante</span><span class="sxs-lookup"><span data-stu-id="55664-208">Ambient scene color</span></span>                                                            |
| <span data-ttu-id="55664-209">Groupe d’attributs :</span><span class="sxs-lookup"><span data-stu-id="55664-209">Attribute group:</span></span> | <span data-ttu-id="55664-210">éclairage</span><span class="sxs-lookup"><span data-stu-id="55664-210">lighting</span></span>                                                                       |
| <span data-ttu-id="55664-211">Valeur initiale :</span><span class="sxs-lookup"><span data-stu-id="55664-211">Initial value:</span></span>   | <span data-ttu-id="55664-212">(0,2, 0,2, 0,2, 1,0)</span><span class="sxs-lookup"><span data-stu-id="55664-212">(0.2,0.2,0.2,1.0)</span></span>                                                              |
| <span data-ttu-id="55664-213">Commande d’extraction :</span><span class="sxs-lookup"><span data-stu-id="55664-213">Get command:</span></span>     | [<span data-ttu-id="55664-214">**glGetFloatv**</span><span class="sxs-lookup"><span data-stu-id="55664-214">**glGetFloatv**</span></span>](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) |



 

<span data-ttu-id="55664-215"></dd> <dt><span id="GL_LIGHT_MODEL_LOCAL_VIEWER"></span><span id="gl_light_model_local_viewer"></span>\_ \_ visionneuse locale du modèle de lumière \_ GL \_</dt> </span><span class="sxs-lookup"><span data-stu-id="55664-215"></dd> <dt><span id="GL_LIGHT_MODEL_LOCAL_VIEWER"></span><span id="gl_light_model_local_viewer"></span>GL\_LIGHT\_MODEL\_LOCAL\_VIEWER</dt> </span></span><dd> 

| <span data-ttu-id="55664-216">Propriété</span><span class="sxs-lookup"><span data-stu-id="55664-216">Property</span></span> | <span data-ttu-id="55664-217">Valeur</span><span class="sxs-lookup"><span data-stu-id="55664-217">Value</span></span> |
|------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="55664-218">Description :</span><span class="sxs-lookup"><span data-stu-id="55664-218">Description:</span></span>     | <span data-ttu-id="55664-219">La visionneuse est locale</span><span class="sxs-lookup"><span data-stu-id="55664-219">Viewer is local</span></span>                                                                  |
| <span data-ttu-id="55664-220">Groupe d’attributs :</span><span class="sxs-lookup"><span data-stu-id="55664-220">Attribute group:</span></span> | <span data-ttu-id="55664-221">éclairage</span><span class="sxs-lookup"><span data-stu-id="55664-221">lighting</span></span>                                                                         |
| <span data-ttu-id="55664-222">Valeur initiale :</span><span class="sxs-lookup"><span data-stu-id="55664-222">Initial value:</span></span>   | <span data-ttu-id="55664-223">GL- \_ faux</span><span class="sxs-lookup"><span data-stu-id="55664-223">GL\_FALSE</span></span>                                                                        |
| <span data-ttu-id="55664-224">Commande d’extraction :</span><span class="sxs-lookup"><span data-stu-id="55664-224">Get command:</span></span>     | [<span data-ttu-id="55664-225">**glGetBooleanv**</span><span class="sxs-lookup"><span data-stu-id="55664-225">**glGetBooleanv**</span></span>](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) |



 

<span data-ttu-id="55664-226"></dd> <dt><span id="GL_LIGHT_MODEL_TWO_SIDE"></span><span id="gl_light_model_two_side"></span>\_ \_ côté 2 du modèle GL clair \_ \_</dt> </span><span class="sxs-lookup"><span data-stu-id="55664-226"></dd> <dt><span id="GL_LIGHT_MODEL_TWO_SIDE"></span><span id="gl_light_model_two_side"></span>GL\_LIGHT\_MODEL\_TWO\_SIDE</dt> </span></span><dd> 

| <span data-ttu-id="55664-227">Propriété</span><span class="sxs-lookup"><span data-stu-id="55664-227">Property</span></span> | <span data-ttu-id="55664-228">Valeur</span><span class="sxs-lookup"><span data-stu-id="55664-228">Value</span></span> |
|------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="55664-229">Description :</span><span class="sxs-lookup"><span data-stu-id="55664-229">Description:</span></span>     | <span data-ttu-id="55664-230">Utiliser l’éclairage à deux côtés</span><span class="sxs-lookup"><span data-stu-id="55664-230">Use two-sided lighting</span></span>                                                           |
| <span data-ttu-id="55664-231">Groupe d’attributs :</span><span class="sxs-lookup"><span data-stu-id="55664-231">Attribute group:</span></span> | <span data-ttu-id="55664-232">éclairage</span><span class="sxs-lookup"><span data-stu-id="55664-232">lighting</span></span>                                                                         |
| <span data-ttu-id="55664-233">Valeur initiale :</span><span class="sxs-lookup"><span data-stu-id="55664-233">Initial value:</span></span>   | <span data-ttu-id="55664-234">GL- \_ faux</span><span class="sxs-lookup"><span data-stu-id="55664-234">GL\_FALSE</span></span>                                                                        |
| <span data-ttu-id="55664-235">Commande d’extraction :</span><span class="sxs-lookup"><span data-stu-id="55664-235">Get command:</span></span>     | [<span data-ttu-id="55664-236">**glGetBooleanv**</span><span class="sxs-lookup"><span data-stu-id="55664-236">**glGetBooleanv**</span></span>](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) |



 

<span data-ttu-id="55664-237"></dd> <dt><span id="GL_AMBIENT"></span><span id="gl_ambient"></span>ambiant du GL \_</dt> </span><span class="sxs-lookup"><span data-stu-id="55664-237"></dd> <dt><span id="GL_AMBIENT"></span><span id="gl_ambient"></span>GL\_AMBIENT</dt> </span></span><dd> 

| <span data-ttu-id="55664-238">Propriété</span><span class="sxs-lookup"><span data-stu-id="55664-238">Property</span></span> | <span data-ttu-id="55664-239">Valeur</span><span class="sxs-lookup"><span data-stu-id="55664-239">Value</span></span> |
|------------------|------------------------------------|
| <span data-ttu-id="55664-240">Description :</span><span class="sxs-lookup"><span data-stu-id="55664-240">Description:</span></span>     | <span data-ttu-id="55664-241">Intensité ambiante de la lumière *i*</span><span class="sxs-lookup"><span data-stu-id="55664-241">Ambient intensity of light *i*</span></span>     |
| <span data-ttu-id="55664-242">Groupe d’attributs :</span><span class="sxs-lookup"><span data-stu-id="55664-242">Attribute group:</span></span> | <span data-ttu-id="55664-243">éclairage</span><span class="sxs-lookup"><span data-stu-id="55664-243">lighting</span></span>                           |
| <span data-ttu-id="55664-244">Valeur initiale :</span><span class="sxs-lookup"><span data-stu-id="55664-244">Initial value:</span></span>   | <span data-ttu-id="55664-245">(0.0, 0.0, 0.0, 1.0)</span><span class="sxs-lookup"><span data-stu-id="55664-245">(0.0,0.0,0.0,1.0)</span></span>                  |
| <span data-ttu-id="55664-246">Commande d’extraction :</span><span class="sxs-lookup"><span data-stu-id="55664-246">Get command:</span></span>     | [<span data-ttu-id="55664-247">**glGetLightfv**</span><span class="sxs-lookup"><span data-stu-id="55664-247">**glGetLightfv**</span></span>](glgetlight.md) |



 

<span data-ttu-id="55664-248"></dd> <dt><span id="GL_DIFFUSE"></span><span id="gl_diffuse"></span>\_diffusion GL</dt> </span><span class="sxs-lookup"><span data-stu-id="55664-248"></dd> <dt><span id="GL_DIFFUSE"></span><span id="gl_diffuse"></span>GL\_DIFFUSE</dt> </span></span><dd> 

| <span data-ttu-id="55664-249">Propriété</span><span class="sxs-lookup"><span data-stu-id="55664-249">Property</span></span> | <span data-ttu-id="55664-250">Valeur</span><span class="sxs-lookup"><span data-stu-id="55664-250">Value</span></span> |
|------------------|------------------------------------|
| <span data-ttu-id="55664-251">Description :</span><span class="sxs-lookup"><span data-stu-id="55664-251">Description:</span></span>     | <span data-ttu-id="55664-252">Intensité diffuse de la lumière *i*</span><span class="sxs-lookup"><span data-stu-id="55664-252">Diffuse intensity of light *i*</span></span>     |
| <span data-ttu-id="55664-253">Groupe d’attributs :</span><span class="sxs-lookup"><span data-stu-id="55664-253">Attribute group:</span></span> | <span data-ttu-id="55664-254">éclairage</span><span class="sxs-lookup"><span data-stu-id="55664-254">lighting</span></span>                           |
| <span data-ttu-id="55664-255">Valeur initiale :</span><span class="sxs-lookup"><span data-stu-id="55664-255">Initial value:</span></span>   |                                    |
| <span data-ttu-id="55664-256">Commande d’extraction :</span><span class="sxs-lookup"><span data-stu-id="55664-256">Get command:</span></span>     | [<span data-ttu-id="55664-257">**glGetLightfv**</span><span class="sxs-lookup"><span data-stu-id="55664-257">**glGetLightfv**</span></span>](glgetlight.md) |



 

<span data-ttu-id="55664-258"></dd> <dt><span id="GL_SPECULAR"></span><span id="gl_specular"></span>\_spéculaire GL</dt> </span><span class="sxs-lookup"><span data-stu-id="55664-258"></dd> <dt><span id="GL_SPECULAR"></span><span id="gl_specular"></span>GL\_SPECULAR</dt> </span></span><dd> 

| <span data-ttu-id="55664-259">Propriété</span><span class="sxs-lookup"><span data-stu-id="55664-259">Property</span></span> | <span data-ttu-id="55664-260">Valeur</span><span class="sxs-lookup"><span data-stu-id="55664-260">Value</span></span> |
|------------------|------------------------------------|
| <span data-ttu-id="55664-261">Description :</span><span class="sxs-lookup"><span data-stu-id="55664-261">Description:</span></span>     | <span data-ttu-id="55664-262">Intensité spéculaire de la lumière *i*</span><span class="sxs-lookup"><span data-stu-id="55664-262">Specular intensity of light *i*</span></span>    |
| <span data-ttu-id="55664-263">Groupe d’attributs :</span><span class="sxs-lookup"><span data-stu-id="55664-263">Attribute group:</span></span> | <span data-ttu-id="55664-264">éclairage</span><span class="sxs-lookup"><span data-stu-id="55664-264">lighting</span></span>                           |
| <span data-ttu-id="55664-265">Valeur initiale :</span><span class="sxs-lookup"><span data-stu-id="55664-265">Initial value:</span></span>   |                                    |
| <span data-ttu-id="55664-266">Commande d’extraction :</span><span class="sxs-lookup"><span data-stu-id="55664-266">Get command:</span></span>     | [<span data-ttu-id="55664-267">**glGetLightfv**</span><span class="sxs-lookup"><span data-stu-id="55664-267">**glGetLightfv**</span></span>](glgetlight.md) |



 

<span data-ttu-id="55664-268"></dd> <dt><span id="GL_POSITION"></span><span id="gl_position"></span>\_position GL</dt> </span><span class="sxs-lookup"><span data-stu-id="55664-268"></dd> <dt><span id="GL_POSITION"></span><span id="gl_position"></span>GL\_POSITION</dt> </span></span><dd> 

| <span data-ttu-id="55664-269">Propriété</span><span class="sxs-lookup"><span data-stu-id="55664-269">Property</span></span> | <span data-ttu-id="55664-270">Valeur</span><span class="sxs-lookup"><span data-stu-id="55664-270">Value</span></span> |
|------------------|------------------------------------|
| <span data-ttu-id="55664-271">Description :</span><span class="sxs-lookup"><span data-stu-id="55664-271">Description:</span></span>     | <span data-ttu-id="55664-272">Position de la lumière *i*</span><span class="sxs-lookup"><span data-stu-id="55664-272">Position of light *i*</span></span>              |
| <span data-ttu-id="55664-273">Groupe d’attributs :</span><span class="sxs-lookup"><span data-stu-id="55664-273">Attribute group:</span></span> | <span data-ttu-id="55664-274">éclairage</span><span class="sxs-lookup"><span data-stu-id="55664-274">lighting</span></span>                           |
| <span data-ttu-id="55664-275">Valeur initiale :</span><span class="sxs-lookup"><span data-stu-id="55664-275">Initial value:</span></span>   | <span data-ttu-id="55664-276">(0.0, 0.0, 1.0, 0.0)</span><span class="sxs-lookup"><span data-stu-id="55664-276">(0.0,0.0,1.0,0.0)</span></span>                  |
| <span data-ttu-id="55664-277">Commande d’extraction :</span><span class="sxs-lookup"><span data-stu-id="55664-277">Get command:</span></span>     | [<span data-ttu-id="55664-278">**glGetLightfv**</span><span class="sxs-lookup"><span data-stu-id="55664-278">**glGetLightfv**</span></span>](glgetlight.md) |



 

<span data-ttu-id="55664-279"></dd> <dt><span id="GL_CONSTANT_ATTENUATION"></span><span id="gl_constant_attenuation"></span>\_atténuation constante du GL \_</dt> </span><span class="sxs-lookup"><span data-stu-id="55664-279"></dd> <dt><span id="GL_CONSTANT_ATTENUATION"></span><span id="gl_constant_attenuation"></span>GL\_CONSTANT\_ATTENUATION</dt> </span></span><dd> 

| <span data-ttu-id="55664-280">Propriété</span><span class="sxs-lookup"><span data-stu-id="55664-280">Property</span></span> | <span data-ttu-id="55664-281">Valeur</span><span class="sxs-lookup"><span data-stu-id="55664-281">Value</span></span> |
|------------------|------------------------------------|
| <span data-ttu-id="55664-282">Description :</span><span class="sxs-lookup"><span data-stu-id="55664-282">Description:</span></span>     | <span data-ttu-id="55664-283">Facteur d’atténuation constant</span><span class="sxs-lookup"><span data-stu-id="55664-283">Constant attenuation factor</span></span>        |
| <span data-ttu-id="55664-284">Groupe d’attributs :</span><span class="sxs-lookup"><span data-stu-id="55664-284">Attribute group:</span></span> | <span data-ttu-id="55664-285">éclairage</span><span class="sxs-lookup"><span data-stu-id="55664-285">lighting</span></span>                           |
| <span data-ttu-id="55664-286">Valeur initiale :</span><span class="sxs-lookup"><span data-stu-id="55664-286">Initial value:</span></span>   | <span data-ttu-id="55664-287">1.0</span><span class="sxs-lookup"><span data-stu-id="55664-287">1.0</span></span>                                |
| <span data-ttu-id="55664-288">Commande d’extraction :</span><span class="sxs-lookup"><span data-stu-id="55664-288">Get command:</span></span>     | [<span data-ttu-id="55664-289">**glGetLightfv**</span><span class="sxs-lookup"><span data-stu-id="55664-289">**glGetLightfv**</span></span>](glgetlight.md) |



 

<span data-ttu-id="55664-290"></dd> <dt><span id="GL_LINEAR_ATTENUATION"></span><span id="gl_linear_attenuation"></span>\_atténuation linéaire du GL \_</dt> </span><span class="sxs-lookup"><span data-stu-id="55664-290"></dd> <dt><span id="GL_LINEAR_ATTENUATION"></span><span id="gl_linear_attenuation"></span>GL\_LINEAR\_ATTENUATION</dt> </span></span><dd> 

| <span data-ttu-id="55664-291">Propriété</span><span class="sxs-lookup"><span data-stu-id="55664-291">Property</span></span> | <span data-ttu-id="55664-292">Valeur</span><span class="sxs-lookup"><span data-stu-id="55664-292">Value</span></span> |
|------------------|------------------------------------|
| <span data-ttu-id="55664-293">Description :</span><span class="sxs-lookup"><span data-stu-id="55664-293">Description:</span></span>     | <span data-ttu-id="55664-294">Facteur d’atténuation linéaire</span><span class="sxs-lookup"><span data-stu-id="55664-294">Linear attenuation factor</span></span>          |
| <span data-ttu-id="55664-295">Groupe d’attributs :</span><span class="sxs-lookup"><span data-stu-id="55664-295">Attribute group:</span></span> | <span data-ttu-id="55664-296">éclairage</span><span class="sxs-lookup"><span data-stu-id="55664-296">lighting</span></span>                           |
| <span data-ttu-id="55664-297">Valeur initiale :</span><span class="sxs-lookup"><span data-stu-id="55664-297">Initial value:</span></span>   | <span data-ttu-id="55664-298">0.0</span><span class="sxs-lookup"><span data-stu-id="55664-298">0.0</span></span>                                |
| <span data-ttu-id="55664-299">Commande d’extraction :</span><span class="sxs-lookup"><span data-stu-id="55664-299">Get command:</span></span>     | [<span data-ttu-id="55664-300">**glGetLightfv**</span><span class="sxs-lookup"><span data-stu-id="55664-300">**glGetLightfv**</span></span>](glgetlight.md) |



 

<span data-ttu-id="55664-301"></dd> <dt><span id="GL_QUADRATIC_ATTENUATION"></span><span id="gl_quadratic_attenuation"></span>\_atténuation quadratique du \_ GL</dt> </span><span class="sxs-lookup"><span data-stu-id="55664-301"></dd> <dt><span id="GL_QUADRATIC_ATTENUATION"></span><span id="gl_quadratic_attenuation"></span>GL\_QUADRATIC\_ATTENUATION</dt> </span></span><dd> 

| <span data-ttu-id="55664-302">Propriété</span><span class="sxs-lookup"><span data-stu-id="55664-302">Property</span></span> | <span data-ttu-id="55664-303">Valeur</span><span class="sxs-lookup"><span data-stu-id="55664-303">Value</span></span> |
|------------------|------------------------------------|
| <span data-ttu-id="55664-304">Description :</span><span class="sxs-lookup"><span data-stu-id="55664-304">Description:</span></span>     | <span data-ttu-id="55664-305">Facteur d’atténuation quadratique</span><span class="sxs-lookup"><span data-stu-id="55664-305">Quadratic attenuation factor</span></span>       |
| <span data-ttu-id="55664-306">Groupe d’attributs :</span><span class="sxs-lookup"><span data-stu-id="55664-306">Attribute group:</span></span> | <span data-ttu-id="55664-307">éclairage</span><span class="sxs-lookup"><span data-stu-id="55664-307">lighting</span></span>                           |
| <span data-ttu-id="55664-308">Valeur initiale :</span><span class="sxs-lookup"><span data-stu-id="55664-308">Initial value:</span></span>   | <span data-ttu-id="55664-309">0.0</span><span class="sxs-lookup"><span data-stu-id="55664-309">0.0</span></span>                                |
| <span data-ttu-id="55664-310">Commande d’extraction :</span><span class="sxs-lookup"><span data-stu-id="55664-310">Get command:</span></span>     | [<span data-ttu-id="55664-311">**glGetLightfv**</span><span class="sxs-lookup"><span data-stu-id="55664-311">**glGetLightfv**</span></span>](glgetlight.md) |



 

<span data-ttu-id="55664-312"></dd> <dt><span id="GL_SPOT_DIRECTION"></span><span id="gl_spot_direction"></span>\_sens du spot GL \_</dt> </span><span class="sxs-lookup"><span data-stu-id="55664-312"></dd> <dt><span id="GL_SPOT_DIRECTION"></span><span id="gl_spot_direction"></span>GL\_SPOT\_DIRECTION</dt> </span></span><dd> 

| <span data-ttu-id="55664-313">Propriété</span><span class="sxs-lookup"><span data-stu-id="55664-313">Property</span></span> | <span data-ttu-id="55664-314">Valeur</span><span class="sxs-lookup"><span data-stu-id="55664-314">Value</span></span> |
|------------------|------------------------------------|
| <span data-ttu-id="55664-315">Description :</span><span class="sxs-lookup"><span data-stu-id="55664-315">Description:</span></span>     | <span data-ttu-id="55664-316">Direction Spotlight de la lumière *i*</span><span class="sxs-lookup"><span data-stu-id="55664-316">Spotlight direction of light *i*</span></span>   |
| <span data-ttu-id="55664-317">Groupe d’attributs :</span><span class="sxs-lookup"><span data-stu-id="55664-317">Attribute group:</span></span> | <span data-ttu-id="55664-318">éclairage</span><span class="sxs-lookup"><span data-stu-id="55664-318">lighting</span></span>                           |
| <span data-ttu-id="55664-319">Valeur initiale :</span><span class="sxs-lookup"><span data-stu-id="55664-319">Initial value:</span></span>   | <span data-ttu-id="55664-320">(0.0, 0.0,-1,0)</span><span class="sxs-lookup"><span data-stu-id="55664-320">(0.0,0.0,-1.0)</span></span>                     |
| <span data-ttu-id="55664-321">Commande d’extraction :</span><span class="sxs-lookup"><span data-stu-id="55664-321">Get command:</span></span>     | [<span data-ttu-id="55664-322">**glGetLightfv**</span><span class="sxs-lookup"><span data-stu-id="55664-322">**glGetLightfv**</span></span>](glgetlight.md) |



 

<span data-ttu-id="55664-323"></dd> <dt><span id="GL_SPOT_EXPONENT"></span><span id="gl_spot_exponent"></span>exposant de point comptable \_ \_</dt> </span><span class="sxs-lookup"><span data-stu-id="55664-323"></dd> <dt><span id="GL_SPOT_EXPONENT"></span><span id="gl_spot_exponent"></span>GL\_SPOT\_EXPONENT</dt> </span></span><dd> 

| <span data-ttu-id="55664-324">Propriété</span><span class="sxs-lookup"><span data-stu-id="55664-324">Property</span></span> | <span data-ttu-id="55664-325">Valeur</span><span class="sxs-lookup"><span data-stu-id="55664-325">Value</span></span> |
|------------------|------------------------------------|
| <span data-ttu-id="55664-326">Description :</span><span class="sxs-lookup"><span data-stu-id="55664-326">Description:</span></span>     | <span data-ttu-id="55664-327">Exposant Gong de la lumière *i*</span><span class="sxs-lookup"><span data-stu-id="55664-327">Spotlight exponent of light *i*</span></span>    |
| <span data-ttu-id="55664-328">Groupe d’attributs :</span><span class="sxs-lookup"><span data-stu-id="55664-328">Attribute group:</span></span> | <span data-ttu-id="55664-329">éclairage</span><span class="sxs-lookup"><span data-stu-id="55664-329">lighting</span></span>                           |
| <span data-ttu-id="55664-330">Valeur initiale :</span><span class="sxs-lookup"><span data-stu-id="55664-330">Initial value:</span></span>   | <span data-ttu-id="55664-331">0.0</span><span class="sxs-lookup"><span data-stu-id="55664-331">0.0</span></span>                                |
| <span data-ttu-id="55664-332">Commande d’extraction :</span><span class="sxs-lookup"><span data-stu-id="55664-332">Get command:</span></span>     | [<span data-ttu-id="55664-333">**glGetLightfv**</span><span class="sxs-lookup"><span data-stu-id="55664-333">**glGetLightfv**</span></span>](glgetlight.md) |



 

<span data-ttu-id="55664-334"></dd> <dt><span id="GL_SPOT_CUTOFF"></span><span id="gl_spot_cutoff"></span>coupure de l' \_ emplacement GL \_</dt> </span><span class="sxs-lookup"><span data-stu-id="55664-334"></dd> <dt><span id="GL_SPOT_CUTOFF"></span><span id="gl_spot_cutoff"></span>GL\_SPOT\_CUTOFF</dt> </span></span><dd> 

| <span data-ttu-id="55664-335">Propriété</span><span class="sxs-lookup"><span data-stu-id="55664-335">Property</span></span> | <span data-ttu-id="55664-336">Valeur</span><span class="sxs-lookup"><span data-stu-id="55664-336">Value</span></span> |
|------------------|------------------------------------|
| <span data-ttu-id="55664-337">Description :</span><span class="sxs-lookup"><span data-stu-id="55664-337">Description:</span></span>     | <span data-ttu-id="55664-338">Angle Spotlight de la lumière *i*</span><span class="sxs-lookup"><span data-stu-id="55664-338">Spotlight angle of light *i*</span></span>       |
| <span data-ttu-id="55664-339">Groupe d’attributs :</span><span class="sxs-lookup"><span data-stu-id="55664-339">Attribute group:</span></span> | <span data-ttu-id="55664-340">éclairage</span><span class="sxs-lookup"><span data-stu-id="55664-340">lighting</span></span>                           |
| <span data-ttu-id="55664-341">Valeur initiale :</span><span class="sxs-lookup"><span data-stu-id="55664-341">Initial value:</span></span>   | <span data-ttu-id="55664-342">180,0</span><span class="sxs-lookup"><span data-stu-id="55664-342">180.0</span></span>                              |
| <span data-ttu-id="55664-343">Commande d’extraction :</span><span class="sxs-lookup"><span data-stu-id="55664-343">Get command:</span></span>     | [<span data-ttu-id="55664-344">**glGetLightfv**</span><span class="sxs-lookup"><span data-stu-id="55664-344">**glGetLightfv**</span></span>](glgetlight.md) |



 

<span data-ttu-id="55664-345"></dd> <dt><span id="GL_LIGHT_i"></span><span id="gl_light_i"></span><span id="GL_LIGHT_I"></span>GL \_ clair *i*</dt> </span><span class="sxs-lookup"><span data-stu-id="55664-345"></dd> <dt><span id="GL_LIGHT_i"></span><span id="gl_light_i"></span><span id="GL_LIGHT_I"></span>GL\_LIGHT *i*</dt> </span></span><dd> 

| <span data-ttu-id="55664-346">Propriété</span><span class="sxs-lookup"><span data-stu-id="55664-346">Property</span></span> | <span data-ttu-id="55664-347">Valeur</span><span class="sxs-lookup"><span data-stu-id="55664-347">Value</span></span> |
|------------------|------------------------------------|
| <span data-ttu-id="55664-348">Description :</span><span class="sxs-lookup"><span data-stu-id="55664-348">Description:</span></span>     | <span data-ttu-id="55664-349">True si l’option Light *i* est activée</span><span class="sxs-lookup"><span data-stu-id="55664-349">True if light *i* enabled</span></span>          |
| <span data-ttu-id="55664-350">Groupe d’attributs :</span><span class="sxs-lookup"><span data-stu-id="55664-350">Attribute group:</span></span> | <span data-ttu-id="55664-351">éclairage/activation</span><span class="sxs-lookup"><span data-stu-id="55664-351">lighting/enable</span></span>                    |
| <span data-ttu-id="55664-352">Valeur initiale :</span><span class="sxs-lookup"><span data-stu-id="55664-352">Initial value:</span></span>   | <span data-ttu-id="55664-353">GL- \_ faux</span><span class="sxs-lookup"><span data-stu-id="55664-353">GL\_FALSE</span></span>                          |
| <span data-ttu-id="55664-354">Commande d’extraction :</span><span class="sxs-lookup"><span data-stu-id="55664-354">Get command:</span></span>     | [<span data-ttu-id="55664-355">**glIsEnabled**</span><span class="sxs-lookup"><span data-stu-id="55664-355">**glIsEnabled**</span></span>](glisenabled.md) |



 

<span data-ttu-id="55664-356"></dd> <dt><span id="GL_COLOR_INDEXES"></span><span id="gl_color_indexes"></span>\_index de couleurs GL \_</dt> </span><span class="sxs-lookup"><span data-stu-id="55664-356"></dd> <dt><span id="GL_COLOR_INDEXES"></span><span id="gl_color_indexes"></span>GL\_COLOR\_INDEXES</dt> </span></span><dd> 

| <span data-ttu-id="55664-357">Propriété</span><span class="sxs-lookup"><span data-stu-id="55664-357">Property</span></span> | <span data-ttu-id="55664-358">Valeur</span><span class="sxs-lookup"><span data-stu-id="55664-358">Value</span></span> |
|------------------|--------------------------------------------------------------------------------|
| <span data-ttu-id="55664-359">Description :</span><span class="sxs-lookup"><span data-stu-id="55664-359">Description:</span></span>     | <span data-ttu-id="55664-360">*C (a)*, *c (d)* et *c (s)* pour l’éclairage d’index de couleurs</span><span class="sxs-lookup"><span data-stu-id="55664-360">*C (a)*, *C (d)*, and *C (s)* for color-index lighting</span></span>                         |
| <span data-ttu-id="55664-361">Groupe d’attributs :</span><span class="sxs-lookup"><span data-stu-id="55664-361">Attribute group:</span></span> | <span data-ttu-id="55664-362">éclairage/activation</span><span class="sxs-lookup"><span data-stu-id="55664-362">lighting/enable</span></span>                                                                |
| <span data-ttu-id="55664-363">Valeur initiale :</span><span class="sxs-lookup"><span data-stu-id="55664-363">Initial value:</span></span>   | <span data-ttu-id="55664-364">0, 1, 1</span><span class="sxs-lookup"><span data-stu-id="55664-364">0,1,1</span></span>                                                                          |
| <span data-ttu-id="55664-365">Commande d’extraction :</span><span class="sxs-lookup"><span data-stu-id="55664-365">Get command:</span></span>     | [<span data-ttu-id="55664-366">**glGetFloatv**</span><span class="sxs-lookup"><span data-stu-id="55664-366">**glGetFloatv**</span></span>](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) |



 

</dd> </dl>

 

 




