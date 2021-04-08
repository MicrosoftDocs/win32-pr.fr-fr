---
title: Message MCIWNDM_GETEND (VFW. h)
description: Le \_ message MCIWNDM GETEND récupère l’emplacement de la fin du contenu d’un périphérique ou d’un fichier MCI. Vous pouvez envoyer ce message explicitement ou à l’aide de la macro MCIWndGetEnd.
ms.assetid: 3fa45928-af63-4f87-835d-f409011a797e
keywords:
- Message MCIWNDM_GETEND Windows Multimedia
topic_type:
- apiref
api_name:
- MCIWNDM_GETEND
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 00d18057619e31fa9b22d7f6354527c394c02798
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103844225"
---
# <a name="mciwndm_getend-message"></a><span data-ttu-id="1df72-105">\_Message MCIWNDM GETEND</span><span class="sxs-lookup"><span data-stu-id="1df72-105">MCIWNDM\_GETEND message</span></span>

<span data-ttu-id="1df72-106">Le message **MCIWNDM \_ GETEND** récupère l’emplacement de la fin du contenu d’un périphérique ou d’un fichier MCI.</span><span class="sxs-lookup"><span data-stu-id="1df72-106">The **MCIWNDM\_GETEND** message retrieves the location of the end of the content of an MCI device or file.</span></span> <span data-ttu-id="1df72-107">Vous pouvez envoyer ce message explicitement ou à l’aide de la macro [**MCIWndGetEnd**](/windows/desktop/api/Vfw/nf-vfw-mciwndgetend) .</span><span class="sxs-lookup"><span data-stu-id="1df72-107">You can send this message explicitly or by using the [**MCIWndGetEnd**](/windows/desktop/api/Vfw/nf-vfw-mciwndgetend) macro.</span></span>


```C++
MCIWNDM_GETEND 
wParam = 0; 
lParam = 0; 
```



## <a name="return-value"></a><span data-ttu-id="1df72-108">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="1df72-108">Return Value</span></span>

<span data-ttu-id="1df72-109">Retourne l’emplacement au format d’heure actuel.</span><span class="sxs-lookup"><span data-stu-id="1df72-109">Returns the location in the current time format.</span></span>

## <a name="requirements"></a><span data-ttu-id="1df72-110">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="1df72-110">Requirements</span></span>



| <span data-ttu-id="1df72-111">Condition requise</span><span class="sxs-lookup"><span data-stu-id="1df72-111">Requirement</span></span> | <span data-ttu-id="1df72-112">Valeur</span><span class="sxs-lookup"><span data-stu-id="1df72-112">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="1df72-113">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="1df72-113">Minimum supported client</span></span><br/> | <span data-ttu-id="1df72-114">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="1df72-114">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="1df72-115">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="1df72-115">Minimum supported server</span></span><br/> | <span data-ttu-id="1df72-116">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="1df72-116">Windows 2000 Server \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="1df72-117">En-tête</span><span class="sxs-lookup"><span data-stu-id="1df72-117">Header</span></span><br/>                   | <dl> <span data-ttu-id="1df72-118"><dt>VFW. h</dt></span><span class="sxs-lookup"><span data-stu-id="1df72-118"><dt>Vfw.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1df72-119">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="1df72-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1df72-120">**MCIWndGetEnd**</span><span class="sxs-lookup"><span data-stu-id="1df72-120">**MCIWndGetEnd**</span></span>](/windows/desktop/api/Vfw/nf-vfw-mciwndgetend)
</dt> </dl>

 

 





