---
description: Indicateurs de capacité du pilote.
ms.assetid: d9cd7388-3413-472d-aacb-0b8c9c60031a
title: D3DCAPS3
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fda81aa7f77dcaf03eb06b357ebfb91b4956f6d4
ms.sourcegitcommit: b40a986d5ded926ae7617119cdd35d99b533bad9
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/24/2021
ms.locfileid: "110343364"
---
# <a name="d3dcaps3"></a><span data-ttu-id="d33a4-103">D3DCAPS3</span><span class="sxs-lookup"><span data-stu-id="d33a4-103">D3DCAPS3</span></span>

<span data-ttu-id="d33a4-104">Indicateurs de capacité du pilote.</span><span class="sxs-lookup"><span data-stu-id="d33a4-104">Driver capability flags.</span></span>



<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<tbody>
<tr class="odd">
<td><span data-ttu-id="d33a4-105">#définition</span><span class="sxs-lookup"><span data-stu-id="d33a4-105">#define</span></span></td>
<td><span data-ttu-id="d33a4-106">Valeur</span><span class="sxs-lookup"><span data-stu-id="d33a4-106">Value</span></span></td>
<td><span data-ttu-id="d33a4-107">Description</span><span class="sxs-lookup"><span data-stu-id="d33a4-107">Description</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="d33a4-108">D3DCAPS3_ALPHA_FULLSCREEN_FLIP_OR_DISCARD</span><span class="sxs-lookup"><span data-stu-id="d33a4-108">D3DCAPS3_ALPHA_FULLSCREEN_FLIP_OR_DISCARD</span></span></td>
<td><span data-ttu-id="d33a4-109">0x00000020L</span><span class="sxs-lookup"><span data-stu-id="d33a4-109">0x00000020L</span></span></td>
<td><span data-ttu-id="d33a4-110">Indique que l’appareil peut respecter l’état de rendu D3DRS_ALPHABLENDENABLE en mode plein écran lors de l’utilisation de l’effet d’échange de retournement ou de suppression.</span><span class="sxs-lookup"><span data-stu-id="d33a4-110">Indicates that the device can respect the D3DRS_ALPHABLENDENABLE render state in full-screen mode while using the FLIP or DISCARD swap effect.</span></span> <span data-ttu-id="d33a4-111">Cela s’applique uniquement lorsque les États D3DRS_SRCBLEND ou D3DRS_DESTBLEND sont définis sur l’un des éléments suivants :</span><span class="sxs-lookup"><span data-stu-id="d33a4-111">This only applies when the D3DRS_SRCBLEND or D3DRS_DESTBLEND states are set to one of the following:</span></span>
<ul>
<li><span data-ttu-id="d33a4-112">D3DBLEND_DESTALPHA</span><span class="sxs-lookup"><span data-stu-id="d33a4-112">D3DBLEND_DESTALPHA</span></span></li>
<li><span data-ttu-id="d33a4-113">D3DBLEND_INVDESTALPHA</span><span class="sxs-lookup"><span data-stu-id="d33a4-113">D3DBLEND_INVDESTALPHA</span></span></li>
<li><span data-ttu-id="d33a4-114">D3DBLEND_DESTCOLOR</span><span class="sxs-lookup"><span data-stu-id="d33a4-114">D3DBLEND_DESTCOLOR</span></span></li>
<li><span data-ttu-id="d33a4-115">D3DBLEND_INVDESTCOLOR</span><span class="sxs-lookup"><span data-stu-id="d33a4-115">D3DBLEND_INVDESTCOLOR</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="d33a4-116">D3DCAPS3_COPY_TO_VIDMEM</span><span class="sxs-lookup"><span data-stu-id="d33a4-116">D3DCAPS3_COPY_TO_VIDMEM</span></span></td>
<td><span data-ttu-id="d33a4-117">0x00000100L</span><span class="sxs-lookup"><span data-stu-id="d33a4-117">0x00000100L</span></span></td>
<td><span data-ttu-id="d33a4-118">L’appareil peut accélérer la copie mémoire de la mémoire système à la mémoire vidéo locale.</span><span class="sxs-lookup"><span data-stu-id="d33a4-118">Device can accelerate a memory copy from system memory to local video memory.</span></span> <span data-ttu-id="d33a4-119">Cette limite garantit que les appels <a href="/windows/desktop/api"><strong>UpdateSurface</strong></a> et <a href="/windows/desktop/api"><strong>UpdateTexture</strong></a> seront accélérés par le matériel.</span><span class="sxs-lookup"><span data-stu-id="d33a4-119">This cap guarantees that <a href="/windows/desktop/api"><strong>UpdateSurface</strong></a> and <a href="/windows/desktop/api"><strong>UpdateTexture</strong></a> calls will be hardware accelerated.</span></span> <span data-ttu-id="d33a4-120">Si cette limite est absente, ces appels échouent, mais ils sont plus lents.</span><span class="sxs-lookup"><span data-stu-id="d33a4-120">If this cap is absent, these calls will succeed but will be slower.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="d33a4-121">D3DCAPS3_COPY_TO_SYSTEMMEM</span><span class="sxs-lookup"><span data-stu-id="d33a4-121">D3DCAPS3_COPY_TO_SYSTEMMEM</span></span></td>
<td><span data-ttu-id="d33a4-122">0x00000200L</span><span class="sxs-lookup"><span data-stu-id="d33a4-122">0x00000200L</span></span></td>
<td><span data-ttu-id="d33a4-123">L’appareil peut accélérer la copie en mémoire de la mémoire vidéo locale jusqu’à la mémoire système.</span><span class="sxs-lookup"><span data-stu-id="d33a4-123">Device can accelerate a memory copy from local video memory to system memory.</span></span> <span data-ttu-id="d33a4-124">Cette limite garantit que les appels <a href="/windows/desktop/api"><strong>GetRenderTargetData</strong></a> seront accélérés par le matériel.</span><span class="sxs-lookup"><span data-stu-id="d33a4-124">This cap guarantees that <a href="/windows/desktop/api"><strong>GetRenderTargetData</strong></a> calls will be hardware accelerated.</span></span> <span data-ttu-id="d33a4-125">Si cette limite est absente, cet appel échouera, mais sera plus lent.</span><span class="sxs-lookup"><span data-stu-id="d33a4-125">If this cap is absent, this call will succeed but will be slower.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="d33a4-126">D3DCAPS3_DXVAHD</span><span class="sxs-lookup"><span data-stu-id="d33a4-126">D3DCAPS3_DXVAHD</span></span></td>
<td><span data-ttu-id="d33a4-127">0x00000400L</span><span class="sxs-lookup"><span data-stu-id="d33a4-127">0x00000400L</span></span></td>
<td><span data-ttu-id="d33a4-128">Le pilote d’affichage prend en charge l’interface DDI DXVA-HD.</span><span class="sxs-lookup"><span data-stu-id="d33a4-128">The display driver supports the DXVA-HD DDI.</span></span> <span data-ttu-id="d33a4-129">Pour plus d’informations sur la DDI DXVA-HD, consultez <a href="https://msdn.microsoft.com/library/dd835176.aspx">traitement d' High-Definition vidéo</a>.</span><span class="sxs-lookup"><span data-stu-id="d33a4-129">For more information about DXVA-HD DDI, see <a href="https://msdn.microsoft.com/library/dd835176.aspx">Processing High-Definition Video</a>.</span></span><br/> 
<table>
<tbody>
<tr class="odd">
<td><span data-ttu-id="d33a4-130">Différences entre Direct3D 9 et Direct3D 9Ex :</span><span class="sxs-lookup"><span data-stu-id="d33a4-130">Differences between Direct3D 9 and Direct3D 9Ex:</span></span><br/> <span data-ttu-id="d33a4-131">Cet indicateur est disponible uniquement dans Direct3D 9Ex.</span><span class="sxs-lookup"><span data-stu-id="d33a4-131">This flag is available in Direct3D 9Ex only.</span></span><br/></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="even">
<td><span data-ttu-id="d33a4-132">D3DCAPS3_LINEAR_TO_SRGB_PRESENTATION</span><span class="sxs-lookup"><span data-stu-id="d33a4-132">D3DCAPS3_LINEAR_TO_SRGB_PRESENTATION</span></span></td>
<td><span data-ttu-id="d33a4-133">0x00000080L</span><span class="sxs-lookup"><span data-stu-id="d33a4-133">0x00000080L</span></span></td>
<td><span data-ttu-id="d33a4-134">Indique que l’appareil peut effectuer une correction gamma à partir d’une mémoire tampon d’arrière-plan (contenant du contenu linéaire) sur un bureau sRVB.</span><span class="sxs-lookup"><span data-stu-id="d33a4-134">Indicates that the device can perform gamma correction from a windowed back buffer (containing linear content) to an sRGB desktop.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="d33a4-135">D3DCAPS3_RESERVED</span><span class="sxs-lookup"><span data-stu-id="d33a4-135">D3DCAPS3_RESERVED</span></span></td>
<td><span data-ttu-id="d33a4-136">0x8000001fL</span><span class="sxs-lookup"><span data-stu-id="d33a4-136">0x8000001fL</span></span></td>
<td><span data-ttu-id="d33a4-137">Réservé non utilisé.</span><span class="sxs-lookup"><span data-stu-id="d33a4-137">Reserved; not used.</span></span></td>
</tr>
</tbody>
</table>



 

<span data-ttu-id="d33a4-138">Ces constantes sont utilisées par le membre D3CAPS3 de [**D3DCAPS9**](/windows/desktop/api/D3D9Caps/ns-d3d9caps-d3dcaps9).</span><span class="sxs-lookup"><span data-stu-id="d33a4-138">These constants are used by the D3CAPS3 member of [**D3DCAPS9**](/windows/desktop/api/D3D9Caps/ns-d3d9caps-d3dcaps9).</span></span>

## <a name="constant-information"></a><span data-ttu-id="d33a4-139">Informations constantes</span><span class="sxs-lookup"><span data-stu-id="d33a4-139">Constant Information</span></span>



|  <span data-ttu-id="d33a4-140">Condition requise</span><span class="sxs-lookup"><span data-stu-id="d33a4-140">Requirement</span></span>                        | <span data-ttu-id="d33a4-141">Valeur</span><span class="sxs-lookup"><span data-stu-id="d33a4-141">Value</span></span>           |
|--------------------------|------------|
| <span data-ttu-id="d33a4-142">En-tête</span><span class="sxs-lookup"><span data-stu-id="d33a4-142">Header</span></span>                   | <span data-ttu-id="d33a4-143">d3d9caps. h</span><span class="sxs-lookup"><span data-stu-id="d33a4-143">d3d9caps.h</span></span> |
| <span data-ttu-id="d33a4-144">Système d’exploitation minimal</span><span class="sxs-lookup"><span data-stu-id="d33a4-144">Minimum operating system</span></span> | <span data-ttu-id="d33a4-145">Windows 98</span><span class="sxs-lookup"><span data-stu-id="d33a4-145">Windows 98</span></span> |



 

## <a name="related-topics"></a><span data-ttu-id="d33a4-146">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="d33a4-146">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="d33a4-147">Constantes Direct3D</span><span class="sxs-lookup"><span data-stu-id="d33a4-147">Direct3D Constants</span></span>](dx9-graphics-reference-d3d-constants.md)
</dt> </dl>

 

 




