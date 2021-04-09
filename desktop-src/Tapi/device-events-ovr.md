---
description: L’interface TAPI répond aux modifications de l’appareil, telles qu’un téléphone qui a démarré la sonnerie ou un modem qui a été supprimé en déclenchant des événements d’appareil.
ms.assetid: afa504ca-6e70-4076-a179-31002d3b38e2
title: Événements d’appareil (API de téléphonie)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 47f5508e74424a13117facc1c4c370144ecd46de
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103751628"
---
# <a name="device-events-telephony-api"></a><span data-ttu-id="c8257-103">Événements d’appareil (API de téléphonie)</span><span class="sxs-lookup"><span data-stu-id="c8257-103">Device Events (Telephony API)</span></span>

<span data-ttu-id="c8257-104">L’interface TAPI répond aux modifications de l’appareil, telles qu’un téléphone qui a démarré la sonnerie ou un modem qui a été supprimé en déclenchant des événements d’appareil.</span><span class="sxs-lookup"><span data-stu-id="c8257-104">TAPI responds to device changes such as a phone that has started ringing or a modem that has been removed by firing device events.</span></span> <span data-ttu-id="c8257-105">Une application TAPI doit répondre à un événement d’appareil en interrogeant les modifications spécifiques qui se sont produites, puis en prenant les mesures appropriées.</span><span class="sxs-lookup"><span data-stu-id="c8257-105">A TAPI application should respond to a device event by querying for the specific change that has occurred and then taking appropriate action.</span></span> <span data-ttu-id="c8257-106">Une application peut s’afficher pour les événements qu’elle recevra à l’aide de la [notification d’événement](event-notification.md).</span><span class="sxs-lookup"><span data-stu-id="c8257-106">An application may screen for events it will receive using [event notification](event-notification.md).</span></span>

<span data-ttu-id="c8257-107">**TAPI 2. x :** Les applications reçoivent une notification des événements de l’appareil à l’aide du message [**\_ LINEDEVSTATE de ligne**](./line-linedevstate.md) .</span><span class="sxs-lookup"><span data-stu-id="c8257-107">**TAPI 2.x:** Applications receive notification of device events using the [**LINE\_LINEDEVSTATE**](./line-linedevstate.md) message.</span></span> <span data-ttu-id="c8257-108">L’état actuel d’une adresse est déterminé par l’appel de [**lineGetAddressStatus**](/windows/win32/api/tapi/nf-tapi-linegetaddressstatus), qui retourne ses informations dans une structure [**LINEADDRESSSTATUS**](/windows/win32/api/tapi/ns-tapi-lineaddressstatus) .</span><span class="sxs-lookup"><span data-stu-id="c8257-108">The current status of an address is determined by calling [**lineGetAddressStatus**](/windows/win32/api/tapi/nf-tapi-linegetaddressstatus), which returns its information in a [**LINEADDRESSSTATUS**](/windows/win32/api/tapi/ns-tapi-lineaddressstatus) structure.</span></span> <span data-ttu-id="c8257-109">L’état d’un périphérique Open Line spécifié est obtenu en appelant [**lineGetLineDevStatus**](/windows/win32/api/tapi/nf-tapi-linegetlinedevstatus), qui retourne ses informations dans une structure [**LINEDEVSTATUS**](/windows/win32/api/tapi/ns-tapi-linedevstatus) .</span><span class="sxs-lookup"><span data-stu-id="c8257-109">The status of a specified open line device is obtained by calling [**lineGetLineDevStatus**](/windows/win32/api/tapi/nf-tapi-linegetlinedevstatus), which returns its information in a [**LINEDEVSTATUS**](/windows/win32/api/tapi/ns-tapi-linedevstatus) structure.</span></span>

<span data-ttu-id="c8257-110">**TAPI 3. x :** Les applications reçoivent une notification d' [**\_ événement d’adresse**](/windows/desktop/api/Tapi3if/ne-tapi3if-address_event) , qui est traitée à l’aide de l’interface [**ITAddressEvent**](/windows/desktop/api/tapi3if/nn-tapi3if-itaddressevent) .</span><span class="sxs-lookup"><span data-stu-id="c8257-110">**TAPI 3.x:** Applications receive an [**ADDRESS\_EVENT**](/windows/desktop/api/Tapi3if/ne-tapi3if-address_event) notification, which is processed using the [**ITAddressEvent**](/windows/desktop/api/tapi3if/nn-tapi3if-itaddressevent) interface.</span></span> <span data-ttu-id="c8257-111">Le [**ITAddressCapabilities**](/windows/desktop/api/tapi3if/nn-tapi3if-itaddresscapabilities) peut ensuite être utilisé pour obtenir plus d’informations détaillées.</span><span class="sxs-lookup"><span data-stu-id="c8257-111">The [**ITAddressCapabilities**](/windows/desktop/api/tapi3if/nn-tapi3if-itaddresscapabilities) can then be used to acquire more detail information.</span></span>

 

 
