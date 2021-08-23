---
description: TAPI version 3,1 est une API COM qui fusionne les téléphonie classiques et IP. Les applications possibles sont comprises entre les appels vocaux simples sur le réseau téléphonique commuté public et la multidiffusion des conférences IP multimédias avec la qualité de service (QOS).
ms.assetid: 1f7ccef8-5aad-48e7-90e9-a378dd83a870
title: Vue d’ensemble de TAPI 3,1
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c55aff75690894cc8c8a0d5e692b0c9b019a39116a617dbf2a4ae050200f6892
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119139895"
---
# <a name="tapi-31-overview"></a>Vue d’ensemble de TAPI 3,1

TAPI version 3,1 est une API COM qui fusionne les téléphonie classiques et IP. Les applications possibles sont comprises entre les appels vocaux simples sur le réseau téléphonique commuté public et la multidiffusion des conférences IP multimédias avec la qualité de service (QOS).

Pour plus d’informations sur les fonctionnalités de téléphonie IP TAPI 3,1, consultez le livre blanc « téléphonie IP avec TAPI 3 », qui se trouve sur le site Web de Microsoft.

Il existe quatre principaux composants pour TAPI 3,1 :

-   API COM
-   Serveur TAPI
-   Fournisseurs de services de téléphonie (TSPs)
-   Fournisseurs de flux de médias (MSP)

Le diagramme suivant illustre l’architecture TAPI 3,1 :

![architecture TAPI 3](images/callarc-gif-1.png)

L’API est implémentée en tant que suite d’objets COM (Component Object Model). le déplacement de l’interface tapi vers le modèle COM orienté objet permet aux développeurs d’écrire des applications compatibles tapi dans de nombreux langages, tels que Java, Visual Basic ou C/C++. L’utilisation de COM active les mises à niveau de composants des fonctionnalités TAPI.

Le processus de serveur TAPI (TAPISRV) extrait l’interface du fournisseur de services (TSPI) TAPI des 3. x et TAPI 2. x, ce qui permet d’utiliser les fournisseurs de services de téléphonie TAPI 2. x avec TAPI 3. x, en conservant l’état interne de l’interface TAPI. TAPISRV est implémenté en tant que processus de service dans SVCHOST.

Les [fournisseurs de services](./tapi-service-providers.md) dérésument les mécanismes de transport de médias spécifiques au fournisseur. Ils existent généralement par paires : un fournisseur de services de téléphonie (TSP) pour le contrôle d’appel et un fournisseur de services de média (MSP) pour le contrôle de média.

Les [fournisseurs de services de téléphonie](./telephony-service-providers-start-page.md) (TSPs) sont responsables de la résolution du modèle d’appel indépendant du protocole de l’interface TAPI en mécanismes de contrôle d’appels spécifiques au protocole. TAPI 3,1 offre une compatibilité descendante avec TAPI 2,1 TSPs. Deux fournisseurs de services de téléphonie IP (et leurs MSP associés) sont livrés par défaut avec TAPI 3,1 : le TSP H. 323 et le TSP de conférence IP multicast.

les [fournisseurs de services multimédias](media-service-providers-start-page.md) (msp) offrent un moyen uniforme d’accéder aux flux de média dans un appel, en prenant en charge l’API DirectShow<sup>TM</sup> comme gestionnaire de flux de média principal. les msp TAPI implémentent des interfaces DirectShow pour un TSP particulier et sont nécessaires pour tout service de téléphonie qui utilise la diffusion en continu DirectShow. Les flux génériques sont gérés par l’application.

 

 
