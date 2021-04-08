---
title: Variables d’État diverses
description: Variables d’État diverses
ms.assetid: 4c99b9b6-5cd3-49d1-9bfe-fa1421d892f2
keywords:
- Variables d’État diverses OpenGL
topic_type:
- apiref
api_name:
- Miscellaneous State Variables
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 73da6292187fcbc9cd17f94fe88f63160d89be5b
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/25/2019
ms.locfileid: "103678129"
---
# <a name="miscellaneous-state-variables"></a><span data-ttu-id="5816f-104">Variables d’État diverses</span><span class="sxs-lookup"><span data-stu-id="5816f-104">Miscellaneous State Variables</span></span>

<dl> <span data-ttu-id="5816f-105"><dt><span id="GL_LIST_BASE"></span><span id="gl_list_base"></span>BASE de la \_ liste GL \_</dt> </span><span class="sxs-lookup"><span data-stu-id="5816f-105"><dt><span id="GL_LIST_BASE"></span><span id="gl_list_base"></span>GL\_LIST\_BASE</dt> </span></span><dd> 

|                  |                                        |
|------------------|----------------------------------------|
| <span data-ttu-id="5816f-106">Description :</span><span class="sxs-lookup"><span data-stu-id="5816f-106">Description:</span></span>     | <span data-ttu-id="5816f-107">Définition de **glListBase**</span><span class="sxs-lookup"><span data-stu-id="5816f-107">Setting of **glListBase**</span></span>              |
| <span data-ttu-id="5816f-108">Groupe d’attributs :</span><span class="sxs-lookup"><span data-stu-id="5816f-108">Attribute group:</span></span> | <span data-ttu-id="5816f-109">list</span><span class="sxs-lookup"><span data-stu-id="5816f-109">list</span></span>                                   |
| <span data-ttu-id="5816f-110">Valeur initiale :</span><span class="sxs-lookup"><span data-stu-id="5816f-110">Initial value:</span></span>   | <span data-ttu-id="5816f-111">0</span><span class="sxs-lookup"><span data-stu-id="5816f-111">0</span></span>                                      |
| <span data-ttu-id="5816f-112">Commande d’extraction :</span><span class="sxs-lookup"><span data-stu-id="5816f-112">Get command:</span></span>     | [<span data-ttu-id="5816f-113">**glGetIntegerv**</span><span class="sxs-lookup"><span data-stu-id="5816f-113">**glGetIntegerv**</span></span>](glgetintegerv.md) |



 

<span data-ttu-id="5816f-114"></dd> <dt><span id="GL_LIST_INDEX"></span><span id="gl_list_index"></span>\_index de liste GL \_</dt> </span><span class="sxs-lookup"><span data-stu-id="5816f-114"></dd> <dt><span id="GL_LIST_INDEX"></span><span id="gl_list_index"></span>GL\_LIST\_INDEX</dt> </span></span><dd> 

|                  |                                                                                  |
|------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="5816f-115">Description :</span><span class="sxs-lookup"><span data-stu-id="5816f-115">Description:</span></span>     | <span data-ttu-id="5816f-116">Nombre de listes d’affichage en cours de construction ; 0 si aucun</span><span class="sxs-lookup"><span data-stu-id="5816f-116">Number of display lists under construction; 0 if none</span></span>                            |
| <span data-ttu-id="5816f-117">Groupe d’attributs :</span><span class="sxs-lookup"><span data-stu-id="5816f-117">Attribute group:</span></span> |                                                                                  |
| <span data-ttu-id="5816f-118">Valeur initiale :</span><span class="sxs-lookup"><span data-stu-id="5816f-118">Initial value:</span></span>   | <span data-ttu-id="5816f-119">0</span><span class="sxs-lookup"><span data-stu-id="5816f-119">0</span></span>                                                                                |
| <span data-ttu-id="5816f-120">Commande d’extraction :</span><span class="sxs-lookup"><span data-stu-id="5816f-120">Get command:</span></span>     | [<span data-ttu-id="5816f-121">**glGetIntegerv**</span><span class="sxs-lookup"><span data-stu-id="5816f-121">**glGetIntegerv**</span></span>](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) |



 

<span data-ttu-id="5816f-122"></dd> <dt><span id="GL_LIST_MODE"></span><span id="gl_list_mode"></span>\_mode de liste du GL \_</dt> </span><span class="sxs-lookup"><span data-stu-id="5816f-122"></dd> <dt><span id="GL_LIST_MODE"></span><span id="gl_list_mode"></span>GL\_LIST\_MODE</dt> </span></span><dd> 

|                  |                                                                                  |
|------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="5816f-123">Description :</span><span class="sxs-lookup"><span data-stu-id="5816f-123">Description:</span></span>     | <span data-ttu-id="5816f-124">Mode de la liste d’affichage en cours de construction ; non défini si aucun</span><span class="sxs-lookup"><span data-stu-id="5816f-124">Mode of display list under construction; undefined if none</span></span>                       |
| <span data-ttu-id="5816f-125">Groupe d’attributs :</span><span class="sxs-lookup"><span data-stu-id="5816f-125">Attribute group:</span></span> |                                                                                  |
| <span data-ttu-id="5816f-126">Valeur initiale :</span><span class="sxs-lookup"><span data-stu-id="5816f-126">Initial value:</span></span>   | <span data-ttu-id="5816f-127">0</span><span class="sxs-lookup"><span data-stu-id="5816f-127">0</span></span>                                                                                |
| <span data-ttu-id="5816f-128">Commande d’extraction :</span><span class="sxs-lookup"><span data-stu-id="5816f-128">Get command:</span></span>     | [<span data-ttu-id="5816f-129">**glGetIntegerv**</span><span class="sxs-lookup"><span data-stu-id="5816f-129">**glGetIntegerv**</span></span>](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) |



 

<span data-ttu-id="5816f-130"></dd> <dt><span id="GL_ATTRIB_STACK_DEPTH"></span><span id="gl_attrib_stack_depth"></span>profondeur de la \_ pile GL attrib \_ \_</dt> </span><span class="sxs-lookup"><span data-stu-id="5816f-130"></dd> <dt><span id="GL_ATTRIB_STACK_DEPTH"></span><span id="gl_attrib_stack_depth"></span>GL\_ATTRIB\_STACK\_DEPTH</dt> </span></span><dd> 

|                  |                                                                                  |
|------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="5816f-131">Description :</span><span class="sxs-lookup"><span data-stu-id="5816f-131">Description:</span></span>     | <span data-ttu-id="5816f-132">Pointeur de pile d’attributs</span><span class="sxs-lookup"><span data-stu-id="5816f-132">Attribute stack pointer</span></span>                                                          |
| <span data-ttu-id="5816f-133">Groupe d’attributs :</span><span class="sxs-lookup"><span data-stu-id="5816f-133">Attribute group:</span></span> |                                                                                  |
| <span data-ttu-id="5816f-134">Valeur initiale :</span><span class="sxs-lookup"><span data-stu-id="5816f-134">Initial value:</span></span>   | <span data-ttu-id="5816f-135">0</span><span class="sxs-lookup"><span data-stu-id="5816f-135">0</span></span>                                                                                |
| <span data-ttu-id="5816f-136">Commande d’extraction :</span><span class="sxs-lookup"><span data-stu-id="5816f-136">Get command:</span></span>     | [<span data-ttu-id="5816f-137">**glGetIntegerv**</span><span class="sxs-lookup"><span data-stu-id="5816f-137">**glGetIntegerv**</span></span>](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) |



 

<span data-ttu-id="5816f-138"></dd> <dt><span id="GL_NAME_STACK_DEPTH"></span><span id="gl_name_stack_depth"></span>profondeur de la \_ pile de noms GL \_ \_</dt> </span><span class="sxs-lookup"><span data-stu-id="5816f-138"></dd> <dt><span id="GL_NAME_STACK_DEPTH"></span><span id="gl_name_stack_depth"></span>GL\_NAME\_STACK\_DEPTH</dt> </span></span><dd> 

|                  |                                                                                  |
|------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="5816f-139">Description :</span><span class="sxs-lookup"><span data-stu-id="5816f-139">Description:</span></span>     | <span data-ttu-id="5816f-140">Profondeur de la pile de noms</span><span class="sxs-lookup"><span data-stu-id="5816f-140">Name stack depth</span></span>                                                                 |
| <span data-ttu-id="5816f-141">Groupe d’attributs :</span><span class="sxs-lookup"><span data-stu-id="5816f-141">Attribute group:</span></span> |                                                                                  |
| <span data-ttu-id="5816f-142">Valeur initiale :</span><span class="sxs-lookup"><span data-stu-id="5816f-142">Initial value:</span></span>   | <span data-ttu-id="5816f-143">0</span><span class="sxs-lookup"><span data-stu-id="5816f-143">0</span></span>                                                                                |
| <span data-ttu-id="5816f-144">Commande d’extraction :</span><span class="sxs-lookup"><span data-stu-id="5816f-144">Get command:</span></span>     | [<span data-ttu-id="5816f-145">**glGetIntegerv**</span><span class="sxs-lookup"><span data-stu-id="5816f-145">**glGetIntegerv**</span></span>](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) |



 

<span data-ttu-id="5816f-146"></dd> <dt><span id="GL_RENDER_MODE"></span><span id="gl_render_mode"></span>\_mode de rendu du GL \_</dt> </span><span class="sxs-lookup"><span data-stu-id="5816f-146"></dd> <dt><span id="GL_RENDER_MODE"></span><span id="gl_render_mode"></span>GL\_RENDER\_MODE</dt> </span></span><dd> 

|                  |                                                                                  |
|------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="5816f-147">Description :</span><span class="sxs-lookup"><span data-stu-id="5816f-147">Description:</span></span>     | <span data-ttu-id="5816f-148">paramètre **glRenderMode**</span><span class="sxs-lookup"><span data-stu-id="5816f-148">**glRenderMode** setting</span></span>                                                         |
| <span data-ttu-id="5816f-149">Groupe d’attributs :</span><span class="sxs-lookup"><span data-stu-id="5816f-149">Attribute group:</span></span> |                                                                                  |
| <span data-ttu-id="5816f-150">Valeur initiale :</span><span class="sxs-lookup"><span data-stu-id="5816f-150">Initial value:</span></span>   | <span data-ttu-id="5816f-151">\_rendu GL</span><span class="sxs-lookup"><span data-stu-id="5816f-151">GL\_RENDER</span></span>                                                                       |
| <span data-ttu-id="5816f-152">Commande d’extraction :</span><span class="sxs-lookup"><span data-stu-id="5816f-152">Get command:</span></span>     | [<span data-ttu-id="5816f-153">**glGetIntegerv**</span><span class="sxs-lookup"><span data-stu-id="5816f-153">**glGetIntegerv**</span></span>](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) |



 



|                  |                                  |
|------------------|----------------------------------|
| <span data-ttu-id="5816f-154">Description :</span><span class="sxs-lookup"><span data-stu-id="5816f-154">Description:</span></span>     | <span data-ttu-id="5816f-155">Codes d’erreur actuels</span><span class="sxs-lookup"><span data-stu-id="5816f-155">Current error codes</span></span>              |
| <span data-ttu-id="5816f-156">Groupe d’attributs :</span><span class="sxs-lookup"><span data-stu-id="5816f-156">Attribute group:</span></span> |                                  |
| <span data-ttu-id="5816f-157">Valeur initiale :</span><span class="sxs-lookup"><span data-stu-id="5816f-157">Initial value:</span></span>   | <span data-ttu-id="5816f-158">0</span><span class="sxs-lookup"><span data-stu-id="5816f-158">0</span></span>                                |
| <span data-ttu-id="5816f-159">Commande d’extraction :</span><span class="sxs-lookup"><span data-stu-id="5816f-159">Get command:</span></span>     | [<span data-ttu-id="5816f-160">**glGetError**</span><span class="sxs-lookup"><span data-stu-id="5816f-160">**glGetError**</span></span>](glgeterror.md) |



 

</dd> </dl>

 

 




