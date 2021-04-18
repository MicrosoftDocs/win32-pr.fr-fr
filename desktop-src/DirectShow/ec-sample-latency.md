---
description: Spécifie la distance de planification d’un composant pour les exemples de traitement.
ms.assetid: 8bd202fb-3015-41a2-ad14-862f64cb252f
title: EC_SAMPLE_LATENCY (DShow. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ee90d42e6464eccc4bc93b1052e29392b74bb2d7
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106543036"
---
# <a name="ec_sample_latency"></a><span data-ttu-id="794e1-103">latence de l' \_ exemple EC \_</span><span class="sxs-lookup"><span data-stu-id="794e1-103">EC\_SAMPLE\_LATENCY</span></span>

<span data-ttu-id="794e1-104">Spécifie la distance de planification d’un composant pour les exemples de traitement.</span><span class="sxs-lookup"><span data-stu-id="794e1-104">Specifies how far behind schedule a component is for processing samples.</span></span>

## <a name="parameters"></a><span data-ttu-id="794e1-105">Paramètres</span><span class="sxs-lookup"><span data-stu-id="794e1-105">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="794e1-106"><span id="lParam1"></span><span id="lparam1"></span><span id="LPARAM1"></span>*lParam1*</span><span class="sxs-lookup"><span data-stu-id="794e1-106"><span id="lParam1"></span><span id="lparam1"></span><span id="LPARAM1"></span>*lParam1*</span></span>
</dt> <dd>

<span data-ttu-id="794e1-107">(**const Reference \_ Time** \* ) à l’arrière-plan du composant, en unités de 100 nanosecondes.</span><span class="sxs-lookup"><span data-stu-id="794e1-107">(**const REFERENCE\_TIME**\*) How far behind the component is, in 100-nanosecond units.</span></span> <span data-ttu-id="794e1-108">Si cette valeur est positive, le composant est en arrière-plan.</span><span class="sxs-lookup"><span data-stu-id="794e1-108">If this value is positive, the component is behind schedule.</span></span> <span data-ttu-id="794e1-109">Si cette valeur est négative, le composant est en avance sur Schedule.</span><span class="sxs-lookup"><span data-stu-id="794e1-109">If this value is negative, the component is ahead of schedule.</span></span>

</dd> <dt>

<span data-ttu-id="794e1-110"><span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*</span><span class="sxs-lookup"><span data-stu-id="794e1-110"><span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*</span></span>
</dt> <dd>

<span data-ttu-id="794e1-111">Zéro.</span><span class="sxs-lookup"><span data-stu-id="794e1-111">Zero.</span></span>

</dd> </dl>

## <a name="default-action"></a><span data-ttu-id="794e1-112">Action par défaut</span><span class="sxs-lookup"><span data-stu-id="794e1-112">Default Action</span></span>

<span data-ttu-id="794e1-113">Aucun.</span><span class="sxs-lookup"><span data-stu-id="794e1-113">None.</span></span>

## <a name="remarks"></a><span data-ttu-id="794e1-114">Notes</span><span class="sxs-lookup"><span data-stu-id="794e1-114">Remarks</span></span>

<span data-ttu-id="794e1-115">Un présentateur personnalisé pour le filtre EVR ( [**Enhanced Video Renderer**](enhanced-video-renderer-filter.md) ) peut envoyer ce message à EVR, pour informer le EVR si le présenteur est en retard ou en avance sur la planification.</span><span class="sxs-lookup"><span data-stu-id="794e1-115">A custom presenter for the [**Enhanced Video Renderer**](enhanced-video-renderer-filter.md) (EVR) filter can send this message to the EVR, to notify the EVR whether the presenter is behind schedule or ahead of schedule.</span></span>

<span data-ttu-id="794e1-116">La façon la plus simple de calculer *lParam1* est la suivante : *QPC maintenant*   *QPC Target*, où *QPC* est désormais l’heure de l’horloge, et *QPC Target* est l’heure de la présentation.</span><span class="sxs-lookup"><span data-stu-id="794e1-116">The simplest way to calculate *lParam1* is: *QPC now*   *QPC target*, where *QPC now* is the clock time now, and *QPC target* is the presentation time.</span></span>

## <a name="requirements"></a><span data-ttu-id="794e1-117">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="794e1-117">Requirements</span></span>



| <span data-ttu-id="794e1-118">Condition requise</span><span class="sxs-lookup"><span data-stu-id="794e1-118">Requirement</span></span> | <span data-ttu-id="794e1-119">Valeur</span><span class="sxs-lookup"><span data-stu-id="794e1-119">Value</span></span> |
|-------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="794e1-120">En-tête</span><span class="sxs-lookup"><span data-stu-id="794e1-120">Header</span></span><br/> | <dl> <span data-ttu-id="794e1-121"><dt>DShow. h</dt></span><span class="sxs-lookup"><span data-stu-id="794e1-121"><dt>Dshow.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="794e1-122">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="794e1-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="794e1-123">Codes de notification d’événement</span><span class="sxs-lookup"><span data-stu-id="794e1-123">Event Notification Codes</span></span>](event-notification-codes.md)
</dt> <dt>

[<span data-ttu-id="794e1-124">Comment écrire un présentateur EVR</span><span class="sxs-lookup"><span data-stu-id="794e1-124">How to Write an EVR Presenter</span></span>](/windows/desktop/medfound/how-to-write-an-evr-presenter)
</dt> </dl>

 

