---
description: Les fonctions suivantes sont utilisées avec le gestionnaire de protection de sortie (OPM).
ms.assetid: 7ecde6ae-56fd-451b-bebb-224c6801be05
title: Fonctions OPM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e32b4ef210ace3f7f179b59980cedb962a5bee44
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106520429"
---
# <a name="opm-functions"></a><span data-ttu-id="68a27-103">Fonctions OPM</span><span class="sxs-lookup"><span data-stu-id="68a27-103">OPM Functions</span></span>

<span data-ttu-id="68a27-104">Les fonctions suivantes sont utilisées avec le [Gestionnaire de protection de sortie](output-protection-manager.md) (OPM).</span><span class="sxs-lookup"><span data-stu-id="68a27-104">The following functions are used with [Output Protection Manager](output-protection-manager.md) (OPM).</span></span>



| <span data-ttu-id="68a27-105">Fonction</span><span class="sxs-lookup"><span data-stu-id="68a27-105">Function</span></span>                                                                                             | <span data-ttu-id="68a27-106">Description</span><span class="sxs-lookup"><span data-stu-id="68a27-106">Description</span></span>                                                                                                                           |
|------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="68a27-107">**OPMGetVideoOutputForTarget**</span><span class="sxs-lookup"><span data-stu-id="68a27-107">**OPMGetVideoOutputForTarget**</span></span>](/windows/desktop/api/opmapi/nf-opmapi-opmgetvideooutputfortarget)                                     | <span data-ttu-id="68a27-108">Retourne un objet de sortie vidéo pour la cible VidPN sur l’adaptateur spécifié.</span><span class="sxs-lookup"><span data-stu-id="68a27-108">Returns a video output object for the VidPN target on the specified adapter.</span></span>                                                          |
| [<span data-ttu-id="68a27-109">**OPMGetVideoOutputsFromHMONITOR**</span><span class="sxs-lookup"><span data-stu-id="68a27-109">**OPMGetVideoOutputsFromHMONITOR**</span></span>](/windows/desktop/api/opmapi/nf-opmapi-opmgetvideooutputsfromhmonitor)                             | <span data-ttu-id="68a27-110">Crée un objet de sortie Protection Manager (OPM) pour chaque moniteur physique associé à un handle **HMONITOR** particulier.</span><span class="sxs-lookup"><span data-stu-id="68a27-110">Creates an Output Protection Manager (OPM) object for each physical monitor that is associated with a particular **HMONITOR** handle.</span></span> |
| [<span data-ttu-id="68a27-111">**OPMGetVideoOutputsFromIDirect3DDevice9Object**</span><span class="sxs-lookup"><span data-stu-id="68a27-111">**OPMGetVideoOutputsFromIDirect3DDevice9Object**</span></span>](/windows/desktop/api/opmapi/nf-opmapi-opmgetvideooutputsfromidirect3ddevice9object) | <span data-ttu-id="68a27-112">Crée un objet OPM pour chaque moniteur physique associé à un appareil Direct3D particulier.</span><span class="sxs-lookup"><span data-stu-id="68a27-112">Creates an OPM object for each physical monitor that is associated with a particular Direct3D device.</span></span>                                 |



 

<span data-ttu-id="68a27-113">Les fonctions suivantes sont utilisées par OPM pour accéder aux fonctionnalités dans le pilote d’affichage.</span><span class="sxs-lookup"><span data-stu-id="68a27-113">The following functions are used by OPM to access functionality in the display driver.</span></span> <span data-ttu-id="68a27-114">Les applications ne doivent pas appeler ces fonctions.</span><span class="sxs-lookup"><span data-stu-id="68a27-114">Applications should not call these functions.</span></span>

-   [<span data-ttu-id="68a27-115">**ConfigureOPMProtectedOutput**</span><span class="sxs-lookup"><span data-stu-id="68a27-115">**ConfigureOPMProtectedOutput**</span></span>](configureopmprotectedoutput.md)
-   [<span data-ttu-id="68a27-116">**CreateOPMProtectedOutputs**</span><span class="sxs-lookup"><span data-stu-id="68a27-116">**CreateOPMProtectedOutputs**</span></span>](createopmprotectedoutputs.md)
-   [<span data-ttu-id="68a27-117">**DestroyOPMProtectedOutput**</span><span class="sxs-lookup"><span data-stu-id="68a27-117">**DestroyOPMProtectedOutput**</span></span>](destroyopmprotectedoutput.md)
-   [<span data-ttu-id="68a27-118">**GetCertificate**</span><span class="sxs-lookup"><span data-stu-id="68a27-118">**GetCertificate**</span></span>](/windows/desktop/api/d3d9/nf-d3d9-idirect3dauthenticatedchannel9-getcertificate)
-   [<span data-ttu-id="68a27-119">**GetCertificateSize**</span><span class="sxs-lookup"><span data-stu-id="68a27-119">**GetCertificateSize**</span></span>](/windows/desktop/api/d3d9/nf-d3d9-idirect3dauthenticatedchannel9-getcertificatesize)
-   [<span data-ttu-id="68a27-120">**GetCOPPCompatibleOPMInformation**</span><span class="sxs-lookup"><span data-stu-id="68a27-120">**GetCOPPCompatibleOPMInformation**</span></span>](getcoppcompatibleopminformation.md)
-   [<span data-ttu-id="68a27-121">**GetOPMInformation**</span><span class="sxs-lookup"><span data-stu-id="68a27-121">**GetOPMInformation**</span></span>](getopminformation.md)
-   [<span data-ttu-id="68a27-122">**GetOPMRandomNumber**</span><span class="sxs-lookup"><span data-stu-id="68a27-122">**GetOPMRandomNumber**</span></span>](getopmrandomnumber.md)
-   [<span data-ttu-id="68a27-123">**GetSuggestedOPMProtectedOutputArraySize**</span><span class="sxs-lookup"><span data-stu-id="68a27-123">**GetSuggestedOPMProtectedOutputArraySize**</span></span>](getsuggestedopmprotectedoutputarraysize.md)
-   [<span data-ttu-id="68a27-124">**SetOPMSigningKeyAndSequenceNumbers**</span><span class="sxs-lookup"><span data-stu-id="68a27-124">**SetOPMSigningKeyAndSequenceNumbers**</span></span>](setopmsigningkeyandsequencenumbers.md)

## <a name="related-topics"></a><span data-ttu-id="68a27-125">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="68a27-125">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="68a27-126">Informations de référence sur la programmation OPM</span><span class="sxs-lookup"><span data-stu-id="68a27-126">OPM Programming Reference</span></span>](opm-programming-reference.md)
</dt> <dt>

[<span data-ttu-id="68a27-127">Gestionnaire de protection de sortie</span><span class="sxs-lookup"><span data-stu-id="68a27-127">Output Protection Manager</span></span>](output-protection-manager.md)
</dt> </dl>

 

 



