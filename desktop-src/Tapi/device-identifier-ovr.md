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
# <a name="device-identifier"></a>Identificateur de l’appareil

Un *ID d’appareil* est un identificateur indépendant de l’application pour un appareil de communication spécifique. Elle est généralement nécessaire uniquement lorsqu’une application TAPI doit transférer une partie du traitement impliquant dans une session de communication vers les fonctions d’une autre API. Par exemple, les applications TAPI 2,2 peuvent ne pas être en mesure d’accéder directement à un flux multimédia et peuvent utiliser l’API Wave.

**TAPI 2. x :** Consultez [**lineGetID**](/windows/win32/api/tapi/nf-tapi-linegetid).

**TAPI 3. x :** Consultez [**ITAddressCapabilities :: obtenir \_ AddressCapability**](/windows/desktop/api/tapi3if/nf-tapi3if-itaddresscapabilities-get_addresscapability) (*AddressCap* défini sur le membre **AC \_ PERMANENTDEVICEID** de [**la \_ fonctionnalité d’adresse**](/windows/desktop/api/Tapi3if/ne-tapi3if-address_capability)).

 

 
