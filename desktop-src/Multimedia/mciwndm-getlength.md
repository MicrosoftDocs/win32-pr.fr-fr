---
title: Message MCIWNDM_GETLENGTH (VFW. h)
description: Le \_ message MCIWNDM GETLENGTH récupère la longueur du contenu ou du fichier actuellement utilisé par un périphérique MCI. Vous pouvez envoyer ce message explicitement ou à l’aide de la macro MCIWndGetLength.
ms.assetid: bee4d9fc-78eb-4577-98bb-d6c2d9acbb7f
keywords:
- Message MCIWNDM_GETLENGTH Windows Multimedia
topic_type:
- apiref
api_name:
- MCIWNDM_GETLENGTH
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2347647fcff0beb87be12b7f6a05790b97f36d51
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104464515"
---
# <a name="mciwndm_getlength-message"></a><span data-ttu-id="f5ecd-105">\_Message MCIWNDM GETLENGTH</span><span class="sxs-lookup"><span data-stu-id="f5ecd-105">MCIWNDM\_GETLENGTH message</span></span>

<span data-ttu-id="f5ecd-106">Le message **MCIWNDM \_ GETLENGTH** récupère la longueur du contenu ou du fichier actuellement utilisé par un périphérique MCI.</span><span class="sxs-lookup"><span data-stu-id="f5ecd-106">The **MCIWNDM\_GETLENGTH** message retrieves the length of the content or file currently used by an MCI device.</span></span> <span data-ttu-id="f5ecd-107">Vous pouvez envoyer ce message explicitement ou à l’aide de la macro [**MCIWndGetLength**](/windows/desktop/api/Vfw/nf-vfw-mciwndgetlength) .</span><span class="sxs-lookup"><span data-stu-id="f5ecd-107">You can send this message explicitly or by using the [**MCIWndGetLength**](/windows/desktop/api/Vfw/nf-vfw-mciwndgetlength) macro.</span></span>


```C++
MCIWNDM_GETLENGTH 
wParam = 0; 
lParam = 0; 
```



## <a name="return-value"></a><span data-ttu-id="f5ecd-108">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="f5ecd-108">Return Value</span></span>

<span data-ttu-id="f5ecd-109">Retourne la longueur.</span><span class="sxs-lookup"><span data-stu-id="f5ecd-109">Returns the length.</span></span> <span data-ttu-id="f5ecd-110">Les unités de la longueur dépendent du format d’heure actuel.</span><span class="sxs-lookup"><span data-stu-id="f5ecd-110">The units for the length depend on the current time format.</span></span>

## <a name="requirements"></a><span data-ttu-id="f5ecd-111">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="f5ecd-111">Requirements</span></span>



| <span data-ttu-id="f5ecd-112">Condition requise</span><span class="sxs-lookup"><span data-stu-id="f5ecd-112">Requirement</span></span> | <span data-ttu-id="f5ecd-113">Valeur</span><span class="sxs-lookup"><span data-stu-id="f5ecd-113">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="f5ecd-114">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="f5ecd-114">Minimum supported client</span></span><br/> | <span data-ttu-id="f5ecd-115">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="f5ecd-115">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="f5ecd-116">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="f5ecd-116">Minimum supported server</span></span><br/> | <span data-ttu-id="f5ecd-117">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="f5ecd-117">Windows 2000 Server \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="f5ecd-118">En-tête</span><span class="sxs-lookup"><span data-stu-id="f5ecd-118">Header</span></span><br/>                   | <dl> <span data-ttu-id="f5ecd-119"><dt>VFW. h</dt></span><span class="sxs-lookup"><span data-stu-id="f5ecd-119"><dt>Vfw.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f5ecd-120">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="f5ecd-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f5ecd-121">**MCIWndGetLength**</span><span class="sxs-lookup"><span data-stu-id="f5ecd-121">**MCIWndGetLength**</span></span>](/windows/desktop/api/Vfw/nf-vfw-mciwndgetlength)
</dt> </dl>

 

 





