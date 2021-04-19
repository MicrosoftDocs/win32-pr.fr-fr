---
title: Interface IVMParallelPort (VPCCOMInterfaces. h)
description: Définit un port parallèle à l’intérieur d’une machine virtuelle.
ms.assetid: da8daf16-5d22-49be-8fe9-72d5018c0622
keywords:
- Virtual PC de l’interface IVMParallelPort
- IVMParallelPort interface Virtual PC, Description
topic_type:
- apiref
api_name:
- IVMParallelPort
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 71b76b23f48e728104a3826afa80a8f272cd7e66
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "106512204"
---
# <a name="ivmparallelport-interface"></a>Interface IVMParallelPort

\[Windows Virtual PC n’est plus disponible pour une utilisation à partir de Windows 8. Au lieu de cela, utilisez le [fournisseur WMI Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]

Définit un port parallèle à l’intérieur d’une machine virtuelle. Cette interface vous permet de configurer des ports parallèles à l’intérieur d’une machine virtuelle. Vous pouvez récupérer un objet **IVMParallelPort** à partir de l’objet [**IVMParallelPortCollection**](ivmparallelportcollection.md) retourné à partir de la propriété [**IVMVirtualMachine ::P arallelports**](ivmvirtualmachine-parallelports.md) .

## <a name="members"></a>Membres

L’interface **IVMParallelPort** hérite de l’interface [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) . **IVMParallelPort** a également les types de membres suivants :

-   [Méthodes](#methods)
-   [Propriétés](#properties)

### <a name="methods"></a>Méthodes

L’interface **IVMParallelPort** possède ces méthodes.



| Méthode                              | Description                                                        |
|:------------------------------------|:-------------------------------------------------------------------|
| [**\_IDENTIFI**](ivmparallelport--id.md) | Récupère l’identificateur interne du port parallèle.<br/> |



 

### <a name="properties"></a>Propriétés

L’interface **IVMParallelPort** possède les propriétés suivantes.



| Propriété                                        | Type d’accès           | Description                               |
|:------------------------------------------------|:----------------------|:------------------------------------------|
| [**Nom**](ivmparallelport-name.md)<br/> | Lecture/écriture<br/> | Nom du port parallèle.<br/> |



 

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Applications de \[ Bureau Windows 7 uniquement\]<br/>                                                    |
| Serveur minimal pris en charge<br/> | Aucun pris en charge<br/>                                                                     |
| Fin de la prise en charge des clients<br/>    | Windows 7<br/>                                                                          |
| Produit<br/>                  | Windows Virtual PC<br/>                                                                 |
| En-tête<br/>                   | <dl> <dt>VPCCOMInterfaces. h</dt> </dl> |
| IID<br/>                      | IID \_ IVMParallelPort est défini en tant que 097beecb-0a02-474F-abd6-298b22293fc6<br/>            |



 

