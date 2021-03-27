---
description: Vous avertit que le menu se réduit.
title: Message SMC_EXITMENU (ShObjIdl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 868b4819-1dbf-497a-9c79-5935f503969a
api_name:
- SMC_EXITMENU
api_type:
- HeaderDef
api_location:
- Shobjidl.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: e9a8680617a17ce0069a8633e1c70ff6b32a4be7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103952332"
---
# <a name="smc_exitmenu-message"></a><span data-ttu-id="725b8-103">\_Message SMC EXITMENU</span><span class="sxs-lookup"><span data-stu-id="725b8-103">SMC\_EXITMENU message</span></span>

<span data-ttu-id="725b8-104">Vous avertit que le menu se réduit.</span><span class="sxs-lookup"><span data-stu-id="725b8-104">Notifies you that the menu is collapsing.</span></span>


```C++
SMC_EXITMENU
            
```



## <a name="parameters"></a><span data-ttu-id="725b8-105">Paramètres</span><span class="sxs-lookup"><span data-stu-id="725b8-105">Parameters</span></span>

<span data-ttu-id="725b8-106">Ce message n’a pas de paramètres.</span><span class="sxs-lookup"><span data-stu-id="725b8-106">This message has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="725b8-107">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="725b8-107">Return value</span></span>

<span data-ttu-id="725b8-108">Retourne S \_ OK.</span><span class="sxs-lookup"><span data-stu-id="725b8-108">Return S\_OK.</span></span>

## <a name="remarks"></a><span data-ttu-id="725b8-109">Notes</span><span class="sxs-lookup"><span data-stu-id="725b8-109">Remarks</span></span>

<span data-ttu-id="725b8-110">Cette notification est reçue par la méthode [**IShellMenuCallback :: CallbackSM**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellmenucallback-callbacksm) .</span><span class="sxs-lookup"><span data-stu-id="725b8-110">This notification is received by the [**IShellMenuCallback::CallbackSM**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellmenucallback-callbacksm) method.</span></span>

## <a name="requirements"></a><span data-ttu-id="725b8-111">Spécifications</span><span class="sxs-lookup"><span data-stu-id="725b8-111">Requirements</span></span>



| <span data-ttu-id="725b8-112">Condition requise</span><span class="sxs-lookup"><span data-stu-id="725b8-112">Requirement</span></span> | <span data-ttu-id="725b8-113">Valeur</span><span class="sxs-lookup"><span data-stu-id="725b8-113">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="725b8-114">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="725b8-114">Minimum supported client</span></span><br/> | <span data-ttu-id="725b8-115">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="725b8-115">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="725b8-116">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="725b8-116">Minimum supported server</span></span><br/> | <span data-ttu-id="725b8-117">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="725b8-117">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="725b8-118">En-tête</span><span class="sxs-lookup"><span data-stu-id="725b8-118">Header</span></span><br/>                   | <dl> <span data-ttu-id="725b8-119"><dt>ShObjIdl. h</dt></span><span class="sxs-lookup"><span data-stu-id="725b8-119"><dt>Shobjidl.h</dt></span></span> </dl>   |
| <span data-ttu-id="725b8-120">MIDL</span><span class="sxs-lookup"><span data-stu-id="725b8-120">IDL</span></span><br/>                      | <dl> <span data-ttu-id="725b8-121"><dt>ShObjIdl. idl</dt></span><span class="sxs-lookup"><span data-stu-id="725b8-121"><dt>Shobjidl.idl</dt></span></span> </dl> |



 

 




