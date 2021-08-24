---
title: Énumération des appareils (WMDM)
description: Windows Le Gestionnaire de périphériques de média gère un cache d’appareils connectés. découvrez comment Windows Media Gestionnaire de périphériques gère ou met à jour son cache.
ms.assetid: 7602da65-4c98-4766-b206-2129dad4cc2a
keywords:
- Windows Gestionnaire de périphériques de média, énumération des appareils
- Gestionnaire de périphériques, énumération des appareils
- Guide de programmation, énumération des appareils
- fournisseurs de services, énumération des appareils
- création de fournisseurs de services, énumération d’appareils
- énumération des appareils
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 500375f01e718ab6f9824868ffabd7c83e11c3e812ce0288f0c15186bc1d2de9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119767049"
---
# <a name="enumerating-devices-wmdm"></a>Énumération des appareils (WMDM)

Windows le Gestionnaire de périphériques de média gère un cache de périphériques connectés qui est mis à jour lors du démarrage d’une application Windows Media Gestionnaire de périphériques, lorsqu’un appareil Plug-and-Play (PnP) se connecte ou se déconnecte, ou quand l’application appelle [**IWMDeviceManager2 :: reinitialize**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdevicemanager2-reinitialize). Ce cache est exposé à l’application lorsqu’il appelle [**IWMDeviceManager :: EnumDevices**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdevicemanager-enumdevices) ou [**IWMDeviceManager2 :: EnumDevices2**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdevicemanager2-enumdevices2). Chaque appareil est exposé à l’application en tant qu’interface [**IWMDMDevice**](/windows/desktop/api/mswmdm/nn-mswmdm-iwmdmdevice) . si le fournisseur de services est inscrit pour gérer les périphériques PnP, Windows Media Gestionnaire de périphériques sera informé de la liste actuelle des appareils connectés. Si le fournisseur de services est inscrit pour gérer les périphériques non Plug-and-Play, le fournisseur de services est responsable de la détection des appareils attachés. Un fournisseur de services ne peut être inscrit que pour des appareils PnP ou non Plug-and-Play, jamais les deux à la fois.

les actions suivantes montrent comment Windows Media Gestionnaire de périphériques gère ou met à jour son cache. Notez que le cache n’est jamais mis à jour lorsqu’un appareil non Plug-and-Play se connecte ou se déconnecte.

démarrage d’une application de Gestionnaire de périphériques multimédia Windows

-   Windows Media Gestionnaire de périphériques récupère une liste des périphériques PnP attachés à partir du sous-système PnP et appelle [**IMDServiceProvider2 :: CreateDevice**](/windows/desktop/api/mswmdm/nf-mswmdm-imdserviceprovider2-createdevice) sur le SP inscrit pour chaque périphérique connecté. (Il découvre le fournisseur de services approprié en interrogeant le paramètre d’appareil WMDMSPCLSID pour l’ID de classe du fournisseur de services responsable de cet appareil. Pour plus d’informations, consultez Paramètres de l' [appareil](device-parameters.md) .) tous les appareils renvoyés sont ajoutés au Windows Media Gestionnaire de périphériques cache des appareils.
-   Windows Le Gestionnaire de périphériques de média recherche tous les fournisseurs de services non Plug-and-PnP inscrits auprès de celui-ci et appelle [**IMDServiceProvider :: EnumDevices**](/windows/desktop/api/mswmdm/nf-mswmdm-imdserviceprovider-enumdevices) sur chaque fournisseur de services pour obtenir une liste d’appareils de chacun d’eux. Tous les appareils retournés sont ajoutés au cache.

L’application appelle IWMDeviceManager/2 :: EnumDevices/2

-   Windows Media Gestionnaire de périphériques retourne sa liste de périphériques mis en cache.

Connexion d’un appareil PnP

-   Windows Le Gestionnaire de périphériques de média recherche le fournisseur de services approprié et appelle **IMDServiceProvider2 :: CreateDevice**, puis ajoute l’appareil à son cache.
-   si l’application implémente [**IWMDMNotification**](/windows/desktop/api/mswmdm/nn-mswmdm-iwmdmnotification), Windows Media Gestionnaire de périphériques appelle [**IWMDMNotification :: WMDMMessage**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmnotification-wmdmmessage) avec une notification d’arrivée.

Déconnexion d’un appareil PnP

-   Windows Le Gestionnaire de périphériques de média supprime l’élément de son cache.
-   si l’application implémente IWMDMNotification, Windows Media Gestionnaire de périphériques appelle IWMDMNotification :: WMDMMessage avec une notification de départ.

L’application appelle IWMDeviceManager2 :: Reinitialize

-   Actualise le cache avec tous les appareils connectés.

Un appareil non PnP se connecte ou se déconnecte

-   Windows Le Gestionnaire de périphériques de média n’est pas informé de l’arrivée ou du départ et n’entreprend aucune action.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[**Création d’un fournisseur de services**](creating-a-service-provider.md)
</dt> </dl>

 

 




