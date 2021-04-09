---
title: Message BCM_SETIMAGELIST (commctrl. h)
description: Assigne une liste d’images à un contrôle bouton. Vous pouvez envoyer ce message de manière explicite ou utiliser le bouton \_ SetImageList macro.
ms.assetid: 805d2d9b-3e8f-4323-abaf-0dd5765cd740
keywords:
- BCM_SETIMAGELIST les contrôles de message Windows
topic_type:
- apiref
api_name:
- BCM_SETIMAGELIST
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c9bdf29735958f3c40af544bca4b946458df8431
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104032762"
---
# <a name="bcm_setimagelist-message"></a><span data-ttu-id="446e4-105">\_Message SETIMAGELIST BCM</span><span class="sxs-lookup"><span data-stu-id="446e4-105">BCM\_SETIMAGELIST message</span></span>

<span data-ttu-id="446e4-106">Assigne une liste d’images à un contrôle bouton.</span><span class="sxs-lookup"><span data-stu-id="446e4-106">Assigns an image list to a button control.</span></span> <span data-ttu-id="446e4-107">Vous pouvez envoyer ce message de manière explicite ou utiliser le [**bouton \_ SetImageList**](/windows/desktop/api/Commctrl/nf-commctrl-button_setimagelist) macro.</span><span class="sxs-lookup"><span data-stu-id="446e4-107">You can send this message explicitly or use the [**Button\_SetImageList**](/windows/desktop/api/Commctrl/nf-commctrl-button_setimagelist) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="446e4-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="446e4-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="446e4-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="446e4-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="446e4-110">Non utilisé ; doit être égal à zéro.</span><span class="sxs-lookup"><span data-stu-id="446e4-110">Not used; must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="446e4-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="446e4-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="446e4-112">Pointeur vers une structure [**\_ IMAGELIST de bouton**](/windows/desktop/api/Commctrl/ns-commctrl-button_imagelist) qui contient des informations sur la liste d’images.</span><span class="sxs-lookup"><span data-stu-id="446e4-112">A pointer to a [**BUTTON\_IMAGELIST**](/windows/desktop/api/Commctrl/ns-commctrl-button_imagelist) structure that contains image list information.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="446e4-113">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="446e4-113">Return value</span></span>

<span data-ttu-id="446e4-114">Si le message est correctement exécuté, la méthode retourne la **valeur true**.</span><span class="sxs-lookup"><span data-stu-id="446e4-114">If the message succeeds, it returns **TRUE**.</span></span> <span data-ttu-id="446e4-115">Sinon, elle retourne **false**.</span><span class="sxs-lookup"><span data-stu-id="446e4-115">Otherwise it returns **FALSE**.</span></span>

## <a name="remarks"></a><span data-ttu-id="446e4-116">Notes</span><span class="sxs-lookup"><span data-stu-id="446e4-116">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="446e4-117">Pour utiliser ce message, vous devez fournir un manifeste spécifiant Comclt32.dll version 6,0.</span><span class="sxs-lookup"><span data-stu-id="446e4-117">To use this message, you must provide a manifest specifying Comclt32.dll version 6.0.</span></span> <span data-ttu-id="446e4-118">Pour plus d’informations sur les manifestes, consultez [activation des styles visuels](cookbook-overview.md).</span><span class="sxs-lookup"><span data-stu-id="446e4-118">For more information on manifests, see [Enabling Visual Styles](cookbook-overview.md).</span></span>

 

<span data-ttu-id="446e4-119">La liste d’images référencée dans le membre **himl** de la structure [**\_ IMAGELIST Button**](/windows/desktop/api/Commctrl/ns-commctrl-button_imagelist) doit contenir une seule image à utiliser pour tous les États ou des images individuelles pour chaque État.</span><span class="sxs-lookup"><span data-stu-id="446e4-119">The image list referred to in the **himl** member of the [**BUTTON\_IMAGELIST**](/windows/desktop/api/Commctrl/ns-commctrl-button_imagelist) structure should contain either a single image to be used for all states or individual images for each state.</span></span> <span data-ttu-id="446e4-120">Les États suivants sont définis dans vssym32. h.</span><span class="sxs-lookup"><span data-stu-id="446e4-120">The following states are defined in vssym32.h.</span></span>

``` syntax
enum PUSHBUTTONSTATES {
    PBS_NORMAL = 1,
    PBS_HOT = 2,
    PBS_PRESSED = 3,
    PBS_DISABLED = 4,
    PBS_DEFAULTED = 5,
    PBS_STYLUSHOT = 6,
};
```

<span data-ttu-id="446e4-121">Notez que PBS \_ STYLUSHOT est utilisé uniquement sur les Tablet PC.</span><span class="sxs-lookup"><span data-stu-id="446e4-121">Note that PBS\_STYLUSHOT is used only on tablet computers.</span></span>

<span data-ttu-id="446e4-122">Chaque valeur est un index de l’image appropriée dans la liste d’images.</span><span class="sxs-lookup"><span data-stu-id="446e4-122">Each value is an index to the appropriate image in the image list.</span></span> <span data-ttu-id="446e4-123">Si une seule image est présente, elle est utilisée pour tous les États.</span><span class="sxs-lookup"><span data-stu-id="446e4-123">If only one image is present, it is used for all states.</span></span> <span data-ttu-id="446e4-124">Si la liste d’images contient plus d’une image, chaque index correspond à un État du bouton.</span><span class="sxs-lookup"><span data-stu-id="446e4-124">If the image list contains more than one image, each index corresponds to one state of the button.</span></span> <span data-ttu-id="446e4-125">Si aucune image n’est fournie pour chaque État, rien n’est dessiné pour ces États sans images.</span><span class="sxs-lookup"><span data-stu-id="446e4-125">If an image is not provided for each state, nothing is drawn for those states without images.</span></span>

## <a name="requirements"></a><span data-ttu-id="446e4-126">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="446e4-126">Requirements</span></span>



| <span data-ttu-id="446e4-127">Condition requise</span><span class="sxs-lookup"><span data-stu-id="446e4-127">Requirement</span></span> | <span data-ttu-id="446e4-128">Valeur</span><span class="sxs-lookup"><span data-stu-id="446e4-128">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="446e4-129">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="446e4-129">Minimum supported client</span></span><br/> | <span data-ttu-id="446e4-130">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="446e4-130">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="446e4-131">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="446e4-131">Minimum supported server</span></span><br/> | <span data-ttu-id="446e4-132">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="446e4-132">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="446e4-133">En-tête</span><span class="sxs-lookup"><span data-stu-id="446e4-133">Header</span></span><br/>                   | <dl> <span data-ttu-id="446e4-134"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="446e4-134"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





