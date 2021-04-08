---
title: Interface IVMVirtualNetworkCollection (VPCCOMInterfaces. h)
description: Définit une collection d’objets IVMVirtualNetwork. Pour obtenir un objet IVMVirtualNetworkCollection, utilisez la propriété VirtualNetworks IVMVirtualPC.
ms.assetid: 3d595bc3-1a8d-4e09-a809-944d4dcdc675
keywords:
- Virtual PC de l’interface IVMVirtualNetworkCollection
- IVMVirtualNetworkCollection interface Virtual PC, Description
topic_type:
- apiref
api_name:
- IVMVirtualNetworkCollection
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 76935fd4a67983847e211d8aa53f4a616bed9d4d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103743084"
---
# <a name="ivmvirtualnetworkcollection-interface"></a>Interface IVMVirtualNetworkCollection

\[Windows Virtual PC n’est plus disponible pour une utilisation à partir de Windows 8. Au lieu de cela, utilisez le [fournisseur WMI Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]

Définit une collection d’objets [**IVMVirtualNetwork**](ivmvirtualnetwork.md) . Pour obtenir un objet **IVMVirtualNetworkCollection** , utilisez la propriété [**IVMVirtualPC :: VirtualNetworks**](ivmvirtualpc-virtualnetworks.md) .

## <a name="members"></a>Membres

L’interface **IVMVirtualNetworkCollection** hérite de l’interface [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) . **IVMVirtualNetworkCollection** a également les types de membres suivants :

-   [Propriétés](#properties)

### <a name="properties"></a>Propriétés

L’interface **IVMVirtualNetworkCollection** possède les propriétés suivantes.



| Propriété                                                             | Type d’accès          | Description                                                                                                   |
|:---------------------------------------------------------------------|:---------------------|:--------------------------------------------------------------------------------------------------------------|
| [**\_NewEnum**](ivmvirtualnetworkcollection--newenum.md)<br/> | Lecture seule<br/> | Énumérateur de la collection.<br/>                                                                  |
| [**Saut**](ivmvirtualnetworkcollection-count.md)<br/>        | Lecture seule<br/> | Nombre de réseaux virtuels dans ce regroupement.<br/>                                                 |
| [**Élément**](ivmvirtualnetworkcollection-item.md)<br/>          | Lecture seule<br/> | Objet [**IVMVirtualNetwork**](ivmvirtualnetwork.md) qui correspond à l’index spécifié.<br/> |



 

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Applications de \[ Bureau Windows 7 uniquement\]<br/>                                                     |
| Serveur minimal pris en charge<br/> | Aucun pris en charge<br/>                                                                      |
| Fin de la prise en charge des clients<br/>    | Windows 7<br/>                                                                           |
| Produit<br/>                  | Windows Virtual PC<br/>                                                                  |
| En-tête<br/>                   | <dl> <dt>VPCCOMInterfaces. h</dt> </dl>  |
| IID<br/>                      | IID \_ IVMVirtualNetworkCollection est défini en tant que 8ed680be-4242-4B2A-A21C-1982d8b0f675<br/> |



 

