---
description: L’utilisateur a cliqué sur un Chevron pour développer l’élément spécifié par la structure SMDATA qui l’accompagne.
title: Message SMC_CHEVRONEXPAND (ShObjIdl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: cb0b3cf1-1a12-4236-96e9-cc04360d269f
api_name:
- SMC_CHEVRONEXPAND
api_type:
- HeaderDef
api_location:
- Shobjidl.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 6ecf8f86e111326b3f37f3111c382d2d04ef2fa7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104203668"
---
# <a name="smc_chevronexpand-message"></a><span data-ttu-id="779ef-103">\_Message SMC CHEVRONEXPAND</span><span class="sxs-lookup"><span data-stu-id="779ef-103">SMC\_CHEVRONEXPAND message</span></span>

<span data-ttu-id="779ef-104">L’utilisateur a cliqué sur un Chevron pour développer l’élément spécifié par la structure [**SMDATA**](/windows/win32/api/shobjidl_core/ns-shobjidl_core-smdata) qui l’accompagne.</span><span class="sxs-lookup"><span data-stu-id="779ef-104">The user has clicked a chevron to expand the item specified by the accompanying [**SMDATA**](/windows/win32/api/shobjidl_core/ns-shobjidl_core-smdata) structure.</span></span>


```C++
SMC_CHEVRONEXPAND
            
```



## <a name="parameters"></a><span data-ttu-id="779ef-105">Paramètres</span><span class="sxs-lookup"><span data-stu-id="779ef-105">Parameters</span></span>

<span data-ttu-id="779ef-106">Ce message n’a pas de paramètres.</span><span class="sxs-lookup"><span data-stu-id="779ef-106">This message has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="779ef-107">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="779ef-107">Return value</span></span>

<span data-ttu-id="779ef-108">Retourne S \_ OK.</span><span class="sxs-lookup"><span data-stu-id="779ef-108">Return S\_OK.</span></span>

## <a name="remarks"></a><span data-ttu-id="779ef-109">Notes</span><span class="sxs-lookup"><span data-stu-id="779ef-109">Remarks</span></span>

<span data-ttu-id="779ef-110">Cette notification est reçue par la méthode [**IShellMenuCallback :: CallbackSM**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellmenucallback-callbacksm) .</span><span class="sxs-lookup"><span data-stu-id="779ef-110">This notification is received by the [**IShellMenuCallback::CallbackSM**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellmenucallback-callbacksm) method.</span></span>

## <a name="requirements"></a><span data-ttu-id="779ef-111">Spécifications</span><span class="sxs-lookup"><span data-stu-id="779ef-111">Requirements</span></span>



| <span data-ttu-id="779ef-112">Condition requise</span><span class="sxs-lookup"><span data-stu-id="779ef-112">Requirement</span></span> | <span data-ttu-id="779ef-113">Valeur</span><span class="sxs-lookup"><span data-stu-id="779ef-113">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="779ef-114">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="779ef-114">Minimum supported client</span></span><br/> | <span data-ttu-id="779ef-115">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="779ef-115">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="779ef-116">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="779ef-116">Minimum supported server</span></span><br/> | <span data-ttu-id="779ef-117">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="779ef-117">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="779ef-118">En-tête</span><span class="sxs-lookup"><span data-stu-id="779ef-118">Header</span></span><br/>                   | <dl> <span data-ttu-id="779ef-119"><dt>ShObjIdl. h</dt></span><span class="sxs-lookup"><span data-stu-id="779ef-119"><dt>Shobjidl.h</dt></span></span> </dl>   |
| <span data-ttu-id="779ef-120">MIDL</span><span class="sxs-lookup"><span data-stu-id="779ef-120">IDL</span></span><br/>                      | <dl> <span data-ttu-id="779ef-121"><dt>ShObjIdl. idl</dt></span><span class="sxs-lookup"><span data-stu-id="779ef-121"><dt>Shobjidl.idl</dt></span></span> </dl> |



 

 




