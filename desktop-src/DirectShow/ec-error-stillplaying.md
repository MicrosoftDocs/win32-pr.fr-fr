---
description: Une commande asynchrone pour exécuter le graphique a échoué.
ms.assetid: 0bfcf4b4-b35a-4593-9956-8e1e8c9139cb
title: EC_ERROR_STILLPLAYING (DShow. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1d1c99db8c6b332ad4531f04171d960c5cfa9824
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106540183"
---
# <a name="ec_error_stillplaying"></a><span data-ttu-id="85333-103">\_erreur EC \_ STILLPLAYING</span><span class="sxs-lookup"><span data-stu-id="85333-103">EC\_ERROR\_STILLPLAYING</span></span>

<span data-ttu-id="85333-104">Une commande asynchrone pour exécuter le graphique a échoué.</span><span class="sxs-lookup"><span data-stu-id="85333-104">An asynchronous command to run the graph has failed.</span></span>

## <a name="parameters"></a><span data-ttu-id="85333-105">Paramètres</span><span class="sxs-lookup"><span data-stu-id="85333-105">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="85333-106"><span id="lParam1"></span><span id="lparam1"></span><span id="LPARAM1"></span>*lParam1*</span><span class="sxs-lookup"><span data-stu-id="85333-106"><span id="lParam1"></span><span id="lparam1"></span><span id="LPARAM1"></span>*lParam1*</span></span>
</dt> <dd>

<span data-ttu-id="85333-107">(**HRESULT**) Code d’échec de l’opération qui a échoué.</span><span class="sxs-lookup"><span data-stu-id="85333-107">(**HRESULT**) Failure code of the operation that failed.</span></span>

</dd> <dt>

<span data-ttu-id="85333-108"><span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*</span><span class="sxs-lookup"><span data-stu-id="85333-108"><span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*</span></span>
</dt> <dd>

<span data-ttu-id="85333-109">Zéro.</span><span class="sxs-lookup"><span data-stu-id="85333-109">Zero.</span></span>

</dd> </dl>

## <a name="default-action"></a><span data-ttu-id="85333-110">Action par défaut</span><span class="sxs-lookup"><span data-stu-id="85333-110">Default Action</span></span>

<span data-ttu-id="85333-111">Aucun.</span><span class="sxs-lookup"><span data-stu-id="85333-111">None.</span></span>

## <a name="remarks"></a><span data-ttu-id="85333-112">Notes</span><span class="sxs-lookup"><span data-stu-id="85333-112">Remarks</span></span>

<span data-ttu-id="85333-113">Si le gestionnaire de graphes de filtres émet une commande d’exécution asynchrone qui échoue, il envoie cet événement à l’application.</span><span class="sxs-lookup"><span data-stu-id="85333-113">If the filter graph manager issues an asynchronous run command that fails, it sends this event to the application.</span></span> <span data-ttu-id="85333-114">Le graphique reste à l’État en cours d’exécution.</span><span class="sxs-lookup"><span data-stu-id="85333-114">The graph remains in a running state.</span></span> <span data-ttu-id="85333-115">L’état des filtres sous-jacents est indéterminé.</span><span class="sxs-lookup"><span data-stu-id="85333-115">The state of the underlying filters is indeterminate.</span></span> <span data-ttu-id="85333-116">Certains filtres sont peut-être en cours d’exécution, d’autres non.</span><span class="sxs-lookup"><span data-stu-id="85333-116">Some filters might be running, others might not.</span></span>

## <a name="requirements"></a><span data-ttu-id="85333-117">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="85333-117">Requirements</span></span>



| <span data-ttu-id="85333-118">Condition requise</span><span class="sxs-lookup"><span data-stu-id="85333-118">Requirement</span></span> | <span data-ttu-id="85333-119">Valeur</span><span class="sxs-lookup"><span data-stu-id="85333-119">Value</span></span> |
|-------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="85333-120">En-tête</span><span class="sxs-lookup"><span data-stu-id="85333-120">Header</span></span><br/> | <dl> <span data-ttu-id="85333-121"><dt>DShow. h</dt></span><span class="sxs-lookup"><span data-stu-id="85333-121"><dt>Dshow.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="85333-122">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="85333-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="85333-123">Codes de notification d’événement</span><span class="sxs-lookup"><span data-stu-id="85333-123">Event Notification Codes</span></span>](event-notification-codes.md)
</dt> <dt>

[<span data-ttu-id="85333-124">Notification d’événement dans DirectShow</span><span class="sxs-lookup"><span data-stu-id="85333-124">Event Notification in DirectShow</span></span>](event-notification-in-directshow.md)
</dt> </dl>

 

 




