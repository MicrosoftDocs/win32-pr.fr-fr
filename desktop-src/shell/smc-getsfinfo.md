---
description: Demande des informations sur un élément de menu de dossier de Shell.
title: Message SMC_GETSFINFO (ShObjIdl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 4459670c-f0fd-4ae8-8a1f-810e1dcac713
api_name:
- SMC_GETSFINFO
api_type:
- HeaderDef
api_location:
- Shobjidl.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: f3a02b61565eb08f623978900d6ce47e30eea85e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104991641"
---
# <a name="smc_getsfinfo-message"></a><span data-ttu-id="391c3-103">\_Message SMC GETSFINFO</span><span class="sxs-lookup"><span data-stu-id="391c3-103">SMC\_GETSFINFO message</span></span>

<span data-ttu-id="391c3-104">Demande des informations sur un élément de menu de dossier de Shell.</span><span class="sxs-lookup"><span data-stu-id="391c3-104">Requests information about a Shell folder menu item.</span></span>


```C++
SMC_GETINFO 
    lParam = (LPARAM) (LPSMINFO) psminfo
            
```



## <a name="parameters"></a><span data-ttu-id="391c3-105">Paramètres</span><span class="sxs-lookup"><span data-stu-id="391c3-105">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="391c3-106">*psminfo*</span><span class="sxs-lookup"><span data-stu-id="391c3-106">*psminfo*</span></span> 
</dt> <dd>

<span data-ttu-id="391c3-107">Pointeur vers une structure [**SMINFO**](/windows/win32/api/shobjidl_core/ns-shobjidl_core-sminfo) .</span><span class="sxs-lookup"><span data-stu-id="391c3-107">Pointer to a [**SMINFO**](/windows/win32/api/shobjidl_core/ns-shobjidl_core-sminfo) structure.</span></span> <span data-ttu-id="391c3-108">Remplissez la structure avec les informations appropriées et renvoyez \_ OK.</span><span class="sxs-lookup"><span data-stu-id="391c3-108">Fill the structure with the appropriate information and return S\_OK.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="391c3-109">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="391c3-109">Return value</span></span>

<span data-ttu-id="391c3-110">Retourne S \_ OK.</span><span class="sxs-lookup"><span data-stu-id="391c3-110">Return S\_OK.</span></span>

## <a name="remarks"></a><span data-ttu-id="391c3-111">Notes</span><span class="sxs-lookup"><span data-stu-id="391c3-111">Remarks</span></span>

<span data-ttu-id="391c3-112">Cette notification est reçue par la méthode [**IShellMenuCallback :: CallbackSM**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellmenucallback-callbacksm) .</span><span class="sxs-lookup"><span data-stu-id="391c3-112">This notification is received by the [**IShellMenuCallback::CallbackSM**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellmenucallback-callbacksm) method.</span></span>

## <a name="requirements"></a><span data-ttu-id="391c3-113">Spécifications</span><span class="sxs-lookup"><span data-stu-id="391c3-113">Requirements</span></span>



| <span data-ttu-id="391c3-114">Condition requise</span><span class="sxs-lookup"><span data-stu-id="391c3-114">Requirement</span></span> | <span data-ttu-id="391c3-115">Valeur</span><span class="sxs-lookup"><span data-stu-id="391c3-115">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="391c3-116">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="391c3-116">Minimum supported client</span></span><br/> | <span data-ttu-id="391c3-117">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="391c3-117">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="391c3-118">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="391c3-118">Minimum supported server</span></span><br/> | <span data-ttu-id="391c3-119">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="391c3-119">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="391c3-120">En-tête</span><span class="sxs-lookup"><span data-stu-id="391c3-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="391c3-121"><dt>ShObjIdl. h</dt></span><span class="sxs-lookup"><span data-stu-id="391c3-121"><dt>Shobjidl.h</dt></span></span> </dl>   |
| <span data-ttu-id="391c3-122">MIDL</span><span class="sxs-lookup"><span data-stu-id="391c3-122">IDL</span></span><br/>                      | <dl> <span data-ttu-id="391c3-123"><dt>ShObjIdl. idl</dt></span><span class="sxs-lookup"><span data-stu-id="391c3-123"><dt>Shobjidl.idl</dt></span></span> </dl> |



 

 




