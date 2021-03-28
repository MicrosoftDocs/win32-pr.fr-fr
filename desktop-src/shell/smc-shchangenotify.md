---
description: Vous avertit qu’une modification a eu lieu.
title: Message SMC_SHCHANGENOTIFY (ShObjIdl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 8232f170-0dab-475a-ace0-67c04f01c777
api_name:
- SMC_SHCHANGENOTIFY
api_type:
- HeaderDef
api_location:
- Shobjidl.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 258a885ddaf61b45df1cfff9f9c77ce37a233dd0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104973274"
---
# <a name="smc_shchangenotify-message"></a><span data-ttu-id="f9443-103">\_Message SMC SHCHANGENOTIFY</span><span class="sxs-lookup"><span data-stu-id="f9443-103">SMC\_SHCHANGENOTIFY message</span></span>

<span data-ttu-id="f9443-104">Vous avertit qu’une modification a eu lieu.</span><span class="sxs-lookup"><span data-stu-id="f9443-104">Notifies you that a change has taken place.</span></span>


```C++
SMC_SHCHANGENOTIFY
    lParam = (LPARAM) (PSMCSCHANGENOTIFYSTRUCT) psmc
            
```



## <a name="parameters"></a><span data-ttu-id="f9443-105">Paramètres</span><span class="sxs-lookup"><span data-stu-id="f9443-105">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f9443-106">*psmc*</span><span class="sxs-lookup"><span data-stu-id="f9443-106">*psmc*</span></span> 
</dt> <dd>

<span data-ttu-id="f9443-107">Pointeur vers une structure [**SMCSHCHANGENOTIFYSTRUCT**](/windows/win32/api/shobjidl_core/ns-shobjidl_core-smcshchangenotifystruct) avec des informations sur la modification.</span><span class="sxs-lookup"><span data-stu-id="f9443-107">A pointer to an [**SMCSHCHANGENOTIFYSTRUCT**](/windows/win32/api/shobjidl_core/ns-shobjidl_core-smcshchangenotifystruct) structure with information on the change.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f9443-108">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="f9443-108">Return value</span></span>

<span data-ttu-id="f9443-109">Retourne S \_ OK.</span><span class="sxs-lookup"><span data-stu-id="f9443-109">Return S\_OK.</span></span>

## <a name="remarks"></a><span data-ttu-id="f9443-110">Notes</span><span class="sxs-lookup"><span data-stu-id="f9443-110">Remarks</span></span>

<span data-ttu-id="f9443-111">Cette notification est reçue par la méthode [**IShellMenuCallback :: CallbackSM**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellmenucallback-callbacksm) .</span><span class="sxs-lookup"><span data-stu-id="f9443-111">This notification is received by the [**IShellMenuCallback::CallbackSM**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellmenucallback-callbacksm) method.</span></span>

## <a name="requirements"></a><span data-ttu-id="f9443-112">Spécifications</span><span class="sxs-lookup"><span data-stu-id="f9443-112">Requirements</span></span>



| <span data-ttu-id="f9443-113">Condition requise</span><span class="sxs-lookup"><span data-stu-id="f9443-113">Requirement</span></span> | <span data-ttu-id="f9443-114">Valeur</span><span class="sxs-lookup"><span data-stu-id="f9443-114">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="f9443-115">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="f9443-115">Minimum supported client</span></span><br/> | <span data-ttu-id="f9443-116">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="f9443-116">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="f9443-117">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="f9443-117">Minimum supported server</span></span><br/> | <span data-ttu-id="f9443-118">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="f9443-118">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="f9443-119">En-tête</span><span class="sxs-lookup"><span data-stu-id="f9443-119">Header</span></span><br/>                   | <dl> <span data-ttu-id="f9443-120"><dt>ShObjIdl. h</dt></span><span class="sxs-lookup"><span data-stu-id="f9443-120"><dt>Shobjidl.h</dt></span></span> </dl>   |
| <span data-ttu-id="f9443-121">MIDL</span><span class="sxs-lookup"><span data-stu-id="f9443-121">IDL</span></span><br/>                      | <dl> <span data-ttu-id="f9443-122"><dt>ShObjIdl. idl</dt></span><span class="sxs-lookup"><span data-stu-id="f9443-122"><dt>Shobjidl.idl</dt></span></span> </dl> |



 

 




