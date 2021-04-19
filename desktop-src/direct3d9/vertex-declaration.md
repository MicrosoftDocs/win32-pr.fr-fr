---
description: Une déclaration de vertex définit la disposition de la mémoire tampon du vertex et programme le moteur de pavage.
ms.assetid: 09dae498-3b33-4c33-bc7e-47f2bf784e4c
title: Déclaration de vertex (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c769aa6fb80de1fd83067ebb9f32b591baa8e883
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/06/2021
ms.locfileid: "106516740"
---
# <a name="vertex-declaration-direct3d-9"></a><span data-ttu-id="042e9-103">Déclaration de vertex (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="042e9-103">Vertex Declaration (Direct3D 9)</span></span>

<span data-ttu-id="042e9-104">Une déclaration de vertex définit la disposition de la mémoire tampon du vertex et programme le moteur de pavage.</span><span class="sxs-lookup"><span data-stu-id="042e9-104">A vertex declaration defines the vertex buffer layout and programs the tessellation engine.</span></span> <span data-ttu-id="042e9-105">À compter de Direct3D 9, les flux vertex sont exprimés sous la forme d’un tableau de structures [**D3DVERTEXELEMENT9**](d3dvertexelement9.md) (au lieu d’utiliser des codes de format de vertex flexible).</span><span class="sxs-lookup"><span data-stu-id="042e9-105">Starting with Direct3D 9, vertex streams are expressed as an array of [**D3DVERTEXELEMENT9**](d3dvertexelement9.md) structures (instead of using flexible vertex format (FVF) codes).</span></span> <span data-ttu-id="042e9-106">Chaque élément de tableau décrit chaque type de données par vertex.</span><span class="sxs-lookup"><span data-stu-id="042e9-106">Each array element describes each per-vertex data type.</span></span> <span data-ttu-id="042e9-107">La conversion des codes de> de la Commission dans le nouveau format est traitée dans les rubriques suivantes :</span><span class="sxs-lookup"><span data-stu-id="042e9-107">Converting FVF> codes into the new format is covered in the following topics:</span></span>

-   [<span data-ttu-id="042e9-108">Mappage de codes de la Commission des prix à une déclaration Direct3D 9 (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="042e9-108">Mapping FVF Codes to a Direct3D 9 Declaration (Direct3D 9)</span></span>](mapping-fvf-codes-to-a-directx-9-declaration.md)
-   [<span data-ttu-id="042e9-109">Correction des codes de fonction de la Commission (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="042e9-109">Fixed Function FVF Codes (Direct3D 9)</span></span>](fixed-function-fvf-codes.md)
-   [<span data-ttu-id="042e9-110">Mappage entre une déclaration Direct3D et les codes de la Commission de la Commission (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="042e9-110">Mapping between a Direct3D Declaration and FVF Codes (Direct3D 9)</span></span>](mapping-between-a-directx-9-declaration-and-fvf-codes.md)
-   [<span data-ttu-id="042e9-111">Mappage entre une déclaration Direct3D 9 et une déclaration Direct3D 8 (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="042e9-111">Mapping between a Direct3D 9 Declaration and a Direct3D 8 Declaration (Direct3D 9)</span></span>](mapping-between-a-directx-9-declaration-and-directx-8.md)
-   [<span data-ttu-id="042e9-112">Programmation d’un ou plusieurs flux (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="042e9-112">Programming One or More Streams (Direct3D 9)</span></span>](programming-one-or-more-streams.md)

## <a name="related-topics"></a><span data-ttu-id="042e9-113">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="042e9-113">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="042e9-114">Mémoires tampons de vertex</span><span class="sxs-lookup"><span data-stu-id="042e9-114">Vertex Buffers</span></span>](vertex-buffers.md)
</dt> </dl>

 

 



