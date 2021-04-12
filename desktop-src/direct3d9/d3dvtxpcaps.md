---
description: Combinaison d’un ou de plusieurs indicateurs qui contrôlent le comportement de création de l’appareil.
ms.assetid: 2d3e548f-8559-4a36-b814-6d598bead1d0
title: D3DVTXPCAPS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8a2ffff3d1dcc1f68912847b9ce1677c2031189c
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104393207"
---
# <a name="d3dvtxpcaps"></a><span data-ttu-id="afe14-103">D3DVTXPCAPS</span><span class="sxs-lookup"><span data-stu-id="afe14-103">D3DVTXPCAPS</span></span>

<span data-ttu-id="afe14-104">Combinaison d’un ou de plusieurs indicateurs qui contrôlent le comportement de création de l’appareil.</span><span class="sxs-lookup"><span data-stu-id="afe14-104">A combination of one or more flags that control the device create behavior.</span></span>



|                                         |                                                                                                                                                                                                    |
|-----------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="afe14-105">\#définition</span><span class="sxs-lookup"><span data-stu-id="afe14-105">\#define</span></span>                                | <span data-ttu-id="afe14-106">Description</span><span class="sxs-lookup"><span data-stu-id="afe14-106">Description</span></span>                                                                                                                                                                                        |
| <span data-ttu-id="afe14-107">D3DVTXPCAPS \_ DIRECTIONALLIGHTS</span><span class="sxs-lookup"><span data-stu-id="afe14-107">D3DVTXPCAPS\_DIRECTIONALLIGHTS</span></span>          | <span data-ttu-id="afe14-108">L’appareil peut faire des lumières directionnelles.</span><span class="sxs-lookup"><span data-stu-id="afe14-108">Device can do directional lights.</span></span>                                                                                                                                                                  |
| <span data-ttu-id="afe14-109">D3DVTXPCAPS \_ LOCALVIEWER</span><span class="sxs-lookup"><span data-stu-id="afe14-109">D3DVTXPCAPS\_LOCALVIEWER</span></span>                | <span data-ttu-id="afe14-110">L’appareil peut effectuer une visionneuse locale.</span><span class="sxs-lookup"><span data-stu-id="afe14-110">Device can do local viewer.</span></span>                                                                                                                                                                        |
| <span data-ttu-id="afe14-111">D3DVTXPCAPS \_ MATERIALSOURCE7</span><span class="sxs-lookup"><span data-stu-id="afe14-111">D3DVTXPCAPS\_MATERIALSOURCE7</span></span>            | <span data-ttu-id="afe14-112">Lorsque cette limite est définie, l’appareil prend en charge les États de couleur : D3DRS \_ AMBIENTMATERIALSOURCE, D3DRS \_ DIFFUSEMATERIALSOURCE, D3DRS \_ EMISSIVEMATERIALSOURCE et D3DRS SPECULARMATERIALSOURCE \_ .</span><span class="sxs-lookup"><span data-stu-id="afe14-112">When this cap is set, the device supports the color material states: D3DRS\_AMBIENTMATERIALSOURCE, D3DRS\_DIFFUSEMATERIALSOURCE, D3DRS\_EMISSIVEMATERIALSOURCE, and D3DRS\_SPECULARMATERIALSOURCE.</span></span> |
| <span data-ttu-id="afe14-113">D3DVTXPCAPS \_ non \_ TEXGEN \_ NONLOCALVIEWER</span><span class="sxs-lookup"><span data-stu-id="afe14-113">D3DVTXPCAPS\_NO\_TEXGEN\_NONLOCALVIEWER</span></span> | <span data-ttu-id="afe14-114">L’appareil ne prend pas en charge la génération de texture en mode visionneuse non locale.</span><span class="sxs-lookup"><span data-stu-id="afe14-114">Device does not support texture generation in non-local viewer mode.</span></span>                                                                                                                               |
| <span data-ttu-id="afe14-115">D3DVTXPCAPS \_ POSITIONALLIGHTS</span><span class="sxs-lookup"><span data-stu-id="afe14-115">D3DVTXPCAPS\_POSITIONALLIGHTS</span></span>           | <span data-ttu-id="afe14-116">L’appareil peut effectuer des lumières de position (y compris un point et un point).</span><span class="sxs-lookup"><span data-stu-id="afe14-116">Device can do positional lights (includes point and spot).</span></span>                                                                                                                                         |
| <span data-ttu-id="afe14-117">D3DVTXPCAPS \_ TEXGEN</span><span class="sxs-lookup"><span data-stu-id="afe14-117">D3DVTXPCAPS\_TEXGEN</span></span>                     | <span data-ttu-id="afe14-118">L’appareil peut effectuer des texgen.</span><span class="sxs-lookup"><span data-stu-id="afe14-118">Device can do texgen.</span></span>                                                                                                                                                                              |
| <span data-ttu-id="afe14-119">D3DVTXPCAPS \_ TEXGEN \_ SPHEREMAP</span><span class="sxs-lookup"><span data-stu-id="afe14-119">D3DVTXPCAPS\_TEXGEN\_SPHEREMAP</span></span>          | <span data-ttu-id="afe14-120">L’appareil prend en charge D3DTSS \_ TCI \_ SPHEREMAP.</span><span class="sxs-lookup"><span data-stu-id="afe14-120">Device supports D3DTSS\_TCI\_SPHEREMAP.</span></span>                                                                                                                                                            |
| <span data-ttu-id="afe14-121">\_Interpolation D3DVTXPCAPS</span><span class="sxs-lookup"><span data-stu-id="afe14-121">D3DVTXPCAPS\_TWEENING</span></span>                   | <span data-ttu-id="afe14-122">L’appareil peut effectuer l’interpolation des sommets.</span><span class="sxs-lookup"><span data-stu-id="afe14-122">Device can do vertex tweening.</span></span>                                                                                                                                                                     |



 

## <a name="constant-information"></a><span data-ttu-id="afe14-123">Informations constantes</span><span class="sxs-lookup"><span data-stu-id="afe14-123">Constant Information</span></span>



|                          |            |
|--------------------------|------------|
| <span data-ttu-id="afe14-124">En-tête</span><span class="sxs-lookup"><span data-stu-id="afe14-124">Header</span></span>                   | <span data-ttu-id="afe14-125">d3d9caps. h</span><span class="sxs-lookup"><span data-stu-id="afe14-125">d3d9caps.h</span></span> |
| <span data-ttu-id="afe14-126">Système d’exploitation minimal</span><span class="sxs-lookup"><span data-stu-id="afe14-126">Minimum operating system</span></span> | <span data-ttu-id="afe14-127">Windows 98</span><span class="sxs-lookup"><span data-stu-id="afe14-127">Windows 98</span></span> |



 

## <a name="related-topics"></a><span data-ttu-id="afe14-128">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="afe14-128">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="afe14-129">Constantes Direct3D</span><span class="sxs-lookup"><span data-stu-id="afe14-129">Direct3D Constants</span></span>](dx9-graphics-reference-d3d-constants.md)
</dt> </dl>

 

 



