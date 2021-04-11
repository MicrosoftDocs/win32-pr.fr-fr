---
title: Message TBM_SETBUDDY (commctrl. h)
description: Assigne une fenêtre comme fenêtre associée pour un contrôle TrackBar. Les fenêtres de l’ami TrackBar s’affichent automatiquement à un emplacement relatif à l’orientation du contrôle (horizontale ou verticale).
ms.assetid: ab35911f-bf81-47f3-98aa-0901aa877dea
keywords:
- TBM_SETBUDDY les contrôles de message Windows
topic_type:
- apiref
api_name:
- TBM_SETBUDDY
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ab33e53117933390d7a34ec75a49724003255108
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104032560"
---
# <a name="tbm_setbuddy-message"></a><span data-ttu-id="b7497-105">\_Message TBM SETBUDDY</span><span class="sxs-lookup"><span data-stu-id="b7497-105">TBM\_SETBUDDY message</span></span>

<span data-ttu-id="b7497-106">Assigne une fenêtre comme fenêtre associée pour un contrôle TrackBar.</span><span class="sxs-lookup"><span data-stu-id="b7497-106">Assigns a window as the buddy window for a trackbar control.</span></span> <span data-ttu-id="b7497-107">Les fenêtres de l’ami TrackBar s’affichent automatiquement à un emplacement relatif à l’orientation du contrôle (horizontale ou verticale).</span><span class="sxs-lookup"><span data-stu-id="b7497-107">Trackbar buddy windows are automatically displayed in a location relative to the control's orientation (horizontal or vertical).</span></span>

## <a name="parameters"></a><span data-ttu-id="b7497-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="b7497-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b7497-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="b7497-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="b7497-110">Valeur spécifiant l’emplacement d’affichage de la fenêtre associée.</span><span class="sxs-lookup"><span data-stu-id="b7497-110">Value specifying the location at which to display the buddy window.</span></span> <span data-ttu-id="b7497-111">Cette valeur peut être l'une des suivantes :</span><span class="sxs-lookup"><span data-stu-id="b7497-111">This value can be one of the following:</span></span>



| <span data-ttu-id="b7497-112">Valeur</span><span class="sxs-lookup"><span data-stu-id="b7497-112">Value</span></span>                                                                                                                                | <span data-ttu-id="b7497-113">Signification</span><span class="sxs-lookup"><span data-stu-id="b7497-113">Meaning</span></span>                                                                                                                                                                                                                                                                                         |
|--------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="TRUE"></span><span id="true"></span><dl> <span data-ttu-id="b7497-114"><dt>**:**</dt></span><span class="sxs-lookup"><span data-stu-id="b7497-114"><dt>**TRUE**</dt></span></span> </dl>    | <span data-ttu-id="b7497-115">L’ami s’affiche à gauche du TrackBar si le contrôle TrackBar utilise le style de ligne de commande [**tbs \_**](trackbar-control-styles.md) .</span><span class="sxs-lookup"><span data-stu-id="b7497-115">The buddy will appear to the left of the trackbar if the trackbar control uses the [**TBS\_HORZ**](trackbar-control-styles.md) style.</span></span> <span data-ttu-id="b7497-116">Si le TrackBar utilise le style [**tbs \_ vert**](trackbar-control-styles.md) , l’ami s’affiche au-dessus du contrôle TrackBar.</span><span class="sxs-lookup"><span data-stu-id="b7497-116">If the trackbar uses the [**TBS\_VERT**](trackbar-control-styles.md) style, the buddy appears above the trackbar control.</span></span><br/>  |
| <span id="FALSE"></span><span id="false"></span><dl> <span data-ttu-id="b7497-117"><dt>**FAUSSES**</dt></span><span class="sxs-lookup"><span data-stu-id="b7497-117"><dt>**FALSE**</dt></span></span> </dl> | <span data-ttu-id="b7497-118">L’ami s’affiche à droite du TrackBar si le contrôle TrackBar utilise le style de ligne de commande [**tbs \_**](trackbar-control-styles.md) .</span><span class="sxs-lookup"><span data-stu-id="b7497-118">The buddy will appear to the right of the trackbar if the trackbar control uses the [**TBS\_HORZ**](trackbar-control-styles.md) style.</span></span> <span data-ttu-id="b7497-119">Si le TrackBar utilise le style [**tbs \_ vert**](trackbar-control-styles.md) , l’ami apparaît sous le contrôle TrackBar.</span><span class="sxs-lookup"><span data-stu-id="b7497-119">If the trackbar uses the [**TBS\_VERT**](trackbar-control-styles.md) style, the buddy appears below the trackbar control.</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="b7497-120">*lParam*</span><span class="sxs-lookup"><span data-stu-id="b7497-120">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="b7497-121">Handle de la fenêtre qui sera définie en tant que Buddy du contrôle TrackBar.</span><span class="sxs-lookup"><span data-stu-id="b7497-121">Handle to the window that will be set as the trackbar control's buddy.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b7497-122">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="b7497-122">Return value</span></span>

<span data-ttu-id="b7497-123">Retourne le handle de la fenêtre précédemment assignée au contrôle à cet emplacement.</span><span class="sxs-lookup"><span data-stu-id="b7497-123">Returns the handle to the window that was previously assigned to the control at that location.</span></span>

## <a name="remarks"></a><span data-ttu-id="b7497-124">Notes</span><span class="sxs-lookup"><span data-stu-id="b7497-124">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="b7497-125">Les contrôles TrackBar prennent en charge jusqu’à deux fenêtres d’amis.</span><span class="sxs-lookup"><span data-stu-id="b7497-125">Trackbar controls support up to two buddy windows.</span></span> <span data-ttu-id="b7497-126">Cela peut être utile lorsque vous devez afficher du texte ou des images à chaque extrémité du contrôle.</span><span class="sxs-lookup"><span data-stu-id="b7497-126">This can be useful when you must display text or images at each end of the control.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="b7497-127">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="b7497-127">Requirements</span></span>



| <span data-ttu-id="b7497-128">Condition requise</span><span class="sxs-lookup"><span data-stu-id="b7497-128">Requirement</span></span> | <span data-ttu-id="b7497-129">Valeur</span><span class="sxs-lookup"><span data-stu-id="b7497-129">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="b7497-130">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="b7497-130">Minimum supported client</span></span><br/> | <span data-ttu-id="b7497-131">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="b7497-131">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="b7497-132">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="b7497-132">Minimum supported server</span></span><br/> | <span data-ttu-id="b7497-133">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="b7497-133">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="b7497-134">En-tête</span><span class="sxs-lookup"><span data-stu-id="b7497-134">Header</span></span><br/>                   | <dl> <span data-ttu-id="b7497-135"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="b7497-135"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





