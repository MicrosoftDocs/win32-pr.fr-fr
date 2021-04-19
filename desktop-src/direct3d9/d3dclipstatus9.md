---
description: Décrit l’état actuel du clip.
ms.assetid: 3ea8631c-a967-4d24-a49a-1751b3ee6077
title: D3DCLIPSTATUS9, structure (D3D9Types. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DCLIPSTATUS9
api_type:
- HeaderDef
api_location:
- D3D9Types.h
ms.openlocfilehash: 3b22fdfcc136c05ec8fe03ae491612606b2df62f
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "106531325"
---
# <a name="d3dclipstatus9-structure"></a><span data-ttu-id="0f8bb-103">D3DCLIPSTATUS9, structure</span><span class="sxs-lookup"><span data-stu-id="0f8bb-103">D3DCLIPSTATUS9 structure</span></span>

<span data-ttu-id="0f8bb-104">Décrit l’état actuel du clip.</span><span class="sxs-lookup"><span data-stu-id="0f8bb-104">Describes the current clip status.</span></span>

## <a name="syntax"></a><span data-ttu-id="0f8bb-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="0f8bb-105">Syntax</span></span>


```C++
typedef struct D3DCLIPSTATUS9 {
  DWORD ClipUnion;
  DWORD ClipIntersection;
} D3DCLIPSTATUS9, *LPD3DCLIPSTATUS9;
```



## <a name="members"></a><span data-ttu-id="0f8bb-106">Membres</span><span class="sxs-lookup"><span data-stu-id="0f8bb-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="0f8bb-107">**ClipUnion**</span><span class="sxs-lookup"><span data-stu-id="0f8bb-107">**ClipUnion**</span></span>
</dt> <dd>

<span data-ttu-id="0f8bb-108">Type : **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="0f8bb-108">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="0f8bb-109">Découpez les indicateurs d’Union qui décrivent l’état actuel du clip.</span><span class="sxs-lookup"><span data-stu-id="0f8bb-109">Clip union flags that describe the current clip status.</span></span> <span data-ttu-id="0f8bb-110">Ce membre peut être un ou plusieurs des indicateurs suivants :</span><span class="sxs-lookup"><span data-stu-id="0f8bb-110">This member can be one or more of the following flags:</span></span>



| <span data-ttu-id="0f8bb-111">Valeur</span><span class="sxs-lookup"><span data-stu-id="0f8bb-111">Value</span></span>                                                                                                                                                      | <span data-ttu-id="0f8bb-112">Signification</span><span class="sxs-lookup"><span data-stu-id="0f8bb-112">Meaning</span></span>                                                                         |
|------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------|
| <span id="D3DCS_ALL"></span><span id="d3dcs_all"></span><dl> <span data-ttu-id="0f8bb-113"><dt>**D3DCS \_ tout**</dt></span><span class="sxs-lookup"><span data-stu-id="0f8bb-113"><dt>**D3DCS\_ALL**</dt></span></span> </dl>          | <span data-ttu-id="0f8bb-114">Combinaison de tous les indicateurs de clip.</span><span class="sxs-lookup"><span data-stu-id="0f8bb-114">Combination of all clip flags.</span></span><br/>                                       |
| <span id="D3DCS_LEFT"></span><span id="d3dcs_left"></span><dl> <span data-ttu-id="0f8bb-115"><dt>**D3DCS \_ gauche**</dt></span><span class="sxs-lookup"><span data-stu-id="0f8bb-115"><dt>**D3DCS\_LEFT**</dt></span></span> </dl>       | <span data-ttu-id="0f8bb-116">Tous les vertex sont découpés par le plan gauche du frustum d’affichage.</span><span class="sxs-lookup"><span data-stu-id="0f8bb-116">All vertices are clipped by the left plane of the viewing frustum.</span></span><br/>   |
| <span id="D3DCS_RIGHT"></span><span id="d3dcs_right"></span><dl> <span data-ttu-id="0f8bb-117"><dt>**D3DCS \_ droit**</dt></span><span class="sxs-lookup"><span data-stu-id="0f8bb-117"><dt>**D3DCS\_RIGHT**</dt></span></span> </dl>    | <span data-ttu-id="0f8bb-118">Tous les vertex sont découpés par le plan droit du frustum de visualisation.</span><span class="sxs-lookup"><span data-stu-id="0f8bb-118">All vertices are clipped by the right plane of the viewing frustum.</span></span><br/>  |
| <span id="D3DCS_TOP"></span><span id="d3dcs_top"></span><dl> <span data-ttu-id="0f8bb-119"><dt>**D3DCS \_ Top**</dt></span><span class="sxs-lookup"><span data-stu-id="0f8bb-119"><dt>**D3DCS\_TOP**</dt></span></span> </dl>          | <span data-ttu-id="0f8bb-120">Tous les vertex sont découpés par le plan supérieur du frustum d’affichage.</span><span class="sxs-lookup"><span data-stu-id="0f8bb-120">All vertices are clipped by the top plane of the viewing frustum.</span></span><br/>    |
| <span id="D3DCS_BOTTOM"></span><span id="d3dcs_bottom"></span><dl> <span data-ttu-id="0f8bb-121"><dt>**D3DCS \_ bas**</dt></span><span class="sxs-lookup"><span data-stu-id="0f8bb-121"><dt>**D3DCS\_BOTTOM**</dt></span></span> </dl> | <span data-ttu-id="0f8bb-122">Tous les vertex sont découpés par le plan inférieur du frustum d’affichage.</span><span class="sxs-lookup"><span data-stu-id="0f8bb-122">All vertices are clipped by the bottom plane of the viewing frustum.</span></span><br/> |
| <span id="D3DCS_FRONT"></span><span id="d3dcs_front"></span><dl> <span data-ttu-id="0f8bb-123"><dt>**D3DCS \_ avant**</dt></span><span class="sxs-lookup"><span data-stu-id="0f8bb-123"><dt>**D3DCS\_FRONT**</dt></span></span> </dl>    | <span data-ttu-id="0f8bb-124">Tous les vertex sont découpés par le plan frontal de l’frustum de visualisation.</span><span class="sxs-lookup"><span data-stu-id="0f8bb-124">All vertices are clipped by the front plane of the viewing frustum.</span></span><br/>  |
| <span id="D3DCS_BACK"></span><span id="d3dcs_back"></span><dl> <span data-ttu-id="0f8bb-125"><dt>**D3DCS \_**</dt></span><span class="sxs-lookup"><span data-stu-id="0f8bb-125"><dt>**D3DCS\_BACK**</dt></span></span> </dl>       | <span data-ttu-id="0f8bb-126">Tous les vertex sont découpés par le plan arrière du frustum d’affichage.</span><span class="sxs-lookup"><span data-stu-id="0f8bb-126">All vertices are clipped by the back plane of the viewing frustum.</span></span><br/>   |
| <span id="D3DCS_PLANE0"></span><span id="d3dcs_plane0"></span><dl> <span data-ttu-id="0f8bb-127"><dt>**D3DCS \_ PLANE0**</dt></span><span class="sxs-lookup"><span data-stu-id="0f8bb-127"><dt>**D3DCS\_PLANE0**</dt></span></span> </dl> | <span data-ttu-id="0f8bb-128">Plans de découpage définis par l’application.</span><span class="sxs-lookup"><span data-stu-id="0f8bb-128">Application-defined clipping planes.</span></span><br/>                                 |
| <span id="D3DCS_PLANE1"></span><span id="d3dcs_plane1"></span><dl> <span data-ttu-id="0f8bb-129"><dt>**D3DCS \_ PLANE1**</dt></span><span class="sxs-lookup"><span data-stu-id="0f8bb-129"><dt>**D3DCS\_PLANE1**</dt></span></span> </dl> | <span data-ttu-id="0f8bb-130">Plans de découpage définis par l’application.</span><span class="sxs-lookup"><span data-stu-id="0f8bb-130">Application-defined clipping planes.</span></span><br/>                                 |
| <span id="D3DCS_PLANE2"></span><span id="d3dcs_plane2"></span><dl> <span data-ttu-id="0f8bb-131"><dt>**D3DCS \_ PLANE2**</dt></span><span class="sxs-lookup"><span data-stu-id="0f8bb-131"><dt>**D3DCS\_PLANE2**</dt></span></span> </dl> | <span data-ttu-id="0f8bb-132">Plans de découpage définis par l’application.</span><span class="sxs-lookup"><span data-stu-id="0f8bb-132">Application-defined clipping planes.</span></span><br/>                                 |
| <span id="D3DCS_PLANE3"></span><span id="d3dcs_plane3"></span><dl> <span data-ttu-id="0f8bb-133"><dt>**D3DCS \_ PLANE3**</dt></span><span class="sxs-lookup"><span data-stu-id="0f8bb-133"><dt>**D3DCS\_PLANE3**</dt></span></span> </dl> | <span data-ttu-id="0f8bb-134">Plans de découpage définis par l’application.</span><span class="sxs-lookup"><span data-stu-id="0f8bb-134">Application-defined clipping planes.</span></span><br/>                                 |
| <span id="D3DCS_PLANE4"></span><span id="d3dcs_plane4"></span><dl> <span data-ttu-id="0f8bb-135"><dt>**D3DCS \_ PLANE4**</dt></span><span class="sxs-lookup"><span data-stu-id="0f8bb-135"><dt>**D3DCS\_PLANE4**</dt></span></span> </dl> | <span data-ttu-id="0f8bb-136">Plans de découpage définis par l’application.</span><span class="sxs-lookup"><span data-stu-id="0f8bb-136">Application-defined clipping planes.</span></span><br/>                                 |
| <span id="D3DCS_PLANE5"></span><span id="d3dcs_plane5"></span><dl> <span data-ttu-id="0f8bb-137"><dt>**D3DCS \_ PLANE5**</dt></span><span class="sxs-lookup"><span data-stu-id="0f8bb-137"><dt>**D3DCS\_PLANE5**</dt></span></span> </dl> | <span data-ttu-id="0f8bb-138">Plans de découpage définis par l’application.</span><span class="sxs-lookup"><span data-stu-id="0f8bb-138">Application-defined clipping planes.</span></span><br/>                                 |



 

</dd> <dt>

<span data-ttu-id="0f8bb-139">**ClipIntersection**</span><span class="sxs-lookup"><span data-stu-id="0f8bb-139">**ClipIntersection**</span></span>
</dt> <dd>

<span data-ttu-id="0f8bb-140">Type : **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="0f8bb-140">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="0f8bb-141">Indicateurs d’intersection de clips qui décrivent l’état actuel du clip.</span><span class="sxs-lookup"><span data-stu-id="0f8bb-141">Clip intersection flags that describe the current clip status.</span></span> <span data-ttu-id="0f8bb-142">Ce membre peut prendre les mêmes indicateurs que ClipUnion.</span><span class="sxs-lookup"><span data-stu-id="0f8bb-142">This member can take the same flags as ClipUnion.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="0f8bb-143">Notes</span><span class="sxs-lookup"><span data-stu-id="0f8bb-143">Remarks</span></span>

<span data-ttu-id="0f8bb-144">Lorsque le découpage est activé pendant le traitement du vertex (par [**ProcessVertices**](/windows/desktop/api), [**DrawPrimitive**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-drawprimitive)ou d’autres fonctions de dessin), Direct3D calcule un code de découpage pour chaque vertex.</span><span class="sxs-lookup"><span data-stu-id="0f8bb-144">When clipping is enabled during vertex processing (by [**ProcessVertices**](/windows/desktop/api), [**DrawPrimitive**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-drawprimitive), or other drawing functions), Direct3D computes a clip code for every vertex.</span></span> <span data-ttu-id="0f8bb-145">Le code de la séquence est une combinaison de \_ \* bits D3DCS.</span><span class="sxs-lookup"><span data-stu-id="0f8bb-145">The clip code is a combination of D3DCS\_\* bits.</span></span> <span data-ttu-id="0f8bb-146">Lorsqu’un vertex se trouve en dehors d’un plan de découpage particulier, le bit correspondant est défini dans le code de découpage.</span><span class="sxs-lookup"><span data-stu-id="0f8bb-146">When a vertex is outside a particular clipping plane, the corresponding bit is set in the clipping code.</span></span> <span data-ttu-id="0f8bb-147">Direct3D conserve l’état du clip à l’aide de **D3DCLIPSTATUS9**, qui a des membres ClipUnion et ClipIntersection.</span><span class="sxs-lookup"><span data-stu-id="0f8bb-147">Direct3D maintains the clip status using **D3DCLIPSTATUS9**, which has ClipUnion and ClipIntersection members.</span></span> <span data-ttu-id="0f8bb-148">ClipUnion est un or au niveau du bit de tous les codes de clip de vertex et ClipIntersection est une opération and au niveau du bit de tous les codes de clip de vertex.</span><span class="sxs-lookup"><span data-stu-id="0f8bb-148">ClipUnion is a bitwise OR of all vertex clip codes and ClipIntersection is a bitwise AND of all vertex clip codes.</span></span> <span data-ttu-id="0f8bb-149">Les valeurs initiales sont égales à zéro pour ClipUnion et 0xFFFFFFFF pour ClipIntersection.</span><span class="sxs-lookup"><span data-stu-id="0f8bb-149">Initial values are zero for ClipUnion and 0xFFFFFFFF for ClipIntersection.</span></span> <span data-ttu-id="0f8bb-150">Lorsque le \_ découpage D3DRS a la valeur **false**, ClipUnion et ClipIntersection sont définis sur zéro.</span><span class="sxs-lookup"><span data-stu-id="0f8bb-150">When D3DRS\_CLIPPING is set to **FALSE**, ClipUnion and ClipIntersection are set to zero.</span></span> <span data-ttu-id="0f8bb-151">Direct3D met à jour l’état du clip pendant les appels de dessin.</span><span class="sxs-lookup"><span data-stu-id="0f8bb-151">Direct3D updates the clip status during drawing calls.</span></span> <span data-ttu-id="0f8bb-152">Pour calculer l’état du clip d’un objet particulier, définissez ClipUnion et ClipIntersection sur leur valeur initiale et poursuivez le dessin.</span><span class="sxs-lookup"><span data-stu-id="0f8bb-152">To compute clip status for a particular object, set ClipUnion and ClipIntersection to their initial value and continue drawing.</span></span>

<span data-ttu-id="0f8bb-153">L’état du clip n’est pas mis à jour par [**DrawRectPatch**](/windows/desktop/api) et [**DrawTriPatch**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-drawtripatch) , car il n’y a aucune émulation logicielle pour eux.</span><span class="sxs-lookup"><span data-stu-id="0f8bb-153">Clip status is not updated by [**DrawRectPatch**](/windows/desktop/api) and [**DrawTriPatch**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-drawtripatch) because there is no software emulation for them.</span></span>

## <a name="requirements"></a><span data-ttu-id="0f8bb-154">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="0f8bb-154">Requirements</span></span>



| <span data-ttu-id="0f8bb-155">Condition requise</span><span class="sxs-lookup"><span data-stu-id="0f8bb-155">Requirement</span></span> | <span data-ttu-id="0f8bb-156">Valeur</span><span class="sxs-lookup"><span data-stu-id="0f8bb-156">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="0f8bb-157">En-tête</span><span class="sxs-lookup"><span data-stu-id="0f8bb-157">Header</span></span><br/> | <dl> <span data-ttu-id="0f8bb-158"><dt>D3D9Types. h</dt></span><span class="sxs-lookup"><span data-stu-id="0f8bb-158"><dt>D3D9Types.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0f8bb-159">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="0f8bb-159">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0f8bb-160">Structures Direct3D</span><span class="sxs-lookup"><span data-stu-id="0f8bb-160">Direct3D Structures</span></span>](dx9-graphics-reference-d3d-structures.md)
</dt> <dt>

[<span data-ttu-id="0f8bb-161">**GetClipStatus**</span><span class="sxs-lookup"><span data-stu-id="0f8bb-161">**GetClipStatus**</span></span>](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-getclipstatus)
</dt> <dt>

[<span data-ttu-id="0f8bb-162">**SetClipStatus**</span><span class="sxs-lookup"><span data-stu-id="0f8bb-162">**SetClipStatus**</span></span>](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setclipstatus)
</dt> </dl>

 

 
