---
title: Interface IVMHardDiskConnection (VPCCOMInterfaces. h)
description: Définit la connexion d’un disque dur au sein de la machine virtuelle.
ms.assetid: 7ba1ace5-a3af-4b97-b329-f12a0ecbf7d3
keywords:
- Virtual PC de l’interface IVMHardDiskConnection
- IVMHardDiskConnection interface Virtual PC, Description
topic_type:
- apiref
api_name:
- IVMHardDiskConnection
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7e53a092bdca26eee0c46db1d75f7fc040d5ce7e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "106518083"
---
# <a name="ivmharddiskconnection-interface"></a>Interface IVMHardDiskConnection

\[Windows Virtual PC n’est plus disponible pour une utilisation à partir de Windows 8. Au lieu de cela, utilisez le [fournisseur WMI Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]

Définit la connexion d’un disque dur au sein de la machine virtuelle. Un objet **IVMHardDiskConnection** est retourné à partir de la méthode [**IVMVirtualMachine :: AddHardDiskConnection**](ivmvirtualmachine-addharddiskconnection.md) . Vous pouvez également récupérer un objet **IVMHardDiskConnection** à partir de l’objet [**IVMHardDiskConnectionCollection**](ivmharddiskconnectioncollection.md) retourné à partir de la propriété [**IVMVirtualMachine :: HardDiskConnections**](ivmvirtualmachine-harddiskconnections.md) .

## <a name="members"></a>Membres

L’interface **IVMHardDiskConnection** hérite de l’interface [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) . **IVMHardDiskConnection** a également les types de membres suivants :

-   [Méthodes](#methods)
-   [Propriétés](#properties)

### <a name="methods"></a>Méthodes

L’interface **IVMHardDiskConnection** possède ces méthodes.



| Méthode                                                         | Description                                                           |
|:---------------------------------------------------------------|:----------------------------------------------------------------------|
| [**SetBusLocation**](ivmharddiskconnection-setbuslocation.md) | Définit l’emplacement du bus auquel ce disque dur est attaché.<br/> |



 

### <a name="properties"></a>Propriétés

L’interface **IVMHardDiskConnection** possède les propriétés suivantes.



| Propriété                                                              | Type d’accès          | Description                                                                       |
|:----------------------------------------------------------------------|:---------------------|:----------------------------------------------------------------------------------|
| [**BusNumber**](ivmharddiskconnection-busnumber.md)<br/>       | Lecture seule<br/> | Numéro de bus auquel l’image de lecteur est attachée.<br/>                   |
| [**DeviceNumber**](ivmharddiskconnection-devicenumber.md)<br/> | Lecture seule<br/> | Numéro de l’appareil auquel l’image de lecteur est attachée.<br/>                |
| [**Dur**](ivmharddiskconnection-harddisk.md)<br/>         | Lecture seule<br/> | Objet de disque dur correspondant à cette connexion.<br/>                   |
| [**UndoHardDisk**](ivmharddiskconnection-undoharddisk.md)<br/> | Lecture seule<br/> | Objet de disque dur correspondant à l’image de disque d’annulation de cette connexion.<br/> |



 

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Applications de \[ Bureau Windows 7 uniquement\]<br/>                                                    |
| Serveur minimal pris en charge<br/> | Aucun pris en charge<br/>                                                                     |
| Fin de la prise en charge des clients<br/>    | Windows 7<br/>                                                                          |
| Produit<br/>                  | Windows Virtual PC<br/>                                                                 |
| En-tête<br/>                   | <dl> <dt>VPCCOMInterfaces. h</dt> </dl> |
| IID<br/>                      | IID \_ IVMHardDiskconnection est défini en tant que aefa36a5-463a-46AE-9e6c-a1fb4e12e671<br/>      |



 

