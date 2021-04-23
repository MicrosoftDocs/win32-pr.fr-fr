---
title: Variables d’état de transformation
description: Variables d’état de transformation
ms.assetid: 3a6be5ac-ac7a-4c3e-8b65-0404849ae67c
keywords:
- Variables d’état de transformation OpenGL
topic_type:
- apiref
api_name:
- Transformation State Variables
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8c7b53e0abae08447df86d8968a33a361be08a1e
ms.sourcegitcommit: 63753fcfb0afbbe5ec283fb8316e62c2dc950f66
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/22/2021
ms.locfileid: "107908827"
---
# <a name="transformation-state-variables"></a><span data-ttu-id="78558-104">Variables d’état de transformation</span><span class="sxs-lookup"><span data-stu-id="78558-104">Transformation State Variables</span></span>

<dl> <span data-ttu-id="78558-105"><dt><span id="GL_MODELVIEW_MATRIX"></span><span id="gl_modelview_matrix"></span>\_matrice MODELVIEW \_ GL</dt> </span><span class="sxs-lookup"><span data-stu-id="78558-105"><dt><span id="GL_MODELVIEW_MATRIX"></span><span id="gl_modelview_matrix"></span>GL\_MODELVIEW\_MATRIX</dt> </span></span><dd> 

| <span data-ttu-id="78558-106">Propriété</span><span class="sxs-lookup"><span data-stu-id="78558-106">Property</span></span> | <span data-ttu-id="78558-107">Valeur</span><span class="sxs-lookup"><span data-stu-id="78558-107">Value</span></span> |
|------------------|------------------------------------|
| <span data-ttu-id="78558-108">Description :</span><span class="sxs-lookup"><span data-stu-id="78558-108">Description:</span></span>     | <span data-ttu-id="78558-109">Pile de matrices Modelview</span><span class="sxs-lookup"><span data-stu-id="78558-109">Modelview matrix stack</span></span>             |
| <span data-ttu-id="78558-110">Groupe d’attributs :</span><span class="sxs-lookup"><span data-stu-id="78558-110">Attribute group:</span></span> |                                    |
| <span data-ttu-id="78558-111">Valeur initiale :</span><span class="sxs-lookup"><span data-stu-id="78558-111">Initial value:</span></span>   | <span data-ttu-id="78558-112">Identité</span><span class="sxs-lookup"><span data-stu-id="78558-112">Identity</span></span>                           |
| <span data-ttu-id="78558-113">Commande d’extraction :</span><span class="sxs-lookup"><span data-stu-id="78558-113">Get command:</span></span>     | [<span data-ttu-id="78558-114">**glGetFloatv**</span><span class="sxs-lookup"><span data-stu-id="78558-114">**glGetFloatv**</span></span>](glgetfloatv.md) |



 

<span data-ttu-id="78558-115"></dd> <dt><span id="GL_PROJECTION_MATRIX"></span><span id="gl_projection_matrix"></span>\_matrice de projection GL \_</dt> </span><span class="sxs-lookup"><span data-stu-id="78558-115"></dd> <dt><span id="GL_PROJECTION_MATRIX"></span><span id="gl_projection_matrix"></span>GL\_PROJECTION\_MATRIX</dt> </span></span><dd> 

| <span data-ttu-id="78558-116">Propriété</span><span class="sxs-lookup"><span data-stu-id="78558-116">Property</span></span> | <span data-ttu-id="78558-117">Valeur</span><span class="sxs-lookup"><span data-stu-id="78558-117">Value</span></span> |
|------------------|--------------------------------------------------------------------------------|
| <span data-ttu-id="78558-118">Description :</span><span class="sxs-lookup"><span data-stu-id="78558-118">Description:</span></span>     | <span data-ttu-id="78558-119">Pile de matrice de projection</span><span class="sxs-lookup"><span data-stu-id="78558-119">Projection matrix stack</span></span>                                                        |
| <span data-ttu-id="78558-120">Groupe d’attributs :</span><span class="sxs-lookup"><span data-stu-id="78558-120">Attribute group:</span></span> |                                                                                |
| <span data-ttu-id="78558-121">Valeur initiale :</span><span class="sxs-lookup"><span data-stu-id="78558-121">Initial value:</span></span>   | <span data-ttu-id="78558-122">Identité</span><span class="sxs-lookup"><span data-stu-id="78558-122">Identity</span></span>                                                                       |
| <span data-ttu-id="78558-123">Commande d’extraction :</span><span class="sxs-lookup"><span data-stu-id="78558-123">Get command:</span></span>     | [<span data-ttu-id="78558-124">**glGetFloatv**</span><span class="sxs-lookup"><span data-stu-id="78558-124">**glGetFloatv**</span></span>](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) |



 

<span data-ttu-id="78558-125"></dd> <dt><span id="GL_TEXTURE_MATRIX"></span><span id="gl_texture_matrix"></span>\_matrice de texture GL \_</dt> </span><span class="sxs-lookup"><span data-stu-id="78558-125"></dd> <dt><span id="GL_TEXTURE_MATRIX"></span><span id="gl_texture_matrix"></span>GL\_TEXTURE\_MATRIX</dt> </span></span><dd> 

| <span data-ttu-id="78558-126">Propriété</span><span class="sxs-lookup"><span data-stu-id="78558-126">Property</span></span> | <span data-ttu-id="78558-127">Valeur</span><span class="sxs-lookup"><span data-stu-id="78558-127">Value</span></span> |
|------------------|--------------------------------------------------------------------------------|
| <span data-ttu-id="78558-128">Description :</span><span class="sxs-lookup"><span data-stu-id="78558-128">Description:</span></span>     | <span data-ttu-id="78558-129">Pile de matrices de texture</span><span class="sxs-lookup"><span data-stu-id="78558-129">Texture matrix stack</span></span>                                                           |
| <span data-ttu-id="78558-130">Groupe d’attributs :</span><span class="sxs-lookup"><span data-stu-id="78558-130">Attribute group:</span></span> |                                                                                |
| <span data-ttu-id="78558-131">Valeur initiale :</span><span class="sxs-lookup"><span data-stu-id="78558-131">Initial value:</span></span>   | <span data-ttu-id="78558-132">Identité</span><span class="sxs-lookup"><span data-stu-id="78558-132">Identity</span></span>                                                                       |
| <span data-ttu-id="78558-133">Commande d’extraction :</span><span class="sxs-lookup"><span data-stu-id="78558-133">Get command:</span></span>     | [<span data-ttu-id="78558-134">**glGetFloatv**</span><span class="sxs-lookup"><span data-stu-id="78558-134">**glGetFloatv**</span></span>](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) |



 

<span data-ttu-id="78558-135"></dd> <dt><span id="GL_VIEWPORT"></span><span id="gl_viewport"></span>\_fenêtre d’affichage comptabilité</dt> </span><span class="sxs-lookup"><span data-stu-id="78558-135"></dd> <dt><span id="GL_VIEWPORT"></span><span id="gl_viewport"></span>GL\_VIEWPORT</dt> </span></span><dd> 

| <span data-ttu-id="78558-136">Propriété</span><span class="sxs-lookup"><span data-stu-id="78558-136">Property</span></span> | <span data-ttu-id="78558-137">Valeur</span><span class="sxs-lookup"><span data-stu-id="78558-137">Value</span></span> |
|------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="78558-138">Description :</span><span class="sxs-lookup"><span data-stu-id="78558-138">Description:</span></span>     | <span data-ttu-id="78558-139">Origine de la fenêtre d’affichage et étendue</span><span class="sxs-lookup"><span data-stu-id="78558-139">Viewport origin and extent</span></span>                                                       |
| <span data-ttu-id="78558-140">Groupe d’attributs :</span><span class="sxs-lookup"><span data-stu-id="78558-140">Attribute group:</span></span> | <span data-ttu-id="78558-141">fenêtre d'affichage</span><span class="sxs-lookup"><span data-stu-id="78558-141">viewport</span></span>                                                                         |
| <span data-ttu-id="78558-142">Valeur initiale :</span><span class="sxs-lookup"><span data-stu-id="78558-142">Initial value:</span></span>   |                                                                                  |
| <span data-ttu-id="78558-143">Commande d’extraction :</span><span class="sxs-lookup"><span data-stu-id="78558-143">Get command:</span></span>     | [<span data-ttu-id="78558-144">**glGetIntegerv**</span><span class="sxs-lookup"><span data-stu-id="78558-144">**glGetIntegerv**</span></span>](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) |



 

<span data-ttu-id="78558-145"></dd> <dt><span id="GL_DEPTH_RANGE"></span><span id="gl_depth_range"></span>\_plage de profondeur GL \_</dt> </span><span class="sxs-lookup"><span data-stu-id="78558-145"></dd> <dt><span id="GL_DEPTH_RANGE"></span><span id="gl_depth_range"></span>GL\_DEPTH\_RANGE</dt> </span></span><dd> 

| <span data-ttu-id="78558-146">Propriété</span><span class="sxs-lookup"><span data-stu-id="78558-146">Property</span></span> | <span data-ttu-id="78558-147">Valeur</span><span class="sxs-lookup"><span data-stu-id="78558-147">Value</span></span> |
|------------------|--------------------------------------------------------------------------------|
| <span data-ttu-id="78558-148">Description :</span><span class="sxs-lookup"><span data-stu-id="78558-148">Description:</span></span>     | <span data-ttu-id="78558-149">Plage de profondeur proche et éloignée</span><span class="sxs-lookup"><span data-stu-id="78558-149">Depth range near and far</span></span>                                                       |
| <span data-ttu-id="78558-150">Groupe d’attributs :</span><span class="sxs-lookup"><span data-stu-id="78558-150">Attribute group:</span></span> | <span data-ttu-id="78558-151">fenêtre d'affichage</span><span class="sxs-lookup"><span data-stu-id="78558-151">viewport</span></span>                                                                       |
| <span data-ttu-id="78558-152">Valeur initiale :</span><span class="sxs-lookup"><span data-stu-id="78558-152">Initial value:</span></span>   | <span data-ttu-id="78558-153">0, 1</span><span class="sxs-lookup"><span data-stu-id="78558-153">0, 1</span></span>                                                                           |
| <span data-ttu-id="78558-154">Commande d’extraction :</span><span class="sxs-lookup"><span data-stu-id="78558-154">Get command:</span></span>     | [<span data-ttu-id="78558-155">**glGetFloatv**</span><span class="sxs-lookup"><span data-stu-id="78558-155">**glGetFloatv**</span></span>](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) |



 

<span data-ttu-id="78558-156"></dd> <dt><span id="GL_MODELVIEW_STACK_DEPTH"></span><span id="gl_modelview_stack_depth"></span>profondeur de la \_ pile MODELVIEW GL \_ \_</dt> </span><span class="sxs-lookup"><span data-stu-id="78558-156"></dd> <dt><span id="GL_MODELVIEW_STACK_DEPTH"></span><span id="gl_modelview_stack_depth"></span>GL\_MODELVIEW\_STACK\_DEPTH</dt> </span></span><dd> 

| <span data-ttu-id="78558-157">Propriété</span><span class="sxs-lookup"><span data-stu-id="78558-157">Property</span></span> | <span data-ttu-id="78558-158">Valeur</span><span class="sxs-lookup"><span data-stu-id="78558-158">Value</span></span> |
|------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="78558-159">Description :</span><span class="sxs-lookup"><span data-stu-id="78558-159">Description:</span></span>     | <span data-ttu-id="78558-160">Pointeur de pile de matrices Modelview</span><span class="sxs-lookup"><span data-stu-id="78558-160">Modelview matrix stack pointer</span></span>                                                   |
| <span data-ttu-id="78558-161">Groupe d’attributs :</span><span class="sxs-lookup"><span data-stu-id="78558-161">Attribute group:</span></span> |                                                                                  |
| <span data-ttu-id="78558-162">Valeur initiale :</span><span class="sxs-lookup"><span data-stu-id="78558-162">Initial value:</span></span>   | <span data-ttu-id="78558-163">1</span><span class="sxs-lookup"><span data-stu-id="78558-163">1</span></span>                                                                                |
| <span data-ttu-id="78558-164">Commande d’extraction :</span><span class="sxs-lookup"><span data-stu-id="78558-164">Get command:</span></span>     | [<span data-ttu-id="78558-165">**glGetIntegerv**</span><span class="sxs-lookup"><span data-stu-id="78558-165">**glGetIntegerv**</span></span>](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) |



 

<span data-ttu-id="78558-166"></dd> <dt><span id="GL_PROJECTION_STACK_DEPTH"></span><span id="gl_projection_stack_depth"></span>profondeur de la \_ pile de projection GL \_ \_</dt> </span><span class="sxs-lookup"><span data-stu-id="78558-166"></dd> <dt><span id="GL_PROJECTION_STACK_DEPTH"></span><span id="gl_projection_stack_depth"></span>GL\_PROJECTION\_STACK\_DEPTH</dt> </span></span><dd> 

| <span data-ttu-id="78558-167">Propriété</span><span class="sxs-lookup"><span data-stu-id="78558-167">Property</span></span> | <span data-ttu-id="78558-168">Valeur</span><span class="sxs-lookup"><span data-stu-id="78558-168">Value</span></span> |
|------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="78558-169">Description :</span><span class="sxs-lookup"><span data-stu-id="78558-169">Description:</span></span>     | <span data-ttu-id="78558-170">Pointeur de pile de la matrice de projection</span><span class="sxs-lookup"><span data-stu-id="78558-170">Projection matrix stack pointer</span></span>                                                  |
| <span data-ttu-id="78558-171">Groupe d’attributs :</span><span class="sxs-lookup"><span data-stu-id="78558-171">Attribute group:</span></span> |                                                                                  |
| <span data-ttu-id="78558-172">Valeur initiale :</span><span class="sxs-lookup"><span data-stu-id="78558-172">Initial value:</span></span>   | <span data-ttu-id="78558-173">1</span><span class="sxs-lookup"><span data-stu-id="78558-173">1</span></span>                                                                                |
| <span data-ttu-id="78558-174">Commande d’extraction :</span><span class="sxs-lookup"><span data-stu-id="78558-174">Get command:</span></span>     | [<span data-ttu-id="78558-175">**glGetIntegerv**</span><span class="sxs-lookup"><span data-stu-id="78558-175">**glGetIntegerv**</span></span>](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) |



 

<span data-ttu-id="78558-176"></dd> <dt><span id="GL_TEXTURE_STACK_DEPTH"></span><span id="gl_texture_stack_depth"></span>profondeur de la \_ pile de textures GL \_ \_</dt> </span><span class="sxs-lookup"><span data-stu-id="78558-176"></dd> <dt><span id="GL_TEXTURE_STACK_DEPTH"></span><span id="gl_texture_stack_depth"></span>GL\_TEXTURE\_STACK\_DEPTH</dt> </span></span><dd> 

| <span data-ttu-id="78558-177">Propriété</span><span class="sxs-lookup"><span data-stu-id="78558-177">Property</span></span> | <span data-ttu-id="78558-178">Valeur</span><span class="sxs-lookup"><span data-stu-id="78558-178">Value</span></span> |
|------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="78558-179">Description :</span><span class="sxs-lookup"><span data-stu-id="78558-179">Description:</span></span>     | <span data-ttu-id="78558-180">Pointeur de pile de matrice de texture</span><span class="sxs-lookup"><span data-stu-id="78558-180">Texture matrix stack pointer</span></span>                                                     |
| <span data-ttu-id="78558-181">Groupe d’attributs :</span><span class="sxs-lookup"><span data-stu-id="78558-181">Attribute group:</span></span> |                                                                                  |
| <span data-ttu-id="78558-182">Valeur initiale :</span><span class="sxs-lookup"><span data-stu-id="78558-182">Initial value:</span></span>   | <span data-ttu-id="78558-183">1</span><span class="sxs-lookup"><span data-stu-id="78558-183">1</span></span>                                                                                |
| <span data-ttu-id="78558-184">Commande d’extraction :</span><span class="sxs-lookup"><span data-stu-id="78558-184">Get command:</span></span>     | [<span data-ttu-id="78558-185">**glGetIntegerv**</span><span class="sxs-lookup"><span data-stu-id="78558-185">**glGetIntegerv**</span></span>](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) |



 

<span data-ttu-id="78558-186"></dd> <dt><span id="GL_MATRIX_MODE"></span><span id="gl_matrix_mode"></span>\_mode de matrice du GL \_</dt> </span><span class="sxs-lookup"><span data-stu-id="78558-186"></dd> <dt><span id="GL_MATRIX_MODE"></span><span id="gl_matrix_mode"></span>GL\_MATRIX\_MODE</dt> </span></span><dd> 

| <span data-ttu-id="78558-187">Propriété</span><span class="sxs-lookup"><span data-stu-id="78558-187">Property</span></span> | <span data-ttu-id="78558-188">Valeur</span><span class="sxs-lookup"><span data-stu-id="78558-188">Value</span></span> |
|------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="78558-189">Description :</span><span class="sxs-lookup"><span data-stu-id="78558-189">Description:</span></span>     | <span data-ttu-id="78558-190">Mode matrice actuel</span><span class="sxs-lookup"><span data-stu-id="78558-190">Current matrix mode</span></span>                                                              |
| <span data-ttu-id="78558-191">Groupe d’attributs :</span><span class="sxs-lookup"><span data-stu-id="78558-191">Attribute group:</span></span> | <span data-ttu-id="78558-192">transformation</span><span class="sxs-lookup"><span data-stu-id="78558-192">transform</span></span>                                                                        |
| <span data-ttu-id="78558-193">Valeur initiale :</span><span class="sxs-lookup"><span data-stu-id="78558-193">Initial value:</span></span>   | <span data-ttu-id="78558-194">\_MODELVIEW GL</span><span class="sxs-lookup"><span data-stu-id="78558-194">GL\_MODELVIEW</span></span>                                                                    |
| <span data-ttu-id="78558-195">Commande d’extraction :</span><span class="sxs-lookup"><span data-stu-id="78558-195">Get command:</span></span>     | [<span data-ttu-id="78558-196">**glGetIntegerv**</span><span class="sxs-lookup"><span data-stu-id="78558-196">**glGetIntegerv**</span></span>](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) |



 

<span data-ttu-id="78558-197"></dd> <dt><span id="GL_NORMALIZE"></span><span id="gl_normalize"></span>normalisation du GL \_</dt> </span><span class="sxs-lookup"><span data-stu-id="78558-197"></dd> <dt><span id="GL_NORMALIZE"></span><span id="gl_normalize"></span>GL\_NORMALIZE</dt> </span></span><dd> 

| <span data-ttu-id="78558-198">Propriété</span><span class="sxs-lookup"><span data-stu-id="78558-198">Property</span></span> | <span data-ttu-id="78558-199">Valeur</span><span class="sxs-lookup"><span data-stu-id="78558-199">Value</span></span> |
|------------------|-------------------------------------|
| <span data-ttu-id="78558-200">Description :</span><span class="sxs-lookup"><span data-stu-id="78558-200">Description:</span></span>     | <span data-ttu-id="78558-201">Normalisation normale active/inactive</span><span class="sxs-lookup"><span data-stu-id="78558-201">Current normal normalization on/off</span></span> |
| <span data-ttu-id="78558-202">Groupe d’attributs :</span><span class="sxs-lookup"><span data-stu-id="78558-202">Attribute group:</span></span> | <span data-ttu-id="78558-203">transformation/activation</span><span class="sxs-lookup"><span data-stu-id="78558-203">transform/enable</span></span>                    |
| <span data-ttu-id="78558-204">Valeur initiale :</span><span class="sxs-lookup"><span data-stu-id="78558-204">Initial value:</span></span>   | <span data-ttu-id="78558-205">GL- \_ faux</span><span class="sxs-lookup"><span data-stu-id="78558-205">GL\_FALSE</span></span>                           |
| <span data-ttu-id="78558-206">Commande d’extraction :</span><span class="sxs-lookup"><span data-stu-id="78558-206">Get command:</span></span>     | [<span data-ttu-id="78558-207">**glIsEnabled**</span><span class="sxs-lookup"><span data-stu-id="78558-207">**glIsEnabled**</span></span>](glisenabled.md)  |



 

<span data-ttu-id="78558-208"></dd> <dt><span id="GL_CLIP_PLANE_i"></span><span id="gl_clip_plane_i"></span><span id="GL_CLIP_PLANE_I"></span>\_Plan de clip GL \_ *i*</dt> </span><span class="sxs-lookup"><span data-stu-id="78558-208"></dd> <dt><span id="GL_CLIP_PLANE_i"></span><span id="gl_clip_plane_i"></span><span id="GL_CLIP_PLANE_I"></span>GL\_CLIP\_PLANE *i*</dt> </span></span><dd> 

| <span data-ttu-id="78558-209">Propriété</span><span class="sxs-lookup"><span data-stu-id="78558-209">Property</span></span> | <span data-ttu-id="78558-210">Valeur</span><span class="sxs-lookup"><span data-stu-id="78558-210">Value</span></span> |
|------------------|------------------------------------------|
| <span data-ttu-id="78558-211">Description :</span><span class="sxs-lookup"><span data-stu-id="78558-211">Description:</span></span>     | <span data-ttu-id="78558-212">Coefficients de plan de découpage utilisateur</span><span class="sxs-lookup"><span data-stu-id="78558-212">User clipping plane coefficients</span></span>         |
| <span data-ttu-id="78558-213">Groupe d’attributs :</span><span class="sxs-lookup"><span data-stu-id="78558-213">Attribute group:</span></span> | <span data-ttu-id="78558-214">transformation</span><span class="sxs-lookup"><span data-stu-id="78558-214">transform</span></span>                                |
| <span data-ttu-id="78558-215">Valeur initiale :</span><span class="sxs-lookup"><span data-stu-id="78558-215">Initial value:</span></span>   | <span data-ttu-id="78558-216">0, 0, 0, 0</span><span class="sxs-lookup"><span data-stu-id="78558-216">0, 0, 0, 0</span></span>                               |
| <span data-ttu-id="78558-217">Commande d’extraction :</span><span class="sxs-lookup"><span data-stu-id="78558-217">Get command:</span></span>     | [<span data-ttu-id="78558-218">**glGetClipPlane**</span><span class="sxs-lookup"><span data-stu-id="78558-218">**glGetClipPlane**</span></span>](glgetclipplane.md) |



 

<span data-ttu-id="78558-219"></dd> <dt><span id="GL_CLIP_PLANE_i"></span><span id="gl_clip_plane_i"></span><span id="GL_CLIP_PLANE_I"></span>\_Plan de clip GL \_ *i*</dt> </span><span class="sxs-lookup"><span data-stu-id="78558-219"></dd> <dt><span id="GL_CLIP_PLANE_i"></span><span id="gl_clip_plane_i"></span><span id="GL_CLIP_PLANE_I"></span>GL\_CLIP\_PLANE *i*</dt> </span></span><dd> 

| <span data-ttu-id="78558-220">Propriété</span><span class="sxs-lookup"><span data-stu-id="78558-220">Property</span></span> | <span data-ttu-id="78558-221">Valeur</span><span class="sxs-lookup"><span data-stu-id="78558-221">Value</span></span> |
|------------------|------------------------------------|
| <span data-ttu-id="78558-222">Description :</span><span class="sxs-lookup"><span data-stu-id="78558-222">Description:</span></span>     | <span data-ttu-id="78558-223">*mon* plan de découpage d’utilisateur est activé</span><span class="sxs-lookup"><span data-stu-id="78558-223">*i* th user clipping plane enabled</span></span> |
| <span data-ttu-id="78558-224">Groupe d’attributs :</span><span class="sxs-lookup"><span data-stu-id="78558-224">Attribute group:</span></span> | <span data-ttu-id="78558-225">transformation/activation</span><span class="sxs-lookup"><span data-stu-id="78558-225">transform/enable</span></span>                   |
| <span data-ttu-id="78558-226">Valeur initiale :</span><span class="sxs-lookup"><span data-stu-id="78558-226">Initial value:</span></span>   | <span data-ttu-id="78558-227">GL- \_ faux</span><span class="sxs-lookup"><span data-stu-id="78558-227">GL\_FALSE</span></span>                          |
| <span data-ttu-id="78558-228">Commande d’extraction :</span><span class="sxs-lookup"><span data-stu-id="78558-228">Get command:</span></span>     | [<span data-ttu-id="78558-229">**glIsEnabled**</span><span class="sxs-lookup"><span data-stu-id="78558-229">**glIsEnabled**</span></span>](glisenabled.md) |



 

</dd> </dl>

 

 




