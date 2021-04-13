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
ms.openlocfilehash: 3434fe9f9aa528aa8d201b56ed363753c594690f
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/25/2019
ms.locfileid: "104312736"
---
# <a name="transformation-state-variables"></a><span data-ttu-id="19680-104">Variables d’état de transformation</span><span class="sxs-lookup"><span data-stu-id="19680-104">Transformation State Variables</span></span>

<dl> <span data-ttu-id="19680-105"><dt><span id="GL_MODELVIEW_MATRIX"></span><span id="gl_modelview_matrix"></span>\_matrice MODELVIEW \_ GL</dt> </span><span class="sxs-lookup"><span data-stu-id="19680-105"><dt><span id="GL_MODELVIEW_MATRIX"></span><span id="gl_modelview_matrix"></span>GL\_MODELVIEW\_MATRIX</dt> </span></span><dd> 

|                  |                                    |
|------------------|------------------------------------|
| <span data-ttu-id="19680-106">Description :</span><span class="sxs-lookup"><span data-stu-id="19680-106">Description:</span></span>     | <span data-ttu-id="19680-107">Pile de matrices Modelview</span><span class="sxs-lookup"><span data-stu-id="19680-107">Modelview matrix stack</span></span>             |
| <span data-ttu-id="19680-108">Groupe d’attributs :</span><span class="sxs-lookup"><span data-stu-id="19680-108">Attribute group:</span></span> |                                    |
| <span data-ttu-id="19680-109">Valeur initiale :</span><span class="sxs-lookup"><span data-stu-id="19680-109">Initial value:</span></span>   | <span data-ttu-id="19680-110">Identité</span><span class="sxs-lookup"><span data-stu-id="19680-110">Identity</span></span>                           |
| <span data-ttu-id="19680-111">Commande d’extraction :</span><span class="sxs-lookup"><span data-stu-id="19680-111">Get command:</span></span>     | [<span data-ttu-id="19680-112">**glGetFloatv**</span><span class="sxs-lookup"><span data-stu-id="19680-112">**glGetFloatv**</span></span>](glgetfloatv.md) |



 

<span data-ttu-id="19680-113"></dd> <dt><span id="GL_PROJECTION_MATRIX"></span><span id="gl_projection_matrix"></span>\_matrice de projection GL \_</dt> </span><span class="sxs-lookup"><span data-stu-id="19680-113"></dd> <dt><span id="GL_PROJECTION_MATRIX"></span><span id="gl_projection_matrix"></span>GL\_PROJECTION\_MATRIX</dt> </span></span><dd> 

|                  |                                                                                |
|------------------|--------------------------------------------------------------------------------|
| <span data-ttu-id="19680-114">Description :</span><span class="sxs-lookup"><span data-stu-id="19680-114">Description:</span></span>     | <span data-ttu-id="19680-115">Pile de matrice de projection</span><span class="sxs-lookup"><span data-stu-id="19680-115">Projection matrix stack</span></span>                                                        |
| <span data-ttu-id="19680-116">Groupe d’attributs :</span><span class="sxs-lookup"><span data-stu-id="19680-116">Attribute group:</span></span> |                                                                                |
| <span data-ttu-id="19680-117">Valeur initiale :</span><span class="sxs-lookup"><span data-stu-id="19680-117">Initial value:</span></span>   | <span data-ttu-id="19680-118">Identité</span><span class="sxs-lookup"><span data-stu-id="19680-118">Identity</span></span>                                                                       |
| <span data-ttu-id="19680-119">Commande d’extraction :</span><span class="sxs-lookup"><span data-stu-id="19680-119">Get command:</span></span>     | [<span data-ttu-id="19680-120">**glGetFloatv**</span><span class="sxs-lookup"><span data-stu-id="19680-120">**glGetFloatv**</span></span>](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) |



 

<span data-ttu-id="19680-121"></dd> <dt><span id="GL_TEXTURE_MATRIX"></span><span id="gl_texture_matrix"></span>\_matrice de texture GL \_</dt> </span><span class="sxs-lookup"><span data-stu-id="19680-121"></dd> <dt><span id="GL_TEXTURE_MATRIX"></span><span id="gl_texture_matrix"></span>GL\_TEXTURE\_MATRIX</dt> </span></span><dd> 

|                  |                                                                                |
|------------------|--------------------------------------------------------------------------------|
| <span data-ttu-id="19680-122">Description :</span><span class="sxs-lookup"><span data-stu-id="19680-122">Description:</span></span>     | <span data-ttu-id="19680-123">Pile de matrices de texture</span><span class="sxs-lookup"><span data-stu-id="19680-123">Texture matrix stack</span></span>                                                           |
| <span data-ttu-id="19680-124">Groupe d’attributs :</span><span class="sxs-lookup"><span data-stu-id="19680-124">Attribute group:</span></span> |                                                                                |
| <span data-ttu-id="19680-125">Valeur initiale :</span><span class="sxs-lookup"><span data-stu-id="19680-125">Initial value:</span></span>   | <span data-ttu-id="19680-126">Identité</span><span class="sxs-lookup"><span data-stu-id="19680-126">Identity</span></span>                                                                       |
| <span data-ttu-id="19680-127">Commande d’extraction :</span><span class="sxs-lookup"><span data-stu-id="19680-127">Get command:</span></span>     | [<span data-ttu-id="19680-128">**glGetFloatv**</span><span class="sxs-lookup"><span data-stu-id="19680-128">**glGetFloatv**</span></span>](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) |



 

<span data-ttu-id="19680-129"></dd> <dt><span id="GL_VIEWPORT"></span><span id="gl_viewport"></span>\_fenêtre d’affichage comptabilité</dt> </span><span class="sxs-lookup"><span data-stu-id="19680-129"></dd> <dt><span id="GL_VIEWPORT"></span><span id="gl_viewport"></span>GL\_VIEWPORT</dt> </span></span><dd> 

|                  |                                                                                  |
|------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="19680-130">Description :</span><span class="sxs-lookup"><span data-stu-id="19680-130">Description:</span></span>     | <span data-ttu-id="19680-131">Origine de la fenêtre d’affichage et étendue</span><span class="sxs-lookup"><span data-stu-id="19680-131">Viewport origin and extent</span></span>                                                       |
| <span data-ttu-id="19680-132">Groupe d’attributs :</span><span class="sxs-lookup"><span data-stu-id="19680-132">Attribute group:</span></span> | <span data-ttu-id="19680-133">fenêtre d'affichage</span><span class="sxs-lookup"><span data-stu-id="19680-133">viewport</span></span>                                                                         |
| <span data-ttu-id="19680-134">Valeur initiale :</span><span class="sxs-lookup"><span data-stu-id="19680-134">Initial value:</span></span>   |                                                                                  |
| <span data-ttu-id="19680-135">Commande d’extraction :</span><span class="sxs-lookup"><span data-stu-id="19680-135">Get command:</span></span>     | [<span data-ttu-id="19680-136">**glGetIntegerv**</span><span class="sxs-lookup"><span data-stu-id="19680-136">**glGetIntegerv**</span></span>](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) |



 

<span data-ttu-id="19680-137"></dd> <dt><span id="GL_DEPTH_RANGE"></span><span id="gl_depth_range"></span>\_plage de profondeur GL \_</dt> </span><span class="sxs-lookup"><span data-stu-id="19680-137"></dd> <dt><span id="GL_DEPTH_RANGE"></span><span id="gl_depth_range"></span>GL\_DEPTH\_RANGE</dt> </span></span><dd> 

|                  |                                                                                |
|------------------|--------------------------------------------------------------------------------|
| <span data-ttu-id="19680-138">Description :</span><span class="sxs-lookup"><span data-stu-id="19680-138">Description:</span></span>     | <span data-ttu-id="19680-139">Plage de profondeur proche et éloignée</span><span class="sxs-lookup"><span data-stu-id="19680-139">Depth range near and far</span></span>                                                       |
| <span data-ttu-id="19680-140">Groupe d’attributs :</span><span class="sxs-lookup"><span data-stu-id="19680-140">Attribute group:</span></span> | <span data-ttu-id="19680-141">fenêtre d'affichage</span><span class="sxs-lookup"><span data-stu-id="19680-141">viewport</span></span>                                                                       |
| <span data-ttu-id="19680-142">Valeur initiale :</span><span class="sxs-lookup"><span data-stu-id="19680-142">Initial value:</span></span>   | <span data-ttu-id="19680-143">0, 1</span><span class="sxs-lookup"><span data-stu-id="19680-143">0, 1</span></span>                                                                           |
| <span data-ttu-id="19680-144">Commande d’extraction :</span><span class="sxs-lookup"><span data-stu-id="19680-144">Get command:</span></span>     | [<span data-ttu-id="19680-145">**glGetFloatv**</span><span class="sxs-lookup"><span data-stu-id="19680-145">**glGetFloatv**</span></span>](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) |



 

<span data-ttu-id="19680-146"></dd> <dt><span id="GL_MODELVIEW_STACK_DEPTH"></span><span id="gl_modelview_stack_depth"></span>profondeur de la \_ pile MODELVIEW GL \_ \_</dt> </span><span class="sxs-lookup"><span data-stu-id="19680-146"></dd> <dt><span id="GL_MODELVIEW_STACK_DEPTH"></span><span id="gl_modelview_stack_depth"></span>GL\_MODELVIEW\_STACK\_DEPTH</dt> </span></span><dd> 

|                  |                                                                                  |
|------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="19680-147">Description :</span><span class="sxs-lookup"><span data-stu-id="19680-147">Description:</span></span>     | <span data-ttu-id="19680-148">Pointeur de pile de matrices Modelview</span><span class="sxs-lookup"><span data-stu-id="19680-148">Modelview matrix stack pointer</span></span>                                                   |
| <span data-ttu-id="19680-149">Groupe d’attributs :</span><span class="sxs-lookup"><span data-stu-id="19680-149">Attribute group:</span></span> |                                                                                  |
| <span data-ttu-id="19680-150">Valeur initiale :</span><span class="sxs-lookup"><span data-stu-id="19680-150">Initial value:</span></span>   | <span data-ttu-id="19680-151">1</span><span class="sxs-lookup"><span data-stu-id="19680-151">1</span></span>                                                                                |
| <span data-ttu-id="19680-152">Commande d’extraction :</span><span class="sxs-lookup"><span data-stu-id="19680-152">Get command:</span></span>     | [<span data-ttu-id="19680-153">**glGetIntegerv**</span><span class="sxs-lookup"><span data-stu-id="19680-153">**glGetIntegerv**</span></span>](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) |



 

<span data-ttu-id="19680-154"></dd> <dt><span id="GL_PROJECTION_STACK_DEPTH"></span><span id="gl_projection_stack_depth"></span>profondeur de la \_ pile de projection GL \_ \_</dt> </span><span class="sxs-lookup"><span data-stu-id="19680-154"></dd> <dt><span id="GL_PROJECTION_STACK_DEPTH"></span><span id="gl_projection_stack_depth"></span>GL\_PROJECTION\_STACK\_DEPTH</dt> </span></span><dd> 

|                  |                                                                                  |
|------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="19680-155">Description :</span><span class="sxs-lookup"><span data-stu-id="19680-155">Description:</span></span>     | <span data-ttu-id="19680-156">Pointeur de pile de la matrice de projection</span><span class="sxs-lookup"><span data-stu-id="19680-156">Projection matrix stack pointer</span></span>                                                  |
| <span data-ttu-id="19680-157">Groupe d’attributs :</span><span class="sxs-lookup"><span data-stu-id="19680-157">Attribute group:</span></span> |                                                                                  |
| <span data-ttu-id="19680-158">Valeur initiale :</span><span class="sxs-lookup"><span data-stu-id="19680-158">Initial value:</span></span>   | <span data-ttu-id="19680-159">1</span><span class="sxs-lookup"><span data-stu-id="19680-159">1</span></span>                                                                                |
| <span data-ttu-id="19680-160">Commande d’extraction :</span><span class="sxs-lookup"><span data-stu-id="19680-160">Get command:</span></span>     | [<span data-ttu-id="19680-161">**glGetIntegerv**</span><span class="sxs-lookup"><span data-stu-id="19680-161">**glGetIntegerv**</span></span>](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) |



 

<span data-ttu-id="19680-162"></dd> <dt><span id="GL_TEXTURE_STACK_DEPTH"></span><span id="gl_texture_stack_depth"></span>profondeur de la \_ pile de textures GL \_ \_</dt> </span><span class="sxs-lookup"><span data-stu-id="19680-162"></dd> <dt><span id="GL_TEXTURE_STACK_DEPTH"></span><span id="gl_texture_stack_depth"></span>GL\_TEXTURE\_STACK\_DEPTH</dt> </span></span><dd> 

|                  |                                                                                  |
|------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="19680-163">Description :</span><span class="sxs-lookup"><span data-stu-id="19680-163">Description:</span></span>     | <span data-ttu-id="19680-164">Pointeur de pile de matrice de texture</span><span class="sxs-lookup"><span data-stu-id="19680-164">Texture matrix stack pointer</span></span>                                                     |
| <span data-ttu-id="19680-165">Groupe d’attributs :</span><span class="sxs-lookup"><span data-stu-id="19680-165">Attribute group:</span></span> |                                                                                  |
| <span data-ttu-id="19680-166">Valeur initiale :</span><span class="sxs-lookup"><span data-stu-id="19680-166">Initial value:</span></span>   | <span data-ttu-id="19680-167">1</span><span class="sxs-lookup"><span data-stu-id="19680-167">1</span></span>                                                                                |
| <span data-ttu-id="19680-168">Commande d’extraction :</span><span class="sxs-lookup"><span data-stu-id="19680-168">Get command:</span></span>     | [<span data-ttu-id="19680-169">**glGetIntegerv**</span><span class="sxs-lookup"><span data-stu-id="19680-169">**glGetIntegerv**</span></span>](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) |



 

<span data-ttu-id="19680-170"></dd> <dt><span id="GL_MATRIX_MODE"></span><span id="gl_matrix_mode"></span>\_mode de matrice du GL \_</dt> </span><span class="sxs-lookup"><span data-stu-id="19680-170"></dd> <dt><span id="GL_MATRIX_MODE"></span><span id="gl_matrix_mode"></span>GL\_MATRIX\_MODE</dt> </span></span><dd> 

|                  |                                                                                  |
|------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="19680-171">Description :</span><span class="sxs-lookup"><span data-stu-id="19680-171">Description:</span></span>     | <span data-ttu-id="19680-172">Mode matrice actuel</span><span class="sxs-lookup"><span data-stu-id="19680-172">Current matrix mode</span></span>                                                              |
| <span data-ttu-id="19680-173">Groupe d’attributs :</span><span class="sxs-lookup"><span data-stu-id="19680-173">Attribute group:</span></span> | <span data-ttu-id="19680-174">transformation</span><span class="sxs-lookup"><span data-stu-id="19680-174">transform</span></span>                                                                        |
| <span data-ttu-id="19680-175">Valeur initiale :</span><span class="sxs-lookup"><span data-stu-id="19680-175">Initial value:</span></span>   | <span data-ttu-id="19680-176">\_MODELVIEW GL</span><span class="sxs-lookup"><span data-stu-id="19680-176">GL\_MODELVIEW</span></span>                                                                    |
| <span data-ttu-id="19680-177">Commande d’extraction :</span><span class="sxs-lookup"><span data-stu-id="19680-177">Get command:</span></span>     | [<span data-ttu-id="19680-178">**glGetIntegerv**</span><span class="sxs-lookup"><span data-stu-id="19680-178">**glGetIntegerv**</span></span>](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) |



 

<span data-ttu-id="19680-179"></dd> <dt><span id="GL_NORMALIZE"></span><span id="gl_normalize"></span>normalisation du GL \_</dt> </span><span class="sxs-lookup"><span data-stu-id="19680-179"></dd> <dt><span id="GL_NORMALIZE"></span><span id="gl_normalize"></span>GL\_NORMALIZE</dt> </span></span><dd> 

|                  |                                     |
|------------------|-------------------------------------|
| <span data-ttu-id="19680-180">Description :</span><span class="sxs-lookup"><span data-stu-id="19680-180">Description:</span></span>     | <span data-ttu-id="19680-181">Normalisation normale active/inactive</span><span class="sxs-lookup"><span data-stu-id="19680-181">Current normal normalization on/off</span></span> |
| <span data-ttu-id="19680-182">Groupe d’attributs :</span><span class="sxs-lookup"><span data-stu-id="19680-182">Attribute group:</span></span> | <span data-ttu-id="19680-183">transformation/activation</span><span class="sxs-lookup"><span data-stu-id="19680-183">transform/enable</span></span>                    |
| <span data-ttu-id="19680-184">Valeur initiale :</span><span class="sxs-lookup"><span data-stu-id="19680-184">Initial value:</span></span>   | <span data-ttu-id="19680-185">GL- \_ faux</span><span class="sxs-lookup"><span data-stu-id="19680-185">GL\_FALSE</span></span>                           |
| <span data-ttu-id="19680-186">Commande d’extraction :</span><span class="sxs-lookup"><span data-stu-id="19680-186">Get command:</span></span>     | [<span data-ttu-id="19680-187">**glIsEnabled**</span><span class="sxs-lookup"><span data-stu-id="19680-187">**glIsEnabled**</span></span>](glisenabled.md)  |



 

<span data-ttu-id="19680-188"></dd> <dt><span id="GL_CLIP_PLANE_i"></span><span id="gl_clip_plane_i"></span><span id="GL_CLIP_PLANE_I"></span>\_Plan de clip GL \_ *i*</dt> </span><span class="sxs-lookup"><span data-stu-id="19680-188"></dd> <dt><span id="GL_CLIP_PLANE_i"></span><span id="gl_clip_plane_i"></span><span id="GL_CLIP_PLANE_I"></span>GL\_CLIP\_PLANE *i*</dt> </span></span><dd> 

|                  |                                          |
|------------------|------------------------------------------|
| <span data-ttu-id="19680-189">Description :</span><span class="sxs-lookup"><span data-stu-id="19680-189">Description:</span></span>     | <span data-ttu-id="19680-190">Coefficients de plan de découpage utilisateur</span><span class="sxs-lookup"><span data-stu-id="19680-190">User clipping plane coefficients</span></span>         |
| <span data-ttu-id="19680-191">Groupe d’attributs :</span><span class="sxs-lookup"><span data-stu-id="19680-191">Attribute group:</span></span> | <span data-ttu-id="19680-192">transformation</span><span class="sxs-lookup"><span data-stu-id="19680-192">transform</span></span>                                |
| <span data-ttu-id="19680-193">Valeur initiale :</span><span class="sxs-lookup"><span data-stu-id="19680-193">Initial value:</span></span>   | <span data-ttu-id="19680-194">0, 0, 0, 0</span><span class="sxs-lookup"><span data-stu-id="19680-194">0, 0, 0, 0</span></span>                               |
| <span data-ttu-id="19680-195">Commande d’extraction :</span><span class="sxs-lookup"><span data-stu-id="19680-195">Get command:</span></span>     | [<span data-ttu-id="19680-196">**glGetClipPlane**</span><span class="sxs-lookup"><span data-stu-id="19680-196">**glGetClipPlane**</span></span>](glgetclipplane.md) |



 

<span data-ttu-id="19680-197"></dd> <dt><span id="GL_CLIP_PLANE_i"></span><span id="gl_clip_plane_i"></span><span id="GL_CLIP_PLANE_I"></span>\_Plan de clip GL \_ *i*</dt> </span><span class="sxs-lookup"><span data-stu-id="19680-197"></dd> <dt><span id="GL_CLIP_PLANE_i"></span><span id="gl_clip_plane_i"></span><span id="GL_CLIP_PLANE_I"></span>GL\_CLIP\_PLANE *i*</dt> </span></span><dd> 

|                  |                                    |
|------------------|------------------------------------|
| <span data-ttu-id="19680-198">Description :</span><span class="sxs-lookup"><span data-stu-id="19680-198">Description:</span></span>     | <span data-ttu-id="19680-199">*mon* plan de découpage d’utilisateur est activé</span><span class="sxs-lookup"><span data-stu-id="19680-199">*i* th user clipping plane enabled</span></span> |
| <span data-ttu-id="19680-200">Groupe d’attributs :</span><span class="sxs-lookup"><span data-stu-id="19680-200">Attribute group:</span></span> | <span data-ttu-id="19680-201">transformation/activation</span><span class="sxs-lookup"><span data-stu-id="19680-201">transform/enable</span></span>                   |
| <span data-ttu-id="19680-202">Valeur initiale :</span><span class="sxs-lookup"><span data-stu-id="19680-202">Initial value:</span></span>   | <span data-ttu-id="19680-203">GL- \_ faux</span><span class="sxs-lookup"><span data-stu-id="19680-203">GL\_FALSE</span></span>                          |
| <span data-ttu-id="19680-204">Commande d’extraction :</span><span class="sxs-lookup"><span data-stu-id="19680-204">Get command:</span></span>     | [<span data-ttu-id="19680-205">**glIsEnabled**</span><span class="sxs-lookup"><span data-stu-id="19680-205">**glIsEnabled**</span></span>](glisenabled.md) |



 

</dd> </dl>

 

 




