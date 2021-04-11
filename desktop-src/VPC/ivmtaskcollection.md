---
title: Interface IVMTaskCollection (VPCCOMInterfaces. h)
description: Définit la collection d’objets Task. Pour obtenir un objet IVMTaskCollection, utilisez la propriété tâches IVMVirtualPC.
ms.assetid: 5cfc543c-81a1-49d2-93a9-9b1db1cb5070
keywords:
- Virtual PC de l’interface IVMTaskCollection
- IVMTaskCollection interface Virtual PC, Description
topic_type:
- apiref
api_name:
- IVMTaskCollection
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 43ff7a4b12b936f2b5c72a73818eca0f927eef12
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104385043"
---
# <a name="ivmtaskcollection-interface"></a>Interface IVMTaskCollection

\[Windows Virtual PC n’est plus disponible pour une utilisation à partir de Windows 8. Au lieu de cela, utilisez le [fournisseur WMI Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]

Définit la collection d’objets Task. Pour obtenir un objet **IVMTaskCollection** , utilisez la propriété [**IVMVirtualPC :: Tasks**](ivmvirtualpc-tasks.md) .

## <a name="members"></a>Membres

L’interface **IVMTaskCollection** hérite de l’interface [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) . **IVMTaskCollection** a également les types de membres suivants :

-   [Propriétés](#properties)

### <a name="properties"></a>Propriétés

L’interface **IVMTaskCollection** possède les propriétés suivantes.



| Propriété                                                   | Type d’accès          | Description                                                         |
|:-----------------------------------------------------------|:---------------------|:--------------------------------------------------------------------|
| [**\_NewEnum**](ivmtaskcollection--newenum.md)<br/> | Lecture seule<br/> | Énumérateur de la collection.<br/>                        |
| [**Saut**](ivmtaskcollection-count.md)<br/>        | Lecture seule<br/> | Nombre de tâches de cette collection.<br/>                  |
| [**Élément**](ivmtaskcollection-item.md)<br/>          | Lecture seule<br/> | Objet de tâche qui correspond à l’index spécifié.<br/> |



 

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Applications de \[ Bureau Windows 7 uniquement\]<br/>                                                    |
| Serveur minimal pris en charge<br/> | Aucun pris en charge<br/>                                                                     |
| Fin de la prise en charge des clients<br/>    | Windows 7<br/>                                                                          |
| Produit<br/>                  | Windows Virtual PC<br/>                                                                 |
| En-tête<br/>                   | <dl> <dt>VPCCOMInterfaces. h</dt> </dl> |
| IID<br/>                      | IID \_ IVMTaskCollection est défini en tant que 5c4387c8-0e8b-4B97-8058-84679adf4c40<br/>          |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**IVMTask**](ivmtask.md)
</dt> <dt>

[**IVMVirtualPC :: Tasks**](ivmvirtualpc-tasks.md)
</dt> </dl>

 

