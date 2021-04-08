---
description: Mode de lecture non rendu VMR (Allocator personnalisé-présentateur)
ms.assetid: 0381f862-2f16-4b4d-be48-40f7fe151585
title: Mode de lecture non rendu VMR (Allocator personnalisé-présentateur)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3ad9cd4dcb5e5b2f1965d49c7f31b4ef8c9ebd78
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103757666"
---
# <a name="vmr-renderless-playback-mode-custom-allocator-presenters"></a><span data-ttu-id="ba190-103">Mode de lecture non rendu VMR (Allocator personnalisé-présentateur)</span><span class="sxs-lookup"><span data-stu-id="ba190-103">VMR Renderless Playback Mode (Custom Allocator-Presenters)</span></span>

<span data-ttu-id="ba190-104">En mode de lecture sans rendu, VMR n’effectue pas le rendu.</span><span class="sxs-lookup"><span data-stu-id="ba190-104">In renderless playback mode, the VMR does not perform the rendering.</span></span> <span data-ttu-id="ba190-105">Au lieu de cela, il utilise un allocateur-présentateur personnalisé fourni par l’application.</span><span class="sxs-lookup"><span data-stu-id="ba190-105">Instead, it uses a custom allocator-presenter supplied by the application.</span></span> <span data-ttu-id="ba190-106">Ce mode est utile pour les jeux et les autres types d’applications qui ont des effets vidéo sophistiqués.</span><span class="sxs-lookup"><span data-stu-id="ba190-106">This mode is useful for games and other types of applications that have sophisticated video effects.</span></span> <span data-ttu-id="ba190-107">Le mode de lecture non rendu permet aux applications de créer et contrôler sa propre surface DirectDraw (VMR-7) ou la surface Direct3D (VMR-9) et d’accéder aux bits vidéo au moment de la présentation.</span><span class="sxs-lookup"><span data-stu-id="ba190-107">Renderless playback mode enables the applications to create and control its own DirectDraw surface (VMR-7) or Direct3D surface (VMR-9), and to access the video bits at presentation time.</span></span>

<span data-ttu-id="ba190-108">En mode sans rendu, VMR-9 ne charge pas automatiquement son composant mixer.</span><span class="sxs-lookup"><span data-stu-id="ba190-108">In renderless mode, the VMR-9 does not automatically load its mixer component.</span></span>

<span data-ttu-id="ba190-109">En mode de lecture sans rendu, l’application effectue les tâches suivantes :</span><span class="sxs-lookup"><span data-stu-id="ba190-109">In renderless playback mode, the application does the following tasks:</span></span>

-   <span data-ttu-id="ba190-110">Gère la fenêtre de lecture.</span><span class="sxs-lookup"><span data-stu-id="ba190-110">Manages the playback window.</span></span>
-   <span data-ttu-id="ba190-111">Alloue l’objet DirectDraw ou Direct3D et la mémoire tampon de frame finale.</span><span class="sxs-lookup"><span data-stu-id="ba190-111">Allocates the DirectDraw or Direct3D object and the final frame buffer.</span></span>
-   <span data-ttu-id="ba190-112">Notifie le reste du système de lecture de l’objet utilisé.</span><span class="sxs-lookup"><span data-stu-id="ba190-112">Notifies the rest of the playback system of the object being used.</span></span>
-   <span data-ttu-id="ba190-113">Affiche la mémoire tampon de frame à l’heure correcte.</span><span class="sxs-lookup"><span data-stu-id="ba190-113">Presents the frame buffer at the correct time.</span></span>
-   <span data-ttu-id="ba190-114">Gère toutes les modifications du mode de résolution, surveille les modifications et les pertes de surface.</span><span class="sxs-lookup"><span data-stu-id="ba190-114">Handles all resolution-mode changes, monitor changes, and surface losses.</span></span> <span data-ttu-id="ba190-115">Il doit informer le reste du système de lecture de ces événements.</span><span class="sxs-lookup"><span data-stu-id="ba190-115">It must advise the rest of the playback system of these events.</span></span>

<span data-ttu-id="ba190-116">VMR effectue les opérations suivantes :</span><span class="sxs-lookup"><span data-stu-id="ba190-116">The VMR does the following:</span></span>

-   <span data-ttu-id="ba190-117">Gère tout le minutage lié à la présentation de l’image vidéo.</span><span class="sxs-lookup"><span data-stu-id="ba190-117">Handles all timing related to presenting the video frame.</span></span>
-   <span data-ttu-id="ba190-118">Fournit des informations de contrôle qualité à l’application et au reste du système de lecture.</span><span class="sxs-lookup"><span data-stu-id="ba190-118">Provides quality-control information to the application and the rest of the playback system.</span></span>
-   <span data-ttu-id="ba190-119">Présente une interface cohérente aux composants en amont du système de lecture, qui ne savent pas que l’application fournit l’allocation de mémoire tampon de trame et effectue le rendu.</span><span class="sxs-lookup"><span data-stu-id="ba190-119">Presents a consistent interface to the upstream components of the playback system, which are not aware that the application is providing the frame buffer allocation and performing the rendering.</span></span>
-   <span data-ttu-id="ba190-120">Fournit toute combinaison de flux vidéo qui peut être nécessaire avant le rendu.</span><span class="sxs-lookup"><span data-stu-id="ba190-120">Provides any mixing of video streams that may be required prior to rendering.</span></span>

<span data-ttu-id="ba190-121">Étant donné que l’opération de désentrelacement est effectuée par le mélangeur, l’allocateur-presenter a toujours reçu des frames désentrelacés.</span><span class="sxs-lookup"><span data-stu-id="ba190-121">Because deinterlacing is performed by the mixer, the allocator-presenter always received deinterlaced frames.</span></span> <span data-ttu-id="ba190-122">Pour plus d’informations, consultez [définition des préférences de désentrelacement](setting-deinterlace-preferences.md).</span><span class="sxs-lookup"><span data-stu-id="ba190-122">For more information, see [Setting Deinterlace Preferences](setting-deinterlace-preferences.md).</span></span>

<span data-ttu-id="ba190-123">Pour plus d’informations sur la fourniture d’un Allocator-Presenter personnalisé, consultez les rubriques suivantes :</span><span class="sxs-lookup"><span data-stu-id="ba190-123">For more information about providing a custom allocator-presenter, see the following topics:</span></span>

-   [<span data-ttu-id="ba190-124">Fourniture d’un Allocator-Presenter personnalisé pour VMR-7</span><span class="sxs-lookup"><span data-stu-id="ba190-124">Supplying a Custom Allocator-Presenter for VMR-7</span></span>](supplying-a-custom-allocator-presenter-for-vmr-7.md)
-   [<span data-ttu-id="ba190-125">Fourniture d’un Allocator-Presenter personnalisé pour VMR-9</span><span class="sxs-lookup"><span data-stu-id="ba190-125">Supplying a Custom Allocator-Presenter for VMR-9</span></span>](supplying-a-custom-allocator-presenter-for-vmr-9.md)
-   [<span data-ttu-id="ba190-126">Synchronisation de VMR avec la fréquence d’actualisation du moniteur</span><span class="sxs-lookup"><span data-stu-id="ba190-126">Synchronizing the VMR to the Monitor's Refresh Rate</span></span>](synchronizing-the-vmr-to-the-monitors-refresh-rate.md)

 

 



