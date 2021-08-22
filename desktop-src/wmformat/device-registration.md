---
title: Inscription des appareils
description: Inscription des appareils
ms.assetid: 64a6f366-1317-47b6-94a2-ca2ef14d1f88
keywords:
- Windows Media Format SDK, inscription de l’appareil
- Windows Media Format SDK, inscription des appareils
- ASF (Advanced Systems Format), inscription de l’appareil
- ASF (format avancé des systèmes), inscription de l’appareil
- ASF (Advanced Systems Format), inscription des appareils
- ASF (format des systèmes avancés), inscription des appareils
- gestion des droits numériques (DRM), inscription de l’appareil
- DRM (gestion des droits numériques), inscription de l’appareil
- gestion des droits numériques (DRM), inscription des appareils
- DRM (gestion des droits numériques), inscription des appareils
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4f2efbfefaaabf3af0a33f304ad2cc32f7fe3b84691da8242203eddbb18fdb90
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119027927"
---
# <a name="device-registration"></a>Inscription des appareils

le kit de développement logiciel (SDK) Windows Media Format fournit un accès à la base de données d’inscription des appareils. cette base de données est sécurisée sur l’ordinateur client et est utilisée pour inscrire les appareils qui prennent en charge Windows Media DRM 10 pour les périphériques réseau.

quand un appareil est ajouté à un réseau auquel est connecté l’ordinateur client, ce dernier tente de contacter un Windows Media DRM 10 pour les périphériques réseau émetteurs. Après avoir établi la communication, l’appareil envoie un message de demande d’inscription.

Votre application doit effectuer les étapes suivantes lorsqu’elle reçoit un message de demande d’inscription :

1.  Analysez le message en appelant la méthode [**IWMDRMMessageParser ::P arseregistrationreqmsg**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdrmmessageparser-parseregistrationreqmsg) . Cette méthode récupère le certificat de l’appareil et le numéro de série de l’appareil, qui sont tous deux nécessaires pour identifier l’appareil.
2.  Appelez la méthode [**IWMDeviceRegistration :: GetRegisteredDeviceByID**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdeviceregistration-getregistereddevicebyid) , en passant le certificat et le numéro de série de l’appareil récupérés à l’étape 1. Si le périphérique est trouvé, il est déjà inscrit et vous pouvez ignorer l’étape suivante.
3.  Appelez la méthode [**IWMDeviceRegistration :: RegisterDevice**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdeviceregistration-registerdevice) pour ajouter l’appareil à la base de données d’inscription des appareils.

Vous pouvez accéder aux informations sur n’importe quel appareil de la base de données d’inscription en extrayant l’objet d’appareil inscrit qui lui est associé. Il existe deux façons d’obtenir un objet d’appareil inscrit. Si vous avez le certificat et le numéro de série de l’appareil, vous pouvez appeler la méthode [**IWMDeviceRegistration :: GetRegisteredDeviceByID**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdeviceregistration-getregistereddevicebyid) . Si vous n’avez pas le certificat et le numéro de série de l’appareil, vous pouvez énumérer tous les appareils dans la base de données en appelant [**IWMDeviceRegistration :: GetFirstRegisteredDevice**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdeviceregistration-getfirstregistereddevice) suivi d’appels répétés à [**IWMDeviceRegistration :: GetNextRegisteredDevice**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdeviceregistration-getnextregistereddevice) jusqu’à ce qu’un appel retourne la \_ valeur false.

Pour que votre application puisse envoyer des données à un appareil, vous devez vous assurer que l’appareil est approuvé, validé et ouvert.

L’approbation de l’appareil doit impliquer l’interaction avec l’utilisateur. Lorsqu’un appareil envoie un message d’inscription, votre application peut inviter l’utilisateur à décider s’il s’agit d’un appareil qui doit recevoir les données de cet utilisateur. Ensuite, mettez à jour la base de données d’inscription des appareils en appelant la méthode [**IWMRegisteredDevice :: Approve**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmregistereddevice-approve) , en passant **true** ou **false** selon le cas.

La validation est également appelée détection de proximité. il s’agit d’un processus par lequel les objets DRM internes du kit de développement logiciel (SDK) de Format multimédia Windows déterminent si l’appareil est « presque » suffisant pour l’ordinateur exécutant votre application afin de transmettre en toute sécurité des médias. La proximité est déterminée par le temps nécessaire pour obtenir une réponse à un message. Cette fonctionnalité est conçue pour empêcher les utilisateurs non autorisés d’accéder à votre réseau et d’obtenir votre support sécurisé. Pour plus d’informations, consultez exécution de la [détection de proximité](performing-proximity-detection.md).

Pour ouvrir un appareil, appelez [**IWMRegisteredDevice :: Open**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmregistereddevice-open).

> [!Note]  
> DRM n’est pas pris en charge par la version x64 de ce kit de développement logiciel (SDK).

 

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[**IWMRegisteredDevice**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmregistereddevice)
</dt> <dt>

[**utilisation du protocole Windows Media DRM 10 pour les périphériques réseau**](using-the-windows-media-drm-10-for-network-devices-protocol.md)
</dt> </dl>

 

 




