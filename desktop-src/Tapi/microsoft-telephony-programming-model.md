---
description: Le modèle de programmation de téléphonie de Microsoft permet d’extraire le contrôle des communications du contrôle de périphérique, de libérer les applications et les fabricants d’appareils des utilisateurs finaux des besoins en mars dans échelons.
ms.assetid: 07dd8447-08dc-4ae3-9a22-70e914c392db
title: Modèle de programmation de téléphonie Microsoft
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 33407069c8ff489006c3cb85e03b676126eca1abedf484d9d1bb5b1305677a15
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119518642"
---
# <a name="microsoft-telephony-programming-model"></a>Modèle de programmation de téléphonie Microsoft

Le modèle de programmation de téléphonie de Microsoft permet d’extraire le contrôle des communications du contrôle de périphérique, de libérer les applications et les fabricants d’appareils des utilisateurs finaux des besoins en mars dans échelons. À l’aide de ce modèle, une application de serveur ou d’utilisateur final ne requiert pas d’informations détaillées sur le contrôle de périphérique et l’appareil n’a pas besoin d’être adapté à l’application. Les applications et les appareils peuvent subir des innovations et changer sans que cela ne soit pas rendu superflu aux clients.

Le diagramme suivant illustre la façon dont cette abstraction est accomplie.

![Comment l’interface TAPI isole le contrôle des communications du contrôle de périphérique](images/tapicomp.png)

Ces composants peuvent être affichés en tant que référentiels de connaissances spécialisées. L’application TAPI (Telephony Application Programming Interface) connaît les besoins des utilisateurs, la DLL TAPI et TAPISRV comprennent la téléphonie générale, et les fournisseurs de services (TSP et MSP) connaissent le contrôle détaillé de l’appareil. Les créateurs d’applications et les fabricants de périphériques n’ont besoin que d’une connaissance générale des exigences des autres.

-   Une application charge la DLL TAPI dans son espace de processus et utilise l’interface TAPI pour communiquer les besoins.
-   L’interface TAPI établit une communication de liaison RPC avec le serveur TAPI.
-   En outre, TAPI 3. x crée un objet MSP et communique avec lui à l’aide d’un ensemble de commandes défini, l’interface MSPI (Media Service Provider Interface).
-   Quand une application appelle une opération TAPI, la bibliothèque de liens dynamiques TAPI valide et marshale les paramètres, puis transfère les informations à TAPISRV.
-   TAPISRV effectue le suivi des ressources de communication disponibles sur l’ordinateur local et des interfaces avec les fournisseurs de services de téléphonie (TSPs) à l’aide de l’interface du fournisseur de services de téléphonie (TSPI).
-   Les communications entre un TSP et un MSP s’effectuent à l’aide d’une connexion virtuelle qui passe par la DLL TAPI et TAPISRV.
-   La paire TSP/MSP fournit des informations sur l’État et les fonctionnalités de l’appareil et implémente les commandes spécifiques requises pour la réponse souhaitée.

Le résultat de l’utilisation de ce modèle de programmation est que les applications peuvent ignorer ou ajuster aux modifications des appareils et que de nouveaux appareils peuvent être utilisés instantanément au lieu d’attendre les modifications de base du code. La part de marché potentielle est étendue pour les rédacteurs d’applications et les fabricants de périphériques.

Les rubriques suivantes décrivent les composants de téléphonie Microsoft plus en détail :

-   [Applications TAPI](tapi-applications.md)
-   [DLL TAPI](tapi-dll.md)
-   [Serveur TAPI](tapi-server.md)
-   [Fournisseurs de services](service-providers.md)
-   [Modèle synchrone/asynchrone](synchronous-asynchronous-model.md)
-   [Structures de données TAPI](tapi-data-structures.md)
-   [Niveaux de service TAPI](tapi-levels-of-service.md)

 

 



