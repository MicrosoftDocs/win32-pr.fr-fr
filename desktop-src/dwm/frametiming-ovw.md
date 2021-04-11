---
title: Accès et contrôle des données de frame DWM
description: Cette rubrique décrit les API Gestionnaire de fenêtrage (DWM) utilisées pour la planification et la présentation multimédia.
ms.assetid: e5d010ea-8411-4537-b9f8-6dc84841087a
keywords:
- Gestionnaire de fenêtrage (DWM), planification et API de présentation multimédia
- DWM (Gestionnaire de fenêtrage), planification et API de présentation multimédia
- API de planification et de présentation multimédia
- Gestionnaire de fenêtrage (DWM), accéder aux données de frame
- DWM (Gestionnaire de fenêtrage), accéder aux données de frame
- accès aux données de frame
- Gestionnaire de fenêtrage (DWM), contrôle des données de frame
- DWM (Gestionnaire de fenêtrage), contrôle des données de frame
- contrôle des données de frame
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0a577847dc20883c84af680d1c39e285a6085e70
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104310181"
---
# <a name="accessing-and-controlling-dwm-frame-data"></a><span data-ttu-id="b4ed8-112">Accès et contrôle des données de frame DWM</span><span class="sxs-lookup"><span data-stu-id="b4ed8-112">Accessing and Controlling DWM Frame Data</span></span>

<span data-ttu-id="b4ed8-113">Cette rubrique décrit les API Gestionnaire de fenêtrage (DWM) utilisées pour la planification et la présentation multimédia.</span><span class="sxs-lookup"><span data-stu-id="b4ed8-113">This topic discusses the Desktop Window Manager (DWM) APIs that are used for scheduling and media presentation.</span></span>

## <a name="dwm-frame-timing-api"></a><span data-ttu-id="b4ed8-114">API de minutage des frames DWM</span><span class="sxs-lookup"><span data-stu-id="b4ed8-114">DWM Frame Timing API</span></span>

<span data-ttu-id="b4ed8-115">Les API de planification et de présentation multimédia permettent de contrôler plus en détail le moment où l’image de bureau est composite et présentée.</span><span class="sxs-lookup"><span data-stu-id="b4ed8-115">The scheduling and media presentation APIs enable more detailed control of when the desktop image is composited and presented.</span></span> <span data-ttu-id="b4ed8-116">Cela est généralement nécessaire pour les applications de lecture vidéo et de média pour lesquelles le DWM s’exécute de façon asynchrone avec leur propre planification de présentation, ce qui peut entraîner des artefacts d’échantillonnage s’ils ne sont pas étroitement contrôlés.</span><span class="sxs-lookup"><span data-stu-id="b4ed8-116">This is typically needed by media and video playback applications for whom the DWM is running asynchronously with their own presentation schedule, which can lead to sampling artifacts if not tightly controlled.</span></span>

<span data-ttu-id="b4ed8-117">Les fonctions de planification et de présentation multimédia sont les suivantes.</span><span class="sxs-lookup"><span data-stu-id="b4ed8-117">The scheduling and media presentation functions include the following.</span></span> <span data-ttu-id="b4ed8-118">Les détails de leur utilisation se trouvent sur ces pages.</span><span class="sxs-lookup"><span data-stu-id="b4ed8-118">Details of their use are found on those pages.</span></span>

-   <span data-ttu-id="b4ed8-119">[**DwmEnableMMCSS**](/windows/desktop/api/Dwmapi/nf-dwmapi-dwmenablemmcss).</span><span class="sxs-lookup"><span data-stu-id="b4ed8-119">[**DwmEnableMMCSS**](/windows/desktop/api/Dwmapi/nf-dwmapi-dwmenablemmcss).</span></span> <span data-ttu-id="b4ed8-120">Notifie le DWM d’activer la planification de service de planification de classe multimédia (MMCSS) pendant que le processus appelant est actif.</span><span class="sxs-lookup"><span data-stu-id="b4ed8-120">Notifies the DWM to enable Multimedia Class Schedule Service (MMCSS) scheduling while the calling process is alive.</span></span>
-   <span data-ttu-id="b4ed8-121">[**DwmGetCompositionTimingInfo**](/windows/desktop/api/Dwmapi/nf-dwmapi-dwmgetcompositiontiminginfo).</span><span class="sxs-lookup"><span data-stu-id="b4ed8-121">[**DwmGetCompositionTimingInfo**](/windows/desktop/api/Dwmapi/nf-dwmapi-dwmgetcompositiontiminginfo).</span></span> <span data-ttu-id="b4ed8-122">Récupère les informations de minutage de la composition actuelle.</span><span class="sxs-lookup"><span data-stu-id="b4ed8-122">Retrieves the current composition timing information.</span></span>
-   <span data-ttu-id="b4ed8-123">[**DwmModifyPreviousDxFrameDuration**](/windows/desktop/api/Dwmapi/nf-dwmapi-dwmmodifypreviousdxframeduration).</span><span class="sxs-lookup"><span data-stu-id="b4ed8-123">[**DwmModifyPreviousDxFrameDuration**](/windows/desktop/api/Dwmapi/nf-dwmapi-dwmmodifypreviousdxframeduration).</span></span> <span data-ttu-id="b4ed8-124">Modifie le nombre d’actualisations pendant lesquelles le frame précédent s’affiche.</span><span class="sxs-lookup"><span data-stu-id="b4ed8-124">Changes the number of refreshes during which the previous frame will be displayed.</span></span>
-   <span data-ttu-id="b4ed8-125">[**DwmSetDxFrameDuration**](/windows/desktop/api/Dwmapi/nf-dwmapi-dwmsetdxframeduration).</span><span class="sxs-lookup"><span data-stu-id="b4ed8-125">[**DwmSetDxFrameDuration**](/windows/desktop/api/Dwmapi/nf-dwmapi-dwmsetdxframeduration).</span></span> <span data-ttu-id="b4ed8-126">Définit le nombre d’actualisations dans lesquelles afficher le frame présenté.</span><span class="sxs-lookup"><span data-stu-id="b4ed8-126">Sets the number of refreshes in which to display the presented frame.</span></span>
-   <span data-ttu-id="b4ed8-127">[**DwmSetPresentParameters**](/windows/desktop/api/Dwmapi/nf-dwmapi-dwmsetpresentparameters).</span><span class="sxs-lookup"><span data-stu-id="b4ed8-127">[**DwmSetPresentParameters**](/windows/desktop/api/Dwmapi/nf-dwmapi-dwmsetpresentparameters).</span></span> <span data-ttu-id="b4ed8-128">Définit les paramètres présents pour la composition de frame.</span><span class="sxs-lookup"><span data-stu-id="b4ed8-128">Sets the present parameters for frame composition.</span></span>

 

 




