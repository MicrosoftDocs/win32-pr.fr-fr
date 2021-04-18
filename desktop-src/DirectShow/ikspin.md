---
description: L’interface IKsPin fournit une méthode pour récupérer les supports pris en charge par un code confidentiel sur un filtre en mode noyau. IKsPin a des méthodes supplémentaires en plus de celle présentée ici, mais elles ne sont pas prises en charge pour DirectShow.
ms.assetid: 14d9bef2-e8f0-49d5-bd89-69a95814cf8c
title: Interface IKsPin (ksproxy. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IKsPin
api_type:
- COM
api_location:
- Strmiids.lib
- Strmiids.dll
ms.openlocfilehash: 3d65e5ba5525b977ebae27da9964579614a1d653
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/06/2021
ms.locfileid: "106516343"
---
# <a name="ikspin-interface"></a><span data-ttu-id="65506-104">Interface IKsPin</span><span class="sxs-lookup"><span data-stu-id="65506-104">IKsPin interface</span></span>

<span data-ttu-id="65506-105">L' `IKsPin` interface fournit une méthode pour récupérer les supports pris en charge par un code confidentiel sur un filtre en mode noyau.</span><span class="sxs-lookup"><span data-stu-id="65506-105">The `IKsPin` interface provides a method to retrieve the mediums supported by a pin on a kernel-mode filter.</span></span> <span data-ttu-id="65506-106">`IKsPin` a des méthodes supplémentaires autres que celles indiquées ici, mais elles ne sont pas prises en charge pour DirectShow.</span><span class="sxs-lookup"><span data-stu-id="65506-106">`IKsPin` has additional methods besides the one shown here, but they are not supported for DirectShow.</span></span>

## <a name="members"></a><span data-ttu-id="65506-107">Membres</span><span class="sxs-lookup"><span data-stu-id="65506-107">Members</span></span>

<span data-ttu-id="65506-108">L’interface **IKsPin** hérite de l’interface [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) .</span><span class="sxs-lookup"><span data-stu-id="65506-108">The **IKsPin** interface inherits from the [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="65506-109">**IKsPin** a également les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="65506-109">**IKsPin** also has these types of members:</span></span>

-   [<span data-ttu-id="65506-110">Méthodes</span><span class="sxs-lookup"><span data-stu-id="65506-110">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="65506-111">Méthodes</span><span class="sxs-lookup"><span data-stu-id="65506-111">Methods</span></span>

<span data-ttu-id="65506-112">L’interface **IKsPin** possède ces méthodes.</span><span class="sxs-lookup"><span data-stu-id="65506-112">The **IKsPin** interface has these methods.</span></span>



| <span data-ttu-id="65506-113">Méthode</span><span class="sxs-lookup"><span data-stu-id="65506-113">Method</span></span>                                          | <span data-ttu-id="65506-114">Description</span><span class="sxs-lookup"><span data-stu-id="65506-114">Description</span></span>                                          |
|:------------------------------------------------|:-----------------------------------------------------|
| [<span data-ttu-id="65506-115">**KsQueryMediums**</span><span class="sxs-lookup"><span data-stu-id="65506-115">**KsQueryMediums**</span></span>](ikspin-ksquerymediums.md) | <span data-ttu-id="65506-116">Récupère les supports pris en charge par un code confidentiel.</span><span class="sxs-lookup"><span data-stu-id="65506-116">Retrieves the mediums supported by a pin.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="65506-117">Notes</span><span class="sxs-lookup"><span data-stu-id="65506-117">Remarks</span></span>

<span data-ttu-id="65506-118">Vous devez inclure KS. h avant ksproxy. h.</span><span class="sxs-lookup"><span data-stu-id="65506-118">You must include Ks.h before Ksproxy.h.</span></span>

## <a name="requirements"></a><span data-ttu-id="65506-119">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="65506-119">Requirements</span></span>



| <span data-ttu-id="65506-120">Condition requise</span><span class="sxs-lookup"><span data-stu-id="65506-120">Requirement</span></span> | <span data-ttu-id="65506-121">Valeur</span><span class="sxs-lookup"><span data-stu-id="65506-121">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="65506-122">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="65506-122">Minimum supported client</span></span><br/> | <span data-ttu-id="65506-123">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="65506-123">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="65506-124">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="65506-124">Minimum supported server</span></span><br/> | <span data-ttu-id="65506-125">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="65506-125">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="65506-126">En-tête</span><span class="sxs-lookup"><span data-stu-id="65506-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="65506-127"><dt>Ksproxy. h</dt></span><span class="sxs-lookup"><span data-stu-id="65506-127"><dt>Ksproxy.h</dt></span></span> </dl>    |
| <span data-ttu-id="65506-128">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="65506-128">Library</span></span><br/>                  | <dl> <span data-ttu-id="65506-129"><dt>Strmiids. lib</dt></span><span class="sxs-lookup"><span data-stu-id="65506-129"><dt>Strmiids.lib</dt></span></span> </dl> |



 

 
