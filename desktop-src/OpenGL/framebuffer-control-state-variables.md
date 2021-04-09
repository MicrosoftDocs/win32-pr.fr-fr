---
title: Variables d’état de contrôle trame
description: Variables d’état de contrôle trame
ms.assetid: ab57e07d-a694-45e7-a3b3-2e856111b87d
keywords:
- Variables d’état de contrôle trame OpenGL
topic_type:
- apiref
api_name:
- Framebuffer Control State Variables
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d44327858ae43212fcaa4364ed23045de5e0296f
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/25/2019
ms.locfileid: "103840957"
---
# <a name="framebuffer-control-state-variables"></a><span data-ttu-id="e83a1-104">Variables d’état de contrôle trame</span><span class="sxs-lookup"><span data-stu-id="e83a1-104">Framebuffer Control State Variables</span></span>

<dl> <span data-ttu-id="e83a1-105"><dt><span id="GL_DRAW_BUFFER"></span><span id="gl_draw_buffer"></span>\_mémoire tampon de dessin GL \_</dt> </span><span class="sxs-lookup"><span data-stu-id="e83a1-105"><dt><span id="GL_DRAW_BUFFER"></span><span id="gl_draw_buffer"></span>GL\_DRAW\_BUFFER</dt> </span></span><dd> 

|                  |                                        |
|------------------|----------------------------------------|
| <span data-ttu-id="e83a1-106">Description :</span><span class="sxs-lookup"><span data-stu-id="e83a1-106">Description:</span></span>     | <span data-ttu-id="e83a1-107">Mémoires tampons sélectionnées pour le dessin</span><span class="sxs-lookup"><span data-stu-id="e83a1-107">Buffers selected for drawing</span></span>           |
| <span data-ttu-id="e83a1-108">Groupe d’attributs :</span><span class="sxs-lookup"><span data-stu-id="e83a1-108">Attribute group:</span></span> | <span data-ttu-id="e83a1-109">mémoire tampon de couleur</span><span class="sxs-lookup"><span data-stu-id="e83a1-109">color-buffer</span></span>                           |
| <span data-ttu-id="e83a1-110">Valeur initiale :</span><span class="sxs-lookup"><span data-stu-id="e83a1-110">Initial value:</span></span>   |                                        |
| <span data-ttu-id="e83a1-111">Commande d’extraction :</span><span class="sxs-lookup"><span data-stu-id="e83a1-111">Get command:</span></span>     | [<span data-ttu-id="e83a1-112">**glGetIntegerv**</span><span class="sxs-lookup"><span data-stu-id="e83a1-112">**glGetIntegerv**</span></span>](glgetintegerv.md) |



 

<span data-ttu-id="e83a1-113"></dd> <dt><span id="GL_INDEX_WRITEMASK"></span><span id="gl_index_writemask"></span>\_WRITEMASK d’index GL \_</dt> </span><span class="sxs-lookup"><span data-stu-id="e83a1-113"></dd> <dt><span id="GL_INDEX_WRITEMASK"></span><span id="gl_index_writemask"></span>GL\_INDEX\_WRITEMASK</dt> </span></span><dd> 

|                  |                                                                                  |
|------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="e83a1-114">Description :</span><span class="sxs-lookup"><span data-stu-id="e83a1-114">Description:</span></span>     | <span data-ttu-id="e83a1-115">Writemask d’index de couleurs</span><span class="sxs-lookup"><span data-stu-id="e83a1-115">Color-index writemask</span></span>                                                            |
| <span data-ttu-id="e83a1-116">Groupe d’attributs :</span><span class="sxs-lookup"><span data-stu-id="e83a1-116">Attribute group:</span></span> | <span data-ttu-id="e83a1-117">mémoire tampon de couleur</span><span class="sxs-lookup"><span data-stu-id="e83a1-117">color-buffer</span></span>                                                                     |
| <span data-ttu-id="e83a1-118">Valeur initiale :</span><span class="sxs-lookup"><span data-stu-id="e83a1-118">Initial value:</span></span>   | <span data-ttu-id="e83a1-119">du 1</span><span class="sxs-lookup"><span data-stu-id="e83a1-119">1's</span></span>                                                                              |
| <span data-ttu-id="e83a1-120">Commande d’extraction :</span><span class="sxs-lookup"><span data-stu-id="e83a1-120">Get command:</span></span>     | [<span data-ttu-id="e83a1-121">**glGetIntegerv**</span><span class="sxs-lookup"><span data-stu-id="e83a1-121">**glGetIntegerv**</span></span>](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) |



 

<span data-ttu-id="e83a1-122"></dd> <dt><span id="GL_COLOR_WRITEMASK"></span><span id="gl_color_writemask"></span>\_WRITEMASK de couleur GL \_</dt> </span><span class="sxs-lookup"><span data-stu-id="e83a1-122"></dd> <dt><span id="GL_COLOR_WRITEMASK"></span><span id="gl_color_writemask"></span>GL\_COLOR\_WRITEMASK</dt> </span></span><dd> 

|                  |                                                                                  |
|------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="e83a1-123">Description :</span><span class="sxs-lookup"><span data-stu-id="e83a1-123">Description:</span></span>     | <span data-ttu-id="e83a1-124">L’écriture des couleurs active ; R, G, B ou A</span><span class="sxs-lookup"><span data-stu-id="e83a1-124">Color write enables; R, G, B, or A</span></span>                                               |
| <span data-ttu-id="e83a1-125">Groupe d’attributs :</span><span class="sxs-lookup"><span data-stu-id="e83a1-125">Attribute group:</span></span> | <span data-ttu-id="e83a1-126">mémoire tampon de couleur</span><span class="sxs-lookup"><span data-stu-id="e83a1-126">color-buffer</span></span>                                                                     |
| <span data-ttu-id="e83a1-127">Valeur initiale :</span><span class="sxs-lookup"><span data-stu-id="e83a1-127">Initial value:</span></span>   | <span data-ttu-id="e83a1-128">GL \_ true</span><span class="sxs-lookup"><span data-stu-id="e83a1-128">GL\_TRUE</span></span>                                                                         |
| <span data-ttu-id="e83a1-129">Commande d’extraction :</span><span class="sxs-lookup"><span data-stu-id="e83a1-129">Get command:</span></span>     | [<span data-ttu-id="e83a1-130">**glGetBooleanv**</span><span class="sxs-lookup"><span data-stu-id="e83a1-130">**glGetBooleanv**</span></span>](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) |



 

<span data-ttu-id="e83a1-131"></dd> <dt><span id="GL_DEPTH_WRITEMASK"></span><span id="gl_depth_writemask"></span>\_profondeur GL \_ WRITEMASK</dt> </span><span class="sxs-lookup"><span data-stu-id="e83a1-131"></dd> <dt><span id="GL_DEPTH_WRITEMASK"></span><span id="gl_depth_writemask"></span>GL\_DEPTH\_WRITEMASK</dt> </span></span><dd> 

|                  |                                                                                  |
|------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="e83a1-132">Description :</span><span class="sxs-lookup"><span data-stu-id="e83a1-132">Description:</span></span>     | <span data-ttu-id="e83a1-133">Mémoire tampon de profondeur activée pour l’écriture</span><span class="sxs-lookup"><span data-stu-id="e83a1-133">Depth buffer enabled for writing</span></span>                                                 |
| <span data-ttu-id="e83a1-134">Groupe d’attributs :</span><span class="sxs-lookup"><span data-stu-id="e83a1-134">Attribute group:</span></span> | <span data-ttu-id="e83a1-135">mémoire tampon de profondeur</span><span class="sxs-lookup"><span data-stu-id="e83a1-135">depth-buffer</span></span>                                                                     |
| <span data-ttu-id="e83a1-136">Valeur initiale :</span><span class="sxs-lookup"><span data-stu-id="e83a1-136">Initial value:</span></span>   | <span data-ttu-id="e83a1-137">GL \_ true</span><span class="sxs-lookup"><span data-stu-id="e83a1-137">GL\_TRUE</span></span>                                                                         |
| <span data-ttu-id="e83a1-138">Commande d’extraction :</span><span class="sxs-lookup"><span data-stu-id="e83a1-138">Get command:</span></span>     | [<span data-ttu-id="e83a1-139">**glGetBooleanv**</span><span class="sxs-lookup"><span data-stu-id="e83a1-139">**glGetBooleanv**</span></span>](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) |



 

<span data-ttu-id="e83a1-140"></dd> <dt><span id="GL_STENCIL_WRITEMASK"></span><span id="gl_stencil_writemask"></span>\_WRITEMASK du stencil du GL \_</dt> </span><span class="sxs-lookup"><span data-stu-id="e83a1-140"></dd> <dt><span id="GL_STENCIL_WRITEMASK"></span><span id="gl_stencil_writemask"></span>GL\_STENCIL\_WRITEMASK</dt> </span></span><dd> 

|                  |                                                                                  |
|------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="e83a1-141">Description :</span><span class="sxs-lookup"><span data-stu-id="e83a1-141">Description:</span></span>     | <span data-ttu-id="e83a1-142">Stencil-tampon writemask</span><span class="sxs-lookup"><span data-stu-id="e83a1-142">Stencil-buffer writemask</span></span>                                                         |
| <span data-ttu-id="e83a1-143">Groupe d’attributs :</span><span class="sxs-lookup"><span data-stu-id="e83a1-143">Attribute group:</span></span> | <span data-ttu-id="e83a1-144">stencil-tampon</span><span class="sxs-lookup"><span data-stu-id="e83a1-144">stencil-buffer</span></span>                                                                   |
| <span data-ttu-id="e83a1-145">Valeur initiale :</span><span class="sxs-lookup"><span data-stu-id="e83a1-145">Initial value:</span></span>   | <span data-ttu-id="e83a1-146">du 1</span><span class="sxs-lookup"><span data-stu-id="e83a1-146">1's</span></span>                                                                              |
| <span data-ttu-id="e83a1-147">Commande d’extraction :</span><span class="sxs-lookup"><span data-stu-id="e83a1-147">Get command:</span></span>     | [<span data-ttu-id="e83a1-148">**glGetIntegerv**</span><span class="sxs-lookup"><span data-stu-id="e83a1-148">**glGetIntegerv**</span></span>](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) |



 

<span data-ttu-id="e83a1-149"></dd> <dt><span id="GL_COLOR_CLEAR_VALUE"></span><span id="gl_color_clear_value"></span>\_ \_ valeur Clear de couleur GL \_</dt> </span><span class="sxs-lookup"><span data-stu-id="e83a1-149"></dd> <dt><span id="GL_COLOR_CLEAR_VALUE"></span><span id="gl_color_clear_value"></span>GL\_COLOR\_CLEAR\_VALUE</dt> </span></span><dd> 

|                  |                                                                                |
|------------------|--------------------------------------------------------------------------------|
| <span data-ttu-id="e83a1-150">Description :</span><span class="sxs-lookup"><span data-stu-id="e83a1-150">Description:</span></span>     | <span data-ttu-id="e83a1-151">Valeur effacée de la mémoire tampon de couleur (mode RVBA)</span><span class="sxs-lookup"><span data-stu-id="e83a1-151">Color-buffer clear value (RGBA mode)</span></span>                                           |
| <span data-ttu-id="e83a1-152">Groupe d’attributs :</span><span class="sxs-lookup"><span data-stu-id="e83a1-152">Attribute group:</span></span> | <span data-ttu-id="e83a1-153">mémoire tampon de couleur</span><span class="sxs-lookup"><span data-stu-id="e83a1-153">color-buffer</span></span>                                                                   |
| <span data-ttu-id="e83a1-154">Valeur initiale :</span><span class="sxs-lookup"><span data-stu-id="e83a1-154">Initial value:</span></span>   | <span data-ttu-id="e83a1-155">0, 0, 0, 0</span><span class="sxs-lookup"><span data-stu-id="e83a1-155">0, 0, 0, 0</span></span>                                                                     |
| <span data-ttu-id="e83a1-156">Commande d’extraction :</span><span class="sxs-lookup"><span data-stu-id="e83a1-156">Get command:</span></span>     | [<span data-ttu-id="e83a1-157">**glGetFloatv**</span><span class="sxs-lookup"><span data-stu-id="e83a1-157">**glGetFloatv**</span></span>](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) |



 

<span data-ttu-id="e83a1-158"></dd> <dt><span id="GL_INDEX_CLEAR_VALUE"></span><span id="gl_index_clear_value"></span>\_ \_ valeur effacer de l’index GL \_</dt> </span><span class="sxs-lookup"><span data-stu-id="e83a1-158"></dd> <dt><span id="GL_INDEX_CLEAR_VALUE"></span><span id="gl_index_clear_value"></span>GL\_INDEX\_CLEAR\_VALUE</dt> </span></span><dd> 

|                  |                                                                                |
|------------------|--------------------------------------------------------------------------------|
| <span data-ttu-id="e83a1-159">Description :</span><span class="sxs-lookup"><span data-stu-id="e83a1-159">Description:</span></span>     | <span data-ttu-id="e83a1-160">Valeur effacée de la mémoire tampon de couleur (mode index des couleurs)</span><span class="sxs-lookup"><span data-stu-id="e83a1-160">Color-buffer clear value (color-index mode)</span></span>                                    |
| <span data-ttu-id="e83a1-161">Groupe d’attributs :</span><span class="sxs-lookup"><span data-stu-id="e83a1-161">Attribute group:</span></span> | <span data-ttu-id="e83a1-162">mémoire tampon de couleur</span><span class="sxs-lookup"><span data-stu-id="e83a1-162">color-buffer</span></span>                                                                   |
| <span data-ttu-id="e83a1-163">Valeur initiale :</span><span class="sxs-lookup"><span data-stu-id="e83a1-163">Initial value:</span></span>   | <span data-ttu-id="e83a1-164">0</span><span class="sxs-lookup"><span data-stu-id="e83a1-164">0</span></span>                                                                              |
| <span data-ttu-id="e83a1-165">Commande d’extraction :</span><span class="sxs-lookup"><span data-stu-id="e83a1-165">Get command:</span></span>     | [<span data-ttu-id="e83a1-166">**glGetFloatv**</span><span class="sxs-lookup"><span data-stu-id="e83a1-166">**glGetFloatv**</span></span>](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) |



 

<span data-ttu-id="e83a1-167"></dd> <dt><span id="GL_DEPTH_CLEAR_VALUE"></span><span id="gl_depth_clear_value"></span>\_ \_ valeur effacer de profondeur du GL \_</dt> </span><span class="sxs-lookup"><span data-stu-id="e83a1-167"></dd> <dt><span id="GL_DEPTH_CLEAR_VALUE"></span><span id="gl_depth_clear_value"></span>GL\_DEPTH\_CLEAR\_VALUE</dt> </span></span><dd> 

|                  |                                                                                  |
|------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="e83a1-168">Description :</span><span class="sxs-lookup"><span data-stu-id="e83a1-168">Description:</span></span>     | <span data-ttu-id="e83a1-169">Valeur effacée de la mémoire tampon de profondeur</span><span class="sxs-lookup"><span data-stu-id="e83a1-169">Depth-buffer clear value</span></span>                                                         |
| <span data-ttu-id="e83a1-170">Groupe d’attributs :</span><span class="sxs-lookup"><span data-stu-id="e83a1-170">Attribute group:</span></span> | <span data-ttu-id="e83a1-171">mémoire tampon de profondeur</span><span class="sxs-lookup"><span data-stu-id="e83a1-171">depth-buffer</span></span>                                                                     |
| <span data-ttu-id="e83a1-172">Valeur initiale :</span><span class="sxs-lookup"><span data-stu-id="e83a1-172">Initial value:</span></span>   | <span data-ttu-id="e83a1-173">1</span><span class="sxs-lookup"><span data-stu-id="e83a1-173">1</span></span>                                                                                |
| <span data-ttu-id="e83a1-174">Commande d’extraction :</span><span class="sxs-lookup"><span data-stu-id="e83a1-174">Get command:</span></span>     | [<span data-ttu-id="e83a1-175">**glGetIntegerv**</span><span class="sxs-lookup"><span data-stu-id="e83a1-175">**glGetIntegerv**</span></span>](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) |



 

<span data-ttu-id="e83a1-176"></dd> <dt><span id="GL_STENCIL_CLEAR_VALUE"></span><span id="gl_stencil_clear_value"></span>\_ \_ valeur effacer du stencil du GL \_</dt> </span><span class="sxs-lookup"><span data-stu-id="e83a1-176"></dd> <dt><span id="GL_STENCIL_CLEAR_VALUE"></span><span id="gl_stencil_clear_value"></span>GL\_STENCIL\_CLEAR\_VALUE</dt> </span></span><dd> 

|                  |                                                                                  |
|------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="e83a1-177">Description :</span><span class="sxs-lookup"><span data-stu-id="e83a1-177">Description:</span></span>     | <span data-ttu-id="e83a1-178">Valeur effacer du tampon stencil</span><span class="sxs-lookup"><span data-stu-id="e83a1-178">Stencil-buffer clear value</span></span>                                                       |
| <span data-ttu-id="e83a1-179">Groupe d’attributs :</span><span class="sxs-lookup"><span data-stu-id="e83a1-179">Attribute group:</span></span> | <span data-ttu-id="e83a1-180">stencil-tampon</span><span class="sxs-lookup"><span data-stu-id="e83a1-180">stencil-buffer</span></span>                                                                   |
| <span data-ttu-id="e83a1-181">Valeur initiale :</span><span class="sxs-lookup"><span data-stu-id="e83a1-181">Initial value:</span></span>   | <span data-ttu-id="e83a1-182">0</span><span class="sxs-lookup"><span data-stu-id="e83a1-182">0</span></span>                                                                                |
| <span data-ttu-id="e83a1-183">Commande d’extraction :</span><span class="sxs-lookup"><span data-stu-id="e83a1-183">Get command:</span></span>     | [<span data-ttu-id="e83a1-184">**glGetIntegerv**</span><span class="sxs-lookup"><span data-stu-id="e83a1-184">**glGetIntegerv**</span></span>](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) |



 

<span data-ttu-id="e83a1-185"></dd> <dt><span id="GL_ACCUM_CLEAR_VALUE"></span><span id="gl_accum_clear_value"></span>\_valeur effacer GL amort \_ \_</dt> </span><span class="sxs-lookup"><span data-stu-id="e83a1-185"></dd> <dt><span id="GL_ACCUM_CLEAR_VALUE"></span><span id="gl_accum_clear_value"></span>GL\_ACCUM\_CLEAR\_VALUE</dt> </span></span><dd> 

|                  |                                                                                |
|------------------|--------------------------------------------------------------------------------|
| <span data-ttu-id="e83a1-186">Description :</span><span class="sxs-lookup"><span data-stu-id="e83a1-186">Description:</span></span>     | <span data-ttu-id="e83a1-187">Accumulation-valeur effacée de la mémoire tampon</span><span class="sxs-lookup"><span data-stu-id="e83a1-187">Accumulation-buffer clear value</span></span>                                                |
| <span data-ttu-id="e83a1-188">Groupe d’attributs :</span><span class="sxs-lookup"><span data-stu-id="e83a1-188">Attribute group:</span></span> | <span data-ttu-id="e83a1-189">mémoire tampon cumulée</span><span class="sxs-lookup"><span data-stu-id="e83a1-189">accum-buffer</span></span>                                                                   |
| <span data-ttu-id="e83a1-190">Valeur initiale :</span><span class="sxs-lookup"><span data-stu-id="e83a1-190">Initial value:</span></span>   | <span data-ttu-id="e83a1-191">0</span><span class="sxs-lookup"><span data-stu-id="e83a1-191">0</span></span>                                                                              |
| <span data-ttu-id="e83a1-192">Commande d’extraction :</span><span class="sxs-lookup"><span data-stu-id="e83a1-192">Get command:</span></span>     | [<span data-ttu-id="e83a1-193">**glGetFloatv**</span><span class="sxs-lookup"><span data-stu-id="e83a1-193">**glGetFloatv**</span></span>](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) |



 

</dd> </dl>

 

 




