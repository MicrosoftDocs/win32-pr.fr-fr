---
title: Interface IVMDVDDrive (VPCCOMInterfaces. h)
description: Contrôle un lecteur de CD-ROM ou de DVD-ROM au sein d’un ordinateur virtuel. IVMDVDDrive peut informer les clients des événements à l’aide de l’interface sortante IVMDVDDriveEvents.
ms.assetid: 0900b3a8-ba52-4c26-bd96-b37334d6d03c
keywords:
- Virtual PC de l’interface IVMDVDDrive
- IVMDVDDrive interface Virtual PC, Description
topic_type:
- apiref
api_name:
- IVMDVDDrive
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 951213923f74f8425fc4d9eaec85e76f7481eeb9
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104032996"
---
# <a name="ivmdvddrive-interface"></a>Interface IVMDVDDrive

\[Windows Virtual PC n’est plus disponible pour une utilisation à partir de Windows 8. Au lieu de cela, utilisez le [fournisseur WMI Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]

Contrôle un lecteur de CD-ROM ou de DVD-ROM au sein d’un ordinateur virtuel. **IVMDVDDrive** peut informer les clients des événements à l’aide de l’interface sortante [**IVMDVDDriveEvents**](ivmdvddriveevents.md) .

Vous pouvez ajouter un nouveau lecteur de CD-ROM ou de DVD-ROM à une machine virtuelle à l’aide de la méthode [**IVMVirtualMachine :: AddDVDROMDrive**](ivmvirtualmachine-adddvdromdrive.md) . Vous pouvez supprimer un lecteur de CD-ROM ou de DVD-ROM existant d’une machine virtuelle à l’aide de la méthode [**IVMVirtualMachine :: RemoveDVDROMDrive**](ivmvirtualmachine-removedvdromdrive.md) . Vous pouvez récupérer un objet **IVMDVDDrive** à partir de l’objet [**IVMDVDDriveCollection**](ivmdvddrivecollection.md) retourné à partir de la propriété [**IVMVirtualMachine ::D vdromdrives**](ivmvirtualmachine-dvdromdrives.md) .

## <a name="members"></a>Membres

L’interface **IVMDVDDrive** hérite de l’interface [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) . **IVMDVDDrive** a également les types de membres suivants :

-   [Méthodes](#methods)
-   [Propriétés](#properties)

### <a name="methods"></a>Méthodes

L’interface **IVMDVDDrive** possède ces méthodes.



| Méthode                                                   | Description                                                                             |
|:---------------------------------------------------------|:----------------------------------------------------------------------------------------|
| [**AttachHostDrive**](ivmdvddrive-attachhostdrive.md)   | Attache un lecteur hôte au lecteur de DVD de l’ordinateur virtuel.<br/>           |
| [**AttachImage**](ivmdvddrive-attachimage.md)           | Attache une image ISO au lecteur de DVD de l’ordinateur virtuel.<br/>           |
| [**ReleaseHostDrive**](ivmdvddrive-releasehostdrive.md) | Libère un lecteur hôte capturé à partir du lecteur de DVD.<br/>                           |
| [**ReleaseImage**](ivmdvddrive-releaseimage.md)         | Libère une image ISO capturée à partir du lecteur de DVD.<br/>                            |
| [**SetBusLocation**](ivmdvddrive-setbuslocation.md)     | Attache le lecteur de DVD à l’emplacement de bus spécifié sur l’ordinateur virtuel.<br/> |



 

### <a name="properties"></a>Propriétés

L’interface **IVMDVDDrive** possède les propriétés suivantes.



| Propriété                                                          | Type d’accès          | Description                                                                        |
|:------------------------------------------------------------------|:---------------------|:-----------------------------------------------------------------------------------|
| [**Pièce jointe**](ivmdvddrive-attachment.md)<br/>           | Lecture seule<br/> | Type de support attaché au lecteur de DVD au sein de la machine virtuelle.<br/> |
| [**BusNumber**](ivmdvddrive-busnumber.md)<br/>             | Lecture seule<br/> | Numéro de bus auquel cet appareil est attaché.<br/>                        |
| [**DeviceNumber**](ivmdvddrive-devicenumber.md)<br/>       | Lecture seule<br/> | Numéro de l’appareil auquel ce lecteur est attaché.<br/>                      |
| [**HostDriveLetter**](ivmdvddrive-hostdriveletter.md)<br/> | Lecture seule<br/> | Lettre du lecteur hôte défini pour cet appareil.<br/>                       |
| [**ImageFile**](ivmdvddrive-imagefile.md)<br/>             | Lecture seule<br/> | Chemin d’accès complet du jeu de fichiers image pour cet appareil.<br/>                    |



 

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Applications de \[ Bureau Windows 7 uniquement\]<br/>                                                    |
| Serveur minimal pris en charge<br/> | Aucun pris en charge<br/>                                                                     |
| Fin de la prise en charge des clients<br/>    | Windows 7<br/>                                                                          |
| Produit<br/>                  | Windows Virtual PC<br/>                                                                 |
| En-tête<br/>                   | <dl> <dt>VPCCOMInterfaces. h</dt> </dl> |
| IID<br/>                      | IID \_ IVMDVDDrive est défini en tant que b96328f6-6732-437D-A00D-ffa47e43971c<br/>                |



 

