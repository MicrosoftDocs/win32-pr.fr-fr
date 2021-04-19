---
description: Signale l’état d’intégrité d’une application qui s’exécute sur un ordinateur virtuel aux composants d’intégration Hyper-V qui s’exécutent sur le même ordinateur virtuel.
ms.assetid: C463391B-669C-4CBA-9EC7-7E0ABC5A63A1
title: Interface IVmApplicationHealthMonitor
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IVmApplicationHealthMonitor
api_type:
- COM
api_location:
- VmApplicationHealthMonitor.idl
ms.openlocfilehash: ac9f6574dd8261a120e434cc0351fd07985c71a4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106534160"
---
# <a name="ivmapplicationhealthmonitor-interface"></a>Interface IVmApplicationHealthMonitor

Signale l’état d’intégrité d’une application qui s’exécute sur un ordinateur virtuel aux composants d’intégration Hyper-V qui s’exécutent sur le même ordinateur virtuel. L’état des applications en cours d’exécution sur l’ordinateur virtuel est reflété dans la valeur de la propriété **OperationalStatus** \[ 1 \] de la classe [**MSVM \_ HeartbeatComponent**](msvm-heartbeatcomponent.md) . Cette interface fournit également un moyen de réinitialiser l’ensemble de l’état de l’application accumulé dans Hyper-V.

Cette interface est implémentée par les composants d’intégration Hyper-V de Windows 8. Une instance de cette interface est obtenue en créant une instance du CLSID **397a2e5f-348C-482D-b9a3-57d383b483cd** .

## <a name="members"></a>Membres

L’interface **IVmApplicationHealthMonitor** hérite de l’interface [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) . **IVmApplicationHealthMonitor** a également les types de membres suivants :

-   [Méthodes](#methods)

### <a name="methods"></a>Méthodes

L’interface **IVmApplicationHealthMonitor** possède ces méthodes.



| Méthode                                                                                   | Description                                                                              |
|:-----------------------------------------------------------------------------------------|:-----------------------------------------------------------------------------------------|
| [**ResetAllApplicationState**](ivmapplicationhealthmonitor-resetallapplicationstate.md) | Réinitialise l’état d’intégrité de toutes les applications d’une machine virtuelle.<br/>            |
| [**SetApplicationState**](ivmapplicationhealthmonitor-setapplicationstate.md)           | Définit l’état d’intégrité d’une application qui s’exécute sur un ordinateur virtuel.<br/> |



 

## <a name="remarks"></a>Notes

Pour utiliser cet élément de programmation, les composants d’intégration Windows 8 doivent être installés sur l’ordinateur virtuel dans lequel l’application s’exécute.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Applications de \[ Bureau Windows 8 uniquement\]<br/>                                                                                                                                     |
| Serveur minimal pris en charge<br/> | Applications de bureau Windows Server 2012 \[ uniquement\]<br/>                                                                                                                           |
| Version<br/>                  | Composants d’intégration pour Windows 8<br/>                                                                                                                                |
| MIDL<br/>                      | <dl> <dt>VmApplicationHealthMonitor. idl</dt> </dl>                                                                      |
| IID<br/>                      | IID \_ IVmApplicationHealthMonitor est défini en tant que 267a0284-848f-447e-A096-5e10a1a76bca<br/> L’identificateur d’objet est défini en tant que 397a2e5f-348C-482D-b9a3-57d383b483cd<br/> |



 

