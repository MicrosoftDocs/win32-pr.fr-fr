---
title: Message MCIWNDM_NOTIFYERROR (VFW. h)
description: Le \_ message MCIWNDM NOTIFYERROR notifie la fenêtre parente d’une application qu’une erreur MCI s’est produite.
ms.assetid: 0f54886a-77dc-43cc-be46-2d322c75471a
keywords:
- Message MCIWNDM_NOTIFYERROR Windows Multimedia
topic_type:
- apiref
api_name:
- MCIWNDM_NOTIFYERROR
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bbef9180c31091f3bd1a85f23a08990c2f7e7ea0
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104032731"
---
# <a name="mciwndm_notifyerror-message"></a><span data-ttu-id="08ea9-104">\_Message MCIWNDM NOTIFYERROR</span><span class="sxs-lookup"><span data-stu-id="08ea9-104">MCIWNDM\_NOTIFYERROR message</span></span>

<span data-ttu-id="08ea9-105">Le message **MCIWNDM \_ NOTIFYERROR** notifie la fenêtre parente d’une application qu’une erreur MCI s’est produite.</span><span class="sxs-lookup"><span data-stu-id="08ea9-105">The **MCIWNDM\_NOTIFYERROR** message notifies the parent window of an application that an MCI error occurred.</span></span>


```C++
MCIWNDM_NOTIFYERROR 
wParam = (WPARAM) (HWND) hwnd; 
lParam = (LPARAM) (LONG) errorCode; 
```



## <a name="parameters"></a><span data-ttu-id="08ea9-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="08ea9-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="08ea9-107"><span id="hwnd"></span><span id="HWND"></span>*HWND*</span><span class="sxs-lookup"><span data-stu-id="08ea9-107"><span id="hwnd"></span><span id="HWND"></span>*hwnd*</span></span>
</dt> <dd>

<span data-ttu-id="08ea9-108">Handle vers la fenêtre MCIWnd.</span><span class="sxs-lookup"><span data-stu-id="08ea9-108">Handle to the MCIWnd window.</span></span>

</dd> <dt>

<span data-ttu-id="08ea9-109"><span id="errorCode"></span><span id="errorcode"></span><span id="ERRORCODE"></span>*errorCode*</span><span class="sxs-lookup"><span data-stu-id="08ea9-109"><span id="errorCode"></span><span id="errorcode"></span><span id="ERRORCODE"></span>*errorCode*</span></span>
</dt> <dd>

<span data-ttu-id="08ea9-110">Code numérique de l’erreur MCI.</span><span class="sxs-lookup"><span data-stu-id="08ea9-110">Numerical code for the MCI error.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="08ea9-111">Notes</span><span class="sxs-lookup"><span data-stu-id="08ea9-111">Remarks</span></span>

<span data-ttu-id="08ea9-112">Vous pouvez activer la notification d’erreur MCI en spécifiant le \_ style de fenêtre MCIWNDF NOTIFYERROR.</span><span class="sxs-lookup"><span data-stu-id="08ea9-112">You can enable MCI error notification by specifying the MCIWNDF\_NOTIFYERROR window style.</span></span>

## <a name="requirements"></a><span data-ttu-id="08ea9-113">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="08ea9-113">Requirements</span></span>



| <span data-ttu-id="08ea9-114">Condition requise</span><span class="sxs-lookup"><span data-stu-id="08ea9-114">Requirement</span></span> | <span data-ttu-id="08ea9-115">Valeur</span><span class="sxs-lookup"><span data-stu-id="08ea9-115">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="08ea9-116">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="08ea9-116">Minimum supported client</span></span><br/> | <span data-ttu-id="08ea9-117">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="08ea9-117">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="08ea9-118">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="08ea9-118">Minimum supported server</span></span><br/> | <span data-ttu-id="08ea9-119">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="08ea9-119">Windows 2000 Server \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="08ea9-120">En-tête</span><span class="sxs-lookup"><span data-stu-id="08ea9-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="08ea9-121"><dt>VFW. h</dt></span><span class="sxs-lookup"><span data-stu-id="08ea9-121"><dt>Vfw.h</dt></span></span> </dl> |



 

 





