---
description: Demande un pointeur vers un objet spécifié.
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
ms.openlocfilehash: 5d0c0592356bff13e60c122b3c88cad05733e4f9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104991645"
---
# <a name="smc_getobject-message"></a><span data-ttu-id="c4edc-103">\_Message SMC GETOBJECT</span><span class="sxs-lookup"><span data-stu-id="c4edc-103">SMC\_GETOBJECT message</span></span>

<span data-ttu-id="c4edc-104">Demande un pointeur vers un objet spécifié.</span><span class="sxs-lookup"><span data-stu-id="c4edc-104">Requests a pointer to a specified object.</span></span>


```C++
SMC_GETOBJECT 
    wParam = (WPARAM) (REFIID) iid;
    lParam = (LPARAM) (void **) pv
            
```



## <a name="parameters"></a><span data-ttu-id="c4edc-105">Paramètres</span><span class="sxs-lookup"><span data-stu-id="c4edc-105">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c4edc-106">*vaut*</span><span class="sxs-lookup"><span data-stu-id="c4edc-106">*iid*</span></span> 
</dt> <dd>

<span data-ttu-id="c4edc-107">IID associé à l’objet demandé.</span><span class="sxs-lookup"><span data-stu-id="c4edc-107">The IID associated with the requested object.</span></span>

</dd> <dt>

<span data-ttu-id="c4edc-108">*va*</span><span class="sxs-lookup"><span data-stu-id="c4edc-108">*pv*</span></span> 
</dt> <dd>

<span data-ttu-id="c4edc-109">Pointeur void qui reçoit un pointeur vers l’interface demandée.</span><span class="sxs-lookup"><span data-stu-id="c4edc-109">A void pointer that receives a pointer to the requested interface.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c4edc-110">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="c4edc-110">Return value</span></span>

<span data-ttu-id="c4edc-111">Retourne S \_ OK.</span><span class="sxs-lookup"><span data-stu-id="c4edc-111">Return S\_OK.</span></span>

## <a name="remarks"></a><span data-ttu-id="c4edc-112">Notes</span><span class="sxs-lookup"><span data-stu-id="c4edc-112">Remarks</span></span>

<span data-ttu-id="c4edc-113">Cette notification est reçue par la méthode [**IShellMenuCallback :: CallbackSM**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellmenucallback-callbacksm) .</span><span class="sxs-lookup"><span data-stu-id="c4edc-113">This notification is received by the [**IShellMenuCallback::CallbackSM**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellmenucallback-callbacksm) method.</span></span> <span data-ttu-id="c4edc-114">Créez l’objet demandé et assignez un pointeur vers l’interface demandée à *va*.</span><span class="sxs-lookup"><span data-stu-id="c4edc-114">Create the requested object and assign a pointer to the requested interface to *pv*.</span></span>

<span data-ttu-id="c4edc-115">Les interfaces suivantes peuvent être demandées.</span><span class="sxs-lookup"><span data-stu-id="c4edc-115">The following interfaces may be requested.</span></span>

-   [<span data-ttu-id="c4edc-116">**IShellMenu**</span><span class="sxs-lookup"><span data-stu-id="c4edc-116">**IShellMenu**</span></span>](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellmenu)
-   [<span data-ttu-id="c4edc-117">**IContextMenu**</span><span class="sxs-lookup"><span data-stu-id="c4edc-117">**IContextMenu**</span></span>](/windows/win32/api/shobjidl_core/nn-shobjidl_core-icontextmenu)
-   [<span data-ttu-id="c4edc-118">**IShellMenuCallback**</span><span class="sxs-lookup"><span data-stu-id="c4edc-118">**IShellMenuCallback**</span></span>](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellmenucallback)
-   [<span data-ttu-id="c4edc-119">**IDropTarget**</span><span class="sxs-lookup"><span data-stu-id="c4edc-119">**IDropTarget**</span></span>](/windows/win32/api/oleidl/nn-oleidl-idroptarget)

## <a name="requirements"></a><span data-ttu-id="c4edc-120">Spécifications</span><span class="sxs-lookup"><span data-stu-id="c4edc-120">Requirements</span></span>



| <span data-ttu-id="c4edc-121">Condition requise</span><span class="sxs-lookup"><span data-stu-id="c4edc-121">Requirement</span></span> | <span data-ttu-id="c4edc-122">Valeur</span><span class="sxs-lookup"><span data-stu-id="c4edc-122">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="c4edc-123">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="c4edc-123">Minimum supported client</span></span><br/> | <span data-ttu-id="c4edc-124">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="c4edc-124">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="c4edc-125">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="c4edc-125">Minimum supported server</span></span><br/> | <span data-ttu-id="c4edc-126">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="c4edc-126">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="c4edc-127">En-tête</span><span class="sxs-lookup"><span data-stu-id="c4edc-127">Header</span></span><br/>                   | <dl> <span data-ttu-id="c4edc-128"><dt>ShObjIdl. h</dt></span><span class="sxs-lookup"><span data-stu-id="c4edc-128"><dt>Shobjidl.h</dt></span></span> </dl>   |
| <span data-ttu-id="c4edc-129">MIDL</span><span class="sxs-lookup"><span data-stu-id="c4edc-129">IDL</span></span><br/>                      | <dl> <span data-ttu-id="c4edc-130"><dt>ShObjIdl. idl</dt></span><span class="sxs-lookup"><span data-stu-id="c4edc-130"><dt>Shobjidl.idl</dt></span></span> </dl> |



 

 
