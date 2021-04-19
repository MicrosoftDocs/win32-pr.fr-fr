---
title: Objet d’inscription de l’appareil
description: Objet d’inscription de l’appareil
ms.assetid: 6a23b314-deec-47aa-b12e-cb8f4ff71fb6
keywords:
- Windows Media Format SDK, objets d’inscription d’appareils
- ASF (Advanced Systems Format), objets d’inscription des appareils
- ASF (format des systèmes avancés), objets d’inscription des appareils
- objets, objets d’inscription de l’appareil
- objets d’inscription d’appareil
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 67ba6b72637cf7ba439d0bb38109645742cda4ac
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/19/2020
ms.locfileid: "106509634"
---
# <a name="device-registration-object"></a>Objet d’inscription de l’appareil

L’objet d’inscription de l’appareil gère la base de données d’inscription des appareils. Cette base de données stocke des informations sur les périphériques réseau, tels que les lecteurs vidéo configurés, qui sont connectés à l’ordinateur client. L’objectif principal de la base de données d’inscription des appareils est de gérer les appareils qui utilisent le protocole Windows Media DRM 10 pour les périphériques réseau pour recevoir des flux de données sécurisés.

Si votre application prend en charge Windows Media DRM 10 pour les périphériques réseau, vous devez utiliser les interfaces de cet objet pour inscrire des périphériques réseau et valider ces appareils. Vous pouvez également utiliser la base de données d’inscription d’appareils pour stocker des informations sur les périphériques réseau qui n’utilisent pas Windows Media DRM 10 pour les périphériques réseau, bien que toutes les informations de la base de données ne s’appliquent pas à ces appareils.

L’objet d’inscription de l’appareil est créé par la fonction [**WMCreateDeviceRegistration**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-wmcreatedeviceregistration) , qui définit un pointeur vers une interface **IWMDeviceRegistration** . Les autres méthodes de l’objet d’inscription de l’appareil peuvent être obtenues en appelant la méthode **QueryInterface** .

Les interfaces suivantes sont prises en charge par l’objet d’inscription de l’appareil.



| Interface                                              | Description                               |
|--------------------------------------------------------|-------------------------------------------|
| [**IWMDeviceRegistration**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmdeviceregistration) | Gère la base de données d’inscription des appareils. |
| [**IWMDRMMessageParser**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmdrmmessageparser)     | Analyse les messages envoyés par les appareils.          |
| [**IWMProximityDetection**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmproximitydetection) | Gère la validation de l’appareil.                |



 

L’interface de rappel suivante doit être implémentée par l’application afin d’utiliser les méthodes de l’interface **IWMProximityDetection** .



| Interface                                      | Description                                                                |
|------------------------------------------------|----------------------------------------------------------------------------|
| [**IWMStatusCallback**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmstatuscallback) | Reçoit des messages d’état des processus qui s’exécutent dans un thread séparé. |



 

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[**Objets**](objects.md)
</dt> </dl>

 

 




