---
description: L’interface IWiaPreview met en cache les images non filtrées en interne et les transmet via des filtres de traitement d’image.
ms.assetid: 8a51c42b-aa1d-4df0-aba3-6aeb8e1ca2cf
title: Interface IWiaPreview (WIA. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWiaPreview
api_type:
- COM
api_location:
- Wia.h
ms.openlocfilehash: 5e1c01daae4e86fa18c087b67bf902daaf6f8793
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104201493"
---
# <a name="iwiapreview-interface"></a><span data-ttu-id="dec19-103">Interface IWiaPreview</span><span class="sxs-lookup"><span data-stu-id="dec19-103">IWiaPreview interface</span></span>

<span data-ttu-id="dec19-104">L’interface **IWiaPreview** met en cache les images non filtrées en interne et les transmet via des filtres de traitement d’image.</span><span class="sxs-lookup"><span data-stu-id="dec19-104">The **IWiaPreview** interface caches unfiltered images internally and passes them through image processing filters.</span></span>

## <a name="members"></a><span data-ttu-id="dec19-105">Membres</span><span class="sxs-lookup"><span data-stu-id="dec19-105">Members</span></span>

<span data-ttu-id="dec19-106">L’interface **IWiaPreview** hérite de l’interface [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) .</span><span class="sxs-lookup"><span data-stu-id="dec19-106">The **IWiaPreview** interface inherits from the [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="dec19-107">**IWiaPreview** a également les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="dec19-107">**IWiaPreview** also has these types of members:</span></span>

-   [<span data-ttu-id="dec19-108">Méthodes</span><span class="sxs-lookup"><span data-stu-id="dec19-108">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="dec19-109">Méthodes</span><span class="sxs-lookup"><span data-stu-id="dec19-109">Methods</span></span>

<span data-ttu-id="dec19-110">L’interface **IWiaPreview** possède ces méthodes.</span><span class="sxs-lookup"><span data-stu-id="dec19-110">The **IWiaPreview** interface has these methods.</span></span>



| <span data-ttu-id="dec19-111">Méthode</span><span class="sxs-lookup"><span data-stu-id="dec19-111">Method</span></span>                                                  | <span data-ttu-id="dec19-112">Description</span><span class="sxs-lookup"><span data-stu-id="dec19-112">Description</span></span>                                                                                                                                                                                 |
|:--------------------------------------------------------|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="dec19-113">**Effacé**</span><span class="sxs-lookup"><span data-stu-id="dec19-113">**Clear**</span></span>](-wia-iwiapreview-clear.md)                 | <span data-ttu-id="dec19-114">Libère l’image non filtrée mise en cache par la méthode [**IWiaPreview :: GetNewPreview**](-wia-iwiapreview-getnewpreview.md) .</span><span class="sxs-lookup"><span data-stu-id="dec19-114">Releases the unfiltered image cached by the [**IWiaPreview::GetNewPreview**](-wia-iwiapreview-getnewpreview.md) method.</span></span> <span data-ttu-id="dec19-115">Il libère également le filtre de traitement d’image.</span><span class="sxs-lookup"><span data-stu-id="dec19-115">It also releases the image processing filter.</span></span> <br/>          |
| [<span data-ttu-id="dec19-116">**DetectRegions**</span><span class="sxs-lookup"><span data-stu-id="dec19-116">**DetectRegions**</span></span>](-wia-iwiapreview-detectregions.md) | <span data-ttu-id="dec19-117">Appelle le filtre de segmentation du pilote et passe l’image non filtrée mise en cache par la méthode [**IWiaPreview :: GetNewPreview**](-wia-iwiapreview-getnewpreview.md) au filtre.</span><span class="sxs-lookup"><span data-stu-id="dec19-117">Invokes the driver segmentation filter and passes the unfiltered image cached by the [**IWiaPreview::GetNewPreview**](-wia-iwiapreview-getnewpreview.md) method to the filter.</span></span> <br/> |
| [<span data-ttu-id="dec19-118">**GetNewPreview**</span><span class="sxs-lookup"><span data-stu-id="dec19-118">**GetNewPreview**</span></span>](-wia-iwiapreview-getnewpreview.md) | <span data-ttu-id="dec19-119">Met en cache en interne l’image non filtrée retournée par le pilote.</span><span class="sxs-lookup"><span data-stu-id="dec19-119">Caches internally the unfiltered image returned from the driver.</span></span> <br/>                                                                                                                |
| [<span data-ttu-id="dec19-120">**UpdatePreview**</span><span class="sxs-lookup"><span data-stu-id="dec19-120">**UpdatePreview**</span></span>](-wia-iwiapreview-updatepreview.md) | <span data-ttu-id="dec19-121">Obtient l’image non filtrée mise en cache par la méthode [**IWiaPreview :: GetNewPreview**](-wia-iwiapreview-getnewpreview.md) .</span><span class="sxs-lookup"><span data-stu-id="dec19-121">Gets the unfiltered image cached by the [**IWiaPreview::GetNewPreview**](-wia-iwiapreview-getnewpreview.md) method.</span></span> <br/>                                                            |



 

## <a name="remarks"></a><span data-ttu-id="dec19-122">Notes</span><span class="sxs-lookup"><span data-stu-id="dec19-122">Remarks</span></span>

<span data-ttu-id="dec19-123">Ce filtre est appelé automatiquement par la méthode [**IWiaTransfer ::D lécharger**](-wia-iwiatransfer-download.md) .</span><span class="sxs-lookup"><span data-stu-id="dec19-123">This filter is called automatically by the [**IWiaTransfer::Download**](-wia-iwiatransfer-download.md) method.</span></span>

<span data-ttu-id="dec19-124">L’interface **IWiaPreview** , comme toutes les interfaces COM (Component Object Model), hérite des méthodes d’interface [IUnknown](/windows/win32/api/unknwn/nn-unknwn-iunknown) .</span><span class="sxs-lookup"><span data-stu-id="dec19-124">The **IWiaPreview** interface, like all Component Object Model (COM) interfaces, inherits the [IUnknown](/windows/win32/api/unknwn/nn-unknwn-iunknown) interface methods.</span></span>



| <span data-ttu-id="dec19-125">Méthodes IUnknown</span><span class="sxs-lookup"><span data-stu-id="dec19-125">IUnknown Methods</span></span>                                        | <span data-ttu-id="dec19-126">Description</span><span class="sxs-lookup"><span data-stu-id="dec19-126">Description</span></span>                               |
|---------------------------------------------------------|-------------------------------------------|
| <span data-ttu-id="dec19-127">[IUnknown :: QueryInterface](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q))</span><span class="sxs-lookup"><span data-stu-id="dec19-127">[IUnknown::QueryInterface](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q))</span></span> | <span data-ttu-id="dec19-128">Retourne des pointeurs aux interfaces prises en charge.</span><span class="sxs-lookup"><span data-stu-id="dec19-128">Returns pointers to supported interfaces.</span></span> |
| [<span data-ttu-id="dec19-129">IUnknown :: AddRef</span><span class="sxs-lookup"><span data-stu-id="dec19-129">IUnknown::AddRef</span></span>](/windows/win32/api/unknwn/nf-unknwn-iunknown-addref)                 | <span data-ttu-id="dec19-130">Incrémente le décompte de références.</span><span class="sxs-lookup"><span data-stu-id="dec19-130">Increments reference count.</span></span>               |
| [<span data-ttu-id="dec19-131">IUnknown :: Release</span><span class="sxs-lookup"><span data-stu-id="dec19-131">IUnknown::Release</span></span>](/windows/win32/api/unknwn/nf-unknwn-iunknown-release)               | <span data-ttu-id="dec19-132">Décrémente le décompte de références.</span><span class="sxs-lookup"><span data-stu-id="dec19-132">Decrements reference count.</span></span>               |



 

## <a name="requirements"></a><span data-ttu-id="dec19-133">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="dec19-133">Requirements</span></span>



| <span data-ttu-id="dec19-134">Condition requise</span><span class="sxs-lookup"><span data-stu-id="dec19-134">Requirement</span></span> | <span data-ttu-id="dec19-135">Valeur</span><span class="sxs-lookup"><span data-stu-id="dec19-135">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="dec19-136">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="dec19-136">Minimum supported client</span></span><br/> | <span data-ttu-id="dec19-137">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="dec19-137">Windows Vista \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="dec19-138">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="dec19-138">Minimum supported server</span></span><br/> | <span data-ttu-id="dec19-139">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="dec19-139">Windows Server 2008 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="dec19-140">En-tête</span><span class="sxs-lookup"><span data-stu-id="dec19-140">Header</span></span><br/>                   | <dl> <span data-ttu-id="dec19-141"><dt>WIA. h</dt></span><span class="sxs-lookup"><span data-stu-id="dec19-141"><dt>Wia.h</dt></span></span> </dl>   |
| <span data-ttu-id="dec19-142">MIDL</span><span class="sxs-lookup"><span data-stu-id="dec19-142">IDL</span></span><br/>                      | <dl> <span data-ttu-id="dec19-143"><dt>WIA. idl</dt></span><span class="sxs-lookup"><span data-stu-id="dec19-143"><dt>Wia.idl</dt></span></span> </dl> |



 

 
