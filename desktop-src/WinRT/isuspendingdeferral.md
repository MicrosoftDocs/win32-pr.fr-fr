---
description: Gère une opération d’interruption d’application retardée.
ms.assetid: 9F40659E-9B16-4FC9-B320-5679BB8A8161
title: Interface ISuspendingDeferral (Windows. ApplicationModel. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISuspendingDeferral
api_type:
- COM
api_location:
- Windows.ApplicationModel.h
ms.openlocfilehash: e4f1801960f2d3b9183550e18fb76378bf4f17f3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106515854"
---
# <a name="isuspendingdeferral-interface"></a><span data-ttu-id="dd44d-103">Interface ISuspendingDeferral</span><span class="sxs-lookup"><span data-stu-id="dd44d-103">ISuspendingDeferral interface</span></span>

<span data-ttu-id="dd44d-104">Gère une opération d’interruption d’application retardée.</span><span class="sxs-lookup"><span data-stu-id="dd44d-104">Manages a delayed app suspending operation.</span></span>

## <a name="members"></a><span data-ttu-id="dd44d-105">Membres</span><span class="sxs-lookup"><span data-stu-id="dd44d-105">Members</span></span>

<span data-ttu-id="dd44d-106">L’interface **ISuspendingDeferral** hérite de [**IInspectable**](/windows/win32/api/inspectable/nn-inspectable-iinspectable).</span><span class="sxs-lookup"><span data-stu-id="dd44d-106">The **ISuspendingDeferral** interface inherits from [**IInspectable**](/windows/win32/api/inspectable/nn-inspectable-iinspectable).</span></span> <span data-ttu-id="dd44d-107">**ISuspendingDeferral** a également les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="dd44d-107">**ISuspendingDeferral** also has these types of members:</span></span>

-   [<span data-ttu-id="dd44d-108">Méthodes</span><span class="sxs-lookup"><span data-stu-id="dd44d-108">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="dd44d-109">Méthodes</span><span class="sxs-lookup"><span data-stu-id="dd44d-109">Methods</span></span>

<span data-ttu-id="dd44d-110">L’interface **ISuspendingDeferral** possède ces méthodes.</span><span class="sxs-lookup"><span data-stu-id="dd44d-110">The **ISuspendingDeferral** interface has these methods.</span></span>



| <span data-ttu-id="dd44d-111">Méthode</span><span class="sxs-lookup"><span data-stu-id="dd44d-111">Method</span></span>                                           | <span data-ttu-id="dd44d-112">Description</span><span class="sxs-lookup"><span data-stu-id="dd44d-112">Description</span></span>                                                                                  |
|:-------------------------------------------------|:---------------------------------------------------------------------------------------------|
| [<span data-ttu-id="dd44d-113">**Terminé**</span><span class="sxs-lookup"><span data-stu-id="dd44d-113">**Complete**</span></span>](isuspendingdeferral-complete.md) | <span data-ttu-id="dd44d-114">Indique au système que l’application a enregistré ses données et qu’elle est prête à être suspendue.</span><span class="sxs-lookup"><span data-stu-id="dd44d-114">Notifies the system that the app has saved its data and is ready to be suspended.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="dd44d-115">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="dd44d-115">Requirements</span></span>



| <span data-ttu-id="dd44d-116">Condition requise</span><span class="sxs-lookup"><span data-stu-id="dd44d-116">Requirement</span></span> | <span data-ttu-id="dd44d-117">Valeur</span><span class="sxs-lookup"><span data-stu-id="dd44d-117">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="dd44d-118">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="dd44d-118">Minimum supported client</span></span><br/> | <span data-ttu-id="dd44d-119">Applications de \[ Bureau Windows 8 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="dd44d-119">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="dd44d-120">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="dd44d-120">Minimum supported server</span></span><br/> | <span data-ttu-id="dd44d-121">Applications de bureau Windows Server 2012 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="dd44d-121">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="dd44d-122">En-tête</span><span class="sxs-lookup"><span data-stu-id="dd44d-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="dd44d-123"><dt>Windows. ApplicationModel. h</dt></span><span class="sxs-lookup"><span data-stu-id="dd44d-123"><dt>Windows.ApplicationModel.h</dt></span></span> </dl>   |
| <span data-ttu-id="dd44d-124">MIDL</span><span class="sxs-lookup"><span data-stu-id="dd44d-124">IDL</span></span><br/>                      | <dl> <span data-ttu-id="dd44d-125"><dt>Windows. ApplicationModel. idl</dt></span><span class="sxs-lookup"><span data-stu-id="dd44d-125"><dt>Windows.ApplicationModel.idl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="dd44d-126">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="dd44d-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="dd44d-127">**IInspectable**</span><span class="sxs-lookup"><span data-stu-id="dd44d-127">**IInspectable**</span></span>](/windows/win32/api/inspectable/nn-inspectable-iinspectable)
</dt> <dt>

[<span data-ttu-id="dd44d-128">**ISuspendingEventArgs**</span><span class="sxs-lookup"><span data-stu-id="dd44d-128">**ISuspendingEventArgs**</span></span>](isuspendingeventargs.md)
</dt> <dt>

[<span data-ttu-id="dd44d-129">**ISuspendingOperation**</span><span class="sxs-lookup"><span data-stu-id="dd44d-129">**ISuspendingOperation**</span></span>](isuspendingoperation.md)
</dt> </dl>

 

 
