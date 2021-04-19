---
description: Représente des informations sur l’historique des pixels.
MS-HAID: vspixengine.PixelHistoryOperation
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: PixelHistoryOperation, structure
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 59DC72FC-3865-48D3-9F92-9BE93DCA093B
api_name:
- PixelHistoryOperation
api_type:
- HeaderDef
api_location:
- vspixengine.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: c02a6725f588aaa4c7d72c48d03d921503d4e6a6
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/06/2021
ms.locfileid: "106517380"
---
# <a name="span-idvspixenginepixelhistoryoperationspanpixelhistoryoperation-structure"></a><span data-ttu-id="5ca2d-103"><span id="vspixengine.pixelhistoryoperation"></span>PixelHistoryOperation, structure</span><span class="sxs-lookup"><span data-stu-id="5ca2d-103"><span id="vspixengine.pixelhistoryoperation"></span>PixelHistoryOperation structure</span></span>

<span data-ttu-id="5ca2d-104">Représente des informations sur l’historique des pixels.</span><span class="sxs-lookup"><span data-stu-id="5ca2d-104">Represents information about pixel history.</span></span>

## <a name="syntax"></a><span data-ttu-id="5ca2d-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="5ca2d-105">Syntax</span></span>


```C++
} PixelHistoryOperation;
```

## <a name="members"></a><span data-ttu-id="5ca2d-106">Membres</span><span class="sxs-lookup"><span data-stu-id="5ca2d-106">Members</span></span>

<span data-ttu-id="5ca2d-107">**Numéro**</span><span class="sxs-lookup"><span data-stu-id="5ca2d-107">**eid**</span></span>  
<span data-ttu-id="5ca2d-108">ID de l’événement graphique associé à cette opération.</span><span class="sxs-lookup"><span data-stu-id="5ca2d-108">The ID of the graphics event associated with this operation.</span></span>

<span data-ttu-id="5ca2d-109">**PCP**</span><span class="sxs-lookup"><span data-stu-id="5ca2d-109">**PCP**</span></span>  
<span data-ttu-id="5ca2d-110">Appels empaquetés associés à cette opération.</span><span class="sxs-lookup"><span data-stu-id="5ca2d-110">Packed calls associated with this operation.</span></span>

<span data-ttu-id="5ca2d-111">**renderTargetPtr**</span><span class="sxs-lookup"><span data-stu-id="5ca2d-111">**renderTargetPtr**</span></span>  
<span data-ttu-id="5ca2d-112">Cible de rendu associée à l’origine (à l’intérieur de l’application capturée) avec cette opération.</span><span class="sxs-lookup"><span data-stu-id="5ca2d-112">The render target originally associated (inside the captured application) with this operation.</span></span>

<span data-ttu-id="5ca2d-113">**iPrim**</span><span class="sxs-lookup"><span data-stu-id="5ca2d-113">**iPrim**</span></span>  
<span data-ttu-id="5ca2d-114">Index de la primitive réelle associée à son opération.</span><span class="sxs-lookup"><span data-stu-id="5ca2d-114">The index of the actual primitive associated witht his operation.</span></span>

<span data-ttu-id="5ca2d-115">**numPrims**</span><span class="sxs-lookup"><span data-stu-id="5ca2d-115">**numPrims**</span></span>  
<span data-ttu-id="5ca2d-116">Nombre total de primitives associées à cette opération.</span><span class="sxs-lookup"><span data-stu-id="5ca2d-116">The total number of primitives associated with this operation.</span></span>

<span data-ttu-id="5ca2d-117">**numVertsPerPrim**</span><span class="sxs-lookup"><span data-stu-id="5ca2d-117">**numVertsPerPrim**</span></span>  
<span data-ttu-id="5ca2d-118">Nombre de vertex par primitive.</span><span class="sxs-lookup"><span data-stu-id="5ca2d-118">The number of vertices per primitive.</span></span>

<span data-ttu-id="5ca2d-119">**iInstance**</span><span class="sxs-lookup"><span data-stu-id="5ca2d-119">**iInstance**</span></span>  
<span data-ttu-id="5ca2d-120">Lors du rendu des instances, le numéro d’instance de l’instance réelle associée à cette opération.</span><span class="sxs-lookup"><span data-stu-id="5ca2d-120">When rendering instances, the instance number of the actual instance associated with this operation.</span></span>

<span data-ttu-id="5ca2d-121">**iInstanceCount**</span><span class="sxs-lookup"><span data-stu-id="5ca2d-121">**iInstanceCount**</span></span>  
<span data-ttu-id="5ca2d-122">Lors du rendu des instances, nombre total d’instances associées à cette opération.</span><span class="sxs-lookup"><span data-stu-id="5ca2d-122">When rendering instances, the total number of instances associated with this operation.</span></span>

<span data-ttu-id="5ca2d-123">**bAssemblerStageGeneratesInstanceID**</span><span class="sxs-lookup"><span data-stu-id="5ca2d-123">**bAssemblerStageGeneratesInstanceID**</span></span>  
<span data-ttu-id="5ca2d-124">true si l’assembleur d’entrée génère des ID d’instance ; Sinon, false.</span><span class="sxs-lookup"><span data-stu-id="5ca2d-124">true if the input assembler generates instance IDs; otherwise false.</span></span>

<span data-ttu-id="5ca2d-125">**flags**</span><span class="sxs-lookup"><span data-stu-id="5ca2d-125">**flags**</span></span>  
<span data-ttu-id="5ca2d-126">Combinaison de valeurs PIXELHISTORYFLAGS.</span><span class="sxs-lookup"><span data-stu-id="5ca2d-126">A combination of PIXELHISTORYFLAGS values.</span></span> <span data-ttu-id="5ca2d-127">Pour plus d’informations, consultez l’énumération PIXELHISTORYFLAGS.</span><span class="sxs-lookup"><span data-stu-id="5ca2d-127">For more information, see the PIXELHISTORYFLAGS enumeration.</span></span>

<span data-ttu-id="5ca2d-128">**pVSFile**</span><span class="sxs-lookup"><span data-stu-id="5ca2d-128">**pVSFile**</span></span>  
<span data-ttu-id="5ca2d-129">FILEPTR pour le flux d’octets du nuanceur de pixels.</span><span class="sxs-lookup"><span data-stu-id="5ca2d-129">A FILEPTR for the pixel shader byte stream.</span></span> <span data-ttu-id="5ca2d-130">Cette valeur est retournée pour déboguer.</span><span class="sxs-lookup"><span data-stu-id="5ca2d-130">This is passed back in order to debug.</span></span>

<span data-ttu-id="5ca2d-131">**pGSFile**</span><span class="sxs-lookup"><span data-stu-id="5ca2d-131">**pGSFile**</span></span>  
<span data-ttu-id="5ca2d-132">FILEPTR pour le flux d’octets du nuanceur Geometry.</span><span class="sxs-lookup"><span data-stu-id="5ca2d-132">A FILEPTR for the geometry shader byte stream.</span></span> <span data-ttu-id="5ca2d-133">Cette valeur est retournée pour déboguer.</span><span class="sxs-lookup"><span data-stu-id="5ca2d-133">This is passed back in order to debug.</span></span>

<span data-ttu-id="5ca2d-134">**pPSFile**</span><span class="sxs-lookup"><span data-stu-id="5ca2d-134">**pPSFile**</span></span>  
<span data-ttu-id="5ca2d-135">FILEPTR pour le flux d’octets du nuanceur de pixels.</span><span class="sxs-lookup"><span data-stu-id="5ca2d-135">A FILEPTR for the pixel shader byte stream.</span></span> <span data-ttu-id="5ca2d-136">Cette valeur est retournée pour déboguer.</span><span class="sxs-lookup"><span data-stu-id="5ca2d-136">This is passed back in order to debug.</span></span>

<span data-ttu-id="5ca2d-137">**pHSFile**</span><span class="sxs-lookup"><span data-stu-id="5ca2d-137">**pHSFile**</span></span>  
<span data-ttu-id="5ca2d-138">FILEPTR pour le flux d’octets du nuanceur de coque.</span><span class="sxs-lookup"><span data-stu-id="5ca2d-138">A FILEPTR for the hull shader byte stream.</span></span> <span data-ttu-id="5ca2d-139">Cette valeur est retournée pour déboguer.</span><span class="sxs-lookup"><span data-stu-id="5ca2d-139">This is passed back in order to debug.</span></span>

<span data-ttu-id="5ca2d-140">**pDSFile**</span><span class="sxs-lookup"><span data-stu-id="5ca2d-140">**pDSFile**</span></span>  
<span data-ttu-id="5ca2d-141">FILEPTR pour le flux d’octets du nuanceur de domaine.</span><span class="sxs-lookup"><span data-stu-id="5ca2d-141">A FILEPTR for the domain shader byte stream.</span></span> <span data-ttu-id="5ca2d-142">Cette valeur est retournée pour déboguer.</span><span class="sxs-lookup"><span data-stu-id="5ca2d-142">This is passed back in order to debug.</span></span>

<span data-ttu-id="5ca2d-143">**pCSFile**</span><span class="sxs-lookup"><span data-stu-id="5ca2d-143">**pCSFile**</span></span>  
<span data-ttu-id="5ca2d-144">FILEPTR pour le flux d’octets du nuanceur de calcul.</span><span class="sxs-lookup"><span data-stu-id="5ca2d-144">A FILEPTR for the compute shader byte stream.</span></span> <span data-ttu-id="5ca2d-145">Cette valeur est retournée pour déboguer.</span><span class="sxs-lookup"><span data-stu-id="5ca2d-145">This is passed back in order to debug.</span></span>

<span data-ttu-id="5ca2d-146">**VertexShaderFile**</span><span class="sxs-lookup"><span data-stu-id="5ca2d-146">**VertexShaderFile**</span></span>  
<span data-ttu-id="5ca2d-147">Chaîne COM contenant le chemin d’accès du fichier source du nuanceur de sommets.</span><span class="sxs-lookup"><span data-stu-id="5ca2d-147">A COM string containing the filepath of the vertex shader source file.</span></span>

<span data-ttu-id="5ca2d-148">**PixelShaderFile**</span><span class="sxs-lookup"><span data-stu-id="5ca2d-148">**PixelShaderFile**</span></span>  
<span data-ttu-id="5ca2d-149">Chaîne COM contenant le chemin d’accès du fichier source du nuanceur de pixels.</span><span class="sxs-lookup"><span data-stu-id="5ca2d-149">A COM string containing the filepath of the pixel shader source file.</span></span>

<span data-ttu-id="5ca2d-150">**GeometryShaderFile**</span><span class="sxs-lookup"><span data-stu-id="5ca2d-150">**GeometryShaderFile**</span></span>  
<span data-ttu-id="5ca2d-151">Chaîne COM contenant le chemin d’accès du fichier source du nuanceur Geometry.</span><span class="sxs-lookup"><span data-stu-id="5ca2d-151">A COM string containing the filepath of the geometry shader source file.</span></span>

<span data-ttu-id="5ca2d-152">**HullShaderFile**</span><span class="sxs-lookup"><span data-stu-id="5ca2d-152">**HullShaderFile**</span></span>  
<span data-ttu-id="5ca2d-153">Chaîne COM contenant le chemin d’accès du fichier source du nuanceur de coque.</span><span class="sxs-lookup"><span data-stu-id="5ca2d-153">A COM string containing the filepath of the hull shader source file.</span></span>

<span data-ttu-id="5ca2d-154">**DomainShaderFile**</span><span class="sxs-lookup"><span data-stu-id="5ca2d-154">**DomainShaderFile**</span></span>  
<span data-ttu-id="5ca2d-155">Chaîne COM contenant le chemin d’accès du fichier source du nuanceur de domaine.</span><span class="sxs-lookup"><span data-stu-id="5ca2d-155">A COM string containing the filepath of the domain shader source file.</span></span>

<span data-ttu-id="5ca2d-156">**psRed**</span><span class="sxs-lookup"><span data-stu-id="5ca2d-156">**psRed**</span></span>  
<span data-ttu-id="5ca2d-157">Sortie du nuanceur de pixels : valeur du composant de couleur rouge.</span><span class="sxs-lookup"><span data-stu-id="5ca2d-157">Pixel shader output: value of red color component.</span></span>

<span data-ttu-id="5ca2d-158">**psGreen**</span><span class="sxs-lookup"><span data-stu-id="5ca2d-158">**psGreen**</span></span>  
<span data-ttu-id="5ca2d-159">Sortie du nuanceur de pixels : valeur du composant de couleur verte.</span><span class="sxs-lookup"><span data-stu-id="5ca2d-159">Pixel shader output: value of green color component.</span></span>

<span data-ttu-id="5ca2d-160">**psBlue**</span><span class="sxs-lookup"><span data-stu-id="5ca2d-160">**psBlue**</span></span>  
<span data-ttu-id="5ca2d-161">Sortie du nuanceur de pixels : valeur du composant de couleur bleu</span><span class="sxs-lookup"><span data-stu-id="5ca2d-161">Pixel shader output: value of blue color component</span></span>

<span data-ttu-id="5ca2d-162">**psAlpha**</span><span class="sxs-lookup"><span data-stu-id="5ca2d-162">**psAlpha**</span></span>  
<span data-ttu-id="5ca2d-163">Sortie du nuanceur de pixels : valeur du composant de couleur alpha</span><span class="sxs-lookup"><span data-stu-id="5ca2d-163">Pixel shader output: value of alpha color component</span></span>

<span data-ttu-id="5ca2d-164">**LabelPSRed**</span><span class="sxs-lookup"><span data-stu-id="5ca2d-164">**LabelPSRed**</span></span>  
<span data-ttu-id="5ca2d-165">Chaîne COM contenant le nom de l’étiquette associée au composant de couleur rouge de la sortie du nuanceur de pixels.</span><span class="sxs-lookup"><span data-stu-id="5ca2d-165">A COM string containing the name of the label associated with the red color component of the pixel shader output.</span></span>

<span data-ttu-id="5ca2d-166">**LabelPSGreen**</span><span class="sxs-lookup"><span data-stu-id="5ca2d-166">**LabelPSGreen**</span></span>  
<span data-ttu-id="5ca2d-167">Chaîne COM contenant le nom de l’étiquette associée au composant de couleur verte de la sortie du nuanceur de pixels.</span><span class="sxs-lookup"><span data-stu-id="5ca2d-167">A COM string containing the name of the label associated with the green color component of the pixel shader output.</span></span>

<span data-ttu-id="5ca2d-168">**LabelPSBlue**</span><span class="sxs-lookup"><span data-stu-id="5ca2d-168">**LabelPSBlue**</span></span>  
<span data-ttu-id="5ca2d-169">Chaîne COM contenant le nom de l’étiquette associée au composant de couleur bleu de la sortie du nuanceur de pixels.</span><span class="sxs-lookup"><span data-stu-id="5ca2d-169">A COM string containing the name of the label associated with the blue color component of the pixel shader output.</span></span>

<span data-ttu-id="5ca2d-170">**LabelPSAlpha**</span><span class="sxs-lookup"><span data-stu-id="5ca2d-170">**LabelPSAlpha**</span></span>  
<span data-ttu-id="5ca2d-171">Chaîne COM contenant le nom de l’étiquette associée au composant de couleur alpha de la sortie du nuanceur de pixels.</span><span class="sxs-lookup"><span data-stu-id="5ca2d-171">A COM string containing the name of the label associated with the alpha color component of the pixel shader output.</span></span>

<span data-ttu-id="5ca2d-172">**pixelKillReason**</span><span class="sxs-lookup"><span data-stu-id="5ca2d-172">**pixelKillReason**</span></span>  
<span data-ttu-id="5ca2d-173">Sortie du nuanceur de pixels : raison pour laquelle la sortie de pixel a été arrêtée.</span><span class="sxs-lookup"><span data-stu-id="5ca2d-173">Pixel shader output: reason the pixel output was killed.</span></span>

<span data-ttu-id="5ca2d-174">**pixelOccluded**</span><span class="sxs-lookup"><span data-stu-id="5ca2d-174">**pixelOccluded**</span></span>  
<span data-ttu-id="5ca2d-175">true si le pixel est bloqués ; Sinon, false.</span><span class="sxs-lookup"><span data-stu-id="5ca2d-175">true if the pixel is occluded; otherwise, false.</span></span>

<span data-ttu-id="5ca2d-176">**fbRed**</span><span class="sxs-lookup"><span data-stu-id="5ca2d-176">**fbRed**</span></span>  
<span data-ttu-id="5ca2d-177">Trame : la valeur du composant de couleur rouge de trame avant la sortie du nuanceur de pixels est fusionnée.</span><span class="sxs-lookup"><span data-stu-id="5ca2d-177">Framebuffer: value of red color component of framebuffer before pixel shader output is merged.</span></span>

<span data-ttu-id="5ca2d-178">**fbGreen**</span><span class="sxs-lookup"><span data-stu-id="5ca2d-178">**fbGreen**</span></span>  
<span data-ttu-id="5ca2d-179">Trame : la valeur du composant de couleur verte de trame avant la sortie du nuanceur de pixels est fusionnée.</span><span class="sxs-lookup"><span data-stu-id="5ca2d-179">Framebuffer: value of green color component of framebuffer before pixel shader output is merged.</span></span>

<span data-ttu-id="5ca2d-180">**fbBlue**</span><span class="sxs-lookup"><span data-stu-id="5ca2d-180">**fbBlue**</span></span>  
<span data-ttu-id="5ca2d-181">Trame : la valeur du composant de couleur bleu de trame avant la sortie du nuanceur de pixels est fusionnée.</span><span class="sxs-lookup"><span data-stu-id="5ca2d-181">Framebuffer: value of blue color component of framebuffer before pixel shader output is merged.</span></span>

<span data-ttu-id="5ca2d-182">**fbAlpha**</span><span class="sxs-lookup"><span data-stu-id="5ca2d-182">**fbAlpha**</span></span>  
<span data-ttu-id="5ca2d-183">Trame : la valeur du composant de couleur alpha de trame avant la sortie du nuanceur de pixels est fusionnée.</span><span class="sxs-lookup"><span data-stu-id="5ca2d-183">Framebuffer: value of alpha color component of framebuffer before pixel shader output is merged.</span></span>

<span data-ttu-id="5ca2d-184">**LabelFBRed**</span><span class="sxs-lookup"><span data-stu-id="5ca2d-184">**LabelFBRed**</span></span>  
<span data-ttu-id="5ca2d-185">Chaîne COM contenant le nom de l’étiquette associée au composant de couleur rouge du trame.</span><span class="sxs-lookup"><span data-stu-id="5ca2d-185">A COM string containing the name of the label associated with the red color component of the framebuffer.</span></span>

<span data-ttu-id="5ca2d-186">**LabelFBGreen**</span><span class="sxs-lookup"><span data-stu-id="5ca2d-186">**LabelFBGreen**</span></span>  
<span data-ttu-id="5ca2d-187">Chaîne COM contenant le nom de l’étiquette associée au composant de couleur verte du trame.</span><span class="sxs-lookup"><span data-stu-id="5ca2d-187">A COM string containing the name of the label associated with the green color component of the framebuffer.</span></span>

<span data-ttu-id="5ca2d-188">**LabelFBBlue**</span><span class="sxs-lookup"><span data-stu-id="5ca2d-188">**LabelFBBlue**</span></span>  
<span data-ttu-id="5ca2d-189">Chaîne COM contenant le nom de l’étiquette associée au composant de couleur bleu du trame.</span><span class="sxs-lookup"><span data-stu-id="5ca2d-189">A COM string containing the name of the label associated with the blue color component of the framebuffer.</span></span>

<span data-ttu-id="5ca2d-190">**LabelFBAlpha**</span><span class="sxs-lookup"><span data-stu-id="5ca2d-190">**LabelFBAlpha**</span></span>  
<span data-ttu-id="5ca2d-191">Chaîne COM contenant le nom de l’étiquette associée au composant de couleur alpha du trame.</span><span class="sxs-lookup"><span data-stu-id="5ca2d-191">A COM string containing the name of the label associated with the alpha color component of the framebuffer.</span></span>

<span data-ttu-id="5ca2d-192">**topologie**</span><span class="sxs-lookup"><span data-stu-id="5ca2d-192">**topology**</span></span>  
<span data-ttu-id="5ca2d-193">Topologie de vertex des appels de dessin (liste de triangles, bande triangulaire, etc.).</span><span class="sxs-lookup"><span data-stu-id="5ca2d-193">The vertex topology of the draw calls (triangle list, triangle strip, etc).</span></span>

<span data-ttu-id="5ca2d-194">**derniers**</span><span class="sxs-lookup"><span data-stu-id="5ca2d-194">**vertices**</span></span>  
<span data-ttu-id="5ca2d-195">Chaîne COM contenant la mémoire tampon de vertex en commençant à cette primitive.</span><span class="sxs-lookup"><span data-stu-id="5ca2d-195">A COM string containing the vertex buffer starting at this primitive.</span></span> <span data-ttu-id="5ca2d-196">La mémoire tampon de vertex suit le format de disposition d’entrée spécifié dans l’étape de pipeline.</span><span class="sxs-lookup"><span data-stu-id="5ca2d-196">The vertex buffer follows the input layout format specified in the pipeline stage.</span></span>

<span data-ttu-id="5ca2d-197">**vertexSize**</span><span class="sxs-lookup"><span data-stu-id="5ca2d-197">**vertexSize**</span></span>  
<span data-ttu-id="5ca2d-198">Taille d’un seul vertex en octets.</span><span class="sxs-lookup"><span data-stu-id="5ca2d-198">The size of a single vertex in bytes.</span></span>

<span data-ttu-id="5ca2d-199">**InputLayout**</span><span class="sxs-lookup"><span data-stu-id="5ca2d-199">**InputLayout**</span></span>  
<span data-ttu-id="5ca2d-200">Chaîne COM contenant une séquence de structures InputLayoutStruct associées à l’appel de dessin.</span><span class="sxs-lookup"><span data-stu-id="5ca2d-200">A COM string containing a sequence of InputLayoutStruct structures associated with the draw call.</span></span>

<span data-ttu-id="5ca2d-201">**HResult**</span><span class="sxs-lookup"><span data-stu-id="5ca2d-201">**HResult**</span></span>  
<span data-ttu-id="5ca2d-202">HRESULT DirectX.</span><span class="sxs-lookup"><span data-stu-id="5ca2d-202">The DirectX Hresult.</span></span> <span data-ttu-id="5ca2d-203">En cas de problème, vous pouvez l’utiliser pour afficher l’erreur.</span><span class="sxs-lookup"><span data-stu-id="5ca2d-203">In the event of a problem this can be used to display the error.</span></span>

## <a name="requirements"></a><span data-ttu-id="5ca2d-204">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="5ca2d-204">Requirements</span></span>

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><tbody><tr class="odd"><td><p><span data-ttu-id="5ca2d-205">En-tête</span><span class="sxs-lookup"><span data-stu-id="5ca2d-205">Header</span></span></p></td><td><span data-ttu-id="5ca2d-206">Vspixengine. h</span><span class="sxs-lookup"><span data-stu-id="5ca2d-206">Vspixengine.h</span></span></td></tr></tbody></table>

 

 



