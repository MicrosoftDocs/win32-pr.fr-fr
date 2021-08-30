---
title: Interface IVMVirtualMachineCollection (VPCCOMInterfaces. h)
description: définit la collection d’ordinateurs virtuels au sein d’Windows virtual PC. Pour obtenir un objet IVMVirtualMachineCollection, utilisez la propriété VirtualMachines IVMVirtualPC.
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
ms.openlocfilehash: 9d3ca6a04d95d20a6e18e5fe70b285becc6fb1744e1465dad4e20d0c28d9fa45
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120006789"
---
# <a name="ivmvirtualmachinecollection-interface"></a>Interface IVMVirtualMachineCollection

\[Windows Virtual PC ne peut plus être utilisé à partir de Windows 8. Au lieu de cela, utilisez le [fournisseur WMI Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]

définit la collection d’ordinateurs virtuels au sein d’Windows virtual PC. Pour obtenir un objet **IVMVirtualMachineCollection** , utilisez la propriété [**IVMVirtualPC :: VirtualMachines**](ivmvirtualpc-virtualmachines.md) .

## <a name="members"></a>Membres

L’interface **IVMVirtualMachineCollection** hérite de l’interface [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) . **IVMVirtualMachineCollection** a également les types de membres suivants :

-   [Propriétés](#properties)

### <a name="properties"></a>Propriétés

L’interface **IVMVirtualMachineCollection** possède les propriétés suivantes.



| Propriété                                                             | Type d’accès          | Description                                                                    |
|:---------------------------------------------------------------------|:---------------------|:-------------------------------------------------------------------------------|
| [**\_NewEnum**](ivmvirtualmachinecollection--newenum.md)<br/> | Lecture seule<br/> | Énumérateur de la collection.<br/>                                   |
| [**Count**](ivmvirtualmachinecollection-count.md)<br/>        | Lecture seule<br/> | Nombre de machines virtuelles dans ce regroupement.<br/>                  |
| [**Élément**](ivmvirtualmachinecollection-item.md)<br/>          | Lecture seule<br/> | Objet ordinateur virtuel qui correspond à l’index spécifié.<br/> |



 

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | applications de \[ bureau Windows 7 uniquement\]<br/>                                                     |
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

 

