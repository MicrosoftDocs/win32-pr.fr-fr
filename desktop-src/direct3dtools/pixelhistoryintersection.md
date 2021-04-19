---
description: Représente des informations sur un particulier.
MS-HAID: vspixengine.PixelHistoryIntersection
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: PixelHistoryIntersection, structure
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: D67A116D-B1D0-4E88-A2FF-611CDF4003B2
api_name:
- PixelHistoryIntersection
api_type:
- HeaderDef
api_location:
- vspixengine.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 735adc5396551a18b5e2e2dfba781b358289475e
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/06/2021
ms.locfileid: "106513295"
---
# <a name="span-idvspixenginepixelhistoryintersectionspanpixelhistoryintersection-structure"></a><span data-ttu-id="80f7c-103"><span id="vspixengine.pixelhistoryintersection"></span>PixelHistoryIntersection, structure</span><span class="sxs-lookup"><span data-stu-id="80f7c-103"><span id="vspixengine.pixelhistoryintersection"></span>PixelHistoryIntersection structure</span></span>

<span data-ttu-id="80f7c-104">Représente des informations sur un</span><span class="sxs-lookup"><span data-stu-id="80f7c-104">Represents information about a particular</span></span>

## <a name="syntax"></a><span data-ttu-id="80f7c-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="80f7c-105">Syntax</span></span>


```C++
} PixelHistoryIntersection;
```

## <a name="members"></a><span data-ttu-id="80f7c-106">Membres</span><span class="sxs-lookup"><span data-stu-id="80f7c-106">Members</span></span>

<span data-ttu-id="80f7c-107">**frameNumber**</span><span class="sxs-lookup"><span data-stu-id="80f7c-107">**frameNumber**</span></span>  
<span data-ttu-id="80f7c-108">Frame de l’événement Graphics dans avec cette opération.</span><span class="sxs-lookup"><span data-stu-id="80f7c-108">The frame of the graphics event assocaited with this operation.</span></span>

<span data-ttu-id="80f7c-109">**Numéro**</span><span class="sxs-lookup"><span data-stu-id="80f7c-109">**eid**</span></span>  
<span data-ttu-id="80f7c-110">ID de l’événement graphique associé à cette opération.</span><span class="sxs-lookup"><span data-stu-id="80f7c-110">The ID of the graphics event associated with this operation.</span></span>

<span data-ttu-id="80f7c-111">**renderTargetPtr**</span><span class="sxs-lookup"><span data-stu-id="80f7c-111">**renderTargetPtr**</span></span>  
<span data-ttu-id="80f7c-112">Cible de rendu associée à l’origine (à l’intérieur de l’application capturée) avec cette opération.</span><span class="sxs-lookup"><span data-stu-id="80f7c-112">The render target originally associated (inside the captured application) with this operation.</span></span>

<span data-ttu-id="80f7c-113">**eventType**</span><span class="sxs-lookup"><span data-stu-id="80f7c-113">**eventType**</span></span>  
<span data-ttu-id="80f7c-114">Type d’événement associé à cette opération (en particulier, si cet événement est un appel de dessin).</span><span class="sxs-lookup"><span data-stu-id="80f7c-114">The kind of event associated with this operation (specifically, whether this event is a draw call).</span></span>

<span data-ttu-id="80f7c-115">**point**</span><span class="sxs-lookup"><span data-stu-id="80f7c-115">**point**</span></span>  
<span data-ttu-id="80f7c-116">Coordonnées du pixel dans le trame.</span><span class="sxs-lookup"><span data-stu-id="80f7c-116">The coordinates of the pixel in the framebuffer.</span></span>

<span data-ttu-id="80f7c-117">**bAssemblerStageGeneratesInstanceID**</span><span class="sxs-lookup"><span data-stu-id="80f7c-117">**bAssemblerStageGeneratesInstanceID**</span></span>  
<span data-ttu-id="80f7c-118">true si l’assembleur d’entrée génère des ID d’instance ; Sinon, false.</span><span class="sxs-lookup"><span data-stu-id="80f7c-118">true if the input assembler generates instance IDs; otherwise false.</span></span>

<span data-ttu-id="80f7c-119">**flags**</span><span class="sxs-lookup"><span data-stu-id="80f7c-119">**flags**</span></span>  
<span data-ttu-id="80f7c-120">Combinaison de valeurs PIXELHISTORYFLAGS.</span><span class="sxs-lookup"><span data-stu-id="80f7c-120">A combination of PIXELHISTORYFLAGS values.</span></span> <span data-ttu-id="80f7c-121">Pour plus d’informations, consultez l’énumération PIXELHISTORYFLAGS.</span><span class="sxs-lookup"><span data-stu-id="80f7c-121">For more information, see the PIXELHISTORYFLAGS enumeration.</span></span>

<span data-ttu-id="80f7c-122">**fbInitialRed**</span><span class="sxs-lookup"><span data-stu-id="80f7c-122">**fbInitialRed**</span></span>  
<span data-ttu-id="80f7c-123">Trame : valeur du composant de couleur rouge de trame avant la fusion de toute sortie de nuanceur de pixels. autrement dit, au début de ce frame.</span><span class="sxs-lookup"><span data-stu-id="80f7c-123">Framebuffer: value of red color component of framebuffer before any pixel shader output is merged; that is, at the beginning of this frame.</span></span>

<span data-ttu-id="80f7c-124">**fbInitialGreen**</span><span class="sxs-lookup"><span data-stu-id="80f7c-124">**fbInitialGreen**</span></span>  
<span data-ttu-id="80f7c-125">Trame : valeur du composant de couleur verte de trame avant la fusion de toute sortie de nuanceur de pixels. autrement dit, au début de ce frame.</span><span class="sxs-lookup"><span data-stu-id="80f7c-125">Framebuffer: value of green color component of framebuffer before any pixel shader output is merged; that is, at the beginning of this frame.</span></span>

<span data-ttu-id="80f7c-126">**fbInitialBlue**</span><span class="sxs-lookup"><span data-stu-id="80f7c-126">**fbInitialBlue**</span></span>  
<span data-ttu-id="80f7c-127">Trame : valeur du composant de couleur bleu de trame avant la fusion de toute sortie de nuanceur de pixels. autrement dit, au début de ce frame.</span><span class="sxs-lookup"><span data-stu-id="80f7c-127">Framebuffer: value of blue color component of framebuffer before any pixel shader output is merged; that is, at the beginning of this frame.</span></span>

<span data-ttu-id="80f7c-128">**fbInitialAlpha**</span><span class="sxs-lookup"><span data-stu-id="80f7c-128">**fbInitialAlpha**</span></span>  
<span data-ttu-id="80f7c-129">Trame : valeur du composant de couleur alpha de trame avant la fusion de toute sortie de nuanceur de pixels. autrement dit, au début de ce frame.</span><span class="sxs-lookup"><span data-stu-id="80f7c-129">Framebuffer: value of alpha color component of framebuffer before any pixel shader output is merged; that is, at the beginning of this frame.</span></span>

<span data-ttu-id="80f7c-130">**LabelFBInitialRed**</span><span class="sxs-lookup"><span data-stu-id="80f7c-130">**LabelFBInitialRed**</span></span>  
<span data-ttu-id="80f7c-131">Chaîne COM contenant le nom de l’étiquette associée au composant de couleur rouge du trame avant tout ombrage de pixel ; autrement dit, au début de ce frame.</span><span class="sxs-lookup"><span data-stu-id="80f7c-131">A COM string containing the name of the label associated with the red color component of the framebuffer before any pixel shading; that is, at the beginning of this frame.</span></span>

<span data-ttu-id="80f7c-132">**LabelFBInitialGreen**</span><span class="sxs-lookup"><span data-stu-id="80f7c-132">**LabelFBInitialGreen**</span></span>  
<span data-ttu-id="80f7c-133">Chaîne COM contenant le nom de l’étiquette associée au composant de couleur verte du trame avant tout ombrage de pixel ; autrement dit, au début de ce frame.</span><span class="sxs-lookup"><span data-stu-id="80f7c-133">A COM string containing the name of the label associated with the green color component of the framebuffer before any pixel shading; that is, at the beginning of this frame.</span></span>

<span data-ttu-id="80f7c-134">**LabelFBInitialBlue**</span><span class="sxs-lookup"><span data-stu-id="80f7c-134">**LabelFBInitialBlue**</span></span>  
<span data-ttu-id="80f7c-135">Chaîne COM contenant le nom de l’étiquette associée au composant de couleur bleu du trame avant tout ombrage de pixel ; autrement dit, au début de ce frame.</span><span class="sxs-lookup"><span data-stu-id="80f7c-135">A COM string containing the name of the label associated with the blue color component of the framebuffer before any pixel shading; that is, at the beginning of this frame.</span></span>

<span data-ttu-id="80f7c-136">**LabelFBInitialAlpha**</span><span class="sxs-lookup"><span data-stu-id="80f7c-136">**LabelFBInitialAlpha**</span></span>  
<span data-ttu-id="80f7c-137">Chaîne COM contenant le nom de l’étiquette associée au composant de couleur alpha du trame avant tout ombrage de pixel ; autrement dit, au début de ce frame.</span><span class="sxs-lookup"><span data-stu-id="80f7c-137">A COM string containing the name of the label associated with the alpha color component of the framebuffer before any pixel shading; that is, at the beginning of this frame.</span></span>

<span data-ttu-id="80f7c-138">**fbRed**</span><span class="sxs-lookup"><span data-stu-id="80f7c-138">**fbRed**</span></span>  
<span data-ttu-id="80f7c-139">Trame : valeur du composant de couleur rouge de trame une fois que toutes les sorties de nuanceur de pixels ont été fusionnées ; autrement dit, la couleur trame finale.</span><span class="sxs-lookup"><span data-stu-id="80f7c-139">Framebuffer: value of red color component of framebuffer after all pixel shader output is merged; that is, the final framebuffer color.</span></span>

<span data-ttu-id="80f7c-140">**fbGreen**</span><span class="sxs-lookup"><span data-stu-id="80f7c-140">**fbGreen**</span></span>  
<span data-ttu-id="80f7c-141">Trame : valeur du composant de couleur verte de trame une fois que toutes les sorties de nuanceur de pixels ont été fusionnées ; autrement dit, la couleur trame finale.</span><span class="sxs-lookup"><span data-stu-id="80f7c-141">Framebuffer: value of green color component of framebuffer after all pixel shader output is merged; that is, the final framebuffer color.</span></span>

<span data-ttu-id="80f7c-142">**fbBlue**</span><span class="sxs-lookup"><span data-stu-id="80f7c-142">**fbBlue**</span></span>  
<span data-ttu-id="80f7c-143">Trame : valeur du composant de couleur bleu de trame une fois que toutes les sorties de nuanceur de pixels ont été fusionnées ; autrement dit, la couleur trame finale.</span><span class="sxs-lookup"><span data-stu-id="80f7c-143">Framebuffer: value of blue color component of framebuffer after all pixel shader output is merged; that is, the final framebuffer color.</span></span>

<span data-ttu-id="80f7c-144">**fbAlpha**</span><span class="sxs-lookup"><span data-stu-id="80f7c-144">**fbAlpha**</span></span>  
<span data-ttu-id="80f7c-145">Trame : valeur du composant de couleur alpha de trame une fois que toutes les sorties de nuanceur de pixels ont été fusionnées ; autrement dit, la couleur trame finale.</span><span class="sxs-lookup"><span data-stu-id="80f7c-145">Framebuffer: value of alpha color component of framebuffer after all pixel shader output is merged; that is, the final framebuffer color.</span></span>

<span data-ttu-id="80f7c-146">**LabelFBRed**</span><span class="sxs-lookup"><span data-stu-id="80f7c-146">**LabelFBRed**</span></span>  
<span data-ttu-id="80f7c-147">Chaîne COM contenant le nom de l’étiquette associée au composant de couleur rouge du trame après l’ombrage des pixels ; autrement dit, la couleur trame finale.</span><span class="sxs-lookup"><span data-stu-id="80f7c-147">A COM string containing the name of the label associated with the red color component of the framebuffer after all pixel shading; that is, the final framebuffer color.</span></span>

<span data-ttu-id="80f7c-148">**LabelFBGreen**</span><span class="sxs-lookup"><span data-stu-id="80f7c-148">**LabelFBGreen**</span></span>  
<span data-ttu-id="80f7c-149">Chaîne COM contenant le nom de l’étiquette associée au composant de couleur verte du trame après tout l’ombrage de pixel. autrement dit, la couleur trame finale.</span><span class="sxs-lookup"><span data-stu-id="80f7c-149">A COM string containing the name of the label associated with the green color component of the framebuffer after all pixel shading; that is, the final framebuffer color.</span></span>

<span data-ttu-id="80f7c-150">**LabelFBBlue**</span><span class="sxs-lookup"><span data-stu-id="80f7c-150">**LabelFBBlue**</span></span>  
<span data-ttu-id="80f7c-151">Chaîne COM contenant le nom de l’étiquette associée au composant de couleur bleu du trame après l’ombrage des pixels ; autrement dit, la couleur trame finale.</span><span class="sxs-lookup"><span data-stu-id="80f7c-151">A COM string containing the name of the label associated with the blue color component of the framebuffer after all pixel shading; that is, the final framebuffer color.</span></span>

<span data-ttu-id="80f7c-152">**LabelFBAlpha**</span><span class="sxs-lookup"><span data-stu-id="80f7c-152">**LabelFBAlpha**</span></span>  
<span data-ttu-id="80f7c-153">Chaîne COM contenant le nom de l’étiquette associée au composant de couleur alpha du trame après tout l’ombrage de pixel. autrement dit, la couleur trame finale.</span><span class="sxs-lookup"><span data-stu-id="80f7c-153">A COM string containing the name of the label associated with the alpha color component of the framebuffer after all pixel shading; that is, the final framebuffer color.</span></span>

<span data-ttu-id="80f7c-154">**pixelKillReason**</span><span class="sxs-lookup"><span data-stu-id="80f7c-154">**pixelKillReason**</span></span>  
<span data-ttu-id="80f7c-155">Spécifie la raison pour laquelle la contribution de couleur du pixel a été supprimée.</span><span class="sxs-lookup"><span data-stu-id="80f7c-155">Specifies the reason that the pixel's color contribution was killed.</span></span>

<span data-ttu-id="80f7c-156">**HResult**</span><span class="sxs-lookup"><span data-stu-id="80f7c-156">**HResult**</span></span>  
<span data-ttu-id="80f7c-157">Si une erreur s’est produite, contient la valeur HRESULT de DirectX qui spécifie l’erreur.</span><span class="sxs-lookup"><span data-stu-id="80f7c-157">If an error occurred, contains the DirectX HRESULT that specifies the error.</span></span>

## <a name="requirements"></a><span data-ttu-id="80f7c-158">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="80f7c-158">Requirements</span></span>

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><tbody><tr class="odd"><td><p><span data-ttu-id="80f7c-159">En-tête</span><span class="sxs-lookup"><span data-stu-id="80f7c-159">Header</span></span></p></td><td><span data-ttu-id="80f7c-160">Vspixengine. h</span><span class="sxs-lookup"><span data-stu-id="80f7c-160">Vspixengine.h</span></span></td></tr></tbody></table>

 

 



