---
title: Message MCIWNDM_GETFILENAME (VFW. h)
description: Le \_ message MCIWNDM GETFILENAME récupère le nom de fichier actuellement utilisé par un périphérique MCI. Vous pouvez envoyer ce message explicitement ou à l’aide de la macro MCIWndGetFileName.
ms.assetid: d61b1b6d-0fae-4732-993c-41e08a4e05be
keywords:
- Message MCIWNDM_GETFILENAME Windows Multimedia
topic_type:
- apiref
api_name:
- MCIWNDM_GETFILENAME
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 232a1d829b5cdd6da23e7dd3fb0294b95ca79f4b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104508341"
---
# <a name="mciwndm_getfilename-message"></a><span data-ttu-id="88213-105">\_Message MCIWNDM GETFILENAME</span><span class="sxs-lookup"><span data-stu-id="88213-105">MCIWNDM\_GETFILENAME message</span></span>

<span data-ttu-id="88213-106">Le message **MCIWNDM \_ GETFILENAME** récupère le nom de fichier actuellement utilisé par un périphérique MCI.</span><span class="sxs-lookup"><span data-stu-id="88213-106">The **MCIWNDM\_GETFILENAME** message retrieves the filename currently used by an MCI device.</span></span> <span data-ttu-id="88213-107">Vous pouvez envoyer ce message explicitement ou à l’aide de la macro [**MCIWndGetFileName**](/windows/desktop/api/Vfw/nf-vfw-mciwndgetfilename) .</span><span class="sxs-lookup"><span data-stu-id="88213-107">You can send this message explicitly or by using the [**MCIWndGetFileName**](/windows/desktop/api/Vfw/nf-vfw-mciwndgetfilename) macro.</span></span>


```C++
MCIWNDM_GETFILENAME 
wParam = (WPARAM) (UINT) len; 
lParam = (LPARAM) (LPVOID) lp; 
```



## <a name="parameters"></a><span data-ttu-id="88213-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="88213-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="88213-109"><span id="len"></span><span id="LEN"></span>*Len*</span><span class="sxs-lookup"><span data-stu-id="88213-109"><span id="len"></span><span id="LEN"></span>*len*</span></span>
</dt> <dd>

<span data-ttu-id="88213-110">Taille, en octets, de la mémoire tampon.</span><span class="sxs-lookup"><span data-stu-id="88213-110">Size, in bytes, of the buffer.</span></span>

</dd> <dt>

<span data-ttu-id="88213-111"><span id="lp"></span><span id="LP"></span>*Aid*</span><span class="sxs-lookup"><span data-stu-id="88213-111"><span id="lp"></span><span id="LP"></span>*lp*</span></span>
</dt> <dd>

<span data-ttu-id="88213-112">Pointeur vers une mémoire tampon définie par l’application pour retourner le nom de fichier.</span><span class="sxs-lookup"><span data-stu-id="88213-112">Pointer to an application-defined buffer to return the filename.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="88213-113">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="88213-113">Return Value</span></span>

<span data-ttu-id="88213-114">Retourne zéro en cas de réussite ou 1 dans le cas contraire.</span><span class="sxs-lookup"><span data-stu-id="88213-114">Returns zero if successful or 1 otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="88213-115">Notes</span><span class="sxs-lookup"><span data-stu-id="88213-115">Remarks</span></span>

<span data-ttu-id="88213-116">Si la chaîne se terminant par un caractère NULL contenant le nom de fichier est plus longue que la mémoire tampon, MCIWnd tronque le nom de fichier.</span><span class="sxs-lookup"><span data-stu-id="88213-116">If the null-terminated string containing the filename is longer than the buffer, MCIWnd truncates the filename.</span></span>

## <a name="requirements"></a><span data-ttu-id="88213-117">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="88213-117">Requirements</span></span>



| <span data-ttu-id="88213-118">Condition requise</span><span class="sxs-lookup"><span data-stu-id="88213-118">Requirement</span></span> | <span data-ttu-id="88213-119">Valeur</span><span class="sxs-lookup"><span data-stu-id="88213-119">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="88213-120">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="88213-120">Minimum supported client</span></span><br/> | <span data-ttu-id="88213-121">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="88213-121">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="88213-122">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="88213-122">Minimum supported server</span></span><br/> | <span data-ttu-id="88213-123">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="88213-123">Windows 2000 Server \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="88213-124">En-tête</span><span class="sxs-lookup"><span data-stu-id="88213-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="88213-125"><dt>VFW. h</dt></span><span class="sxs-lookup"><span data-stu-id="88213-125"><dt>Vfw.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="88213-126">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="88213-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="88213-127">**MCIWndGetFileName**</span><span class="sxs-lookup"><span data-stu-id="88213-127">**MCIWndGetFileName**</span></span>](/windows/desktop/api/Vfw/nf-vfw-mciwndgetfilename)
</dt> </dl>

 

 





