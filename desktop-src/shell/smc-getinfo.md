---
description: Demande des informations sur un élément de menu normal.
title: Message SMC_GETINFO (ShObjIdl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 07f35a64-eff0-48e8-a2fc-719ccf1eca18
api_name:
- SMC_GETINFO
api_type:
- HeaderDef
api_location:
- Shobjidl.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: f60c1581ae7c4585de48eea943cc23b4d87fa4c4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104991644"
---
# <a name="smc_getinfo-message"></a><span data-ttu-id="be441-103">\_Message SMC GETINFO</span><span class="sxs-lookup"><span data-stu-id="be441-103">SMC\_GETINFO message</span></span>

<span data-ttu-id="be441-104">Demande des informations sur un élément de menu normal.</span><span class="sxs-lookup"><span data-stu-id="be441-104">Requests information about a regular menu item.</span></span>


```C++
SMC_GETINFO 
    lParam = (LPARAM) (LPSMINFO) psminfo
            
```



## <a name="parameters"></a><span data-ttu-id="be441-105">Paramètres</span><span class="sxs-lookup"><span data-stu-id="be441-105">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="be441-106">*psminfo*</span><span class="sxs-lookup"><span data-stu-id="be441-106">*psminfo*</span></span> 
</dt> <dd>

<span data-ttu-id="be441-107">Pointeur vers une structure [**SMINFO**](/windows/win32/api/shobjidl_core/ns-shobjidl_core-sminfo) .</span><span class="sxs-lookup"><span data-stu-id="be441-107">A pointer to a [**SMINFO**](/windows/win32/api/shobjidl_core/ns-shobjidl_core-sminfo) structure.</span></span> <span data-ttu-id="be441-108">Remplissez la structure avec les informations appropriées et renvoyez \_ OK.</span><span class="sxs-lookup"><span data-stu-id="be441-108">Fill the structure with the appropriate information and return S\_OK.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="be441-109">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="be441-109">Return value</span></span>

<span data-ttu-id="be441-110">Retourne S \_ OK.</span><span class="sxs-lookup"><span data-stu-id="be441-110">Return S\_OK.</span></span>

## <a name="remarks"></a><span data-ttu-id="be441-111">Notes</span><span class="sxs-lookup"><span data-stu-id="be441-111">Remarks</span></span>

<span data-ttu-id="be441-112">Cette notification est reçue par la méthode [**IShellMenuCallback :: CallbackSM**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellmenucallback-callbacksm) .</span><span class="sxs-lookup"><span data-stu-id="be441-112">This notification is received by the [**IShellMenuCallback::CallbackSM**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellmenucallback-callbacksm) method.</span></span>

## <a name="requirements"></a><span data-ttu-id="be441-113">Spécifications</span><span class="sxs-lookup"><span data-stu-id="be441-113">Requirements</span></span>



| <span data-ttu-id="be441-114">Condition requise</span><span class="sxs-lookup"><span data-stu-id="be441-114">Requirement</span></span> | <span data-ttu-id="be441-115">Valeur</span><span class="sxs-lookup"><span data-stu-id="be441-115">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="be441-116">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="be441-116">Minimum supported client</span></span><br/> | <span data-ttu-id="be441-117">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="be441-117">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="be441-118">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="be441-118">Minimum supported server</span></span><br/> | <span data-ttu-id="be441-119">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="be441-119">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="be441-120">En-tête</span><span class="sxs-lookup"><span data-stu-id="be441-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="be441-121"><dt>ShObjIdl. h</dt></span><span class="sxs-lookup"><span data-stu-id="be441-121"><dt>Shobjidl.h</dt></span></span> </dl>   |
| <span data-ttu-id="be441-122">MIDL</span><span class="sxs-lookup"><span data-stu-id="be441-122">IDL</span></span><br/>                      | <dl> <span data-ttu-id="be441-123"><dt>ShObjIdl. idl</dt></span><span class="sxs-lookup"><span data-stu-id="be441-123"><dt>Shobjidl.idl</dt></span></span> </dl> |



 

 




