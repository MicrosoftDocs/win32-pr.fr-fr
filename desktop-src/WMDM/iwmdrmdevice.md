---
title: Interface IWMDRMDevice
description: Cette interface n’est pas destinée à être implémentée par un fournisseur de services, mais elle est fournie à des fins de documentation complète. l’interface IWMDRMDevice permet à un fournisseur de contenu sécurisé de communiquer avec des appareils qui utilisent Windows Media DRM 10 pour les appareils mobiles.
ms.assetid: ebad4acd-16cc-433f-a5e0-fcae59030f55
keywords:
- Interface IWMDRMDevice Windows Media Gestionnaire de périphériques
- Interface IWMDRMDevice Windows Media Gestionnaire de périphériques, Description
topic_type:
- apiref
api_name:
- IWMDRMDevice
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: ca240f01f552dfdedb0145e49f61f2ead1f18832
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "126919471"
---
# <a name="iwmdrmdevice-interface"></a>Interface IWMDRMDevice

Cette interface n’est pas destinée à être implémentée par un fournisseur de services, mais elle est fournie à des fins de documentation complète.

l’interface **IWMDRMDevice** permet à un fournisseur de contenu sécurisé de communiquer avec des appareils qui utilisent Windows Media DRM 10 pour les appareils mobiles.

## <a name="members"></a>Membres

L’interface **IWMDRMDevice** hérite de l’interface [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) . **IWMDRMDevice** a également les types de membres suivants :

-   [Méthodes](#methods)

### <a name="methods"></a>Méthodes

L’interface **IWMDRMDevice** possède ces méthodes.



| Méthode                                                                  | Description                                                                                  |
|:------------------------------------------------------------------------|:---------------------------------------------------------------------------------------------|
| [**CleanDataStore**](iwmdrmdevice-cleandatastore.md)                   | Démarre le processus de nettoyage de la Banque de données DRM sur l’appareil.<br/>                  |
| [**GetDeviceCertificate**](iwmdrmdevice-getdevicecertificate.md)       | Récupère le certificat de l’appareil.<br/>                                                 |
| [**GetMeterChallenge**](iwmdrmdevice-getmeterchallenge.md)             | Récupère le test de contrôle.<br/>                                                 |
| [**GetSecureClock**](iwmdrmdevice-getsecureclock.md)                   | Récupère l’horloge sécurisée.<br/>                                                       |
| [**GetSecureClockChallenge**](iwmdrmdevice-getsecureclockchallenge.md) | Récupère le challenge d’horloge sécurisé.<br/>                                             |
| [**GetSyncList**](iwmdrmdevice-getsynclist.md)                         | Récupère la liste de synchronisation de licence.<br/>                                       |
| [**IsWMDRMDevice**](iwmdrmdevice-iswmdrmdevice.md)                     | détermine si l’appareil prend en charge Windows Media DRM 10 pour les appareils mobiles.<br/> |
| [**SetLicenseResponse**](iwmdrmdevice-setlicenseresponse.md)           | Définit la réponse de la licence.<br/>                                                        |
| [**SetMeterResponse**](iwmdrmdevice-setmeterresponse.md)               | Définit la réponse de contrôle.<br/>                                                       |
| [**SetSecureClockResponse**](iwmdrmdevice-setsecureclockresponse.md)   | Définit la réponse de l’horloge sécurisée.<br/>                                                   |



 

## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**Interfaces pour les fournisseurs de services**](interfaces-for-service-providers.md)
</dt> </dl>

 

