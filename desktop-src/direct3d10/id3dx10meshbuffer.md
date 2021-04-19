---
description: Une mémoire tampon de maillage est une mémoire tampon qui contient les données relatives à un maillage.
ms.assetid: a9fdfa22-531d-4da0-89f0-8766c2635e20
title: Interface ID3DX10MeshBuffer (D3DX10. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DX10MeshBuffer
api_type:
- COM
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: 42076393c3be5443688ec4db954131935b62f696
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "106545285"
---
# <a name="id3dx10meshbuffer-interface"></a><span data-ttu-id="28ff0-103">Interface ID3DX10MeshBuffer</span><span class="sxs-lookup"><span data-stu-id="28ff0-103">ID3DX10MeshBuffer interface</span></span>

<span data-ttu-id="28ff0-104">Une mémoire tampon de maillage est une mémoire tampon qui contient les données relatives à un maillage.</span><span class="sxs-lookup"><span data-stu-id="28ff0-104">A mesh buffer is a buffer that contains data about a mesh.</span></span> <span data-ttu-id="28ff0-105">Il peut contenir l’un des cinq types de données suivants : les données de vertex, les données d’index, les données d’contiguïté, les données d’attribut ou les données de point Rep.</span><span class="sxs-lookup"><span data-stu-id="28ff0-105">It can contain one of five different types of data: vertex data, index data, adjacency data, attribute data, or point rep data.</span></span> <span data-ttu-id="28ff0-106">La structure est utilisée pour accéder à ces cinq éléments de données par le biais des cinq API suivantes : [**ID3DX10Mesh :: GetVertexBuffer**](id3dx10mesh-getvertexbuffer.md), [**ID3DX10Mesh :: GetIndexBuffer**](id3dx10mesh-getindexbuffer.md), [**ID3DX10Mesh :: GetAdjacencyBuffer**](id3dx10mesh-getadjacencybuffer.md), [**ID3DX10Mesh :: GetAttributeBuffer**](id3dx10mesh-getattributebuffer.md)ou [**ID3DX10Mesh :: GetPointRepBuffer**](id3dx10mesh-getpointrepbuffer.md).</span><span class="sxs-lookup"><span data-stu-id="28ff0-106">The structure is used to access these five pieces of data through the following five APIs: [**ID3DX10Mesh::GetVertexBuffer**](id3dx10mesh-getvertexbuffer.md), [**ID3DX10Mesh::GetIndexBuffer**](id3dx10mesh-getindexbuffer.md), [**ID3DX10Mesh::GetAdjacencyBuffer**](id3dx10mesh-getadjacencybuffer.md), [**ID3DX10Mesh::GetAttributeBuffer**](id3dx10mesh-getattributebuffer.md), or [**ID3DX10Mesh::GetPointRepBuffer**](id3dx10mesh-getpointrepbuffer.md).</span></span>

## <a name="members"></a><span data-ttu-id="28ff0-107">Membres</span><span class="sxs-lookup"><span data-stu-id="28ff0-107">Members</span></span>

<span data-ttu-id="28ff0-108">L’interface **ID3DX10MeshBuffer** hérite de l’interface [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) .</span><span class="sxs-lookup"><span data-stu-id="28ff0-108">The **ID3DX10MeshBuffer** interface inherits from the [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="28ff0-109">**ID3DX10MeshBuffer** a également les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="28ff0-109">**ID3DX10MeshBuffer** also has these types of members:</span></span>

-   [<span data-ttu-id="28ff0-110">Méthodes</span><span class="sxs-lookup"><span data-stu-id="28ff0-110">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="28ff0-111">Méthodes</span><span class="sxs-lookup"><span data-stu-id="28ff0-111">Methods</span></span>

<span data-ttu-id="28ff0-112">L’interface **ID3DX10MeshBuffer** possède ces méthodes.</span><span class="sxs-lookup"><span data-stu-id="28ff0-112">The **ID3DX10MeshBuffer** interface has these methods.</span></span>



| <span data-ttu-id="28ff0-113">Méthode</span><span class="sxs-lookup"><span data-stu-id="28ff0-113">Method</span></span>                                       | <span data-ttu-id="28ff0-114">Description</span><span class="sxs-lookup"><span data-stu-id="28ff0-114">Description</span></span>                                                                |
|:---------------------------------------------|:---------------------------------------------------------------------------|
| [<span data-ttu-id="28ff0-115">**GetSize,**</span><span class="sxs-lookup"><span data-stu-id="28ff0-115">**GetSize**</span></span>](id3dx10meshbuffer-getsize.md) | <span data-ttu-id="28ff0-116">Obtient la taille de la mémoire tampon de maillage, en octets.</span><span class="sxs-lookup"><span data-stu-id="28ff0-116">Get the size of the mesh buffer, in bytes.</span></span><br/>                      |
| [<span data-ttu-id="28ff0-117">**Canal**</span><span class="sxs-lookup"><span data-stu-id="28ff0-117">**Map**</span></span>](id3dx10meshbuffer-map.md)         | <span data-ttu-id="28ff0-118">Obtient un pointeur vers la mémoire tampon de maillage pour modifier son contenu.</span><span class="sxs-lookup"><span data-stu-id="28ff0-118">Get a pointer to the mesh buffer memory to modify its contents.</span></span><br/> |
| [<span data-ttu-id="28ff0-119">**Unmap**</span><span class="sxs-lookup"><span data-stu-id="28ff0-119">**Unmap**</span></span>](id3dx10meshbuffer-unmap.md)     | <span data-ttu-id="28ff0-120">Annuler le mappage d’une mémoire tampon.</span><span class="sxs-lookup"><span data-stu-id="28ff0-120">Unmap a buffer.</span></span><br/>                                                 |



 

## <a name="requirements"></a><span data-ttu-id="28ff0-121">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="28ff0-121">Requirements</span></span>



| <span data-ttu-id="28ff0-122">Condition requise</span><span class="sxs-lookup"><span data-stu-id="28ff0-122">Requirement</span></span> | <span data-ttu-id="28ff0-123">Valeur</span><span class="sxs-lookup"><span data-stu-id="28ff0-123">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="28ff0-124">En-tête</span><span class="sxs-lookup"><span data-stu-id="28ff0-124">Header</span></span><br/>  | <dl> <span data-ttu-id="28ff0-125"><dt>D3DX10. h</dt></span><span class="sxs-lookup"><span data-stu-id="28ff0-125"><dt>D3DX10.h</dt></span></span> </dl>   |
| <span data-ttu-id="28ff0-126">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="28ff0-126">Library</span></span><br/> | <dl> <span data-ttu-id="28ff0-127"><dt>D3DX10. lib</dt></span><span class="sxs-lookup"><span data-stu-id="28ff0-127"><dt>D3DX10.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="28ff0-128">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="28ff0-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="28ff0-129">Interfaces D3DX</span><span class="sxs-lookup"><span data-stu-id="28ff0-129">D3DX Interfaces</span></span>](d3d10-graphics-reference-d3dx10-interfaces.md)
</dt> </dl>

 

 
