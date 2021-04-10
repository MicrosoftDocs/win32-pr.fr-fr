---
title: Message MCIWNDM_NOTIFYSIZE (VFW. h)
description: Le \_ message MCIWNDM NOTIFYSIZE avertit la fenêtre parente d’une application que la taille de la fenêtre a changé.
ms.assetid: 76e1f663-bfc6-4d3c-9486-c8c7f79e4265
keywords:
- Message MCIWNDM_NOTIFYSIZE Windows Multimedia
topic_type:
- apiref
api_name:
- MCIWNDM_NOTIFYSIZE
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 59db02d69302127937a7203729de9cc8b98a58f4
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104103433"
---
# <a name="mciwndm_notifysize-message"></a><span data-ttu-id="23d67-104">\_Message MCIWNDM NOTIFYSIZE</span><span class="sxs-lookup"><span data-stu-id="23d67-104">MCIWNDM\_NOTIFYSIZE message</span></span>

<span data-ttu-id="23d67-105">Le message **MCIWNDM \_ NOTIFYSIZE** avertit la fenêtre parente d’une application que la taille de la fenêtre a changé.</span><span class="sxs-lookup"><span data-stu-id="23d67-105">The **MCIWNDM\_NOTIFYSIZE** message notifies the parent window of an application that the window size has changed.</span></span>


```C++
MCIWNDM_NOTIFYSIZE 
wParam = (WPARAM) (HWND) hwnd; 
lParam = 0; 
```



## <a name="parameters"></a><span data-ttu-id="23d67-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="23d67-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="23d67-107"><span id="hwnd"></span><span id="HWND"></span>*HWND*</span><span class="sxs-lookup"><span data-stu-id="23d67-107"><span id="hwnd"></span><span id="HWND"></span>*hwnd*</span></span>
</dt> <dd>

<span data-ttu-id="23d67-108">Handle vers la fenêtre MCIWnd.</span><span class="sxs-lookup"><span data-stu-id="23d67-108">Handle to the MCIWnd window.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="23d67-109">Notes</span><span class="sxs-lookup"><span data-stu-id="23d67-109">Remarks</span></span>

<span data-ttu-id="23d67-110">Vous pouvez activer la notification des modifications de la taille d’une fenêtre MCIWnd en spécifiant le \_ style de fenêtre NOTIFYSIZE MCIWNDF.</span><span class="sxs-lookup"><span data-stu-id="23d67-110">You can enable notification of changes in the size of an MCIWnd window by specifying the MCIWNDF\_NOTIFYSIZE window style.</span></span>

## <a name="requirements"></a><span data-ttu-id="23d67-111">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="23d67-111">Requirements</span></span>



| <span data-ttu-id="23d67-112">Condition requise</span><span class="sxs-lookup"><span data-stu-id="23d67-112">Requirement</span></span> | <span data-ttu-id="23d67-113">Valeur</span><span class="sxs-lookup"><span data-stu-id="23d67-113">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="23d67-114">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="23d67-114">Minimum supported client</span></span><br/> | <span data-ttu-id="23d67-115">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="23d67-115">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="23d67-116">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="23d67-116">Minimum supported server</span></span><br/> | <span data-ttu-id="23d67-117">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="23d67-117">Windows 2000 Server \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="23d67-118">En-tête</span><span class="sxs-lookup"><span data-stu-id="23d67-118">Header</span></span><br/>                   | <dl> <span data-ttu-id="23d67-119"><dt>VFW. h</dt></span><span class="sxs-lookup"><span data-stu-id="23d67-119"><dt>Vfw.h</dt></span></span> </dl> |



 

 





