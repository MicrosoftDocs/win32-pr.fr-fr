---
title: Implémentation de Teredo
ms.assetid: f32e908e-a96d-48a2-8b79-e2e53c64cb68
description: 'En savoir plus sur : implémentation de Teredo'
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7ffdf2859d3742bea02e240c6a26bd0e4ade85ac
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104210574"
---
# <a name="implementing-teredo"></a>Implémentation de Teredo

Bien qu’il ne soit pas nécessaire d’apporter des modifications de programmation pour [Teredo](about-teredo.md), il est recommandé que les développeurs apportent des modifications mineures qui se traduisent par l’utilisation la plus efficace de l’interface Teredo :

-   Il est possible pour les applications qui ne peuvent être que le trafic IPv6 d’utiliser Teredo. Toutefois, le traitement du trafic IPv4 et IPv6 doit être pris en considération lors du développement du protocole d’application. L’application doit être liée à AF \_ inet6 ou AF \_ unspec dans les options de Socket.
-   Les applications qui peuvent écouter le trafic non sollicité à partir d’Internet sont requises pour activer l’option de traversée de traduction d’adresses réseau (NAT) à l’intérieur du pare-feu Windows. Pour ce faire, appelez l’API [**INetFwPolicy2**](/previous-versions/windows/desktop/api/netfw/nn-netfw-inetfwpolicy2) avec l’option « traversée latérale » définie sur variant \_ true. Windows Vista garantit que l’adresse Teredo peut être utilisée lorsqu’une application l’exige. Par conséquent, l’adresse Teredo se stabilise automatiquement lorsque l’interface Teredo est utilisée. Si une application veut s’assurer que l’adresse Teredo est stable, l’appel de l’API [**NotifyStableUnicastIpAddressTable**](/windows/desktop/api/netioapi/nf-netioapi-notifystableunicastipaddresstable) déclenche la transition de Teredo vers un état stable.
-   Les applications peuvent également utiliser l’option de socket Winsock du [ \_ \_ niveau de protection IPv6](/windows/desktop/WinSock/ipv6-protection-level) pour définir le niveau de protection, ce qui permet au trafic entrant non sollicité de traverser le pare-feu. Pour plus d’informations, consultez [réception de trafic non sollicité sur Teredo](receiving-unsolicited-traffic-over-teredo.md) .

L’implémentation du programme d’assistance IP (IP Helper) des fonctions Teredo spécifiques sert à illustrer comment l’adresse Teredo peut être vérifiée et mise à la disposition d’une application. Pour plus d’informations, consultez [utilisation de Teredo avec l’assistance IP](using-teredo-with-ip-helper.md).

 

 
