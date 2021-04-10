---
description: Spécifie les éléments de données de maillage à ignorer de l’appareil. Utilisé avec ID3DX10Mesh ::D iscard.
ms.assetid: 8b3c22ab-1337-4a66-ae32-17bd1b73f624
title: Énumération D3DX10_MESH_DISCARD_FLAGS (D3DX10Mesh. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DX10_MESH_DISCARD_FLAGS
api_type:
- HeaderDef
api_location:
- D3DX10Mesh.h
ms.openlocfilehash: 6640834cf81bfa5e4b6263d3b3cfbb1181bb16c9
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "103953958"
---
# <a name="d3dx10_mesh_discard_flags-enumeration"></a><span data-ttu-id="5576d-104">\_ \_ Énumération d’indicateurs d3dx10 Mesh ignore \_</span><span class="sxs-lookup"><span data-stu-id="5576d-104">D3DX10\_MESH\_DISCARD\_FLAGS enumeration</span></span>

<span data-ttu-id="5576d-105">Spécifie les éléments de données de maillage à ignorer de l’appareil.</span><span class="sxs-lookup"><span data-stu-id="5576d-105">Specifies which pieces of mesh data to discard from the device.</span></span> <span data-ttu-id="5576d-106">Utilisé avec [**ID3DX10Mesh ::D iscard**](id3dx10mesh-discard.md).</span><span class="sxs-lookup"><span data-stu-id="5576d-106">Used with [**ID3DX10Mesh::Discard**](id3dx10mesh-discard.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="5576d-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="5576d-107">Syntax</span></span>


```C++
typedef enum D3DX10_MESH_DISCARD_FLAGS { 
  D3DX10_MESH_DISCARD_ATTRIBUTE_BUFFER  = 0x01,
  D3DX10_MESH_DISCARD_ATTRIBUTE_TABLE   = 0x02,
  D3DX10_MESH_DISCARD_POINTREPS         = 0x04,
  D3DX10_MESH_DISCARD_ADJACENCY         = 0x08,
  D3DX10_MESH_DISCARD_DEVICE_BUFFERS    = 0x10
} D3DX10_MESH_DISCARD_FLAGS, *LPD3DX10_MESH_DISCARD_FLAGS;
```



## <a name="constants"></a><span data-ttu-id="5576d-108">Constantes</span><span class="sxs-lookup"><span data-stu-id="5576d-108">Constants</span></span>

<dl> <dt>

<span data-ttu-id="5576d-109"><span id="D3DX10_MESH_DISCARD_ATTRIBUTE_BUFFER"></span><span id="d3dx10_mesh_discard_attribute_buffer"></span>**\_Tampon d' \_ attribut de rejet de maillage d3dx10 \_ \_**</span><span class="sxs-lookup"><span data-stu-id="5576d-109"><span id="D3DX10_MESH_DISCARD_ATTRIBUTE_BUFFER"></span><span id="d3dx10_mesh_discard_attribute_buffer"></span>**D3DX10\_MESH\_DISCARD\_ATTRIBUTE\_BUFFER**</span></span>
</dt> <dd>

<span data-ttu-id="5576d-110">Ignorer la mémoire tampon d’attribut.</span><span class="sxs-lookup"><span data-stu-id="5576d-110">Discard the attribute buffer.</span></span>

</dd> <dt>

<span data-ttu-id="5576d-111"><span id="D3DX10_MESH_DISCARD_ATTRIBUTE_TABLE"></span><span id="d3dx10_mesh_discard_attribute_table"></span>**\_Table d' \_ attributs de rejet de maillage d3dx10 \_ \_**</span><span class="sxs-lookup"><span data-stu-id="5576d-111"><span id="D3DX10_MESH_DISCARD_ATTRIBUTE_TABLE"></span><span id="d3dx10_mesh_discard_attribute_table"></span>**D3DX10\_MESH\_DISCARD\_ATTRIBUTE\_TABLE**</span></span>
</dt> <dd>

<span data-ttu-id="5576d-112">Ignorez la table d’attributs.</span><span class="sxs-lookup"><span data-stu-id="5576d-112">Discard the attribute table.</span></span>

</dd> <dt>

<span data-ttu-id="5576d-113"><span id="D3DX10_MESH_DISCARD_POINTREPS"></span><span id="d3dx10_mesh_discard_pointreps"></span>**D3DX10 \_ Mesh \_ Discard \_ POINTREPS**</span><span class="sxs-lookup"><span data-stu-id="5576d-113"><span id="D3DX10_MESH_DISCARD_POINTREPS"></span><span id="d3dx10_mesh_discard_pointreps"></span>**D3DX10\_MESH\_DISCARD\_POINTREPS**</span></span>
</dt> <dd>

<span data-ttu-id="5576d-114">Ignore la mémoire tampon des délégués du pointeur.</span><span class="sxs-lookup"><span data-stu-id="5576d-114">Discard the pointer reps buffer.</span></span>

</dd> <dt>

<span data-ttu-id="5576d-115"><span id="D3DX10_MESH_DISCARD_ADJACENCY"></span><span id="d3dx10_mesh_discard_adjacency"></span>**D3DX10 de l’écart de la \_ maille \_ \_**</span><span class="sxs-lookup"><span data-stu-id="5576d-115"><span id="D3DX10_MESH_DISCARD_ADJACENCY"></span><span id="d3dx10_mesh_discard_adjacency"></span>**D3DX10\_MESH\_DISCARD\_ADJACENCY**</span></span>
</dt> <dd>

<span data-ttu-id="5576d-116">Ignorer la mémoire tampon de contiguïté.</span><span class="sxs-lookup"><span data-stu-id="5576d-116">Discard the adjacency buffer.</span></span>

</dd> <dt>

<span data-ttu-id="5576d-117"><span id="D3DX10_MESH_DISCARD_DEVICE_BUFFERS"></span><span id="d3dx10_mesh_discard_device_buffers"></span>**\_Tampons de l’appareil d3dx10 Mesh \_ Discard \_ \_**</span><span class="sxs-lookup"><span data-stu-id="5576d-117"><span id="D3DX10_MESH_DISCARD_DEVICE_BUFFERS"></span><span id="d3dx10_mesh_discard_device_buffers"></span>**D3DX10\_MESH\_DISCARD\_DEVICE\_BUFFERS**</span></span>
</dt> <dd>

<span data-ttu-id="5576d-118">Ignorez les mémoires tampons validées sur l’appareil (avec [**ID3DX10Mesh :: CommitToDevice**](id3dx10mesh-committodevice.md)).</span><span class="sxs-lookup"><span data-stu-id="5576d-118">Discard the buffers committed to the device (with [**ID3DX10Mesh::CommitToDevice**](id3dx10mesh-committodevice.md)).</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="5576d-119">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="5576d-119">Requirements</span></span>



| <span data-ttu-id="5576d-120">Condition requise</span><span class="sxs-lookup"><span data-stu-id="5576d-120">Requirement</span></span> | <span data-ttu-id="5576d-121">Valeur</span><span class="sxs-lookup"><span data-stu-id="5576d-121">Value</span></span> |
|-------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="5576d-122">En-tête</span><span class="sxs-lookup"><span data-stu-id="5576d-122">Header</span></span><br/> | <dl> <span data-ttu-id="5576d-123"><dt>D3DX10Mesh. h</dt></span><span class="sxs-lookup"><span data-stu-id="5576d-123"><dt>D3DX10Mesh.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5576d-124">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="5576d-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5576d-125">Énumérations D3DX</span><span class="sxs-lookup"><span data-stu-id="5576d-125">D3DX Enumerations</span></span>](d3d10-graphics-reference-d3dx10-enums.md)
</dt> </dl>

 

 




