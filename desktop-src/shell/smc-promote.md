---
description: Promouvoir l’élément spécifié par la structure SMDATA jointe.
title: Message SMC_PROMOTE (ShObjIdl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: b1208673-06b4-42b2-b4ac-872fd22927df
api_name:
- SMC_PROMOTE
api_type:
- HeaderDef
api_location:
- Shobjidl.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 22718e51d6ef1bf7e3c5652741b95cadb4db9937
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104973447"
---
# <a name="smc_promote-message"></a><span data-ttu-id="05fd5-103">\_Message de promotion SMC</span><span class="sxs-lookup"><span data-stu-id="05fd5-103">SMC\_PROMOTE message</span></span>

<span data-ttu-id="05fd5-104">Promouvoir l’élément spécifié par la structure [**SMDATA**](/windows/win32/api/shobjidl_core/ns-shobjidl_core-smdata) jointe.</span><span class="sxs-lookup"><span data-stu-id="05fd5-104">Promote the item specified by the accompanying [**SMDATA**](/windows/win32/api/shobjidl_core/ns-shobjidl_core-smdata) structure.</span></span>


```C++
SMC_PROMOTE
```



## <a name="parameters"></a><span data-ttu-id="05fd5-105">Paramètres</span><span class="sxs-lookup"><span data-stu-id="05fd5-105">Parameters</span></span>

<span data-ttu-id="05fd5-106">Ce message n’a pas de paramètres.</span><span class="sxs-lookup"><span data-stu-id="05fd5-106">This message has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="05fd5-107">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="05fd5-107">Return value</span></span>

<span data-ttu-id="05fd5-108">Retourne S \_ OK.</span><span class="sxs-lookup"><span data-stu-id="05fd5-108">Returns S\_OK.</span></span>

## <a name="remarks"></a><span data-ttu-id="05fd5-109">Notes</span><span class="sxs-lookup"><span data-stu-id="05fd5-109">Remarks</span></span>

<span data-ttu-id="05fd5-110">Cette notification est reçue par la méthode [**IShellMenuCallback :: CallbackSM**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellmenucallback-callbacksm) .</span><span class="sxs-lookup"><span data-stu-id="05fd5-110">This notification is received by the [**IShellMenuCallback::CallbackSM**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellmenucallback-callbacksm) method.</span></span>

## <a name="requirements"></a><span data-ttu-id="05fd5-111">Spécifications</span><span class="sxs-lookup"><span data-stu-id="05fd5-111">Requirements</span></span>



| <span data-ttu-id="05fd5-112">Condition requise</span><span class="sxs-lookup"><span data-stu-id="05fd5-112">Requirement</span></span> | <span data-ttu-id="05fd5-113">Valeur</span><span class="sxs-lookup"><span data-stu-id="05fd5-113">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="05fd5-114">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="05fd5-114">Minimum supported client</span></span><br/> | <span data-ttu-id="05fd5-115">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="05fd5-115">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="05fd5-116">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="05fd5-116">Minimum supported server</span></span><br/> | <span data-ttu-id="05fd5-117">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="05fd5-117">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="05fd5-118">En-tête</span><span class="sxs-lookup"><span data-stu-id="05fd5-118">Header</span></span><br/>                   | <dl> <span data-ttu-id="05fd5-119"><dt>ShObjIdl. h</dt></span><span class="sxs-lookup"><span data-stu-id="05fd5-119"><dt>Shobjidl.h</dt></span></span> </dl>   |
| <span data-ttu-id="05fd5-120">MIDL</span><span class="sxs-lookup"><span data-stu-id="05fd5-120">IDL</span></span><br/>                      | <dl> <span data-ttu-id="05fd5-121"><dt>ShObjIdl. idl</dt></span><span class="sxs-lookup"><span data-stu-id="05fd5-121"><dt>Shobjidl.idl</dt></span></span> </dl> |



 

 




