---
title: Interface IVMVirtualPCEvents (VPCCOMInterfaces. h)
description: Définit l’interface d’événements sortants pour l’interface IVMVirtualPC.
ms.assetid: 40ce14d8-43e4-4c72-9729-e5503d882be6
keywords:
- Virtual PC de l’interface IVMVirtualPCEvents
- IVMVirtualPCEvents interface Virtual PC, Description
topic_type:
- apiref
api_name:
- IVMVirtualPCEvents
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6c3a6fd22f75027d1424b8605e8e36e373064069
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104033101"
---
# <a name="ivmvirtualpcevents-interface"></a>Interface IVMVirtualPCEvents

\[Windows Virtual PC n’est plus disponible pour une utilisation à partir de Windows 8. Au lieu de cela, utilisez le [fournisseur WMI Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]

Définit l’interface d’événements sortants pour l’interface [**IVMVirtualPC**](ivmvirtualpc.md) . Le client implémente ces méthodes pour recevoir les événements envoyés par [**IVMVirtualPC**](ivmvirtualpc.md).

## <a name="members"></a>Membres

L’interface **IVMVirtualPCEvents** hérite de l’interface [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) . **IVMVirtualPCEvents** a également les types de membres suivants :

-   [Méthodes](#methods)

### <a name="methods"></a>Méthodes

L’interface **IVMVirtualPCEvents** possède ces méthodes.



| Méthode                                                        | Description                                                                  |
|:--------------------------------------------------------------|:-----------------------------------------------------------------------------|
| [**OnEventLogged**](ivmvirtualpcevents-oneventlogged.md)     | Reçoit une notification indiquant que Windows Virtual PC enregistre un événement.<br/>      |
| [**OnVMStateChange**](ivmvirtualpcevents-onvmstatechange.md) | Reçoit une notification indiquant que l’état d’une machine virtuelle a changé.<br/> |



 

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Applications de \[ Bureau Windows 7 uniquement\]<br/>                                                    |
| Serveur minimal pris en charge<br/> | Aucun pris en charge<br/>                                                                     |
| Fin de la prise en charge des clients<br/>    | Windows 7<br/>                                                                          |
| Produit<br/>                  | Windows Virtual PC<br/>                                                                 |
| En-tête<br/>                   | <dl> <dt>VPCCOMInterfaces. h</dt> </dl> |
| IID<br/>                      | DIID \_ IVMVirtualPCEvents est défini comme efed1ef1-3c09-41f7-a9c2-7e29fa286c9d<br/>        |



 

