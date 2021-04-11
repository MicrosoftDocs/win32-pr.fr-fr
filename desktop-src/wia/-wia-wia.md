---
description: L’objet WIA est le point d’entrée pour toutes les fonctionnalités de script WIA (Windows Image Acquisition).
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
ms.openlocfilehash: 3ab1a9d150eebe77537e18aebc8ab1a3e342099e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104113263"
---
# <a name="wia-object"></a>Objet WIA

L’objet **WIA** est le point d’entrée pour toutes les fonctionnalités de script WIA (Windows Image Acquisition). Toute application qui utilise le modèle de script WIA doit créer un objet [**SafeWia**](-wia-safewia.md) ou **WIA** . Utilisez cet objet pour énumérer et créer des appareils et recevoir des notifications d’événements matériels.

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
| [**Créés**](-wia-iwia-create.md) | La méthode [**Create**](-wia-iwia-create.md) de l’objet **WIA** établit une connexion à l’appareil WIA spécifié et retourne un objet [**Item**](-wia-item.md) qui représente l’appareil.<br/> |



 

### <a name="properties"></a>Propriétés

L’objet **WIA** possède les propriétés suivantes.



<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th style="text-align: left;">Propriété</th>
<th style="text-align: left;">Type d’accès</th>
<th style="text-align: left;">Description</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td style="text-align: left;"><a href="-wia-iwia-devices.md"><strong>Appareils</strong></a><br/></td>
<td style="text-align: left;">Lecture seule<br/></td>
<td style="text-align: left;">Collection d’objets <a href="-wia-deviceinfo.md"><strong>DeviceInfo</strong></a> qui représentent tous les périphériques installés sur l’ordinateur. Lecture seule. <br/>
<blockquote>
[!Note]<br />
Cette collection est de base 0.
</blockquote>
<br/></td>
</tr>
</tbody>
</table>



 

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows 2000 professionnel, applications de \[ Bureau Windows XP uniquement\]<br/>                                        |
| Serveur minimal pris en charge<br/> | Applications de bureau Windows Server 2003 \[ uniquement\]<br/>                                                          |
| DLL<br/>                      | <dl> <dt>Wiascr.dll (version 4,90 ou ultérieure)</dt> </dl> |
| IID<br/>                      | CLSID \_ WIA<br/>                                                                                         |



 

 




