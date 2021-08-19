---
title: Annulation de l’inscription d’un appareil
description: Utilisez la méthode IUPnPRegistrar UnregisterDevice pour annuler l’inscription d’un appareil.
ms.assetid: 4f7624e3-4d60-406d-8521-1dfc9aee4408
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 85ff8eeb99ec0ba697c301e8cc15100bd06c0323b95f4099329c46729ceba9c0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118999489"
---
# <a name="unregistering-a-device"></a>Annulation de l’inscription d’un appareil

Utilisez la méthode [**IUPnPRegistrar :: UnregisterDevice**](/windows/desktop/api/Upnphost/nf-upnphost-iupnpregistrar-unregisterdevice) pour annuler l’inscription d’un appareil. L’inscription de l’appareil peut être annulée (supprimée de l’hôte de l’appareil) de manière temporaire ou permanente, en fonction de la valeur de *fPermanent*. Les développeurs doivent supprimer les appareils temporairement si les appareils sont réinscrits, et les appareils doivent utiliser le même UDN. Dans le cas contraire, les appareils sont supprimés définitivement.

Le GUID utilisé pour annuler l’inscription n’est pas UDN. Vous devez utiliser l’ID renvoyé par [**IUPnPRegistrar :: RegisterDevice**](/windows/desktop/api/Upnphost/nf-upnphost-iupnpregistrar-registerdevice) ou [**IUPnPRegistrar :: RegisterRunningDevice**](/windows/desktop/api/Upnphost/nf-upnphost-iupnpregistrar-registerrunningdevice).

> [!Note]  
> Vous pouvez libérer l’objet [**IUPnPRegistrar**](/windows/desktop/api/Upnphost/nn-upnphost-iupnpregistrar) . Seul l’ID doit être mis en cache.

 

Si *fPermanent* a la **valeur false**, l’appareil est supprimé temporairement. Utilisez l’interface [**IUPnPReregistrar**](/windows/desktop/api/Upnphost/nn-upnphost-iupnpreregistrar) pour réinscrire l’appareil. Les méthodes [**IUPnPReregistrar :: ReregisterDevice**](/windows/desktop/api/Upnphost/nf-upnphost-iupnpreregistrar-reregisterdevice) et [**IUPnPReregistrar :: ReregisterRunningDevice**](/windows/desktop/api/Upnphost/nf-upnphost-iupnpreregistrar-reregisterrunningdevice) utilisent le même UDN ou UDNs, dans le cas d’appareils imbriqués, générés précédemment par l’hôte d’appareil pour l’appareil non inscrit.

Si *fPermanent* a la **valeur true**, l’appareil est définitivement supprimé de l’hôte de l’appareil. L’inscription de cet appareil à nouveau sur le même ordinateur crée un UDN différent de celui créé précédemment.

> [!Note]  
> Lorsqu’un appareil est inscrit plusieurs fois sur le même ordinateur, l’hôte de l’appareil génère différents UDNs pour chaque instance de l’appareil.

 

 

 




