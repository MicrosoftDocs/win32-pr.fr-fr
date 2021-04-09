---
description: Utilisation des effets et des transitions
ms.assetid: 00e97d02-ff43-4e1f-9806-abaeb9288058
title: Utilisation des effets et des transitions
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 99029269ac86e17246fd641341b071654582bc4a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103953184"
---
# <a name="working-with-effects-and-transitions"></a><span data-ttu-id="b2250-103">Utilisation des effets et des transitions</span><span class="sxs-lookup"><span data-stu-id="b2250-103">Working with Effects and Transitions</span></span>

<span data-ttu-id="b2250-104">\[Cette API n’est pas prise en charge et peut être modifiée ou non disponible à l’avenir.\]</span><span class="sxs-lookup"><span data-stu-id="b2250-104">\[This API is not supported and may be altered or unavailable in the future.\]</span></span>

<span data-ttu-id="b2250-105">Les effets modifient une seule séquence, piste ou composition.</span><span class="sxs-lookup"><span data-stu-id="b2250-105">Effects modify a single clip, track, or composition.</span></span> <span data-ttu-id="b2250-106">Les transitions créent des seques à partir d’une piste ou d’un compositionsto.</span><span class="sxs-lookup"><span data-stu-id="b2250-106">Transitions create seques from one track or compositionsto another.</span></span>

<span data-ttu-id="b2250-107">Les [services d’édition DirectShow](directshow-editing-services.md) utilisent des objets de transformation DirectX pour ses transitions vidéo et leurs effets vidéo.</span><span class="sxs-lookup"><span data-stu-id="b2250-107">[DirectShow Editing Services](directshow-editing-services.md) uses DirectX Transform objects for its video transitions and video effects.</span></span> <span data-ttu-id="b2250-108">Pour les transitions vidéo, utilisez n’importe quel objet de transformation DirectX à deux entrées 2D.</span><span class="sxs-lookup"><span data-stu-id="b2250-108">For video transitions, use any 2-D two-input DirectX Transform object.</span></span> <span data-ttu-id="b2250-109">Pour les effets vidéo, utilisez n’importe quel objet de transformation DirectX à un entrée en 2D.</span><span class="sxs-lookup"><span data-stu-id="b2250-109">For video effects, use any 2-D one-input DirectX Transform object.</span></span> <span data-ttu-id="b2250-110">Microsoft ne prend plus en charge le développement d’objets de transformation DirectX tiers.</span><span class="sxs-lookup"><span data-stu-id="b2250-110">Microsoft no longer supports the development of third-party DirectX Transform objects.</span></span> <span data-ttu-id="b2250-111">Toutefois, plusieurs sont fournis avec DirectShow et d’autres sont fournis avec Microsoft Internet Explorer.</span><span class="sxs-lookup"><span data-stu-id="b2250-111">However, several are provided with DirectShow and others are provided with Microsoft Internet Explorer.</span></span> <span data-ttu-id="b2250-112">Pour plus d’informations sur les transitions fournies avec Internet Explorer, consultez informations de référence sur les [filtres visuels et les transitions](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/ms532853(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="b2250-112">For more information about the transitions provided with Internet Explorer, see [Visual Filters and Transitions Reference](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/ms532853(v=vs.85)).</span></span>

<span data-ttu-id="b2250-113">Pour les effets audio, vous pouvez utiliser n’importe quel filtre d’effet audio DirectShow.</span><span class="sxs-lookup"><span data-stu-id="b2250-113">For audio effects, you can use any DirectShow audio effect filter.</span></span> <span data-ttu-id="b2250-114">DES fournit également un [effet d’enveloppe de volume](volume-envelope-effect.md) pour la définition du volume sur une piste ou un clip.</span><span class="sxs-lookup"><span data-stu-id="b2250-114">DES also provides a [Volume Envelope Effect](volume-envelope-effect.md) for setting the volume on a track or clip.</span></span> <span data-ttu-id="b2250-115">DES ne prend pas en charge les transitions audio.</span><span class="sxs-lookup"><span data-stu-id="b2250-115">DES does not support audio transitions.</span></span>

<span data-ttu-id="b2250-116">Cette section contient les rubriques suivantes :</span><span class="sxs-lookup"><span data-stu-id="b2250-116">This section contains the following topics:</span></span>

-   [<span data-ttu-id="b2250-117">Ajout d’objets Effect et transition</span><span class="sxs-lookup"><span data-stu-id="b2250-117">Adding Effect and Transition Objects</span></span>](adding-effect-and-transition-objects.md)
-   [<span data-ttu-id="b2250-118">Aperçu des effets et des transitions</span><span class="sxs-lookup"><span data-stu-id="b2250-118">Previewing Effects and Transitions</span></span>](previewing-effects-and-transitions.md)
-   [<span data-ttu-id="b2250-119">Énumération des effets et des transitions</span><span class="sxs-lookup"><span data-stu-id="b2250-119">Enumerating Effects and Transitions</span></span>](enumerating-effects-and-transitions.md)
-   [<span data-ttu-id="b2250-120">Définition des propriétés des effets et des transitions</span><span class="sxs-lookup"><span data-stu-id="b2250-120">Setting Properties on Effects and Transitions</span></span>](setting-properties-on-effects-and-transitions.md)
-   [<span data-ttu-id="b2250-121">Sens de la transition</span><span class="sxs-lookup"><span data-stu-id="b2250-121">Transition Direction</span></span>](transition-direction.md)

## <a name="related-topics"></a><span data-ttu-id="b2250-122">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="b2250-122">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="b2250-123">Utilisation des services de modification DirectShow</span><span class="sxs-lookup"><span data-stu-id="b2250-123">Using DirectShow Editing Services</span></span>](using-directshow-editing-services.md)
</dt> </dl>

 

 
