---
title: Interface IVMAccountant (VPCCOMInterfaces. h)
description: Permet d’accéder aux informations relatives à la comptabilité pour un ordinateur virtuel.
ms.assetid: 047fa4c9-cb2e-4830-bab8-0513247eff9b
keywords:
- Virtual PC de l’interface IVMAccountant
- IVMAccountant interface Virtual PC, Description
topic_type:
- apiref
api_name:
- IVMAccountant
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ae791ce6cd1cd401beba4ff200ffbb54213b89d642c478eca7eb3b3057b4acb4
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119473709"
---
# <a name="ivmaccountant-interface"></a>Interface IVMAccountant

\[Windows Virtual PC ne peut plus être utilisé à partir de Windows 8. Au lieu de cela, utilisez le [fournisseur WMI Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]

Permet d’accéder aux informations relatives à la comptabilité pour un ordinateur virtuel. Pour récupérer les **IVMAccountant** d’un ordinateur virtuel, utilisez la propriété [**IVMVirtualMachine :: comptable**](ivmvirtualmachine-accountant.md) .

## <a name="members"></a>Membres

L’interface **IVMAccountant** hérite de l’interface [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) . **IVMAccountant** a également les types de membres suivants :

-   [Propriétés](#properties)

### <a name="properties"></a>Propriétés

L’interface **IVMAccountant** possède les propriétés suivantes.



| Propriété                                                                        | Type d’accès          | Description                                                                                             |
|:--------------------------------------------------------------------------------|:---------------------|:--------------------------------------------------------------------------------------------------------|
| [**CPUUtilization**](ivmaccountant-cpuutilization.md)<br/>               | Lecture seule<br/> | Pourcentage d’utilisation actuelle du processeur pour cet ordinateur virtuel.<br/>                          |
| [**CPUUtilizationHistory**](ivmaccountant-cpuutilizationhistory.md)<br/> | Lecture seule<br/> | Utilisation récente du processeur de cet ordinateur virtuel (sous la forme d’un tableau de valeurs de pourcentage).<br/>       |
| [**DiskBytesRead**](ivmaccountant-diskbytesread.md)<br/>                 | Lecture seule<br/> | Nombre total d’octets lus par tous les contrôleurs de stockage pour cet ordinateur virtuel.<br/>          |
| [**DiskBytesWritten**](ivmaccountant-diskbyteswritten.md)<br/>           | Lecture seule<br/> | Nombre total d’octets écrits par tous les contrôleurs de stockage pour cet ordinateur virtuel.<br/>       |
| [**NetworkBytesReceived**](ivmaccountant-networkbytesreceived.md)<br/>   | Lecture seule<br/> | Nombre total d’octets reçus par toutes les cartes réseau virtuelles de cet ordinateur virtuel.<br/> |
| [**NetworkBytesSent**](ivmaccountant-networkbytessent.md)<br/>           | Lecture seule<br/> | Nombre total d’octets envoyés par toutes les cartes réseau virtuelles pour cet ordinateur virtuel.<br/>     |
| [**Activité**](ivmaccountant-uptime.md)<br/>                               | Lecture seule<br/> | Nombre de secondes pendant lequel l’ordinateur virtuel a été exécuté.<br/>                             |



 

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | applications de \[ bureau Windows 7 uniquement\]<br/>                                                    |
| Serveur minimal pris en charge<br/> | Aucun pris en charge<br/>                                                                     |
| Fin de la prise en charge des clients<br/>    | Windows 7<br/>                                                                          |
| Produit<br/>                  | Windows Virtual PC<br/>                                                                 |
| En-tête<br/>                   | <dl> <dt>VPCCOMInterfaces. h</dt> </dl> |
| IID<br/>                      | IID \_ IVMAccountant est défini en tant que 6376c067-7f57-4d63-b754-06e2e4f51d73<br/>              |



 

