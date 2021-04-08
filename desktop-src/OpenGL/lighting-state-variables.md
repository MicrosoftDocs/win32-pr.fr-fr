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
ms.openlocfilehash: aa7144e284b5be5abd5a6dc4e08fe2228b621465
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/25/2019
ms.locfileid: "103841282"
---
# <a name="lighting-state-variables"></a><span data-ttu-id="e766b-104">Variables d’état d’éclairage</span><span class="sxs-lookup"><span data-stu-id="e766b-104">Lighting State Variables</span></span>

<dl> <span data-ttu-id="e766b-105"><dt><span id="GL_LIGHTING"></span><span id="gl_lighting"></span>\_éclairage GL</dt> </span><span class="sxs-lookup"><span data-stu-id="e766b-105"><dt><span id="GL_LIGHTING"></span><span id="gl_lighting"></span>GL\_LIGHTING</dt> </span></span><dd> 

|                  |                                    |
|------------------|------------------------------------|
| <span data-ttu-id="e766b-106">Description :</span><span class="sxs-lookup"><span data-stu-id="e766b-106">Description:</span></span>     | <span data-ttu-id="e766b-107">True si l’éclairage est activé</span><span class="sxs-lookup"><span data-stu-id="e766b-107">True if lighting is enabled</span></span>        |
| <span data-ttu-id="e766b-108">Groupe d’attributs :</span><span class="sxs-lookup"><span data-stu-id="e766b-108">Attribute group:</span></span> | <span data-ttu-id="e766b-109">éclairage/activation</span><span class="sxs-lookup"><span data-stu-id="e766b-109">lighting/enable</span></span>                    |
| <span data-ttu-id="e766b-110">Valeur initiale :</span><span class="sxs-lookup"><span data-stu-id="e766b-110">Initial value:</span></span>   | <span data-ttu-id="e766b-111">GL- \_ faux</span><span class="sxs-lookup"><span data-stu-id="e766b-111">GL\_FALSE</span></span>                          |
| <span data-ttu-id="e766b-112">Commande d’extraction :</span><span class="sxs-lookup"><span data-stu-id="e766b-112">Get command:</span></span>     | [<span data-ttu-id="e766b-113">**glIsEnabled**</span><span class="sxs-lookup"><span data-stu-id="e766b-113">**glIsEnabled**</span></span>](glisenabled.md) |



 

<span data-ttu-id="e766b-114"></dd> <dt><span id="GL_COLOR_MATERIAL"></span><span id="gl_color_material"></span>\_matériau de couleur GL \_</dt> </span><span class="sxs-lookup"><span data-stu-id="e766b-114"></dd> <dt><span id="GL_COLOR_MATERIAL"></span><span id="gl_color_material"></span>GL\_COLOR\_MATERIAL</dt> </span></span><dd> 

|                  |                                    |
|------------------|------------------------------------|
| <span data-ttu-id="e766b-115">Description :</span><span class="sxs-lookup"><span data-stu-id="e766b-115">Description:</span></span>     | <span data-ttu-id="e766b-116">True si le suivi des couleurs est activé</span><span class="sxs-lookup"><span data-stu-id="e766b-116">True if color tracking is enabled</span></span>  |
| <span data-ttu-id="e766b-117">Groupe d’attributs :</span><span class="sxs-lookup"><span data-stu-id="e766b-117">Attribute group:</span></span> | <span data-ttu-id="e766b-118">éclairage</span><span class="sxs-lookup"><span data-stu-id="e766b-118">lighting</span></span>                           |
| <span data-ttu-id="e766b-119">Valeur initiale :</span><span class="sxs-lookup"><span data-stu-id="e766b-119">Initial value:</span></span>   | <span data-ttu-id="e766b-120">GL- \_ faux</span><span class="sxs-lookup"><span data-stu-id="e766b-120">GL\_FALSE</span></span>                          |
| <span data-ttu-id="e766b-121">Commande d’extraction :</span><span class="sxs-lookup"><span data-stu-id="e766b-121">Get command:</span></span>     | [<span data-ttu-id="e766b-122">**glIsEnabled**</span><span class="sxs-lookup"><span data-stu-id="e766b-122">**glIsEnabled**</span></span>](glisenabled.md) |



 

<span data-ttu-id="e766b-123"></dd> <dt><span id="GL_COLOR_MATERIAL_PARAMETER"></span><span id="gl_color_material_parameter"></span>\_paramètre de \_ matériau de couleur GL \_</dt> </span><span class="sxs-lookup"><span data-stu-id="e766b-123"></dd> <dt><span id="GL_COLOR_MATERIAL_PARAMETER"></span><span id="gl_color_material_parameter"></span>GL\_COLOR\_MATERIAL\_PARAMETER</dt> </span></span><dd> 

|                  |                                                                                  |
|------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="e766b-124">Description :</span><span class="sxs-lookup"><span data-stu-id="e766b-124">Description:</span></span>     | <span data-ttu-id="e766b-125">Couleur actuelle de suivi des propriétés de matériau</span><span class="sxs-lookup"><span data-stu-id="e766b-125">Material properties tracking current color</span></span>                                       |
| <span data-ttu-id="e766b-126">Groupe d’attributs :</span><span class="sxs-lookup"><span data-stu-id="e766b-126">Attribute group:</span></span> | <span data-ttu-id="e766b-127">éclairage</span><span class="sxs-lookup"><span data-stu-id="e766b-127">lighting</span></span>                                                                         |
| <span data-ttu-id="e766b-128">Valeur initiale :</span><span class="sxs-lookup"><span data-stu-id="e766b-128">Initial value:</span></span>   | <span data-ttu-id="e766b-129">\_ambiants \_ et \_ DIFFUSes du GL</span><span class="sxs-lookup"><span data-stu-id="e766b-129">GL\_AMBIENT\_AND\_DIFFUSE</span></span>                                                        |
| <span data-ttu-id="e766b-130">Commande d’extraction :</span><span class="sxs-lookup"><span data-stu-id="e766b-130">Get command:</span></span>     | [<span data-ttu-id="e766b-131">**glGetIntegerv**</span><span class="sxs-lookup"><span data-stu-id="e766b-131">**glGetIntegerv**</span></span>](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) |



 

<span data-ttu-id="e766b-132"></dd> <dt><span id="GL_COLOR_MATERIAL_FACE"></span><span id="gl_color_material_face"></span>\_ \_ visage matériel de couleur GL \_</dt> </span><span class="sxs-lookup"><span data-stu-id="e766b-132"></dd> <dt><span id="GL_COLOR_MATERIAL_FACE"></span><span id="gl_color_material_face"></span>GL\_COLOR\_MATERIAL\_FACE</dt> </span></span><dd> 

|                  |                                                                                  |
|------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="e766b-133">Description :</span><span class="sxs-lookup"><span data-stu-id="e766b-133">Description:</span></span>     | <span data-ttu-id="e766b-134">Visages affectés par le suivi des couleurs</span><span class="sxs-lookup"><span data-stu-id="e766b-134">Faces affected by color tracking</span></span>                                                 |
| <span data-ttu-id="e766b-135">Groupe d’attributs :</span><span class="sxs-lookup"><span data-stu-id="e766b-135">Attribute group:</span></span> | <span data-ttu-id="e766b-136">éclairage</span><span class="sxs-lookup"><span data-stu-id="e766b-136">lighting</span></span>                                                                         |
| <span data-ttu-id="e766b-137">Valeur initiale :</span><span class="sxs-lookup"><span data-stu-id="e766b-137">Initial value:</span></span>   | <span data-ttu-id="e766b-138">\_recto \_ et \_ Back GL</span><span class="sxs-lookup"><span data-stu-id="e766b-138">GL\_FRONT\_AND\_BACK</span></span>                                                             |
| <span data-ttu-id="e766b-139">Commande d’extraction :</span><span class="sxs-lookup"><span data-stu-id="e766b-139">Get command:</span></span>     | [<span data-ttu-id="e766b-140">**glGetIntegerv**</span><span class="sxs-lookup"><span data-stu-id="e766b-140">**glGetIntegerv**</span></span>](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) |



 

<span data-ttu-id="e766b-141"></dd> <dt><span id="GL_AMBIENT"></span><span id="gl_ambient"></span>ambiant du GL \_</dt> </span><span class="sxs-lookup"><span data-stu-id="e766b-141"></dd> <dt><span id="GL_AMBIENT"></span><span id="gl_ambient"></span>GL\_AMBIENT</dt> </span></span><dd> 

|                  |                                          |
|------------------|------------------------------------------|
| <span data-ttu-id="e766b-142">Description :</span><span class="sxs-lookup"><span data-stu-id="e766b-142">Description:</span></span>     | <span data-ttu-id="e766b-143">Couleur du matériau ambiant</span><span class="sxs-lookup"><span data-stu-id="e766b-143">Ambient material color</span></span>                   |
| <span data-ttu-id="e766b-144">Groupe d’attributs :</span><span class="sxs-lookup"><span data-stu-id="e766b-144">Attribute group:</span></span> | <span data-ttu-id="e766b-145">éclairage</span><span class="sxs-lookup"><span data-stu-id="e766b-145">lighting</span></span>                                 |
| <span data-ttu-id="e766b-146">Valeur initiale :</span><span class="sxs-lookup"><span data-stu-id="e766b-146">Initial value:</span></span>   | <span data-ttu-id="e766b-147">(0,2, 0,2, 0,2, 1,0)</span><span class="sxs-lookup"><span data-stu-id="e766b-147">(0.2,0.2,0.2,1.0)</span></span>                        |
| <span data-ttu-id="e766b-148">Commande d’extraction :</span><span class="sxs-lookup"><span data-stu-id="e766b-148">Get command:</span></span>     | [<span data-ttu-id="e766b-149">**glGetMaterialfv**</span><span class="sxs-lookup"><span data-stu-id="e766b-149">**glGetMaterialfv**</span></span>](glgetmaterial.md) |



 

<span data-ttu-id="e766b-150"></dd> <dt><span id="GL_DIFFUSE"></span><span id="gl_diffuse"></span>\_diffusion GL</dt> </span><span class="sxs-lookup"><span data-stu-id="e766b-150"></dd> <dt><span id="GL_DIFFUSE"></span><span id="gl_diffuse"></span>GL\_DIFFUSE</dt> </span></span><dd> 

|                  |                                          |
|------------------|------------------------------------------|
| <span data-ttu-id="e766b-151">Description :</span><span class="sxs-lookup"><span data-stu-id="e766b-151">Description:</span></span>     | <span data-ttu-id="e766b-152">Couleur du matériau diffus</span><span class="sxs-lookup"><span data-stu-id="e766b-152">Diffuse material color</span></span>                   |
| <span data-ttu-id="e766b-153">Groupe d’attributs :</span><span class="sxs-lookup"><span data-stu-id="e766b-153">Attribute group:</span></span> | <span data-ttu-id="e766b-154">éclairage</span><span class="sxs-lookup"><span data-stu-id="e766b-154">lighting</span></span>                                 |
| <span data-ttu-id="e766b-155">Valeur initiale :</span><span class="sxs-lookup"><span data-stu-id="e766b-155">Initial value:</span></span>   | <span data-ttu-id="e766b-156">(0,8, 0,8, 0,8, 1,0)</span><span class="sxs-lookup"><span data-stu-id="e766b-156">(0.8,0.8,0.8,1.0)</span></span>                        |
| <span data-ttu-id="e766b-157">Commande d’extraction :</span><span class="sxs-lookup"><span data-stu-id="e766b-157">Get command:</span></span>     | [<span data-ttu-id="e766b-158">**glGetMaterialfv**</span><span class="sxs-lookup"><span data-stu-id="e766b-158">**glGetMaterialfv**</span></span>](glgetmaterial.md) |



 

<span data-ttu-id="e766b-159"></dd> <dt><span id="GL_SPECULAR"></span><span id="gl_specular"></span>\_spéculaire GL</dt> </span><span class="sxs-lookup"><span data-stu-id="e766b-159"></dd> <dt><span id="GL_SPECULAR"></span><span id="gl_specular"></span>GL\_SPECULAR</dt> </span></span><dd> 

|                  |                                          |
|------------------|------------------------------------------|
| <span data-ttu-id="e766b-160">Description :</span><span class="sxs-lookup"><span data-stu-id="e766b-160">Description:</span></span>     | <span data-ttu-id="e766b-161">Couleur de matériau spéculaire</span><span class="sxs-lookup"><span data-stu-id="e766b-161">Specular material color</span></span>                  |
| <span data-ttu-id="e766b-162">Groupe d’attributs :</span><span class="sxs-lookup"><span data-stu-id="e766b-162">Attribute group:</span></span> | <span data-ttu-id="e766b-163">éclairage</span><span class="sxs-lookup"><span data-stu-id="e766b-163">lighting</span></span>                                 |
| <span data-ttu-id="e766b-164">Valeur initiale :</span><span class="sxs-lookup"><span data-stu-id="e766b-164">Initial value:</span></span>   | <span data-ttu-id="e766b-165">(0.0, 0.0, 0.0, 1.0)</span><span class="sxs-lookup"><span data-stu-id="e766b-165">(0.0,0.0,0.0,1.0)</span></span>                        |
| <span data-ttu-id="e766b-166">Commande d’extraction :</span><span class="sxs-lookup"><span data-stu-id="e766b-166">Get command:</span></span>     | [<span data-ttu-id="e766b-167">**glGetMaterialfv**</span><span class="sxs-lookup"><span data-stu-id="e766b-167">**glGetMaterialfv**</span></span>](glgetmaterial.md) |



 

<span data-ttu-id="e766b-168"></dd> <dt><span id="GL_EMISSION"></span><span id="gl_emission"></span>\_émission GL</dt> </span><span class="sxs-lookup"><span data-stu-id="e766b-168"></dd> <dt><span id="GL_EMISSION"></span><span id="gl_emission"></span>GL\_EMISSION</dt> </span></span><dd> 

|                  |                                          |
|------------------|------------------------------------------|
| <span data-ttu-id="e766b-169">Description :</span><span class="sxs-lookup"><span data-stu-id="e766b-169">Description:</span></span>     | <span data-ttu-id="e766b-170">Couleur de matériau émissif</span><span class="sxs-lookup"><span data-stu-id="e766b-170">Emissive material color</span></span>                  |
| <span data-ttu-id="e766b-171">Groupe d’attributs :</span><span class="sxs-lookup"><span data-stu-id="e766b-171">Attribute group:</span></span> | <span data-ttu-id="e766b-172">éclairage</span><span class="sxs-lookup"><span data-stu-id="e766b-172">lighting</span></span>                                 |
| <span data-ttu-id="e766b-173">Valeur initiale :</span><span class="sxs-lookup"><span data-stu-id="e766b-173">Initial value:</span></span>   | <span data-ttu-id="e766b-174">(0.0, 0.0, 0.0, 1.0)</span><span class="sxs-lookup"><span data-stu-id="e766b-174">(0.0,0.0,0.0,1.0)</span></span>                        |
| <span data-ttu-id="e766b-175">Commande d’extraction :</span><span class="sxs-lookup"><span data-stu-id="e766b-175">Get command:</span></span>     | [<span data-ttu-id="e766b-176">**glGetMaterialfv**</span><span class="sxs-lookup"><span data-stu-id="e766b-176">**glGetMaterialfv**</span></span>](glgetmaterial.md) |



 

<span data-ttu-id="e766b-177"></dd> <dt><span id="GL_SHININESS"></span><span id="gl_shininess"></span>\_éclat GL</dt> </span><span class="sxs-lookup"><span data-stu-id="e766b-177"></dd> <dt><span id="GL_SHININESS"></span><span id="gl_shininess"></span>GL\_SHININESS</dt> </span></span><dd> 

|                  |                                          |
|------------------|------------------------------------------|
| <span data-ttu-id="e766b-178">Description :</span><span class="sxs-lookup"><span data-stu-id="e766b-178">Description:</span></span>     | <span data-ttu-id="e766b-179">Exposant spéculaire du matériau</span><span class="sxs-lookup"><span data-stu-id="e766b-179">Specular exponent of material</span></span>            |
| <span data-ttu-id="e766b-180">Groupe d’attributs :</span><span class="sxs-lookup"><span data-stu-id="e766b-180">Attribute group:</span></span> | <span data-ttu-id="e766b-181">éclairage</span><span class="sxs-lookup"><span data-stu-id="e766b-181">lighting</span></span>                                 |
| <span data-ttu-id="e766b-182">Valeur initiale :</span><span class="sxs-lookup"><span data-stu-id="e766b-182">Initial value:</span></span>   | <span data-ttu-id="e766b-183">0.0</span><span class="sxs-lookup"><span data-stu-id="e766b-183">0.0</span></span>                                      |
| <span data-ttu-id="e766b-184">Commande d’extraction :</span><span class="sxs-lookup"><span data-stu-id="e766b-184">Get command:</span></span>     | [<span data-ttu-id="e766b-185">**glGetMaterialfv**</span><span class="sxs-lookup"><span data-stu-id="e766b-185">**glGetMaterialfv**</span></span>](glgetmaterial.md) |



 

<span data-ttu-id="e766b-186"></dd> <dt><span id="GL_LIGHT_MODEL_AMBIENT"></span><span id="gl_light_model_ambient"></span>ambiant (GL \_ Light \_ Model) \_</dt> </span><span class="sxs-lookup"><span data-stu-id="e766b-186"></dd> <dt><span id="GL_LIGHT_MODEL_AMBIENT"></span><span id="gl_light_model_ambient"></span>GL\_LIGHT\_MODEL\_AMBIENT</dt> </span></span><dd> 

|                  |                                                                                |
|------------------|--------------------------------------------------------------------------------|
| <span data-ttu-id="e766b-187">Description :</span><span class="sxs-lookup"><span data-stu-id="e766b-187">Description:</span></span>     | <span data-ttu-id="e766b-188">Couleur de scène ambiante</span><span class="sxs-lookup"><span data-stu-id="e766b-188">Ambient scene color</span></span>                                                            |
| <span data-ttu-id="e766b-189">Groupe d’attributs :</span><span class="sxs-lookup"><span data-stu-id="e766b-189">Attribute group:</span></span> | <span data-ttu-id="e766b-190">éclairage</span><span class="sxs-lookup"><span data-stu-id="e766b-190">lighting</span></span>                                                                       |
| <span data-ttu-id="e766b-191">Valeur initiale :</span><span class="sxs-lookup"><span data-stu-id="e766b-191">Initial value:</span></span>   | <span data-ttu-id="e766b-192">(0,2, 0,2, 0,2, 1,0)</span><span class="sxs-lookup"><span data-stu-id="e766b-192">(0.2,0.2,0.2,1.0)</span></span>                                                              |
| <span data-ttu-id="e766b-193">Commande d’extraction :</span><span class="sxs-lookup"><span data-stu-id="e766b-193">Get command:</span></span>     | [<span data-ttu-id="e766b-194">**glGetFloatv**</span><span class="sxs-lookup"><span data-stu-id="e766b-194">**glGetFloatv**</span></span>](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) |



 

<span data-ttu-id="e766b-195"></dd> <dt><span id="GL_LIGHT_MODEL_LOCAL_VIEWER"></span><span id="gl_light_model_local_viewer"></span>\_ \_ visionneuse locale du modèle de lumière \_ GL \_</dt> </span><span class="sxs-lookup"><span data-stu-id="e766b-195"></dd> <dt><span id="GL_LIGHT_MODEL_LOCAL_VIEWER"></span><span id="gl_light_model_local_viewer"></span>GL\_LIGHT\_MODEL\_LOCAL\_VIEWER</dt> </span></span><dd> 

|                  |                                                                                  |
|------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="e766b-196">Description :</span><span class="sxs-lookup"><span data-stu-id="e766b-196">Description:</span></span>     | <span data-ttu-id="e766b-197">La visionneuse est locale</span><span class="sxs-lookup"><span data-stu-id="e766b-197">Viewer is local</span></span>                                                                  |
| <span data-ttu-id="e766b-198">Groupe d’attributs :</span><span class="sxs-lookup"><span data-stu-id="e766b-198">Attribute group:</span></span> | <span data-ttu-id="e766b-199">éclairage</span><span class="sxs-lookup"><span data-stu-id="e766b-199">lighting</span></span>                                                                         |
| <span data-ttu-id="e766b-200">Valeur initiale :</span><span class="sxs-lookup"><span data-stu-id="e766b-200">Initial value:</span></span>   | <span data-ttu-id="e766b-201">GL- \_ faux</span><span class="sxs-lookup"><span data-stu-id="e766b-201">GL\_FALSE</span></span>                                                                        |
| <span data-ttu-id="e766b-202">Commande d’extraction :</span><span class="sxs-lookup"><span data-stu-id="e766b-202">Get command:</span></span>     | [<span data-ttu-id="e766b-203">**glGetBooleanv**</span><span class="sxs-lookup"><span data-stu-id="e766b-203">**glGetBooleanv**</span></span>](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) |



 

<span data-ttu-id="e766b-204"></dd> <dt><span id="GL_LIGHT_MODEL_TWO_SIDE"></span><span id="gl_light_model_two_side"></span>\_ \_ côté 2 du modèle GL clair \_ \_</dt> </span><span class="sxs-lookup"><span data-stu-id="e766b-204"></dd> <dt><span id="GL_LIGHT_MODEL_TWO_SIDE"></span><span id="gl_light_model_two_side"></span>GL\_LIGHT\_MODEL\_TWO\_SIDE</dt> </span></span><dd> 

|                  |                                                                                  |
|------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="e766b-205">Description :</span><span class="sxs-lookup"><span data-stu-id="e766b-205">Description:</span></span>     | <span data-ttu-id="e766b-206">Utiliser l’éclairage à deux côtés</span><span class="sxs-lookup"><span data-stu-id="e766b-206">Use two-sided lighting</span></span>                                                           |
| <span data-ttu-id="e766b-207">Groupe d’attributs :</span><span class="sxs-lookup"><span data-stu-id="e766b-207">Attribute group:</span></span> | <span data-ttu-id="e766b-208">éclairage</span><span class="sxs-lookup"><span data-stu-id="e766b-208">lighting</span></span>                                                                         |
| <span data-ttu-id="e766b-209">Valeur initiale :</span><span class="sxs-lookup"><span data-stu-id="e766b-209">Initial value:</span></span>   | <span data-ttu-id="e766b-210">GL- \_ faux</span><span class="sxs-lookup"><span data-stu-id="e766b-210">GL\_FALSE</span></span>                                                                        |
| <span data-ttu-id="e766b-211">Commande d’extraction :</span><span class="sxs-lookup"><span data-stu-id="e766b-211">Get command:</span></span>     | [<span data-ttu-id="e766b-212">**glGetBooleanv**</span><span class="sxs-lookup"><span data-stu-id="e766b-212">**glGetBooleanv**</span></span>](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) |



 

<span data-ttu-id="e766b-213"></dd> <dt><span id="GL_AMBIENT"></span><span id="gl_ambient"></span>ambiant du GL \_</dt> </span><span class="sxs-lookup"><span data-stu-id="e766b-213"></dd> <dt><span id="GL_AMBIENT"></span><span id="gl_ambient"></span>GL\_AMBIENT</dt> </span></span><dd> 

|                  |                                    |
|------------------|------------------------------------|
| <span data-ttu-id="e766b-214">Description :</span><span class="sxs-lookup"><span data-stu-id="e766b-214">Description:</span></span>     | <span data-ttu-id="e766b-215">Intensité ambiante de la lumière *i*</span><span class="sxs-lookup"><span data-stu-id="e766b-215">Ambient intensity of light *i*</span></span>     |
| <span data-ttu-id="e766b-216">Groupe d’attributs :</span><span class="sxs-lookup"><span data-stu-id="e766b-216">Attribute group:</span></span> | <span data-ttu-id="e766b-217">éclairage</span><span class="sxs-lookup"><span data-stu-id="e766b-217">lighting</span></span>                           |
| <span data-ttu-id="e766b-218">Valeur initiale :</span><span class="sxs-lookup"><span data-stu-id="e766b-218">Initial value:</span></span>   | <span data-ttu-id="e766b-219">(0.0, 0.0, 0.0, 1.0)</span><span class="sxs-lookup"><span data-stu-id="e766b-219">(0.0,0.0,0.0,1.0)</span></span>                  |
| <span data-ttu-id="e766b-220">Commande d’extraction :</span><span class="sxs-lookup"><span data-stu-id="e766b-220">Get command:</span></span>     | [<span data-ttu-id="e766b-221">**glGetLightfv**</span><span class="sxs-lookup"><span data-stu-id="e766b-221">**glGetLightfv**</span></span>](glgetlight.md) |



 

<span data-ttu-id="e766b-222"></dd> <dt><span id="GL_DIFFUSE"></span><span id="gl_diffuse"></span>\_diffusion GL</dt> </span><span class="sxs-lookup"><span data-stu-id="e766b-222"></dd> <dt><span id="GL_DIFFUSE"></span><span id="gl_diffuse"></span>GL\_DIFFUSE</dt> </span></span><dd> 

|                  |                                    |
|------------------|------------------------------------|
| <span data-ttu-id="e766b-223">Description :</span><span class="sxs-lookup"><span data-stu-id="e766b-223">Description:</span></span>     | <span data-ttu-id="e766b-224">Intensité diffuse de la lumière *i*</span><span class="sxs-lookup"><span data-stu-id="e766b-224">Diffuse intensity of light *i*</span></span>     |
| <span data-ttu-id="e766b-225">Groupe d’attributs :</span><span class="sxs-lookup"><span data-stu-id="e766b-225">Attribute group:</span></span> | <span data-ttu-id="e766b-226">éclairage</span><span class="sxs-lookup"><span data-stu-id="e766b-226">lighting</span></span>                           |
| <span data-ttu-id="e766b-227">Valeur initiale :</span><span class="sxs-lookup"><span data-stu-id="e766b-227">Initial value:</span></span>   |                                    |
| <span data-ttu-id="e766b-228">Commande d’extraction :</span><span class="sxs-lookup"><span data-stu-id="e766b-228">Get command:</span></span>     | [<span data-ttu-id="e766b-229">**glGetLightfv**</span><span class="sxs-lookup"><span data-stu-id="e766b-229">**glGetLightfv**</span></span>](glgetlight.md) |



 

<span data-ttu-id="e766b-230"></dd> <dt><span id="GL_SPECULAR"></span><span id="gl_specular"></span>\_spéculaire GL</dt> </span><span class="sxs-lookup"><span data-stu-id="e766b-230"></dd> <dt><span id="GL_SPECULAR"></span><span id="gl_specular"></span>GL\_SPECULAR</dt> </span></span><dd> 

|                  |                                    |
|------------------|------------------------------------|
| <span data-ttu-id="e766b-231">Description :</span><span class="sxs-lookup"><span data-stu-id="e766b-231">Description:</span></span>     | <span data-ttu-id="e766b-232">Intensité spéculaire de la lumière *i*</span><span class="sxs-lookup"><span data-stu-id="e766b-232">Specular intensity of light *i*</span></span>    |
| <span data-ttu-id="e766b-233">Groupe d’attributs :</span><span class="sxs-lookup"><span data-stu-id="e766b-233">Attribute group:</span></span> | <span data-ttu-id="e766b-234">éclairage</span><span class="sxs-lookup"><span data-stu-id="e766b-234">lighting</span></span>                           |
| <span data-ttu-id="e766b-235">Valeur initiale :</span><span class="sxs-lookup"><span data-stu-id="e766b-235">Initial value:</span></span>   |                                    |
| <span data-ttu-id="e766b-236">Commande d’extraction :</span><span class="sxs-lookup"><span data-stu-id="e766b-236">Get command:</span></span>     | [<span data-ttu-id="e766b-237">**glGetLightfv**</span><span class="sxs-lookup"><span data-stu-id="e766b-237">**glGetLightfv**</span></span>](glgetlight.md) |



 

<span data-ttu-id="e766b-238"></dd> <dt><span id="GL_POSITION"></span><span id="gl_position"></span>\_position GL</dt> </span><span class="sxs-lookup"><span data-stu-id="e766b-238"></dd> <dt><span id="GL_POSITION"></span><span id="gl_position"></span>GL\_POSITION</dt> </span></span><dd> 

|                  |                                    |
|------------------|------------------------------------|
| <span data-ttu-id="e766b-239">Description :</span><span class="sxs-lookup"><span data-stu-id="e766b-239">Description:</span></span>     | <span data-ttu-id="e766b-240">Position de la lumière *i*</span><span class="sxs-lookup"><span data-stu-id="e766b-240">Position of light *i*</span></span>              |
| <span data-ttu-id="e766b-241">Groupe d’attributs :</span><span class="sxs-lookup"><span data-stu-id="e766b-241">Attribute group:</span></span> | <span data-ttu-id="e766b-242">éclairage</span><span class="sxs-lookup"><span data-stu-id="e766b-242">lighting</span></span>                           |
| <span data-ttu-id="e766b-243">Valeur initiale :</span><span class="sxs-lookup"><span data-stu-id="e766b-243">Initial value:</span></span>   | <span data-ttu-id="e766b-244">(0.0, 0.0, 1.0, 0.0)</span><span class="sxs-lookup"><span data-stu-id="e766b-244">(0.0,0.0,1.0,0.0)</span></span>                  |
| <span data-ttu-id="e766b-245">Commande d’extraction :</span><span class="sxs-lookup"><span data-stu-id="e766b-245">Get command:</span></span>     | [<span data-ttu-id="e766b-246">**glGetLightfv**</span><span class="sxs-lookup"><span data-stu-id="e766b-246">**glGetLightfv**</span></span>](glgetlight.md) |



 

<span data-ttu-id="e766b-247"></dd> <dt><span id="GL_CONSTANT_ATTENUATION"></span><span id="gl_constant_attenuation"></span>\_atténuation constante du GL \_</dt> </span><span class="sxs-lookup"><span data-stu-id="e766b-247"></dd> <dt><span id="GL_CONSTANT_ATTENUATION"></span><span id="gl_constant_attenuation"></span>GL\_CONSTANT\_ATTENUATION</dt> </span></span><dd> 

|                  |                                    |
|------------------|------------------------------------|
| <span data-ttu-id="e766b-248">Description :</span><span class="sxs-lookup"><span data-stu-id="e766b-248">Description:</span></span>     | <span data-ttu-id="e766b-249">Facteur d’atténuation constant</span><span class="sxs-lookup"><span data-stu-id="e766b-249">Constant attenuation factor</span></span>        |
| <span data-ttu-id="e766b-250">Groupe d’attributs :</span><span class="sxs-lookup"><span data-stu-id="e766b-250">Attribute group:</span></span> | <span data-ttu-id="e766b-251">éclairage</span><span class="sxs-lookup"><span data-stu-id="e766b-251">lighting</span></span>                           |
| <span data-ttu-id="e766b-252">Valeur initiale :</span><span class="sxs-lookup"><span data-stu-id="e766b-252">Initial value:</span></span>   | <span data-ttu-id="e766b-253">1.0</span><span class="sxs-lookup"><span data-stu-id="e766b-253">1.0</span></span>                                |
| <span data-ttu-id="e766b-254">Commande d’extraction :</span><span class="sxs-lookup"><span data-stu-id="e766b-254">Get command:</span></span>     | [<span data-ttu-id="e766b-255">**glGetLightfv**</span><span class="sxs-lookup"><span data-stu-id="e766b-255">**glGetLightfv**</span></span>](glgetlight.md) |



 

<span data-ttu-id="e766b-256"></dd> <dt><span id="GL_LINEAR_ATTENUATION"></span><span id="gl_linear_attenuation"></span>\_atténuation linéaire du GL \_</dt> </span><span class="sxs-lookup"><span data-stu-id="e766b-256"></dd> <dt><span id="GL_LINEAR_ATTENUATION"></span><span id="gl_linear_attenuation"></span>GL\_LINEAR\_ATTENUATION</dt> </span></span><dd> 

|                  |                                    |
|------------------|------------------------------------|
| <span data-ttu-id="e766b-257">Description :</span><span class="sxs-lookup"><span data-stu-id="e766b-257">Description:</span></span>     | <span data-ttu-id="e766b-258">Facteur d’atténuation linéaire</span><span class="sxs-lookup"><span data-stu-id="e766b-258">Linear attenuation factor</span></span>          |
| <span data-ttu-id="e766b-259">Groupe d’attributs :</span><span class="sxs-lookup"><span data-stu-id="e766b-259">Attribute group:</span></span> | <span data-ttu-id="e766b-260">éclairage</span><span class="sxs-lookup"><span data-stu-id="e766b-260">lighting</span></span>                           |
| <span data-ttu-id="e766b-261">Valeur initiale :</span><span class="sxs-lookup"><span data-stu-id="e766b-261">Initial value:</span></span>   | <span data-ttu-id="e766b-262">0.0</span><span class="sxs-lookup"><span data-stu-id="e766b-262">0.0</span></span>                                |
| <span data-ttu-id="e766b-263">Commande d’extraction :</span><span class="sxs-lookup"><span data-stu-id="e766b-263">Get command:</span></span>     | [<span data-ttu-id="e766b-264">**glGetLightfv**</span><span class="sxs-lookup"><span data-stu-id="e766b-264">**glGetLightfv**</span></span>](glgetlight.md) |



 

<span data-ttu-id="e766b-265"></dd> <dt><span id="GL_QUADRATIC_ATTENUATION"></span><span id="gl_quadratic_attenuation"></span>\_atténuation quadratique du \_ GL</dt> </span><span class="sxs-lookup"><span data-stu-id="e766b-265"></dd> <dt><span id="GL_QUADRATIC_ATTENUATION"></span><span id="gl_quadratic_attenuation"></span>GL\_QUADRATIC\_ATTENUATION</dt> </span></span><dd> 

|                  |                                    |
|------------------|------------------------------------|
| <span data-ttu-id="e766b-266">Description :</span><span class="sxs-lookup"><span data-stu-id="e766b-266">Description:</span></span>     | <span data-ttu-id="e766b-267">Facteur d’atténuation quadratique</span><span class="sxs-lookup"><span data-stu-id="e766b-267">Quadratic attenuation factor</span></span>       |
| <span data-ttu-id="e766b-268">Groupe d’attributs :</span><span class="sxs-lookup"><span data-stu-id="e766b-268">Attribute group:</span></span> | <span data-ttu-id="e766b-269">éclairage</span><span class="sxs-lookup"><span data-stu-id="e766b-269">lighting</span></span>                           |
| <span data-ttu-id="e766b-270">Valeur initiale :</span><span class="sxs-lookup"><span data-stu-id="e766b-270">Initial value:</span></span>   | <span data-ttu-id="e766b-271">0.0</span><span class="sxs-lookup"><span data-stu-id="e766b-271">0.0</span></span>                                |
| <span data-ttu-id="e766b-272">Commande d’extraction :</span><span class="sxs-lookup"><span data-stu-id="e766b-272">Get command:</span></span>     | [<span data-ttu-id="e766b-273">**glGetLightfv**</span><span class="sxs-lookup"><span data-stu-id="e766b-273">**glGetLightfv**</span></span>](glgetlight.md) |



 

<span data-ttu-id="e766b-274"></dd> <dt><span id="GL_SPOT_DIRECTION"></span><span id="gl_spot_direction"></span>\_sens du spot GL \_</dt> </span><span class="sxs-lookup"><span data-stu-id="e766b-274"></dd> <dt><span id="GL_SPOT_DIRECTION"></span><span id="gl_spot_direction"></span>GL\_SPOT\_DIRECTION</dt> </span></span><dd> 

|                  |                                    |
|------------------|------------------------------------|
| <span data-ttu-id="e766b-275">Description :</span><span class="sxs-lookup"><span data-stu-id="e766b-275">Description:</span></span>     | <span data-ttu-id="e766b-276">Direction Spotlight de la lumière *i*</span><span class="sxs-lookup"><span data-stu-id="e766b-276">Spotlight direction of light *i*</span></span>   |
| <span data-ttu-id="e766b-277">Groupe d’attributs :</span><span class="sxs-lookup"><span data-stu-id="e766b-277">Attribute group:</span></span> | <span data-ttu-id="e766b-278">éclairage</span><span class="sxs-lookup"><span data-stu-id="e766b-278">lighting</span></span>                           |
| <span data-ttu-id="e766b-279">Valeur initiale :</span><span class="sxs-lookup"><span data-stu-id="e766b-279">Initial value:</span></span>   | <span data-ttu-id="e766b-280">(0.0, 0.0,-1,0)</span><span class="sxs-lookup"><span data-stu-id="e766b-280">(0.0,0.0,-1.0)</span></span>                     |
| <span data-ttu-id="e766b-281">Commande d’extraction :</span><span class="sxs-lookup"><span data-stu-id="e766b-281">Get command:</span></span>     | [<span data-ttu-id="e766b-282">**glGetLightfv**</span><span class="sxs-lookup"><span data-stu-id="e766b-282">**glGetLightfv**</span></span>](glgetlight.md) |



 

<span data-ttu-id="e766b-283"></dd> <dt><span id="GL_SPOT_EXPONENT"></span><span id="gl_spot_exponent"></span>exposant de point comptable \_ \_</dt> </span><span class="sxs-lookup"><span data-stu-id="e766b-283"></dd> <dt><span id="GL_SPOT_EXPONENT"></span><span id="gl_spot_exponent"></span>GL\_SPOT\_EXPONENT</dt> </span></span><dd> 

|                  |                                    |
|------------------|------------------------------------|
| <span data-ttu-id="e766b-284">Description :</span><span class="sxs-lookup"><span data-stu-id="e766b-284">Description:</span></span>     | <span data-ttu-id="e766b-285">Exposant Gong de la lumière *i*</span><span class="sxs-lookup"><span data-stu-id="e766b-285">Spotlight exponent of light *i*</span></span>    |
| <span data-ttu-id="e766b-286">Groupe d’attributs :</span><span class="sxs-lookup"><span data-stu-id="e766b-286">Attribute group:</span></span> | <span data-ttu-id="e766b-287">éclairage</span><span class="sxs-lookup"><span data-stu-id="e766b-287">lighting</span></span>                           |
| <span data-ttu-id="e766b-288">Valeur initiale :</span><span class="sxs-lookup"><span data-stu-id="e766b-288">Initial value:</span></span>   | <span data-ttu-id="e766b-289">0.0</span><span class="sxs-lookup"><span data-stu-id="e766b-289">0.0</span></span>                                |
| <span data-ttu-id="e766b-290">Commande d’extraction :</span><span class="sxs-lookup"><span data-stu-id="e766b-290">Get command:</span></span>     | [<span data-ttu-id="e766b-291">**glGetLightfv**</span><span class="sxs-lookup"><span data-stu-id="e766b-291">**glGetLightfv**</span></span>](glgetlight.md) |



 

<span data-ttu-id="e766b-292"></dd> <dt><span id="GL_SPOT_CUTOFF"></span><span id="gl_spot_cutoff"></span>coupure de l' \_ emplacement GL \_</dt> </span><span class="sxs-lookup"><span data-stu-id="e766b-292"></dd> <dt><span id="GL_SPOT_CUTOFF"></span><span id="gl_spot_cutoff"></span>GL\_SPOT\_CUTOFF</dt> </span></span><dd> 

|                  |                                    |
|------------------|------------------------------------|
| <span data-ttu-id="e766b-293">Description :</span><span class="sxs-lookup"><span data-stu-id="e766b-293">Description:</span></span>     | <span data-ttu-id="e766b-294">Angle Spotlight de la lumière *i*</span><span class="sxs-lookup"><span data-stu-id="e766b-294">Spotlight angle of light *i*</span></span>       |
| <span data-ttu-id="e766b-295">Groupe d’attributs :</span><span class="sxs-lookup"><span data-stu-id="e766b-295">Attribute group:</span></span> | <span data-ttu-id="e766b-296">éclairage</span><span class="sxs-lookup"><span data-stu-id="e766b-296">lighting</span></span>                           |
| <span data-ttu-id="e766b-297">Valeur initiale :</span><span class="sxs-lookup"><span data-stu-id="e766b-297">Initial value:</span></span>   | <span data-ttu-id="e766b-298">180,0</span><span class="sxs-lookup"><span data-stu-id="e766b-298">180.0</span></span>                              |
| <span data-ttu-id="e766b-299">Commande d’extraction :</span><span class="sxs-lookup"><span data-stu-id="e766b-299">Get command:</span></span>     | [<span data-ttu-id="e766b-300">**glGetLightfv**</span><span class="sxs-lookup"><span data-stu-id="e766b-300">**glGetLightfv**</span></span>](glgetlight.md) |



 

<span data-ttu-id="e766b-301"></dd> <dt><span id="GL_LIGHT_i"></span><span id="gl_light_i"></span><span id="GL_LIGHT_I"></span>GL \_ clair *i*</dt> </span><span class="sxs-lookup"><span data-stu-id="e766b-301"></dd> <dt><span id="GL_LIGHT_i"></span><span id="gl_light_i"></span><span id="GL_LIGHT_I"></span>GL\_LIGHT *i*</dt> </span></span><dd> 

|                  |                                    |
|------------------|------------------------------------|
| <span data-ttu-id="e766b-302">Description :</span><span class="sxs-lookup"><span data-stu-id="e766b-302">Description:</span></span>     | <span data-ttu-id="e766b-303">True si l’option Light *i* est activée</span><span class="sxs-lookup"><span data-stu-id="e766b-303">True if light *i* enabled</span></span>          |
| <span data-ttu-id="e766b-304">Groupe d’attributs :</span><span class="sxs-lookup"><span data-stu-id="e766b-304">Attribute group:</span></span> | <span data-ttu-id="e766b-305">éclairage/activation</span><span class="sxs-lookup"><span data-stu-id="e766b-305">lighting/enable</span></span>                    |
| <span data-ttu-id="e766b-306">Valeur initiale :</span><span class="sxs-lookup"><span data-stu-id="e766b-306">Initial value:</span></span>   | <span data-ttu-id="e766b-307">GL- \_ faux</span><span class="sxs-lookup"><span data-stu-id="e766b-307">GL\_FALSE</span></span>                          |
| <span data-ttu-id="e766b-308">Commande d’extraction :</span><span class="sxs-lookup"><span data-stu-id="e766b-308">Get command:</span></span>     | [<span data-ttu-id="e766b-309">**glIsEnabled**</span><span class="sxs-lookup"><span data-stu-id="e766b-309">**glIsEnabled**</span></span>](glisenabled.md) |



 

<span data-ttu-id="e766b-310"></dd> <dt><span id="GL_COLOR_INDEXES"></span><span id="gl_color_indexes"></span>\_index de couleurs GL \_</dt> </span><span class="sxs-lookup"><span data-stu-id="e766b-310"></dd> <dt><span id="GL_COLOR_INDEXES"></span><span id="gl_color_indexes"></span>GL\_COLOR\_INDEXES</dt> </span></span><dd> 

|                  |                                                                                |
|------------------|--------------------------------------------------------------------------------|
| <span data-ttu-id="e766b-311">Description :</span><span class="sxs-lookup"><span data-stu-id="e766b-311">Description:</span></span>     | <span data-ttu-id="e766b-312">*C (a)*, *c (d)* et *c (s)* pour l’éclairage d’index de couleurs</span><span class="sxs-lookup"><span data-stu-id="e766b-312">*C (a)*, *C (d)*, and *C (s)* for color-index lighting</span></span>                         |
| <span data-ttu-id="e766b-313">Groupe d’attributs :</span><span class="sxs-lookup"><span data-stu-id="e766b-313">Attribute group:</span></span> | <span data-ttu-id="e766b-314">éclairage/activation</span><span class="sxs-lookup"><span data-stu-id="e766b-314">lighting/enable</span></span>                                                                |
| <span data-ttu-id="e766b-315">Valeur initiale :</span><span class="sxs-lookup"><span data-stu-id="e766b-315">Initial value:</span></span>   | <span data-ttu-id="e766b-316">0, 1, 1</span><span class="sxs-lookup"><span data-stu-id="e766b-316">0,1,1</span></span>                                                                          |
| <span data-ttu-id="e766b-317">Commande d’extraction :</span><span class="sxs-lookup"><span data-stu-id="e766b-317">Get command:</span></span>     | [<span data-ttu-id="e766b-318">**glGetFloatv**</span><span class="sxs-lookup"><span data-stu-id="e766b-318">**glGetFloatv**</span></span>](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) |



 

</dd> </dl>

 

 




