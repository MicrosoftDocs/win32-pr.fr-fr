---
description: Vous avertit qu’une info-bulle est sur le point d’être affichée pour le Chevron associé à l’élément spécifié par la structure SMDATA qui l’accompagne.
title: Message SMC_DISPLAYCHEVRONTIP (ShObjIdl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: e4ec4839-e49a-4563-9bc9-79f9d4d54658
api_name:
- SMC_DISPLAYCHEVRONTIP
api_type:
- HeaderDef
api_location:
- Shobjidl.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 09e01fc6ea169d8dcbf5758ace341198166a3a9e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104485505"
---
# <a name="smc_displaychevrontip-message"></a><span data-ttu-id="3b879-103">\_Message SMC DISPLAYCHEVRONTIP</span><span class="sxs-lookup"><span data-stu-id="3b879-103">SMC\_DISPLAYCHEVRONTIP message</span></span>

<span data-ttu-id="3b879-104">Vous avertit qu’une info-bulle est sur le point d’être affichée pour le Chevron associé à l’élément spécifié par la structure [**SMDATA**](/windows/win32/api/shobjidl_core/ns-shobjidl_core-smdata) qui l’accompagne.</span><span class="sxs-lookup"><span data-stu-id="3b879-104">Notifies you that an infotip is about to be displayed for the chevron associated with the item specified by the accompanying [**SMDATA**](/windows/win32/api/shobjidl_core/ns-shobjidl_core-smdata) structure.</span></span>


```C++
SMC_DISPLAYCHEVRONTIP
            
```



## <a name="parameters"></a><span data-ttu-id="3b879-105">Paramètres</span><span class="sxs-lookup"><span data-stu-id="3b879-105">Parameters</span></span>

<span data-ttu-id="3b879-106">Ce message n’a pas de paramètres.</span><span class="sxs-lookup"><span data-stu-id="3b879-106">This message has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="3b879-107">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="3b879-107">Return value</span></span>

<span data-ttu-id="3b879-108">Return \_ OK pour afficher l’info-bulle.</span><span class="sxs-lookup"><span data-stu-id="3b879-108">Return S\_OK to display the infotip.</span></span> <span data-ttu-id="3b879-109">Retourne \_ la valeur false pour empêcher l’affichage de l’info-bulle.</span><span class="sxs-lookup"><span data-stu-id="3b879-109">Return S\_FALSE to prevent the infotip from being displayed.</span></span>

## <a name="remarks"></a><span data-ttu-id="3b879-110">Notes</span><span class="sxs-lookup"><span data-stu-id="3b879-110">Remarks</span></span>

<span data-ttu-id="3b879-111">Cette notification est reçue par la méthode [**IShellMenuCallback :: CallbackSM**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellmenucallback-callbacksm) .</span><span class="sxs-lookup"><span data-stu-id="3b879-111">This notification is received by the [**IShellMenuCallback::CallbackSM**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellmenucallback-callbacksm) method.</span></span>

## <a name="requirements"></a><span data-ttu-id="3b879-112">Spécifications</span><span class="sxs-lookup"><span data-stu-id="3b879-112">Requirements</span></span>



| <span data-ttu-id="3b879-113">Condition requise</span><span class="sxs-lookup"><span data-stu-id="3b879-113">Requirement</span></span> | <span data-ttu-id="3b879-114">Valeur</span><span class="sxs-lookup"><span data-stu-id="3b879-114">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="3b879-115">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="3b879-115">Minimum supported client</span></span><br/> | <span data-ttu-id="3b879-116">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="3b879-116">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="3b879-117">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="3b879-117">Minimum supported server</span></span><br/> | <span data-ttu-id="3b879-118">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="3b879-118">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="3b879-119">En-tête</span><span class="sxs-lookup"><span data-stu-id="3b879-119">Header</span></span><br/>                   | <dl> <span data-ttu-id="3b879-120"><dt>ShObjIdl. h</dt></span><span class="sxs-lookup"><span data-stu-id="3b879-120"><dt>Shobjidl.h</dt></span></span> </dl>   |
| <span data-ttu-id="3b879-121">MIDL</span><span class="sxs-lookup"><span data-stu-id="3b879-121">IDL</span></span><br/>                      | <dl> <span data-ttu-id="3b879-122"><dt>ShObjIdl. idl</dt></span><span class="sxs-lookup"><span data-stu-id="3b879-122"><dt>Shobjidl.idl</dt></span></span> </dl> |



 

 




