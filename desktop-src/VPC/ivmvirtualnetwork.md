---
title: Interface IVMVirtualNetwork (VPCCOMInterfaces. h)
description: Définit un réseau virtuel.
ms.assetid: 1ddafc33-05d4-45fb-924d-9830288aa240
keywords:
- Virtual PC de l’interface IVMVirtualNetwork
- IVMVirtualNetwork interface Virtual PC, Description
topic_type:
- apiref
api_name:
- IVMVirtualNetwork
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a9caf5accb0add3354953d09e74a0893e2392deee7720b7a2cba0136b3f4b7c2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118592584"
---
# <a name="ivmvirtualnetwork-interface"></a>Interface IVMVirtualNetwork

\[Windows Virtual PC ne peut plus être utilisé à partir de Windows 8. Au lieu de cela, utilisez le [fournisseur WMI Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]

Définit un réseau virtuel. Les objets **IVMVirtualNetwork** sont retournés à partir de la méthode [**IVMVirtualPC**](ivmvirtualpc.md) [**FindVirtualNetwork**](ivmvirtualpc-findvirtualnetwork.md). Vous pouvez également récupérer un objet **IVMVirtualNetwork** à partir de l’objet [**IVMVirtualNetworkCollection**](ivmvirtualnetworkcollection.md) retourné à partir de la propriété [**IVMVirtualPC :: VirtualNetworks**](ivmvirtualpc-virtualnetworks.md) .

Un réseau virtuel se compose d’un commutateur virtuel qui effectue tout le routage interne et plusieurs connexions « connectées » au commutateur virtuel. Ces connexions peuvent être une connexion d’hôte externe réelle, un « réseau interne » ou une mise en réseau partagée (NAT).

## <a name="members"></a>Membres

L’interface **IVMVirtualNetwork** hérite de l’interface [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) . **IVMVirtualNetwork** a également les types de membres suivants :

-   [Méthodes](#methods)
-   [Propriétés](#properties)

### <a name="methods"></a>Méthodes

L’interface **IVMVirtualNetwork** possède ces méthodes.



| Méthode                                | Description                                                          |
|:--------------------------------------|:---------------------------------------------------------------------|
| [**\_ID**](ivmvirtualnetwork--id.md) | Récupère l’identificateur interne du réseau virtuel.<br/> |



 

### <a name="properties"></a>Propriétés

L’interface **IVMVirtualNetwork** possède les propriétés suivantes.



| Propriété                                                                | Type d’accès          | Description                                                                    |
|:------------------------------------------------------------------------|:---------------------|:-------------------------------------------------------------------------------|
| [**HostAdapter**](ivmvirtualnetwork-hostadapter.md)<br/>         | Lecture seule<br/> | Nom de l’adaptateur auquel le réseau virtuel est connecté.<br/>  |
| [**MediaType**](/previous-versions/windows/desktop/legacy/dd796707(v=vs.85))<br/>             | Lecture seule<br/> | Détermine si l’instance de réseau virtuel est sans fil ou non.<br/> |
| [**Nom**](ivmvirtualnetwork-name.md)<br/>                       | Lecture seule<br/> | Nom unique de l’instance de réseau virtuel.<br/>                    |
| [**NetworkAdapters**](ivmvirtualnetwork-networkadapters.md)<br/> | Lecture seule<br/> | Collection énumérable de cartes réseau attachées au réseau virtuel.<br/>   |



 

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | applications de \[ bureau Windows 7 uniquement\]<br/>                                                    |
| Serveur minimal pris en charge<br/> | Aucun pris en charge<br/>                                                                     |
| Fin de la prise en charge des clients<br/>    | Windows 7<br/>                                                                          |
| Produit<br/>                  | Windows Virtual PC<br/>                                                                 |
| En-tête<br/>                   | <dl> <dt>VPCCOMInterfaces. h</dt> </dl> |
| IID<br/>                      | IID \_ IVMVirtualNetwork est défini en tant que 431cb7a1-2469-4563-b94e-38b987adca63<br/>          |



 

