---
title: Constantes et énumérations DWM
description: Cette section contient des informations sur les constantes et énumérations utilisées dans les API Gestionnaire de fenêtrage (DWM).
ms.assetid: b01f620d-ac87-4e93-88ab-f4297d8cf1d5
keywords:
- Gestionnaire de fenêtrage (DWM), référence
- DWM (Gestionnaire de fenêtrage), référence
- Gestionnaire de fenêtrage (DWM), constantes
- DWM (Gestionnaire de fenêtrage), constantes
- Gestionnaire de fenêtrage (DWM), énumérations
- DWM (Gestionnaire de fenêtrage), énumérations
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 280fff527f95176b47fc99f88d09453dbf579f38
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103673657"
---
# <a name="dwm-constants-and-enumerations"></a><span data-ttu-id="66b6d-109">Constantes et énumérations DWM</span><span class="sxs-lookup"><span data-stu-id="66b6d-109">DWM Constants and Enumerations</span></span>

<span data-ttu-id="66b6d-110">Cette section contient des informations sur les constantes et énumérations utilisées dans les API Gestionnaire de fenêtrage (DWM).</span><span class="sxs-lookup"><span data-stu-id="66b6d-110">This section contains information about the constants and enumerations used in the Desktop Window Manager (DWM) APIs.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="66b6d-111">Contenu de cette section</span><span class="sxs-lookup"><span data-stu-id="66b6d-111">In this section</span></span>



| <span data-ttu-id="66b6d-112">Rubrique</span><span class="sxs-lookup"><span data-stu-id="66b6d-112">Topic</span></span>                                                                                     | <span data-ttu-id="66b6d-113">Description</span><span class="sxs-lookup"><span data-stu-id="66b6d-113">Description</span></span>                                                                                                                                                                                                     |
|-------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="66b6d-114">**Brouilleur de DWM derrière les constantes**</span><span class="sxs-lookup"><span data-stu-id="66b6d-114">**DWM Blur Behind Constants**</span></span>](dwm-bb-constants.md)<br/>                          | <span data-ttu-id="66b6d-115">Indicateurs utilisés par la structure [**DWM \_ BLURBEHIND**](/windows/desktop/api/Dwmapi/ns-dwmapi-dwm_blurbehind) pour indiquer les membres qui contiennent des informations valides.</span><span class="sxs-lookup"><span data-stu-id="66b6d-115">Flags used by the [**DWM\_BLURBEHIND**](/windows/desktop/api/Dwmapi/ns-dwmapi-dwm_blurbehind) structure to indicate which of its members contain valid information.</span></span><br/>                                                                    |
| [<span data-ttu-id="66b6d-116">**DWM-activer les constantes de composition**</span><span class="sxs-lookup"><span data-stu-id="66b6d-116">**DWM Enable Composition Constants**</span></span>](dwm-ec-constants.md)<br/>                   | <span data-ttu-id="66b6d-117">Indicateurs utilisés par la fonction [**DwmEnableComposition**](/windows/desktop/api/Dwmapi/nf-dwmapi-dwmenablecomposition)  pour modifier l’état de la composition DWM.</span><span class="sxs-lookup"><span data-stu-id="66b6d-117">Flags used by the [**DwmEnableComposition**](/windows/desktop/api/Dwmapi/nf-dwmapi-dwmenablecomposition)  function to change the state of DWM composition.</span></span><br/>                                                                             |
| [<span data-ttu-id="66b6d-118">**\_échantillonnage de \_ frame \_ source DWM**</span><span class="sxs-lookup"><span data-stu-id="66b6d-118">**DWM\_SOURCE\_FRAME\_SAMPLING**</span></span>](/windows/desktop/api/Dwmapi/ne-dwmapi-dwm_source_frame_sampling)<br/>              | <span data-ttu-id="66b6d-119">Indicateurs utilisés par la fonction [**DwmSetPresentParameters**](/windows/desktop/api/Dwmapi/nf-dwmapi-dwmsetpresentparameters) pour spécifier le type d’échantillonnage de frame.</span><span class="sxs-lookup"><span data-stu-id="66b6d-119">Flags used by the [**DwmSetPresentParameters**](/windows/desktop/api/Dwmapi/nf-dwmapi-dwmsetpresentparameters) function to specify the frame sampling type.</span></span><br/>                                                                            |
| [<span data-ttu-id="66b6d-120">**\_ \_ conditions requises pour les fenêtres d’onglet DWM \_**</span><span class="sxs-lookup"><span data-stu-id="66b6d-120">**DWM\_TAB\_WINDOW\_REQUIREMENTS**</span></span>](/windows/desktop/api/dwmapi/ne-dwmapi-dwm_tab_window_requirements)<br/>          | <span data-ttu-id="66b6d-121">Retourné par DwmGetUnmetTabRequirements pour indiquer les conditions requises pour qu’une fenêtre place des onglets dans la barre de titre de l’application.</span><span class="sxs-lookup"><span data-stu-id="66b6d-121">Returned by DwmGetUnmetTabRequirements to indicate the requirements needed for a window to put tabs in the application title bar.</span></span><br/>                                                                    |
| [<span data-ttu-id="66b6d-122">**\_Constantes DWM TNP**</span><span class="sxs-lookup"><span data-stu-id="66b6d-122">**DWM\_TNP Constants**</span></span>](dwm-tnp-constants.md)<br/>                                | <span data-ttu-id="66b6d-123">Indicateurs utilisés par la structure des [**\_ \_ Propriétés de la miniature DWM**](/windows/desktop/api/Dwmapi/ns-dwmapi-dwm_thumbnail_properties) pour indiquer les membres qui contiennent des informations valides.</span><span class="sxs-lookup"><span data-stu-id="66b6d-123">Flags used by the [**DWM\_THUMBNAIL\_PROPERTIES**](/windows/desktop/api/Dwmapi/ns-dwmapi-dwm_thumbnail_properties) structure to indicate which of its members contain valid information.</span></span><br/>                                               |
| [<span data-ttu-id="66b6d-124">**DWMFLIP3DWINDOWPOLICY**</span><span class="sxs-lookup"><span data-stu-id="66b6d-124">**DWMFLIP3DWINDOWPOLICY**</span></span>](/windows/desktop/api/Dwmapi/ne-dwmapi-dwmflip3dwindowpolicy)<br/>                         | <span data-ttu-id="66b6d-125">Indicateurs utilisés par la fonction [**DwmSetWindowAttribute**](/windows/desktop/api/Dwmapi/nf-dwmapi-dwmsetwindowattribute) pour spécifier la stratégie de fenêtre Flip3D.</span><span class="sxs-lookup"><span data-stu-id="66b6d-125">Flags used by the [**DwmSetWindowAttribute**](/windows/desktop/api/Dwmapi/nf-dwmapi-dwmsetwindowattribute) function to specify the Flip3D window policy.</span></span><br/>                                                                               |
| [<span data-ttu-id="66b6d-126">**DWMNCRENDERINGPOLICY**</span><span class="sxs-lookup"><span data-stu-id="66b6d-126">**DWMNCRENDERINGPOLICY**</span></span>](/windows/desktop/api/Dwmapi/ne-dwmapi-dwmncrenderingpolicy)<br/>                           | <span data-ttu-id="66b6d-127">Indicateurs utilisés par la fonction [**DwmSetWindowAttribute**](/windows/desktop/api/Dwmapi/nf-dwmapi-dwmsetwindowattribute) pour spécifier la stratégie de rendu de la zone non cliente.</span><span class="sxs-lookup"><span data-stu-id="66b6d-127">Flags used by the [**DwmSetWindowAttribute**](/windows/desktop/api/Dwmapi/nf-dwmapi-dwmsetwindowattribute) function to specify the non-client area rendering policy.</span></span><br/>                                                                   |
| [<span data-ttu-id="66b6d-128">**DWMTRANSITION \_ OWNEDWINDOW \_ cible**</span><span class="sxs-lookup"><span data-stu-id="66b6d-128">**DWMTRANSITION\_OWNEDWINDOW\_TARGET**</span></span>](/windows/desktop/api/Dwmapi/ne-dwmapi-dwmtransition_ownedwindow_target)<br/> | <span data-ttu-id="66b6d-129">Identifie la cible.</span><span class="sxs-lookup"><span data-stu-id="66b6d-129">Identifies the target.</span></span><br/>                                                                                                                                                                               |
| [<span data-ttu-id="66b6d-130">**DWMWINDOWATTRIBUTE**</span><span class="sxs-lookup"><span data-stu-id="66b6d-130">**DWMWINDOWATTRIBUTE**</span></span>](/windows/desktop/api/Dwmapi/ne-dwmapi-dwmwindowattribute)<br/>                               | <span data-ttu-id="66b6d-131">Indicateurs utilisés par les fonctions [**DwmGetWindowAttribute**](/windows/desktop/api/Dwmapi/nf-dwmapi-dwmgetwindowattribute) et [**DwmSetWindowAttribute**](/windows/desktop/api/Dwmapi/nf-dwmapi-dwmsetwindowattribute) pour spécifier les attributs de fenêtre pour le rendu non-client.</span><span class="sxs-lookup"><span data-stu-id="66b6d-131">Flags used by the [**DwmGetWindowAttribute**](/windows/desktop/api/Dwmapi/nf-dwmapi-dwmgetwindowattribute) and [**DwmSetWindowAttribute**](/windows/desktop/api/Dwmapi/nf-dwmapi-dwmsetwindowattribute) functions to specify window attributes for non-client rendering.</span></span><br/> |
| [<span data-ttu-id="66b6d-132">**TYPE de mouvement \_**</span><span class="sxs-lookup"><span data-stu-id="66b6d-132">**GESTURE\_TYPE**</span></span>](/windows/desktop/api/Dwmapi/ne-dwmapi-gesture_type)<br/>                                          | <span data-ttu-id="66b6d-133">Identifie le type de mouvement spécifié dans [**DwmRenderGesture**](/windows/desktop/api/Dwmapi/nf-dwmapi-dwmrendergesture).</span><span class="sxs-lookup"><span data-stu-id="66b6d-133">Identifies the gesture type specified in [**DwmRenderGesture**](/windows/desktop/api/Dwmapi/nf-dwmapi-dwmrendergesture).</span></span><br/>                                                                                                               |



 

 

 





