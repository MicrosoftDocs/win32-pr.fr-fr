---
description: Envoie une notification indiquant que les menus ont été complètement actualisés et que vous pouvez réinitialiser votre état.
title: Message SMC_REFRESH (ShObjIdl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 8c79d9d5-b7dc-4271-9edb-93b40606c9be
api_name:
- SMC_REFRESH
api_type:
- HeaderDef
api_location:
- Shobjidl.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: aab18245c6502d4d3424e6ed6727eceb5a329d48
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103866538"
---
# <a name="smc_refresh-message"></a><span data-ttu-id="388e0-103">\_Message d’actualisation SMC</span><span class="sxs-lookup"><span data-stu-id="388e0-103">SMC\_REFRESH message</span></span>

<span data-ttu-id="388e0-104">Envoie une notification indiquant que les menus ont été complètement actualisés et que vous pouvez réinitialiser votre état.</span><span class="sxs-lookup"><span data-stu-id="388e0-104">Sends notification that the menus have completely refreshed and you can reset your state.</span></span>


```C++
SMC_REFRESH
            
```



## <a name="parameters"></a><span data-ttu-id="388e0-105">Paramètres</span><span class="sxs-lookup"><span data-stu-id="388e0-105">Parameters</span></span>

<span data-ttu-id="388e0-106">Ce message n’a pas de paramètres.</span><span class="sxs-lookup"><span data-stu-id="388e0-106">This message has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="388e0-107">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="388e0-107">Return value</span></span>

<span data-ttu-id="388e0-108">Retourne S \_ OK.</span><span class="sxs-lookup"><span data-stu-id="388e0-108">Return S\_OK.</span></span>

## <a name="remarks"></a><span data-ttu-id="388e0-109">Notes</span><span class="sxs-lookup"><span data-stu-id="388e0-109">Remarks</span></span>

<span data-ttu-id="388e0-110">Cette notification est reçue par la méthode [**IShellMenuCallback :: CallbackSM**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellmenucallback-callbacksm) .</span><span class="sxs-lookup"><span data-stu-id="388e0-110">This notification is received by the [**IShellMenuCallback::CallbackSM**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellmenucallback-callbacksm) method.</span></span>

## <a name="requirements"></a><span data-ttu-id="388e0-111">Spécifications</span><span class="sxs-lookup"><span data-stu-id="388e0-111">Requirements</span></span>



| <span data-ttu-id="388e0-112">Condition requise</span><span class="sxs-lookup"><span data-stu-id="388e0-112">Requirement</span></span> | <span data-ttu-id="388e0-113">Valeur</span><span class="sxs-lookup"><span data-stu-id="388e0-113">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="388e0-114">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="388e0-114">Minimum supported client</span></span><br/> | <span data-ttu-id="388e0-115">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="388e0-115">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="388e0-116">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="388e0-116">Minimum supported server</span></span><br/> | <span data-ttu-id="388e0-117">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="388e0-117">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="388e0-118">En-tête</span><span class="sxs-lookup"><span data-stu-id="388e0-118">Header</span></span><br/>                   | <dl> <span data-ttu-id="388e0-119"><dt>ShObjIdl. h</dt></span><span class="sxs-lookup"><span data-stu-id="388e0-119"><dt>Shobjidl.h</dt></span></span> </dl>   |
| <span data-ttu-id="388e0-120">MIDL</span><span class="sxs-lookup"><span data-stu-id="388e0-120">IDL</span></span><br/>                      | <dl> <span data-ttu-id="388e0-121"><dt>ShObjIdl. idl</dt></span><span class="sxs-lookup"><span data-stu-id="388e0-121"><dt>Shobjidl.idl</dt></span></span> </dl> |



 

 




