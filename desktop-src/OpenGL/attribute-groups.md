---
title: Groupes d'attributs
description: Groupes d'attributs
ms.assetid: 9fd7dc6e-6749-4e32-b795-21b63b64c291
keywords:
- OpenGL, groupes d’attributs
- Référence OpenGL, groupes d’attributs
- référence pour OpenGL, groupes d’attributs
- groupes Attribut
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1d93582c8996438ad99d7bf896cf83bdf6fbf72d
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "106512662"
---
# <a name="attribute-groups"></a><span data-ttu-id="adbbf-107">Groupes d'attributs</span><span class="sxs-lookup"><span data-stu-id="adbbf-107">Attribute Groups</span></span>



| <span data-ttu-id="adbbf-108">Bit de masque</span><span class="sxs-lookup"><span data-stu-id="adbbf-108">Mask bit</span></span>                  | <span data-ttu-id="adbbf-109">Groupe d'attributs</span><span class="sxs-lookup"><span data-stu-id="adbbf-109">Attribute group</span></span> |
|---------------------------|-----------------|
| <span data-ttu-id="adbbf-110">\_bit de tampon amort \_ \_</span><span class="sxs-lookup"><span data-stu-id="adbbf-110">GL\_ACCUM\_BUFFER\_BIT</span></span>    | <span data-ttu-id="adbbf-111">mémoire tampon cumulée</span><span class="sxs-lookup"><span data-stu-id="adbbf-111">accum-buffer</span></span>    |
| <span data-ttu-id="adbbf-112">\_bits de tous les \_ attributs du GL \_</span><span class="sxs-lookup"><span data-stu-id="adbbf-112">GL\_ALL\_ATTRIB\_BITS</span></span>     |                 |
| <span data-ttu-id="adbbf-113">\_bit de \_ mémoire tampon de couleur GL \_</span><span class="sxs-lookup"><span data-stu-id="adbbf-113">GL\_COLOR\_BUFFER\_BIT</span></span>    | <span data-ttu-id="adbbf-114">mémoire tampon de couleur</span><span class="sxs-lookup"><span data-stu-id="adbbf-114">color-buffer</span></span>    |
| <span data-ttu-id="adbbf-115">\_bit actuel du GL \_</span><span class="sxs-lookup"><span data-stu-id="adbbf-115">GL\_CURRENT\_BIT</span></span>          | <span data-ttu-id="adbbf-116">actuels</span><span class="sxs-lookup"><span data-stu-id="adbbf-116">current</span></span>         |
| <span data-ttu-id="adbbf-117">\_bit de \_ mémoire tampon de profondeur GL \_</span><span class="sxs-lookup"><span data-stu-id="adbbf-117">GL\_DEPTH\_BUFFER\_BIT</span></span>    | <span data-ttu-id="adbbf-118">mémoire tampon de profondeur</span><span class="sxs-lookup"><span data-stu-id="adbbf-118">depth-buffer</span></span>    |
| <span data-ttu-id="adbbf-119">\_bit d’activation du GL \_</span><span class="sxs-lookup"><span data-stu-id="adbbf-119">GL\_ENABLE\_BIT</span></span>           | <span data-ttu-id="adbbf-120">enable</span><span class="sxs-lookup"><span data-stu-id="adbbf-120">enable</span></span>          |
| <span data-ttu-id="adbbf-121">\_bit d’évaluation du GL \_</span><span class="sxs-lookup"><span data-stu-id="adbbf-121">GL\_EVAL\_BIT</span></span>             | <span data-ttu-id="adbbf-122">eval</span><span class="sxs-lookup"><span data-stu-id="adbbf-122">eval</span></span>            |
| <span data-ttu-id="adbbf-123">\_bit de brouillard GL \_</span><span class="sxs-lookup"><span data-stu-id="adbbf-123">GL\_FOG\_BIT</span></span>              | <span data-ttu-id="adbbf-124">brouillard</span><span class="sxs-lookup"><span data-stu-id="adbbf-124">fog</span></span>             |
| <span data-ttu-id="adbbf-125">\_bit indicateur \_ GL</span><span class="sxs-lookup"><span data-stu-id="adbbf-125">GL\_HINT\_BIT</span></span>             | <span data-ttu-id="adbbf-126">indicateur</span><span class="sxs-lookup"><span data-stu-id="adbbf-126">hint</span></span>            |
| <span data-ttu-id="adbbf-127">\_bit d’éclairage GL \_</span><span class="sxs-lookup"><span data-stu-id="adbbf-127">GL\_LIGHTING\_BIT</span></span>         | <span data-ttu-id="adbbf-128">éclairage</span><span class="sxs-lookup"><span data-stu-id="adbbf-128">lighting</span></span>        |
| <span data-ttu-id="adbbf-129">\_bit de ligne GL \_</span><span class="sxs-lookup"><span data-stu-id="adbbf-129">GL\_LINE\_BIT</span></span>             | <span data-ttu-id="adbbf-130">line</span><span class="sxs-lookup"><span data-stu-id="adbbf-130">line</span></span>            |
| <span data-ttu-id="adbbf-131">\_bit de liste GL \_</span><span class="sxs-lookup"><span data-stu-id="adbbf-131">GL\_LIST\_BIT</span></span>             | <span data-ttu-id="adbbf-132">list</span><span class="sxs-lookup"><span data-stu-id="adbbf-132">list</span></span>            |
| <span data-ttu-id="adbbf-133">\_bit du \_ mode de pixel GL \_</span><span class="sxs-lookup"><span data-stu-id="adbbf-133">GL\_PIXEL\_MODE\_BIT</span></span>      | <span data-ttu-id="adbbf-134">pixel</span><span class="sxs-lookup"><span data-stu-id="adbbf-134">pixel</span></span>           |
| <span data-ttu-id="adbbf-135">\_bit de point GL \_</span><span class="sxs-lookup"><span data-stu-id="adbbf-135">GL\_POINT\_BIT</span></span>            | <span data-ttu-id="adbbf-136">point</span><span class="sxs-lookup"><span data-stu-id="adbbf-136">point</span></span>           |
| <span data-ttu-id="adbbf-137">\_bit de polygone GL \_</span><span class="sxs-lookup"><span data-stu-id="adbbf-137">GL\_POLYGON\_BIT</span></span>          | <span data-ttu-id="adbbf-138">polygon</span><span class="sxs-lookup"><span data-stu-id="adbbf-138">polygon</span></span>         |
| <span data-ttu-id="adbbf-139">\_STIPPLE- \_ \_ bit de polygone de GL</span><span class="sxs-lookup"><span data-stu-id="adbbf-139">GL\_POLYGON\_STIPPLE\_BIT</span></span> | <span data-ttu-id="adbbf-140">Polygon-stipple</span><span class="sxs-lookup"><span data-stu-id="adbbf-140">polygon-stipple</span></span> |
| <span data-ttu-id="adbbf-141">\_bit de ciseaux de GL \_</span><span class="sxs-lookup"><span data-stu-id="adbbf-141">GL\_SCISSOR\_BIT</span></span>          | <span data-ttu-id="adbbf-142">ciseaux</span><span class="sxs-lookup"><span data-stu-id="adbbf-142">scissor</span></span>         |
| <span data-ttu-id="adbbf-143">\_bit de \_ tampon de stencil du GL \_</span><span class="sxs-lookup"><span data-stu-id="adbbf-143">GL\_STENCIL\_BUFFER\_BIT</span></span>  | <span data-ttu-id="adbbf-144">stencil-tampon</span><span class="sxs-lookup"><span data-stu-id="adbbf-144">stencil-buffer</span></span>  |
| <span data-ttu-id="adbbf-145">\_bit de texture GL \_</span><span class="sxs-lookup"><span data-stu-id="adbbf-145">GL\_TEXTURE\_BIT</span></span>          | <span data-ttu-id="adbbf-146">texture</span><span class="sxs-lookup"><span data-stu-id="adbbf-146">texture</span></span>         |
| <span data-ttu-id="adbbf-147">\_bit de transformation GL \_</span><span class="sxs-lookup"><span data-stu-id="adbbf-147">GL\_TRANSFORM\_BIT</span></span>        | <span data-ttu-id="adbbf-148">transformation</span><span class="sxs-lookup"><span data-stu-id="adbbf-148">transform</span></span>       |
| <span data-ttu-id="adbbf-149">\_bit de fenêtre d’affichage GL \_</span><span class="sxs-lookup"><span data-stu-id="adbbf-149">GL\_VIEWPORT\_BIT</span></span>         | <span data-ttu-id="adbbf-150">fenêtre d'affichage</span><span class="sxs-lookup"><span data-stu-id="adbbf-150">viewport</span></span>        |



 

 

 




