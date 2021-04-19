---
description: Représente la méthode qui est appelée lorsqu’une action asynchrone se termine.
ms.assetid: B410E7C1-B108-4204-9AD1-663F7E05BBC3
title: Interface AsyncActionCompletedHandler
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- AsyncActionCompletedHandler
api_type:
- COM
api_location:
- Windows.Foundation.idl
ms.openlocfilehash: 639f5c39d0d9e4086009fd08bd0204f9f5f25060
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106529119"
---
# <a name="asyncactioncompletedhandler-interface"></a><span data-ttu-id="873ca-103">Interface AsyncActionCompletedHandler</span><span class="sxs-lookup"><span data-stu-id="873ca-103">AsyncActionCompletedHandler interface</span></span>

<span data-ttu-id="873ca-104">Représente la méthode qui est appelée lorsqu’une action asynchrone se termine.</span><span class="sxs-lookup"><span data-stu-id="873ca-104">Represents the method that is called when an asynchronous action completes.</span></span>

## <a name="members"></a><span data-ttu-id="873ca-105">Membres</span><span class="sxs-lookup"><span data-stu-id="873ca-105">Members</span></span>

<span data-ttu-id="873ca-106">L’interface **AsyncActionCompletedHandler** hérite de [**IAsyncInfo**](/windows/win32/api/asyncinfo/nn-asyncinfo-iasyncinfo).</span><span class="sxs-lookup"><span data-stu-id="873ca-106">The **AsyncActionCompletedHandler** interface inherits from [**IAsyncInfo**](/windows/win32/api/asyncinfo/nn-asyncinfo-iasyncinfo).</span></span> <span data-ttu-id="873ca-107">**AsyncActionCompletedHandler** a également les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="873ca-107">**AsyncActionCompletedHandler** also has these types of members:</span></span>

-   [<span data-ttu-id="873ca-108">Méthodes</span><span class="sxs-lookup"><span data-stu-id="873ca-108">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="873ca-109">Méthodes</span><span class="sxs-lookup"><span data-stu-id="873ca-109">Methods</span></span>

<span data-ttu-id="873ca-110">L’interface **AsyncActionCompletedHandler** possède ces méthodes.</span><span class="sxs-lookup"><span data-stu-id="873ca-110">The **AsyncActionCompletedHandler** interface has these methods.</span></span>



| <span data-ttu-id="873ca-111">Méthode</span><span class="sxs-lookup"><span data-stu-id="873ca-111">Method</span></span>                                               | <span data-ttu-id="873ca-112">Description</span><span class="sxs-lookup"><span data-stu-id="873ca-112">Description</span></span>                                                                                    |
|:-----------------------------------------------------|:-----------------------------------------------------------------------------------------------|
| [<span data-ttu-id="873ca-113">**Appeler**</span><span class="sxs-lookup"><span data-stu-id="873ca-113">**Invoke**</span></span>](asyncactioncompletedhandler-invoke.md) | <span data-ttu-id="873ca-114">Appelle la méthode qui est appelée lorsque l’action asynchrone spécifiée se termine.</span><span class="sxs-lookup"><span data-stu-id="873ca-114">Invokes the method that is called when the specified asynchronous action completes.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="873ca-115">Notes</span><span class="sxs-lookup"><span data-stu-id="873ca-115">Remarks</span></span>

<span data-ttu-id="873ca-116">Assignez un **AsyncActionCompletedHandler** à un [**IAsyncAction**](/windows/win32/api/windows.foundation/nn-windows-foundation-iasyncaction) pour recevoir une notification lorsque l’action asynchrone se termine.</span><span class="sxs-lookup"><span data-stu-id="873ca-116">Assign an **AsyncActionCompletedHandler** to an [**IAsyncAction**](/windows/win32/api/windows.foundation/nn-windows-foundation-iasyncaction) to receive a notification when the asynchronous action completes.</span></span>

## <a name="requirements"></a><span data-ttu-id="873ca-117">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="873ca-117">Requirements</span></span>



| <span data-ttu-id="873ca-118">Condition requise</span><span class="sxs-lookup"><span data-stu-id="873ca-118">Requirement</span></span> | <span data-ttu-id="873ca-119">Valeur</span><span class="sxs-lookup"><span data-stu-id="873ca-119">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------|
| <span data-ttu-id="873ca-120">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="873ca-120">Minimum supported client</span></span><br/> | <span data-ttu-id="873ca-121">Windows 8</span><span class="sxs-lookup"><span data-stu-id="873ca-121">Windows 8</span></span><br/>                                                                              |
| <span data-ttu-id="873ca-122">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="873ca-122">Minimum supported server</span></span><br/> | <span data-ttu-id="873ca-123">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="873ca-123">Windows Server 2012</span></span><br/>                                                                    |
| <span data-ttu-id="873ca-124">En-tête</span><span class="sxs-lookup"><span data-stu-id="873ca-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="873ca-125"><dt>Windows. Foundation. idl</dt></span><span class="sxs-lookup"><span data-stu-id="873ca-125"><dt>Windows.Foundation.idl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="873ca-126">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="873ca-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="873ca-127">**IAsyncInfo**</span><span class="sxs-lookup"><span data-stu-id="873ca-127">**IAsyncInfo**</span></span>](/windows/win32/api/asyncinfo/nn-asyncinfo-iasyncinfo)
</dt> </dl>

 

