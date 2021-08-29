---
title: Interface IVMNetworkAdapterCollection (VPCCOMInterfaces. h)
description: Définit une collection de cartes d’interface réseau virtuelles. Pour obtenir un objet IVMNetworkAdapterCollection, utilisez les propriétés IVMVirtualMachine NetworkAdapters, IVMVirtualNetwork NetworkAdapters et IVMVirtualPC UnconnectedNetworkAdapters.
ms.assetid: cfb03a7c-a568-488c-9284-798b7e21027a
keywords:
- Virtual PC de l’interface IVMNetworkAdapterCollection
- IVMNetworkAdapterCollection interface Virtual PC, Description
topic_type:
- apiref
api_name:
- IVMNetworkAdapterCollection
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b532f96343ac0ced3598b8da9f74f1334e6a081e8217994ffce1d2314cadfc79
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119973957"
---
# <a name="ivmnetworkadaptercollection-interface"></a>Interface IVMNetworkAdapterCollection

\[Windows Virtual PC ne peut plus être utilisé à partir de Windows 8. Au lieu de cela, utilisez le [fournisseur WMI Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]

Définit une collection de cartes d’interface réseau virtuelles. Pour obtenir un objet IVMNetworkAdapterCollection, utilisez les propriétés [**IVMVirtualMachine :: NetworkAdapters**](ivmvirtualmachine-networkadapters.md), [**IVMVirtualNetwork :: NetworkAdapters**](ivmvirtualnetwork-networkadapters.md)et [**IVMVirtualPC :: UnconnectedNetworkAdapters**](ivmvirtualpc-unconnectednetworkadapters.md) .

## <a name="members"></a>Membres

L’interface **IVMNetworkAdapterCollection** hérite de l’interface [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) . **IVMNetworkAdapterCollection** a également les types de membres suivants :

-   [Propriétés](#properties)

### <a name="properties"></a>Propriétés

L’interface **IVMNetworkAdapterCollection** possède les propriétés suivantes.



| Propriété                                                             | Type d’accès          | Description                                                                                                   |
|:---------------------------------------------------------------------|:---------------------|:--------------------------------------------------------------------------------------------------------------|
| [**\_NewEnum**](ivmnetworkadaptercollection--newenum.md)<br/> | Lecture seule<br/> | Énumérateur de la collection.<br/>                                                                  |
| [**Count**](ivmnetworkadaptercollection-count.md)<br/>        | Lecture seule<br/> | Nombre d’interfaces réseau de cette collection.<br/>                                               |
| [**Élément**](ivmnetworkadaptercollection-item.md)<br/>          | Lecture seule<br/> | Objet [**IVMNetworkAdapter**](ivmnetworkadapter.md) qui correspond à l’index spécifié.<br/> |



 

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | applications de \[ bureau Windows 7 uniquement\]<br/>                                                     |
| Serveur minimal pris en charge<br/> | Aucun pris en charge<br/>                                                                      |
| Fin de la prise en charge des clients<br/>    | Windows 7<br/>                                                                           |
| Produit<br/>                  | Windows Virtual PC<br/>                                                                  |
| En-tête<br/>                   | <dl> <dt>VPCCOMInterfaces. h</dt> </dl>  |
| IID<br/>                      | IID \_ IVMNetworkAdapterCollection est défini en tant que ebaeafe9-EBCD-47cf-866e-ad87d735e479<br/> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**IVMNetworkAdapter**](ivmnetworkadapter.md)
</dt> <dt>

[**IVMVirtualMachine::NetworkAdapters**](ivmvirtualmachine-networkadapters.md)
</dt> <dt>

[**IVMVirtualNetwork::NetworkAdapters**](ivmvirtualnetwork-networkadapters.md)
</dt> <dt>

[**IVMVirtualPC::UnconnectedNetworkAdapters**](ivmvirtualpc-unconnectednetworkadapters.md)
</dt> </dl>

 

