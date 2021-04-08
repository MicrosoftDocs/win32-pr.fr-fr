---
description: Un fournisseur de services de téléphonie TAPI (TSP) est une bibliothèque de liens dynamiques (DLL) qui prend en charge le contrôle des appareils de communication via un ensemble de fonctions de service exportées.
ms.assetid: 6e4fb295-940e-4f76-ad43-fad7da90094a
title: À propos du fournisseur de services de téléphonie (TSP)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5200a4291bdd91aba9f93a5552fecf4b52d24ee3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103750789"
---
# <a name="about-the-telephony-service-provider-tsp"></a>À propos du fournisseur de services de téléphonie (TSP)

\[ Les TSPs H323 et IPConf ne peuvent pas être utilisés dans Windows Vista, Windows Server 2008 et les versions ultérieures du système d’exploitation. L’API cliente RTC offre des fonctionnalités similaires.\]

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
> Un TSP est une DLL créée par l’utilisateur. Si vous créez un TSP pour une plateforme Windows 64 bits, vous devez le compiler en tant que DLL 64 bits ou dll.

 

 

 
