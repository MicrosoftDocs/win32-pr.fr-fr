---
description: Quand une nouvelle session de communication arrive, les applications TAPI qui ont inscrit un intérêt pour l’adresse et le type de média reçoivent une notification d’événement.
ms.assetid: 6074619c-6aa0-4b03-9208-10268682e704
title: Répondre à une session lancée ailleurs
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 85e25651b58f8841ac4de9bf14f4d139161c1359
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106529499"
---
# <a name="respond-to-session-initiated-elsewhere"></a><span data-ttu-id="bf1a8-103">Répondre à une session lancée ailleurs</span><span class="sxs-lookup"><span data-stu-id="bf1a8-103">Respond to Session Initiated Elsewhere</span></span>

<span data-ttu-id="bf1a8-104">Quand une nouvelle session de communication arrive, les applications TAPI qui ont inscrit un intérêt pour l' [adresse](address-ovr.md) et le [type de média](media-type-ovr.md) reçoivent une [notification d’événement](event-notification.md).</span><span class="sxs-lookup"><span data-stu-id="bf1a8-104">When a new communications session arrives, TAPI applications that registered an interest in the [address](address-ovr.md) and [media type](media-type-ovr.md) will be sent an [event notification](event-notification.md).</span></span> <span data-ttu-id="bf1a8-105">Une seule application recevra [des privilèges](privilege-ovr.md) de propriété sur la session.</span><span class="sxs-lookup"><span data-stu-id="bf1a8-105">Only one application will be offered ownership [privileges](privilege-ovr.md) over the session.</span></span> <span data-ttu-id="bf1a8-106">Cette application ne peut pas refuser la session.</span><span class="sxs-lookup"><span data-stu-id="bf1a8-106">This application cannot refuse the session.</span></span>

<span data-ttu-id="bf1a8-107">L’état d’appel initial d’une session entrante offre.</span><span class="sxs-lookup"><span data-stu-id="bf1a8-107">The initial call state of an incoming session is offering.</span></span> <span data-ttu-id="bf1a8-108">Lorsque l’appel est dans l’état d’offre, une application peut obtenir des informations telles que le mode de support et la raison de l’appel, si les fournisseurs de services ont fourni ces informations et qu’elles sont disponibles.</span><span class="sxs-lookup"><span data-stu-id="bf1a8-108">While the call is in the offering state, an application can obtain information such as bearer mode and call reason, if the service providers supplied this information and it is available.</span></span> <span data-ttu-id="bf1a8-109">Certaines informations sur les appels peuvent ne pas être disponibles immédiatement, telles que l’ID de l’appelant.</span><span class="sxs-lookup"><span data-stu-id="bf1a8-109">Some call information may not be available immediately, such as caller ID.</span></span>

<span data-ttu-id="bf1a8-110">Il existe six réponses de base à une session proposée : [réponse](answer-ovr.md), [acceptation](accept-ovr.md), [remise](handoffs-ovr.md), [supprimer](drop-ovr.md), [transférer](forward-ovr.md)et [Rediriger](redirect-ovr.md).</span><span class="sxs-lookup"><span data-stu-id="bf1a8-110">There are six basic responses to an offered session: [answer](answer-ovr.md), [accept](accept-ovr.md), [handoff](handoffs-ovr.md), [drop](drop-ovr.md), [forward](forward-ovr.md), and [redirect](redirect-ovr.md).</span></span> <span data-ttu-id="bf1a8-111">En fonction du fournisseur de services, l’ensemble complet de ces opérations peut ne pas être disponible.</span><span class="sxs-lookup"><span data-stu-id="bf1a8-111">Depending on the service provider, the full set of these operations may not be available.</span></span>

 

 



