---
description: Objet chargeant des données utilisé par l’interface ID3DX10ThreadPump pour le chargement des données de façon asynchrone.
ms.assetid: bda2414c-bbab-47ac-b23a-f58fb86e732d
title: Interface ID3DX10DataLoader (D3DX10. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DX10DataLoader
api_type:
- COM
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: b0e45d24d663f0ba9a8978bc251a4adf0c7868fd
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "103953864"
---
# <a name="id3dx10dataloader-interface"></a><span data-ttu-id="ddf52-103">Interface ID3DX10DataLoader</span><span class="sxs-lookup"><span data-stu-id="ddf52-103">ID3DX10DataLoader interface</span></span>

<span data-ttu-id="ddf52-104">Objet chargeant des données utilisé par l' [**interface ID3DX10ThreadPump**](id3dx10threadpump.md) pour le chargement des données de façon asynchrone.</span><span class="sxs-lookup"><span data-stu-id="ddf52-104">Data loading object used by [**ID3DX10ThreadPump Interface**](id3dx10threadpump.md) for loading data asynchronously.</span></span>

## <a name="members"></a><span data-ttu-id="ddf52-105">Membres</span><span class="sxs-lookup"><span data-stu-id="ddf52-105">Members</span></span>

<span data-ttu-id="ddf52-106">L’interface **ID3DX10DataLoader** hérite de l’interface [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) .</span><span class="sxs-lookup"><span data-stu-id="ddf52-106">The **ID3DX10DataLoader** interface inherits from the [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="ddf52-107">**ID3DX10DataLoader** a également les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="ddf52-107">**ID3DX10DataLoader** also has these types of members:</span></span>

-   [<span data-ttu-id="ddf52-108">Méthodes</span><span class="sxs-lookup"><span data-stu-id="ddf52-108">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="ddf52-109">Méthodes</span><span class="sxs-lookup"><span data-stu-id="ddf52-109">Methods</span></span>

<span data-ttu-id="ddf52-110">L’interface **ID3DX10DataLoader** possède ces méthodes.</span><span class="sxs-lookup"><span data-stu-id="ddf52-110">The **ID3DX10DataLoader** interface has these methods.</span></span>



| <span data-ttu-id="ddf52-111">Méthode</span><span class="sxs-lookup"><span data-stu-id="ddf52-111">Method</span></span>                                             | <span data-ttu-id="ddf52-112">Description</span><span class="sxs-lookup"><span data-stu-id="ddf52-112">Description</span></span>                                                                                                                                                                                                                        |
|:---------------------------------------------------|:-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="ddf52-113">**Décompresser**</span><span class="sxs-lookup"><span data-stu-id="ddf52-113">**Decompress**</span></span>](id3dx10dataloader-decompress.md) | <span data-ttu-id="ddf52-114">Utilisé pour décompresser des données encodées.</span><span class="sxs-lookup"><span data-stu-id="ddf52-114">Used to decompress encoded data.</span></span> <span data-ttu-id="ddf52-115">En général, cette valeur est utilisée pour charger des ressources à partir de systèmes de fichiers, tels que des fichiers ZIP.</span><span class="sxs-lookup"><span data-stu-id="ddf52-115">Typically this would be used to load resources from file systems, such as ZIP files.</span></span> <span data-ttu-id="ddf52-116">Lors du chargement à partir d’une ressource non compressée, l’étape de décompression n’a pas besoin d’effectuer de travail.</span><span class="sxs-lookup"><span data-stu-id="ddf52-116">When loading from an uncompressed resource, the decompression stage does not have to do any work.</span></span><br/> |
| [<span data-ttu-id="ddf52-117">**Suppression**</span><span class="sxs-lookup"><span data-stu-id="ddf52-117">**Destroy**</span></span>](id3dx10dataloader-destroy.md)       | <span data-ttu-id="ddf52-118">Utilisé par une [**interface ID3DX10ThreadPump**](id3dx10threadpump.md) pour détruire le chargeur après l’achèvement d’un élément de travail.</span><span class="sxs-lookup"><span data-stu-id="ddf52-118">Used by a [**ID3DX10ThreadPump Interface**](id3dx10threadpump.md) to destroy the loader after a work item completes.</span></span><br/>                                                                                                   |
| [<span data-ttu-id="ddf52-119">**Load**</span><span class="sxs-lookup"><span data-stu-id="ddf52-119">**Load**</span></span>](id3dx10dataloader-load.md)             | <span data-ttu-id="ddf52-120">Utilisé par une [**interface ID3DX10ThreadPump**](id3dx10threadpump.md) pour charger des données à partir d’un disque.</span><span class="sxs-lookup"><span data-stu-id="ddf52-120">Used by a [**ID3DX10ThreadPump Interface**](id3dx10threadpump.md) to load data from a disk.</span></span><br/>                                                                                                                            |



 

## <a name="remarks"></a><span data-ttu-id="ddf52-121">Notes</span><span class="sxs-lookup"><span data-stu-id="ddf52-121">Remarks</span></span>

<span data-ttu-id="ddf52-122">Cet objet peut être hérité et ses membres redéfinis.</span><span class="sxs-lookup"><span data-stu-id="ddf52-122">This object can be inherited and its members redefined.</span></span> <span data-ttu-id="ddf52-123">Cela vous permettrait de personnaliser l’API pour le chargement et la décompression de vos propres formats de fichiers personnalisés.</span><span class="sxs-lookup"><span data-stu-id="ddf52-123">Doing so would enable you to customize the API for loading and decompressing your own custom file formats.</span></span>

## <a name="requirements"></a><span data-ttu-id="ddf52-124">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="ddf52-124">Requirements</span></span>



| <span data-ttu-id="ddf52-125">Condition requise</span><span class="sxs-lookup"><span data-stu-id="ddf52-125">Requirement</span></span> | <span data-ttu-id="ddf52-126">Valeur</span><span class="sxs-lookup"><span data-stu-id="ddf52-126">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="ddf52-127">En-tête</span><span class="sxs-lookup"><span data-stu-id="ddf52-127">Header</span></span><br/>  | <dl> <span data-ttu-id="ddf52-128"><dt>D3DX10. h</dt></span><span class="sxs-lookup"><span data-stu-id="ddf52-128"><dt>D3DX10.h</dt></span></span> </dl>   |
| <span data-ttu-id="ddf52-129">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="ddf52-129">Library</span></span><br/> | <dl> <span data-ttu-id="ddf52-130"><dt>D3DX10. lib</dt></span><span class="sxs-lookup"><span data-stu-id="ddf52-130"><dt>D3DX10.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ddf52-131">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="ddf52-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ddf52-132">Interfaces D3DX</span><span class="sxs-lookup"><span data-stu-id="ddf52-132">D3DX Interfaces</span></span>](d3d10-graphics-reference-d3dx10-interfaces.md)
</dt> </dl>

 

 
