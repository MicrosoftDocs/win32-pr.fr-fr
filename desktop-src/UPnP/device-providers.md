---
title: Fournisseurs d’appareils
description: Les fournisseurs d’appareils sont des objets inscrits que l’ordinateur démarre à chaque démarrage du système.
ms.assetid: 80c08993-0a8b-4ee9-93cd-bcc3c00e843b
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 67fac270342830045fc3bac9f0573f283d87dc6a
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104101752"
---
# <a name="device-providers"></a>Fournisseurs d’appareils

Les fournisseurs d’appareils sont des objets inscrits que l’ordinateur démarre à chaque démarrage du système. Les fournisseurs d’appareils enregistrent et annulent l’inscription des appareils en cours d’exécution avec l’hôte d’appareil en réponse à un événement. Ces appareils sont des appareils qui ont été démarrés automatiquement au moment du démarrage du système. Pour des raisons de sécurité, un fournisseur d’appareil doit généralement s’exécuter en tant que [LocalService](/windows/desktop/Services/localservice-account), plutôt que [LocalSystem](/windows/desktop/Services/localsystem-account).

Les fournisseurs de périphériques peuvent être utilisés pour les appareils temporaires. Les fournisseurs d’appareils peuvent également servir à relier des appareils à des médias interrogés. Par exemple, un périphérique périphérique, tel qu’un lecteur de musique numérique, est connecté à un ordinateur par le biais d’un port série. Pour exposer le lecteur de musique en tant qu’appareil UPnP, un objet de contrôle de périphérique et un ensemble d’objets de service sont requis. Ces objets implémentent les actions de lecteur de musique UPnP en tant que commandes en série. Toutefois, le lecteur de musique doit être connecté au port série et disponible pour le contrôle avant l’inscription de ces objets.

Étant donné que le port série n’offre pas de mécanisme de notification explicite lorsque des appareils sont connectés, le code d’interrogation est nécessaire. Ce code peut être implémenté dans un objet fournisseur d’appareils, un service ou dans une application autonome. Lorsque l’ordinateur est démarré, l’hôte d’appareil instancie l’objet fournisseur de l’appareil, puis appelle sa méthode [**Start**](/windows/desktop/api/Upnphost/nf-upnphost-iupnpdeviceprovider-start) . Lorsque le fournisseur de l’appareil détecte la présence d’un périphérique de lecteur de musique, il instancie l’objet de contrôle d’appareil approprié et l’inscrit en appelant [**IUPnPRegistrar :: RegisterRunningDevice**](/windows/desktop/api/Upnphost/nf-upnphost-iupnpregistrar-registerrunningdevice). Cette méthode publie l’appareil et l’annonce au réseau UPnP.

La même fonctionnalité peut également être obtenue en implémentant un service qui interroge le port série. Toutefois, les fournisseurs d’appareils simplifient les choses en exigeant uniquement les fonctionnalités principales (l’interrogation) à implémenter, car les fournisseurs d’appareils s’appuient sur l’hôte de l’appareil pour les démarrer et les arrêter. L’utilisation de fournisseurs de périphériques est plus simple que l’implémentation d’un service.

Au moment de l’inscription, et à chaque démarrage suivant du système, l’ordinateur instancie l’objet fournisseur de l’appareil, puis appelle sa méthode [**IUPnPDeviceProvider :: Start**](/windows/desktop/api/Upnphost/nf-upnphost-iupnpdeviceprovider-start) , en lui transmettant la chaîne d’initialisation spécifiée lors de l’inscription.

Une fois la méthode [**Start**](/windows/desktop/api/Upnphost/nf-upnphost-iupnpdeviceprovider-start) appelée, le fournisseur de l’appareil effectue le traitement nécessaire et, le cas échéant, le fournisseur de l’appareil inscrit les appareils en appelant [**IUPnPRegistrar :: RegisterRunningDevice**](/windows/desktop/api/Upnphost/nf-upnphost-iupnpregistrar-registerrunningdevice), comme décrit dans la section [inscription d’un appareil hébergé auprès de l’hôte de l’appareil](registering-a-hosted-device-with-the-device-host.md).

Lorsque l’ordinateur est arrêté, l’hôte de l’appareil appelle la méthode [**IUPnPDeviceProvider :: Stop**](/windows/desktop/api/Upnphost/nf-upnphost-iupnpdeviceprovider-stop) pour indiquer que le fournisseur de l’appareil a terminé ses opérations.

 

 