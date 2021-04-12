---
title: Message MCIWNDM_RETURNSTRING (VFW. h)
description: Le \_ message MCIWNDM RETURNSTRING récupère la réponse à la commande de chaîne MCI la plus récente envoyée à un périphérique MCI.
ms.assetid: 36a5222c-a63c-4b8c-ad0c-a00477e95b96
keywords:
- Message MCIWNDM_RETURNSTRING Windows Multimedia
topic_type:
- apiref
api_name:
- MCIWNDM_RETURNSTRING
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7b99307bd7d61a70db594d0a696cceccd6d246a3
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104032832"
---
# <a name="mciwndm_returnstring-message"></a><span data-ttu-id="cba2f-104">\_Message MCIWNDM RETURNSTRING</span><span class="sxs-lookup"><span data-stu-id="cba2f-104">MCIWNDM\_RETURNSTRING message</span></span>

<span data-ttu-id="cba2f-105">Le message **MCIWNDM \_ RETURNSTRING** récupère la réponse à la commande de chaîne MCI la plus récente envoyée à un périphérique MCI.</span><span class="sxs-lookup"><span data-stu-id="cba2f-105">The **MCIWNDM\_RETURNSTRING** message retrieves the reply to the most recent MCI string command sent to an MCI device.</span></span> <span data-ttu-id="cba2f-106">Les informations contenues dans la réponse sont fournies sous la forme d’une chaîne terminée par le caractère null.</span><span class="sxs-lookup"><span data-stu-id="cba2f-106">Information in the reply is supplied as a null-terminated string.</span></span> <span data-ttu-id="cba2f-107">Vous pouvez envoyer ce message explicitement ou à l’aide de la macro [**MCIWndReturnString**](/windows/desktop/api/Vfw/nf-vfw-mciwndreturnstring) .</span><span class="sxs-lookup"><span data-stu-id="cba2f-107">You can send this message explicitly or by using the [**MCIWndReturnString**](/windows/desktop/api/Vfw/nf-vfw-mciwndreturnstring) macro.</span></span>


```C++
MCIWNDM_RETURNSTRING 
wParam = (WPARAM) (UINT) len; 
lParam = (LPARAM) (LPVOID) lp; 
```



## <a name="parameters"></a><span data-ttu-id="cba2f-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="cba2f-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="cba2f-109"><span id="len"></span><span id="LEN"></span>*Len*</span><span class="sxs-lookup"><span data-stu-id="cba2f-109"><span id="len"></span><span id="LEN"></span>*len*</span></span>
</dt> <dd>

<span data-ttu-id="cba2f-110">Taille, en octets, de la mémoire tampon.</span><span class="sxs-lookup"><span data-stu-id="cba2f-110">Size, in bytes, of the buffer.</span></span>

</dd> <dt>

<span data-ttu-id="cba2f-111"><span id="lp"></span><span id="LP"></span>*Aid*</span><span class="sxs-lookup"><span data-stu-id="cba2f-111"><span id="lp"></span><span id="LP"></span>*lp*</span></span>
</dt> <dd>

<span data-ttu-id="cba2f-112">Pointeur vers une mémoire tampon définie par l’application devant contenir la chaîne terminée par le caractère null.</span><span class="sxs-lookup"><span data-stu-id="cba2f-112">Pointer to an application-defined buffer to contain the null-terminated string.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="cba2f-113">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="cba2f-113">Return Value</span></span>

<span data-ttu-id="cba2f-114">Retourne un entier correspondant à la chaîne MCI.</span><span class="sxs-lookup"><span data-stu-id="cba2f-114">Returns an integer corresponding to the MCI string.</span></span>

## <a name="remarks"></a><span data-ttu-id="cba2f-115">Notes</span><span class="sxs-lookup"><span data-stu-id="cba2f-115">Remarks</span></span>

<span data-ttu-id="cba2f-116">Si la chaîne se terminant par un caractère NULL est plus longue que la mémoire tampon, la chaîne est tronquée.</span><span class="sxs-lookup"><span data-stu-id="cba2f-116">If the null-terminated string is longer than the buffer, the string is truncated.</span></span>

## <a name="requirements"></a><span data-ttu-id="cba2f-117">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="cba2f-117">Requirements</span></span>



| <span data-ttu-id="cba2f-118">Condition requise</span><span class="sxs-lookup"><span data-stu-id="cba2f-118">Requirement</span></span> | <span data-ttu-id="cba2f-119">Valeur</span><span class="sxs-lookup"><span data-stu-id="cba2f-119">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="cba2f-120">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="cba2f-120">Minimum supported client</span></span><br/> | <span data-ttu-id="cba2f-121">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="cba2f-121">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="cba2f-122">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="cba2f-122">Minimum supported server</span></span><br/> | <span data-ttu-id="cba2f-123">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="cba2f-123">Windows 2000 Server \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="cba2f-124">En-tête</span><span class="sxs-lookup"><span data-stu-id="cba2f-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="cba2f-125"><dt>VFW. h</dt></span><span class="sxs-lookup"><span data-stu-id="cba2f-125"><dt>Vfw.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="cba2f-126">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="cba2f-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cba2f-127">**MCIWndReturnString**</span><span class="sxs-lookup"><span data-stu-id="cba2f-127">**MCIWndReturnString**</span></span>](/windows/desktop/api/Vfw/nf-vfw-mciwndreturnstring)
</dt> </dl>

 

 





