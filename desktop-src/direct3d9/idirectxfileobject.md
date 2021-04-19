---
description: Les applications utilisent les méthodes de l’interface IDirectXFileObject pour récupérer des informations sur les objets fichiers Microsoft DirectX. Action déconseillée.
ms.assetid: 015d2c4e-4a25-40da-b88a-bad0c4e20e09
title: Interface IDirectXFileObject (DXFile. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IDirectXFileObject
api_type:
- COM
api_location:
- d3dxof.lib
- d3dxof.dll
ms.openlocfilehash: e03f4a80c0cff25fa9416d35c20f2d60d17b206b
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "106539439"
---
# <a name="idirectxfileobject-interface"></a><span data-ttu-id="04df6-104">Interface IDirectXFileObject</span><span class="sxs-lookup"><span data-stu-id="04df6-104">IDirectXFileObject interface</span></span>

<span data-ttu-id="04df6-105">Les applications utilisent les méthodes de l’interface IDirectXFileObject pour récupérer des informations sur les objets fichiers Microsoft DirectX.</span><span class="sxs-lookup"><span data-stu-id="04df6-105">Applications use the methods of the IDirectXFileObject interface to retrieve information about Microsoft DirectX file objects.</span></span> <span data-ttu-id="04df6-106">Action déconseillée.</span><span class="sxs-lookup"><span data-stu-id="04df6-106">Deprecated.</span></span>

## <a name="members"></a><span data-ttu-id="04df6-107">Membres</span><span class="sxs-lookup"><span data-stu-id="04df6-107">Members</span></span>

<span data-ttu-id="04df6-108">L’interface **IDirectXFileObject** hérite de l’interface [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) .</span><span class="sxs-lookup"><span data-stu-id="04df6-108">The **IDirectXFileObject** interface inherits from the [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="04df6-109">**IDirectXFileObject** a également les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="04df6-109">**IDirectXFileObject** also has these types of members:</span></span>

-   [<span data-ttu-id="04df6-110">Méthodes</span><span class="sxs-lookup"><span data-stu-id="04df6-110">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="04df6-111">Méthodes</span><span class="sxs-lookup"><span data-stu-id="04df6-111">Methods</span></span>

<span data-ttu-id="04df6-112">L’interface **IDirectXFileObject** possède ces méthodes.</span><span class="sxs-lookup"><span data-stu-id="04df6-112">The **IDirectXFileObject** interface has these methods.</span></span>



| <span data-ttu-id="04df6-113">Méthode</span><span class="sxs-lookup"><span data-stu-id="04df6-113">Method</span></span>                                         | <span data-ttu-id="04df6-114">Description</span><span class="sxs-lookup"><span data-stu-id="04df6-114">Description</span></span>                                                                                   |
|:-----------------------------------------------|:----------------------------------------------------------------------------------------------|
| [<span data-ttu-id="04df6-115">**GetId**</span><span class="sxs-lookup"><span data-stu-id="04df6-115">**GetId**</span></span>](idirectxfileobject--getid.md)     | <span data-ttu-id="04df6-116">Récupère un pointeur vers le GUID qui identifie un objet fichier DirectX.</span><span class="sxs-lookup"><span data-stu-id="04df6-116">Retrieves a pointer to the GUID that identifies a DirectX file object.</span></span> <span data-ttu-id="04df6-117">Action déconseillée.</span><span class="sxs-lookup"><span data-stu-id="04df6-117">Deprecated.</span></span><br/> |
| [<span data-ttu-id="04df6-118">**GetName**</span><span class="sxs-lookup"><span data-stu-id="04df6-118">**GetName**</span></span>](idirectxfileobject--getname.md) | <span data-ttu-id="04df6-119">Récupère un pointeur vers le nom d’un objet de fichier DirectX.</span><span class="sxs-lookup"><span data-stu-id="04df6-119">Retrieves a pointer to a DirectX file object's name.</span></span> <span data-ttu-id="04df6-120">Action déconseillée.</span><span class="sxs-lookup"><span data-stu-id="04df6-120">Deprecated.</span></span><br/>                   |



 

## <a name="remarks"></a><span data-ttu-id="04df6-121">Notes</span><span class="sxs-lookup"><span data-stu-id="04df6-121">Remarks</span></span>

<span data-ttu-id="04df6-122">Le GUID de l’interface IDirectXFileObject est IID \_ IDirectXFileObject.</span><span class="sxs-lookup"><span data-stu-id="04df6-122">The GUID for the IDirectXFileObject interface is IID\_IDirectXFileObject.</span></span>

<span data-ttu-id="04df6-123">Le type LPDIRECTXFILEOBJECT est défini en tant que pointeur vers cette interface.</span><span class="sxs-lookup"><span data-stu-id="04df6-123">The LPDIRECTXFILEOBJECT type is defined as a pointer to this interface.</span></span>


```
typedef interface IDirectXFileObject *LPDIRECTXFILEOBJECT;
```



## <a name="requirements"></a><span data-ttu-id="04df6-124">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="04df6-124">Requirements</span></span>



| <span data-ttu-id="04df6-125">Condition requise</span><span class="sxs-lookup"><span data-stu-id="04df6-125">Requirement</span></span> | <span data-ttu-id="04df6-126">Valeur</span><span class="sxs-lookup"><span data-stu-id="04df6-126">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="04df6-127">En-tête</span><span class="sxs-lookup"><span data-stu-id="04df6-127">Header</span></span><br/>  | <dl> <span data-ttu-id="04df6-128"><dt>DXFile. h</dt></span><span class="sxs-lookup"><span data-stu-id="04df6-128"><dt>DXFile.h</dt></span></span> </dl>   |
| <span data-ttu-id="04df6-129">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="04df6-129">Library</span></span><br/> | <dl> <span data-ttu-id="04df6-130"><dt>D3dxof. lib</dt></span><span class="sxs-lookup"><span data-stu-id="04df6-130"><dt>D3dxof.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="04df6-131">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="04df6-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="04df6-132">X, interfaces de fichiers</span><span class="sxs-lookup"><span data-stu-id="04df6-132">X File Interfaces</span></span>](dx9-graphics-reference-x-file-interfaces.md)
</dt> </dl>

 

 
