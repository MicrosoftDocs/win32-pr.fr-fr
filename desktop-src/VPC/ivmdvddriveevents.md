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
ms.openlocfilehash: dcb34bf77b6692c90977262ac7e2177019169e3195ee44415a0693102e6d15ea
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119136792"
---
# <a name="ivmdvddriveevents-interface"></a>Interface IVMDVDDriveEvents

\[Windows Virtual PC ne peut plus être utilisé à partir de Windows 8. Au lieu de cela, utilisez le [fournisseur WMI Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]

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
| Client minimal pris en charge<br/> | applications de \[ bureau Windows 7 uniquement\]<br/>                                                    |
| Serveur minimal pris en charge<br/> | Aucun pris en charge<br/>                                                                     |
| Fin de la prise en charge des clients<br/>    | Windows 7<br/>                                                                          |
| Produit<br/>                  | Windows Virtual PC<br/>                                                                 |
| En-tête<br/>                   | <dl> <dt>VPCCOMInterfaces. h</dt> </dl> |
| IID<br/>                      | DIID \_ IVMDVDDriveEvents est défini comme c2a7d8e9-E76C-4EB8-94f7-71a5122d249b<br/>         |



 

