---
title: Message MCIWNDM_NOTIFYMODE (VFW. h)
description: Le \_ message MCIWNDM NOTIFYMODE notifie la fenêtre parente d’une application que le mode d’opération du périphérique MCI a changé.
ms.assetid: 08adfa8b-4d88-4953-acd8-8a4728f9e1b6
keywords:
- Message MCIWNDM_NOTIFYMODE Windows Multimedia
topic_type:
- apiref
api_name:
- MCIWNDM_NOTIFYMODE
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7fe75048a53023dab67bef4048d6149438ad54d2
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104032326"
---
# <a name="mciwndm_notifymode-message"></a><span data-ttu-id="605b0-104">\_Message MCIWNDM NOTIFYMODE</span><span class="sxs-lookup"><span data-stu-id="605b0-104">MCIWNDM\_NOTIFYMODE message</span></span>

<span data-ttu-id="605b0-105">Le message **MCIWNDM \_ NOTIFYMODE** notifie la fenêtre parente d’une application que le mode d’opération du périphérique MCI a changé.</span><span class="sxs-lookup"><span data-stu-id="605b0-105">The **MCIWNDM\_NOTIFYMODE** message notifies the parent window of an application that the operating mode of the MCI device has changed.</span></span>


```C++
MCIWNDM_NOTIFYMODE 
wParam = (WPARAM) (HWND) hwnd; 
lParam = (LPARAM) (LONG) mode; 
```



## <a name="parameters"></a><span data-ttu-id="605b0-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="605b0-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="605b0-107"><span id="hwnd"></span><span id="HWND"></span>*HWND*</span><span class="sxs-lookup"><span data-stu-id="605b0-107"><span id="hwnd"></span><span id="HWND"></span>*hwnd*</span></span>
</dt> <dd>

<span data-ttu-id="605b0-108">Handle vers la fenêtre MCIWnd.</span><span class="sxs-lookup"><span data-stu-id="605b0-108">Handle to the MCIWnd window.</span></span>

</dd> <dt>

<span data-ttu-id="605b0-109"><span id="mode"></span><span id="MODE"></span>*mode*</span><span class="sxs-lookup"><span data-stu-id="605b0-109"><span id="mode"></span><span id="MODE"></span>*mode*</span></span>
</dt> <dd>

<span data-ttu-id="605b0-110">Entier correspondant au mode MCI.</span><span class="sxs-lookup"><span data-stu-id="605b0-110">Integer corresponding to the MCI mode.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="605b0-111">Notes</span><span class="sxs-lookup"><span data-stu-id="605b0-111">Remarks</span></span>

<span data-ttu-id="605b0-112">Vous pouvez activer la notification des modifications de mode d’un appareil MCI en spécifiant le \_ style de fenêtre MCIWNDF NOTIFYMODE.</span><span class="sxs-lookup"><span data-stu-id="605b0-112">You can enable notification of mode changes of an MCI device by specifying the MCIWNDF\_NOTIFYMODE window style.</span></span>

## <a name="requirements"></a><span data-ttu-id="605b0-113">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="605b0-113">Requirements</span></span>



| <span data-ttu-id="605b0-114">Condition requise</span><span class="sxs-lookup"><span data-stu-id="605b0-114">Requirement</span></span> | <span data-ttu-id="605b0-115">Valeur</span><span class="sxs-lookup"><span data-stu-id="605b0-115">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="605b0-116">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="605b0-116">Minimum supported client</span></span><br/> | <span data-ttu-id="605b0-117">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="605b0-117">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="605b0-118">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="605b0-118">Minimum supported server</span></span><br/> | <span data-ttu-id="605b0-119">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="605b0-119">Windows 2000 Server \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="605b0-120">En-tête</span><span class="sxs-lookup"><span data-stu-id="605b0-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="605b0-121"><dt>VFW. h</dt></span><span class="sxs-lookup"><span data-stu-id="605b0-121"><dt>Vfw.h</dt></span></span> </dl> |



 

 





