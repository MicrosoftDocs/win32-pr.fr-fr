---
title: Message MCIWNDM_GETERROR (VFW. h)
description: Le \_ message MCIWNDM GETERROR récupère la dernière erreur MCI rencontrée. Vous pouvez envoyer ce message explicitement ou à l’aide de la macro MCIWndGetError.
ms.assetid: f110a9b3-5b05-4bf0-85d1-b49ce7396222
keywords:
- Message MCIWNDM_GETERROR Windows Multimedia
topic_type:
- apiref
api_name:
- MCIWNDM_GETERROR
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5c2977bb079351824b48da21f4ba3cc2dc5afe7e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103843194"
---
# <a name="mciwndm_geterror-message"></a><span data-ttu-id="600de-105">\_Message MCIWNDM GETERROR</span><span class="sxs-lookup"><span data-stu-id="600de-105">MCIWNDM\_GETERROR message</span></span>

<span data-ttu-id="600de-106">Le message **MCIWNDM \_ GETERROR** récupère la dernière erreur MCI rencontrée.</span><span class="sxs-lookup"><span data-stu-id="600de-106">The **MCIWNDM\_GETERROR** message retrieves the last MCI error encountered.</span></span> <span data-ttu-id="600de-107">Vous pouvez envoyer ce message explicitement ou à l’aide de la macro [**MCIWndGetError**](/windows/desktop/api/Vfw/nf-vfw-mciwndgeterror) .</span><span class="sxs-lookup"><span data-stu-id="600de-107">You can send this message explicitly or by using the [**MCIWndGetError**](/windows/desktop/api/Vfw/nf-vfw-mciwndgeterror) macro.</span></span>


```C++
MCIWNDM_GETERROR 
wParam = (WPARAM) (UINT) len; 
lParam = (LPARAM) (LPVOID) lp; 
```



## <a name="parameters"></a><span data-ttu-id="600de-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="600de-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="600de-109"><span id="len"></span><span id="LEN"></span>*Len*</span><span class="sxs-lookup"><span data-stu-id="600de-109"><span id="len"></span><span id="LEN"></span>*len*</span></span>
</dt> <dd>

<span data-ttu-id="600de-110">Taille, en octets, de la mémoire tampon d’erreur.</span><span class="sxs-lookup"><span data-stu-id="600de-110">Size, in bytes, of the error buffer.</span></span>

</dd> <dt>

<span data-ttu-id="600de-111"><span id="lp"></span><span id="LP"></span>*Aid*</span><span class="sxs-lookup"><span data-stu-id="600de-111"><span id="lp"></span><span id="LP"></span>*lp*</span></span>
</dt> <dd>

<span data-ttu-id="600de-112">Pointeur vers une mémoire tampon définie par l’application utilisée pour retourner la chaîne d’erreur.</span><span class="sxs-lookup"><span data-stu-id="600de-112">Pointer to an application-defined buffer used to return the error string.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="600de-113">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="600de-113">Return Value</span></span>

<span data-ttu-id="600de-114">Retourne la valeur d’erreur entière en cas de réussite.</span><span class="sxs-lookup"><span data-stu-id="600de-114">Returns the integer error value if successful.</span></span>

## <a name="remarks"></a><span data-ttu-id="600de-115">Notes</span><span class="sxs-lookup"><span data-stu-id="600de-115">Remarks</span></span>

<span data-ttu-id="600de-116">Si *LP* est un pointeur valide, une chaîne se terminant par un caractère null qui correspond à l’erreur est retournée dans sa mémoire tampon.</span><span class="sxs-lookup"><span data-stu-id="600de-116">If *lp* is a valid pointer, a null-terminated string corresponding to the error is returned in its buffer.</span></span> <span data-ttu-id="600de-117">Si la chaîne d’erreur est plus longue que la mémoire tampon, MCIWnd la tronque.</span><span class="sxs-lookup"><span data-stu-id="600de-117">If the error string is longer than the buffer, MCIWnd truncates it.</span></span>

## <a name="requirements"></a><span data-ttu-id="600de-118">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="600de-118">Requirements</span></span>



| <span data-ttu-id="600de-119">Condition requise</span><span class="sxs-lookup"><span data-stu-id="600de-119">Requirement</span></span> | <span data-ttu-id="600de-120">Valeur</span><span class="sxs-lookup"><span data-stu-id="600de-120">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="600de-121">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="600de-121">Minimum supported client</span></span><br/> | <span data-ttu-id="600de-122">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="600de-122">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="600de-123">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="600de-123">Minimum supported server</span></span><br/> | <span data-ttu-id="600de-124">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="600de-124">Windows 2000 Server \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="600de-125">En-tête</span><span class="sxs-lookup"><span data-stu-id="600de-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="600de-126"><dt>VFW. h</dt></span><span class="sxs-lookup"><span data-stu-id="600de-126"><dt>Vfw.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="600de-127">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="600de-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="600de-128">**MCIWndGetError**</span><span class="sxs-lookup"><span data-stu-id="600de-128">**MCIWndGetError**</span></span>](/windows/desktop/api/Vfw/nf-vfw-mciwndgeterror)
</dt> </dl>

 

 





