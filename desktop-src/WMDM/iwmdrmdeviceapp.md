---
title: Interface IWMDRMDeviceApp
description: L’interface IWMDRMDeviceApp permet à une application de mesurer, de synchroniser des licences et de mettre à jour les composants DRM d’un appareil.
ms.assetid: e47167c2-ea14-4173-8ce9-8d8540a0fc73
keywords:
- Interface IWMDRMDeviceApp Windows Media Gestionnaire de périphériques
- Interface IWMDRMDeviceApp Windows Media Gestionnaire de périphériques, Description
topic_type:
- apiref
api_name:
- IWMDRMDeviceApp
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 9cf44295c9972d7549eb4a82fda7c415ba81c31d
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "106544157"
---
# <a name="iwmdrmdeviceapp-interface"></a>Interface IWMDRMDeviceApp

\[La fonctionnalité Windows Media DRM est déconseillée et ne doit pas être utilisée. Utilisez plutôt [Microsoft PlayReady](/windows/uwp/audio-video-camera/playready-client-sdk) .\]

L’interface **IWMDRMDeviceApp** permet à une application de mesurer, de synchroniser des licences et de mettre à jour les composants DRM d’un appareil. Cette interface ne fonctionne que pour les appareils qui prennent en charge Windows Media DRM 10 pour les appareils mobiles.

Pour accéder à cette interface, appelez **CoCreateInstance**, en transmettant CLSID \_ WMDRMDeviceApp.

> [!Note]  
> Cette interface est définie dans le fichier d’en-tête généré à partir de WMDRMDeviceApp. idl. Cet en-tête **\# inclut**« WMDM. h ». Vous devrez peut-être modifier ce nom de fichier pour qu’il corresponde à l’en-tête généré à partir de WMDM. idl.

 

## <a name="members"></a>Membres

L’interface **IWMDRMDeviceApp** hérite de l’interface [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) . **IWMDRMDeviceApp** a également les types de membres suivants :

-   [Méthodes](#methods)

### <a name="methods"></a>Méthodes

L’interface **IWMDRMDeviceApp** possède ces méthodes.



| Méthode                                                                   | Description                                                                                                                                |
|:-------------------------------------------------------------------------|:-------------------------------------------------------------------------------------------------------------------------------------------|
| [**AcquireDeviceData**](iwmdrmdeviceapp-acquiredevicedata.md)           | Initialise ou réinitialise une horloge sécurisée de l’appareil<br/>                                                                                     |
| [**GenerateMeterChallenge**](iwmdrmdeviceapp-generatemeterchallenge.md) | Acquiert des données de contrôle à partir d’un appareil.<br/>                                                                                           |
| [**ProcessMeterResponse**](iwmdrmdeviceapp-processmeterresponse.md)     | Réinitialise tout ou partie des nombres de contrôle sur un appareil, une fois que les données de l’appareil ont été envoyées et traitées par le serveur.<br/> |
| [**QueryDeviceStatus**](iwmdrmdeviceapp-querydevicestatus.md)           | Interroge un appareil pour obtenir son état et ses capacités DRM actuels.<br/>                                                                   |
| [**SynchronizeLicenses**](iwmdrmdeviceapp-synchronizelicenses.md)       | Met à jour les licences sur un appareil lorsqu’elles arrivent à expiration.<br/>                                                                   |



 

## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**Gestion du contenu protégé dans l’application**](handling-protected-content-in-the-application.md)
</dt> <dt>

[**Interfaces pour les applications**](interfaces-for-applications.md)
</dt> <dt>

[**Contrôle de l’utilisation du contenu**](metering-content-usage.md)
</dt> </dl>

 

