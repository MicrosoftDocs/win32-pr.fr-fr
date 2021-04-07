---
title: Structures DWM
description: Cette section contient des informations sur les structures de Gestionnaire de fenêtrage (DWM).
ms.assetid: 26b36617-54c2-405a-9a7d-bd86fefa94b6
keywords:
- Gestionnaire de fenêtrage (DWM), référence
- DWM (Gestionnaire de fenêtrage), référence
- Gestionnaire de fenêtrage (DWM), structures
- DWM (Gestionnaire de fenêtrage), structures
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5f212d248c0f70cfd51e6e47b2d37c89d24f630b
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104029242"
---
# <a name="dwm-structures"></a><span data-ttu-id="1f216-107">Structures DWM</span><span class="sxs-lookup"><span data-stu-id="1f216-107">DWM Structures</span></span>

<span data-ttu-id="1f216-108">Cette section contient des informations sur les structures de Gestionnaire de fenêtrage (DWM).</span><span class="sxs-lookup"><span data-stu-id="1f216-108">This section contains information about the Desktop Window Manager (DWM) structures.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="1f216-109">Contenu de cette section</span><span class="sxs-lookup"><span data-stu-id="1f216-109">In this section</span></span>



| <span data-ttu-id="1f216-110">Rubrique</span><span class="sxs-lookup"><span data-stu-id="1f216-110">Topic</span></span>                                                                     | <span data-ttu-id="1f216-111">Description</span><span class="sxs-lookup"><span data-stu-id="1f216-111">Description</span></span>                                                                                                                                               |
|---------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="1f216-112">**\_BLURBEHIND DWM**</span><span class="sxs-lookup"><span data-stu-id="1f216-112">**DWM\_BLURBEHIND**</span></span>](/windows/desktop/api/Dwmapi/ns-dwmapi-dwm_blurbehind)<br/>                      | <span data-ttu-id="1f216-113">Spécifie les propriétés de l’effet de flou DWM.</span><span class="sxs-lookup"><span data-stu-id="1f216-113">Specifies DWM blur-behind properties.</span></span> <span data-ttu-id="1f216-114">Utilisé par la fonction [**DwmEnableBlurBehindWindow**](/windows/desktop/api/Dwmapi/nf-dwmapi-dwmenableblurbehindwindow) .</span><span class="sxs-lookup"><span data-stu-id="1f216-114">Used by the [**DwmEnableBlurBehindWindow**](/windows/desktop/api/Dwmapi/nf-dwmapi-dwmenableblurbehindwindow) function.</span></span><br/>                     |
| [<span data-ttu-id="1f216-115">**paramètres de DWM \_ présents \_**</span><span class="sxs-lookup"><span data-stu-id="1f216-115">**DWM\_PRESENT\_PARAMETERS**</span></span>](/windows/desktop/api/Dwmapi/ns-dwmapi-dwm_present_parameters)<br/>     | <span data-ttu-id="1f216-116">Spécifie les paramètres de trame vidéo DWM pour la composition de frame.</span><span class="sxs-lookup"><span data-stu-id="1f216-116">Specifies DWM video frame parameters for frame composition.</span></span> <span data-ttu-id="1f216-117">Utilisé par la fonction [**DwmSetPresentParameters**](/windows/desktop/api/Dwmapi/nf-dwmapi-dwmsetpresentparameters) .</span><span class="sxs-lookup"><span data-stu-id="1f216-117">Used by the [**DwmSetPresentParameters**](/windows/desktop/api/Dwmapi/nf-dwmapi-dwmsetpresentparameters) function.</span></span><br/>   |
| [<span data-ttu-id="1f216-118">**Propriétés de la \_ miniature DWM \_**</span><span class="sxs-lookup"><span data-stu-id="1f216-118">**DWM\_THUMBNAIL\_PROPERTIES**</span></span>](/windows/desktop/api/Dwmapi/ns-dwmapi-dwm_thumbnail_properties)<br/> | <span data-ttu-id="1f216-119">Spécifie les propriétés de la miniature DWM.</span><span class="sxs-lookup"><span data-stu-id="1f216-119">Specifies DWM thumbnail properties.</span></span> <span data-ttu-id="1f216-120">Utilisé par la fonction [**DwmUpdateThumbnailProperties**](/windows/desktop/api/Dwmapi/nf-dwmapi-dwmupdatethumbnailproperties) .</span><span class="sxs-lookup"><span data-stu-id="1f216-120">Used by the [**DwmUpdateThumbnailProperties**](/windows/desktop/api/Dwmapi/nf-dwmapi-dwmupdatethumbnailproperties) function.</span></span><br/>                 |
| [<span data-ttu-id="1f216-121">**\_informations de minutage DWM \_**</span><span class="sxs-lookup"><span data-stu-id="1f216-121">**DWM\_TIMING\_INFO**</span></span>](/windows/desktop/api/Dwmapi/ns-dwmapi-dwm_timing_info)<br/>                   | <span data-ttu-id="1f216-122">Spécifie les informations de minutage de la composition DWM.</span><span class="sxs-lookup"><span data-stu-id="1f216-122">Specifies DWM composition timing information.</span></span> <span data-ttu-id="1f216-123">Utilisé par la fonction [**DwmGetCompositionTimingInfo**](/windows/desktop/api/Dwmapi/nf-dwmapi-dwmgetcompositiontiminginfo) .</span><span class="sxs-lookup"><span data-stu-id="1f216-123">Used by the [**DwmGetCompositionTimingInfo**](/windows/desktop/api/Dwmapi/nf-dwmapi-dwmgetcompositiontiminginfo) function.</span></span><br/>         |
| [<span data-ttu-id="1f216-124">**MilMatrix3x2D**</span><span class="sxs-lookup"><span data-stu-id="1f216-124">**MilMatrix3x2D**</span></span>](/windows/desktop/api/Dwmapi/ns-dwmapi-milmatrix3x2d)<br/>                         | <span data-ttu-id="1f216-125">Spécifie une matrice matrice qui décrit une transformation.</span><span class="sxs-lookup"><span data-stu-id="1f216-125">Specifies a 3x2 matrix that describes a transform.</span></span> <br/>                                                                                            |
| [<span data-ttu-id="1f216-126">**RATIO non signé \_**</span><span class="sxs-lookup"><span data-stu-id="1f216-126">**UNSIGNED\_RATIO**</span></span>](/windows/desktop/api/Dwmapi/ns-dwmapi-unsigned_ratio)<br/>                      | <span data-ttu-id="1f216-127">Définit un type de données utilisé par les API DWM.</span><span class="sxs-lookup"><span data-stu-id="1f216-127">Defines a data type used by the DWM APIs.</span></span> <span data-ttu-id="1f216-128">Il représente un ratio générique et est utilisé à des fins et des unités différentes, même dans une seule API.</span><span class="sxs-lookup"><span data-stu-id="1f216-128">It represents a generic ratio and is used for different purposes and units even within a single API.</span></span><br/> |



 

 

 





