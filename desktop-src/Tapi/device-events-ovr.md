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
# <a name="device-events-telephony-api"></a>Événements d’appareil (API de téléphonie)

L’interface TAPI répond aux modifications de l’appareil, telles qu’un téléphone qui a démarré la sonnerie ou un modem qui a été supprimé en déclenchant des événements d’appareil. Une application TAPI doit répondre à un événement d’appareil en interrogeant les modifications spécifiques qui se sont produites, puis en prenant les mesures appropriées. Une application peut s’afficher pour les événements qu’elle recevra à l’aide de la [notification d’événement](event-notification.md).

**TAPI 2. x :** Les applications reçoivent une notification des événements de l’appareil à l’aide du message [**\_ LINEDEVSTATE de ligne**](./line-linedevstate.md) . L’état actuel d’une adresse est déterminé par l’appel de [**lineGetAddressStatus**](/windows/win32/api/tapi/nf-tapi-linegetaddressstatus), qui retourne ses informations dans une structure [**LINEADDRESSSTATUS**](/windows/win32/api/tapi/ns-tapi-lineaddressstatus) . L’état d’un périphérique Open Line spécifié est obtenu en appelant [**lineGetLineDevStatus**](/windows/win32/api/tapi/nf-tapi-linegetlinedevstatus), qui retourne ses informations dans une structure [**LINEDEVSTATUS**](/windows/win32/api/tapi/ns-tapi-linedevstatus) .

**TAPI 3. x :** Les applications reçoivent une notification d' [**\_ événement d’adresse**](/windows/desktop/api/Tapi3if/ne-tapi3if-address_event) , qui est traitée à l’aide de l’interface [**ITAddressEvent**](/windows/desktop/api/tapi3if/nn-tapi3if-itaddressevent) . Le [**ITAddressCapabilities**](/windows/desktop/api/tapi3if/nn-tapi3if-itaddresscapabilities) peut ensuite être utilisé pour obtenir plus d’informations détaillées.

 

 
