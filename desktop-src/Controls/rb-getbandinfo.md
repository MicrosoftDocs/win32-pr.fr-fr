---
title: Message RB_GETBANDINFO (commctrl. h)
description: Récupère des informations sur une bande spécifiée dans un contrôle rebar.
ms.assetid: c2a76c91-7d44-4278-823d-bd263520e7a8
keywords:
- RB_GETBANDINFO les contrôles de message Windows
topic_type:
- apiref
api_name:
- RB_GETBANDINFO
- RB_GETBANDINFOA
- RB_GETBANDINFOW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b87715cf61b4eb2726eab83d500330721f41719f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104104791"
---
# <a name="rb_getbandinfo-message"></a><span data-ttu-id="759b1-104">\_Message GETBANDINFO RB</span><span class="sxs-lookup"><span data-stu-id="759b1-104">RB\_GETBANDINFO message</span></span>

<span data-ttu-id="759b1-105">Récupère des informations sur une bande spécifiée dans un contrôle rebar.</span><span class="sxs-lookup"><span data-stu-id="759b1-105">Retrieves information about a specified band in a rebar control.</span></span>

## <a name="parameters"></a><span data-ttu-id="759b1-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="759b1-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="759b1-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="759b1-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="759b1-108">Index de base zéro de la bande pour laquelle les informations sont récupérées.</span><span class="sxs-lookup"><span data-stu-id="759b1-108">Zero-based index of the band for which the information will be retrieved.</span></span>

</dd> <dt>

<span data-ttu-id="759b1-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="759b1-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="759b1-110">Pointeur vers une structure [**REBARBANDINFO**](/windows/win32/api/commctrl/ns-commctrl-rebarbandinfoa) qui recevra les informations de la bande demandée.</span><span class="sxs-lookup"><span data-stu-id="759b1-110">Pointer to a [**REBARBANDINFO**](/windows/win32/api/commctrl/ns-commctrl-rebarbandinfoa) structure that will receive the requested band information.</span></span> <span data-ttu-id="759b1-111">Avant d’envoyer ce message, vous devez définir le membre **cbSize** de cette structure sur la taille de la structure **REBARBANDINFO** et définir le membre **fmask** sur les éléments que vous souhaitez récupérer.</span><span class="sxs-lookup"><span data-stu-id="759b1-111">Before sending this message, you must set the **cbSize** member of this structure to the size of the **REBARBANDINFO** structure and set the **fMask** member to the items you want to retrieve.</span></span> <span data-ttu-id="759b1-112">En outre, vous devez définir le membre **CCH** de la structure **REBARBANDINFO** sur la taille de la mémoire tampon **lpText** lorsque le \_ texte RBBIM est spécifié.</span><span class="sxs-lookup"><span data-stu-id="759b1-112">Additionally, you must set the **cch** member of the **REBARBANDINFO** structure to the size of the **lpText** buffer when RBBIM\_TEXT is specified.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="759b1-113">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="759b1-113">Return value</span></span>

<span data-ttu-id="759b1-114">Retourne une valeur différente de zéro en cas de réussite, ou zéro dans le cas contraire.</span><span class="sxs-lookup"><span data-stu-id="759b1-114">Returns nonzero if successful, or zero otherwise.</span></span>

## <a name="requirements"></a><span data-ttu-id="759b1-115">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="759b1-115">Requirements</span></span>



| <span data-ttu-id="759b1-116">Condition requise</span><span class="sxs-lookup"><span data-stu-id="759b1-116">Requirement</span></span> | <span data-ttu-id="759b1-117">Valeur</span><span class="sxs-lookup"><span data-stu-id="759b1-117">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="759b1-118">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="759b1-118">Minimum supported client</span></span><br/> | <span data-ttu-id="759b1-119">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="759b1-119">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="759b1-120">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="759b1-120">Minimum supported server</span></span><br/> | <span data-ttu-id="759b1-121">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="759b1-121">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="759b1-122">En-tête</span><span class="sxs-lookup"><span data-stu-id="759b1-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="759b1-123"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="759b1-123"><dt>Commctrl.h</dt></span></span> </dl> |
| <span data-ttu-id="759b1-124">Noms Unicode et ANSI</span><span class="sxs-lookup"><span data-stu-id="759b1-124">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="759b1-125">**RB \_ GETBANDINFOW** (Unicode) et **RB \_ GETBANDINFOA** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="759b1-125">**RB\_GETBANDINFOW** (Unicode) and **RB\_GETBANDINFOA** (ANSI)</span></span><br/>             |



## <a name="see-also"></a><span data-ttu-id="759b1-126">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="759b1-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="759b1-127">**\_SETBANDINFO RB**</span><span class="sxs-lookup"><span data-stu-id="759b1-127">**RB\_SETBANDINFO**</span></span>](rb-setbandinfo.md)
</dt> </dl>

 

 





