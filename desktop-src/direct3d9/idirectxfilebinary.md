---
description: Les applications utilisent les méthodes de l’interface IDirectXFileBinary pour lire et récupérer des informations sur les données binaires. Action déconseillée.
ms.assetid: 43b20ab3-67b2-4717-ad90-0bf4ddb3207e
title: Interface IDirectXFileBinary (DXFile. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IDirectXFileBinary
api_type:
- COM
api_location:
- d3dxof.lib
- d3dxof.dll
ms.openlocfilehash: b6707e4e685289f16b85ab85c2cce13dcd1da962
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "104211724"
---
# <a name="idirectxfilebinary-interface"></a><span data-ttu-id="c1106-104">Interface IDirectXFileBinary</span><span class="sxs-lookup"><span data-stu-id="c1106-104">IDirectXFileBinary interface</span></span>

<span data-ttu-id="c1106-105">Les applications utilisent les méthodes de l’interface IDirectXFileBinary pour lire et récupérer des informations sur les données binaires.</span><span class="sxs-lookup"><span data-stu-id="c1106-105">Applications use the methods of the IDirectXFileBinary interface to read and retrieve information about binary data.</span></span> <span data-ttu-id="c1106-106">Action déconseillée.</span><span class="sxs-lookup"><span data-stu-id="c1106-106">Deprecated.</span></span>

## <a name="members"></a><span data-ttu-id="c1106-107">Membres</span><span class="sxs-lookup"><span data-stu-id="c1106-107">Members</span></span>

<span data-ttu-id="c1106-108">L’interface **IDirectXFileBinary** hérite de [**IDirectXFileObject**](idirectxfileobject.md).</span><span class="sxs-lookup"><span data-stu-id="c1106-108">The **IDirectXFileBinary** interface inherits from [**IDirectXFileObject**](idirectxfileobject.md).</span></span> <span data-ttu-id="c1106-109">**IDirectXFileBinary** a également les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="c1106-109">**IDirectXFileBinary** also has these types of members:</span></span>

-   [<span data-ttu-id="c1106-110">Méthodes</span><span class="sxs-lookup"><span data-stu-id="c1106-110">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="c1106-111">Méthodes</span><span class="sxs-lookup"><span data-stu-id="c1106-111">Methods</span></span>

<span data-ttu-id="c1106-112">L’interface **IDirectXFileBinary** possède ces méthodes.</span><span class="sxs-lookup"><span data-stu-id="c1106-112">The **IDirectXFileBinary** interface has these methods.</span></span>



| <span data-ttu-id="c1106-113">Méthode</span><span class="sxs-lookup"><span data-stu-id="c1106-113">Method</span></span>                                                 | <span data-ttu-id="c1106-114">Description</span><span class="sxs-lookup"><span data-stu-id="c1106-114">Description</span></span>                                                                                                 |
|:-------------------------------------------------------|:------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="c1106-115">**GetMimeType**</span><span class="sxs-lookup"><span data-stu-id="c1106-115">**GetMimeType**</span></span>](idirectxfilebinary--getmimetype.md) | <span data-ttu-id="c1106-116">Récupère le type MIME (Multipurpose Internet Mail Extensions) pour les données binaires.</span><span class="sxs-lookup"><span data-stu-id="c1106-116">Retrieves the Multipurpose Internet Mail Extensions (MIME) type for the binary data.</span></span> <span data-ttu-id="c1106-117">Action déconseillée.</span><span class="sxs-lookup"><span data-stu-id="c1106-117">Deprecated.</span></span><br/> |
| [<span data-ttu-id="c1106-118">**GetSize,**</span><span class="sxs-lookup"><span data-stu-id="c1106-118">**GetSize**</span></span>](idirectxfilebinary--getsize.md)         | <span data-ttu-id="c1106-119">Récupère la taille des données binaires.</span><span class="sxs-lookup"><span data-stu-id="c1106-119">Retrieves the size of the binary data.</span></span> <span data-ttu-id="c1106-120">Action déconseillée.</span><span class="sxs-lookup"><span data-stu-id="c1106-120">Deprecated.</span></span><br/>                                               |
| [<span data-ttu-id="c1106-121">**En lecture**</span><span class="sxs-lookup"><span data-stu-id="c1106-121">**Read**</span></span>](idirectxfilebinary--read.md)               | <span data-ttu-id="c1106-122">Lit les données binaires.</span><span class="sxs-lookup"><span data-stu-id="c1106-122">Reads the binary data.</span></span> <span data-ttu-id="c1106-123">Action déconseillée.</span><span class="sxs-lookup"><span data-stu-id="c1106-123">Deprecated.</span></span><br/>                                                               |



 

## <a name="remarks"></a><span data-ttu-id="c1106-124">Notes</span><span class="sxs-lookup"><span data-stu-id="c1106-124">Remarks</span></span>

<span data-ttu-id="c1106-125">Le GUID de l’interface IDirectXFileBinary est IID \_ IDirectXFileBinary.</span><span class="sxs-lookup"><span data-stu-id="c1106-125">The GUID for the IDirectXFileBinary interface is IID\_IDirectXFileBinary.</span></span>

<span data-ttu-id="c1106-126">Le type LPDIRECTXFileBinary est défini en tant que pointeur vers cette interface.</span><span class="sxs-lookup"><span data-stu-id="c1106-126">The LPDIRECTXFileBinary type is defined as a pointer to this interface.</span></span>


```
typedef interface IDirectXFileBinary *LPDIRECTXFILEBINARY;
```



## <a name="requirements"></a><span data-ttu-id="c1106-127">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="c1106-127">Requirements</span></span>



| <span data-ttu-id="c1106-128">Condition requise</span><span class="sxs-lookup"><span data-stu-id="c1106-128">Requirement</span></span> | <span data-ttu-id="c1106-129">Valeur</span><span class="sxs-lookup"><span data-stu-id="c1106-129">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="c1106-130">En-tête</span><span class="sxs-lookup"><span data-stu-id="c1106-130">Header</span></span><br/>  | <dl> <span data-ttu-id="c1106-131"><dt>DXFile. h</dt></span><span class="sxs-lookup"><span data-stu-id="c1106-131"><dt>DXFile.h</dt></span></span> </dl>   |
| <span data-ttu-id="c1106-132">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="c1106-132">Library</span></span><br/> | <dl> <span data-ttu-id="c1106-133"><dt>D3dxof. lib</dt></span><span class="sxs-lookup"><span data-stu-id="c1106-133"><dt>D3dxof.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c1106-134">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="c1106-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c1106-135">**IDirectXFileObject**</span><span class="sxs-lookup"><span data-stu-id="c1106-135">**IDirectXFileObject**</span></span>](idirectxfileobject.md)
</dt> <dt>

[<span data-ttu-id="c1106-136">X, interfaces de fichiers</span><span class="sxs-lookup"><span data-stu-id="c1106-136">X File Interfaces</span></span>](dx9-graphics-reference-x-file-interfaces.md)
</dt> </dl>

 

 




