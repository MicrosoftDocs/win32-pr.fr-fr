---
description: L’interface ID3DXBuffer est utilisée comme mémoire tampon de données, en stockant les informations de vertex, d’adjacence et de matériau pendant les opérations d’optimisation et de chargement du maillage.
ms.assetid: 63ee3b2d-c0e6-4ad4-9274-2b1dfd77f89d
title: Interface ID3DXBuffer (D3DX9Mesh. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXBuffer
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 5fff273d2e38daeb003fb360f099e7a7b4985504
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "106539450"
---
# <a name="id3dxbuffer-interface"></a><span data-ttu-id="e9f8d-103">Interface ID3DXBuffer</span><span class="sxs-lookup"><span data-stu-id="e9f8d-103">ID3DXBuffer interface</span></span>

<span data-ttu-id="e9f8d-104">L’interface ID3DXBuffer est utilisée comme mémoire tampon de données, en stockant les informations de vertex, d’adjacence et de matériau pendant les opérations d’optimisation et de chargement du maillage.</span><span class="sxs-lookup"><span data-stu-id="e9f8d-104">The ID3DXBuffer interface is used as a data buffer, storing vertex, adjacency, and material information during mesh optimization and loading operations.</span></span> <span data-ttu-id="e9f8d-105">L’objet buffer est utilisé pour retourner des données de longueur arbitraire.</span><span class="sxs-lookup"><span data-stu-id="e9f8d-105">The buffer object is used to return arbitrary length data.</span></span> <span data-ttu-id="e9f8d-106">En outre, les objets de mémoire tampon sont utilisés pour retourner le code objet et les messages d’erreur dans les méthodes qui assemblent des nuanceurs vertex et de pixels.</span><span class="sxs-lookup"><span data-stu-id="e9f8d-106">Also, buffer objects are used to return object code and error messages in methods that assemble vertex and pixel shaders.</span></span>

## <a name="members"></a><span data-ttu-id="e9f8d-107">Membres</span><span class="sxs-lookup"><span data-stu-id="e9f8d-107">Members</span></span>

<span data-ttu-id="e9f8d-108">L’interface **ID3DXBuffer** hérite de l’interface [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) .</span><span class="sxs-lookup"><span data-stu-id="e9f8d-108">The **ID3DXBuffer** interface inherits from the [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="e9f8d-109">**ID3DXBuffer** a également les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="e9f8d-109">**ID3DXBuffer** also has these types of members:</span></span>

-   [<span data-ttu-id="e9f8d-110">Méthodes</span><span class="sxs-lookup"><span data-stu-id="e9f8d-110">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="e9f8d-111">Méthodes</span><span class="sxs-lookup"><span data-stu-id="e9f8d-111">Methods</span></span>

<span data-ttu-id="e9f8d-112">L’interface **ID3DXBuffer** possède ces méthodes.</span><span class="sxs-lookup"><span data-stu-id="e9f8d-112">The **ID3DXBuffer** interface has these methods.</span></span>



| <span data-ttu-id="e9f8d-113">Méthode</span><span class="sxs-lookup"><span data-stu-id="e9f8d-113">Method</span></span>                                                    | <span data-ttu-id="e9f8d-114">Description</span><span class="sxs-lookup"><span data-stu-id="e9f8d-114">Description</span></span>                                                    |
|:----------------------------------------------------------|:---------------------------------------------------------------|
| [<span data-ttu-id="e9f8d-115">**GetBufferPointer**</span><span class="sxs-lookup"><span data-stu-id="e9f8d-115">**GetBufferPointer**</span></span>](id3dxbuffer--getbufferpointer.md) | <span data-ttu-id="e9f8d-116">Récupère un pointeur vers les données dans la mémoire tampon.</span><span class="sxs-lookup"><span data-stu-id="e9f8d-116">Retrieves a pointer to the data in the buffer.</span></span><br/>      |
| [<span data-ttu-id="e9f8d-117">**GetBufferSize**</span><span class="sxs-lookup"><span data-stu-id="e9f8d-117">**GetBufferSize**</span></span>](id3dxbuffer--getbuffersize.md)       | <span data-ttu-id="e9f8d-118">Récupère la taille totale des données dans la mémoire tampon.</span><span class="sxs-lookup"><span data-stu-id="e9f8d-118">Retrieves the total size of the data in the buffer.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="e9f8d-119">Notes</span><span class="sxs-lookup"><span data-stu-id="e9f8d-119">Remarks</span></span>

<span data-ttu-id="e9f8d-120">L’interface **ID3DXBuffer** est obtenue en appelant la fonction [**D3DXCreateBuffer**](d3dxcreatebuffer.md) .</span><span class="sxs-lookup"><span data-stu-id="e9f8d-120">The **ID3DXBuffer** interface is obtained by calling the [**D3DXCreateBuffer**](d3dxcreatebuffer.md) function.</span></span>

<span data-ttu-id="e9f8d-121">Le type LPD3DXBUFFER est défini comme un pointeur vers l’interface **ID3DXBuffer** .</span><span class="sxs-lookup"><span data-stu-id="e9f8d-121">The LPD3DXBUFFER type is defined as a pointer to the **ID3DXBuffer** interface.</span></span>


```
typedef interface ID3DXBuffer ID3DXBuffer;
typedef interface ID3DXBuffer *LPD3DXBUFFER;
```



## <a name="requirements"></a><span data-ttu-id="e9f8d-122">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="e9f8d-122">Requirements</span></span>



| <span data-ttu-id="e9f8d-123">Condition requise</span><span class="sxs-lookup"><span data-stu-id="e9f8d-123">Requirement</span></span> | <span data-ttu-id="e9f8d-124">Valeur</span><span class="sxs-lookup"><span data-stu-id="e9f8d-124">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="e9f8d-125">En-tête</span><span class="sxs-lookup"><span data-stu-id="e9f8d-125">Header</span></span><br/>  | <dl> <span data-ttu-id="e9f8d-126"><dt>D3DX9Mesh. h</dt></span><span class="sxs-lookup"><span data-stu-id="e9f8d-126"><dt>D3DX9Mesh.h</dt></span></span> </dl> |
| <span data-ttu-id="e9f8d-127">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="e9f8d-127">Library</span></span><br/> | <dl> <span data-ttu-id="e9f8d-128"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="e9f8d-128"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="e9f8d-129">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="e9f8d-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e9f8d-130">Interfaces D3DX</span><span class="sxs-lookup"><span data-stu-id="e9f8d-130">D3DX Interfaces</span></span>](dx9-graphics-reference-d3dx-interfaces.md)
</dt> </dl>

 

 
