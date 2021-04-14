---
title: Message MCIWNDM_OPENINTERFACE (VFW. h)
description: Le \_ message MCIWNDM OPENINTERFACE joint le flux de données ou le fichier associé à l’interface spécifiée à une fenêtre MCIWnd. Vous pouvez envoyer ce message explicitement ou à l’aide de la macro MCIWndOpenInterface.
ms.assetid: 73cbd637-d315-4b39-a978-2b72aed1f303
keywords:
- Message MCIWNDM_OPENINTERFACE Windows Multimedia
topic_type:
- apiref
api_name:
- MCIWNDM_OPENINTERFACE
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9c40453f4d587429508a5aae19bc432fc46088ae
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104383848"
---
# <a name="mciwndm_openinterface-message"></a><span data-ttu-id="57fb5-105">\_Message MCIWNDM OPENINTERFACE</span><span class="sxs-lookup"><span data-stu-id="57fb5-105">MCIWNDM\_OPENINTERFACE message</span></span>

<span data-ttu-id="57fb5-106">Le message **MCIWNDM \_ OPENINTERFACE** joint le flux de données ou le fichier associé à l’interface spécifiée à une fenêtre MCIWnd.</span><span class="sxs-lookup"><span data-stu-id="57fb5-106">The **MCIWNDM\_OPENINTERFACE** message attaches the data stream or file associated with the specified interface to an MCIWnd window.</span></span> <span data-ttu-id="57fb5-107">Vous pouvez envoyer ce message explicitement ou à l’aide de la macro [**MCIWndOpenInterface**](/windows/desktop/api/Vfw/nf-vfw-mciwndopeninterface) .</span><span class="sxs-lookup"><span data-stu-id="57fb5-107">You can send this message explicitly or by using the [**MCIWndOpenInterface**](/windows/desktop/api/Vfw/nf-vfw-mciwndopeninterface) macro.</span></span>


```C++
MCIWNDM_OPENINTERFACE 
wParam = 0; 
lParam = (LPARAM) (LPUNKNOWN) pUnk; 
```



## <a name="parameters"></a><span data-ttu-id="57fb5-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="57fb5-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="57fb5-109"><span id="pUnk"></span><span id="punk"></span><span id="PUNK"></span>*pUnk*</span><span class="sxs-lookup"><span data-stu-id="57fb5-109"><span id="pUnk"></span><span id="punk"></span><span id="PUNK"></span>*pUnk*</span></span>
</dt> <dd>

<span data-ttu-id="57fb5-110">Pointeur vers une interface IAVI qui pointe vers un fichier ou un flux de données dans un fichier.</span><span class="sxs-lookup"><span data-stu-id="57fb5-110">Pointer to an IAVI interface that points to a file or a data stream in a file.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="57fb5-111">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="57fb5-111">Return Value</span></span>

<span data-ttu-id="57fb5-112">Retourne zéro en cas de réussite ou une erreur.</span><span class="sxs-lookup"><span data-stu-id="57fb5-112">Returns zero if successful or an error otherwise.</span></span>

## <a name="requirements"></a><span data-ttu-id="57fb5-113">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="57fb5-113">Requirements</span></span>



| <span data-ttu-id="57fb5-114">Condition requise</span><span class="sxs-lookup"><span data-stu-id="57fb5-114">Requirement</span></span> | <span data-ttu-id="57fb5-115">Valeur</span><span class="sxs-lookup"><span data-stu-id="57fb5-115">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="57fb5-116">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="57fb5-116">Minimum supported client</span></span><br/> | <span data-ttu-id="57fb5-117">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="57fb5-117">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="57fb5-118">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="57fb5-118">Minimum supported server</span></span><br/> | <span data-ttu-id="57fb5-119">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="57fb5-119">Windows 2000 Server \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="57fb5-120">En-tête</span><span class="sxs-lookup"><span data-stu-id="57fb5-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="57fb5-121"><dt>VFW. h</dt></span><span class="sxs-lookup"><span data-stu-id="57fb5-121"><dt>Vfw.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="57fb5-122">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="57fb5-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="57fb5-123">**MCIWndOpenInterface**</span><span class="sxs-lookup"><span data-stu-id="57fb5-123">**MCIWndOpenInterface**</span></span>](/windows/desktop/api/Vfw/nf-vfw-mciwndopeninterface)
</dt> </dl>

 

 





