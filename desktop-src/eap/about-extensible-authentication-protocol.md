---
title: À propos d’EAP
description: Le protocole EAP (Extensible Authentication Protocol), un standard pris en charge par de nombreux composants de mise en réseau Microsoft.
ms.assetid: a2f41808-4316-431a-ab58-f1e25d3c61f6
keywords:
- Protocole EAP (Extensible Authentication Protocol), décrit
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 84866f7f550213850bf95c39a6f0847df31bed3550db66139f2ec30bf921b5a6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118276042"
---
# <a name="about-eap"></a>À propos d’EAP

Cette rubrique décrit le protocole EAP (Extensible Authentication Protocol), un standard pris en charge par de nombreux composants de mise en réseau Microsoft.

## <a name="eap-components"></a>Composants EAP

EAP est essentiel pour la protection de la sécurité des réseaux locaux (LAN) sans fil (802.1 X), des réseaux locaux câblés et des réseaux privés virtuels (VPN) et d’accès à distance.

Les composants suivants prennent en charge le protocole EAP.

-   Les clients et les serveurs d’accès à distance Microsoft pour l’accès à distance et VPN (PPTP et L2TP/IPSec) implémentent EAP en tant qu’extension de PPP. Pour plus d’informations, consultez la [RFC 3748](https://go.microsoft.com/fwlink/p/?linkid=84063).
-   Les clients LAN câblés et sans fil compatibles Microsoft IEEE 802.1 X implémentent le protocole EAP tel que défini dans la norme IEEE 802.1 X Draft.
-   Le serveur Microsoft RADIUS, appelé service d’authentification Internet (IAS), implémente le protocole EAP tel que défini dans la [norme RFC 2865](https://go.microsoft.com/fwlink/p/?linkid=84055).

tous les composants ci-dessus prennent en charge cette architecture extensible via le kit de développement logiciel (SDK) de Microsoft Windows, ce qui vous permet d’intégrer des modules d’authentification tiers. Ce mécanisme extensible peut être utilisé pour prendre en charge les cartes à jetons, Kerberos, la clé publique et les protocoles d’authentification S/Key.

## <a name="protected-extensible-authentication-protocol"></a>Protocole EAP (Protected Extensible Authentication Protocol)

En plus de l’EAP, l’implémentation sans fil (802.1 X) et le serveur RADIUS prennent également en charge une norme émergente appelée PEAP (Protected EAP).

PEAP fournit plusieurs services clés à d’autres protocoles d’authentification EAP, comme suit.

-   PEAP chiffre les paquets EAP d’autres protocoles d’authentification EAP à l’aide de TLS (Transport Layer Security), une technologie SSL (Secure Socket Layer). Pour plus d’informations, consultez la [RFC 2716](https://go.microsoft.com/fwlink/p/?linkid=84050).
-   PEAP authentifie le côté serveur à l’aide d’un certificat de serveur, avec le serveur RADIUS.
-   PEAP offre une nouvelle fonctionnalité d’authentification rapide qui prend en charge l’itinérance efficace entre les périphériques sans fil.
-   PEAP gère la fragmentation et le réassemblage des paquets EAP.
-   PEAP génère des clés utilisées pour le chiffrement du trafic sans fil.

Grâce à PEAP, il est beaucoup plus facile d’écrire un protocole EAP, car le programmeur n’a plus à résoudre ces problèmes.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[À propos d’EAP et d’EAPHost](about-extenstible-authentication-protocol-and-eaphhost.md)
</dt> </dl>

 

 




