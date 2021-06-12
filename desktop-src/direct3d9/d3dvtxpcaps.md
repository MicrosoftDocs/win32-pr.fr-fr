---
description: En savoir plus sur une combinaison d’un ou plusieurs indicateurs qui contrôlent le comportement de création de l’appareil dans la constante D3DVTXPCAPS.
ms.assetid: 2d3e548f-8559-4a36-b814-6d598bead1d0
title: D3DVTXPCAPS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6b544f3e4a69de23607366832aca110e42c61d6d
ms.sourcegitcommit: 8f0a1d212dd154e8d94ab4c0e4ced053fa16823a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2021
ms.locfileid: "112011082"
---
# <a name="d3dvtxpcaps"></a><span data-ttu-id="a9787-103">D3DVTXPCAPS</span><span class="sxs-lookup"><span data-stu-id="a9787-103">D3DVTXPCAPS</span></span>

<span data-ttu-id="a9787-104">Combinaison d’un ou de plusieurs indicateurs qui contrôlent le comportement de création de l’appareil.</span><span class="sxs-lookup"><span data-stu-id="a9787-104">A combination of one or more flags that control the device create behavior.</span></span>



| <span data-ttu-id="a9787-105">\#définition</span><span class="sxs-lookup"><span data-stu-id="a9787-105">\#define</span></span>                                | <span data-ttu-id="a9787-106">Description</span><span class="sxs-lookup"><span data-stu-id="a9787-106">Description</span></span>                                                                                                                                                                                        |
|-----------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a9787-107">D3DVTXPCAPS \_ DIRECTIONALLIGHTS</span><span class="sxs-lookup"><span data-stu-id="a9787-107">D3DVTXPCAPS\_DIRECTIONALLIGHTS</span></span>          | <span data-ttu-id="a9787-108">L’appareil peut faire des lumières directionnelles.</span><span class="sxs-lookup"><span data-stu-id="a9787-108">Device can do directional lights.</span></span>                                                                                                                                                                  |
| <span data-ttu-id="a9787-109">D3DVTXPCAPS \_ LOCALVIEWER</span><span class="sxs-lookup"><span data-stu-id="a9787-109">D3DVTXPCAPS\_LOCALVIEWER</span></span>                | <span data-ttu-id="a9787-110">L’appareil peut effectuer une visionneuse locale.</span><span class="sxs-lookup"><span data-stu-id="a9787-110">Device can do local viewer.</span></span>                                                                                                                                                                        |
| <span data-ttu-id="a9787-111">D3DVTXPCAPS \_ MATERIALSOURCE7</span><span class="sxs-lookup"><span data-stu-id="a9787-111">D3DVTXPCAPS\_MATERIALSOURCE7</span></span>            | <span data-ttu-id="a9787-112">Lorsque cette limite est définie, l’appareil prend en charge les États de couleur : D3DRS \_ AMBIENTMATERIALSOURCE, D3DRS \_ DIFFUSEMATERIALSOURCE, D3DRS \_ EMISSIVEMATERIALSOURCE et D3DRS SPECULARMATERIALSOURCE \_ .</span><span class="sxs-lookup"><span data-stu-id="a9787-112">When this cap is set, the device supports the color material states: D3DRS\_AMBIENTMATERIALSOURCE, D3DRS\_DIFFUSEMATERIALSOURCE, D3DRS\_EMISSIVEMATERIALSOURCE, and D3DRS\_SPECULARMATERIALSOURCE.</span></span> |
| <span data-ttu-id="a9787-113">D3DVTXPCAPS \_ non \_ TEXGEN \_ NONLOCALVIEWER</span><span class="sxs-lookup"><span data-stu-id="a9787-113">D3DVTXPCAPS\_NO\_TEXGEN\_NONLOCALVIEWER</span></span> | <span data-ttu-id="a9787-114">L’appareil ne prend pas en charge la génération de texture en mode visionneuse non locale.</span><span class="sxs-lookup"><span data-stu-id="a9787-114">Device does not support texture generation in non-local viewer mode.</span></span>                                                                                                                               |
| <span data-ttu-id="a9787-115">D3DVTXPCAPS \_ POSITIONALLIGHTS</span><span class="sxs-lookup"><span data-stu-id="a9787-115">D3DVTXPCAPS\_POSITIONALLIGHTS</span></span>           | <span data-ttu-id="a9787-116">L’appareil peut effectuer des lumières de position (y compris un point et un point).</span><span class="sxs-lookup"><span data-stu-id="a9787-116">Device can do positional lights (includes point and spot).</span></span>                                                                                                                                         |
| <span data-ttu-id="a9787-117">D3DVTXPCAPS \_ TEXGEN</span><span class="sxs-lookup"><span data-stu-id="a9787-117">D3DVTXPCAPS\_TEXGEN</span></span>                     | <span data-ttu-id="a9787-118">L’appareil peut effectuer des texgen.</span><span class="sxs-lookup"><span data-stu-id="a9787-118">Device can do texgen.</span></span>                                                                                                                                                                              |
| <span data-ttu-id="a9787-119">D3DVTXPCAPS \_ TEXGEN \_ SPHEREMAP</span><span class="sxs-lookup"><span data-stu-id="a9787-119">D3DVTXPCAPS\_TEXGEN\_SPHEREMAP</span></span>          | <span data-ttu-id="a9787-120">L’appareil prend en charge D3DTSS \_ TCI \_ SPHEREMAP.</span><span class="sxs-lookup"><span data-stu-id="a9787-120">Device supports D3DTSS\_TCI\_SPHEREMAP.</span></span>                                                                                                                                                            |
| <span data-ttu-id="a9787-121">\_Interpolation D3DVTXPCAPS</span><span class="sxs-lookup"><span data-stu-id="a9787-121">D3DVTXPCAPS\_TWEENING</span></span>                   | <span data-ttu-id="a9787-122">L’appareil peut effectuer l’interpolation des sommets.</span><span class="sxs-lookup"><span data-stu-id="a9787-122">Device can do vertex tweening.</span></span>                                                                                                                                                                     |



 

## <a name="constant-information"></a><span data-ttu-id="a9787-123">Informations constantes</span><span class="sxs-lookup"><span data-stu-id="a9787-123">Constant Information</span></span>



| <span data-ttu-id="a9787-124">Condition requise</span><span class="sxs-lookup"><span data-stu-id="a9787-124">Requirement</span></span>                         | <span data-ttu-id="a9787-125">Valeur</span><span class="sxs-lookup"><span data-stu-id="a9787-125">Value</span></span>           |
|--------------------------|------------|
| <span data-ttu-id="a9787-126">En-tête</span><span class="sxs-lookup"><span data-stu-id="a9787-126">Header</span></span>                   | <span data-ttu-id="a9787-127">d3d9caps. h</span><span class="sxs-lookup"><span data-stu-id="a9787-127">d3d9caps.h</span></span> |
| <span data-ttu-id="a9787-128">Système d’exploitation minimal</span><span class="sxs-lookup"><span data-stu-id="a9787-128">Minimum operating system</span></span> | <span data-ttu-id="a9787-129">Windows 98</span><span class="sxs-lookup"><span data-stu-id="a9787-129">Windows 98</span></span> |



 

## <a name="related-topics"></a><span data-ttu-id="a9787-130">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="a9787-130">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="a9787-131">Constantes Direct3D</span><span class="sxs-lookup"><span data-stu-id="a9787-131">Direct3D Constants</span></span>](dx9-graphics-reference-d3d-constants.md)
</dt> </dl>

 

 



