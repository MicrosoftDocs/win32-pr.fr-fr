---
description: Consultez la liste des indicateurs de capacité du pilote D3DCAPS3. Comprend les définitions, les valeurs et les descriptions avec des liens vers des API.
ms.assetid: d9cd7388-3413-472d-aacb-0b8c9c60031a
title: D3DCAPS3
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7b28614b2b2ea3c20f828b39f2b8926cb484a88c
ms.sourcegitcommit: 5d4e99f4c8f42f5f543e52cb9beb9fb13ec56c5f
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/19/2021
ms.locfileid: "112408262"
---
# <a name="d3dcaps3"></a><span data-ttu-id="27c32-104">D3DCAPS3</span><span class="sxs-lookup"><span data-stu-id="27c32-104">D3DCAPS3</span></span>

<span data-ttu-id="27c32-105">Indicateurs de capacité du pilote.</span><span class="sxs-lookup"><span data-stu-id="27c32-105">Driver capability flags.</span></span>



<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<tbody>
<tr class="odd">
<td><span data-ttu-id="27c32-106">#définition</span><span class="sxs-lookup"><span data-stu-id="27c32-106">#define</span></span></td>
<td><span data-ttu-id="27c32-107">Valeur</span><span class="sxs-lookup"><span data-stu-id="27c32-107">Value</span></span></td>
<td><span data-ttu-id="27c32-108">Description</span><span class="sxs-lookup"><span data-stu-id="27c32-108">Description</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="27c32-109">D3DCAPS3_ALPHA_FULLSCREEN_FLIP_OR_DISCARD</span><span class="sxs-lookup"><span data-stu-id="27c32-109">D3DCAPS3_ALPHA_FULLSCREEN_FLIP_OR_DISCARD</span></span></td>
<td><span data-ttu-id="27c32-110">0x00000020L</span><span class="sxs-lookup"><span data-stu-id="27c32-110">0x00000020L</span></span></td>
<td><span data-ttu-id="27c32-111">Indique que l’appareil peut respecter l’état de rendu D3DRS_ALPHABLENDENABLE en mode plein écran lors de l’utilisation de l’effet d’échange de retournement ou de suppression.</span><span class="sxs-lookup"><span data-stu-id="27c32-111">Indicates that the device can respect the D3DRS_ALPHABLENDENABLE render state in full-screen mode while using the FLIP or DISCARD swap effect.</span></span> <span data-ttu-id="27c32-112">Cela s’applique uniquement lorsque les États D3DRS_SRCBLEND ou D3DRS_DESTBLEND sont définis sur l’un des éléments suivants :</span><span class="sxs-lookup"><span data-stu-id="27c32-112">This only applies when the D3DRS_SRCBLEND or D3DRS_DESTBLEND states are set to one of the following:</span></span>
<ul>
<li><span data-ttu-id="27c32-113">D3DBLEND_DESTALPHA</span><span class="sxs-lookup"><span data-stu-id="27c32-113">D3DBLEND_DESTALPHA</span></span></li>
<li><span data-ttu-id="27c32-114">D3DBLEND_INVDESTALPHA</span><span class="sxs-lookup"><span data-stu-id="27c32-114">D3DBLEND_INVDESTALPHA</span></span></li>
<li><span data-ttu-id="27c32-115">D3DBLEND_DESTCOLOR</span><span class="sxs-lookup"><span data-stu-id="27c32-115">D3DBLEND_DESTCOLOR</span></span></li>
<li><span data-ttu-id="27c32-116">D3DBLEND_INVDESTCOLOR</span><span class="sxs-lookup"><span data-stu-id="27c32-116">D3DBLEND_INVDESTCOLOR</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="27c32-117">D3DCAPS3_COPY_TO_VIDMEM</span><span class="sxs-lookup"><span data-stu-id="27c32-117">D3DCAPS3_COPY_TO_VIDMEM</span></span></td>
<td><span data-ttu-id="27c32-118">0x00000100L</span><span class="sxs-lookup"><span data-stu-id="27c32-118">0x00000100L</span></span></td>
<td><span data-ttu-id="27c32-119">L’appareil peut accélérer la copie mémoire de la mémoire système à la mémoire vidéo locale.</span><span class="sxs-lookup"><span data-stu-id="27c32-119">Device can accelerate a memory copy from system memory to local video memory.</span></span> <span data-ttu-id="27c32-120">Cette limite garantit que les appels <a href="/windows/desktop/api"><strong>UpdateSurface</strong></a> et <a href="/windows/desktop/api"><strong>UpdateTexture</strong></a> seront accélérés par le matériel.</span><span class="sxs-lookup"><span data-stu-id="27c32-120">This cap guarantees that <a href="/windows/desktop/api"><strong>UpdateSurface</strong></a> and <a href="/windows/desktop/api"><strong>UpdateTexture</strong></a> calls will be hardware accelerated.</span></span> <span data-ttu-id="27c32-121">Si cette limite est absente, ces appels échouent, mais ils sont plus lents.</span><span class="sxs-lookup"><span data-stu-id="27c32-121">If this cap is absent, these calls will succeed but will be slower.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="27c32-122">D3DCAPS3_COPY_TO_SYSTEMMEM</span><span class="sxs-lookup"><span data-stu-id="27c32-122">D3DCAPS3_COPY_TO_SYSTEMMEM</span></span></td>
<td><span data-ttu-id="27c32-123">0x00000200L</span><span class="sxs-lookup"><span data-stu-id="27c32-123">0x00000200L</span></span></td>
<td><span data-ttu-id="27c32-124">L’appareil peut accélérer la copie en mémoire de la mémoire vidéo locale jusqu’à la mémoire système.</span><span class="sxs-lookup"><span data-stu-id="27c32-124">Device can accelerate a memory copy from local video memory to system memory.</span></span> <span data-ttu-id="27c32-125">Cette limite garantit que les appels <a href="/windows/desktop/api"><strong>GetRenderTargetData</strong></a> seront accélérés par le matériel.</span><span class="sxs-lookup"><span data-stu-id="27c32-125">This cap guarantees that <a href="/windows/desktop/api"><strong>GetRenderTargetData</strong></a> calls will be hardware accelerated.</span></span> <span data-ttu-id="27c32-126">Si cette limite est absente, cet appel échouera, mais sera plus lent.</span><span class="sxs-lookup"><span data-stu-id="27c32-126">If this cap is absent, this call will succeed but will be slower.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="27c32-127">D3DCAPS3_DXVAHD</span><span class="sxs-lookup"><span data-stu-id="27c32-127">D3DCAPS3_DXVAHD</span></span></td>
<td><span data-ttu-id="27c32-128">0x00000400L</span><span class="sxs-lookup"><span data-stu-id="27c32-128">0x00000400L</span></span></td>
<td><span data-ttu-id="27c32-129">Le pilote d’affichage prend en charge l’interface DDI DXVA-HD.</span><span class="sxs-lookup"><span data-stu-id="27c32-129">The display driver supports the DXVA-HD DDI.</span></span> <span data-ttu-id="27c32-130">Pour plus d’informations sur la DDI DXVA-HD, consultez <a href="https://msdn.microsoft.com/library/dd835176.aspx">traitement d' High-Definition vidéo</a>.</span><span class="sxs-lookup"><span data-stu-id="27c32-130">For more information about DXVA-HD DDI, see <a href="https://msdn.microsoft.com/library/dd835176.aspx">Processing High-Definition Video</a>.</span></span><br/> 
<table>
<tbody>
<tr class="odd">
<td><span data-ttu-id="27c32-131">Différences entre Direct3D 9 et Direct3D 9Ex :</span><span class="sxs-lookup"><span data-stu-id="27c32-131">Differences between Direct3D 9 and Direct3D 9Ex:</span></span><br/> <span data-ttu-id="27c32-132">Cet indicateur est disponible uniquement dans Direct3D 9Ex.</span><span class="sxs-lookup"><span data-stu-id="27c32-132">This flag is available in Direct3D 9Ex only.</span></span><br/></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="even">
<td><span data-ttu-id="27c32-133">D3DCAPS3_LINEAR_TO_SRGB_PRESENTATION</span><span class="sxs-lookup"><span data-stu-id="27c32-133">D3DCAPS3_LINEAR_TO_SRGB_PRESENTATION</span></span></td>
<td><span data-ttu-id="27c32-134">0x00000080L</span><span class="sxs-lookup"><span data-stu-id="27c32-134">0x00000080L</span></span></td>
<td><span data-ttu-id="27c32-135">Indique que l’appareil peut effectuer une correction gamma à partir d’une mémoire tampon d’arrière-plan (contenant du contenu linéaire) sur un bureau sRVB.</span><span class="sxs-lookup"><span data-stu-id="27c32-135">Indicates that the device can perform gamma correction from a windowed back buffer (containing linear content) to an sRGB desktop.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="27c32-136">D3DCAPS3_RESERVED</span><span class="sxs-lookup"><span data-stu-id="27c32-136">D3DCAPS3_RESERVED</span></span></td>
<td><span data-ttu-id="27c32-137">0x8000001fL</span><span class="sxs-lookup"><span data-stu-id="27c32-137">0x8000001fL</span></span></td>
<td><span data-ttu-id="27c32-138">Réservé non utilisé.</span><span class="sxs-lookup"><span data-stu-id="27c32-138">Reserved; not used.</span></span></td>
</tr>
</tbody>
</table>



 

<span data-ttu-id="27c32-139">Ces constantes sont utilisées par le membre D3CAPS3 de [**D3DCAPS9**](/windows/desktop/api/D3D9Caps/ns-d3d9caps-d3dcaps9).</span><span class="sxs-lookup"><span data-stu-id="27c32-139">These constants are used by the D3CAPS3 member of [**D3DCAPS9**](/windows/desktop/api/D3D9Caps/ns-d3d9caps-d3dcaps9).</span></span>

## <a name="constant-information"></a><span data-ttu-id="27c32-140">Informations constantes</span><span class="sxs-lookup"><span data-stu-id="27c32-140">Constant Information</span></span>



|  <span data-ttu-id="27c32-141">Condition requise</span><span class="sxs-lookup"><span data-stu-id="27c32-141">Requirement</span></span>                        | <span data-ttu-id="27c32-142">Valeur</span><span class="sxs-lookup"><span data-stu-id="27c32-142">Value</span></span>           |
|--------------------------|------------|
| <span data-ttu-id="27c32-143">En-tête</span><span class="sxs-lookup"><span data-stu-id="27c32-143">Header</span></span>                   | <span data-ttu-id="27c32-144">d3d9caps. h</span><span class="sxs-lookup"><span data-stu-id="27c32-144">d3d9caps.h</span></span> |
| <span data-ttu-id="27c32-145">Système d’exploitation minimal</span><span class="sxs-lookup"><span data-stu-id="27c32-145">Minimum operating system</span></span> | <span data-ttu-id="27c32-146">Windows 98</span><span class="sxs-lookup"><span data-stu-id="27c32-146">Windows 98</span></span> |



 

## <a name="related-topics"></a><span data-ttu-id="27c32-147">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="27c32-147">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="27c32-148">Constantes Direct3D</span><span class="sxs-lookup"><span data-stu-id="27c32-148">Direct3D Constants</span></span>](dx9-graphics-reference-d3d-constants.md)
</dt> </dl>

 

 




