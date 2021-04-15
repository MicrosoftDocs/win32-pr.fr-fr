---
title: Message MCIWNDM_VALIDATEMEDIA (VFW. h)
description: Le \_ message MCIWNDM VALIDATEMEDIA met à jour les emplacements de début et de fin du contenu, la position actuelle dans le contenu et le TrackBar en fonction du format d’heure actuel.
ms.assetid: 98ac6227-fc90-4276-8e26-2bd005e35dc6
keywords:
- Message MCIWNDM_VALIDATEMEDIA Windows Multimedia
topic_type:
- apiref
api_name:
- MCIWNDM_VALIDATEMEDIA
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 43cb6e6a4a7c320d4eb6472c3c72da2843d0814c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104508330"
---
# <a name="mciwndm_validatemedia-message"></a><span data-ttu-id="8d66a-104">\_Message MCIWNDM VALIDATEMEDIA</span><span class="sxs-lookup"><span data-stu-id="8d66a-104">MCIWNDM\_VALIDATEMEDIA message</span></span>

<span data-ttu-id="8d66a-105">Le message **MCIWNDM \_ VALIDATEMEDIA** met à jour les emplacements de début et de fin du contenu, la position actuelle dans le contenu et le TrackBar en fonction du format d’heure actuel.</span><span class="sxs-lookup"><span data-stu-id="8d66a-105">The **MCIWNDM\_VALIDATEMEDIA** message updates the starting and ending locations of the content, the current position in the content, and the trackbar according to the current time format.</span></span> <span data-ttu-id="8d66a-106">Vous pouvez envoyer ce message explicitement ou à l’aide de la macro [**MCIWndValidateMedia**](/windows/desktop/api/Vfw/nf-vfw-mciwndvalidatemedia) .</span><span class="sxs-lookup"><span data-stu-id="8d66a-106">You can send this message explicitly or by using the [**MCIWndValidateMedia**](/windows/desktop/api/Vfw/nf-vfw-mciwndvalidatemedia) macro.</span></span>


```C++
MCIWNDM_VALIDATEMEDIA 
wParam = 0; 
lParam = 0; 
```



## <a name="return-value"></a><span data-ttu-id="8d66a-107">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="8d66a-107">Return Value</span></span>

<span data-ttu-id="8d66a-108">Ce message ne retourne pas de valeur.</span><span class="sxs-lookup"><span data-stu-id="8d66a-108">This message does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="8d66a-109">Notes</span><span class="sxs-lookup"><span data-stu-id="8d66a-109">Remarks</span></span>

<span data-ttu-id="8d66a-110">En règle générale, vous n’avez pas besoin d’utiliser cette macro. Toutefois, si votre application modifie le format d’heure d’un appareil sans utiliser MCIWnd ; les emplacements de début et de fin du contenu, ainsi que le TrackBar, continuent à utiliser l’ancien format.</span><span class="sxs-lookup"><span data-stu-id="8d66a-110">Typically, you should not need to use this macro; however, if your application changes the time format of a device without using MCIWnd; the starting and ending locations of the content, as well as the trackbar, continue to use the old format.</span></span> <span data-ttu-id="8d66a-111">Vous pouvez utiliser cette macro pour mettre à jour ces valeurs.</span><span class="sxs-lookup"><span data-stu-id="8d66a-111">You can use this macro to update these values.</span></span>

## <a name="requirements"></a><span data-ttu-id="8d66a-112">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="8d66a-112">Requirements</span></span>



| <span data-ttu-id="8d66a-113">Condition requise</span><span class="sxs-lookup"><span data-stu-id="8d66a-113">Requirement</span></span> | <span data-ttu-id="8d66a-114">Valeur</span><span class="sxs-lookup"><span data-stu-id="8d66a-114">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="8d66a-115">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="8d66a-115">Minimum supported client</span></span><br/> | <span data-ttu-id="8d66a-116">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="8d66a-116">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="8d66a-117">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="8d66a-117">Minimum supported server</span></span><br/> | <span data-ttu-id="8d66a-118">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="8d66a-118">Windows 2000 Server \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="8d66a-119">En-tête</span><span class="sxs-lookup"><span data-stu-id="8d66a-119">Header</span></span><br/>                   | <dl> <span data-ttu-id="8d66a-120"><dt>VFW. h</dt></span><span class="sxs-lookup"><span data-stu-id="8d66a-120"><dt>Vfw.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8d66a-121">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="8d66a-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8d66a-122">**MCIWndValidateMedia**</span><span class="sxs-lookup"><span data-stu-id="8d66a-122">**MCIWndValidateMedia**</span></span>](/windows/desktop/api/Vfw/nf-vfw-mciwndvalidatemedia)
</dt> </dl>

 

 





