---
description: Le graphique de filtre s’arrête, avant d’être détruit.
ms.assetid: f1b3fc87-16ec-485b-b659-fc7d975c4a22
title: EC_SHUTTING_DOWN (DShow. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 471b746df3980afd96bbfc122a164ccd30561846
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106523983"
---
# <a name="ec_shutting_down"></a><span data-ttu-id="ab3d7-103">arrêt de l’EC \_ \_</span><span class="sxs-lookup"><span data-stu-id="ab3d7-103">EC\_SHUTTING\_DOWN</span></span>

<span data-ttu-id="ab3d7-104">Le graphique de filtre s’arrête, avant d’être détruit.</span><span class="sxs-lookup"><span data-stu-id="ab3d7-104">The filter graph is shutting down, prior to being destroyed.</span></span>

## <a name="parameters"></a><span data-ttu-id="ab3d7-105">Paramètres</span><span class="sxs-lookup"><span data-stu-id="ab3d7-105">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ab3d7-106"><span id="lParam1"></span><span id="lparam1"></span><span id="LPARAM1"></span>*lParam1*</span><span class="sxs-lookup"><span data-stu-id="ab3d7-106"><span id="lParam1"></span><span id="lparam1"></span><span id="LPARAM1"></span>*lParam1*</span></span>
</dt> <dd>

<span data-ttu-id="ab3d7-107">Zéro.</span><span class="sxs-lookup"><span data-stu-id="ab3d7-107">Zero.</span></span>

</dd> <dt>

<span data-ttu-id="ab3d7-108"><span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*</span><span class="sxs-lookup"><span data-stu-id="ab3d7-108"><span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*</span></span>
</dt> <dd>

<span data-ttu-id="ab3d7-109">Zéro.</span><span class="sxs-lookup"><span data-stu-id="ab3d7-109">Zero.</span></span>

</dd> </dl>

## <a name="default-action"></a><span data-ttu-id="ab3d7-110">Action par défaut</span><span class="sxs-lookup"><span data-stu-id="ab3d7-110">Default Action</span></span>

<span data-ttu-id="ab3d7-111">Cet événement n’est pas envoyé à l’application.</span><span class="sxs-lookup"><span data-stu-id="ab3d7-111">This event is not sent to the application.</span></span> <span data-ttu-id="ab3d7-112">Le gestionnaire de graphes de filtres l’envoie aux serveurs de distribution de plug-in pour les informer que le graphique est en cours d’arrêt.</span><span class="sxs-lookup"><span data-stu-id="ab3d7-112">The filter graph manager sends it to plug-in distributors, to notify them that the graph is shutting down.</span></span> <span data-ttu-id="ab3d7-113">Les applications ne peuvent pas remplacer l’action par défaut de cet événement.</span><span class="sxs-lookup"><span data-stu-id="ab3d7-113">Applications cannot override the default action of this event.</span></span>

## <a name="requirements"></a><span data-ttu-id="ab3d7-114">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="ab3d7-114">Requirements</span></span>



| <span data-ttu-id="ab3d7-115">Condition requise</span><span class="sxs-lookup"><span data-stu-id="ab3d7-115">Requirement</span></span> | <span data-ttu-id="ab3d7-116">Valeur</span><span class="sxs-lookup"><span data-stu-id="ab3d7-116">Value</span></span> |
|-------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="ab3d7-117">En-tête</span><span class="sxs-lookup"><span data-stu-id="ab3d7-117">Header</span></span><br/> | <dl> <span data-ttu-id="ab3d7-118"><dt>DShow. h</dt></span><span class="sxs-lookup"><span data-stu-id="ab3d7-118"><dt>Dshow.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ab3d7-119">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="ab3d7-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ab3d7-120">Codes de notification d’événement</span><span class="sxs-lookup"><span data-stu-id="ab3d7-120">Event Notification Codes</span></span>](event-notification-codes.md)
</dt> <dt>

[<span data-ttu-id="ab3d7-121">Notification d’événement dans DirectShow</span><span class="sxs-lookup"><span data-stu-id="ab3d7-121">Event Notification in DirectShow</span></span>](event-notification-in-directshow.md)
</dt> </dl>

 

 




