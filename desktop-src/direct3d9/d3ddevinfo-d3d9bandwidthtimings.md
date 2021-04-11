---
description: Les métriques de débit pour vous aider à comprendre les performances d’une application.
ms.assetid: c0bcf060-a0ed-4c85-9554-398ffe4b4235
title: Structure D3DDEVINFO_D3D9BANDWIDTHTIMINGS (D3D9Types. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DDEVINFO_D3D9BANDWIDTHTIMINGS
api_type:
- HeaderDef
api_location:
- D3D9Types.h
ms.openlocfilehash: 3bfb98045e645f20fa77cf8523040b995f6c254a
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "104211721"
---
# <a name="d3ddevinfo_d3d9bandwidthtimings-structure"></a><span data-ttu-id="aaf53-103">D3DDEVINFO \_ D3D9BANDWIDTHTIMINGS, structure</span><span class="sxs-lookup"><span data-stu-id="aaf53-103">D3DDEVINFO\_D3D9BANDWIDTHTIMINGS structure</span></span>

<span data-ttu-id="aaf53-104">Les métriques de débit pour vous aider à comprendre les performances d’une application.</span><span class="sxs-lookup"><span data-stu-id="aaf53-104">Throughput metrics for help in understanding the performance of an application.</span></span>

## <a name="syntax"></a><span data-ttu-id="aaf53-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="aaf53-105">Syntax</span></span>


```C++
typedef struct D3DDEVINFO_D3D9BANDWIDTHTIMINGS {
  FLOAT MaxBandwidthUtilized;
  FLOAT FrontEndUploadMemoryUtilizedPercent;
  FLOAT VertexRateUtilizedPercent;
  FLOAT TriangleSetupRateUtilizedPercent;
  FLOAT FillRateUtilizedPercent;
} D3DDEVINFO_D3D9BANDWIDTHTIMINGS, *LPD3DDEVINFO_D3D9BANDWIDTHTIMINGS;
```



## <a name="members"></a><span data-ttu-id="aaf53-106">Membres</span><span class="sxs-lookup"><span data-stu-id="aaf53-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="aaf53-107">**MaxBandwidthUtilized**</span><span class="sxs-lookup"><span data-stu-id="aaf53-107">**MaxBandwidthUtilized**</span></span>
</dt> <dd>

<span data-ttu-id="aaf53-108">Type : **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="aaf53-108">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="aaf53-109">La bande passante ou le taux de transfert de données maximal du processeur de l’ordinateur hôte vers le GPU.</span><span class="sxs-lookup"><span data-stu-id="aaf53-109">The bandwidth or maximum data transfer rate from the host CPU to the GPU.</span></span> <span data-ttu-id="aaf53-110">Il s’agit généralement de la bande passante du bus PCI ou AGP qui connecte l’UC et le GPU.</span><span class="sxs-lookup"><span data-stu-id="aaf53-110">This is typically the bandwidth of the PCI or AGP bus which connects the CPU and the GPU.</span></span>

</dd> <dt>

<span data-ttu-id="aaf53-111">**FrontEndUploadMemoryUtilizedPercent**</span><span class="sxs-lookup"><span data-stu-id="aaf53-111">**FrontEndUploadMemoryUtilizedPercent**</span></span>
</dt> <dd>

<span data-ttu-id="aaf53-112">Type : **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="aaf53-112">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="aaf53-113">Pourcentage d’utilisation de la mémoire lors du chargement des données du processeur de l’ordinateur hôte vers le GPU.</span><span class="sxs-lookup"><span data-stu-id="aaf53-113">Memory utilized percentage when uploading data from the host CPU to the GPU.</span></span>

</dd> <dt>

<span data-ttu-id="aaf53-114">**VertexRateUtilizedPercent**</span><span class="sxs-lookup"><span data-stu-id="aaf53-114">**VertexRateUtilizedPercent**</span></span>
</dt> <dd>

<span data-ttu-id="aaf53-115">Type : **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="aaf53-115">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="aaf53-116">Pourcentage du débit du vertex.</span><span class="sxs-lookup"><span data-stu-id="aaf53-116">Vertex throughput percentage.</span></span> <span data-ttu-id="aaf53-117">Il s’agit du nombre de vertex traités par rapport au taux de traitement de vertex maximal théorique.</span><span class="sxs-lookup"><span data-stu-id="aaf53-117">This is the number of vertices processed compared to the theoretical maximum vertex processing rate.</span></span>

</dd> <dt>

<span data-ttu-id="aaf53-118">**TriangleSetupRateUtilizedPercent**</span><span class="sxs-lookup"><span data-stu-id="aaf53-118">**TriangleSetupRateUtilizedPercent**</span></span>
</dt> <dd>

<span data-ttu-id="aaf53-119">Type : **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="aaf53-119">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="aaf53-120">Pourcentage de débit de paramétrage des triangles.</span><span class="sxs-lookup"><span data-stu-id="aaf53-120">Triangle set-up throughput percentage.</span></span> <span data-ttu-id="aaf53-121">Il s’agit du nombre de triangles qui sont configurés pour la pixellisation par rapport au taux maximal de paramétrage du triangle théorique.</span><span class="sxs-lookup"><span data-stu-id="aaf53-121">This is the number of triangles that are set up for rasterization compared to the theoretical maximum triangle set-up rate.</span></span>

</dd> <dt>

<span data-ttu-id="aaf53-122">**FillRateUtilizedPercent**</span><span class="sxs-lookup"><span data-stu-id="aaf53-122">**FillRateUtilizedPercent**</span></span>
</dt> <dd>

<span data-ttu-id="aaf53-123">Type : **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="aaf53-123">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="aaf53-124">Pourcentage du débit de remplissage des pixels.</span><span class="sxs-lookup"><span data-stu-id="aaf53-124">Pixel fill throughput percentage.</span></span> <span data-ttu-id="aaf53-125">Il s’agit du nombre de pixels qui sont remplis par rapport au remplissage de pixel théorique.</span><span class="sxs-lookup"><span data-stu-id="aaf53-125">This is the number of pixels that are filled compared to the theoretical pixel fill.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="aaf53-126">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="aaf53-126">Requirements</span></span>



| <span data-ttu-id="aaf53-127">Condition requise</span><span class="sxs-lookup"><span data-stu-id="aaf53-127">Requirement</span></span> | <span data-ttu-id="aaf53-128">Valeur</span><span class="sxs-lookup"><span data-stu-id="aaf53-128">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="aaf53-129">En-tête</span><span class="sxs-lookup"><span data-stu-id="aaf53-129">Header</span></span><br/> | <dl> <span data-ttu-id="aaf53-130"><dt>D3D9Types. h</dt></span><span class="sxs-lookup"><span data-stu-id="aaf53-130"><dt>D3D9Types.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="aaf53-131">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="aaf53-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="aaf53-132">Structures Direct3D</span><span class="sxs-lookup"><span data-stu-id="aaf53-132">Direct3D Structures</span></span>](dx9-graphics-reference-d3d-structures.md)
</dt> <dt>

[<span data-ttu-id="aaf53-133">**GetData**</span><span class="sxs-lookup"><span data-stu-id="aaf53-133">**GetData**</span></span>](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dquery9-getdata)
</dt> </dl>

 

 
