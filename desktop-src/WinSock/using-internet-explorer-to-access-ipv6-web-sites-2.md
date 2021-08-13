---
description: "Microsoft Internet Explorer prend en charge l’utilisation du protocole IPv6 pour se connecter et accéder aux sites compatibles IPv6 (par exemple, les serveurs Web et les serveurs FTP) lorsque les conditions suivantes sont remplies : IPv6 doit être installé et activé sur l’ordinateur hôte exécutant Internet Explorer. Lors de la connexion à un ordinateur hôte qui se trouve en dehors du sous-réseau local, l’interface qui fournit la connectivité doit avoir une adresse IPv6 routable attribuée. Lors de la connexion à l’adresse de bouclage IPv6 ( :: 1) ou à une destination de liaison locale, aucune adresse IPv6 routable n’est requise. Si l’URL demandée contient un nom (www.contoso.com, par exemple), la requête DNS (Domain Name System) pour ce nom doit retourner une ou plusieurs adresses IPv6. Si l’URL demandée contient une adresse IPv6 ( :: 1, par exemple), l’adresse IPv6 doit être placée entre crochets (https:// \\[ :: 1 \\] ). Les ID d’étendue, parfois appelés index de zone, sont pris en charge dans le cadre de l’adresse IPv6. L’ID d’étendue est utilisé pour déterminer l’interface réseau à utiliser lors de l’envoi de la demande sur les ordinateurs avec plusieurs interfaces réseau. L’ID d’étendue est spécifié à l’aide du caractère « % » après l’adresse IPv6 principale (FE80 :: 1% 11, par exemple). Toutefois, le caractère'% 'doit être placé dans une séquence d’échappement dans l’URL utilisée avec Internet Explorer. Par exemple, l’ID d’étendue 11 sur une adresse lien-local est spécifié en tant que https:// \\[ FE80 :: 1% 2511 \\] lors de l’utilisation d’Internet Explorer. Cette possibilité d’utiliser des adresses IPv6 dans une URL est prise en charge sur Internet Explorer 7 et versions ultérieures."
ms.assetid: c3a8303a-50d6-4deb-a371-171ac0a7c5a9
title: Utilisation d’Internet Explorer pour accéder aux sites Web IPv6
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e48a9f18e80e0e163ad6fe4ccda0aaef43826edd4becb28e294aad5eca7085c3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118559270"
---
# <a name="using-internet-explorer-to-access-ipv6-websites"></a>Utilisation d’Internet Explorer pour accéder aux sites Web IPv6

Microsoft Internet Explorer prend en charge l’utilisation d’IPv6 pour se connecter aux sites compatibles IPv6 et y accéder (par exemple, des serveurs Web et des serveurs FTP) lorsque les conditions suivantes sont remplies :

-   IPv6 doit être installé et activé sur l’ordinateur hôte exécutant Internet Explorer.
    -   Lors de la connexion à un ordinateur hôte qui se trouve en dehors du sous-réseau local, l’interface qui fournit la connectivité doit avoir une adresse IPv6 routable attribuée.
    -   Lors de la connexion à l’adresse de bouclage IPv6 ( :: 1) ou à une destination de liaison locale, aucune adresse IPv6 routable n’est requise.
-   Si l’URL demandée contient un nom (www.contoso.com, par exemple), la requête DNS (Domain Name System) pour ce nom doit retourner une ou plusieurs adresses IPv6.
-   Si l’URL demandée contient une adresse IPv6 ( :: 1, par exemple), l’adresse IPv6 doit être placée entre crochets (https:// \[ :: 1 \] ). Les ID d’étendue, parfois appelés index de zone, sont pris en charge dans le cadre de l’adresse IPv6. L’ID d’étendue est utilisé pour déterminer l’interface réseau à utiliser lors de l’envoi de la demande sur les ordinateurs avec plusieurs interfaces réseau. L’ID d’étendue est spécifié à l’aide du caractère « % » après l’adresse IPv6 principale (FE80 :: 1% 11, par exemple). Toutefois, le caractère'% 'doit être placé dans une séquence d’échappement dans l’URL utilisée avec Internet Explorer. Par exemple, l’ID d’étendue 11 sur une adresse lien-local est spécifié en tant que https:// \[ FE80 :: 1% 2511 \] lors de l’utilisation d’Internet Explorer. Cette possibilité d’utiliser des adresses IPv6 dans une URL est prise en charge sur Internet Explorer 7 et versions ultérieures.

> [!Note]  
> Si Internet Explorer est configuré pour utiliser un serveur proxy, une adresse IPv6 doit être attribuée au serveur proxy et le serveur proxy doit être en mesure de proxyer les adresses IPv6. Le serveur proxy est utilisé pour se connecter à un hôte externe à l’aide du protocole IPv6. Normalement, le serveur proxy est contourné pour les adresses IPv6 de bouclage et lien-local IPv6.

 

 

 



