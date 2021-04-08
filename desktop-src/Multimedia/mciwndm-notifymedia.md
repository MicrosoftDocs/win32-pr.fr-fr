---
title: Message MCIWNDM_NOTIFYMEDIA (VFW. h)
description: Le \_ message MCIWNDM NOTIFYMEDIA notifie la fenêtre parente d’une application que le média a changé.
ms.assetid: cc31502d-09a9-4580-9ff8-9c2be51c8e35
keywords:
- Message MCIWNDM_NOTIFYMEDIA Windows Multimedia
topic_type:
- apiref
api_name:
- MCIWNDM_NOTIFYMEDIA
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7026bd984e1d79775aac52caad56c87be6e8098e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103741149"
---
# <a name="mciwndm_notifymedia-message"></a><span data-ttu-id="c5826-104">\_Message MCIWNDM NOTIFYMEDIA</span><span class="sxs-lookup"><span data-stu-id="c5826-104">MCIWNDM\_NOTIFYMEDIA message</span></span>

<span data-ttu-id="c5826-105">Le message **MCIWNDM \_ NOTIFYMEDIA** notifie la fenêtre parente d’une application que le média a changé.</span><span class="sxs-lookup"><span data-stu-id="c5826-105">The **MCIWNDM\_NOTIFYMEDIA** message notifies the parent window of an application that the media has changed.</span></span>


```C++
MCIWNDM_NOTIFYMEDIA 
wParam = (WPARAM) (HWND) hwnd; 
lParam = (LPARAM) (LPSTR) lp; 
```



## <a name="parameters"></a><span data-ttu-id="c5826-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="c5826-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c5826-107"><span id="hwnd"></span><span id="HWND"></span>*HWND*</span><span class="sxs-lookup"><span data-stu-id="c5826-107"><span id="hwnd"></span><span id="HWND"></span>*hwnd*</span></span>
</dt> <dd>

<span data-ttu-id="c5826-108">Handle vers la fenêtre MCIWnd.</span><span class="sxs-lookup"><span data-stu-id="c5826-108">Handle to the MCIWnd window.</span></span>

</dd> <dt>

<span data-ttu-id="c5826-109"><span id="lp"></span><span id="LP"></span>*Aid*</span><span class="sxs-lookup"><span data-stu-id="c5826-109"><span id="lp"></span><span id="LP"></span>*lp*</span></span>
</dt> <dd>

<span data-ttu-id="c5826-110">Pointeur vers une chaîne se terminant par un caractère null qui contient le nouveau nom de fichier.</span><span class="sxs-lookup"><span data-stu-id="c5826-110">Pointer to a null-terminated string containing the new filename.</span></span> <span data-ttu-id="c5826-111">Si le média est en fermeture, il spécifie une chaîne NULL.</span><span class="sxs-lookup"><span data-stu-id="c5826-111">If the media is closing, it specifies a null string.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="c5826-112">Notes</span><span class="sxs-lookup"><span data-stu-id="c5826-112">Remarks</span></span>

<span data-ttu-id="c5826-113">Vous pouvez activer la notification des modifications de média en spécifiant le \_ style de fenêtre MCIWNDF NOTIFYMEDIA.</span><span class="sxs-lookup"><span data-stu-id="c5826-113">You can enable notification of media changes by specifying the MCIWNDF\_NOTIFYMEDIA window style.</span></span>

## <a name="requirements"></a><span data-ttu-id="c5826-114">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="c5826-114">Requirements</span></span>



| <span data-ttu-id="c5826-115">Condition requise</span><span class="sxs-lookup"><span data-stu-id="c5826-115">Requirement</span></span> | <span data-ttu-id="c5826-116">Valeur</span><span class="sxs-lookup"><span data-stu-id="c5826-116">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="c5826-117">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="c5826-117">Minimum supported client</span></span><br/> | <span data-ttu-id="c5826-118">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="c5826-118">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="c5826-119">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="c5826-119">Minimum supported server</span></span><br/> | <span data-ttu-id="c5826-120">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="c5826-120">Windows 2000 Server \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="c5826-121">En-tête</span><span class="sxs-lookup"><span data-stu-id="c5826-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="c5826-122"><dt>VFW. h</dt></span><span class="sxs-lookup"><span data-stu-id="c5826-122"><dt>Vfw.h</dt></span></span> </dl> |



 

 





