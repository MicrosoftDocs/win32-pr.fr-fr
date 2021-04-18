---
title: Interface IMsRdpDevice
description: Contient des informations sur un objet appareil.
ms.assetid: b486a591-870b-446c-8028-9e4406cdf0ce
ms.tgt_platform: multiple
keywords:
- Services Bureau à distance de l’interface IMsRdpDevice
- Services Bureau à distance de l’interface IMsRdpDevice, Description
topic_type:
- apiref
api_name:
- IMsRdpDevice
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d7ddfbb739a8cf8e93ee2c2214e14095ac68bd77
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "106512788"
---
# <a name="imsrdpdevice-interface"></a>Interface IMsRdpDevice

Contient des informations sur un objet appareil.

## <a name="members"></a>Membres

L’interface **IMsRdpDevice** hérite de l’interface [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) . **IMsRdpDevice** a également les types de membres suivants :

-   [Propriétés](#properties)

### <a name="properties"></a>Propriétés

L’interface **IMsRdpDevice** possède les propriétés suivantes.



| Propriété                                                               | Type d’accès           | Description                                                                                                   |
|:-----------------------------------------------------------------------|:----------------------|:--------------------------------------------------------------------------------------------------------------|
| [**DeviceDescription**](imsrdpdevice-devicedescription.md)<br/> | Lecture seule<br/>  | Récupère la description de l’appareil à afficher à l’utilisateur si le nom complet n’est pas disponible.<br/> |
| [**DeviceInstanceId**](imsrdpdevice-deviceinstanceid.md)<br/>   | Lecture seule<br/>  | Récupère l’identificateur d’instance d’appareil de l’appareil.<br/>                                            |
| [**FriendlyName**](imsrdpdevice-friendlyname.md)<br/>           | Lecture seule<br/>  | Récupère le nom complet de l’appareil.<br/>                                                         |
| [**RedirectionState**](imsrdpdevice-redirectionstate.md)<br/>   | Lecture/écriture<br/> | Indique l’état de redirection de l’appareil.<br/>                                                     |



 

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows Vista<br/>                                                               |
| Serveur minimal pris en charge<br/> | Windows Server 2008<br/>                                                         |
| Bibliothèque de types<br/>             | <dl> <dt>MsTscAx.dll</dt> </dl> |
| DLL<br/>                      | <dl> <dt>MsTscAx.dll</dt> </dl> |
| IID<br/>                      | IID \_ IMsRdpDevice est défini en tant que 60c3b9c8-9E92-4f5e-a3e7-604a912093ea<br/>        |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Référence Connexion Bureau à distance par le Web](remote-desktop-web-connection-reference.md)
</dt> <dt>

[**IMsRdpDeviceCollection**](imsrdpdevicecollection.md)
</dt> </dl>

 

