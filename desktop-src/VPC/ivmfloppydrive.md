---
title: Interface IVMFloppyDrive (VPCCOMInterfaces. h)
description: Contrôle un lecteur de disquette au sein d’une machine virtuelle.
ms.assetid: b652182a-27ae-4390-81b1-b644a82924df
keywords:
- Virtual PC de l’interface IVMFloppyDrive
- IVMFloppyDrive interface Virtual PC, Description
topic_type:
- apiref
api_name:
- IVMFloppyDrive
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bab1034bc56c5fe10bb12941bd99309e13e22dca
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103942681"
---
# <a name="ivmfloppydrive-interface"></a>Interface IVMFloppyDrive

\[Windows Virtual PC n’est plus disponible pour une utilisation à partir de Windows 8. Au lieu de cela, utilisez le [fournisseur WMI Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]

Contrôle un lecteur de disquette au sein d’une machine virtuelle. **IVMFloppyDrive** peut informer les clients des événements à l’aide de l’interface sortante [**IVMFloppyDriveEvents**](ivmfloppydriveevents.md) . Vous pouvez récupérer un objet **IVMFloppyDrive** à partir de l’objet [**IVMFloppyDriveCollection**](ivmfloppydrivecollection.md) retourné à partir de la propriété [**IVMVirtualMachine :: FloppyDrives**](ivmvirtualmachine-floppydrives.md) .

## <a name="members"></a>Membres

L’interface **IVMFloppyDrive** hérite de l’interface [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) . **IVMFloppyDrive** a également les types de membres suivants :

-   [Méthodes](#methods)
-   [Propriétés](#properties)

### <a name="methods"></a>Méthodes

L’interface **IVMFloppyDrive** possède ces méthodes.



| Méthode                                                      | Description                                                                                  |
|:------------------------------------------------------------|:---------------------------------------------------------------------------------------------|
| [**AttachHostDrive**](ivmfloppydrive-attachhostdrive.md)   | Attache un lecteur physique sur l’ordinateur hôte au lecteur de disquette dans l’ordinateur virtuel.<br/> |
| [**AttachImage**](ivmfloppydrive-attachimage.md)           | Attache une image de support de disquette sur l’ordinateur hôte au lecteur de disquette.<br/>                    |
| [**ReleaseHostDrive**](ivmfloppydrive-releasehostdrive.md) | Libère un lecteur physique sur l’ordinateur hôte à partir du lecteur de disquette.<br/>                      |
| [**ReleaseImage**](ivmfloppydrive-releaseimage.md)         | Libère une image de support de disquette sur l’ordinateur hôte à partir du lecteur de disquette.<br/>                  |



 

### <a name="properties"></a>Propriétés

L’interface **IVMFloppyDrive** possède les propriétés suivantes.



| Propriété                                                             | Type d’accès          | Description                                                                               |
|:---------------------------------------------------------------------|:---------------------|:------------------------------------------------------------------------------------------|
| [**Pièce jointe**](ivmfloppydrive-attachment.md)<br/>           | Lecture seule<br/> | Type de support attaché au lecteur de disquette au sein de la machine virtuelle.<br/>     |
| [**DriveNumber**](ivmfloppydrive-drivenumber.md)<br/>         | Lecture seule<br/> | Index de base zéro du contrôleur auquel ce lecteur de disquette est attaché.<br/> |
| [**HostDriveLetter**](ivmfloppydrive-hostdriveletter.md)<br/> | Lecture seule<br/> | Lettre du lecteur hôte auquel le lecteur de disquette est attaché.<br/>            |
| [**ImageFile**](ivmfloppydrive-imagefile.md)<br/>             | Lecture seule<br/> | Chemin d’accès complet du fichier image auquel le lecteur de disquette est attaché.<br/>         |



 

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Applications de \[ Bureau Windows 7 uniquement\]<br/>                                                    |
| Serveur minimal pris en charge<br/> | Aucun pris en charge<br/>                                                                     |
| Fin de la prise en charge des clients<br/>    | Windows 7<br/>                                                                          |
| Produit<br/>                  | Windows Virtual PC<br/>                                                                 |
| En-tête<br/>                   | <dl> <dt>VPCCOMInterfaces. h</dt> </dl> |
| IID<br/>                      | IID \_ IVMFloppyDrive est défini en tant que 661abee6-112a-4ED9-babf-3c874969f10e<br/>             |



 

