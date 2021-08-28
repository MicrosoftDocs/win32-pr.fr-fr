---
title: Interface IMsRdpDriveCollection
description: Représente une collection d’objets Drive.
ms.assetid: 26926b85-021d-4678-845f-93ba62b2b4a3
ms.tgt_platform: multiple
keywords:
- Services Bureau à distance de l’interface IMsRdpDriveCollection
- Services Bureau à distance de l’interface IMsRdpDriveCollection, Description
topic_type:
- apiref
api_name:
- IMsRdpDriveCollection
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1d9f85a491da97fe0093d9b02e8ceda59c3562f237d8678323078e2613250f28
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120125629"
---
# <a name="imsrdpdrivecollection-interface"></a>Interface IMsRdpDriveCollection

Représente une collection d’objets Drive.

## <a name="members"></a>Membres

L’interface **IMsRdpDriveCollection** hérite de l’interface [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) . **IMsRdpDriveCollection** a également les types de membres suivants :

-   [Méthodes](#methods)
-   [Propriétés](#properties)

### <a name="methods"></a>Méthodes

L’interface **IMsRdpDriveCollection** possède ces méthodes.



| Méthode                                                     | Description                                                 |
|:-----------------------------------------------------------|:------------------------------------------------------------|
| [**RescanDrives**](imsrdpdrivecollection-rescandrives.md) | Actualise la liste des objets dans la collection.<br/> |



 

### <a name="properties"></a>Propriétés

L’interface **IMsRdpDriveCollection** possède les propriétés suivantes.



| Propriété                                                              | Type d’accès          | Description                                                  |
|:----------------------------------------------------------------------|:---------------------|:-------------------------------------------------------------|
| [**DriveByIndex**](imsrdpdrivecollection-drivebyindex.md)<br/> | Lecture seule<br/> | Récupère le lecteur à l’index spécifié.<br/>       |
| [**DriveCount**](imsrdpdrivecollection-drivecount.md)<br/>     | Lecture seule<br/> | Récupère le nombre d’objets dans la collection.<br/> |



 

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows Vista<br/>                                                                 |
| Serveur minimal pris en charge<br/> | Windows Server 2008<br/>                                                           |
| Bibliothèque de types<br/>             | <dl> <dt>MsTscAx.dll</dt> </dl>   |
| DLL<br/>                      | <dl> <dt>MsTscAx.dll</dt> </dl>   |
| IID<br/>                      | IID \_ IMsRdpDriveCollection est défini en tant que 7ff17599-da2c-4677-ad35-f60c04fe1585<br/> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Référence Connexion Bureau à distance par le Web](remote-desktop-web-connection-reference.md)
</dt> <dt>

[**IMsRdpDrive**](imsrdpdrive.md)
</dt> </dl>

 

