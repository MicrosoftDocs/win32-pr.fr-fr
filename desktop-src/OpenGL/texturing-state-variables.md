---
title: Variables d’état de texturation
description: Variables d’état de texturation
ms.assetid: 2d9d3d8b-ecaa-412c-8105-ae2ca801784e
keywords:
- Variables d’état de texturage OpenGL
topic_type:
- apiref
api_name:
- Texturing State Variables
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 73a9894e9f3723cca957fdeeb2882ede8f689ee7
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/25/2019
ms.locfileid: "106511053"
---
# <a name="texturing-state-variables"></a><span data-ttu-id="cd1b4-104">Variables d’état de texturation</span><span class="sxs-lookup"><span data-stu-id="cd1b4-104">Texturing State Variables</span></span>

<dl> <span data-ttu-id="cd1b4-105"><dt><span id="GL_TEXTURE_x"></span><span id="gl_texture_x"></span><span id="GL_TEXTURE_X"></span>\_Texture GL \_ *x*</dt> </span><span class="sxs-lookup"><span data-stu-id="cd1b4-105"><dt><span id="GL_TEXTURE_x"></span><span id="gl_texture_x"></span><span id="GL_TEXTURE_X"></span>GL\_TEXTURE\_*x*</dt> </span></span><dd> 

|                  |                                                       |
|------------------|-------------------------------------------------------|
| <span data-ttu-id="cd1b4-106">Description :</span><span class="sxs-lookup"><span data-stu-id="cd1b4-106">Description:</span></span>     | <span data-ttu-id="cd1b4-107">True si la texture *x*   -d est activée (*x* est 1-d ou 2D-d)</span><span class="sxs-lookup"><span data-stu-id="cd1b4-107">True if *x* - D texturing enabled (*x* is 1-D or 2-D)</span></span> |
| <span data-ttu-id="cd1b4-108">Groupe d’attributs :</span><span class="sxs-lookup"><span data-stu-id="cd1b4-108">Attribute group:</span></span> | <span data-ttu-id="cd1b4-109">texture/activation</span><span class="sxs-lookup"><span data-stu-id="cd1b4-109">texture/enable</span></span>                                        |
| <span data-ttu-id="cd1b4-110">Valeur initiale :</span><span class="sxs-lookup"><span data-stu-id="cd1b4-110">Initial value:</span></span>   | <span data-ttu-id="cd1b4-111">GL- \_ faux</span><span class="sxs-lookup"><span data-stu-id="cd1b4-111">GL\_FALSE</span></span>                                             |
| <span data-ttu-id="cd1b4-112">Commande d’extraction :</span><span class="sxs-lookup"><span data-stu-id="cd1b4-112">Get command:</span></span>     | [<span data-ttu-id="cd1b4-113">**glIsEnabled**</span><span class="sxs-lookup"><span data-stu-id="cd1b4-113">**glIsEnabled**</span></span>](glisenabled.md)                    |



 

<span data-ttu-id="cd1b4-114"></dd> <dt><span id="GL_TEXTURE"></span><span id="gl_texture"></span>\_texture GL</dt> </span><span class="sxs-lookup"><span data-stu-id="cd1b4-114"></dd> <dt><span id="GL_TEXTURE"></span><span id="gl_texture"></span>GL\_TEXTURE</dt> </span></span><dd> 

|                  |                                              |
|------------------|----------------------------------------------|
| <span data-ttu-id="cd1b4-115">Description :</span><span class="sxs-lookup"><span data-stu-id="cd1b4-115">Description:</span></span>     | <span data-ttu-id="cd1b4-116">*x*   Image de texture-D au niveau de détail *i*</span><span class="sxs-lookup"><span data-stu-id="cd1b4-116">*x* - D texture image at level of detail *i*</span></span> |
| <span data-ttu-id="cd1b4-117">Groupe d’attributs :</span><span class="sxs-lookup"><span data-stu-id="cd1b4-117">Attribute group:</span></span> |                                              |
| <span data-ttu-id="cd1b4-118">Valeur initiale :</span><span class="sxs-lookup"><span data-stu-id="cd1b4-118">Initial value:</span></span>   |                                              |
| <span data-ttu-id="cd1b4-119">Commande d’extraction :</span><span class="sxs-lookup"><span data-stu-id="cd1b4-119">Get command:</span></span>     | [<span data-ttu-id="cd1b4-120">**glGetTexImage**</span><span class="sxs-lookup"><span data-stu-id="cd1b4-120">**glGetTexImage**</span></span>](glgetteximage.md)       |



 

<span data-ttu-id="cd1b4-121"></dd> <dt><span id="GL_TEXTURE_WIDTH"></span><span id="gl_texture_width"></span>largeur de la \_ texture GL \_</dt> </span><span class="sxs-lookup"><span data-stu-id="cd1b4-121"></dd> <dt><span id="GL_TEXTURE_WIDTH"></span><span id="gl_texture_width"></span>GL\_TEXTURE\_WIDTH</dt> </span></span><dd> 

|                  |                                                          |
|------------------|----------------------------------------------------------|
| <span data-ttu-id="cd1b4-122">Description :</span><span class="sxs-lookup"><span data-stu-id="cd1b4-122">Description:</span></span>     | <span data-ttu-id="cd1b4-123">*x*   -D image de texture D *i*   largeur</span><span class="sxs-lookup"><span data-stu-id="cd1b4-123">*x* - D texture image *i* 's width</span></span>                       |
| <span data-ttu-id="cd1b4-124">Groupe d’attributs :</span><span class="sxs-lookup"><span data-stu-id="cd1b4-124">Attribute group:</span></span> |                                                          |
| <span data-ttu-id="cd1b4-125">Valeur initiale :</span><span class="sxs-lookup"><span data-stu-id="cd1b4-125">Initial value:</span></span>   | <span data-ttu-id="cd1b4-126">0</span><span class="sxs-lookup"><span data-stu-id="cd1b4-126">0</span></span>                                                        |
| <span data-ttu-id="cd1b4-127">Commande d’extraction :</span><span class="sxs-lookup"><span data-stu-id="cd1b4-127">Get command:</span></span>     | [<span data-ttu-id="cd1b4-128">**glGetTexLevelParameter**</span><span class="sxs-lookup"><span data-stu-id="cd1b4-128">**glGetTexLevelParameter**</span></span>](glgettexlevelparameter.md) |



 

<span data-ttu-id="cd1b4-129"></dd> <dt><span id="GL_TEXTURE_HEIGHT"></span><span id="gl_texture_height"></span>hauteur de la \_ texture GL \_</dt> </span><span class="sxs-lookup"><span data-stu-id="cd1b4-129"></dd> <dt><span id="GL_TEXTURE_HEIGHT"></span><span id="gl_texture_height"></span>GL\_TEXTURE\_HEIGHT</dt> </span></span><dd> 

|                  |                                                          |
|------------------|----------------------------------------------------------|
| <span data-ttu-id="cd1b4-130">Description :</span><span class="sxs-lookup"><span data-stu-id="cd1b4-130">Description:</span></span>     | <span data-ttu-id="cd1b4-131">*x*   -D image de texture D *i*   hauteur</span><span class="sxs-lookup"><span data-stu-id="cd1b4-131">*x* - D texture image *i* 's height</span></span>                      |
| <span data-ttu-id="cd1b4-132">Groupe d’attributs :</span><span class="sxs-lookup"><span data-stu-id="cd1b4-132">Attribute group:</span></span> |                                                          |
| <span data-ttu-id="cd1b4-133">Valeur initiale :</span><span class="sxs-lookup"><span data-stu-id="cd1b4-133">Initial value:</span></span>   | <span data-ttu-id="cd1b4-134">0</span><span class="sxs-lookup"><span data-stu-id="cd1b4-134">0</span></span>                                                        |
| <span data-ttu-id="cd1b4-135">Commande d’extraction :</span><span class="sxs-lookup"><span data-stu-id="cd1b4-135">Get command:</span></span>     | [<span data-ttu-id="cd1b4-136">**glGetTexLevelParameter**</span><span class="sxs-lookup"><span data-stu-id="cd1b4-136">**glGetTexLevelParameter**</span></span>](glgettexlevelparameter.md) |



 

<span data-ttu-id="cd1b4-137"></dd> <dt><span id="GL_TEXTURE_BORDER"></span><span id="gl_texture_border"></span>bordure de la \_ texture GL \_</dt> </span><span class="sxs-lookup"><span data-stu-id="cd1b4-137"></dd> <dt><span id="GL_TEXTURE_BORDER"></span><span id="gl_texture_border"></span>GL\_TEXTURE\_BORDER</dt> </span></span><dd> 

|                  |                                                          |
|------------------|----------------------------------------------------------|
| <span data-ttu-id="cd1b4-138">Description :</span><span class="sxs-lookup"><span data-stu-id="cd1b4-138">Description:</span></span>     | <span data-ttu-id="cd1b4-139">*x*   -D image de texture D *i*   bordure</span><span class="sxs-lookup"><span data-stu-id="cd1b4-139">*x* - D texture image *i* 's border</span></span>                      |
| <span data-ttu-id="cd1b4-140">Groupe d’attributs :</span><span class="sxs-lookup"><span data-stu-id="cd1b4-140">Attribute group:</span></span> |                                                          |
| <span data-ttu-id="cd1b4-141">Valeur initiale :</span><span class="sxs-lookup"><span data-stu-id="cd1b4-141">Initial value:</span></span>   | <span data-ttu-id="cd1b4-142">0</span><span class="sxs-lookup"><span data-stu-id="cd1b4-142">0</span></span>                                                        |
| <span data-ttu-id="cd1b4-143">Commande d’extraction :</span><span class="sxs-lookup"><span data-stu-id="cd1b4-143">Get command:</span></span>     | [<span data-ttu-id="cd1b4-144">**glGetTexLevelParameter**</span><span class="sxs-lookup"><span data-stu-id="cd1b4-144">**glGetTexLevelParameter**</span></span>](glgettexlevelparameter.md) |



 

<span data-ttu-id="cd1b4-145"></dd> <dt><span id="GL_TEXTURE_COMPONENTS"></span><span id="gl_texture_components"></span>\_composants de texture GL \_</dt> </span><span class="sxs-lookup"><span data-stu-id="cd1b4-145"></dd> <dt><span id="GL_TEXTURE_COMPONENTS"></span><span id="gl_texture_components"></span>GL\_TEXTURE\_COMPONENTS</dt> </span></span><dd> 

|                  |                                                          |
|------------------|----------------------------------------------------------|
| <span data-ttu-id="cd1b4-146">Description :</span><span class="sxs-lookup"><span data-stu-id="cd1b4-146">Description:</span></span>     | <span data-ttu-id="cd1b4-147">Composants d’image de texture</span><span class="sxs-lookup"><span data-stu-id="cd1b4-147">Texture image components</span></span>                                 |
| <span data-ttu-id="cd1b4-148">Groupe d’attributs :</span><span class="sxs-lookup"><span data-stu-id="cd1b4-148">Attribute group:</span></span> |                                                          |
| <span data-ttu-id="cd1b4-149">Valeur initiale :</span><span class="sxs-lookup"><span data-stu-id="cd1b4-149">Initial value:</span></span>   | <span data-ttu-id="cd1b4-150">1</span><span class="sxs-lookup"><span data-stu-id="cd1b4-150">1</span></span>                                                        |
| <span data-ttu-id="cd1b4-151">Commande d’extraction :</span><span class="sxs-lookup"><span data-stu-id="cd1b4-151">Get command:</span></span>     | [<span data-ttu-id="cd1b4-152">**glGetTexLevelParameter**</span><span class="sxs-lookup"><span data-stu-id="cd1b4-152">**glGetTexLevelParameter**</span></span>](glgettexlevelparameter.md) |



 

<span data-ttu-id="cd1b4-153"></dd> <dt><span id="GL_TEXTURE_BORDER_COLOR"></span><span id="gl_texture_border_color"></span>couleur de bordure de la \_ texture GL \_ \_</dt> </span><span class="sxs-lookup"><span data-stu-id="cd1b4-153"></dd> <dt><span id="GL_TEXTURE_BORDER_COLOR"></span><span id="gl_texture_border_color"></span>GL\_TEXTURE\_BORDER\_COLOR</dt> </span></span><dd> 

|                  |                                                |
|------------------|------------------------------------------------|
| <span data-ttu-id="cd1b4-154">Description :</span><span class="sxs-lookup"><span data-stu-id="cd1b4-154">Description:</span></span>     | <span data-ttu-id="cd1b4-155">Couleur de bordure de la texture</span><span class="sxs-lookup"><span data-stu-id="cd1b4-155">Texture border color</span></span>                           |
| <span data-ttu-id="cd1b4-156">Groupe d’attributs :</span><span class="sxs-lookup"><span data-stu-id="cd1b4-156">Attribute group:</span></span> | <span data-ttu-id="cd1b4-157">texture</span><span class="sxs-lookup"><span data-stu-id="cd1b4-157">texture</span></span>                                        |
| <span data-ttu-id="cd1b4-158">Valeur initiale :</span><span class="sxs-lookup"><span data-stu-id="cd1b4-158">Initial value:</span></span>   | <span data-ttu-id="cd1b4-159">0, 0, 0, 0</span><span class="sxs-lookup"><span data-stu-id="cd1b4-159">0, 0, 0, 0</span></span>                                     |
| <span data-ttu-id="cd1b4-160">Commande d’extraction :</span><span class="sxs-lookup"><span data-stu-id="cd1b4-160">Get command:</span></span>     | [<span data-ttu-id="cd1b4-161">**glGetTexParameter**</span><span class="sxs-lookup"><span data-stu-id="cd1b4-161">**glGetTexParameter**</span></span>](glgettexparameter.md) |



 

<span data-ttu-id="cd1b4-162"></dd> <dt><span id="GL_TEXTURE_MIN_FILTER"></span><span id="gl_texture_min_filter"></span>filtre de la \_ texture GL \_ min. \_</dt> </span><span class="sxs-lookup"><span data-stu-id="cd1b4-162"></dd> <dt><span id="GL_TEXTURE_MIN_FILTER"></span><span id="gl_texture_min_filter"></span>GL\_TEXTURE\_MIN\_FILTER</dt> </span></span><dd> 

|                  |                                                |
|------------------|------------------------------------------------|
| <span data-ttu-id="cd1b4-163">Description :</span><span class="sxs-lookup"><span data-stu-id="cd1b4-163">Description:</span></span>     | <span data-ttu-id="cd1b4-164">Fonction de réduction de texture</span><span class="sxs-lookup"><span data-stu-id="cd1b4-164">Texture minification function</span></span>                  |
| <span data-ttu-id="cd1b4-165">Groupe d’attributs :</span><span class="sxs-lookup"><span data-stu-id="cd1b4-165">Attribute group:</span></span> | <span data-ttu-id="cd1b4-166">texture</span><span class="sxs-lookup"><span data-stu-id="cd1b4-166">texture</span></span>                                        |
| <span data-ttu-id="cd1b4-167">Valeur initiale :</span><span class="sxs-lookup"><span data-stu-id="cd1b4-167">Initial value:</span></span>   | <span data-ttu-id="cd1b4-168">MIPMAP linéaire de la comptabilité la \_ plus proche \_ \_</span><span class="sxs-lookup"><span data-stu-id="cd1b4-168">GL\_NEAREST\_MIPMAP\_LINEAR</span></span>                    |
| <span data-ttu-id="cd1b4-169">Commande d’extraction :</span><span class="sxs-lookup"><span data-stu-id="cd1b4-169">Get command:</span></span>     | [<span data-ttu-id="cd1b4-170">**glGetTexParameter**</span><span class="sxs-lookup"><span data-stu-id="cd1b4-170">**glGetTexParameter**</span></span>](glgettexparameter.md) |



 

<span data-ttu-id="cd1b4-171"></dd> <dt><span id="GL_TEXTURE_MAG_FILTER"></span><span id="gl_texture_mag_filter"></span>filtre de la \_ texture GL \_ \_</dt> </span><span class="sxs-lookup"><span data-stu-id="cd1b4-171"></dd> <dt><span id="GL_TEXTURE_MAG_FILTER"></span><span id="gl_texture_mag_filter"></span>GL\_TEXTURE\_MAG\_FILTER</dt> </span></span><dd> 

|                  |                                                |
|------------------|------------------------------------------------|
| <span data-ttu-id="cd1b4-172">Description :</span><span class="sxs-lookup"><span data-stu-id="cd1b4-172">Description:</span></span>     | <span data-ttu-id="cd1b4-173">Fonction d’agrandissement de texture</span><span class="sxs-lookup"><span data-stu-id="cd1b4-173">Texture magnification function</span></span>                 |
| <span data-ttu-id="cd1b4-174">Groupe d’attributs :</span><span class="sxs-lookup"><span data-stu-id="cd1b4-174">Attribute group:</span></span> | <span data-ttu-id="cd1b4-175">texture</span><span class="sxs-lookup"><span data-stu-id="cd1b4-175">texture</span></span>                                        |
| <span data-ttu-id="cd1b4-176">Valeur initiale :</span><span class="sxs-lookup"><span data-stu-id="cd1b4-176">Initial value:</span></span>   | <span data-ttu-id="cd1b4-177">linéaire du GL \_</span><span class="sxs-lookup"><span data-stu-id="cd1b4-177">GL\_LINEAR</span></span>                                     |
| <span data-ttu-id="cd1b4-178">Commande d’extraction :</span><span class="sxs-lookup"><span data-stu-id="cd1b4-178">Get command:</span></span>     | [<span data-ttu-id="cd1b4-179">**glGetTexParameter**</span><span class="sxs-lookup"><span data-stu-id="cd1b4-179">**glGetTexParameter**</span></span>](glgettexparameter.md) |



 

<span data-ttu-id="cd1b4-180"></dd> <dt><span id="GL_TEXTURE_WRAP__x"></span><span id="gl_texture_wrap__x"></span><span id="GL_TEXTURE_WRAP__X"></span>\_Enveloppe de \_ la texture GL \_ *x*</dt> </span><span class="sxs-lookup"><span data-stu-id="cd1b4-180"></dd> <dt><span id="GL_TEXTURE_WRAP__x"></span><span id="gl_texture_wrap__x"></span><span id="GL_TEXTURE_WRAP__X"></span>GL\_TEXTURE\_WRAP\_ *x*</dt> </span></span><dd> 

|                  |                                                |
|------------------|------------------------------------------------|
| <span data-ttu-id="cd1b4-181">Description :</span><span class="sxs-lookup"><span data-stu-id="cd1b4-181">Description:</span></span>     | <span data-ttu-id="cd1b4-182">Mode habillage de la texture (*x*   est S ou T)</span><span class="sxs-lookup"><span data-stu-id="cd1b4-182">Texture wrap mode (*x* is S or T)</span></span>              |
| <span data-ttu-id="cd1b4-183">Groupe d’attributs :</span><span class="sxs-lookup"><span data-stu-id="cd1b4-183">Attribute group:</span></span> | <span data-ttu-id="cd1b4-184">texture</span><span class="sxs-lookup"><span data-stu-id="cd1b4-184">texture</span></span>                                        |
| <span data-ttu-id="cd1b4-185">Valeur initiale :</span><span class="sxs-lookup"><span data-stu-id="cd1b4-185">Initial value:</span></span>   | <span data-ttu-id="cd1b4-186">répétition du GL \_</span><span class="sxs-lookup"><span data-stu-id="cd1b4-186">GL\_REPEAT</span></span>                                     |
| <span data-ttu-id="cd1b4-187">Commande d’extraction :</span><span class="sxs-lookup"><span data-stu-id="cd1b4-187">Get command:</span></span>     | [<span data-ttu-id="cd1b4-188">**glGetTexParameter**</span><span class="sxs-lookup"><span data-stu-id="cd1b4-188">**glGetTexParameter**</span></span>](glgettexparameter.md) |



 

<span data-ttu-id="cd1b4-189"></dd> <dt><span id="GL_TEXTURE_ENV_MODE"></span><span id="gl_texture_env_mode"></span>\_ \_ mode env de la texture GL \_</dt> </span><span class="sxs-lookup"><span data-stu-id="cd1b4-189"></dd> <dt><span id="GL_TEXTURE_ENV_MODE"></span><span id="gl_texture_env_mode"></span>GL\_TEXTURE\_ENV\_MODE</dt> </span></span><dd> 

|                  |                                      |
|------------------|--------------------------------------|
| <span data-ttu-id="cd1b4-190">Description :</span><span class="sxs-lookup"><span data-stu-id="cd1b4-190">Description:</span></span>     | <span data-ttu-id="cd1b4-191">Fonction d’application de texture</span><span class="sxs-lookup"><span data-stu-id="cd1b4-191">Texture application function</span></span>         |
| <span data-ttu-id="cd1b4-192">Groupe d’attributs :</span><span class="sxs-lookup"><span data-stu-id="cd1b4-192">Attribute group:</span></span> | <span data-ttu-id="cd1b4-193">texture</span><span class="sxs-lookup"><span data-stu-id="cd1b4-193">texture</span></span>                              |
| <span data-ttu-id="cd1b4-194">Valeur initiale :</span><span class="sxs-lookup"><span data-stu-id="cd1b4-194">Initial value:</span></span>   | <span data-ttu-id="cd1b4-195">module comptabilité GL \_</span><span class="sxs-lookup"><span data-stu-id="cd1b4-195">GL\_MODULATE</span></span>                         |
| <span data-ttu-id="cd1b4-196">Commande d’extraction :</span><span class="sxs-lookup"><span data-stu-id="cd1b4-196">Get command:</span></span>     | [<span data-ttu-id="cd1b4-197">**glGetTexEnviv**</span><span class="sxs-lookup"><span data-stu-id="cd1b4-197">**glGetTexEnviv**</span></span>](glgettexenv.md) |



 

<span data-ttu-id="cd1b4-198"></dd> <dt><span id="GL_TEXTURE_ENV_COLOR"></span><span id="gl_texture_env_color"></span>couleur de la texture du GL \_ \_ env \_</dt> </span><span class="sxs-lookup"><span data-stu-id="cd1b4-198"></dd> <dt><span id="GL_TEXTURE_ENV_COLOR"></span><span id="gl_texture_env_color"></span>GL\_TEXTURE\_ENV\_COLOR</dt> </span></span><dd> 

|                  |                                      |
|------------------|--------------------------------------|
| <span data-ttu-id="cd1b4-199">Description :</span><span class="sxs-lookup"><span data-stu-id="cd1b4-199">Description:</span></span>     | <span data-ttu-id="cd1b4-200">Couleur de l’environnement de texture</span><span class="sxs-lookup"><span data-stu-id="cd1b4-200">Texture environment color</span></span>            |
| <span data-ttu-id="cd1b4-201">Groupe d’attributs :</span><span class="sxs-lookup"><span data-stu-id="cd1b4-201">Attribute group:</span></span> | <span data-ttu-id="cd1b4-202">texture</span><span class="sxs-lookup"><span data-stu-id="cd1b4-202">texture</span></span>                              |
| <span data-ttu-id="cd1b4-203">Valeur initiale :</span><span class="sxs-lookup"><span data-stu-id="cd1b4-203">Initial value:</span></span>   | <span data-ttu-id="cd1b4-204">0, 0, 0, 0</span><span class="sxs-lookup"><span data-stu-id="cd1b4-204">0, 0, 0, 0</span></span>                           |
| <span data-ttu-id="cd1b4-205">Commande d’extraction :</span><span class="sxs-lookup"><span data-stu-id="cd1b4-205">Get command:</span></span>     | [<span data-ttu-id="cd1b4-206">**glGetTexEnvfv**</span><span class="sxs-lookup"><span data-stu-id="cd1b4-206">**glGetTexEnvfv**</span></span>](glgettexenv.md) |



 

<span data-ttu-id="cd1b4-207"></dd> <dt><span id="GL_TEXTURE_GEN__x"></span><span id="gl_texture_gen__x"></span><span id="GL_TEXTURE_GEN__X"></span>GL \_ texture \_ GEN \_ *x*</dt> </span><span class="sxs-lookup"><span data-stu-id="cd1b4-207"></dd> <dt><span id="GL_TEXTURE_GEN__x"></span><span id="gl_texture_gen__x"></span><span id="GL_TEXTURE_GEN__X"></span>GL\_TEXTURE\_GEN\_ *x*</dt> </span></span><dd> 

|                  |                                          |
|------------------|------------------------------------------|
| <span data-ttu-id="cd1b4-208">Description :</span><span class="sxs-lookup"><span data-stu-id="cd1b4-208">Description:</span></span>     | <span data-ttu-id="cd1b4-209">Texgen est activé (*x*   est S, T, R ou Q)</span><span class="sxs-lookup"><span data-stu-id="cd1b4-209">Texgen is enabled (*x* is S, T, R, or Q)</span></span> |
| <span data-ttu-id="cd1b4-210">Groupe d’attributs :</span><span class="sxs-lookup"><span data-stu-id="cd1b4-210">Attribute group:</span></span> | <span data-ttu-id="cd1b4-211">texture/activation</span><span class="sxs-lookup"><span data-stu-id="cd1b4-211">texture/enable</span></span>                           |
| <span data-ttu-id="cd1b4-212">Valeur initiale :</span><span class="sxs-lookup"><span data-stu-id="cd1b4-212">Initial value:</span></span>   | <span data-ttu-id="cd1b4-213">GL- \_ faux</span><span class="sxs-lookup"><span data-stu-id="cd1b4-213">GL\_FALSE</span></span>                                |
| <span data-ttu-id="cd1b4-214">Commande d’extraction :</span><span class="sxs-lookup"><span data-stu-id="cd1b4-214">Get command:</span></span>     | [<span data-ttu-id="cd1b4-215">**glIsEnabled**</span><span class="sxs-lookup"><span data-stu-id="cd1b4-215">**glIsEnabled**</span></span>](glisenabled.md)       |



 

<span data-ttu-id="cd1b4-216"></dd> <dt><span id="GL_EYE_PLANE"></span><span id="gl_eye_plane"></span>\_plan oculaire \_ GL</dt> </span><span class="sxs-lookup"><span data-stu-id="cd1b4-216"></dd> <dt><span id="GL_EYE_PLANE"></span><span id="gl_eye_plane"></span>GL\_EYE\_PLANE</dt> </span></span><dd> 

|                  |                                      |
|------------------|--------------------------------------|
| <span data-ttu-id="cd1b4-217">Description :</span><span class="sxs-lookup"><span data-stu-id="cd1b4-217">Description:</span></span>     | <span data-ttu-id="cd1b4-218">Coefficients d’équation du plan Texgen</span><span class="sxs-lookup"><span data-stu-id="cd1b4-218">Texgen plane equation coefficients</span></span>   |
| <span data-ttu-id="cd1b4-219">Groupe d’attributs :</span><span class="sxs-lookup"><span data-stu-id="cd1b4-219">Attribute group:</span></span> | <span data-ttu-id="cd1b4-220">texture</span><span class="sxs-lookup"><span data-stu-id="cd1b4-220">texture</span></span>                              |
| <span data-ttu-id="cd1b4-221">Valeur initiale :</span><span class="sxs-lookup"><span data-stu-id="cd1b4-221">Initial value:</span></span>   |                                      |
| <span data-ttu-id="cd1b4-222">Commande d’extraction :</span><span class="sxs-lookup"><span data-stu-id="cd1b4-222">Get command:</span></span>     | [<span data-ttu-id="cd1b4-223">**glGetTexGenfv**</span><span class="sxs-lookup"><span data-stu-id="cd1b4-223">**glGetTexGenfv**</span></span>](glgettexgen.md) |



 

<span data-ttu-id="cd1b4-224"></dd> <dt><span id="GL_OBJECT_PLANE"></span><span id="gl_object_plane"></span>\_plan d’objet GL \_</dt> </span><span class="sxs-lookup"><span data-stu-id="cd1b4-224"></dd> <dt><span id="GL_OBJECT_PLANE"></span><span id="gl_object_plane"></span>GL\_OBJECT\_PLANE</dt> </span></span><dd> 

|                  |                                      |
|------------------|--------------------------------------|
| <span data-ttu-id="cd1b4-225">Description :</span><span class="sxs-lookup"><span data-stu-id="cd1b4-225">Description:</span></span>     | <span data-ttu-id="cd1b4-226">Objets Texgen-coefficients linéaires</span><span class="sxs-lookup"><span data-stu-id="cd1b4-226">Texgen object linear coefficients</span></span>    |
| <span data-ttu-id="cd1b4-227">Groupe d’attributs :</span><span class="sxs-lookup"><span data-stu-id="cd1b4-227">Attribute group:</span></span> | <span data-ttu-id="cd1b4-228">texture</span><span class="sxs-lookup"><span data-stu-id="cd1b4-228">texture</span></span>                              |
| <span data-ttu-id="cd1b4-229">Valeur initiale :</span><span class="sxs-lookup"><span data-stu-id="cd1b4-229">Initial value:</span></span>   |                                      |
| <span data-ttu-id="cd1b4-230">Commande d’extraction :</span><span class="sxs-lookup"><span data-stu-id="cd1b4-230">Get command:</span></span>     | [<span data-ttu-id="cd1b4-231">**glGetTexGenfv**</span><span class="sxs-lookup"><span data-stu-id="cd1b4-231">**glGetTexGenfv**</span></span>](glgettexgen.md) |



 

<span data-ttu-id="cd1b4-232"></dd> <dt><span id="GL_TEXTURE_GEN_MODE"></span><span id="gl_texture_gen_mode"></span>\_mode de génération de textures GL \_ \_</dt> </span><span class="sxs-lookup"><span data-stu-id="cd1b4-232"></dd> <dt><span id="GL_TEXTURE_GEN_MODE"></span><span id="gl_texture_gen_mode"></span>GL\_TEXTURE\_GEN\_MODE</dt> </span></span><dd> 

|                  |                                      |
|------------------|--------------------------------------|
| <span data-ttu-id="cd1b4-233">Description :</span><span class="sxs-lookup"><span data-stu-id="cd1b4-233">Description:</span></span>     | <span data-ttu-id="cd1b4-234">Fonction utilisée pour texgen</span><span class="sxs-lookup"><span data-stu-id="cd1b4-234">Function used for texgen</span></span>             |
| <span data-ttu-id="cd1b4-235">Groupe d’attributs :</span><span class="sxs-lookup"><span data-stu-id="cd1b4-235">Attribute group:</span></span> | <span data-ttu-id="cd1b4-236">texture</span><span class="sxs-lookup"><span data-stu-id="cd1b4-236">texture</span></span>                              |
| <span data-ttu-id="cd1b4-237">Valeur initiale :</span><span class="sxs-lookup"><span data-stu-id="cd1b4-237">Initial value:</span></span>   | <span data-ttu-id="cd1b4-238">linéaire de l' \_ oeil GL \_</span><span class="sxs-lookup"><span data-stu-id="cd1b4-238">GL\_EYE\_LINEAR</span></span>                      |
| <span data-ttu-id="cd1b4-239">Commande d’extraction :</span><span class="sxs-lookup"><span data-stu-id="cd1b4-239">Get command:</span></span>     | [<span data-ttu-id="cd1b4-240">**glGetTexGeniv**</span><span class="sxs-lookup"><span data-stu-id="cd1b4-240">**glGetTexGeniv**</span></span>](glgettexgen.md) |



 

</dd> </dl>

 

 




