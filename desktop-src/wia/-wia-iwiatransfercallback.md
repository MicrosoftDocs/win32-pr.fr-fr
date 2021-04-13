---
description: L’interface IWiaTransferCallback reçoit des rappels pendant un transfert de données.
ms.assetid: 8fcaccf5-4d7b-4984-97ec-ec8c838a8360
title: Interface IWiaTransferCallback (WIA. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWiaTransferCallback
api_type:
- COM
api_location:
- Wiaguid.lib
- Wiaguid.dll
ms.openlocfilehash: 918482ebcb24f2638a006ab1bbc452ea28ff61e4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104113294"
---
# <a name="iwiatransfercallback-interface"></a><span data-ttu-id="47ce9-103">Interface IWiaTransferCallback</span><span class="sxs-lookup"><span data-stu-id="47ce9-103">IWiaTransferCallback interface</span></span>

<span data-ttu-id="47ce9-104">L’interface **IWiaTransferCallback** reçoit des rappels pendant un transfert de données.</span><span class="sxs-lookup"><span data-stu-id="47ce9-104">The **IWiaTransferCallback** interface receives callbacks during a data transfer.</span></span>

## <a name="members"></a><span data-ttu-id="47ce9-105">Membres</span><span class="sxs-lookup"><span data-stu-id="47ce9-105">Members</span></span>

<span data-ttu-id="47ce9-106">L’interface **IWiaTransferCallback** hérite de l’interface [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) .</span><span class="sxs-lookup"><span data-stu-id="47ce9-106">The **IWiaTransferCallback** interface inherits from the [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="47ce9-107">**IWiaTransferCallback** a également les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="47ce9-107">**IWiaTransferCallback** also has these types of members:</span></span>

-   [<span data-ttu-id="47ce9-108">Méthodes</span><span class="sxs-lookup"><span data-stu-id="47ce9-108">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="47ce9-109">Méthodes</span><span class="sxs-lookup"><span data-stu-id="47ce9-109">Methods</span></span>

<span data-ttu-id="47ce9-110">L’interface **IWiaTransferCallback** possède ces méthodes.</span><span class="sxs-lookup"><span data-stu-id="47ce9-110">The **IWiaTransferCallback** interface has these methods.</span></span>



| <span data-ttu-id="47ce9-111">Méthode</span><span class="sxs-lookup"><span data-stu-id="47ce9-111">Method</span></span>                                                                 | <span data-ttu-id="47ce9-112">Description</span><span class="sxs-lookup"><span data-stu-id="47ce9-112">Description</span></span>                                                              |
|:-----------------------------------------------------------------------|:-------------------------------------------------------------------------|
| [<span data-ttu-id="47ce9-113">**GetNextStream**</span><span class="sxs-lookup"><span data-stu-id="47ce9-113">**GetNextStream**</span></span>](-wia-iwiatransfercallback-getnextstream.md)       | <span data-ttu-id="47ce9-114">Obtient un nouveau flux pour l’élément spécifié.</span><span class="sxs-lookup"><span data-stu-id="47ce9-114">Gets a new stream for the specified item.</span></span> <br/>                    |
| [<span data-ttu-id="47ce9-115">**TransferCallback**</span><span class="sxs-lookup"><span data-stu-id="47ce9-115">**TransferCallback**</span></span>](-wia-iwiatransfercallback-transfercallback.md) | <span data-ttu-id="47ce9-116">Fournit la progression et d’autres notifications pendant un transfert.</span><span class="sxs-lookup"><span data-stu-id="47ce9-116">Provides progress and other notifications during a transfer.</span></span> <br/> |



 

## <a name="remarks"></a><span data-ttu-id="47ce9-117">Notes</span><span class="sxs-lookup"><span data-stu-id="47ce9-117">Remarks</span></span>

<span data-ttu-id="47ce9-118">Les développeurs de filtres de traitement d’images doivent implémenter cette interface et l’interface [**IWiaImageFilter**](-wia-iwiaimagefilter.md) .</span><span class="sxs-lookup"><span data-stu-id="47ce9-118">Image processing filter developers should implement this interface and the [**IWiaImageFilter**](-wia-iwiaimagefilter.md) interface.</span></span>

<span data-ttu-id="47ce9-119">L’interface **IWiaTransferCallback** , comme toutes les interfaces COM (Component Object Model), hérite des méthodes d’interface [IUnknown](/windows/win32/api/unknwn/nn-unknwn-iunknown) .</span><span class="sxs-lookup"><span data-stu-id="47ce9-119">The **IWiaTransferCallback** interface, like all Component Object Model (COM) interfaces, inherits the [IUnknown](/windows/win32/api/unknwn/nn-unknwn-iunknown) interface methods.</span></span>



| <span data-ttu-id="47ce9-120">Méthodes IUnknown</span><span class="sxs-lookup"><span data-stu-id="47ce9-120">IUnknown Methods</span></span>                                        | <span data-ttu-id="47ce9-121">Description</span><span class="sxs-lookup"><span data-stu-id="47ce9-121">Description</span></span>                               |
|---------------------------------------------------------|-------------------------------------------|
| <span data-ttu-id="47ce9-122">[IUnknown :: QueryInterface](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q))</span><span class="sxs-lookup"><span data-stu-id="47ce9-122">[IUnknown::QueryInterface](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q))</span></span> | <span data-ttu-id="47ce9-123">Retourne des pointeurs aux interfaces prises en charge.</span><span class="sxs-lookup"><span data-stu-id="47ce9-123">Returns pointers to supported interfaces.</span></span> |
| [<span data-ttu-id="47ce9-124">IUnknown :: AddRef</span><span class="sxs-lookup"><span data-stu-id="47ce9-124">IUnknown::AddRef</span></span>](/windows/win32/api/unknwn/nf-unknwn-iunknown-addref)                 | <span data-ttu-id="47ce9-125">Incrémente le décompte de références.</span><span class="sxs-lookup"><span data-stu-id="47ce9-125">Increments reference count.</span></span>               |
| [<span data-ttu-id="47ce9-126">IUnknown :: Release</span><span class="sxs-lookup"><span data-stu-id="47ce9-126">IUnknown::Release</span></span>](/windows/win32/api/unknwn/nf-unknwn-iunknown-release)               | <span data-ttu-id="47ce9-127">Décrémente le décompte de références.</span><span class="sxs-lookup"><span data-stu-id="47ce9-127">Decrements reference count.</span></span>               |



 

## <a name="requirements"></a><span data-ttu-id="47ce9-128">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="47ce9-128">Requirements</span></span>



| <span data-ttu-id="47ce9-129">Condition requise</span><span class="sxs-lookup"><span data-stu-id="47ce9-129">Requirement</span></span> | <span data-ttu-id="47ce9-130">Valeur</span><span class="sxs-lookup"><span data-stu-id="47ce9-130">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="47ce9-131">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="47ce9-131">Minimum supported client</span></span><br/> | <span data-ttu-id="47ce9-132">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="47ce9-132">Windows Vista \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="47ce9-133">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="47ce9-133">Minimum supported server</span></span><br/> | <span data-ttu-id="47ce9-134">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="47ce9-134">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="47ce9-135">En-tête</span><span class="sxs-lookup"><span data-stu-id="47ce9-135">Header</span></span><br/>                   | <dl> <span data-ttu-id="47ce9-136"><dt>WIA. h</dt></span><span class="sxs-lookup"><span data-stu-id="47ce9-136"><dt>Wia.h</dt></span></span> </dl>       |
| <span data-ttu-id="47ce9-137">MIDL</span><span class="sxs-lookup"><span data-stu-id="47ce9-137">IDL</span></span><br/>                      | <dl> <span data-ttu-id="47ce9-138"><dt>WIA. idl</dt></span><span class="sxs-lookup"><span data-stu-id="47ce9-138"><dt>Wia.idl</dt></span></span> </dl>     |
| <span data-ttu-id="47ce9-139">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="47ce9-139">Library</span></span><br/>                  | <dl> <span data-ttu-id="47ce9-140"><dt>Wiaguid. lib</dt></span><span class="sxs-lookup"><span data-stu-id="47ce9-140"><dt>Wiaguid.lib</dt></span></span> </dl> |



 

 
