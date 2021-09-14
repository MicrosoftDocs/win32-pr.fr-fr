---
title: Réception de trafic non sollicité sur Teredo
description: Teredo offre une connectivité globale à l’aide des fonctionnalités de traversée IPv6 et NAT.
ms.assetid: 0c03d1bb-15f8-4e77-9a96-e182b1d190ac
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8a5c7ffe7b84cfa325b3ecd8c0858ad96445e629
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127193456"
---
# <a name="receiving-unsolicited-traffic-over-teredo"></a>Réception de trafic non sollicité sur Teredo

[Teredo](about-teredo.md) offre une connectivité globale à l’aide des fonctionnalités de traversée IPv6 et NAT. Toutefois, de nombreuses applications, y compris pair à pair, requièrent Teredo pour recevoir le trafic non sollicité d’Internet. Une application peut être programmée pour recevoir le trafic via une interface IPv6 unique ou toutes les interfaces compatibles IPv6. Cette documentation décrit la configuration requise pour les applications qui utilisent l’interface Teredo pour recevoir le trafic IPv6 non sollicité.

une application recevra le trafic non sollicité sur l’interface Teredo uniquement si l’application est inscrite auprès d' [Windows pare-feu](/previous-versions/windows/desktop/ics/windows-firewall-start-page). Pour recevoir du trafic non sollicité, les conditions suivantes doivent être remplies :

-   Les utilisateurs doivent être invités à utiliser la console MMC (Microsoft Management Console) pour activer l’option « traversée latérale » pour une application. cette option est disponible sous Windows pare-feu Snap-In--> <application name> --> onglet « avancé ». L’option « traversée latérale » doit être activée individuellement pour chaque application.

-   L’option « traversée latérale » est activée par l’application. il est possible pour les applications qui peuvent recevoir du trafic non sollicité de s’inscrire auprès d’Windows pare-feu pour « traversée latérale » et de recevoir le trafic non sollicité sur l’interface Teredo. Pour ce faire, une application doit appeler l’API [**INetFwPolicy2**](/previous-versions/windows/desktop/api/netfw/nn-netfw-inetfwpolicy2) avec l’option « traversée latérale » définie sur variant \_ true. Le consentement de l’utilisateur est requis pour cet appel d’API avant qu’une application soit autorisée à écouter le trafic.

-   L’application définit l’option de socket de [ \_ \_ niveau de protection IPv6 IPv6](/windows/desktop/WinSock/ipv6-protection-level) sur le **niveau de protection non \_ \_ restreint** via [**setsockopt**](/windows/desktop/api/winsock/nf-winsock-setsockopt). Cela permettra à l’application de recevoir le trafic de traversée latérale.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Réception du trafic sollicité sur Teredo](receiving-solicited-traffic-over-teredo.md)
</dt> </dl>

 

 