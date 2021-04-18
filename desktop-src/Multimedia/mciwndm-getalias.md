---
title: Message MCIWNDM_GETALIAS (VFW. h)
description: Le \_ message MCIWNDM GETALIAS récupère l’alias utilisé pour ouvrir un fichier ou un périphérique MCI avec la fonction mciSendString. Vous pouvez envoyer ce message explicitement ou à l’aide de la macro MCIWndGetAlias.
ms.assetid: 37131b89-275c-4ab6-9278-0e08c42471bd
keywords:
- Message MCIWNDM_GETALIAS Windows Multimedia
topic_type:
- apiref
api_name:
- MCIWNDM_GETALIAS
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9e971c50b9abc450387ac29f9a7331bfdca5c38c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "106512143"
---
# <a name="mciwndm_getalias-message"></a><span data-ttu-id="439b6-105">\_Message MCIWNDM GETALIAS</span><span class="sxs-lookup"><span data-stu-id="439b6-105">MCIWNDM\_GETALIAS message</span></span>

<span data-ttu-id="439b6-106">Le message **MCIWNDM \_ GETALIAS** récupère l’alias utilisé pour ouvrir un fichier ou un périphérique MCI avec la fonction [**mciSendString**](/previous-versions//dd757161(v=vs.85)) .</span><span class="sxs-lookup"><span data-stu-id="439b6-106">The **MCIWNDM\_GETALIAS** message retrieves the alias used to open an MCI device or file with the [**mciSendString**](/previous-versions//dd757161(v=vs.85)) function.</span></span> <span data-ttu-id="439b6-107">Vous pouvez envoyer ce message explicitement ou à l’aide de la macro [**MCIWndGetAlias**](/windows/desktop/api/Vfw/nf-vfw-mciwndgetalias) .</span><span class="sxs-lookup"><span data-stu-id="439b6-107">You can send this message explicitly or by using the [**MCIWndGetAlias**](/windows/desktop/api/Vfw/nf-vfw-mciwndgetalias) macro.</span></span>


```C++
MCIWNDM_GETALIAS 
wParam = 0; 
lParam = 0; 
```



## <a name="return-value"></a><span data-ttu-id="439b6-108">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="439b6-108">Return Value</span></span>

<span data-ttu-id="439b6-109">Retourne l’alias de l’appareil.</span><span class="sxs-lookup"><span data-stu-id="439b6-109">Returns the device alias.</span></span>

## <a name="requirements"></a><span data-ttu-id="439b6-110">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="439b6-110">Requirements</span></span>



| <span data-ttu-id="439b6-111">Condition requise</span><span class="sxs-lookup"><span data-stu-id="439b6-111">Requirement</span></span> | <span data-ttu-id="439b6-112">Valeur</span><span class="sxs-lookup"><span data-stu-id="439b6-112">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="439b6-113">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="439b6-113">Minimum supported client</span></span><br/> | <span data-ttu-id="439b6-114">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="439b6-114">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="439b6-115">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="439b6-115">Minimum supported server</span></span><br/> | <span data-ttu-id="439b6-116">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="439b6-116">Windows 2000 Server \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="439b6-117">En-tête</span><span class="sxs-lookup"><span data-stu-id="439b6-117">Header</span></span><br/>                   | <dl> <span data-ttu-id="439b6-118"><dt>VFW. h</dt></span><span class="sxs-lookup"><span data-stu-id="439b6-118"><dt>Vfw.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="439b6-119">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="439b6-119">See also</span></span>

<dl> <dt>

<span data-ttu-id="439b6-120">[**mciSendString**](/previous-versions//dd757161(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="439b6-120">[**mciSendString**](/previous-versions//dd757161(v=vs.85))</span></span>
</dt> <dt>

[<span data-ttu-id="439b6-121">**MCIWndGetAlias**</span><span class="sxs-lookup"><span data-stu-id="439b6-121">**MCIWndGetAlias**</span></span>](/windows/desktop/api/Vfw/nf-vfw-mciwndgetalias)
</dt> </dl>

 

