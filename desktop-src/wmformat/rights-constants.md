---
title: Constantes de droits
description: Constantes de droits
ms.assetid: fb20dc57-25da-4613-a324-e081ba87df73
keywords:
- Windows Media Format SDK, constantes
- gestion des droits numériques (DRM), constantes
- DRM (gestion des droits numériques), constantes
- API étendues du client DRM, constantes
- API étendues clientes, constantes
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b1349da53b63b1b7df59c13e0e69f7fdbf47ee3f
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104100781"
---
# <a name="rights-constants"></a><span data-ttu-id="27b0f-108">Constantes de droits</span><span class="sxs-lookup"><span data-stu-id="27b0f-108">Rights Constants</span></span>

<span data-ttu-id="27b0f-109">Les constantes répertoriées dans le tableau suivant sont utilisées pour identifier les actions DRM et pour créer des listes d’actions.</span><span class="sxs-lookup"><span data-stu-id="27b0f-109">The constants listed in the following table are used to identify DRM actions and to build lists of actions.</span></span>



| <span data-ttu-id="27b0f-110">Constante</span><span class="sxs-lookup"><span data-stu-id="27b0f-110">Constant</span></span>                                        | <span data-ttu-id="27b0f-111">Description</span><span class="sxs-lookup"><span data-stu-id="27b0f-111">Description</span></span>                                                                                                                                                                                                                                                    |
|-------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="27b0f-112">g \_ wszWMDRM \_ ActionList \_</span><span class="sxs-lookup"><span data-stu-id="27b0f-112">g\_wszWMDRM\_ACTIONLIST\_TAG</span></span>                    | <span data-ttu-id="27b0f-113">Définit le nom d’élément XML pour une liste d’actions.</span><span class="sxs-lookup"><span data-stu-id="27b0f-113">Defines the XML element name for an action list.</span></span>                                                                                                                                                                                                               |
| <span data-ttu-id="27b0f-114">g \_ ( \_ balise d’action wszWMDRM) \_</span><span class="sxs-lookup"><span data-stu-id="27b0f-114">g\_wszWMDRM\_ACTION\_TAG</span></span>                        | <span data-ttu-id="27b0f-115">Définit le nom d’élément XML pour une entrée dans une liste d’actions.</span><span class="sxs-lookup"><span data-stu-id="27b0f-115">Defines the XML element name for an entry in an action list.</span></span>                                                                                                                                                                                                   |
| <span data-ttu-id="27b0f-116">\_ \_ lecture droite g \_ wszWMDRM</span><span class="sxs-lookup"><span data-stu-id="27b0f-116">g\_wszWMDRM\_RIGHT\_PLAYBACK</span></span>                    | <span data-ttu-id="27b0f-117">Définit la chaîne pour le droit de lire le contenu.</span><span class="sxs-lookup"><span data-stu-id="27b0f-117">Defines the string for the right to play content.</span></span>                                                                                                                                                                                                              |
| <span data-ttu-id="27b0f-118">\_wszWMDRM g \_ droit de \_ copie</span><span class="sxs-lookup"><span data-stu-id="27b0f-118">g\_wszWMDRM\_RIGHT\_COPY</span></span>                        | <span data-ttu-id="27b0f-119">Définit la chaîne du droit de copie du contenu.</span><span class="sxs-lookup"><span data-stu-id="27b0f-119">Defines the string for the right to copy content.</span></span>                                                                                                                                                                                                              |
| <span data-ttu-id="27b0f-120">wszWMDRM de la \_ \_ sélection à droite \_ \_ g</span><span class="sxs-lookup"><span data-stu-id="27b0f-120">g\_wszWMDRM\_RIGHT\_PLAYLIST\_BURN</span></span>              | <span data-ttu-id="27b0f-121">Définit la chaîne pour le droit de graver du contenu sur CD dans le cadre d’une sélection.</span><span class="sxs-lookup"><span data-stu-id="27b0f-121">Defines the string for the right to burn content to CD as part of a playlist.</span></span>                                                                                                                                                                                  |
| <span data-ttu-id="27b0f-122">wszWMDRM g de \_ \_ droite \_ créer une \_ \_ image miniature</span><span class="sxs-lookup"><span data-stu-id="27b0f-122">g\_wszWMDRM\_RIGHT\_CREATE\_THUMBNAIL\_IMAGE</span></span>    | <span data-ttu-id="27b0f-123">Définit la chaîne de droite pour créer une image miniature à partir du contenu vidéo.</span><span class="sxs-lookup"><span data-stu-id="27b0f-123">Defines the string for the right to create a thumbnail image from video content.</span></span>                                                                                                                                                                               |
| <span data-ttu-id="27b0f-124">\_wszWMDRM g \_ droit \_ \_ de copie sur le \_ CD</span><span class="sxs-lookup"><span data-stu-id="27b0f-124">g\_wszWMDRM\_RIGHT\_COPY\_TO\_CD</span></span>                | <span data-ttu-id="27b0f-125">Définit la chaîne pour le droit de copier le contenu sur un CD.</span><span class="sxs-lookup"><span data-stu-id="27b0f-125">Defines the string for the right to copy content to a CD.</span></span> <span data-ttu-id="27b0f-126">Les nouvelles licences ne doivent pas utiliser ce droit.</span><span class="sxs-lookup"><span data-stu-id="27b0f-126">New licenses should not use this right.</span></span> <span data-ttu-id="27b0f-127">Au lieu de cela, tous les droits accordant l’autorisation de copier du contenu doivent être couverts par le droit de copie et le droit de gravure de sélection.</span><span class="sxs-lookup"><span data-stu-id="27b0f-127">Instead, all rights granting permission to copy content should be covered by the copy right and the playlist burn right.</span></span>                                     |
| <span data-ttu-id="27b0f-128">g \_ wszWMDRM \_ droit \_ \_ de copie sur l' \_ \_ appareil SDMI</span><span class="sxs-lookup"><span data-stu-id="27b0f-128">g\_wszWMDRM\_RIGHT\_COPY\_TO\_SDMI\_DEVICE</span></span>      | <span data-ttu-id="27b0f-129">Définit la chaîne pour le droit de copier le contenu sur un appareil qui est conforme à l’initiative de musique numérique sécurisée (SDMI).</span><span class="sxs-lookup"><span data-stu-id="27b0f-129">Defines the string for the right to copy content to a device that conforms to the Secure Digital Music Initiative (SDMI).</span></span> <span data-ttu-id="27b0f-130">Les nouvelles licences ne doivent pas utiliser ce droit.</span><span class="sxs-lookup"><span data-stu-id="27b0f-130">New licenses should not use this right.</span></span> <span data-ttu-id="27b0f-131">Au lieu de cela, tous les droits accordant l’autorisation de copier du contenu doivent être couverts par le droit copier.</span><span class="sxs-lookup"><span data-stu-id="27b0f-131">Instead, all rights granting permission to copy content should be covered by the copy right.</span></span> |
| <span data-ttu-id="27b0f-132">g \_ wszWMDRM \_ droit \_ \_ de copie sur un \_ \_ appareil non SDMI \_</span><span class="sxs-lookup"><span data-stu-id="27b0f-132">g\_wszWMDRM\_RIGHT\_COPY\_TO\_NON\_SDMI\_DEVICE</span></span> | <span data-ttu-id="27b0f-133">Définit la chaîne du droit à copier sur un appareil qui n’est pas conforme à l’initiative de musique numérique sécurisée (SDMI).</span><span class="sxs-lookup"><span data-stu-id="27b0f-133">Defines the string for the right to copy to a device that does not conform to the Secure Digital Music Initiative (SDMI).</span></span> <span data-ttu-id="27b0f-134">Les nouvelles licences ne doivent pas utiliser ce droit.</span><span class="sxs-lookup"><span data-stu-id="27b0f-134">New licenses should not use this right.</span></span> <span data-ttu-id="27b0f-135">Au lieu de cela, tous les droits accordant l’autorisation de copier du contenu doivent être couverts par le droit copier.</span><span class="sxs-lookup"><span data-stu-id="27b0f-135">Instead, all rights granting permission to copy content should be covered by the copy right.</span></span> |
| <span data-ttu-id="27b0f-136">\_wszWMDRM la \_ sauvegarde à droite g \_</span><span class="sxs-lookup"><span data-stu-id="27b0f-136">g\_wszWMDRM\_RIGHT\_BACKUP</span></span>                      | <span data-ttu-id="27b0f-137">Définit la chaîne pour le droit de sauvegarder la licence.</span><span class="sxs-lookup"><span data-stu-id="27b0f-137">Defines the string for the right to backup the license.</span></span>                                                                                                                                                                                                        |
| <span data-ttu-id="27b0f-138">wszWMDRM de la \_ \_ bonne \_ \_ lecture collaborative</span><span class="sxs-lookup"><span data-stu-id="27b0f-138">g\_wszWMDRM\_RIGHT\_COLLABORATIVE\_PLAY</span></span>         | <span data-ttu-id="27b0f-139">Définit la chaîne pour le droit de lire le contenu sur un réseau dans le cadre d’une sélection partagée.</span><span class="sxs-lookup"><span data-stu-id="27b0f-139">Defines the string for the right to play content over a network as part of a shared playlist.</span></span>                                                                                                                                                                  |



 

## <a name="related-topics"></a><span data-ttu-id="27b0f-140">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="27b0f-140">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="27b0f-141">**Constantes**</span><span class="sxs-lookup"><span data-stu-id="27b0f-141">**Constants**</span></span>](constants.md)
</dt> </dl>

 

 




