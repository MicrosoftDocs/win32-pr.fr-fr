---
title: Message MCIWNDM_NOTIFYPOS (VFW. h)
description: Le \_ message MCIWNDM NOTIFYPOS notifie la fenêtre parente d’une application que la position de la fenêtre a changé.
ms.assetid: ccc8903b-ad79-495a-8003-20e120ad28ff
keywords:
- Message MCIWNDM_NOTIFYPOS Windows Multimedia
topic_type:
- apiref
api_name:
- MCIWNDM_NOTIFYPOS
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5bebb3a8facd6478c21888cf0cf5ca81e3735ff8
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103942630"
---
# <a name="mciwndm_notifypos-message"></a><span data-ttu-id="85ae3-104">\_Message MCIWNDM NOTIFYPOS</span><span class="sxs-lookup"><span data-stu-id="85ae3-104">MCIWNDM\_NOTIFYPOS message</span></span>

<span data-ttu-id="85ae3-105">Le message **MCIWNDM \_ NOTIFYPOS** notifie la fenêtre parente d’une application que la position de la fenêtre a changé.</span><span class="sxs-lookup"><span data-stu-id="85ae3-105">The **MCIWNDM\_NOTIFYPOS** message notifies the parent window of an application that the window position has changed.</span></span>


```C++
MCIWNDM_NOTIFYPOS 
wParam = (WPARAM) (HWND) hwnd; 
lParam = (LPARAM) (LONG) pos; 
```



## <a name="parameters"></a><span data-ttu-id="85ae3-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="85ae3-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="85ae3-107"><span id="hwnd"></span><span id="HWND"></span>*HWND*</span><span class="sxs-lookup"><span data-stu-id="85ae3-107"><span id="hwnd"></span><span id="HWND"></span>*hwnd*</span></span>
</dt> <dd>

<span data-ttu-id="85ae3-108">Handle vers la fenêtre MCIWnd.</span><span class="sxs-lookup"><span data-stu-id="85ae3-108">Handle to the MCIWnd window.</span></span>

</dd> <dt>

<span data-ttu-id="85ae3-109"><span id="pos"></span><span id="POS"></span>*imprim*</span><span class="sxs-lookup"><span data-stu-id="85ae3-109"><span id="pos"></span><span id="POS"></span>*pos*</span></span>
</dt> <dd>

<span data-ttu-id="85ae3-110">Décrit la nouvelle position.</span><span class="sxs-lookup"><span data-stu-id="85ae3-110">Describes the new position.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="85ae3-111">Notes</span><span class="sxs-lookup"><span data-stu-id="85ae3-111">Remarks</span></span>

<span data-ttu-id="85ae3-112">Vous pouvez activer la notification des modifications apportées à la position d’une fenêtre MCIWnd en spécifiant le \_ style de fenêtre NOTIFYPOS MCIWNDF.</span><span class="sxs-lookup"><span data-stu-id="85ae3-112">You can enable notification of changes in the position of an MCIWnd window by specifying the MCIWNDF\_NOTIFYPOS window style.</span></span>

## <a name="requirements"></a><span data-ttu-id="85ae3-113">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="85ae3-113">Requirements</span></span>



| <span data-ttu-id="85ae3-114">Condition requise</span><span class="sxs-lookup"><span data-stu-id="85ae3-114">Requirement</span></span> | <span data-ttu-id="85ae3-115">Valeur</span><span class="sxs-lookup"><span data-stu-id="85ae3-115">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="85ae3-116">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="85ae3-116">Minimum supported client</span></span><br/> | <span data-ttu-id="85ae3-117">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="85ae3-117">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="85ae3-118">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="85ae3-118">Minimum supported server</span></span><br/> | <span data-ttu-id="85ae3-119">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="85ae3-119">Windows 2000 Server \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="85ae3-120">En-tête</span><span class="sxs-lookup"><span data-stu-id="85ae3-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="85ae3-121"><dt>VFW. h</dt></span><span class="sxs-lookup"><span data-stu-id="85ae3-121"><dt>Vfw.h</dt></span></span> </dl> |



 

 





