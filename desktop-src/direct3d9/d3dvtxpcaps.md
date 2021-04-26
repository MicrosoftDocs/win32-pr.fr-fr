---
description: Combinaison d’un ou de plusieurs indicateurs qui contrôlent le comportement de création de l’appareil.
ms.assetid: 2d3e548f-8559-4a36-b814-6d598bead1d0
title: D3DVTXPCAPS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 55ee7e5d423169e561df28b5d69017c77a71e183
ms.sourcegitcommit: b6fe9acffad983c14864b8fe0296f6025cb1f961
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/26/2021
ms.locfileid: "107998656"
---
# <a name="d3dvtxpcaps"></a><span data-ttu-id="6e8f8-103">D3DVTXPCAPS</span><span class="sxs-lookup"><span data-stu-id="6e8f8-103">D3DVTXPCAPS</span></span>

<span data-ttu-id="6e8f8-104">Combinaison d’un ou de plusieurs indicateurs qui contrôlent le comportement de création de l’appareil.</span><span class="sxs-lookup"><span data-stu-id="6e8f8-104">A combination of one or more flags that control the device create behavior.</span></span>



| <span data-ttu-id="6e8f8-105">\#définition</span><span class="sxs-lookup"><span data-stu-id="6e8f8-105">\#define</span></span>                                | <span data-ttu-id="6e8f8-106">Description</span><span class="sxs-lookup"><span data-stu-id="6e8f8-106">Description</span></span>                                                                                                                                                                                        |
|-----------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6e8f8-107">D3DVTXPCAPS \_ DIRECTIONALLIGHTS</span><span class="sxs-lookup"><span data-stu-id="6e8f8-107">D3DVTXPCAPS\_DIRECTIONALLIGHTS</span></span>          | <span data-ttu-id="6e8f8-108">L’appareil peut faire des lumières directionnelles.</span><span class="sxs-lookup"><span data-stu-id="6e8f8-108">Device can do directional lights.</span></span>                                                                                                                                                                  |
| <span data-ttu-id="6e8f8-109">D3DVTXPCAPS \_ LOCALVIEWER</span><span class="sxs-lookup"><span data-stu-id="6e8f8-109">D3DVTXPCAPS\_LOCALVIEWER</span></span>                | <span data-ttu-id="6e8f8-110">L’appareil peut effectuer une visionneuse locale.</span><span class="sxs-lookup"><span data-stu-id="6e8f8-110">Device can do local viewer.</span></span>                                                                                                                                                                        |
| <span data-ttu-id="6e8f8-111">D3DVTXPCAPS \_ MATERIALSOURCE7</span><span class="sxs-lookup"><span data-stu-id="6e8f8-111">D3DVTXPCAPS\_MATERIALSOURCE7</span></span>            | <span data-ttu-id="6e8f8-112">Lorsque cette limite est définie, l’appareil prend en charge les États de couleur : D3DRS \_ AMBIENTMATERIALSOURCE, D3DRS \_ DIFFUSEMATERIALSOURCE, D3DRS \_ EMISSIVEMATERIALSOURCE et D3DRS SPECULARMATERIALSOURCE \_ .</span><span class="sxs-lookup"><span data-stu-id="6e8f8-112">When this cap is set, the device supports the color material states: D3DRS\_AMBIENTMATERIALSOURCE, D3DRS\_DIFFUSEMATERIALSOURCE, D3DRS\_EMISSIVEMATERIALSOURCE, and D3DRS\_SPECULARMATERIALSOURCE.</span></span> |
| <span data-ttu-id="6e8f8-113">D3DVTXPCAPS \_ non \_ TEXGEN \_ NONLOCALVIEWER</span><span class="sxs-lookup"><span data-stu-id="6e8f8-113">D3DVTXPCAPS\_NO\_TEXGEN\_NONLOCALVIEWER</span></span> | <span data-ttu-id="6e8f8-114">L’appareil ne prend pas en charge la génération de texture en mode visionneuse non locale.</span><span class="sxs-lookup"><span data-stu-id="6e8f8-114">Device does not support texture generation in non-local viewer mode.</span></span>                                                                                                                               |
| <span data-ttu-id="6e8f8-115">D3DVTXPCAPS \_ POSITIONALLIGHTS</span><span class="sxs-lookup"><span data-stu-id="6e8f8-115">D3DVTXPCAPS\_POSITIONALLIGHTS</span></span>           | <span data-ttu-id="6e8f8-116">L’appareil peut effectuer des lumières de position (y compris un point et un point).</span><span class="sxs-lookup"><span data-stu-id="6e8f8-116">Device can do positional lights (includes point and spot).</span></span>                                                                                                                                         |
| <span data-ttu-id="6e8f8-117">D3DVTXPCAPS \_ TEXGEN</span><span class="sxs-lookup"><span data-stu-id="6e8f8-117">D3DVTXPCAPS\_TEXGEN</span></span>                     | <span data-ttu-id="6e8f8-118">L’appareil peut effectuer des texgen.</span><span class="sxs-lookup"><span data-stu-id="6e8f8-118">Device can do texgen.</span></span>                                                                                                                                                                              |
| <span data-ttu-id="6e8f8-119">D3DVTXPCAPS \_ TEXGEN \_ SPHEREMAP</span><span class="sxs-lookup"><span data-stu-id="6e8f8-119">D3DVTXPCAPS\_TEXGEN\_SPHEREMAP</span></span>          | <span data-ttu-id="6e8f8-120">L’appareil prend en charge D3DTSS \_ TCI \_ SPHEREMAP.</span><span class="sxs-lookup"><span data-stu-id="6e8f8-120">Device supports D3DTSS\_TCI\_SPHEREMAP.</span></span>                                                                                                                                                            |
| <span data-ttu-id="6e8f8-121">\_Interpolation D3DVTXPCAPS</span><span class="sxs-lookup"><span data-stu-id="6e8f8-121">D3DVTXPCAPS\_TWEENING</span></span>                   | <span data-ttu-id="6e8f8-122">L’appareil peut effectuer l’interpolation des sommets.</span><span class="sxs-lookup"><span data-stu-id="6e8f8-122">Device can do vertex tweening.</span></span>                                                                                                                                                                     |



 

## <a name="constant-information"></a><span data-ttu-id="6e8f8-123">Informations constantes</span><span class="sxs-lookup"><span data-stu-id="6e8f8-123">Constant Information</span></span>



|                          |            |
|--------------------------|------------|
| <span data-ttu-id="6e8f8-124">En-tête</span><span class="sxs-lookup"><span data-stu-id="6e8f8-124">Header</span></span>                   | <span data-ttu-id="6e8f8-125">d3d9caps. h</span><span class="sxs-lookup"><span data-stu-id="6e8f8-125">d3d9caps.h</span></span> |
| <span data-ttu-id="6e8f8-126">Système d’exploitation minimal</span><span class="sxs-lookup"><span data-stu-id="6e8f8-126">Minimum operating system</span></span> | <span data-ttu-id="6e8f8-127">Windows 98</span><span class="sxs-lookup"><span data-stu-id="6e8f8-127">Windows 98</span></span> |



 

## <a name="related-topics"></a><span data-ttu-id="6e8f8-128">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="6e8f8-128">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="6e8f8-129">Constantes Direct3D</span><span class="sxs-lookup"><span data-stu-id="6e8f8-129">Direct3D Constants</span></span>](dx9-graphics-reference-d3d-constants.md)
</dt> </dl>

 

 



