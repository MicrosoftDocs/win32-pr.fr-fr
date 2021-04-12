---
title: Bande passante réseau
description: Les transferts en arrière-plan utilisent uniquement la bande passante réseau inactive pour préserver l’expérience interactive de l’utilisateur avec d’autres applications réseau, telles que Internet Explorer.
ms.assetid: c0b92a33-7afc-4250-8549-54cc46013239
ms.topic: article
ms.date: 10/09/2018
ms.openlocfilehash: 39a38a0efd5f2caea432fc9d13f7a958b6bcd407
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104031475"
---
# <a name="network-bandwidth"></a>Bande passante réseau

Les transferts en arrière-plan utilisent uniquement la bande passante réseau inactive pour préserver l’expérience interactive de l’utilisateur avec d’autres applications réseau telles que les navigateurs Web. BITS ajuste l’utilisation de la bande passante lorsque l’utilisateur augmente ou diminue l’utilisation de la bande passante. Notez que le service BITS transfère encore une petite quantité de données lors d’une utilisation intensive du réseau pour s’assurer que les travaux BITS progressent.

BITS surveille le trafic réseau au niveau du périphérique de passerelle Internet (IGD) ou de la carte d’interface réseau (NIC) du client et utilise uniquement la partie inactive de la bande passante réseau. BITS permet également à [LEDBAT](https://blogs.technet.microsoft.com/networking/2018/07/25/ledbat/) sur les connexions HTTP de réduire l’encombrement du réseau.

Si le service BITS utilise la carte d’interface réseau pour mesurer le trafic et qu’il n’y a aucune application réseau en cours d’exécution sur le client, le service BITS consommera la plus grande partie de la bande passante disponible. Cela ne signifie pas que le réseau au-delà du client est inactif ; le réseau est peut-être à pleine capacité.

Cela peut être un problème si le client dispose d’une carte réseau rapide, mais que la connexion Internet complète se fait via une liaison lente (comme un routeur DSL), car le service BITS est en concurrence pour la bande passante complète au lieu d’utiliser uniquement la bande passante disponible sur la liaison lente. BITS n’a aucune visibilité sur le trafic réseau au-delà du client.

Un périphérique de passerelle qui prend en charge les compteurs peut éliminer ce problème, car le service BITS mesure le trafic sur la liaison lente et utilise la bande passante de manière appropriée. Si l’appareil ne prend pas en charge les compteurs, vous pouvez réduire l’impact de ce type de connexion, en utilisant la stratégie **MaxInternetBandwidth** pour limiter la bande passante utilisée par bits sur l’ordinateur client. Pour plus d’informations, consultez [stratégies de groupe](group-policies.md).

Si l’ordinateur contient plusieurs interfaces réseau, telles qu’un modem, un réseau privé virtuel (VPN) et plusieurs cartes d’interface réseau (NIC), BITS appelle la fonction d’assistance IP, [**GetBestInterfaceEx**](/windows/desktop/api/iphlpapi/nf-iphlpapi-getbestinterfaceex), pour déterminer l’interface qui a le meilleur itinéraire vers l’adresse IP spécifiée. BITS surveillera ensuite l’utilisation de la bande passante sur cette interface.

## <a name="using-an-internet-gateway-device-igd-to-determine-usage"></a>Utilisation d’un périphérique de passerelle Internet (IGD) pour déterminer l’utilisation

Pour utiliser un périphérique de passerelle, l’appareil doit prendre en charge les compteurs d’octets (l’appareil doit répondre aux actions GetTotalBytesSent et GetTotalBytesReceived) et le Plug-and-Play universel (UPnP) doit être activé.

Le service BITS utilise la carte d’interface réseau dans les cas suivants :

-   L’appareil de passerelle ne prend pas en charge les compteurs
-   UPnP n’est pas activé
-   Le serveur se trouve dans le même sous-réseau
-   L’appareil de passerelle ne retourne pas les données du compteur en moins de 200 cycles

Si l’utilisateur utilise un profil de réseau public, le profil doit autoriser l’UPnP. Par défaut, les profils de réseau privé et de domaine autorisent UPnP.

Si une connexion VPN est utilisée, le service BITS utilise le premier périphérique renvoyé par UPnP.