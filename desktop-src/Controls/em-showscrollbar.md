---
title: Message EM_SHOWSCROLLBAR (RichEdit. h)
description: Affiche ou masque l’une des barres de défilement dans la fenêtre hôte d’un contrôle RichEdit.
ms.assetid: 0a6ec010-4870-4faf-9dc2-1da961dc8194
keywords:
- EM_SHOWSCROLLBAR les contrôles de message Windows
topic_type:
- apiref
api_name:
- EM_SHOWSCROLLBAR
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: eb569b194be3d744db67f98b71a595ba18a2d3a8
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103942025"
---
# <a name="em_showscrollbar-message"></a><span data-ttu-id="ad00d-104">\_Message SHOWSCROLLBAR em</span><span class="sxs-lookup"><span data-stu-id="ad00d-104">EM\_SHOWSCROLLBAR message</span></span>

<span data-ttu-id="ad00d-105">Affiche ou masque l’une des barres de défilement dans la fenêtre hôte d’un contrôle RichEdit.</span><span class="sxs-lookup"><span data-stu-id="ad00d-105">Shows or hides one of the scroll bars in the host window of a rich edit control.</span></span>

## <a name="parameters"></a><span data-ttu-id="ad00d-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="ad00d-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ad00d-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="ad00d-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="ad00d-108">Identifie la barre de défilement à afficher : horizontale ou verticale.</span><span class="sxs-lookup"><span data-stu-id="ad00d-108">Identifies which scroll bar to display: horizontal or vertical.</span></span> <span data-ttu-id="ad00d-109">Ce paramètre doit être **SB \_ vert** ou **SB \_ Horiz**.</span><span class="sxs-lookup"><span data-stu-id="ad00d-109">This parameter must be **SB\_VERT** or **SB\_HORZ**.</span></span>

</dd> <dt>

<span data-ttu-id="ad00d-110">*lParam*</span><span class="sxs-lookup"><span data-stu-id="ad00d-110">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="ad00d-111">Spécifie si la barre de défilement doit être affichée ou masquée.</span><span class="sxs-lookup"><span data-stu-id="ad00d-111">Specifies whether to show the scroll bar or hide it.</span></span> <span data-ttu-id="ad00d-112">Spécifiez **true** pour afficher la barre de défilement et **false** pour la masquer.</span><span class="sxs-lookup"><span data-stu-id="ad00d-112">Specify **TRUE** to show the scroll bar and **FALSE** to hide it.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ad00d-113">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="ad00d-113">Return value</span></span>

<span data-ttu-id="ad00d-114">Ce message ne retourne pas de valeur.</span><span class="sxs-lookup"><span data-stu-id="ad00d-114">This message does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="ad00d-115">Notes</span><span class="sxs-lookup"><span data-stu-id="ad00d-115">Remarks</span></span>

<span data-ttu-id="ad00d-116">Cette méthode est valide uniquement lorsque le contrôle est actif sur place.</span><span class="sxs-lookup"><span data-stu-id="ad00d-116">This method is only valid when the control is in-place active.</span></span> <span data-ttu-id="ad00d-117">Les appels effectués alors que le contrôle est inactif peuvent échouer.</span><span class="sxs-lookup"><span data-stu-id="ad00d-117">Calls made while the control is inactive may fail.</span></span>

## <a name="requirements"></a><span data-ttu-id="ad00d-118">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="ad00d-118">Requirements</span></span>



| <span data-ttu-id="ad00d-119">Condition requise</span><span class="sxs-lookup"><span data-stu-id="ad00d-119">Requirement</span></span> | <span data-ttu-id="ad00d-120">Valeur</span><span class="sxs-lookup"><span data-stu-id="ad00d-120">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="ad00d-121">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="ad00d-121">Minimum supported client</span></span><br/> | <span data-ttu-id="ad00d-122">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="ad00d-122">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="ad00d-123">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="ad00d-123">Minimum supported server</span></span><br/> | <span data-ttu-id="ad00d-124">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="ad00d-124">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="ad00d-125">En-tête</span><span class="sxs-lookup"><span data-stu-id="ad00d-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="ad00d-126"><dt>RichEdit. h</dt></span><span class="sxs-lookup"><span data-stu-id="ad00d-126"><dt>Richedit.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ad00d-127">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="ad00d-127">See also</span></span>

<dl> <dt>

<span data-ttu-id="ad00d-128">**Référence**</span><span class="sxs-lookup"><span data-stu-id="ad00d-128">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="ad00d-129">**\_GETSCROLLPOS em**</span><span class="sxs-lookup"><span data-stu-id="ad00d-129">**EM\_GETSCROLLPOS**</span></span>](em-getscrollpos.md)
</dt> <dt>

[<span data-ttu-id="ad00d-130">**\_SETSCROLLPOS em**</span><span class="sxs-lookup"><span data-stu-id="ad00d-130">**EM\_SETSCROLLPOS**</span></span>](em-setscrollpos.md)
</dt> </dl>

 

 





