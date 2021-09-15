---
description: l’objet wia est le point d’entrée pour toutes les fonctionnalités de script de l’acquisition d’images Windows (wia).
ms.assetid: 1905e344-32cc-41ec-885f-bfabd8edd419
title: Objet WIA
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Wia
api_type:
- COM
api_location:
- Wiascr.dll
ms.openlocfilehash: 38dc5f7ac4440320827e009a7fd38dd6554ceb70
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127525241"
---
# <a name="wia-object"></a>Objet WIA

l’objet **wia** est le point d’entrée pour toutes les fonctionnalités de script de l’acquisition d’images Windows (wia). Toute application qui utilise le modèle de script WIA doit créer un objet [**SafeWia**](-wia-safewia.md) ou **WIA** . Utilisez cet objet pour énumérer et créer des appareils et recevoir des notifications d’événements matériels.

> [!Note]  
> Cet objet n’est pas sûr pour l’écriture de scripts. Pour obtenir une version de cet objet sécurisée pour les scripts, consultez [**SafeWia**](-wia-safewia.md).

 

## <a name="members"></a>Membres

L’objet **WIA** possède les types de membres suivants :

-   [Événements](#events)
-   [Méthodes](#methods)
-   [Propriétés](#properties)

### <a name="events"></a>Événements

L’objet **WIA** contient ces événements.



| Événement                                                                 | Description                                                                  |
|:----------------------------------------------------------------------|:-----------------------------------------------------------------------------|
| [**OnDeviceConnected**](-wia--iwiaevents-ondeviceconnected.md)       | Événement qui se produit lorsqu’un nouveau périphérique matériel WIA est connecté.<br/>    |
| [**OnDeviceDisconnected**](-wia--iwiaevents-ondevicedisconnected.md) | Événement qui se produit lorsqu’un nouveau périphérique matériel WIA est déconnecté.<br/> |
| [**OnTransferComplete**](-wia--iwiaevents-ontransfercomplete.md)     | Événement qui se produit lorsqu’un transfert de données est effectué avec succès.<br/> |



 

### <a name="methods"></a>Méthodes

L’objet **WIA** possède les méthodes suivantes.



| Méthode                             | Description                                                                                                                                                                                                |
|:-----------------------------------|:-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Créer**](-wia-iwia-create.md) | La méthode [**Create**](-wia-iwia-create.md) de l’objet **WIA** établit une connexion à l’appareil WIA spécifié et retourne un objet [**Item**](-wia-item.md) qui représente l’appareil.<br/> |



 

### <a name="properties"></a>Propriétés

L’objet **WIA** possède les propriétés suivantes.




| Propriété | Type d’accès | Description | 
|----------|-------------|-------------|
| <a href="-wia-iwia-devices.md"><strong>Appareils</strong></a><br /> | Lecture seule<br /> | Collection d’objets <a href="-wia-deviceinfo.md"><strong>DeviceInfo</strong></a> qui représentent tous les périphériques installés sur l’ordinateur. Lecture seule. <br /><blockquote>[!Note]<br />Cette collection est de base 0.</blockquote><br /> | 




 

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows 2000 Professional, Windows XP \[ desktop apps uniquement\]<br/>                                        |
| Serveur minimal pris en charge<br/> | Windows Serveur 2003 \[ applications de bureau uniquement\]<br/>                                                          |
| DLL<br/>                      | <dl> <dt>Wiascr.dll (version 4,90 ou ultérieure)</dt> </dl> |
| IID<br/>                      | CLSID \_ WIA<br/>                                                                                         |



 

 




