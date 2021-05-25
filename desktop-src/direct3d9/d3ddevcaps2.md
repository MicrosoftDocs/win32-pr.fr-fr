---
description: Indicateurs de capacité du pilote D3DDEVCAPS2.
ms.assetid: 3f3b9f86-dee3-4506-bd2e-1dcc8ba617ed
title: D3DDEVCAPS2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6296db9b338d5f9a8c8ede702a784baf1fdfd462
ms.sourcegitcommit: b40a986d5ded926ae7617119cdd35d99b533bad9
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/24/2021
ms.locfileid: "110343204"
---
# <a name="d3ddevcaps2"></a><span data-ttu-id="8281a-103">D3DDEVCAPS2</span><span class="sxs-lookup"><span data-stu-id="8281a-103">D3DDEVCAPS2</span></span>

<span data-ttu-id="8281a-104">Indicateurs de capacité du pilote D3DDEVCAPS2.</span><span class="sxs-lookup"><span data-stu-id="8281a-104">D3DDEVCAPS2 driver capability flags.</span></span>



| <span data-ttu-id="8281a-105">\#définition</span><span class="sxs-lookup"><span data-stu-id="8281a-105">\#define</span></span>                                        | <span data-ttu-id="8281a-106">Description</span><span class="sxs-lookup"><span data-stu-id="8281a-106">Description</span></span>                                                                                                                                                                                                               |
|-------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8281a-107">D3DDEVCAPS2 \_ ADAPTIVETESSRTPATCH</span><span class="sxs-lookup"><span data-stu-id="8281a-107">D3DDEVCAPS2\_ADAPTIVETESSRTPATCH</span></span>                | <span data-ttu-id="8281a-108">L’appareil prend en charge le pavage adaptatif des correctifs RT</span><span class="sxs-lookup"><span data-stu-id="8281a-108">Device supports adaptive tessellation of RT-patches</span></span>                                                                                                                                                                       |
| <span data-ttu-id="8281a-109">D3DDEVCAPS2 \_ ADAPTIVETESSNPATCH</span><span class="sxs-lookup"><span data-stu-id="8281a-109">D3DDEVCAPS2\_ADAPTIVETESSNPATCH</span></span>                 | <span data-ttu-id="8281a-110">L’appareil prend en charge le pavage adaptatif des N-patchs.</span><span class="sxs-lookup"><span data-stu-id="8281a-110">Device supports adaptive tessellation of N-patches.</span></span>                                                                                                                                                                       |
| <span data-ttu-id="8281a-111">D3DDEVCAPS2 \_ peut \_ STRETCHRECT \_ des \_ textures</span><span class="sxs-lookup"><span data-stu-id="8281a-111">D3DDEVCAPS2\_CAN\_STRETCHRECT\_FROM\_TEXTURES</span></span>   | <span data-ttu-id="8281a-112">L’appareil prend en charge [**StretchRect**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-stretchrect) à l’aide d’une texture comme source.</span><span class="sxs-lookup"><span data-stu-id="8281a-112">Device supports [**StretchRect**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-stretchrect) using a texture as the source.</span></span>                                                                                                                       |
| <span data-ttu-id="8281a-113">D3DDEVCAPS2 \_ DMAPNPATCH</span><span class="sxs-lookup"><span data-stu-id="8281a-113">D3DDEVCAPS2\_DMAPNPATCH</span></span>                         | <span data-ttu-id="8281a-114">L’appareil prend en charge les mappages de déplacement pour N-patchs.</span><span class="sxs-lookup"><span data-stu-id="8281a-114">Device supports displacement maps for N-patches.</span></span>                                                                                                                                                                          |
| <span data-ttu-id="8281a-115">D3DDEVCAPS2 \_ PRESAMPLEDDMAPNPATCH</span><span class="sxs-lookup"><span data-stu-id="8281a-115">D3DDEVCAPS2\_PRESAMPLEDDMAPNPATCH</span></span>               | <span data-ttu-id="8281a-116">L’appareil prend en charge les mappages de remplacement prééchantillonnés pour les N-patchs.</span><span class="sxs-lookup"><span data-stu-id="8281a-116">Device supports presampled displacement maps for N-patches.</span></span> <span data-ttu-id="8281a-117">Pour plus d’informations sur le mappage de déplacement, consultez [mappage de déplacement (Direct3D 9)](displacement-mapping.md).</span><span class="sxs-lookup"><span data-stu-id="8281a-117">For more information about displacement mapping, see [Displacement Mapping (Direct3D 9)](displacement-mapping.md).</span></span>                                           |
| <span data-ttu-id="8281a-118">D3DDEVCAPS2 \_ STREAMOFFSET</span><span class="sxs-lookup"><span data-stu-id="8281a-118">D3DDEVCAPS2\_STREAMOFFSET</span></span>                       | <span data-ttu-id="8281a-119">L’appareil prend en charge les décalages de flux.</span><span class="sxs-lookup"><span data-stu-id="8281a-119">Device supports stream offsets.</span></span>                                                                                                                                                                                           |
| <span data-ttu-id="8281a-120">D3DDEVCAPS2 \_ VERTEXELEMENTSCANSHARESTREAMOFFSET</span><span class="sxs-lookup"><span data-stu-id="8281a-120">D3DDEVCAPS2\_VERTEXELEMENTSCANSHARESTREAMOFFSET</span></span> | <span data-ttu-id="8281a-121">Plusieurs éléments vertex peuvent partager le même offset dans un flux si D3DDEVCAPS2 \_ VERTEXELEMENTSCANSHARESTREAMOFFSET est défini par l’appareil et que la déclaration de vertex n’a pas d’élément avec D3DDECLUSAGE \_ POSITIONT0.</span><span class="sxs-lookup"><span data-stu-id="8281a-121">Multiple vertex elements can share the same offset in a stream if D3DDEVCAPS2\_VERTEXELEMENTSCANSHARESTREAMOFFSET is set by the device and the vertex declaration does not have an element with D3DDECLUSAGE\_POSITIONT0.</span></span> |



 

## <a name="constant-information"></a><span data-ttu-id="8281a-122">Informations constantes</span><span class="sxs-lookup"><span data-stu-id="8281a-122">Constant Information</span></span>



| <span data-ttu-id="8281a-123">Condition requise</span><span class="sxs-lookup"><span data-stu-id="8281a-123">Requirement</span></span>                         | <span data-ttu-id="8281a-124">Valeur</span><span class="sxs-lookup"><span data-stu-id="8281a-124">Value</span></span>           |
|--------------------------|------------|
| <span data-ttu-id="8281a-125">En-tête</span><span class="sxs-lookup"><span data-stu-id="8281a-125">Header</span></span>                   | <span data-ttu-id="8281a-126">d3d9caps. h</span><span class="sxs-lookup"><span data-stu-id="8281a-126">d3d9caps.h</span></span> |
| <span data-ttu-id="8281a-127">Système d’exploitation minimal</span><span class="sxs-lookup"><span data-stu-id="8281a-127">Minimum operating system</span></span> | <span data-ttu-id="8281a-128">Windows 98</span><span class="sxs-lookup"><span data-stu-id="8281a-128">Windows 98</span></span> |



 

## <a name="related-topics"></a><span data-ttu-id="8281a-129">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="8281a-129">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="8281a-130">Constantes Direct3D</span><span class="sxs-lookup"><span data-stu-id="8281a-130">Direct3D Constants</span></span>](dx9-graphics-reference-d3d-constants.md)
</dt> </dl>

 

 
