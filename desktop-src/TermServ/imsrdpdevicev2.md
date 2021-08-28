---
title: Interface IMsRdpDeviceV2
description: Contient des informations sur un objet appareil. Il s’agit d’une amélioration de l’interface IMsRdpDevice.
ms.assetid: 9a380a1a-d44f-4147-8917-bf1e07dbac15
ms.tgt_platform: multiple
keywords:
- Services Bureau à distance de l’interface IMsRdpDeviceV2
- Services Bureau à distance de l’interface IMsRdpDeviceV2, Description
topic_type:
- apiref
api_name:
- IMsRdpDeviceV2
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cca125024592851b260fb8e4c1f43c7621d4897fec0fc19dfc80d18278e09cf2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119000749"
---
# <a name="imsrdpdevicev2-interface"></a>Interface IMsRdpDeviceV2

Contient des informations sur un objet appareil. Il s’agit d’une amélioration de l’interface [**IMsRdpDevice**](imsrdpdevice.md) .

## <a name="members"></a>Membres

L’interface **IMsRdpDeviceV2** hérite de [**IMsRdpDevice**](imsrdpdevice.md). **IMsRdpDeviceV2** a également les types de membres suivants :

-   [Propriétés](#properties)

### <a name="properties"></a>Propriétés

L’interface **IMsRdpDeviceV2** possède les propriétés suivantes.



| Propriété                                                                 | Type d’accès          | Description                                                                                        |
|:-------------------------------------------------------------------------|:---------------------|:---------------------------------------------------------------------------------------------------|
| [**CmClassGuid**](imsrdpdevicev2-cmclassguid.md)<br/>             | Lecture seule<br/> | Contient le GUID de la classe d’installation de Configuration Manager pour l’appareil.<br/>                     |
| [**CmDeviceInstance**](imsrdpdevicev2-cmdeviceinstance.md)<br/>   | Lecture seule<br/> | Contient l’instance d’appareil Configuration Manager de l’appareil.<br/>                       |
| [**DeviceText**](imsrdpdevicev2-devicetext.md)<br/>               | Lecture seule<br/> | Contient le texte de l’appareil.<br/>                                                               |
| [**DriveLetterBitmap**](imsrdpdevicev2-driveletterbitmap.md)<br/> | Lecture seule<br/> | Contient un champ de binaire qui représente une carte des lettres de lecteur contenues dans l’appareil.<br/> |
| [**IsCompositeDevice**](imsrdpdevicev2-iscompositedevice.md)<br/> | Lecture seule<br/> | Spécifie si l’appareil est un appareil composite.<br/>                                          |
| [**IsOptionalDevice**](imsrdpdevicev2-isoptionaldevice.md)<br/>   | Lecture seule<br/> | Spécifie si l’appareil est facultatif pour la redirection USB.<br/>                                |
| [**IsUSBDevice**](imsrdpdevicev2-isusbdevice.md)<br/>             | Lecture seule<br/> | Spécifie si l’appareil est destiné à la redirection USB.<br/>                                         |



 

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows 7 avec SP1<br/>                                                          |
| Serveur minimal pris en charge<br/> | Windows Server 2008 R2 avec SP1<br/>                                             |
| Bibliothèque de types<br/>             | <dl> <dt>MsTscAx.dll</dt> </dl> |
| DLL<br/>                      | <dl> <dt>MsTscAx.dll</dt> </dl> |
| IID<br/>                      | IID \_ IMsRdpDeviceV2 est défini en tant que 5fb94466-7661-42a8-98b7-01904c11668f<br/>      |



 

 





