---
title: Message EM_SETCUEBANNER (commctrl. h)
description: Définit la file d’attente textuelle, ou Tip, qui est affichée par le contrôle d’édition pour inviter l’utilisateur à fournir des informations.
ms.assetid: 1b1ff5e7-e0b8-40c1-8b7e-7003e9ef959b
keywords:
- EM_SETCUEBANNER les contrôles de message Windows
topic_type:
- apiref
api_name:
- EM_SETCUEBANNER
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d740bf0a3a055f45c6d104d44349f078d3bf9ad2
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104466547"
---
# <a name="em_setcuebanner-message"></a><span data-ttu-id="51160-104">\_Message SETCUEBANNER em</span><span class="sxs-lookup"><span data-stu-id="51160-104">EM\_SETCUEBANNER message</span></span>

<span data-ttu-id="51160-105">Définit la file d’attente textuelle, ou Tip, qui est affichée par le contrôle d’édition pour inviter l’utilisateur à fournir des informations.</span><span class="sxs-lookup"><span data-stu-id="51160-105">Sets the textual cue, or tip, that is displayed by the edit control to prompt the user for information.</span></span>

## <a name="parameters"></a><span data-ttu-id="51160-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="51160-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="51160-107">*wParam* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="51160-107">*wParam* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="51160-108">**True** si la bannière de signal doit s’afficher même lorsque le contrôle d’édition a le focus ; Sinon, **false**.</span><span class="sxs-lookup"><span data-stu-id="51160-108">**TRUE** if the cue banner should show even when the edit control has focus; otherwise, **FALSE**.</span></span> <span data-ttu-id="51160-109">**False** est le comportement par défaut où la bannière de signal disparaît lorsque l’utilisateur clique sur le contrôle.</span><span class="sxs-lookup"><span data-stu-id="51160-109">**FALSE** is the default behavior the cue banner disappears when the user clicks in the control.</span></span>

</dd> <dt>

<span data-ttu-id="51160-110">*lParam* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="51160-110">*lParam* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="51160-111">Pointeur vers une chaîne Unicode qui contient le texte à afficher en tant que file d’attente textuelle.</span><span class="sxs-lookup"><span data-stu-id="51160-111">A pointer to a Unicode string that contains the text to display as the textual cue.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="51160-112">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="51160-112">Return value</span></span>

<span data-ttu-id="51160-113">Si le message est correctement exécuté, la méthode retourne la **valeur true**.</span><span class="sxs-lookup"><span data-stu-id="51160-113">If the message succeeds, it returns **TRUE**.</span></span> <span data-ttu-id="51160-114">Sinon, elle retourne **false**.</span><span class="sxs-lookup"><span data-stu-id="51160-114">Otherwise it returns **FALSE**.</span></span>

## <a name="remarks"></a><span data-ttu-id="51160-115">Notes</span><span class="sxs-lookup"><span data-stu-id="51160-115">Remarks</span></span>

<span data-ttu-id="51160-116">Un contrôle d’édition utilisé pour commencer une recherche peut afficher « entrer la recherche ici » en texte gris comme une file d’attente textuelle.</span><span class="sxs-lookup"><span data-stu-id="51160-116">An edit control that is used to begin a search may display "Enter search here" in gray text as a textual cue.</span></span> <span data-ttu-id="51160-117">Lorsque l’utilisateur clique sur le texte, le texte disparaît et l’utilisateur peut taper.</span><span class="sxs-lookup"><span data-stu-id="51160-117">When the user clicks the text, the text goes away and the user can type.</span></span>

<span data-ttu-id="51160-118">Vous ne pouvez pas définir une bannière de signal sur un contrôle d’édition multiligne ou sur un contrôle RichEdit.</span><span class="sxs-lookup"><span data-stu-id="51160-118">You cannot set a cue banner on a multiline edit control or on a rich edit control.</span></span>

> [!Note]  
> <span data-ttu-id="51160-119">Pour utiliser cette API, vous devez fournir un manifeste spécifiant Comclt32.dll version 6,0.</span><span class="sxs-lookup"><span data-stu-id="51160-119">To use this API, you must provide a manifest specifying Comclt32.dll version 6.0.</span></span> <span data-ttu-id="51160-120">Pour plus d’informations sur les manifestes, consultez [activation des styles visuels](cookbook-overview.md).</span><span class="sxs-lookup"><span data-stu-id="51160-120">For more information on manifests, see [Enabling Visual Styles](cookbook-overview.md).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="51160-121">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="51160-121">Requirements</span></span>



| <span data-ttu-id="51160-122">Condition requise</span><span class="sxs-lookup"><span data-stu-id="51160-122">Requirement</span></span> | <span data-ttu-id="51160-123">Valeur</span><span class="sxs-lookup"><span data-stu-id="51160-123">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="51160-124">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="51160-124">Minimum supported client</span></span><br/> | <span data-ttu-id="51160-125">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="51160-125">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="51160-126">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="51160-126">Minimum supported server</span></span><br/> | <span data-ttu-id="51160-127">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="51160-127">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="51160-128">En-tête</span><span class="sxs-lookup"><span data-stu-id="51160-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="51160-129"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="51160-129"><dt>Commctrl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="51160-130">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="51160-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="51160-131">**Modifier \_ SetCueBannerText**</span><span class="sxs-lookup"><span data-stu-id="51160-131">**Edit\_SetCueBannerText**</span></span>](/windows/desktop/api/Commctrl/nf-commctrl-edit_setcuebannertext)
</dt> </dl>

 

 





