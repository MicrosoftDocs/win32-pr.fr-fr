---
title: Interface IMsRdpDeviceCollection
description: Représente une collection d’objets périphériques.
ms.assetid: 9731b16b-12e0-457e-a4e5-a55d8a6db582
ms.tgt_platform: multiple
keywords:
- Services Bureau à distance de l’interface IMsRdpDeviceCollection
- Services Bureau à distance de l’interface IMsRdpDeviceCollection, Description
topic_type:
- apiref
api_name:
- IMsRdpDeviceCollection
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cace1bc684be4e3e8cf20db84ec8923c9b35a8fa
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104383883"
---
# <a name="imsrdpdevicecollection-interface"></a>Interface IMsRdpDeviceCollection

Représente une collection d’objets périphériques.

## <a name="members"></a>Membres

L’interface **IMsRdpDeviceCollection** hérite de l’interface [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) . **IMsRdpDeviceCollection** a également les types de membres suivants :

-   [Méthodes](#methods)
-   [Propriétés](#properties)

### <a name="methods"></a>Méthodes

L’interface **IMsRdpDeviceCollection** possède ces méthodes.



| Méthode                                                        | Description                                                 |
|:--------------------------------------------------------------|:------------------------------------------------------------|
| [**RescanDevices**](imsrdpdevicecollection-rescandevices.md) | Actualise la liste des objets dans la collection.<br/> |



 

### <a name="properties"></a>Propriétés

L’interface **IMsRdpDeviceCollection** possède les propriétés suivantes.



| Propriété                                                                 | Type d’accès          | Description                                                    |
|:-------------------------------------------------------------------------|:---------------------|:---------------------------------------------------------------|
| [**DeviceById**](imsrdpdevicecollection-devicebyid.md)<br/>       | Lecture seule<br/> | Récupère l’appareil avec l’identificateur spécifié.<br/> |
| [**DeviceByIndex**](imsrdpdevicecollection-devicebyindex.md)<br/> | Lecture seule<br/> | Récupère l’appareil au niveau de l’index spécifié.<br/>        |
| [**DeviceCount**](imsrdpdevicecollection-devicecount.md)<br/>     | Lecture seule<br/> | Récupère le nombre d’objets dans la collection.<br/>   |



 

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows Vista<br/>                                                                  |
| Serveur minimal pris en charge<br/> | Windows Server 2008<br/>                                                            |
| Bibliothèque de types<br/>             | <dl> <dt>MsTscAx.dll</dt> </dl>    |
| DLL<br/>                      | <dl> <dt>MsTscAx.dll</dt> </dl>    |
| IID<br/>                      | IID \_ IMsRdpDeviceCollection est défini comme 56540617-D281-488C-8738-6a8fdf64a118<br/> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Référence Connexion Bureau à distance par le Web](remote-desktop-web-connection-reference.md)
</dt> <dt>

[**IMsRdpDevice**](imsrdpdevice.md)
</dt> </dl>

 

