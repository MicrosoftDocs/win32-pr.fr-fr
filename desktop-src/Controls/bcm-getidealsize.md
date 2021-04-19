---
title: Message BCM_GETIDEALSIZE (commctrl. h)
description: Obtient la taille du bouton qui correspond le mieux à son texte et à son image, si une liste d’images est présente. Vous pouvez envoyer ce message de manière explicite ou utiliser le bouton \_ GetIdealSize macro.
ms.assetid: c1bc2043-bf1a-4129-a005-f04048c4c1db
keywords:
- BCM_GETIDEALSIZE les contrôles de message Windows
topic_type:
- apiref
api_name:
- BCM_GETIDEALSIZE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 446f4acba39b8b9722ef1a01a223f671b56ae845
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "106510139"
---
# <a name="bcm_getidealsize-message"></a><span data-ttu-id="5a88c-105">\_Message GETIDEALSIZE BCM</span><span class="sxs-lookup"><span data-stu-id="5a88c-105">BCM\_GETIDEALSIZE message</span></span>

<span data-ttu-id="5a88c-106">Obtient la taille du bouton qui correspond le mieux à son texte et à son image, si une liste d’images est présente.</span><span class="sxs-lookup"><span data-stu-id="5a88c-106">Gets the size of the button that best fits its text and image, if an image list is present.</span></span> <span data-ttu-id="5a88c-107">Vous pouvez envoyer ce message de manière explicite ou utiliser le [**bouton \_ GetIdealSize**](/windows/desktop/api/Commctrl/nf-commctrl-button_getidealsize) macro.</span><span class="sxs-lookup"><span data-stu-id="5a88c-107">You can send this message explicitly or use the [**Button\_GetIdealSize**](/windows/desktop/api/Commctrl/nf-commctrl-button_getidealsize) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="5a88c-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="5a88c-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5a88c-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="5a88c-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="5a88c-110">Non utilisé ; doit être égal à zéro.</span><span class="sxs-lookup"><span data-stu-id="5a88c-110">Not used; must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="5a88c-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="5a88c-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="5a88c-112">Pointeur vers une structure de [**taille**](/previous-versions//dd145106(v=vs.85)) qui reçoit la taille souhaitée du bouton, y compris le texte et la liste d’images, le cas échéant.</span><span class="sxs-lookup"><span data-stu-id="5a88c-112">A pointer to a [**SIZE**](/previous-versions//dd145106(v=vs.85)) structure that receives the desired size of the button, including text and image list, if present.</span></span> <span data-ttu-id="5a88c-113">L’application appelante est chargée d’allouer cette structure.</span><span class="sxs-lookup"><span data-stu-id="5a88c-113">The calling application is responsible for allocating this structure.</span></span> <span data-ttu-id="5a88c-114">Définissez les membres **CX** et **CY** sur zéro pour que la hauteur et la largeur idéales soient retournées dans la structure **Size** .</span><span class="sxs-lookup"><span data-stu-id="5a88c-114">Set the **cx** and **cy** members to zero to have the ideal height and width returned in the **SIZE** structure.</span></span> <span data-ttu-id="5a88c-115">Pour spécifier une largeur de bouton, définissez le membre **CX** sur la largeur de bouton souhaitée.</span><span class="sxs-lookup"><span data-stu-id="5a88c-115">To specify a button width, set the **cx** member to the desired button width.</span></span> <span data-ttu-id="5a88c-116">Le système calcule la hauteur idéale pour cette largeur et le retourne dans le membre **CY** .</span><span class="sxs-lookup"><span data-stu-id="5a88c-116">The system will calculate the ideal height for this width and return it in the **cy** member.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5a88c-117">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="5a88c-117">Return value</span></span>

<span data-ttu-id="5a88c-118">Si le message est correctement exécuté, la méthode retourne la **valeur true**.</span><span class="sxs-lookup"><span data-stu-id="5a88c-118">If the message succeeds, it returns **TRUE**.</span></span> <span data-ttu-id="5a88c-119">Sinon, elle retourne **false**.</span><span class="sxs-lookup"><span data-stu-id="5a88c-119">Otherwise it returns **FALSE**.</span></span>

## <a name="remarks"></a><span data-ttu-id="5a88c-120">Notes</span><span class="sxs-lookup"><span data-stu-id="5a88c-120">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="5a88c-121">Si aucune largeur de bouton spéciale n’est souhaitée, vous devez définir les deux membres de [**Size**](/previous-versions//dd145106(v=vs.85)) sur zéro pour calculer et retourner la hauteur et la largeur idéales.</span><span class="sxs-lookup"><span data-stu-id="5a88c-121">If no special button width is desired, then you must set both members of [**SIZE**](/previous-versions//dd145106(v=vs.85)) to zero to calculate and return the ideal height and width.</span></span> <span data-ttu-id="5a88c-122">Si la valeur du membre **CX** est supérieure à zéro, cette valeur est considérée comme la largeur de bouton souhaitée et la hauteur idéale pour cette largeur est calculée et retournée dans le membre **CY** .</span><span class="sxs-lookup"><span data-stu-id="5a88c-122">If the value of the **cx** member is greater than zero, then this value is considered the desired button width, and the ideal height for this width is calculated and returned in the **cy** member.</span></span>

 

<span data-ttu-id="5a88c-123">Ce message s’applique aux boutons de bouton.</span><span class="sxs-lookup"><span data-stu-id="5a88c-123">This message is most applicable to PushButtons.</span></span> <span data-ttu-id="5a88c-124">Lorsqu’il est envoyé à un PushButton, le message récupère le rectangle englobant requis pour afficher le texte du bouton.</span><span class="sxs-lookup"><span data-stu-id="5a88c-124">When sent to a PushButton, the message retrieves the bounding rectangle required to display the button's text.</span></span> <span data-ttu-id="5a88c-125">En outre, si le PushButton a une liste d’images, le rectangle englobant est également dimensionné pour inclure l’image du bouton.</span><span class="sxs-lookup"><span data-stu-id="5a88c-125">Additionally, if the PushButton has an image list, the bounding rectangle is also sized to include the button's image.</span></span>

<span data-ttu-id="5a88c-126">Lorsqu’elle est envoyée à un bouton de tout autre type, la taille du rectangle de fenêtre du contrôle est récupérée.</span><span class="sxs-lookup"><span data-stu-id="5a88c-126">When sent to a button of any other type, the size of the control's window rectangle is retrieved.</span></span>

> [!Note]  
> <span data-ttu-id="5a88c-127">Pour utiliser ce message, vous devez fournir un manifeste spécifiant Comclt32.dll version 6,0.</span><span class="sxs-lookup"><span data-stu-id="5a88c-127">To use this message, you must provide a manifest specifying Comclt32.dll version 6.0.</span></span> <span data-ttu-id="5a88c-128">Pour plus d’informations sur les manifestes, consultez [activation des styles visuels](cookbook-overview.md).</span><span class="sxs-lookup"><span data-stu-id="5a88c-128">For more information on manifests, see [Enabling Visual Styles](cookbook-overview.md).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="5a88c-129">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="5a88c-129">Requirements</span></span>



| <span data-ttu-id="5a88c-130">Condition requise</span><span class="sxs-lookup"><span data-stu-id="5a88c-130">Requirement</span></span> | <span data-ttu-id="5a88c-131">Valeur</span><span class="sxs-lookup"><span data-stu-id="5a88c-131">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="5a88c-132">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="5a88c-132">Minimum supported client</span></span><br/> | <span data-ttu-id="5a88c-133">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="5a88c-133">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="5a88c-134">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="5a88c-134">Minimum supported server</span></span><br/> | <span data-ttu-id="5a88c-135">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="5a88c-135">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="5a88c-136">En-tête</span><span class="sxs-lookup"><span data-stu-id="5a88c-136">Header</span></span><br/>                   | <dl> <span data-ttu-id="5a88c-137"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="5a88c-137"><dt>Commctrl.h</dt></span></span> </dl> |



 

