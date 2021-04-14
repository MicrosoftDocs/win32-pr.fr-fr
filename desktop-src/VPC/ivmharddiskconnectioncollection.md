---
title: Interface IVMHardDiskConnectionCollection (VPCCOMInterfaces. h)
description: Définit la collection de connexions de disque dur au sein de la machine virtuelle. Pour obtenir un objet IVMHardDiskConnectionCollection, utilisez la propriété HardDiskConnections IVMVirtualMachine.
ms.assetid: 3440318c-45f4-4d24-9609-dbe5ca59b005
keywords:
- Virtual PC de l’interface IVMHardDiskConnectionCollection
- IVMHardDiskConnectionCollection interface Virtual PC, Description
topic_type:
- apiref
api_name:
- IVMHardDiskConnectionCollection
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: dbde67f226c5b2d8cb86a8764c6dd61c24c2a468
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104464186"
---
# <a name="ivmharddiskconnectioncollection-interface"></a>Interface IVMHardDiskConnectionCollection

\[Windows Virtual PC n’est plus disponible pour une utilisation à partir de Windows 8. Au lieu de cela, utilisez le [fournisseur WMI Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]

Définit la collection de connexions de disque dur au sein de la machine virtuelle. Pour obtenir un objet **IVMHardDiskConnectionCollection** , utilisez la propriété [**IVMVirtualMachine :: HardDiskConnections**](ivmvirtualmachine-harddiskconnections.md) .

## <a name="members"></a>Membres

L’interface **IVMHardDiskConnectionCollection** hérite de l’interface [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) . **IVMHardDiskConnectionCollection** a également les types de membres suivants :

-   [Propriétés](#properties)

### <a name="properties"></a>Propriétés

L’interface **IVMHardDiskConnectionCollection** possède les propriétés suivantes.



| Propriété                                                                 | Type d’accès          | Description                                                                         |
|:-------------------------------------------------------------------------|:---------------------|:------------------------------------------------------------------------------------|
| [**\_NewEnum**](ivmharddiskconnectioncollection--newenum.md)<br/> | Lecture seule<br/> | Énumérateur de la collection.<br/>                                        |
| [**Saut**](ivmharddiskconnectioncollection-count.md)<br/>        | Lecture seule<br/> | Nombre de connexions de disque dur dans ce regroupement.<br/>                  |
| [**Élément**](ivmharddiskconnectioncollection-item.md)<br/>          | Lecture seule<br/> | Objet de connexion de disque dur qui correspond à l’index spécifié.<br/> |



 

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|----------------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Applications de \[ Bureau Windows 7 uniquement\]<br/>                                                         |
| Serveur minimal pris en charge<br/> | Aucun pris en charge<br/>                                                                          |
| Fin de la prise en charge des clients<br/>    | Windows 7<br/>                                                                               |
| Produit<br/>                  | Windows Virtual PC<br/>                                                                      |
| En-tête<br/>                   | <dl> <dt>VPCCOMInterfaces. h</dt> </dl>      |
| IID<br/>                      | IID \_ IVMHardDiskconnectionCollection est défini en tant que b9f2caf4-0aeb-4085-B105-ceddb90dbf62<br/> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**IVMHardDiskConnection**](ivmharddiskconnection.md)
</dt> <dt>

[**IVMVirtualMachine::HardDiskConnections**](ivmvirtualmachine-harddiskconnections.md)
</dt> </dl>

 

