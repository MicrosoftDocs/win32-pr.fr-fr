---
description: SMC_GETOBJECT message-demande un pointeur vers un objet spécifié.
title: Message SMC_GETOBJECT (ShObjIdl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 36e8f304-a92a-485f-8413-b9c416087ec9
api_name:
- SMC_GETOBJECT
api_type:
- HeaderDef
api_location:
- Shobjidl.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 58741290d741cc18fd788282d0f302ef87bb15dd
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108100437"
---
# <a name="smc_getobject-message"></a><span data-ttu-id="b9438-103">\_Message SMC GETOBJECT</span><span class="sxs-lookup"><span data-stu-id="b9438-103">SMC\_GETOBJECT message</span></span>

<span data-ttu-id="b9438-104">Demande un pointeur vers un objet spécifié.</span><span class="sxs-lookup"><span data-stu-id="b9438-104">Requests a pointer to a specified object.</span></span>


```C++
SMC_GETOBJECT 
    wParam = (WPARAM) (REFIID) iid;
    lParam = (LPARAM) (void **) pv
            
```



## <a name="parameters"></a><span data-ttu-id="b9438-105">Paramètres</span><span class="sxs-lookup"><span data-stu-id="b9438-105">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b9438-106">*vaut*</span><span class="sxs-lookup"><span data-stu-id="b9438-106">*iid*</span></span> 
</dt> <dd>

<span data-ttu-id="b9438-107">IID associé à l’objet demandé.</span><span class="sxs-lookup"><span data-stu-id="b9438-107">The IID associated with the requested object.</span></span>

</dd> <dt>

<span data-ttu-id="b9438-108">*va*</span><span class="sxs-lookup"><span data-stu-id="b9438-108">*pv*</span></span> 
</dt> <dd>

<span data-ttu-id="b9438-109">Pointeur void qui reçoit un pointeur vers l’interface demandée.</span><span class="sxs-lookup"><span data-stu-id="b9438-109">A void pointer that receives a pointer to the requested interface.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b9438-110">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="b9438-110">Return value</span></span>

<span data-ttu-id="b9438-111">Retourne S \_ OK.</span><span class="sxs-lookup"><span data-stu-id="b9438-111">Return S\_OK.</span></span>

## <a name="remarks"></a><span data-ttu-id="b9438-112">Notes </span><span class="sxs-lookup"><span data-stu-id="b9438-112">Remarks</span></span>

<span data-ttu-id="b9438-113">Cette notification est reçue par la méthode [**IShellMenuCallback :: CallbackSM**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellmenucallback-callbacksm) .</span><span class="sxs-lookup"><span data-stu-id="b9438-113">This notification is received by the [**IShellMenuCallback::CallbackSM**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellmenucallback-callbacksm) method.</span></span> <span data-ttu-id="b9438-114">Créez l’objet demandé et assignez un pointeur vers l’interface demandée à *va*.</span><span class="sxs-lookup"><span data-stu-id="b9438-114">Create the requested object and assign a pointer to the requested interface to *pv*.</span></span>

<span data-ttu-id="b9438-115">Les interfaces suivantes peuvent être demandées.</span><span class="sxs-lookup"><span data-stu-id="b9438-115">The following interfaces may be requested.</span></span>

-   [<span data-ttu-id="b9438-116">**IShellMenu**</span><span class="sxs-lookup"><span data-stu-id="b9438-116">**IShellMenu**</span></span>](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellmenu)
-   [<span data-ttu-id="b9438-117">**IContextMenu**</span><span class="sxs-lookup"><span data-stu-id="b9438-117">**IContextMenu**</span></span>](/windows/win32/api/shobjidl_core/nn-shobjidl_core-icontextmenu)
-   [<span data-ttu-id="b9438-118">**IShellMenuCallback**</span><span class="sxs-lookup"><span data-stu-id="b9438-118">**IShellMenuCallback**</span></span>](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellmenucallback)
-   [<span data-ttu-id="b9438-119">**IDropTarget**</span><span class="sxs-lookup"><span data-stu-id="b9438-119">**IDropTarget**</span></span>](/windows/win32/api/oleidl/nn-oleidl-idroptarget)

## <a name="requirements"></a><span data-ttu-id="b9438-120">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="b9438-120">Requirements</span></span>



| <span data-ttu-id="b9438-121">Condition requise</span><span class="sxs-lookup"><span data-stu-id="b9438-121">Requirement</span></span> | <span data-ttu-id="b9438-122">Valeur</span><span class="sxs-lookup"><span data-stu-id="b9438-122">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="b9438-123">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="b9438-123">Minimum supported client</span></span><br/> | <span data-ttu-id="b9438-124">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="b9438-124">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="b9438-125">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="b9438-125">Minimum supported server</span></span><br/> | <span data-ttu-id="b9438-126">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="b9438-126">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="b9438-127">En-tête</span><span class="sxs-lookup"><span data-stu-id="b9438-127">Header</span></span><br/>                   | <dl> <span data-ttu-id="b9438-128"><dt>ShObjIdl. h</dt></span><span class="sxs-lookup"><span data-stu-id="b9438-128"><dt>Shobjidl.h</dt></span></span> </dl>   |
| <span data-ttu-id="b9438-129">MIDL</span><span class="sxs-lookup"><span data-stu-id="b9438-129">IDL</span></span><br/>                      | <dl> <span data-ttu-id="b9438-130"><dt>ShObjIdl. idl</dt></span><span class="sxs-lookup"><span data-stu-id="b9438-130"><dt>Shobjidl.idl</dt></span></span> </dl> |



 

 
