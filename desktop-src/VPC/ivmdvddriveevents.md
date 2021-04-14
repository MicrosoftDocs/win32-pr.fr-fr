---
title: Interface IVMDVDDriveEvents (VPCCOMInterfaces. h)
description: Définit l’interface d’événements sortants pour l’interface IVMDVDDrive.
ms.assetid: aa68fb6f-032d-4322-8553-b1e840ae63b8
keywords:
- Virtual PC de l’interface IVMDVDDriveEvents
- IVMDVDDriveEvents interface Virtual PC, Description
topic_type:
- apiref
api_name:
- IVMDVDDriveEvents
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4b301a423f5272288c12a900d0fbd19c0a5d5170
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104466838"
---
# <a name="ivmdvddriveevents-interface"></a>Interface IVMDVDDriveEvents

\[Windows Virtual PC n’est plus disponible pour une utilisation à partir de Windows 8. Au lieu de cela, utilisez le [fournisseur WMI Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]

Définit l’interface d’événements sortants pour l’interface [**IVMDVDDrive**](ivmdvddrive.md) .

## <a name="members"></a>Membres

L’interface **IVMDVDDriveEvents** hérite de l’interface [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) . **IVMDVDDriveEvents** a également les types de membres suivants :

-   [Méthodes](#methods)

### <a name="methods"></a>Méthodes

L’interface **IVMDVDDriveEvents** possède ces méthodes.



| Méthode                                                   | Description                                                                   |
|:---------------------------------------------------------|:------------------------------------------------------------------------------|
| [**OnMediaEject**](ivmdvddriveevents-onmediaeject.md)   | Reçoit une notification indiquant que le média a été éjecté du lecteur.<br/>  |
| [**OnMediaInsert**](ivmdvddriveevents-onmediainsert.md) | Reçoit une notification indiquant que le média a été inséré dans le lecteur.<br/> |



 

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Applications de \[ Bureau Windows 7 uniquement\]<br/>                                                    |
| Serveur minimal pris en charge<br/> | Aucun pris en charge<br/>                                                                     |
| Fin de la prise en charge des clients<br/>    | Windows 7<br/>                                                                          |
| Produit<br/>                  | Windows Virtual PC<br/>                                                                 |
| En-tête<br/>                   | <dl> <dt>VPCCOMInterfaces. h</dt> </dl> |
| IID<br/>                      | DIID \_ IVMDVDDriveEvents est défini comme c2a7d8e9-E76C-4EB8-94f7-71a5122d249b<br/>         |



 

