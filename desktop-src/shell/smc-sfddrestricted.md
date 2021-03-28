---
description: Demande s’il est acceptable de supprimer un objet de données sur l’élément spécifié par la structure SMDATA associée.
ms.assetid: 777bbc7e-6b0f-4627-9d92-4aa8209082ca
title: Message SMC_SFDDRESTRICTED (ShObjIdl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 77ae6a852fd342e67edf42429f31eb7e1ba3b566
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104973446"
---
# <a name="smc_sfddrestricted-message"></a><span data-ttu-id="1727b-103">\_Message SMC SFDDRESTRICTED</span><span class="sxs-lookup"><span data-stu-id="1727b-103">SMC\_SFDDRESTRICTED message</span></span>

<span data-ttu-id="1727b-104">Demande s’il est acceptable de supprimer un objet de données sur l’élément spécifié par la structure [**SMDATA**](/windows/win32/api/shobjidl_core/ns-shobjidl_core-smdata) associée.</span><span class="sxs-lookup"><span data-stu-id="1727b-104">Requests whether it is acceptable to drop a data object on the item specified by the accompanying [**SMDATA**](/windows/win32/api/shobjidl_core/ns-shobjidl_core-smdata) structure.</span></span>


```C++
SMC_SFDDRESTRICTED 
    wParam = (WPARAM) (void **) pDropTarget
            
```



## <a name="parameters"></a><span data-ttu-id="1727b-105">Paramètres</span><span class="sxs-lookup"><span data-stu-id="1727b-105">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1727b-106">*pDropTarget*</span><span class="sxs-lookup"><span data-stu-id="1727b-106">*pDropTarget*</span></span> 
</dt> <dd>

<span data-ttu-id="1727b-107">Adresse d’un pointeur void qui reçoit un pointeur vers votre interface [**IDropTarget**](/windows/win32/api/oleidl/nn-oleidl-idroptarget) .</span><span class="sxs-lookup"><span data-stu-id="1727b-107">The address of a void pointer that receives a pointer to your [**IDropTarget**](/windows/win32/api/oleidl/nn-oleidl-idroptarget) interface.</span></span> <span data-ttu-id="1727b-108">Définissez cette valeur sur **null** si vous ne souhaitez pas accepter l’objet de données.</span><span class="sxs-lookup"><span data-stu-id="1727b-108">Set this value to **NULL** if you do not want to accept the data object.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1727b-109">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="1727b-109">Return value</span></span>

<span data-ttu-id="1727b-110">Retourne S \_ OK.</span><span class="sxs-lookup"><span data-stu-id="1727b-110">Return S\_OK.</span></span>

## <a name="remarks"></a><span data-ttu-id="1727b-111">Notes</span><span class="sxs-lookup"><span data-stu-id="1727b-111">Remarks</span></span>

<span data-ttu-id="1727b-112">Cette notification est reçue par la méthode [**IShellMenuCallback :: CallbackSM**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellmenucallback-callbacksm) .</span><span class="sxs-lookup"><span data-stu-id="1727b-112">This notification is received by the [**IShellMenuCallback::CallbackSM**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellmenucallback-callbacksm) method.</span></span>

## <a name="requirements"></a><span data-ttu-id="1727b-113">Spécifications</span><span class="sxs-lookup"><span data-stu-id="1727b-113">Requirements</span></span>



| <span data-ttu-id="1727b-114">Condition requise</span><span class="sxs-lookup"><span data-stu-id="1727b-114">Requirement</span></span> | <span data-ttu-id="1727b-115">Valeur</span><span class="sxs-lookup"><span data-stu-id="1727b-115">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="1727b-116">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="1727b-116">Minimum supported client</span></span><br/> | <span data-ttu-id="1727b-117">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="1727b-117">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="1727b-118">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="1727b-118">Minimum supported server</span></span><br/> | <span data-ttu-id="1727b-119">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="1727b-119">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="1727b-120">En-tête</span><span class="sxs-lookup"><span data-stu-id="1727b-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="1727b-121"><dt>ShObjIdl. h</dt></span><span class="sxs-lookup"><span data-stu-id="1727b-121"><dt>Shobjidl.h</dt></span></span> </dl>   |
| <span data-ttu-id="1727b-122">MIDL</span><span class="sxs-lookup"><span data-stu-id="1727b-122">IDL</span></span><br/>                      | <dl> <span data-ttu-id="1727b-123"><dt>ShObjIdl. idl</dt></span><span class="sxs-lookup"><span data-stu-id="1727b-123"><dt>Shobjidl.idl</dt></span></span> </dl> |



 

 
