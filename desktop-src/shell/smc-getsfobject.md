---
description: Demande un pointeur vers un objet spécifié.
title: Message SMC_GETSFOBJECT (ShObjIdl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: a8478f10-77ce-4e71-a5dc-89d8a90cf513
api_name:
- SMC_GETSFOBJECT
api_type:
- HeaderDef
api_location:
- Shobjidl.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: c7fb57ea8e3f02ce4e773e187310530c14d65515
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104203664"
---
# <a name="smc_getsfobject-message"></a><span data-ttu-id="ae930-103">\_Message SMC GETSFOBJECT</span><span class="sxs-lookup"><span data-stu-id="ae930-103">SMC\_GETSFOBJECT message</span></span>

<span data-ttu-id="ae930-104">Demande un pointeur vers un objet spécifié.</span><span class="sxs-lookup"><span data-stu-id="ae930-104">Requests a pointer to a specified object.</span></span>


```C++
SMC_GETSFOBJECT 
    wParam = (WPARAM) (REFIID) iid;
    lParam = (LPARAM) (void **) pv
            
```



## <a name="parameters"></a><span data-ttu-id="ae930-105">Paramètres</span><span class="sxs-lookup"><span data-stu-id="ae930-105">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ae930-106">*vaut*</span><span class="sxs-lookup"><span data-stu-id="ae930-106">*iid*</span></span> 
</dt> <dd>

<span data-ttu-id="ae930-107">IID associé à l’objet demandé.</span><span class="sxs-lookup"><span data-stu-id="ae930-107">The IID associated with the requested object.</span></span>

</dd> <dt>

<span data-ttu-id="ae930-108">*va*</span><span class="sxs-lookup"><span data-stu-id="ae930-108">*pv*</span></span> 
</dt> <dd>

<span data-ttu-id="ae930-109">Pointeur void qui reçoit un pointeur vers l’interface demandée.</span><span class="sxs-lookup"><span data-stu-id="ae930-109">A void pointer that receives a pointer to the requested interface.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ae930-110">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="ae930-110">Return value</span></span>

<span data-ttu-id="ae930-111">Retourne S \_ OK.</span><span class="sxs-lookup"><span data-stu-id="ae930-111">Return S\_OK.</span></span>

## <a name="remarks"></a><span data-ttu-id="ae930-112">Notes</span><span class="sxs-lookup"><span data-stu-id="ae930-112">Remarks</span></span>

<span data-ttu-id="ae930-113">Cette notification est reçue par la méthode [**IShellMenuCallback :: CallbackSM**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellmenucallback-callbacksm) .</span><span class="sxs-lookup"><span data-stu-id="ae930-113">This notification is received by the [**IShellMenuCallback::CallbackSM**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellmenucallback-callbacksm) method.</span></span> <span data-ttu-id="ae930-114">Il est similaire à [**SMC \_ GETOBJECT**](smc-getobject.md) , mais est utilisé pour les éléments de dossier shell.</span><span class="sxs-lookup"><span data-stu-id="ae930-114">It is similar to [**SMC\_GETOBJECT**](smc-getobject.md) but used for Shell folder items.</span></span> <span data-ttu-id="ae930-115">Créez l’objet demandé et assignez un pointeur vers l’interface demandée à *va*.</span><span class="sxs-lookup"><span data-stu-id="ae930-115">Create the requested object and assign a pointer to the requested interface to *pv*.</span></span>

<span data-ttu-id="ae930-116">Les interfaces suivantes peuvent être demandées.</span><span class="sxs-lookup"><span data-stu-id="ae930-116">The following interfaces may be requested.</span></span>

-   [<span data-ttu-id="ae930-117">**IStream**</span><span class="sxs-lookup"><span data-stu-id="ae930-117">**IStream**</span></span>](/windows/win32/api/objidl/nn-objidl-istream)
-   [<span data-ttu-id="ae930-118">**IShellMenu**</span><span class="sxs-lookup"><span data-stu-id="ae930-118">**IShellMenu**</span></span>](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellmenu)
-   [<span data-ttu-id="ae930-119">**IShellMenuCallback**</span><span class="sxs-lookup"><span data-stu-id="ae930-119">**IShellMenuCallback**</span></span>](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellmenucallback)

## <a name="requirements"></a><span data-ttu-id="ae930-120">Spécifications</span><span class="sxs-lookup"><span data-stu-id="ae930-120">Requirements</span></span>



| <span data-ttu-id="ae930-121">Condition requise</span><span class="sxs-lookup"><span data-stu-id="ae930-121">Requirement</span></span> | <span data-ttu-id="ae930-122">Valeur</span><span class="sxs-lookup"><span data-stu-id="ae930-122">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="ae930-123">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="ae930-123">Minimum supported client</span></span><br/> | <span data-ttu-id="ae930-124">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="ae930-124">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="ae930-125">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="ae930-125">Minimum supported server</span></span><br/> | <span data-ttu-id="ae930-126">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="ae930-126">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="ae930-127">En-tête</span><span class="sxs-lookup"><span data-stu-id="ae930-127">Header</span></span><br/>                   | <dl> <span data-ttu-id="ae930-128"><dt>ShObjIdl. h</dt></span><span class="sxs-lookup"><span data-stu-id="ae930-128"><dt>Shobjidl.h</dt></span></span> </dl>   |
| <span data-ttu-id="ae930-129">MIDL</span><span class="sxs-lookup"><span data-stu-id="ae930-129">IDL</span></span><br/>                      | <dl> <span data-ttu-id="ae930-130"><dt>ShObjIdl. idl</dt></span><span class="sxs-lookup"><span data-stu-id="ae930-130"><dt>Shobjidl.idl</dt></span></span> </dl> |



 

 
