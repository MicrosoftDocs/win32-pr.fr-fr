---
title: Inscription d’un appareil hébergé auprès de l’hôte de l’appareil
description: L’inscription d’un appareil hébergé signifie fournir à l’hôte d’appareil la description de l’appareil et son objet de contrôle de l’appareil.
ms.assetid: 1d85b412-9b1b-415d-8664-8d96a6644793
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 486d01364b684e2aa6792b8a6c0b91ccc87a26670057c67192fe587ac049c388
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118999559"
---
# <a name="registering-a-hosted-device-with-the-device-host"></a>Inscription d’un appareil hébergé auprès de l’hôte de l’appareil

L’inscription d’un appareil hébergé signifie fournir à l’hôte d’appareil la description de l’appareil et son objet de contrôle de l’appareil. L’hôte d’appareil construit ensuite une description complète de l’appareil UPnP, le publie et annonce l’appareil sur le réseau à l’aide du protocole de découverte UPnP. Une fois qu’un appareil est publié, il est disponible pour les points de contrôle.

Les appareils sont inscrits de deux manières :

-   Une application crée une instance de l’objet de contrôle de l’appareil et lui transmet un pointeur vers l’hôte de l’appareil.
-   L’application transmet le ProgID d’un objet de contrôle d’appareil inscrit à l’hôte de l’appareil. L’hôte d’appareil l’instancie lorsque l’hôte de l’appareil reçoit la première demande de l’appareil.

Quelle que soit la méthode utilisée, l’hôte d’appareil publie et annonce l’appareil dès qu’il est enregistré. La différence entre les deux approches concerne le chargement du code de l’appareil. Lorsque l’application passe dans un pointeur vers l’objet de contrôle d’appareil, le code de l’appareil est chargé et en cours d’exécution au moment de l’inscription. Lorsque l’application passe un ProgID, le code de l’appareil n’est chargé qu’au moment de l’appel d’une action, une propriété est interrogée ou une demande d’abonnement à un événement arrive. La deuxième approche est un peu plus efficace. Toutefois, elle ne convient pas pour les appareils qui doivent être en cours d’exécution avant l’arrivée des demandes d’abonnement de contrôle ou d’événement, car l’utilisation de cette approche ne crée des objets de contrôle de périphérique que lorsqu’ils sont nécessaires. Cette deuxième méthode peut également créer des problèmes de performances lorsqu’elle reçoit la première demande pour un type d’appareil.

Si vous souhaitez vous assurer qu’un appareil est annoncé automatiquement par l’hôte d’appareil sur le réseau au démarrage de l’ordinateur, appelez [**IUPnPRegistrar :: RegisterDevice**](/windows/desktop/api/Upnphost/nf-upnphost-iupnpregistrar-registerdevice). **RegisterDevice** garantit que le code de votre appareil est uniquement chargé lors de la réception d’une demande de contrôle ou d’abonnement à un événement.

Si vos appareils sont temporaires ou pontés, appelez [**IUPnPRegistrar :: RegisterRunningDevice**](/windows/desktop/api/Upnphost/nf-upnphost-iupnpregistrar-registerrunningdevice), et l’appareil n’est pas automatiquement republié lorsque l’ordinateur est redémarré.

## <a name="discovery-announcement-lifetime"></a>Durée de vie de l’annonce de découverte

Chaque appareil inscrit auprès de l’hôte d’appareil est associé à une durée de vie spécifiée par l’appareil lors de l’inscription. La durée de vie de l’appareil correspond à la durée pendant laquelle les annonces de découverte de l’appareil sont valides. La durée de vie est passée au point de contrôle en tant qu’en-tête dans l’annonce de découverte initiale. L’hôte d’appareil actualise automatiquement l’annonce avant l’heure d’expiration. Les valeurs de la durée de vie de l’annonce de découverte doivent être de 15 minutes ou plus (la valeur par défaut est 30 minutes).

## <a name="device-identifiers-created-at-registration"></a>Identificateurs de périphérique créés lors de l’inscription

Lorsque vous créez un modèle de description de l’appareil, le développeur de l’appareil doit fournir le chemin d’accès de la ressource à la description du service et les icônes associées. Le chemin d’accès de la ressource est déterminé par l’application de l’appareil.

Étant donné que le même appareil peut être inscrit plusieurs fois sur le même ordinateur, le UDN spécifié dans le modèle de description de l’appareil n’est pas suffisant pour identifier un appareil de manière unique. Par conséquent, lorsqu’un appareil est inscrit, l’hôte de l’appareil crée un identificateur d’appareil. Cet identificateur d’appareil, en association avec le UDN dans le modèle de description de périphérique, peut être utilisé pour identifier un appareil de manière unique.

Cet identificateur est également utilisé lorsque l’appareil est provisoirement désinscrit puis réinscrit. Quand un appareil n’est pas inscrit temporairement, l’hôte de l’appareil ne supprime pas le UDN. Les raisons pour lesquelles il n’est pas supprimé UDN sont les suivantes :

-   L’appareil est en cours de mise à niveau.
-   Vous modifiez les propriétés de l’appareil.
-   Un service est temporairement indisponible.
-   Vous ajoutez un nouveau service à un appareil.
-   Vous mettez à jour la DLL.
-   L’appareil est en mode veille.

Pour plus d’informations sur l’inscription, reportez-vous aux sections suivantes :

-   [Comment inscrire un appareil auprès de l’hôte de l’appareil](how-to-register-a-device-with-the-device-host.md)
-   [Annulation de l’inscription d’un appareil](unregistering-a-device.md)
-   [**IUPnPRegistrar::UnregisterDevice**](/windows/desktop/api/Upnphost/nf-upnphost-iupnpregistrar-unregisterdevice)
-   [**IUPnPReregistrar**](/windows/desktop/api/Upnphost/nn-upnphost-iupnpreregistrar)

 

 




