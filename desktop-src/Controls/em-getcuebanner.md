---
title: Message EM_GETCUEBANNER (commctrl. h)
description: Obtient le texte affiché sous la forme d’une indication textuelle, ou Tip, dans un contrôle d’édition.
ms.assetid: 311b783a-cd78-440f-bfc2-f5108ae7d1f8
keywords:
- EM_GETCUEBANNER les contrôles de message Windows
topic_type:
- apiref
api_name:
- EM_GETCUEBANNER
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5d28d4aeea5a206c74f2e6b41cee27b5073448ba
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103942807"
---
# <a name="em_getcuebanner-message"></a><span data-ttu-id="16a09-104">\_Message GETCUEBANNER em</span><span class="sxs-lookup"><span data-stu-id="16a09-104">EM\_GETCUEBANNER message</span></span>

<span data-ttu-id="16a09-105">Obtient le texte affiché sous la forme d’une indication textuelle, ou Tip, dans un contrôle d’édition.</span><span class="sxs-lookup"><span data-stu-id="16a09-105">Gets the text that is displayed as the textual cue, or tip, in an edit control.</span></span>

## <a name="parameters"></a><span data-ttu-id="16a09-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="16a09-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="16a09-107">*wParam* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="16a09-107">*wParam* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="16a09-108">Pointeur vers une mémoire tampon Unicode qui reçoit le texte défini comme la file d’attente textuelle.</span><span class="sxs-lookup"><span data-stu-id="16a09-108">A pointer to a Unicode buffer that receives the text set as the textual cue.</span></span> <span data-ttu-id="16a09-109">L’appelant est chargé d’allouer la mémoire tampon.</span><span class="sxs-lookup"><span data-stu-id="16a09-109">The caller is responsible for allocating the buffer.</span></span>

</dd> <dt>

<span data-ttu-id="16a09-110">*lParam* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="16a09-110">*lParam* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="16a09-111">Taille de la mémoire tampon désignée par *wParam* dans **WCHARs**, y compris la **valeur null** de fin.</span><span class="sxs-lookup"><span data-stu-id="16a09-111">The size of the buffer pointed to by *wParam* in **WCHARs**, including the terminating **NULL**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="16a09-112">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="16a09-112">Return value</span></span>

<span data-ttu-id="16a09-113">Retourne la **valeur true** en cas de réussite ou **false** dans le cas contraire.</span><span class="sxs-lookup"><span data-stu-id="16a09-113">Returns **TRUE** if successful or **FALSE** otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="16a09-114">Notes</span><span class="sxs-lookup"><span data-stu-id="16a09-114">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="16a09-115">Pour utiliser ce message, vous devez fournir un manifeste spécifiant Comclt32.dll version 6,0.</span><span class="sxs-lookup"><span data-stu-id="16a09-115">To use this message, you must provide a manifest specifying Comclt32.dll version 6.0.</span></span> <span data-ttu-id="16a09-116">Pour plus d’informations sur les manifestes, consultez [activation des styles visuels](cookbook-overview.md).</span><span class="sxs-lookup"><span data-stu-id="16a09-116">For more information on manifests, see [Enabling Visual Styles](cookbook-overview.md).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="16a09-117">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="16a09-117">Requirements</span></span>



| <span data-ttu-id="16a09-118">Condition requise</span><span class="sxs-lookup"><span data-stu-id="16a09-118">Requirement</span></span> | <span data-ttu-id="16a09-119">Valeur</span><span class="sxs-lookup"><span data-stu-id="16a09-119">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="16a09-120">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="16a09-120">Minimum supported client</span></span><br/> | <span data-ttu-id="16a09-121">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="16a09-121">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="16a09-122">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="16a09-122">Minimum supported server</span></span><br/> | <span data-ttu-id="16a09-123">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="16a09-123">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="16a09-124">En-tête</span><span class="sxs-lookup"><span data-stu-id="16a09-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="16a09-125"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="16a09-125"><dt>Commctrl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="16a09-126">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="16a09-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="16a09-127">**Modifier \_ GetCueBannerText**</span><span class="sxs-lookup"><span data-stu-id="16a09-127">**Edit\_GetCueBannerText**</span></span>](/windows/desktop/api/Commctrl/nf-commctrl-edit_getcuebannertext)
</dt> </dl>

 

 





