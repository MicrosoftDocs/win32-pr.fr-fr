---
description: Le type de média (ou mode) d’un appareil décrit le type d’informations qui peuvent être échangées, par exemple la voix interactive. Un appareil donné peut être en mesure de gérer un seul type de média, ou il peut être en mesure de traiter une plage de types.
ms.assetid: fccf85e9-3889-4ebc-b1bf-a60e27ab4586
title: Type de support
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 369954a4b0d1f78e12f6ea42bcc2ec61ca425012
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/03/2021
ms.locfileid: "106522276"
---
# <a name="media-type"></a><span data-ttu-id="c8059-104">Type de support</span><span class="sxs-lookup"><span data-stu-id="c8059-104">Media Type</span></span>

<span data-ttu-id="c8059-105">Le *type de média* (ou mode) d’un appareil décrit le type d’informations qui peuvent être échangées, par exemple la voix interactive.</span><span class="sxs-lookup"><span data-stu-id="c8059-105">The *media type* (or mode) of a device describes the type of information that can be exchanged, such as interactive voice.</span></span> <span data-ttu-id="c8059-106">Un appareil donné peut être en mesure de gérer un seul type de média, ou il peut être en mesure de traiter une plage de types.</span><span class="sxs-lookup"><span data-stu-id="c8059-106">A given device might be able to handle only one media type, or it might be able to deal with a range of types.</span></span>

<span data-ttu-id="c8059-107">Les fournisseurs de services exposent le type de média ou les types pris en charge par les périphériques qu’ils contrôlent.</span><span class="sxs-lookup"><span data-stu-id="c8059-107">Service providers expose the media type or types supported by the devices they control.</span></span> <span data-ttu-id="c8059-108">Les applications interrogent le type de média, puis utilisent ces informations pour sélectionner une adresse appropriée sur laquelle lancer une session.</span><span class="sxs-lookup"><span data-stu-id="c8059-108">Applications query for media type and then use this information to select an appropriate address on which to initiate a session.</span></span> <span data-ttu-id="c8059-109">La réponse d’application à une session proposée peut également être prédicat sur le type de média.</span><span class="sxs-lookup"><span data-stu-id="c8059-109">Application response to a session offered may also be predicated on media type.</span></span>

<span data-ttu-id="c8059-110">Une session de communication donnée, ou appel, peut impliquer plusieurs types de média.</span><span class="sxs-lookup"><span data-stu-id="c8059-110">A given communications session, or call, can involve several media types.</span></span> <span data-ttu-id="c8059-111">Pour plus d’informations, consultez type de média pour une session.</span><span class="sxs-lookup"><span data-stu-id="c8059-111">For further information, see Media type for a session.</span></span>

<span data-ttu-id="c8059-112">**TAPI 2. x :** Consultez [**lineGetAddressCaps**](/windows/win32/api/tapi/nf-tapi-linegetaddresscaps), **dwAvailableMediaModes** , membre de la structure [**LINEADDRESSCAPS**](/windows/win32/api/tapi/ns-tapi-lineaddresscaps) pointée par *lpAddressCaps*, [ \_ constantes LINEMEDIAMODE](./linemediamode--constants.md).</span><span class="sxs-lookup"><span data-stu-id="c8059-112">**TAPI 2.x:** See [**lineGetAddressCaps**](/windows/win32/api/tapi/nf-tapi-linegetaddresscaps), **dwAvailableMediaModes** member of [**LINEADDRESSCAPS**](/windows/win32/api/tapi/ns-tapi-lineaddresscaps) structure pointed to by *lpAddressCaps*, [LINEMEDIAMODE\_ Constants](./linemediamode--constants.md).</span></span>

<span data-ttu-id="c8059-113">**TAPI 3. x :** Consultez [**ITTerminal :: obtenir \_ MediaType**](/windows/win32/api/tapi3if/nf-tapi3if-itterminal-get_mediatype), [ \_ constantes TAPIMEDIATYPE](tapimediatype--constants.md).</span><span class="sxs-lookup"><span data-stu-id="c8059-113">**TAPI 3.x:** See [**ITTerminal::get\_MediaType**](/windows/win32/api/tapi3if/nf-tapi3if-itterminal-get_mediatype), [TAPIMEDIATYPE\_ Constants](tapimediatype--constants.md).</span></span>
