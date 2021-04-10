---
title: Interface IVMVirtualMachineCollection (VPCCOMInterfaces. h)
description: Définit la collection de machines virtuelles au sein de Windows Virtual PC. Pour obtenir un objet IVMVirtualMachineCollection, utilisez la propriété VirtualMachines IVMVirtualPC.
ms.assetid: 3d34e791-2dba-4529-b489-96a0c6227294
keywords:
- Virtual PC de l’interface IVMVirtualMachineCollection
- IVMVirtualMachineCollection interface Virtual PC, Description
topic_type:
- apiref
api_name:
- IVMVirtualMachineCollection
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e27426f96e409a1e67eb519e7a864ee7461879a7
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104105646"
---
# <a name="ivmvirtualmachinecollection-interface"></a>Interface IVMVirtualMachineCollection

\[Windows Virtual PC n’est plus disponible pour une utilisation à partir de Windows 8. Au lieu de cela, utilisez le [fournisseur WMI Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]

Définit la collection de machines virtuelles au sein de Windows Virtual PC. Pour obtenir un objet **IVMVirtualMachineCollection** , utilisez la propriété [**IVMVirtualPC :: VirtualMachines**](ivmvirtualpc-virtualmachines.md) .

## <a name="members"></a>Membres

L’interface **IVMVirtualMachineCollection** hérite de l’interface [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) . **IVMVirtualMachineCollection** a également les types de membres suivants :

-   [Propriétés](#properties)

### <a name="properties"></a>Propriétés

L’interface **IVMVirtualMachineCollection** possède les propriétés suivantes.



| Propriété                                                             | Type d’accès          | Description                                                                    |
|:---------------------------------------------------------------------|:---------------------|:-------------------------------------------------------------------------------|
| [**\_NewEnum**](ivmvirtualmachinecollection--newenum.md)<br/> | Lecture seule<br/> | Énumérateur de la collection.<br/>                                   |
| [**Saut**](ivmvirtualmachinecollection-count.md)<br/>        | Lecture seule<br/> | Nombre de machines virtuelles dans ce regroupement.<br/>                  |
| [**Élément**](ivmvirtualmachinecollection-item.md)<br/>          | Lecture seule<br/> | Objet ordinateur virtuel qui correspond à l’index spécifié.<br/> |



 

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Applications de \[ Bureau Windows 7 uniquement\]<br/>                                                     |
| Serveur minimal pris en charge<br/> | Aucun pris en charge<br/>                                                                      |
| Fin de la prise en charge des clients<br/>    | Windows 7<br/>                                                                           |
| Produit<br/>                  | Windows Virtual PC<br/>                                                                  |
| En-tête<br/>                   | <dl> <dt>VPCCOMInterfaces. h</dt> </dl>  |
| IID<br/>                      | IID \_ IVMVirtualMachineCollection est défini en tant que 59f31786-2a3d-4FBF-9896-d85338ca0da1<br/> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**IVMVirtualMachine**](ivmvirtualmachine.md)
</dt> <dt>

[**IVMVirtualPC :: VirtualMachines**](ivmvirtualpc-virtualmachines.md)
</dt> </dl>

 

