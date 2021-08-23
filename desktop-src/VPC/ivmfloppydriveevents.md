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
ms.openlocfilehash: 53cd275c45e23de1bb437b4c233ff64118952afae76e7c6b9bc9366facf4fe8b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119653509"
---
# <a name="ivmfloppydriveevents-interface"></a>Interface IVMFloppyDriveEvents

\[Windows Virtual PC ne peut plus être utilisé à partir de Windows 8. Au lieu de cela, utilisez le [fournisseur WMI Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]

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
| Client minimal pris en charge<br/> | applications de \[ bureau Windows 7 uniquement\]<br/>                                                    |
| Serveur minimal pris en charge<br/> | Aucun pris en charge<br/>                                                                     |
| Fin de la prise en charge des clients<br/>    | Windows 7<br/>                                                                          |
| Produit<br/>                  | Windows Virtual PC<br/>                                                                 |
| En-tête<br/>                   | <dl> <dt>VPCCOMInterfaces. h</dt> </dl> |
| IID<br/>                      | DIID \_ IVMFloppyDriveEvents est défini comme a9ed3401-4e09-4177-86ec-a13bf9fa7d4e<br/>      |



 

