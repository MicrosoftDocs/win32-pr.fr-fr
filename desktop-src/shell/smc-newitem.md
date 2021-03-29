---
description: Vous avertit d’un nouvel élément, comme spécifié par la structure SMDATA qui l’accompagne.
title: Message SMC_NEWITEM (ShObjIdl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: e0ccf2db-cb46-469f-bc08-4b5100a410ba
api_name:
- SMC_NEWITEM
api_type:
- HeaderDef
api_location:
- Shobjidl.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: ebd8f1b6454a2fb592374b860811ebfc7a14f09d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104973451"
---
# <a name="smc_newitem-message"></a><span data-ttu-id="a7011-103">Message de SMC \_ NEWITEM</span><span class="sxs-lookup"><span data-stu-id="a7011-103">SMC\_NEWITEM message</span></span>

<span data-ttu-id="a7011-104">Vous avertit d’un nouvel élément, comme spécifié par la structure [**SMDATA**](/windows/win32/api/shobjidl_core/ns-shobjidl_core-smdata) qui l’accompagne.</span><span class="sxs-lookup"><span data-stu-id="a7011-104">Notifies you of a new item, as specified by the accompanying [**SMDATA**](/windows/win32/api/shobjidl_core/ns-shobjidl_core-smdata) structure.</span></span>


```C++
SMC_NEWITEM
            
```



## <a name="parameters"></a><span data-ttu-id="a7011-105">Paramètres</span><span class="sxs-lookup"><span data-stu-id="a7011-105">Parameters</span></span>

<span data-ttu-id="a7011-106">Ce message n’a pas de paramètres.</span><span class="sxs-lookup"><span data-stu-id="a7011-106">This message has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="a7011-107">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="a7011-107">Return value</span></span>

<span data-ttu-id="a7011-108">Retourne S \_ OK.</span><span class="sxs-lookup"><span data-stu-id="a7011-108">Return S\_OK.</span></span>

## <a name="remarks"></a><span data-ttu-id="a7011-109">Notes</span><span class="sxs-lookup"><span data-stu-id="a7011-109">Remarks</span></span>

<span data-ttu-id="a7011-110">Cette notification est reçue par la méthode [**IShellMenuCallback :: CallbackSM**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellmenucallback-callbacksm) .</span><span class="sxs-lookup"><span data-stu-id="a7011-110">This notification is received by the [**IShellMenuCallback::CallbackSM**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellmenucallback-callbacksm) method.</span></span>

## <a name="requirements"></a><span data-ttu-id="a7011-111">Spécifications</span><span class="sxs-lookup"><span data-stu-id="a7011-111">Requirements</span></span>



| <span data-ttu-id="a7011-112">Condition requise</span><span class="sxs-lookup"><span data-stu-id="a7011-112">Requirement</span></span> | <span data-ttu-id="a7011-113">Valeur</span><span class="sxs-lookup"><span data-stu-id="a7011-113">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="a7011-114">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="a7011-114">Minimum supported client</span></span><br/> | <span data-ttu-id="a7011-115">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="a7011-115">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="a7011-116">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="a7011-116">Minimum supported server</span></span><br/> | <span data-ttu-id="a7011-117">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="a7011-117">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="a7011-118">En-tête</span><span class="sxs-lookup"><span data-stu-id="a7011-118">Header</span></span><br/>                   | <dl> <span data-ttu-id="a7011-119"><dt>ShObjIdl. h</dt></span><span class="sxs-lookup"><span data-stu-id="a7011-119"><dt>Shobjidl.h</dt></span></span> </dl>   |
| <span data-ttu-id="a7011-120">MIDL</span><span class="sxs-lookup"><span data-stu-id="a7011-120">IDL</span></span><br/>                      | <dl> <span data-ttu-id="a7011-121"><dt>ShObjIdl. idl</dt></span><span class="sxs-lookup"><span data-stu-id="a7011-121"><dt>Shobjidl.idl</dt></span></span> </dl> |



 

 




