---
title: Extensions d’appareil pour le transfert de métadonnées accéléré
description: Extensions d’appareil pour le transfert de métadonnées accéléré
ms.assetid: a79b54d4-dad5-411b-aaff-b58bb549d4d1
keywords:
- Windows Media Player, extensions d’appareils
- Windows Media Player, extensions
- Windows Media Player, transfert de métadonnées accéléré
- Lecteur Windows Media, transfert des métadonnées accéléré
- transfert de métadonnées accéléré
- métadonnées, transfert accéléré
- extensions d’appareils, transfert de métadonnées accéléré
- extensions, transfert de métadonnées accéléré
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cbe661dff0750f2ad46bef96e537b0852d480db8
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104029461"
---
# <a name="device-extensions-for-accelerated-metadata-transfer"></a><span data-ttu-id="e217a-111">Extensions d’appareil pour le transfert de métadonnées accéléré</span><span class="sxs-lookup"><span data-stu-id="e217a-111">Device Extensions for Accelerated Metadata Transfer</span></span>

<span data-ttu-id="e217a-112">Le lecteur Windows Media 10 a introduit de nouvelles fonctionnalités étendues pour la synchronisation des fichiers multimédias numériques avec des appareils portables.</span><span class="sxs-lookup"><span data-stu-id="e217a-112">Windows Media Player 10 introduced new and extended functionality for synchronizing digital media files with portable devices.</span></span> <span data-ttu-id="e217a-113">Les utilisateurs peuvent connecter un appareil à un ordinateur, transférer du contenu à l’appareil, puis déconnecter l’appareil pour profiter du contenu de l’ordinateur.</span><span class="sxs-lookup"><span data-stu-id="e217a-113">Users can connect a device to a computer, transfer content to the device, and then disconnect the device to enjoy content away from the computer.</span></span>

<span data-ttu-id="e217a-114">Lorsque l’utilisateur reconnecte l’appareil à l’ordinateur, il est possible que le contenu stocké sur l’appareil ait été modifié depuis la connexion précédente.</span><span class="sxs-lookup"><span data-stu-id="e217a-114">When the user reconnects the device to the computer, it is possible that the content stored on the device changed since the previous connection.</span></span> <span data-ttu-id="e217a-115">Par exemple, le simple fait de lire un fichier multimédia numérique particulier entraîne la modification du nombre de lecture pour cet élément.</span><span class="sxs-lookup"><span data-stu-id="e217a-115">For example, simply playing a particular digital media file causes the play count for that item to change.</span></span> <span data-ttu-id="e217a-116">Étant donné que les appareils mobiles actuels peuvent stocker de grandes quantités de contenu multimédia numérique, le processus de découverte des modifications serait trop long si le lecteur Windows Media devait énumérer et inspecter chaque élément multimédia numérique.</span><span class="sxs-lookup"><span data-stu-id="e217a-116">Because current portable devices can store large quantities of digital media content, the process of discovering changes would be too time consuming if Windows Media Player were required to enumerate and inspect each digital media item.</span></span> <span data-ttu-id="e217a-117">Au lieu de cela, les fabricants d’appareils mobiles peuvent implémenter des fonctionnalités spéciales pour permettre au lecteur Windows Media 10 ou version ultérieure de récupérer efficacement des informations sur les modifications apportées au contenu stocké sur un appareil.</span><span class="sxs-lookup"><span data-stu-id="e217a-117">Instead, portable device manufacturers can implement special functionality to enable Windows Media Player 10 or later to efficiently retrieve information about changes made to the content stored on a device.</span></span>

<span data-ttu-id="e217a-118">Les sections suivantes décrivent les conventions utilisées pour implémenter cette fonctionnalité.</span><span class="sxs-lookup"><span data-stu-id="e217a-118">The following sections describe the conventions used to implement this functionality.</span></span>

-   [<span data-ttu-id="e217a-119">À propos des métadonnées</span><span class="sxs-lookup"><span data-stu-id="e217a-119">About the Metadata</span></span>](about-the-metadata.md)
-   [<span data-ttu-id="e217a-120">Extensions d’appareil MTP pour le transfert de métadonnées</span><span class="sxs-lookup"><span data-stu-id="e217a-120">MTP Device Extensions for Metadata Transfer</span></span>](mtp-device-extensions-for-metadata-transfer.md)
-   [<span data-ttu-id="e217a-121">Extensions d’appareils Windows Media Gestionnaire de périphériques pour le transfert de métadonnées</span><span class="sxs-lookup"><span data-stu-id="e217a-121">Windows Media Device Manager Device Extensions for Metadata Transfer</span></span>](windows-media-device-manager-device-extensions-for-metadata-transfer.md)

## <a name="related-topics"></a><span data-ttu-id="e217a-122">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="e217a-122">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="e217a-123">**Lecteur Windows Media**</span><span class="sxs-lookup"><span data-stu-id="e217a-123">**Windows Media Player**</span></span>](windows-media-player.md)
</dt> </dl>

 

 




