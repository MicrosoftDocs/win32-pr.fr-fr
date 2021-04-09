---
title: Message BCM_GETTEXTMARGIN (commctrl. h)
description: Obtient les marges utilisées pour dessiner du texte dans un contrôle bouton. Vous pouvez envoyer ce message de manière explicite ou utiliser le bouton \_ GetTextMargin macro.
ms.assetid: 6c141752-e636-41c4-9d05-df8b320ff59f
keywords:
- BCM_GETTEXTMARGIN les contrôles de message Windows
topic_type:
- apiref
api_name:
- BCM_GETTEXTMARGIN
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d6a7d809207c21c74a36c796a9035ed0e3772481
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103942029"
---
# <a name="bcm_gettextmargin-message"></a><span data-ttu-id="ccb13-105">\_Message GETTEXTMARGIN BCM</span><span class="sxs-lookup"><span data-stu-id="ccb13-105">BCM\_GETTEXTMARGIN message</span></span>

<span data-ttu-id="ccb13-106">Obtient les marges utilisées pour dessiner du texte dans un contrôle bouton.</span><span class="sxs-lookup"><span data-stu-id="ccb13-106">Gets the margins used to draw text in a button control.</span></span> <span data-ttu-id="ccb13-107">Vous pouvez envoyer ce message de manière explicite ou utiliser le [**bouton \_ GetTextMargin**](/windows/desktop/api/Commctrl/nf-commctrl-button_gettextmargin) macro.</span><span class="sxs-lookup"><span data-stu-id="ccb13-107">You can send this message explicitly or use the [**Button\_GetTextMargin**](/windows/desktop/api/Commctrl/nf-commctrl-button_gettextmargin) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="ccb13-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="ccb13-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ccb13-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="ccb13-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="ccb13-110">Non utilisé ; doit être égal à zéro.</span><span class="sxs-lookup"><span data-stu-id="ccb13-110">Not used; must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="ccb13-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="ccb13-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="ccb13-112">Pointeur vers une structure [**Rect**](/previous-versions//dd162897(v=vs.85)) qui contient les marges à utiliser pour dessiner du texte.</span><span class="sxs-lookup"><span data-stu-id="ccb13-112">A pointer to a [**RECT**](/previous-versions//dd162897(v=vs.85)) structure that contains the margins to use for drawing text.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ccb13-113">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="ccb13-113">Return value</span></span>

<span data-ttu-id="ccb13-114">Si le message est correctement exécuté, la méthode retourne la **valeur true**.</span><span class="sxs-lookup"><span data-stu-id="ccb13-114">If the message succeeds, it returns **TRUE**.</span></span> <span data-ttu-id="ccb13-115">Sinon, elle retourne **false**.</span><span class="sxs-lookup"><span data-stu-id="ccb13-115">Otherwise it returns **FALSE**.</span></span>

## <a name="remarks"></a><span data-ttu-id="ccb13-116">Notes</span><span class="sxs-lookup"><span data-stu-id="ccb13-116">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="ccb13-117">Pour utiliser ce message, vous devez fournir un manifeste spécifiant Comclt32.dll version 6,0.</span><span class="sxs-lookup"><span data-stu-id="ccb13-117">To use this message, you must provide a manifest specifying Comclt32.dll version 6.0.</span></span> <span data-ttu-id="ccb13-118">Pour plus d’informations sur les manifestes, consultez [activation des styles visuels](cookbook-overview.md).</span><span class="sxs-lookup"><span data-stu-id="ccb13-118">For more information on manifests, see [Enabling Visual Styles](cookbook-overview.md).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="ccb13-119">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="ccb13-119">Requirements</span></span>



| <span data-ttu-id="ccb13-120">Condition requise</span><span class="sxs-lookup"><span data-stu-id="ccb13-120">Requirement</span></span> | <span data-ttu-id="ccb13-121">Valeur</span><span class="sxs-lookup"><span data-stu-id="ccb13-121">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="ccb13-122">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="ccb13-122">Minimum supported client</span></span><br/> | <span data-ttu-id="ccb13-123">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="ccb13-123">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="ccb13-124">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="ccb13-124">Minimum supported server</span></span><br/> | <span data-ttu-id="ccb13-125">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="ccb13-125">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="ccb13-126">En-tête</span><span class="sxs-lookup"><span data-stu-id="ccb13-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="ccb13-127"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="ccb13-127"><dt>Commctrl.h</dt></span></span> </dl> |



 

