---
title: Interface IVMParallelPortCollection (VPCCOMInterfaces. h)
description: Définit la collection de ports parallèles dans l’ordinateur virtuel. Pour obtenir un objet IVMParallelPortCollection, utilisez la propriété ParallelPorts IVMVirtualMachine.
ms.assetid: 038a5c08-cd92-426f-a059-9a4c2110548d
keywords:
- Virtual PC de l’interface IVMParallelPortCollection
- IVMParallelPortCollection interface Virtual PC, Description
topic_type:
- apiref
api_name:
- IVMParallelPortCollection
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8284b3720e0272147c932cfbfd70448babf5606f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104106051"
---
# <a name="ivmparallelportcollection-interface"></a>Interface IVMParallelPortCollection

\[Windows Virtual PC n’est plus disponible pour une utilisation à partir de Windows 8. Au lieu de cela, utilisez le [fournisseur WMI Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]

Définit la collection de ports parallèles dans l’ordinateur virtuel. Pour obtenir un objet **IVMParallelPortCollection** , utilisez la propriété [**IVMVirtualMachine ::P arallelports**](ivmvirtualmachine-parallelports.md) .

## <a name="members"></a>Membres

L’interface **IVMParallelPortCollection** hérite de l’interface [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) . **IVMParallelPortCollection** a également les types de membres suivants :

-   [Propriétés](#properties)

### <a name="properties"></a>Propriétés

L’interface **IVMParallelPortCollection** possède les propriétés suivantes.



| Propriété                                                           | Type d’accès          | Description                                                                  |
|:-------------------------------------------------------------------|:---------------------|:-----------------------------------------------------------------------------|
| [**\_NewEnum**](ivmparallelportcollection--newenum.md)<br/> | Lecture seule<br/> | Énumérateur de la collection.<br/>                                 |
| [**Saut**](ivmparallelportcollection-count.md)<br/>        | Lecture seule<br/> | Nombre de ports parallèles dans cette collection.<br/>                  |
| [**Élément**](ivmparallelportcollection-item.md)<br/>          | Lecture seule<br/> | Objet de port parallèle qui correspond à l’index spécifié.<br/> |



 

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Applications de \[ Bureau Windows 7 uniquement\]<br/>                                                    |
| Serveur minimal pris en charge<br/> | Aucun pris en charge<br/>                                                                     |
| Fin de la prise en charge des clients<br/>    | Windows 7<br/>                                                                          |
| Produit<br/>                  | Windows Virtual PC<br/>                                                                 |
| En-tête<br/>                   | <dl> <dt>VPCCOMInterfaces. h</dt> </dl> |
| IID<br/>                      | IID \_ IVMParallelPortCollection est défini en tant que 27c3e036-198f-430c-8735-6e652f7203fd<br/>  |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**IVMParallelPort**](ivmparallelport.md)
</dt> <dt>

[**IVMVirtualMachine ::P arallelPorts**](ivmvirtualmachine-parallelports.md)
</dt> </dl>

 

