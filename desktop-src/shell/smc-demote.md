---
description: Rétrograde l’élément spécifié par la structure SMDATA qui l’accompagne.
title: Message SMC_DEMOTE (ShObjIdl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 4809fbd1-da66-4453-b4f2-e75cb5b3457c
api_name:
- SMC_DEMOTE
api_type:
- HeaderDef
api_location:
- Shobjidl.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 46e5505571402feec24d81a9184b713e1c61ae0f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104991652"
---
# <a name="smc_demote-message"></a><span data-ttu-id="2e8be-103">\_Message SMC rétrograder</span><span class="sxs-lookup"><span data-stu-id="2e8be-103">SMC\_DEMOTE message</span></span>

<span data-ttu-id="2e8be-104">Rétrograde l’élément spécifié par la structure [**SMDATA**](/windows/win32/api/shobjidl_core/ns-shobjidl_core-smdata) qui l’accompagne.</span><span class="sxs-lookup"><span data-stu-id="2e8be-104">Demote the item specified by the accompanying [**SMDATA**](/windows/win32/api/shobjidl_core/ns-shobjidl_core-smdata) structure.</span></span>


```C++
SMC_DEMOTE
            
```



## <a name="parameters"></a><span data-ttu-id="2e8be-105">Paramètres</span><span class="sxs-lookup"><span data-stu-id="2e8be-105">Parameters</span></span>

<span data-ttu-id="2e8be-106">Ce message n’a pas de paramètres.</span><span class="sxs-lookup"><span data-stu-id="2e8be-106">This message has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="2e8be-107">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="2e8be-107">Return value</span></span>

<span data-ttu-id="2e8be-108">Retourne S \_ OK.</span><span class="sxs-lookup"><span data-stu-id="2e8be-108">Return S\_OK.</span></span>

## <a name="remarks"></a><span data-ttu-id="2e8be-109">Notes</span><span class="sxs-lookup"><span data-stu-id="2e8be-109">Remarks</span></span>

<span data-ttu-id="2e8be-110">Cette notification est reçue par la méthode [**IShellMenuCallback :: CallbackSM**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellmenucallback-callbacksm) .</span><span class="sxs-lookup"><span data-stu-id="2e8be-110">This notification is received by the [**IShellMenuCallback::CallbackSM**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellmenucallback-callbacksm) method.</span></span>

## <a name="requirements"></a><span data-ttu-id="2e8be-111">Spécifications</span><span class="sxs-lookup"><span data-stu-id="2e8be-111">Requirements</span></span>



| <span data-ttu-id="2e8be-112">Condition requise</span><span class="sxs-lookup"><span data-stu-id="2e8be-112">Requirement</span></span> | <span data-ttu-id="2e8be-113">Valeur</span><span class="sxs-lookup"><span data-stu-id="2e8be-113">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="2e8be-114">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="2e8be-114">Minimum supported client</span></span><br/> | <span data-ttu-id="2e8be-115">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="2e8be-115">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="2e8be-116">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="2e8be-116">Minimum supported server</span></span><br/> | <span data-ttu-id="2e8be-117">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="2e8be-117">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="2e8be-118">En-tête</span><span class="sxs-lookup"><span data-stu-id="2e8be-118">Header</span></span><br/>                   | <dl> <span data-ttu-id="2e8be-119"><dt>ShObjIdl. h</dt></span><span class="sxs-lookup"><span data-stu-id="2e8be-119"><dt>Shobjidl.h</dt></span></span> </dl>   |
| <span data-ttu-id="2e8be-120">MIDL</span><span class="sxs-lookup"><span data-stu-id="2e8be-120">IDL</span></span><br/>                      | <dl> <span data-ttu-id="2e8be-121"><dt>ShObjIdl. idl</dt></span><span class="sxs-lookup"><span data-stu-id="2e8be-121"><dt>Shobjidl.idl</dt></span></span> </dl> |



 

 




