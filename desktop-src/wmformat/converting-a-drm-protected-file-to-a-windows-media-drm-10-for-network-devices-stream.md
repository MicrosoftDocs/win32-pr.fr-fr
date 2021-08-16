---
title: conversion d’un fichier de DRM-Protected en un flux Windows Media DRM 10 pour les périphériques réseau
description: conversion d’un fichier de DRM-Protected en un flux Windows Media DRM 10 pour les périphériques réseau
ms.assetid: 11aa0cfd-6d87-4ec4-82d8-db2507402911
keywords:
- Windows Media Format SDK, conversion de fichiers protégés par DRM
- Windows Media Format SDK, fichiers protégés par DRM
- ASF (Advanced Systems Format), conversion de fichiers protégés par DRM
- ASF (format de systèmes avancés), conversion de fichiers protégés par DRM
- Fichiers ASF (Advanced Systems Format), fichiers protégés par DRM
- ASF (format des systèmes avancés), fichiers protégés par DRM
- gestion des droits numériques (DRM), conversion de fichiers protégés par DRM
- DRM (gestion des droits numériques), conversion de fichiers protégés par DRM
- gestion des droits numériques (DRM), fichiers protégés par DRM
- DRM (gestion des droits numériques), fichiers protégés par DRM
- Windows media Format SDK, Windows media DRM 10 pour les périphériques réseau
- Windows Media Format SDK, DRM 10 pour les périphériques réseau
- ASF (Advanced Systems Format), Windows Media DRM 10 pour les périphériques réseau
- ASF (Format de systèmes avancés), Windows Media DRM 10 pour les périphériques réseau
- ASF (Advanced Systems Format), DRM 10 pour les périphériques réseau
- ASF (format de systèmes avancés), DRM 10 pour les périphériques réseau
- gestion des droits numériques (drm), Windows Media drm 10 pour les périphériques réseau
- drm (digital rights management), Windows Media drm 10 pour les périphériques réseau
- gestion des droits numériques (DRM), DRM 10 pour les périphériques réseau
- DRM (gestion des droits numériques), DRM 10 pour les périphériques réseau
- Windows Media DRM 10 pour les périphériques réseau, conversion de fichiers protégés par DRM
- DRM 10 pour les périphériques réseau, conversion de fichiers protégés par DRM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ebe5aa16b13f41c0376da84237a846612b7ae6e730e630be6ec4a45ce48ff4fd
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117848910"
---
# <a name="converting-a-drm-protected-file-to-a-windows-media-drm-10-for-network-devices-stream"></a>conversion d’un fichier de DRM-Protected en un flux Windows Media DRM 10 pour les périphériques réseau

Une fois qu’un appareil est inscrit et validé, vous pouvez commencer à traiter les messages de demande de licence à partir de celui-ci. Les messages de demande de licence sont envoyés par les appareils quand l’action à partir de l’application est nécessaire. La seule action actuellement prise en charge est « Play », qui est une demande de données sécurisées pour la lecture.

Lorsque vous recevez un message de demande de licence, vous devez effectuer les étapes suivantes :

1.  Analysez le message de demande de licence en appelant la méthode [**IWMDRMMessageParser ::P arselicenserequestmsg**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdrmmessageparser-parselicenserequestmsg) .
2.  Obtenez l’interface [**IWMRegisteredDevice**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmregistereddevice) pour l’appareil en appelant la méthode [**IWMDeviceRegistration :: GetRegisteredDeviceByID**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdeviceregistration-getregistereddevicebyid) , en passant le certificat et le numéro de série obtenus à l’étape 1.
3.  Vérifiez que l’appareil est prêt à recevoir des données sécurisées :
    -   Appelez [**IWMRegisteredDevice :: IsApproved**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmregistereddevice-isapproved) pour vérifier que l’appareil a été approuvé. L’approbation doit toujours reposer sur la préférence de l’utilisateur.
    -   Appelez [**IWMRegisteredDevice :: IsValid**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmregistereddevice-isvalid) pour vérifier que l’appareil a été validé au cours des dernières 48 heures. Si l’appareil n’est pas valide, vous devez effectuer la détection de proximité. Pour plus d’informations, consultez exécution de la [détection de proximité](performing-proximity-detection.md).
    -   Appelez [**IWMRegisteredDevice :: IsOpened**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmregistereddevice-isopened) pour vérifier que l’appareil a été ouvert. Si l’appareil n’est pas ouvert, vous pouvez l’ouvrir en appelant [**IWMRegisteredDevice :: Open**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmregistereddevice-open). Vous ne pouvez avoir que 10 appareils ouverts à la fois sur l’ordinateur. Il est possible que vous deviez fermer un autre appareil avant de pouvoir ouvrir celui pour lequel vous traitez la demande. Pour fermer un appareil, appelez la méthode [**IWMRegisteredDevice :: Close**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmregistereddevice-close) .
4.  Créez une instance de l’objet de transcrypteur DRM en appelant la fonction [**WMCreateDRMTranscryptor**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-wmcreatedrmtranscryptor) .
5.  Appelez la méthode [**IWMDRMTranscryptor :: Initialize**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdrmtranscryptor-initialize) pour initialiser le transchiffreur. Cette méthode prend un pointeur vers votre implémentation de l’interface [**IWMStatusCallback**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmstatuscallback) , qu’elle utilise pour remettre des messages d’État. Cette méthode retourne également un message de demande de licence qui doit être envoyé à l’appareil avant de continuer.
6.  Lorsque la méthode [**IWMStatusCallback :: OnStatus**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmstatuscallback-onstatus) de votre application reçoit le message d’état d’initialisation de transcryptor WMT \_ \_ , appelez la méthode [**IWMDRMTranscryptor :: Seek**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdrmtranscryptor-seek) pour rechercher la position de départ appropriée dans le fichier. Pour commencer au début du fichier, vous devez appeler **Seek** avec l’heure 0.
7.  Le transchiffreur envoie un message de recherche de transchiffrement WMT \_ \_ lorsqu’il est prêt à fournir des données à partir du fichier au moment de la nouvelle présentation. Effectuez des appels répétés à la méthode [**IWMDRMTranscryptor :: Read**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdrmtranscryptor-read) pour obtenir des blocs de données multimédias convertis. Chaque appel est asynchrone et n’est pas terminé tant qu’un message de lecture de transcryptour WMT n’a pas \_ \_ été reçu. Lorsque vous recevez le message, vous pouvez envoyer les données à l’appareil de réception.
8.  Lorsque vous recevez un message de lecture de transcryptour WMT \_ \_ avec le paramètre *HR* défini sur le paramètre \_ \_ EOF du transcrypteur NS \_ , le fichier entier a été lu. À ce stade, appelez la méthode [**IWMDRMTranscryptor :: Close**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdrmtranscryptor-close) pour fermer le fichier et libérer des ressources.
9.  Lorsque le message de déchiffrement WMT \_ \_ fermé est reçu, vous pouvez libérer l’interface [**IWMDRMTranscryptor**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmdrmtranscryptor) .

> [!Note]  
> DRM n’est pas pris en charge par la version x64 de ce kit de développement logiciel (SDK).

 

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[**utilisation du protocole Windows Media DRM 10 pour les périphériques réseau**](using-the-windows-media-drm-10-for-network-devices-protocol.md)
</dt> </dl>

 

 




