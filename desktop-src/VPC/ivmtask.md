---
title: Interface IVMTask (VPCCOMInterfaces. h)
description: Utilisez l’interface IVMTask pour surveiller et contrôler les tâches asynchrones pour différentes méthodes COM.
ms.assetid: 9b593444-80f5-43e9-9b95-1a2150c66efd
keywords:
- Virtual PC de l’interface IVMTask
- IVMTask interface Virtual PC, Description
topic_type:
- apiref
api_name:
- IVMTask
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a8e1d519471fe5b1fc32cb6365d1139243c85538
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104508978"
---
# <a name="ivmtask-interface"></a>Interface IVMTask

\[Windows Virtual PC n’est plus disponible pour une utilisation à partir de Windows 8. Au lieu de cela, utilisez le [fournisseur WMI Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]

Utilisez l’interface **IVMTask** pour surveiller et contrôler les tâches asynchrones pour différentes méthodes com.

## <a name="members"></a>Membres

L’interface **IVMTask** hérite de l’interface [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) . **IVMTask** a également les types de membres suivants :

-   [Méthodes](#methods)
-   [Propriétés](#properties)

### <a name="methods"></a>Méthodes

L’interface **IVMTask** possède ces méthodes.



| Méthode                                                 | Description                                                                                 |
|:-------------------------------------------------------|:--------------------------------------------------------------------------------------------|
| [**Annuler**](ivmtask-cancel.md)                       | Annule la tâche.<br/>                                                                |
| [**WaitForCompletion**](ivmtask-waitforcompletion.md) | Attend que la tâche soit terminée ou que l’intervalle de délai d’attente spécifié soit écoulé.<br/> |



 

### <a name="properties"></a>Propriétés

L’interface **IVMTask** possède les propriétés suivantes.



| Propriété                                                        | Type d’accès          | Description                                                        |
|:----------------------------------------------------------------|:---------------------|:-------------------------------------------------------------------|
| [**Description**](ivmtask-description.md)<br/>           | Lecture seule<br/> | Une description de la tâche.<br/>                              |
| [**Error**](ivmtask-error.md)<br/>                       | Lecture seule<br/> | Erreur enregistrée pour cette tâche.<br/>                       |
| [**ErrorDescription**](ivmtask-errordescription.md)<br/> | Lecture seule<br/> | Description d’erreur localisée enregistrée pour cette tâche.<br/> |
| [**IDENTIFI**](ivmtask-id.md)<br/>                             | Lecture seule<br/> | Identificateur unique pour cette tâche.<br/>                      |
| [**IsCancelable**](ivmtask-iscancelable.md)<br/>         | Lecture seule<br/> | Indique si la tâche peut être annulée.<br/>             |
| [**IsComplete**](ivmtask-iscomplete.md)<br/>             | Lecture seule<br/> | Indique si la tâche est terminée.<br/>               |
| [**PercentCompleted**](ivmtask-percentcompleted.md)<br/> | Lecture seule<br/> | Pourcentage d’achèvement de la tâche.<br/>                  |
| [**Venir**](ivmtask-result.md)<br/>                     | Lecture seule<br/> | Résultat de la tâche.<br/>                                 |



 

## <a name="remarks"></a>Notes

Un objet **IVMTask** est retourné par des méthodes qui peuvent éventuellement nécessiter un temps considérable. Cela permet à l’application de surveiller la progression de l’opération souhaitée sans la forcer à bloquer une exécution supplémentaire en attendant la fin de l’opération.

Les méthodes suivantes retournent un objet **IVMTask** qui peut être utilisé pour suivre la progression :

-   [**IVMGuestOS :: Logoff**](ivmguestos-logoff.md)
-   [**IVMGuestOS :: Restart**](ivmguestos-restart.md)
-   [**IVMGuestOS :: Shutdown**](ivmguestos-shutdown.md)
-   [**IVMHardDisk :: compact**](ivmharddisk-compact.md)
-   [**IVMHardDisk :: Convert**](ivmharddisk-convert.md)
-   [**IVMHardDisk :: Merge**](ivmharddisk-merge.md)
-   [**IVMHardDisk::MergeTo**](ivmharddisk-mergeto.md)
-   [**IVMVirtualMachine::MergeUndoDisks**](ivmvirtualmachine-mergeundodisks.md)
-   [**IVMVirtualMachine :: Reset**](ivmvirtualmachine-reset.md)
-   [**IVMVirtualMachine :: enregistrer**](ivmvirtualmachine-save.md)
-   [**IVMVirtualMachine :: Startup**](ivmvirtualmachine-startup.md)
-   [**IVMVirtualMachine :: Startup2**](ivmvirtualmachine-startup2.md)
-   [**IVMVirtualMachine::TurnOff**](ivmvirtualmachine-turnoff.md)
-   [**IVMVirtualPC::CreateDifferencingVirtualHardDisk**](ivmvirtualpc-createdifferencingvirtualharddisk.md)
-   [**IVMVirtualPC::CreateDynamicVirtualHardDisk**](ivmvirtualpc-createdynamicvirtualharddisk.md)
-   [**IVMVirtualPC::CreateFixedVirtualHardDisk**](ivmvirtualpc-createfixedvirtualharddisk.md)

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Applications de \[ Bureau Windows 7 uniquement\]<br/>                                                    |
| Serveur minimal pris en charge<br/> | Aucun pris en charge<br/>                                                                     |
| Fin de la prise en charge des clients<br/>    | Windows 7<br/>                                                                          |
| Produit<br/>                  | Windows Virtual PC<br/>                                                                 |
| En-tête<br/>                   | <dl> <dt>VPCCOMInterfaces. h</dt> </dl> |
| IID<br/>                      | IID \_ IVMTask est défini en tant que ab72b222-6e9c-48ae-aa54-85e3e635767c<br/>                    |



 

