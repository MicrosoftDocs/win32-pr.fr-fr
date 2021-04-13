---
description: Un ID d’appareil est un identificateur indépendant de l’application pour un appareil de communication spécifique.
ms.assetid: c7ca72a6-97fa-441f-92ce-a4c77a53765c
title: Identificateur de l’appareil
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7aeb9c88820ecfe26d3ecd971489d709a34af10f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104529079"
---
# <a name="device-identifier"></a><span data-ttu-id="81aee-103">Identificateur de l’appareil</span><span class="sxs-lookup"><span data-stu-id="81aee-103">Device Identifier</span></span>

<span data-ttu-id="81aee-104">Un *ID d’appareil* est un identificateur indépendant de l’application pour un appareil de communication spécifique.</span><span class="sxs-lookup"><span data-stu-id="81aee-104">A *device ID* is an application-independent identifier for a specific communications device.</span></span> <span data-ttu-id="81aee-105">Elle est généralement nécessaire uniquement lorsqu’une application TAPI doit transférer une partie du traitement impliquant dans une session de communication vers les fonctions d’une autre API.</span><span class="sxs-lookup"><span data-stu-id="81aee-105">It is typically needed only when a TAPI application needs to hand off part of the processing involving in a communications session to the functions of a different API.</span></span> <span data-ttu-id="81aee-106">Par exemple, les applications TAPI 2,2 peuvent ne pas être en mesure d’accéder directement à un flux multimédia et peuvent utiliser l’API Wave.</span><span class="sxs-lookup"><span data-stu-id="81aee-106">For example, TAPI 2.2 applications may be unable to directly access a media stream and might use the Wave API.</span></span>

<span data-ttu-id="81aee-107">**TAPI 2. x :** Consultez [**lineGetID**](/windows/win32/api/tapi/nf-tapi-linegetid).</span><span class="sxs-lookup"><span data-stu-id="81aee-107">**TAPI 2.x:** See [**lineGetID**](/windows/win32/api/tapi/nf-tapi-linegetid).</span></span>

<span data-ttu-id="81aee-108">**TAPI 3. x :** Consultez [**ITAddressCapabilities :: obtenir \_ AddressCapability**](/windows/desktop/api/tapi3if/nf-tapi3if-itaddresscapabilities-get_addresscapability) (*AddressCap* défini sur le membre **AC \_ PERMANENTDEVICEID** de [**la \_ fonctionnalité d’adresse**](/windows/desktop/api/Tapi3if/ne-tapi3if-address_capability)).</span><span class="sxs-lookup"><span data-stu-id="81aee-108">**TAPI 3.x:** See [**ITAddressCapabilities::get\_AddressCapability**](/windows/desktop/api/tapi3if/nf-tapi3if-itaddresscapabilities-get_addresscapability) (*AddressCap* set to the **AC\_PERMANENTDEVICEID** member of [**ADDRESS\_CAPABILITY**](/windows/desktop/api/Tapi3if/ne-tapi3if-address_capability)).</span></span>

 

 
