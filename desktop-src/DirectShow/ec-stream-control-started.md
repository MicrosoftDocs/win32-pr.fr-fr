---
description: Une commande de démarrage de flux de contrôle a pris effet.
ms.assetid: e2f8d9a2-c96c-457c-8a88-7c86d4405928
title: EC_STREAM_CONTROL_STARTED (DShow. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 984562fde9001de14067e5865d5583636b264852
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106530450"
---
# <a name="ec_stream_control_started"></a><span data-ttu-id="0a4ea-103">\_le contrôle de flux EC \_ \_ a démarré</span><span class="sxs-lookup"><span data-stu-id="0a4ea-103">EC\_STREAM\_CONTROL\_STARTED</span></span>

<span data-ttu-id="0a4ea-104">Une commande de démarrage de flux de contrôle a pris effet.</span><span class="sxs-lookup"><span data-stu-id="0a4ea-104">A stream-control start command has taken effect.</span></span>

## <a name="parameters"></a><span data-ttu-id="0a4ea-105">Paramètres</span><span class="sxs-lookup"><span data-stu-id="0a4ea-105">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0a4ea-106"><span id="pSender"></span><span id="psender"></span><span id="PSENDER"></span>*pSender*</span><span class="sxs-lookup"><span data-stu-id="0a4ea-106"><span id="pSender"></span><span id="psender"></span><span id="PSENDER"></span>*pSender*</span></span>
</dt> <dd>

<span data-ttu-id="0a4ea-107">(**IUnknown** \* ) Pointeur vers l’interface [**IPIN**](/windows/desktop/api/Strmif/nn-strmif-ipin) du code confidentiel qui a démarré le flux.</span><span class="sxs-lookup"><span data-stu-id="0a4ea-107">(**IUnknown**\*) Pointer to the [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin) interface of the pin that started the stream.</span></span>

</dd> <dt>

<span data-ttu-id="0a4ea-108"><span id="dwCookie"></span><span id="dwcookie"></span><span id="DWCOOKIE"></span>*dwCookie*</span><span class="sxs-lookup"><span data-stu-id="0a4ea-108"><span id="dwCookie"></span><span id="dwcookie"></span><span id="DWCOOKIE"></span>*dwCookie*</span></span>
</dt> <dd>

<span data-ttu-id="0a4ea-109">(**DWORD**) Valeur définie par l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="0a4ea-109">(**DWORD**) User-defined value.</span></span>

</dd> </dl>

## <a name="default-action"></a><span data-ttu-id="0a4ea-110">Action par défaut</span><span class="sxs-lookup"><span data-stu-id="0a4ea-110">Default Action</span></span>

<span data-ttu-id="0a4ea-111">Aucun.</span><span class="sxs-lookup"><span data-stu-id="0a4ea-111">None.</span></span>

## <a name="remarks"></a><span data-ttu-id="0a4ea-112">Notes</span><span class="sxs-lookup"><span data-stu-id="0a4ea-112">Remarks</span></span>

<span data-ttu-id="0a4ea-113">Les filtres envoient cet événement en réponse à la méthode [**IAMStreamControl :: startat**](/windows/desktop/api/Strmif/nf-strmif-iamstreamcontrol-startat) .</span><span class="sxs-lookup"><span data-stu-id="0a4ea-113">Filters send this event in response to the [**IAMStreamControl::StartAt**](/windows/desktop/api/Strmif/nf-strmif-iamstreamcontrol-startat) method.</span></span> <span data-ttu-id="0a4ea-114">Cette méthode spécifie une durée de référence pour le début de la diffusion en continu d’un code confidentiel.</span><span class="sxs-lookup"><span data-stu-id="0a4ea-114">This method specifies a reference time for a pin to begin streaming.</span></span> <span data-ttu-id="0a4ea-115">Lorsque la diffusion en continu commence, le filtre envoie cet événement.</span><span class="sxs-lookup"><span data-stu-id="0a4ea-115">When streaming does begin, the filter sends this event.</span></span>

<span data-ttu-id="0a4ea-116">Le paramètre *pSender* spécifie le code confidentiel qui exécute la commande de démarrage.</span><span class="sxs-lookup"><span data-stu-id="0a4ea-116">The *pSender* parameter specifies the pin that executes the start command.</span></span> <span data-ttu-id="0a4ea-117">En fonction de l’implémentation, il est possible qu’il ne s’agit pas du code confidentiel qui a reçu l’appel [**startat**](/windows/desktop/api/Strmif/nf-strmif-iamstreamcontrol-startat) .</span><span class="sxs-lookup"><span data-stu-id="0a4ea-117">Depending on the implementation, it might not be the pin that received the [**StartAt**](/windows/desktop/api/Strmif/nf-strmif-iamstreamcontrol-startat) call.</span></span>

<span data-ttu-id="0a4ea-118">Le paramètre *dwCookie* est spécifié par l’application dans la méthode [**startat**](/windows/desktop/api/Strmif/nf-strmif-iamstreamcontrol-startat) .</span><span class="sxs-lookup"><span data-stu-id="0a4ea-118">The *dwCookie* parameter is specified by the application in the [**StartAt**](/windows/desktop/api/Strmif/nf-strmif-iamstreamcontrol-startat) method.</span></span> <span data-ttu-id="0a4ea-119">Ce paramètre permet à l’application d’effectuer le suivi de plusieurs appels à la méthode.</span><span class="sxs-lookup"><span data-stu-id="0a4ea-119">This parameter enables the application to track multiple calls to the method.</span></span>

## <a name="requirements"></a><span data-ttu-id="0a4ea-120">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="0a4ea-120">Requirements</span></span>



| <span data-ttu-id="0a4ea-121">Condition requise</span><span class="sxs-lookup"><span data-stu-id="0a4ea-121">Requirement</span></span> | <span data-ttu-id="0a4ea-122">Valeur</span><span class="sxs-lookup"><span data-stu-id="0a4ea-122">Value</span></span> |
|-------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="0a4ea-123">En-tête</span><span class="sxs-lookup"><span data-stu-id="0a4ea-123">Header</span></span><br/> | <dl> <span data-ttu-id="0a4ea-124"><dt>DShow. h</dt></span><span class="sxs-lookup"><span data-stu-id="0a4ea-124"><dt>Dshow.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0a4ea-125">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="0a4ea-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0a4ea-126">Codes de notification d’événement</span><span class="sxs-lookup"><span data-stu-id="0a4ea-126">Event Notification Codes</span></span>](event-notification-codes.md)
</dt> <dt>

[<span data-ttu-id="0a4ea-127">Notification d’événement dans DirectShow</span><span class="sxs-lookup"><span data-stu-id="0a4ea-127">Event Notification in DirectShow</span></span>](event-notification-in-directshow.md)
</dt> </dl>

 

 




