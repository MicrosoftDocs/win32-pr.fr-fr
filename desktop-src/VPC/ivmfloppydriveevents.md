---
title: Interface IVMFloppyDriveEvents (VPCCOMInterfaces. h)
description: Définit l’interface d’événements sortants pour l’interface IVMFloppyDrive. Le client implémente ces méthodes pour recevoir les événements envoyés par IVMFloppyDrive.
ms.assetid: fbb66554-f042-4891-94be-1a12b8c179c2
keywords:
- Virtual PC de l’interface IVMFloppyDriveEvents
- IVMFloppyDriveEvents interface Virtual PC, Description
topic_type:
- apiref
api_name:
- IVMFloppyDriveEvents
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5f9b799bd6227882c2991f9b310f39d38b20692d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104106060"
---
# <a name="ivmfloppydriveevents-interface"></a>Interface IVMFloppyDriveEvents

\[Windows Virtual PC n’est plus disponible pour une utilisation à partir de Windows 8. Au lieu de cela, utilisez le [fournisseur WMI Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]

Définit l’interface d’événements sortants pour l’interface [**IVMFloppyDrive**](ivmfloppydrive.md) . Le client implémente ces méthodes pour recevoir les événements envoyés par **IVMFloppyDrive**.

## <a name="members"></a>Membres

L’interface **IVMFloppyDriveEvents** hérite de l’interface [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) . **IVMFloppyDriveEvents** a également les types de membres suivants :

-   [Méthodes](#methods)

### <a name="methods"></a>Méthodes

L’interface **IVMFloppyDriveEvents** possède ces méthodes.



| Méthode                                                      | Description                                                                   |
|:------------------------------------------------------------|:------------------------------------------------------------------------------|
| [**OnMediaEject**](ivmfloppydriveevents-onmediaeject.md)   | Reçoit une notification indiquant que le média a été éjecté du lecteur.<br/>  |
| [**OnMediaInsert**](ivmfloppydriveevents-onmediainsert.md) | Reçoit une notification indiquant que le média a été inséré dans le lecteur.<br/> |



 

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Applications de \[ Bureau Windows 7 uniquement\]<br/>                                                    |
| Serveur minimal pris en charge<br/> | Aucun pris en charge<br/>                                                                     |
| Fin de la prise en charge des clients<br/>    | Windows 7<br/>                                                                          |
| Produit<br/>                  | Windows Virtual PC<br/>                                                                 |
| En-tête<br/>                   | <dl> <dt>VPCCOMInterfaces. h</dt> </dl> |
| IID<br/>                      | DIID \_ IVMFloppyDriveEvents est défini comme a9ed3401-4e09-4177-86ec-a13bf9fa7d4e<br/>      |



 

