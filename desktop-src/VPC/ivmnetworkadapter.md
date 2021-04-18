---
title: Interface IVMNetworkAdapter (VPCCOMInterfaces. h)
description: Sert d’interface à une carte d’interface réseau virtuelle.
ms.assetid: df050706-09be-47d1-9ae1-1eb0e1836d64
keywords:
- Virtual PC de l’interface IVMNetworkAdapter
- IVMNetworkAdapter interface Virtual PC, Description
topic_type:
- apiref
api_name:
- IVMNetworkAdapter
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 74a0ccf722715896743129b6666609bd8a88df3f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104384748"
---
# <a name="ivmnetworkadapter-interface"></a>Interface IVMNetworkAdapter

\[Windows Virtual PC n’est plus disponible pour une utilisation à partir de Windows 8. Au lieu de cela, utilisez le [fournisseur WMI Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]

Sert d’interface à une carte d’interface réseau (NIC) virtuelle. Il permet de configurer la façon dont une machine virtuelle est en réseau. Les cartes d’interface réseau peuvent être ajoutées et supprimées à l’aide de [**IVMVirtualMachine :: AddNetworkAdapter**](ivmvirtualmachine-addnetworkadapter.md) et [**IVMVirtualMachine :: RemoveNetworkAdapter**](ivmvirtualmachine-removenetworkadapter.md). Vous pouvez également récupérer un objet **IVMNetworkAdapter** à partir de la collection [**IVMNetworkAdapterCollection**](ivmnetworkadaptercollection.md) retournée par les propriétés [**IVMVirtualMachine :: NetworkAdapters**](ivmvirtualmachine-networkadapters.md) ou [**IVMVirtualNetwork :: NetworkAdapters**](ivmvirtualnetwork-networkadapters.md) .

## <a name="members"></a>Membres

L’interface **IVMNetworkAdapter** hérite de l’interface [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) . **IVMNetworkAdapter** a également les types de membres suivants :

-   [Méthodes](#methods)
-   [Propriétés](#properties)

### <a name="methods"></a>Méthodes

L’interface **IVMNetworkAdapter** possède ces méthodes.



| Méthode                                                                         | Description                                                                 |
|:-------------------------------------------------------------------------------|:----------------------------------------------------------------------------|
| [**\_IDENTIFI**](ivmnetworkadapter--id.md)                                          | Récupère l’identificateur interne de cette interface réseau.<br/>     |
| [**AttachToVirtualNetwork**](ivmnetworkadapter-attachtovirtualnetwork.md)     | Attache l’interface réseau au réseau virtuel spécifié.<br/> |
| [**DetachFromVirtualNetwork**](ivmnetworkadapter-detachfromvirtualnetwork.md) | Détache l’interface réseau de son réseau virtuel.<br/>         |



 

### <a name="properties"></a>Propriétés

L’interface **IVMNetworkAdapter** possède les propriétés suivantes.



| Propriété                                                                                  | Type d’accès           | Description                                                                 |
|:------------------------------------------------------------------------------------------|:----------------------|:----------------------------------------------------------------------------|
| [**EthernetAddress**](ivmnetworkadapter-ethernetaddress.md)<br/>                   | Lecture/écriture<br/> | Adresse Ethernet (MAC) de l’interface réseau.<br/>             |
| [**IsEthernetAddressDynamic**](ivmnetworkadapter-isethernetaddressdynamic.md)<br/> | Lecture/écriture<br/> | Indique si l’adresse Ethernet est générée dynamiquement.<br/> |
| [**VirtualMachine**](ivmnetworkadapter-virtualmachine.md)<br/>                     | Lecture seule<br/>  | Ordinateur virtuel associé à cette interface réseau.<br/>      |
| [**VirtualNetwork**](ivmnetworkadapter-virtualnetwork.md)<br/>                     | Lecture seule<br/>  | Réseau virtuel auquel l’interface réseau est attachée.<br/>  |



 

## <a name="remarks"></a>Notes

L’adresse Ethernet par défaut pour une interface réseau est « 00-00-00-00-00-00 », qui est considérée comme une adresse Ethernet non valide par la plupart des systèmes d’exploitation. Si [**IsEthernetAddressDynamic**](ivmnetworkadapter-isethernetaddressdynamic.md) a la valeur **false**, [**EthernetAddress**](ivmnetworkadapter-ethernetaddress.md) doit être initialisé avec une adresse réseau Ethernet valide.

Les procédures suivantes expliquent comment utiliser l’interface **IVMNetworkAdapter** .

**Pour attacher une carte réseau virtuelle à une carte réseau d’ordinateur hôte**

-   Les cartes réseau virtuelles (invitées) ne sont pas directement attachées à une carte réseau d’ordinateur hôte. Au lieu de cela, la carte d’interface réseau virtuelle est attachée à un réseau virtuel associé à une carte réseau d’ordinateur hôte. Pour plus d’informations sur la configuration des réseaux virtuels, consultez [**IVMVirtualNetwork**](ivmvirtualnetwork.md). Pour attacher la carte réseau virtuelle à un réseau virtuel, utilisez la méthode [**AttachToVirtualNetwork**](ivmnetworkadapter-attachtovirtualnetwork.md) .

**Pour déconnecter une carte réseau virtuelle du réseau virtuel**

-   La méthode [**DetachFromVirtualNetwork**](ivmnetworkadapter-detachfromvirtualnetwork.md) détachera la carte réseau virtuelle du réseau virtuel. Après l’appel de cette fonction, la propriété [**virtualnetwork**](ivmnetworkadapter-virtualnetwork.md) retourne un ID de réseau virtuel qui n’est pas valide.

**Pour supprimer une carte réseau virtuelle d’un ordinateur virtuel si vous avez l’objet de carte réseau virtuelle**

1.  Récupérez l’ordinateur virtuel associé à la carte réseau virtuelle à l’aide de la propriété [**VirtualMachine**](ivmnetworkadapter-virtualmachine.md) .
2.  Utilisez l’objet en cours en tant que paramètre de la méthode [**IVMVirtualMachine :: RemoveNetworkAdapter**](ivmvirtualmachine-removenetworkadapter.md) .

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Applications de \[ Bureau Windows 7 uniquement\]<br/>                                                    |
| Serveur minimal pris en charge<br/> | Aucun pris en charge<br/>                                                                     |
| Fin de la prise en charge des clients<br/>    | Windows 7<br/>                                                                          |
| Produit<br/>                  | Windows Virtual PC<br/>                                                                 |
| En-tête<br/>                   | <dl> <dt>VPCCOMInterfaces. h</dt> </dl> |
| IID<br/>                      | IID \_ IVMNetworkAdapter est défini en tant que e32e4165-22b8-4DC0-8d57-850171ae207a<br/>          |



 

