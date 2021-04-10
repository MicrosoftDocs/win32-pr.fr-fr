---
title: Variables d’État Implementation-Dependent
description: Variables d’État Implementation-Dependent
ms.assetid: 6778b50c-a6ac-4106-9dd6-3a123c257687
keywords:
- Variables d’État Implementation-Dependent OpenGL
topic_type:
- apiref
api_name:
- Implementation-Dependent State Variables
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: afb42c13765678218efcaf58f2b02a01d2f0e160
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/25/2019
ms.locfileid: "104030252"
---
# <a name="implementation-dependent-state-variables"></a><span data-ttu-id="b5e81-104">Variables d’État Implementation-Dependent</span><span class="sxs-lookup"><span data-stu-id="b5e81-104">Implementation-Dependent State Variables</span></span>

<dl> <span data-ttu-id="b5e81-105"><dt><span id="GL_MAX_LIGHTS"></span><span id="gl_max_lights"></span>\_lumières max. GL \_</dt> </span><span class="sxs-lookup"><span data-stu-id="b5e81-105"><dt><span id="GL_MAX_LIGHTS"></span><span id="gl_max_lights"></span>GL\_MAX\_LIGHTS</dt> </span></span><dd> 

|                  |                                        |
|------------------|----------------------------------------|
| <span data-ttu-id="b5e81-106">Description :</span><span class="sxs-lookup"><span data-stu-id="b5e81-106">Description:</span></span>     | <span data-ttu-id="b5e81-107">Nombre maximal d’éclairages</span><span class="sxs-lookup"><span data-stu-id="b5e81-107">Maximum number of lights</span></span>               |
| <span data-ttu-id="b5e81-108">Groupe d’attributs :</span><span class="sxs-lookup"><span data-stu-id="b5e81-108">Attribute group:</span></span> |                                        |
| <span data-ttu-id="b5e81-109">Valeur initiale :</span><span class="sxs-lookup"><span data-stu-id="b5e81-109">Initial value:</span></span>   | <span data-ttu-id="b5e81-110">8</span><span class="sxs-lookup"><span data-stu-id="b5e81-110">8</span></span>                                      |
| <span data-ttu-id="b5e81-111">Commande d’extraction :</span><span class="sxs-lookup"><span data-stu-id="b5e81-111">Get command:</span></span>     | [<span data-ttu-id="b5e81-112">**glGetIntegerv**</span><span class="sxs-lookup"><span data-stu-id="b5e81-112">**glGetIntegerv**</span></span>](glgetintegerv.md) |



 

<span data-ttu-id="b5e81-113"></dd> <dt><span id="GL_MAX_CLIP_PLANES"></span><span id="gl_max_clip_planes"></span>\_plans de \_ clips \_ Max GL</dt> </span><span class="sxs-lookup"><span data-stu-id="b5e81-113"></dd> <dt><span id="GL_MAX_CLIP_PLANES"></span><span id="gl_max_clip_planes"></span>GL\_MAX\_CLIP\_PLANES</dt> </span></span><dd> 

|                  |                                                                                  |
|------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="b5e81-114">Description :</span><span class="sxs-lookup"><span data-stu-id="b5e81-114">Description:</span></span>     | <span data-ttu-id="b5e81-115">Nombre maximal de plans de découpage de l’utilisateur</span><span class="sxs-lookup"><span data-stu-id="b5e81-115">Maximum number of user clipping planes</span></span>                                           |
| <span data-ttu-id="b5e81-116">Groupe d’attributs :</span><span class="sxs-lookup"><span data-stu-id="b5e81-116">Attribute group:</span></span> |                                                                                  |
| <span data-ttu-id="b5e81-117">Valeur initiale :</span><span class="sxs-lookup"><span data-stu-id="b5e81-117">Initial value:</span></span>   | <span data-ttu-id="b5e81-118">6</span><span class="sxs-lookup"><span data-stu-id="b5e81-118">6</span></span>                                                                                |
| <span data-ttu-id="b5e81-119">Commande d’extraction :</span><span class="sxs-lookup"><span data-stu-id="b5e81-119">Get command:</span></span>     | [<span data-ttu-id="b5e81-120">**glGetIntegerv**</span><span class="sxs-lookup"><span data-stu-id="b5e81-120">**glGetIntegerv**</span></span>](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) |



 

<span data-ttu-id="b5e81-121"></dd> <dt><span id="GL_MAX_MODELVIEW_STACK_DEPTH"></span><span id="gl_max_modelview_stack_depth"></span>\_profondeur de \_ la \_ pile \_ MODELVIEW GL Max</dt> </span><span class="sxs-lookup"><span data-stu-id="b5e81-121"></dd> <dt><span id="GL_MAX_MODELVIEW_STACK_DEPTH"></span><span id="gl_max_modelview_stack_depth"></span>GL\_MAX\_MODELVIEW\_STACK\_DEPTH</dt> </span></span><dd> 

|                  |                                                                                  |
|------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="b5e81-122">Description :</span><span class="sxs-lookup"><span data-stu-id="b5e81-122">Description:</span></span>     | <span data-ttu-id="b5e81-123">Profondeur maximale de la pile modelview-Matrix</span><span class="sxs-lookup"><span data-stu-id="b5e81-123">Maximum modelview-matrix stack depth</span></span>                                             |
| <span data-ttu-id="b5e81-124">Groupe d’attributs :</span><span class="sxs-lookup"><span data-stu-id="b5e81-124">Attribute group:</span></span> |                                                                                  |
| <span data-ttu-id="b5e81-125">Valeur initiale :</span><span class="sxs-lookup"><span data-stu-id="b5e81-125">Initial value:</span></span>   | <span data-ttu-id="b5e81-126">32</span><span class="sxs-lookup"><span data-stu-id="b5e81-126">32</span></span>                                                                               |
| <span data-ttu-id="b5e81-127">Commande d’extraction :</span><span class="sxs-lookup"><span data-stu-id="b5e81-127">Get command:</span></span>     | [<span data-ttu-id="b5e81-128">**glGetIntegerv**</span><span class="sxs-lookup"><span data-stu-id="b5e81-128">**glGetIntegerv**</span></span>](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) |



 

<span data-ttu-id="b5e81-129"></dd> <dt><span id="GL_MAX_PROJECTION_STACK_DEPTH"></span><span id="gl_max_projection_stack_depth"></span>profondeur de la \_ \_ pile de projection Max \_ GL \_</dt> </span><span class="sxs-lookup"><span data-stu-id="b5e81-129"></dd> <dt><span id="GL_MAX_PROJECTION_STACK_DEPTH"></span><span id="gl_max_projection_stack_depth"></span>GL\_MAX\_PROJECTION\_STACK\_DEPTH</dt> </span></span><dd> 

|                  |                                                                                  |
|------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="b5e81-130">Description :</span><span class="sxs-lookup"><span data-stu-id="b5e81-130">Description:</span></span>     | <span data-ttu-id="b5e81-131">Profondeur maximale de la pile de projection</span><span class="sxs-lookup"><span data-stu-id="b5e81-131">Maximum projection-matrix stack depth</span></span>                                            |
| <span data-ttu-id="b5e81-132">Groupe d’attributs :</span><span class="sxs-lookup"><span data-stu-id="b5e81-132">Attribute group:</span></span> |                                                                                  |
| <span data-ttu-id="b5e81-133">Valeur initiale :</span><span class="sxs-lookup"><span data-stu-id="b5e81-133">Initial value:</span></span>   | <span data-ttu-id="b5e81-134">2</span><span class="sxs-lookup"><span data-stu-id="b5e81-134">2</span></span>                                                                                |
| <span data-ttu-id="b5e81-135">Commande d’extraction :</span><span class="sxs-lookup"><span data-stu-id="b5e81-135">Get command:</span></span>     | [<span data-ttu-id="b5e81-136">**glGetIntegerv**</span><span class="sxs-lookup"><span data-stu-id="b5e81-136">**glGetIntegerv**</span></span>](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) |



 

<span data-ttu-id="b5e81-137"></dd> <dt><span id="GL_MAX_TEXTURE_STACK_DEPTH"></span><span id="gl_max_texture_stack_depth"></span>profondeur de la \_ \_ pile de texture Max \_ . GL \_</dt> </span><span class="sxs-lookup"><span data-stu-id="b5e81-137"></dd> <dt><span id="GL_MAX_TEXTURE_STACK_DEPTH"></span><span id="gl_max_texture_stack_depth"></span>GL\_MAX\_TEXTURE\_STACK\_DEPTH</dt> </span></span><dd> 

|                  |                                                                                  |
|------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="b5e81-138">Description :</span><span class="sxs-lookup"><span data-stu-id="b5e81-138">Description:</span></span>     | <span data-ttu-id="b5e81-139">Profondeur maximale de la pile de matrices de texture</span><span class="sxs-lookup"><span data-stu-id="b5e81-139">Maximum depth of texture matrix stack</span></span>                                            |
| <span data-ttu-id="b5e81-140">Groupe d’attributs :</span><span class="sxs-lookup"><span data-stu-id="b5e81-140">Attribute group:</span></span> |                                                                                  |
| <span data-ttu-id="b5e81-141">Valeur initiale :</span><span class="sxs-lookup"><span data-stu-id="b5e81-141">Initial value:</span></span>   | <span data-ttu-id="b5e81-142">2</span><span class="sxs-lookup"><span data-stu-id="b5e81-142">2</span></span>                                                                                |
| <span data-ttu-id="b5e81-143">Commande d’extraction :</span><span class="sxs-lookup"><span data-stu-id="b5e81-143">Get command:</span></span>     | [<span data-ttu-id="b5e81-144">**glGetIntegerv**</span><span class="sxs-lookup"><span data-stu-id="b5e81-144">**glGetIntegerv**</span></span>](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) |



 

<span data-ttu-id="b5e81-145"></dd> <dt><span id="GL_SUBPIXEL_BITS"></span><span id="gl_subpixel_bits"></span>BITS de sous- \_ Pixel GL \_</dt> </span><span class="sxs-lookup"><span data-stu-id="b5e81-145"></dd> <dt><span id="GL_SUBPIXEL_BITS"></span><span id="gl_subpixel_bits"></span>GL\_SUBPIXEL\_BITS</dt> </span></span><dd> 

|                  |                                                                                  |
|------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="b5e81-146">Description :</span><span class="sxs-lookup"><span data-stu-id="b5e81-146">Description:</span></span>     | <span data-ttu-id="b5e81-147">Nombre de bits de précision de sous-pixel dans *x*   et *y*</span><span class="sxs-lookup"><span data-stu-id="b5e81-147">Number of bits of subpixel precision in *x* and *y*</span></span>                              |
| <span data-ttu-id="b5e81-148">Groupe d’attributs :</span><span class="sxs-lookup"><span data-stu-id="b5e81-148">Attribute group:</span></span> |                                                                                  |
| <span data-ttu-id="b5e81-149">Valeur initiale :</span><span class="sxs-lookup"><span data-stu-id="b5e81-149">Initial value:</span></span>   | <span data-ttu-id="b5e81-150">4</span><span class="sxs-lookup"><span data-stu-id="b5e81-150">4</span></span>                                                                                |
| <span data-ttu-id="b5e81-151">Commande d’extraction :</span><span class="sxs-lookup"><span data-stu-id="b5e81-151">Get command:</span></span>     | [<span data-ttu-id="b5e81-152">**glGetIntegerv**</span><span class="sxs-lookup"><span data-stu-id="b5e81-152">**glGetIntegerv**</span></span>](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) |



 

<span data-ttu-id="b5e81-153"></dd> <dt><span id="GL_MAX_TEXTURE_SIZE"></span><span id="gl_max_texture_size"></span>\_taille maximale de la \_ texture GL \_</dt> </span><span class="sxs-lookup"><span data-stu-id="b5e81-153"></dd> <dt><span id="GL_MAX_TEXTURE_SIZE"></span><span id="gl_max_texture_size"></span>GL\_MAX\_TEXTURE\_SIZE</dt> </span></span><dd> 

|                  |                                                                                  |
|------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="b5e81-154">Description :</span><span class="sxs-lookup"><span data-stu-id="b5e81-154">Description:</span></span>     | <span data-ttu-id="b5e81-155">Hauteur ou largeur maximale d’une image de texture (sans bordure)</span><span class="sxs-lookup"><span data-stu-id="b5e81-155">Maximum height or width of a texture image (without borders)</span></span>                     |
| <span data-ttu-id="b5e81-156">Groupe d’attributs :</span><span class="sxs-lookup"><span data-stu-id="b5e81-156">Attribute group:</span></span> |                                                                                  |
| <span data-ttu-id="b5e81-157">Valeur initiale :</span><span class="sxs-lookup"><span data-stu-id="b5e81-157">Initial value:</span></span>   | <span data-ttu-id="b5e81-158">64</span><span class="sxs-lookup"><span data-stu-id="b5e81-158">64</span></span>                                                                               |
| <span data-ttu-id="b5e81-159">Commande d’extraction :</span><span class="sxs-lookup"><span data-stu-id="b5e81-159">Get command:</span></span>     | [<span data-ttu-id="b5e81-160">**glGetIntegerv**</span><span class="sxs-lookup"><span data-stu-id="b5e81-160">**glGetIntegerv**</span></span>](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) |



 

<span data-ttu-id="b5e81-161"></dd> <dt><span id="GL_MAX_PIXEL_MAP_TABLE"></span><span id="gl_max_pixel_map_table"></span>\_table de \_ mappage de pixels Max \_ . GL \_</dt> </span><span class="sxs-lookup"><span data-stu-id="b5e81-161"></dd> <dt><span id="GL_MAX_PIXEL_MAP_TABLE"></span><span id="gl_max_pixel_map_table"></span>GL\_MAX\_PIXEL\_MAP\_TABLE</dt> </span></span><dd> 

|                  |                                                                                  |
|------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="b5e81-162">Description :</span><span class="sxs-lookup"><span data-stu-id="b5e81-162">Description:</span></span>     | <span data-ttu-id="b5e81-163">Taille maximale d’une table de traduction **glPixelMap**</span><span class="sxs-lookup"><span data-stu-id="b5e81-163">Maximum size of a **glPixelMap** translation table</span></span>                               |
| <span data-ttu-id="b5e81-164">Groupe d’attributs :</span><span class="sxs-lookup"><span data-stu-id="b5e81-164">Attribute group:</span></span> |                                                                                  |
| <span data-ttu-id="b5e81-165">Valeur initiale :</span><span class="sxs-lookup"><span data-stu-id="b5e81-165">Initial value:</span></span>   | <span data-ttu-id="b5e81-166">32</span><span class="sxs-lookup"><span data-stu-id="b5e81-166">32</span></span>                                                                               |
| <span data-ttu-id="b5e81-167">Commande d’extraction :</span><span class="sxs-lookup"><span data-stu-id="b5e81-167">Get command:</span></span>     | [<span data-ttu-id="b5e81-168">**glGetIntegerv**</span><span class="sxs-lookup"><span data-stu-id="b5e81-168">**glGetIntegerv**</span></span>](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) |



 

<span data-ttu-id="b5e81-169"></dd> <dt><span id="GL_MAX_NAME_STACK_DEPTH"></span><span id="gl_max_name_stack_depth"></span>profondeur de la \_ \_ pile de noms Max \_ . GL \_</dt> </span><span class="sxs-lookup"><span data-stu-id="b5e81-169"></dd> <dt><span id="GL_MAX_NAME_STACK_DEPTH"></span><span id="gl_max_name_stack_depth"></span>GL\_MAX\_NAME\_STACK\_DEPTH</dt> </span></span><dd> 

|                  |                                                                                  |
|------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="b5e81-170">Description :</span><span class="sxs-lookup"><span data-stu-id="b5e81-170">Description:</span></span>     | <span data-ttu-id="b5e81-171">Profondeur maximale de la pile des noms de sélection</span><span class="sxs-lookup"><span data-stu-id="b5e81-171">Maximum selection-name stack depth</span></span>                                               |
| <span data-ttu-id="b5e81-172">Groupe d’attributs :</span><span class="sxs-lookup"><span data-stu-id="b5e81-172">Attribute group:</span></span> |                                                                                  |
| <span data-ttu-id="b5e81-173">Valeur initiale :</span><span class="sxs-lookup"><span data-stu-id="b5e81-173">Initial value:</span></span>   | <span data-ttu-id="b5e81-174">64</span><span class="sxs-lookup"><span data-stu-id="b5e81-174">64</span></span>                                                                               |
| <span data-ttu-id="b5e81-175">Commande d’extraction :</span><span class="sxs-lookup"><span data-stu-id="b5e81-175">Get command:</span></span>     | [<span data-ttu-id="b5e81-176">**glGetIntegerv**</span><span class="sxs-lookup"><span data-stu-id="b5e81-176">**glGetIntegerv**</span></span>](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) |



 

<span data-ttu-id="b5e81-177"></dd> <dt><span id="GL_MAX_LIST_NESTING"></span><span id="gl_max_list_nesting"></span>\_imbrication du nombre maximal de \_ listes GL \_</dt> </span><span class="sxs-lookup"><span data-stu-id="b5e81-177"></dd> <dt><span id="GL_MAX_LIST_NESTING"></span><span id="gl_max_list_nesting"></span>GL\_MAX\_LIST\_NESTING</dt> </span></span><dd> 

|                  |                                                                                  |
|------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="b5e81-178">Description :</span><span class="sxs-lookup"><span data-stu-id="b5e81-178">Description:</span></span>     | <span data-ttu-id="b5e81-179">Imbrication maximale des appels de liste d’affichage</span><span class="sxs-lookup"><span data-stu-id="b5e81-179">Maximum display-list call nesting</span></span>                                                |
| <span data-ttu-id="b5e81-180">Groupe d’attributs :</span><span class="sxs-lookup"><span data-stu-id="b5e81-180">Attribute group:</span></span> |                                                                                  |
| <span data-ttu-id="b5e81-181">Valeur initiale :</span><span class="sxs-lookup"><span data-stu-id="b5e81-181">Initial value:</span></span>   | <span data-ttu-id="b5e81-182">64</span><span class="sxs-lookup"><span data-stu-id="b5e81-182">64</span></span>                                                                               |
| <span data-ttu-id="b5e81-183">Commande d’extraction :</span><span class="sxs-lookup"><span data-stu-id="b5e81-183">Get command:</span></span>     | [<span data-ttu-id="b5e81-184">**glGetIntegerv**</span><span class="sxs-lookup"><span data-stu-id="b5e81-184">**glGetIntegerv**</span></span>](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) |



 

<span data-ttu-id="b5e81-185"></dd> <dt><span id="GL_MAX_EVAL_ORDER"></span><span id="gl_max_eval_order"></span>\_ordre d' \_ évaluation \_ Max GL</dt> </span><span class="sxs-lookup"><span data-stu-id="b5e81-185"></dd> <dt><span id="GL_MAX_EVAL_ORDER"></span><span id="gl_max_eval_order"></span>GL\_MAX\_EVAL\_ORDER</dt> </span></span><dd> 

|                  |                                                                                  |
|------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="b5e81-186">Description :</span><span class="sxs-lookup"><span data-stu-id="b5e81-186">Description:</span></span>     | <span data-ttu-id="b5e81-187">Ordre polynomial maximal de l’évaluateur</span><span class="sxs-lookup"><span data-stu-id="b5e81-187">Maximum evaluator polynomial order</span></span>                                               |
| <span data-ttu-id="b5e81-188">Groupe d’attributs :</span><span class="sxs-lookup"><span data-stu-id="b5e81-188">Attribute group:</span></span> |                                                                                  |
| <span data-ttu-id="b5e81-189">Valeur initiale :</span><span class="sxs-lookup"><span data-stu-id="b5e81-189">Initial value:</span></span>   | <span data-ttu-id="b5e81-190">8</span><span class="sxs-lookup"><span data-stu-id="b5e81-190">8</span></span>                                                                                |
| <span data-ttu-id="b5e81-191">Commande d’extraction :</span><span class="sxs-lookup"><span data-stu-id="b5e81-191">Get command:</span></span>     | [<span data-ttu-id="b5e81-192">**glGetIntegerv**</span><span class="sxs-lookup"><span data-stu-id="b5e81-192">**glGetIntegerv**</span></span>](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) |



 

<span data-ttu-id="b5e81-193"></dd> <dt><span id="GL_MAX_VIEWPORT_DIMS"></span><span id="gl_max_viewport_dims"></span>\_fenêtre d’affichage Max GL- \_ \_ estompe</dt> </span><span class="sxs-lookup"><span data-stu-id="b5e81-193"></dd> <dt><span id="GL_MAX_VIEWPORT_DIMS"></span><span id="gl_max_viewport_dims"></span>GL\_MAX\_VIEWPORT\_DIMS</dt> </span></span><dd> 

|                  |                                                                                  |
|------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="b5e81-194">Description :</span><span class="sxs-lookup"><span data-stu-id="b5e81-194">Description:</span></span>     | <span data-ttu-id="b5e81-195">Dimensions maximales de la fenêtre d’affichage</span><span class="sxs-lookup"><span data-stu-id="b5e81-195">Maximum viewport dimensions</span></span>                                                      |
| <span data-ttu-id="b5e81-196">Groupe d’attributs :</span><span class="sxs-lookup"><span data-stu-id="b5e81-196">Attribute group:</span></span> |                                                                                  |
| <span data-ttu-id="b5e81-197">Valeur initiale :</span><span class="sxs-lookup"><span data-stu-id="b5e81-197">Initial value:</span></span>   |                                                                                  |
| <span data-ttu-id="b5e81-198">Commande d’extraction :</span><span class="sxs-lookup"><span data-stu-id="b5e81-198">Get command:</span></span>     | [<span data-ttu-id="b5e81-199">**glGetIntegerv**</span><span class="sxs-lookup"><span data-stu-id="b5e81-199">**glGetIntegerv**</span></span>](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) |



 

<span data-ttu-id="b5e81-200"></dd> <dt><span id="GL_MAX_ATTRIB_STACK_DEPTH"></span><span id="gl_max_attrib_stack_depth"></span>profondeur de la \_ \_ pile d’attrib Max \_ . GL \_</dt> </span><span class="sxs-lookup"><span data-stu-id="b5e81-200"></dd> <dt><span id="GL_MAX_ATTRIB_STACK_DEPTH"></span><span id="gl_max_attrib_stack_depth"></span>GL\_MAX\_ATTRIB\_STACK\_DEPTH</dt> </span></span><dd> 

|                  |                                                                                  |
|------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="b5e81-201">Description :</span><span class="sxs-lookup"><span data-stu-id="b5e81-201">Description:</span></span>     | <span data-ttu-id="b5e81-202">Profondeur maximale de la pile d’attributs</span><span class="sxs-lookup"><span data-stu-id="b5e81-202">Maximum depth of the attribute stack</span></span>                                             |
| <span data-ttu-id="b5e81-203">Groupe d’attributs :</span><span class="sxs-lookup"><span data-stu-id="b5e81-203">Attribute group:</span></span> |                                                                                  |
| <span data-ttu-id="b5e81-204">Valeur initiale :</span><span class="sxs-lookup"><span data-stu-id="b5e81-204">Initial value:</span></span>   | <span data-ttu-id="b5e81-205">16</span><span class="sxs-lookup"><span data-stu-id="b5e81-205">16</span></span>                                                                               |
| <span data-ttu-id="b5e81-206">Commande d’extraction :</span><span class="sxs-lookup"><span data-stu-id="b5e81-206">Get command:</span></span>     | [<span data-ttu-id="b5e81-207">**glGetIntegerv**</span><span class="sxs-lookup"><span data-stu-id="b5e81-207">**glGetIntegerv**</span></span>](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) |



 

<span data-ttu-id="b5e81-208"></dd> <dt><span id="GL_AUX_BUFFERS"></span><span id="gl_aux_buffers"></span>\_ \_ mémoires TAMPONs GL</dt> </span><span class="sxs-lookup"><span data-stu-id="b5e81-208"></dd> <dt><span id="GL_AUX_BUFFERS"></span><span id="gl_aux_buffers"></span>GL\_AUX\_BUFFERS</dt> </span></span><dd> 

|                  |                                                                                  |
|------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="b5e81-209">Description :</span><span class="sxs-lookup"><span data-stu-id="b5e81-209">Description:</span></span>     | <span data-ttu-id="b5e81-210">Nombre de mémoires tampons auxiliaires</span><span class="sxs-lookup"><span data-stu-id="b5e81-210">Number of auxiliary buffers</span></span>                                                      |
| <span data-ttu-id="b5e81-211">Groupe d’attributs :</span><span class="sxs-lookup"><span data-stu-id="b5e81-211">Attribute group:</span></span> |                                                                                  |
| <span data-ttu-id="b5e81-212">Valeur initiale :</span><span class="sxs-lookup"><span data-stu-id="b5e81-212">Initial value:</span></span>   | <span data-ttu-id="b5e81-213">0</span><span class="sxs-lookup"><span data-stu-id="b5e81-213">0</span></span>                                                                                |
| <span data-ttu-id="b5e81-214">Commande d’extraction :</span><span class="sxs-lookup"><span data-stu-id="b5e81-214">Get command:</span></span>     | [<span data-ttu-id="b5e81-215">**glGetBooleanv**</span><span class="sxs-lookup"><span data-stu-id="b5e81-215">**glGetBooleanv**</span></span>](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) |



 

<span data-ttu-id="b5e81-216"></dd> <dt><span id="GL_RGBA_MODE"></span><span id="gl_rgba_mode"></span>\_mode GL RVBA \_</dt> </span><span class="sxs-lookup"><span data-stu-id="b5e81-216"></dd> <dt><span id="GL_RGBA_MODE"></span><span id="gl_rgba_mode"></span>GL\_RGBA\_MODE</dt> </span></span><dd> 

|                  |                                                                                  |
|------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="b5e81-217">Description :</span><span class="sxs-lookup"><span data-stu-id="b5e81-217">Description:</span></span>     | <span data-ttu-id="b5e81-218">True si les mémoires tampons de couleur stockent RVBA</span><span class="sxs-lookup"><span data-stu-id="b5e81-218">True if color buffers store RGBA</span></span>                                                 |
| <span data-ttu-id="b5e81-219">Groupe d’attributs :</span><span class="sxs-lookup"><span data-stu-id="b5e81-219">Attribute group:</span></span> |                                                                                  |
| <span data-ttu-id="b5e81-220">Valeur initiale :</span><span class="sxs-lookup"><span data-stu-id="b5e81-220">Initial value:</span></span>   |                                                                                  |
| <span data-ttu-id="b5e81-221">Commande d’extraction :</span><span class="sxs-lookup"><span data-stu-id="b5e81-221">Get command:</span></span>     | [<span data-ttu-id="b5e81-222">**glGetBooleanv**</span><span class="sxs-lookup"><span data-stu-id="b5e81-222">**glGetBooleanv**</span></span>](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) |



 

<span data-ttu-id="b5e81-223"></dd> <dt><span id="GL_INDEX_MODE"></span><span id="gl_index_mode"></span>\_mode d’index GL \_</dt> </span><span class="sxs-lookup"><span data-stu-id="b5e81-223"></dd> <dt><span id="GL_INDEX_MODE"></span><span id="gl_index_mode"></span>GL\_INDEX\_MODE</dt> </span></span><dd> 

|                  |                                                                                  |
|------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="b5e81-224">Description :</span><span class="sxs-lookup"><span data-stu-id="b5e81-224">Description:</span></span>     | <span data-ttu-id="b5e81-225">True si les mémoires tampons de couleur stockent les index</span><span class="sxs-lookup"><span data-stu-id="b5e81-225">True if color buffers store indexes</span></span>                                              |
| <span data-ttu-id="b5e81-226">Groupe d’attributs :</span><span class="sxs-lookup"><span data-stu-id="b5e81-226">Attribute group:</span></span> |                                                                                  |
| <span data-ttu-id="b5e81-227">Valeur initiale :</span><span class="sxs-lookup"><span data-stu-id="b5e81-227">Initial value:</span></span>   |                                                                                  |
| <span data-ttu-id="b5e81-228">Commande d’extraction :</span><span class="sxs-lookup"><span data-stu-id="b5e81-228">Get command:</span></span>     | [<span data-ttu-id="b5e81-229">**glGetBooleanv**</span><span class="sxs-lookup"><span data-stu-id="b5e81-229">**glGetBooleanv**</span></span>](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) |



 

<span data-ttu-id="b5e81-230"></dd> <dt><span id="GL_DOUBLEBUFFER"></span><span id="gl_doublebuffer"></span>\_DOUBLEBUFFER GL</dt> </span><span class="sxs-lookup"><span data-stu-id="b5e81-230"></dd> <dt><span id="GL_DOUBLEBUFFER"></span><span id="gl_doublebuffer"></span>GL\_DOUBLEBUFFER</dt> </span></span><dd> 

|                  |                                                                                  |
|------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="b5e81-231">Description :</span><span class="sxs-lookup"><span data-stu-id="b5e81-231">Description:</span></span>     | <span data-ttu-id="b5e81-232">True si des mémoires tampons d’arrière-plan et d’arrière-plan existent</span><span class="sxs-lookup"><span data-stu-id="b5e81-232">True if front and back buffers exist</span></span>                                             |
| <span data-ttu-id="b5e81-233">Groupe d’attributs :</span><span class="sxs-lookup"><span data-stu-id="b5e81-233">Attribute group:</span></span> |                                                                                  |
| <span data-ttu-id="b5e81-234">Valeur initiale :</span><span class="sxs-lookup"><span data-stu-id="b5e81-234">Initial value:</span></span>   |                                                                                  |
| <span data-ttu-id="b5e81-235">Commande d’extraction :</span><span class="sxs-lookup"><span data-stu-id="b5e81-235">Get command:</span></span>     | [<span data-ttu-id="b5e81-236">**glGetBooleanv**</span><span class="sxs-lookup"><span data-stu-id="b5e81-236">**glGetBooleanv**</span></span>](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) |



 

<span data-ttu-id="b5e81-237"></dd> <dt><span id="GL_STEREO"></span><span id="gl_stereo"></span>\_stéréo GL</dt> </span><span class="sxs-lookup"><span data-stu-id="b5e81-237"></dd> <dt><span id="GL_STEREO"></span><span id="gl_stereo"></span>GL\_STEREO</dt> </span></span><dd> 

|                  |                                                                                |
|------------------|--------------------------------------------------------------------------------|
| <span data-ttu-id="b5e81-238">Description :</span><span class="sxs-lookup"><span data-stu-id="b5e81-238">Description:</span></span>     | <span data-ttu-id="b5e81-239">True si les mémoires tampons de gauche et de droite existent</span><span class="sxs-lookup"><span data-stu-id="b5e81-239">True if left and right buffers exist</span></span>                                           |
| <span data-ttu-id="b5e81-240">Groupe d’attributs :</span><span class="sxs-lookup"><span data-stu-id="b5e81-240">Attribute group:</span></span> |                                                                                |
| <span data-ttu-id="b5e81-241">Valeur initiale :</span><span class="sxs-lookup"><span data-stu-id="b5e81-241">Initial value:</span></span>   |                                                                                |
| <span data-ttu-id="b5e81-242">Commande d’extraction :</span><span class="sxs-lookup"><span data-stu-id="b5e81-242">Get command:</span></span>     | [<span data-ttu-id="b5e81-243">**glGetFloatv**</span><span class="sxs-lookup"><span data-stu-id="b5e81-243">**glGetFloatv**</span></span>](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) |



 

<span data-ttu-id="b5e81-244"></dd> <dt><span id="GL_POINT_SIZE_RANGE"></span><span id="gl_point_size_range"></span>\_plage de \_ tailles de points GL \_</dt> </span><span class="sxs-lookup"><span data-stu-id="b5e81-244"></dd> <dt><span id="GL_POINT_SIZE_RANGE"></span><span id="gl_point_size_range"></span>GL\_POINT\_SIZE\_RANGE</dt> </span></span><dd> 

|                  |                                                                                |
|------------------|--------------------------------------------------------------------------------|
| <span data-ttu-id="b5e81-245">Description :</span><span class="sxs-lookup"><span data-stu-id="b5e81-245">Description:</span></span>     | <span data-ttu-id="b5e81-246">Plage (faible à élevée) de tailles de points avec anticrénelage</span><span class="sxs-lookup"><span data-stu-id="b5e81-246">Range (low to high) of antialiased point sizes</span></span>                                 |
| <span data-ttu-id="b5e81-247">Groupe d’attributs :</span><span class="sxs-lookup"><span data-stu-id="b5e81-247">Attribute group:</span></span> |                                                                                |
| <span data-ttu-id="b5e81-248">Valeur initiale :</span><span class="sxs-lookup"><span data-stu-id="b5e81-248">Initial value:</span></span>   | <span data-ttu-id="b5e81-249">1, 1</span><span class="sxs-lookup"><span data-stu-id="b5e81-249">1, 1</span></span>                                                                           |
| <span data-ttu-id="b5e81-250">Commande d’extraction :</span><span class="sxs-lookup"><span data-stu-id="b5e81-250">Get command:</span></span>     | [<span data-ttu-id="b5e81-251">**glGetFloatv**</span><span class="sxs-lookup"><span data-stu-id="b5e81-251">**glGetFloatv**</span></span>](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) |



 

<span data-ttu-id="b5e81-252"></dd> <dt><span id="GL_POINT_SIZE_GRANULARITY"></span><span id="gl_point_size_granularity"></span>\_granularité de la taille du point GL \_ \_</dt> </span><span class="sxs-lookup"><span data-stu-id="b5e81-252"></dd> <dt><span id="GL_POINT_SIZE_GRANULARITY"></span><span id="gl_point_size_granularity"></span>GL\_POINT\_SIZE\_GRANULARITY</dt> </span></span><dd> 

|                  |                                                                                |
|------------------|--------------------------------------------------------------------------------|
| <span data-ttu-id="b5e81-253">Description :</span><span class="sxs-lookup"><span data-stu-id="b5e81-253">Description:</span></span>     | <span data-ttu-id="b5e81-254">Granularité de la taille du point anticrénelage</span><span class="sxs-lookup"><span data-stu-id="b5e81-254">Antialiased point size granularity</span></span>                                             |
| <span data-ttu-id="b5e81-255">Groupe d’attributs :</span><span class="sxs-lookup"><span data-stu-id="b5e81-255">Attribute group:</span></span> |                                                                                |
| <span data-ttu-id="b5e81-256">Valeur initiale :</span><span class="sxs-lookup"><span data-stu-id="b5e81-256">Initial value:</span></span>   |                                                                                |
| <span data-ttu-id="b5e81-257">Commande d’extraction :</span><span class="sxs-lookup"><span data-stu-id="b5e81-257">Get command:</span></span>     | [<span data-ttu-id="b5e81-258">**glGetFloatv**</span><span class="sxs-lookup"><span data-stu-id="b5e81-258">**glGetFloatv**</span></span>](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) |



 

<span data-ttu-id="b5e81-259"></dd> <dt><span id="GL_LINE_WIDTH_RANGE"></span><span id="gl_line_width_range"></span>\_plage de \_ largeur de ligne GL \_</dt> </span><span class="sxs-lookup"><span data-stu-id="b5e81-259"></dd> <dt><span id="GL_LINE_WIDTH_RANGE"></span><span id="gl_line_width_range"></span>GL\_LINE\_WIDTH\_RANGE</dt> </span></span><dd> 

|                  |                                                                                |
|------------------|--------------------------------------------------------------------------------|
| <span data-ttu-id="b5e81-260">Description :</span><span class="sxs-lookup"><span data-stu-id="b5e81-260">Description:</span></span>     | <span data-ttu-id="b5e81-261">Plage (faible à élevée) des largeurs de ligne avec anticrénelage</span><span class="sxs-lookup"><span data-stu-id="b5e81-261">Range (low to high) of antialiased line widths</span></span>                                 |
| <span data-ttu-id="b5e81-262">Groupe d’attributs :</span><span class="sxs-lookup"><span data-stu-id="b5e81-262">Attribute group:</span></span> |                                                                                |
| <span data-ttu-id="b5e81-263">Valeur initiale :</span><span class="sxs-lookup"><span data-stu-id="b5e81-263">Initial value:</span></span>   | <span data-ttu-id="b5e81-264">1, 1</span><span class="sxs-lookup"><span data-stu-id="b5e81-264">1, 1</span></span>                                                                           |
| <span data-ttu-id="b5e81-265">Commande d’extraction :</span><span class="sxs-lookup"><span data-stu-id="b5e81-265">Get command:</span></span>     | [<span data-ttu-id="b5e81-266">**glGetFloatv**</span><span class="sxs-lookup"><span data-stu-id="b5e81-266">**glGetFloatv**</span></span>](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) |



 

<span data-ttu-id="b5e81-267"></dd> <dt><span id="GL_LINE_WIDTH_GRANULARITY"></span><span id="gl_line_width_granularity"></span>\_granularité de la largeur de ligne GL \_ \_</dt> </span><span class="sxs-lookup"><span data-stu-id="b5e81-267"></dd> <dt><span id="GL_LINE_WIDTH_GRANULARITY"></span><span id="gl_line_width_granularity"></span>GL\_LINE\_WIDTH\_GRANULARITY</dt> </span></span><dd> 

|                  |                                                                                |
|------------------|--------------------------------------------------------------------------------|
| <span data-ttu-id="b5e81-268">Description :</span><span class="sxs-lookup"><span data-stu-id="b5e81-268">Description:</span></span>     | <span data-ttu-id="b5e81-269">Granularité de la largeur de ligne avec anticrénelage</span><span class="sxs-lookup"><span data-stu-id="b5e81-269">Antialiased line-width granularity</span></span>                                             |
| <span data-ttu-id="b5e81-270">Groupe d’attributs :</span><span class="sxs-lookup"><span data-stu-id="b5e81-270">Attribute group:</span></span> |                                                                                |
| <span data-ttu-id="b5e81-271">Valeur initiale :</span><span class="sxs-lookup"><span data-stu-id="b5e81-271">Initial value:</span></span>   |                                                                                |
| <span data-ttu-id="b5e81-272">Commande d’extraction :</span><span class="sxs-lookup"><span data-stu-id="b5e81-272">Get command:</span></span>     | [<span data-ttu-id="b5e81-273">**glGetFloatv**</span><span class="sxs-lookup"><span data-stu-id="b5e81-273">**glGetFloatv**</span></span>](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) |



 

</dd> </dl>

 

 




