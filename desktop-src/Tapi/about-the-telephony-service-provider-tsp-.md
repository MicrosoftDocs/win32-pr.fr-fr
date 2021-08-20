---
description: Un fournisseur de services de téléphonie TAPI (TSP) est une bibliothèque de liens dynamiques (DLL) qui prend en charge le contrôle des appareils de communication via un ensemble de fonctions de service exportées.
ms.assetid: 6e4fb295-940e-4f76-ad43-fad7da90094a
title: À propos du fournisseur de services de téléphonie (TSP)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6ab5f7d1d1631c1146bfb06223fa722bf27daa5cd6ec8e3f4f4b83d1d23c5554
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117949266"
---
# <a name="about-the-telephony-service-provider-tsp"></a>À propos du fournisseur de services de téléphonie (TSP)

\[les TSPs H323 et IPConf ne sont pas disponibles pour une utilisation dans Windows Vista, Windows Server 2008 et les versions ultérieures du système d’exploitation. L’API cliente RTC offre des fonctionnalités similaires.\]

Un fournisseur de services de téléphonie TAPI (TSP) est une bibliothèque de liens dynamiques (DLL) qui prend en charge le contrôle des appareils de communication via un ensemble de fonctions de service exportées. Une application TAPI utilise des commandes standardisées, TAPI passe en formation au fournisseur de services de téléphonie et le TSP gère les commandes spécifiques qui doivent être échangées avec l’appareil.

Les sections suivantes décrivent brièvement les TSPs fournis avec Microsoft Windows :

-   [TSP H323](h323-tsp.md)
-   [TSP IPConf](ipconf-tsp.md)
-   [TSP pilote de périphérique en mode noyau](kernel-mode-device-driver-tsp.md)
-   [TSP proxy NDIS](ndis-proxy-tsp.md)
-   [TSP distant](remote-tsp.md)
-   [TSP tiers](third-party-tsp.md)
-   [TSP Unimodem](unimodem-tsp.md)

Pour plus d’informations, consultez le kit de ressources pour le système d’exploitation cible. Les TSPs tiers pour les appareils de communication spécialisés sont généralement fournis par le fabricant et sont installés avec l’appareil.

Les rubriques suivantes décrivent comment créer un TSP qui fonctionnera correctement dans l’environnement de téléphonie Microsoft, et comment créer une paire TSP/MSP :

-   [Interface du fournisseur de services de téléphonie (TSPI)](telephony-service-provider-interface-tspi-.md)
-   [Référence TSPI](tspi-reference.md)
-   [Fournisseurs de services de média](./media-service-providers-start-page.md)

> [!Note]  
> Un TSP est une DLL créée par l’utilisateur. si vous créez un TSP pour une plateforme Windows 64 bits, vous devez le compiler en tant que dll 64 bits ou dll.

 

 

 
