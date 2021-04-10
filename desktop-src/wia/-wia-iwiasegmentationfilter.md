---
description: L’interface IWiaSegmentationFilter détecte les sous-régions d’un flux d’image et crée des éléments IWiaItem2 distincts pour chacun.
ms.assetid: eb7f1284-ab98-4d86-8b30-7abd504cee12
title: Interface IWiaSegmentationFilter (WIA. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWiaSegmentationFilter
api_type:
- COM
api_location:
- Wia.h
ms.openlocfilehash: b9c0bcdee5b40c37fb38b390f5085fe275f0f660
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103862674"
---
# <a name="iwiasegmentationfilter-interface"></a><span data-ttu-id="7e17a-103">Interface IWiaSegmentationFilter</span><span class="sxs-lookup"><span data-stu-id="7e17a-103">IWiaSegmentationFilter interface</span></span>

<span data-ttu-id="7e17a-104">L’interface **IWiaSegmentationFilter** détecte les sous-régions d’un flux d’image et crée des éléments [**IWiaItem2**](-wia-iwiaitem2.md) distincts pour chacun.</span><span class="sxs-lookup"><span data-stu-id="7e17a-104">The **IWiaSegmentationFilter** interface detects sub-regions of an image stream and makes separate [**IWiaItem2**](-wia-iwiaitem2.md) items for each.</span></span>

## <a name="members"></a><span data-ttu-id="7e17a-105">Membres</span><span class="sxs-lookup"><span data-stu-id="7e17a-105">Members</span></span>

<span data-ttu-id="7e17a-106">L’interface **IWiaSegmentationFilter** hérite de l’interface [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) .</span><span class="sxs-lookup"><span data-stu-id="7e17a-106">The **IWiaSegmentationFilter** interface inherits from the [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="7e17a-107">**IWiaSegmentationFilter** a également les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="7e17a-107">**IWiaSegmentationFilter** also has these types of members:</span></span>

-   [<span data-ttu-id="7e17a-108">Méthodes</span><span class="sxs-lookup"><span data-stu-id="7e17a-108">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="7e17a-109">Méthodes</span><span class="sxs-lookup"><span data-stu-id="7e17a-109">Methods</span></span>

<span data-ttu-id="7e17a-110">L’interface **IWiaSegmentationFilter** possède ces méthodes.</span><span class="sxs-lookup"><span data-stu-id="7e17a-110">The **IWiaSegmentationFilter** interface has these methods.</span></span>



| <span data-ttu-id="7e17a-111">Méthode</span><span class="sxs-lookup"><span data-stu-id="7e17a-111">Method</span></span>                                                             | <span data-ttu-id="7e17a-112">Description</span><span class="sxs-lookup"><span data-stu-id="7e17a-112">Description</span></span>                                                                                                                                              |
|:-------------------------------------------------------------------|:---------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="7e17a-113">**DetectRegions**</span><span class="sxs-lookup"><span data-stu-id="7e17a-113">**DetectRegions**</span></span>](-wia-iwiasegmentationfilter-detectregions.md) | <span data-ttu-id="7e17a-114">Détermine les sous-régions d’une image disposées sur le plateau à plat afin que chacune des sous-régions puisse être acquise dans un élément d’image séparé.</span><span class="sxs-lookup"><span data-stu-id="7e17a-114">Determines the sub-regions of an image laid out on the flatbed platen so that each of sub-region can be acquired into a separate image item.</span></span> <br/> |



 

## <a name="remarks"></a><span data-ttu-id="7e17a-115">Notes</span><span class="sxs-lookup"><span data-stu-id="7e17a-115">Remarks</span></span>

<span data-ttu-id="7e17a-116">Une application doit utiliser [**IWiaItem2 :: GetExtension**](-wia-iwiaitem2-getextension.md) pour créer une nouvelle instance du filtre de segmentation.</span><span class="sxs-lookup"><span data-stu-id="7e17a-116">An application should use [**IWiaItem2::GetExtension**](-wia-iwiaitem2-getextension.md) to create a new instance of the segmentation filter.</span></span> <span data-ttu-id="7e17a-117">Une application appelle généralement cette fonction avant d’afficher sa fenêtre d’aperçu.</span><span class="sxs-lookup"><span data-stu-id="7e17a-117">An application typically calls this function before displaying its preview window.</span></span>

<span data-ttu-id="7e17a-118">Lors de l’implémentation de ce filtre, utilisez [**IWiaItem2 :: CreateChildItem**](-wia-iwiaitem2-createchilditem.md) pour créer les éléments enfants.</span><span class="sxs-lookup"><span data-stu-id="7e17a-118">When implementing this filter, use [**IWiaItem2::CreateChildItem**](-wia-iwiaitem2-createchilditem.md) to create the child items.</span></span> <span data-ttu-id="7e17a-119">L’application doit passer **des \_ \_ \_ valeurs de propriétés parentes de copie** au paramètre *ICreationFlags* pour garantir que les propriétés telles que le format et la résolution d’image sont les mêmes dans l’enfant nouvellement créé, comme dans l’élément parent.</span><span class="sxs-lookup"><span data-stu-id="7e17a-119">The application should pass **COPY\_PARENT\_PROPERTY\_VALUES** to the *ICreationFlags* parameter to ensure that properties such as image format and resolution is the same in the newly created child as in the parent item.</span></span>

<span data-ttu-id="7e17a-120">Un filtre de segmentation doit prendre en charge tous les formats d’image pris en charge par le pilote qu’il utilise.</span><span class="sxs-lookup"><span data-stu-id="7e17a-120">A segmentation filter must support all the image formats that the driver it is used with supports.</span></span> <span data-ttu-id="7e17a-121">Le filtre fourni par Microsoft prend en charge les bitmaps (BMP), GIF (Graphics Interchange Format), JPEG, PNG (Portable Network Graphics) et TIFF (Tagged Image File Format).</span><span class="sxs-lookup"><span data-stu-id="7e17a-121">The Microsoft provided filter supports bitmap (BMP), Graphics Interchange Format (GIF), JPEG, Portable Network Graphics (PNG), and Tagged Image File Format (TIFF).</span></span>

<span data-ttu-id="7e17a-122">Le filtre de segmentation doit être utilisé uniquement sur les éléments du scanneur et du film.</span><span class="sxs-lookup"><span data-stu-id="7e17a-122">The segmentation filter should be used only on film and flatbed scanner items.</span></span> <span data-ttu-id="7e17a-123">Pour l’analyse des films, un scanneur est souvent accompagné d’images fixes. dans ce cas, le pilote a créé les éléments enfants et l’application ne doit pas appeler le filtre de segmentation.</span><span class="sxs-lookup"><span data-stu-id="7e17a-123">For film scanning, a scanner often comes with fixed frames in which case the driver created the child items and the application should not invoke the segmentation filter.</span></span>

<span data-ttu-id="7e17a-124">L’interface **IWiaSegmentationFilter** , comme toutes les interfaces COM (Component Object Model), hérite des méthodes d’interface [IUnknown](/windows/win32/api/unknwn/nn-unknwn-iunknown) .</span><span class="sxs-lookup"><span data-stu-id="7e17a-124">The **IWiaSegmentationFilter** interface, like all Component Object Model (COM) interfaces, inherits the [IUnknown](/windows/win32/api/unknwn/nn-unknwn-iunknown) interface methods.</span></span>



| <span data-ttu-id="7e17a-125">Méthodes IUnknown</span><span class="sxs-lookup"><span data-stu-id="7e17a-125">IUnknown Methods</span></span>                                        | <span data-ttu-id="7e17a-126">Description</span><span class="sxs-lookup"><span data-stu-id="7e17a-126">Description</span></span>                               |
|---------------------------------------------------------|-------------------------------------------|
| <span data-ttu-id="7e17a-127">[IUnknown :: QueryInterface](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q))</span><span class="sxs-lookup"><span data-stu-id="7e17a-127">[IUnknown::QueryInterface](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q))</span></span> | <span data-ttu-id="7e17a-128">Retourne des pointeurs aux interfaces prises en charge.</span><span class="sxs-lookup"><span data-stu-id="7e17a-128">Returns pointers to supported interfaces.</span></span> |
| [<span data-ttu-id="7e17a-129">IUnknown :: AddRef</span><span class="sxs-lookup"><span data-stu-id="7e17a-129">IUnknown::AddRef</span></span>](/windows/win32/api/unknwn/nf-unknwn-iunknown-addref)                 | <span data-ttu-id="7e17a-130">Incrémente le décompte de références.</span><span class="sxs-lookup"><span data-stu-id="7e17a-130">Increments reference count.</span></span>               |
| [<span data-ttu-id="7e17a-131">IUnknown :: Release</span><span class="sxs-lookup"><span data-stu-id="7e17a-131">IUnknown::Release</span></span>](/windows/win32/api/unknwn/nf-unknwn-iunknown-release)               | <span data-ttu-id="7e17a-132">Décrémente le décompte de références.</span><span class="sxs-lookup"><span data-stu-id="7e17a-132">Decrements reference count.</span></span>               |



 

## <a name="requirements"></a><span data-ttu-id="7e17a-133">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="7e17a-133">Requirements</span></span>



| <span data-ttu-id="7e17a-134">Condition requise</span><span class="sxs-lookup"><span data-stu-id="7e17a-134">Requirement</span></span> | <span data-ttu-id="7e17a-135">Valeur</span><span class="sxs-lookup"><span data-stu-id="7e17a-135">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="7e17a-136">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="7e17a-136">Minimum supported client</span></span><br/> | <span data-ttu-id="7e17a-137">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="7e17a-137">Windows Vista \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="7e17a-138">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="7e17a-138">Minimum supported server</span></span><br/> | <span data-ttu-id="7e17a-139">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="7e17a-139">Windows Server 2008 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="7e17a-140">En-tête</span><span class="sxs-lookup"><span data-stu-id="7e17a-140">Header</span></span><br/>                   | <dl> <span data-ttu-id="7e17a-141"><dt>WIA. h</dt></span><span class="sxs-lookup"><span data-stu-id="7e17a-141"><dt>Wia.h</dt></span></span> </dl>   |
| <span data-ttu-id="7e17a-142">MIDL</span><span class="sxs-lookup"><span data-stu-id="7e17a-142">IDL</span></span><br/>                      | <dl> <span data-ttu-id="7e17a-143"><dt>WIA. idl</dt></span><span class="sxs-lookup"><span data-stu-id="7e17a-143"><dt>Wia.idl</dt></span></span> </dl> |



 

 
