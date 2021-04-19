---
description: Envoyé par le filtre de l’enregistreur ASF WM lorsqu’il termine le prétraitement pour l’encodage multipasse.
ms.assetid: 2029afc4-419c-494a-ae52-1f84b08bcb35
title: EC_PREPROCESS_COMPLETE (DShow. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ba13938ac848ef37f1a2a2826372d97ff5a5d716
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106539495"
---
# <a name="ec_preprocess_complete"></a><span data-ttu-id="1320a-103">\_prétraitement EC \_ terminé</span><span class="sxs-lookup"><span data-stu-id="1320a-103">EC\_PREPROCESS\_COMPLETE</span></span>

<span data-ttu-id="1320a-104">Envoyé par le filtre de l' [enregistreur ASF WM](wm-asf-writer-filter.md) lorsqu’il termine le prétraitement pour l’encodage multipasse.</span><span class="sxs-lookup"><span data-stu-id="1320a-104">Sent by the [WM ASF Writer](wm-asf-writer-filter.md) filter when it completes the pre-processing for multipass encoding.</span></span>

## <a name="parameters"></a><span data-ttu-id="1320a-105">Paramètres</span><span class="sxs-lookup"><span data-stu-id="1320a-105">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1320a-106"><span id="lParam1"></span><span id="lparam1"></span><span id="LPARAM1"></span>*lParam1*</span><span class="sxs-lookup"><span data-stu-id="1320a-106"><span id="lParam1"></span><span id="lparam1"></span><span id="LPARAM1"></span>*lParam1*</span></span>
</dt> <dd>

<span data-ttu-id="1320a-107">Zéro.</span><span class="sxs-lookup"><span data-stu-id="1320a-107">Zero.</span></span>

</dd> <dt>

<span data-ttu-id="1320a-108"><span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*</span><span class="sxs-lookup"><span data-stu-id="1320a-108"><span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*</span></span>
</dt> <dd>

<span data-ttu-id="1320a-109">(**IUnknown** \* ) Pointeur vers l’interface [**IBaseFilter**](/windows/desktop/api/Strmif/nn-strmif-ibasefilter) du filtre.</span><span class="sxs-lookup"><span data-stu-id="1320a-109">(**IUnknown**\*) Pointer to the [**IBaseFilter**](/windows/desktop/api/Strmif/nn-strmif-ibasefilter) interface of the filter.</span></span>

</dd> </dl>

## <a name="default-action"></a><span data-ttu-id="1320a-110">Action par défaut</span><span class="sxs-lookup"><span data-stu-id="1320a-110">Default Action</span></span>

<span data-ttu-id="1320a-111">Aucun</span><span class="sxs-lookup"><span data-stu-id="1320a-111">None.</span></span>

## <a name="requirements"></a><span data-ttu-id="1320a-112">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="1320a-112">Requirements</span></span>



| <span data-ttu-id="1320a-113">Condition requise</span><span class="sxs-lookup"><span data-stu-id="1320a-113">Requirement</span></span> | <span data-ttu-id="1320a-114">Valeur</span><span class="sxs-lookup"><span data-stu-id="1320a-114">Value</span></span> |
|-------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="1320a-115">En-tête</span><span class="sxs-lookup"><span data-stu-id="1320a-115">Header</span></span><br/> | <dl> <span data-ttu-id="1320a-116"><dt>DShow. h</dt></span><span class="sxs-lookup"><span data-stu-id="1320a-116"><dt>Dshow.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1320a-117">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="1320a-117">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1320a-118">Codes de notification d’événement</span><span class="sxs-lookup"><span data-stu-id="1320a-118">Event Notification Codes</span></span>](event-notification-codes.md)
</dt> <dt>

[<span data-ttu-id="1320a-119">Notification d’événement dans DirectShow</span><span class="sxs-lookup"><span data-stu-id="1320a-119">Event Notification in DirectShow</span></span>](event-notification-in-directshow.md)
</dt> </dl>

 

 




