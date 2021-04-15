---
title: Message MCIWNDM_CAN_CONFIG (VFW. h)
description: Le \_ message MCIWNDM CAN \_ config détermine si un périphérique MCI peut afficher une boîte de dialogue de configuration. Vous pouvez envoyer ce message explicitement ou à l’aide de la macro MCIWndCanConfig.
ms.assetid: f1eb22a8-d0fc-4d2c-a414-392e560cfbed
keywords:
- Message MCIWNDM_CAN_CONFIG Windows Multimedia
topic_type:
- apiref
api_name:
- MCIWNDM_CAN_CONFIG
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 816a8c1dfaec6fc7d7854f8873ce05e74e4de6bc
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104466922"
---
# <a name="mciwndm_can_config-message"></a><span data-ttu-id="f3e6f-105">MCIWNDM \_ peut \_ configurer un message</span><span class="sxs-lookup"><span data-stu-id="f3e6f-105">MCIWNDM\_CAN\_CONFIG message</span></span>

<span data-ttu-id="f3e6f-106">Le message **MCIWNDM \_ CAN \_ config** détermine si un périphérique MCI peut afficher une boîte de dialogue de configuration.</span><span class="sxs-lookup"><span data-stu-id="f3e6f-106">The **MCIWNDM\_CAN\_CONFIG** message determines if an MCI device can display a configuration dialog box.</span></span> <span data-ttu-id="f3e6f-107">Vous pouvez envoyer ce message explicitement ou à l’aide de la macro [**MCIWndCanConfig**](/windows/desktop/api/Vfw/nf-vfw-mciwndcanconfig) .</span><span class="sxs-lookup"><span data-stu-id="f3e6f-107">You can send this message explicitly or by using the [**MCIWndCanConfig**](/windows/desktop/api/Vfw/nf-vfw-mciwndcanconfig) macro.</span></span>


```C++
MCIWNDM_CAN_CONFIG 
wParam = 0; 
lParam = 0; 
```



## <a name="return-value"></a><span data-ttu-id="f3e6f-108">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="f3e6f-108">Return Value</span></span>

<span data-ttu-id="f3e6f-109">Retourne la **valeur true** si l’appareil prend en charge la configuration ou **false** dans le cas contraire.</span><span class="sxs-lookup"><span data-stu-id="f3e6f-109">Returns **TRUE** if the device supports configuration or **FALSE** otherwise.</span></span>

## <a name="requirements"></a><span data-ttu-id="f3e6f-110">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="f3e6f-110">Requirements</span></span>



| <span data-ttu-id="f3e6f-111">Condition requise</span><span class="sxs-lookup"><span data-stu-id="f3e6f-111">Requirement</span></span> | <span data-ttu-id="f3e6f-112">Valeur</span><span class="sxs-lookup"><span data-stu-id="f3e6f-112">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="f3e6f-113">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="f3e6f-113">Minimum supported client</span></span><br/> | <span data-ttu-id="f3e6f-114">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="f3e6f-114">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="f3e6f-115">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="f3e6f-115">Minimum supported server</span></span><br/> | <span data-ttu-id="f3e6f-116">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="f3e6f-116">Windows 2000 Server \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="f3e6f-117">En-tête</span><span class="sxs-lookup"><span data-stu-id="f3e6f-117">Header</span></span><br/>                   | <dl> <span data-ttu-id="f3e6f-118"><dt>VFW. h</dt></span><span class="sxs-lookup"><span data-stu-id="f3e6f-118"><dt>Vfw.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f3e6f-119">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="f3e6f-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f3e6f-120">**MCIWndCanConfig**</span><span class="sxs-lookup"><span data-stu-id="f3e6f-120">**MCIWndCanConfig**</span></span>](/windows/desktop/api/Vfw/nf-vfw-mciwndcanconfig)
</dt> </dl>

 

 





