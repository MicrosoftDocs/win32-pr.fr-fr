---
title: Message MCIWNDM_GETDEVICE (VFW. h)
description: Le \_ message MCIWNDM GETDEVICE récupère le nom de l’appareil MCI actuellement ouvert. Vous pouvez envoyer ce message explicitement ou à l’aide de la macro MCIWndGetDevice.
ms.assetid: e69a73a6-a927-4536-98c7-ee7d5b16668a
keywords:
- Message MCIWNDM_GETDEVICE Windows Multimedia
topic_type:
- apiref
api_name:
- MCIWNDM_GETDEVICE
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 32664508a577db9d5a077e3cb4fd00aab34fbdf3
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104464519"
---
# <a name="mciwndm_getdevice-message"></a><span data-ttu-id="84c02-105">\_Message MCIWNDM GETDEVICE</span><span class="sxs-lookup"><span data-stu-id="84c02-105">MCIWNDM\_GETDEVICE message</span></span>

<span data-ttu-id="84c02-106">Le message **MCIWNDM \_ GETDEVICE** récupère le nom de l’appareil MCI actuellement ouvert.</span><span class="sxs-lookup"><span data-stu-id="84c02-106">The **MCIWNDM\_GETDEVICE** message retrieves the name of the currently open MCI device.</span></span> <span data-ttu-id="84c02-107">Vous pouvez envoyer ce message explicitement ou à l’aide de la macro [**MCIWndGetDevice**](/windows/desktop/api/Vfw/nf-vfw-mciwndgetdevice) .</span><span class="sxs-lookup"><span data-stu-id="84c02-107">You can send this message explicitly or by using the [**MCIWndGetDevice**](/windows/desktop/api/Vfw/nf-vfw-mciwndgetdevice) macro.</span></span>


```C++
MCIWNDM_GETDEVICE 
wParam = (WPARAM) (UINT) len; 
lParam = (LPARAM) (LPVOID) lp; 
```



## <a name="parameters"></a><span data-ttu-id="84c02-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="84c02-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="84c02-109"><span id="len"></span><span id="LEN"></span>*Len*</span><span class="sxs-lookup"><span data-stu-id="84c02-109"><span id="len"></span><span id="LEN"></span>*len*</span></span>
</dt> <dd>

<span data-ttu-id="84c02-110">Taille, en octets, de la mémoire tampon.</span><span class="sxs-lookup"><span data-stu-id="84c02-110">Size, in bytes, of the buffer.</span></span>

</dd> <dt>

<span data-ttu-id="84c02-111"><span id="lp"></span><span id="LP"></span>*Aid*</span><span class="sxs-lookup"><span data-stu-id="84c02-111"><span id="lp"></span><span id="LP"></span>*lp*</span></span>
</dt> <dd>

<span data-ttu-id="84c02-112">Pointeur vers une mémoire tampon définie par l’application pour retourner le nom de l’appareil.</span><span class="sxs-lookup"><span data-stu-id="84c02-112">Pointer to an application-defined buffer to return the device name.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="84c02-113">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="84c02-113">Return Value</span></span>

<span data-ttu-id="84c02-114">Retourne zéro en cas de réussite ou une valeur différente de zéro dans le cas contraire.</span><span class="sxs-lookup"><span data-stu-id="84c02-114">Returns zero if successful or a nonzero value otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="84c02-115">Notes</span><span class="sxs-lookup"><span data-stu-id="84c02-115">Remarks</span></span>

<span data-ttu-id="84c02-116">Si la chaîne se terminant par un caractère NULL contenant le nom de l’appareil est plus longue que la mémoire tampon, MCIWnd la tronque.</span><span class="sxs-lookup"><span data-stu-id="84c02-116">If the null-terminated string containing the device name is longer than the buffer, MCIWnd truncates it.</span></span>

## <a name="requirements"></a><span data-ttu-id="84c02-117">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="84c02-117">Requirements</span></span>



| <span data-ttu-id="84c02-118">Condition requise</span><span class="sxs-lookup"><span data-stu-id="84c02-118">Requirement</span></span> | <span data-ttu-id="84c02-119">Valeur</span><span class="sxs-lookup"><span data-stu-id="84c02-119">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="84c02-120">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="84c02-120">Minimum supported client</span></span><br/> | <span data-ttu-id="84c02-121">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="84c02-121">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="84c02-122">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="84c02-122">Minimum supported server</span></span><br/> | <span data-ttu-id="84c02-123">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="84c02-123">Windows 2000 Server \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="84c02-124">En-tête</span><span class="sxs-lookup"><span data-stu-id="84c02-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="84c02-125"><dt>VFW. h</dt></span><span class="sxs-lookup"><span data-stu-id="84c02-125"><dt>Vfw.h</dt></span></span> </dl> |



 

 





