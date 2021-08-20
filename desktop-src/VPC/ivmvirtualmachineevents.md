---
title: Interface IVMVirtualMachineEvents (VPCCOMInterfaces. h)
description: Définit l’interface d’événements sortants pour l’interface IVMVirtualMachine.
ms.assetid: 52901a95-0f4f-4503-97c5-1459179feeb8
keywords:
- Virtual PC de l’interface IVMVirtualMachineEvents
- IVMVirtualMachineEvents interface Virtual PC, Description
topic_type:
- apiref
api_name:
- IVMVirtualMachineEvents
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c6686585333f33d4732284ab448a82ac722fea03315b08aaa276f2eeabaf2e02
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118122619"
---
# <a name="ivmvirtualmachineevents-interface"></a>Interface IVMVirtualMachineEvents

\[Windows Virtual PC ne peut plus être utilisé à partir de Windows 8. Au lieu de cela, utilisez le [fournisseur WMI Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]

Définit l’interface d’événements sortants pour l’interface [**IVMVirtualMachine**](ivmvirtualmachine.md) . Le client implémente ces méthodes pour recevoir les événements envoyés par [**IVMVirtualMachine**](ivmvirtualmachine.md).

## <a name="members"></a>Membres

L’interface **IVMVirtualMachineEvents** hérite de l’interface [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) . **IVMVirtualMachineEvents** a également les types de membres suivants :

-   [Méthodes](#methods)

### <a name="methods"></a>Méthodes

L’interface **IVMVirtualMachineEvents** possède ces méthodes.



| Méthode                                                                                   | Description                                                                                                                                     |
|:-----------------------------------------------------------------------------------------|:------------------------------------------------------------------------------------------------------------------------------------------------|
| [**OnAdditionsAvailable**](ivmvirtualmachineevents-onadditionsavailable.md)             | Reçoit une notification indiquant que les composants d’intégration sont disponibles sur une machine virtuelle.<br/>                                                |
| [**OnAdditionsUninstalled**](ivmvirtualmachineevents-onadditionsuninstalled.md)         | Reçoit une notification indiquant que les composants d’intégration sont désinstallés sur une machine virtuelle.<br/>                                              |
| [**OnConfigurationChanged**](ivmvirtualmachineevents-onconfigurationchanged.md)         | Reçoit une notification indiquant qu’une valeur de la configuration de cet ordinateur virtuel a changé.<br/>                                        |
| [**OnDiskOutOfSpace**](ivmvirtualmachineevents-ondiskoutofspace.md)                     | Reçoit une notification indiquant qu’un disque requis pour un ordinateur virtuel n’a plus d’espace et que l’ordinateur virtuel ne peut pas s’exécuter.<br/>           |
| [**OnEnhancedVideoModeChanged**](ivmvirtualmachineevents-onenhancedvideomodechanged.md) | Reçoit une notification indiquant que la prise en charge d’un ordinateur virtuel pour le mode vidéo amélioré a changé.<br/>                                          |
| [**OnGuestLogoff**](ivmvirtualmachineevents-onguestlogoff.md)                           | Reçoit une notification indiquant qu’un utilisateur s’est déconnecté du système d’exploitation invité.<br/>                                                    |
| [**OnGuestShutdown**](ivmvirtualmachineevents-onguestshutdown.md)                       | Reçoit une notification indiquant que le système d’exploitation invité s’est arrêté.<br/>                                                                     |
| [**OnHeartbeatStopped**](ivmvirtualmachineevents-onheartbeatstopped.md)                 | Reçoit une notification indiquant que la pulsation d’une machine virtuelle s’est arrêtée. Cela indique généralement que le système d’exploitation invité s’est arrêté.<br/> |
| [**OnRequestShutdown**](ivmvirtualmachineevents-onrequestshutdown.md)                   | Reçoit une notification indiquant qu’une demande d’arrêt a été effectuée.<br/>                                                                         |
| [**OnReset**](ivmvirtualmachineevents-onreset.md)                                       | Reçoit une notification indiquant qu’un ordinateur virtuel a été réinitialisé.<br/>                                                                         |
| [**OnStateChange**](ivmvirtualmachineevents-onstatechange.md)                           | Reçoit une notification indiquant que l’état d’une machine virtuelle a changé.<br/>                                                                    |
| [**OnTripleFault**](ivmvirtualmachineevents-ontriplefault.md)                           | Reçoit une notification indiquant qu’un ordinateur virtuel a une erreur triple.<br/>                                                                     |



 

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | applications de \[ bureau Windows 7 uniquement\]<br/>                                                    |
| Serveur minimal pris en charge<br/> | Aucun pris en charge<br/>                                                                     |
| Fin de la prise en charge des clients<br/>    | Windows 7<br/>                                                                          |
| Produit<br/>                  | Windows Virtual PC<br/>                                                                 |
| En-tête<br/>                   | <dl> <dt>VPCCOMInterfaces. h</dt> </dl> |
| IID<br/>                      | DIID \_ IVMVirtualMachineEvents est défini comme 9d84f560-bb67-4961-BD12-a4da780c67e4<br/>   |



 

