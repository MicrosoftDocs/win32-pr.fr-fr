---
title: Interface IVMSerialPortCollection (VPCCOMInterfaces. h)
description: Définit la collection de ports série au sein de la machine virtuelle. Pour obtenir un objet IVMSerialPortCollection, utilisez la propriété SerialPorts IVMVirtualMachine.
ms.assetid: c0ee9799-f3f7-477e-b33b-52f424752aad
keywords:
- Virtual PC de l’interface IVMSerialPortCollection
- IVMSerialPortCollection interface Virtual PC, Description
topic_type:
- apiref
api_name:
- IVMSerialPortCollection
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f1d2ec37789423b5f9446d667da69eca346a2286
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103741740"
---
# <a name="ivmserialportcollection-interface"></a>Interface IVMSerialPortCollection

\[Windows Virtual PC n’est plus disponible pour une utilisation à partir de Windows 8. Au lieu de cela, utilisez le [fournisseur WMI Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]

Définit la collection de ports série au sein de la machine virtuelle. Pour obtenir un objet **IVMSerialPortCollection** , utilisez la propriété [**IVMVirtualMachine :: SerialPorts**](ivmvirtualmachine-serialports.md) .

## <a name="members"></a>Membres

L’interface **IVMSerialPortCollection** hérite de l’interface [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) . **IVMSerialPortCollection** a également les types de membres suivants :

-   [Propriétés](#properties)

### <a name="properties"></a>Propriétés

L’interface **IVMSerialPortCollection** possède les propriétés suivantes.



| Propriété                                                         | Type d’accès          | Description                                                                |
|:-----------------------------------------------------------------|:---------------------|:---------------------------------------------------------------------------|
| [**\_NewEnum**](ivmserialportcollection--newenum.md)<br/> | Lecture seule<br/> | Énumérateur de la collection.<br/>                               |
| [**Saut**](ivmserialportcollection-count.md)<br/>        | Lecture seule<br/> | Nombre de ports série dans cette collection.<br/>                  |
| [**Élément**](ivmserialportcollection-item.md)<br/>          | Lecture seule<br/> | Objet de port série qui correspond à l’index spécifié.<br/> |



 

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Applications de \[ Bureau Windows 7 uniquement\]<br/>                                                    |
| Serveur minimal pris en charge<br/> | Aucun pris en charge<br/>                                                                     |
| Fin de la prise en charge des clients<br/>    | Windows 7<br/>                                                                          |
| Produit<br/>                  | Windows Virtual PC<br/>                                                                 |
| En-tête<br/>                   | <dl> <dt>VPCCOMInterfaces. h</dt> </dl> |
| IID<br/>                      | IID \_ IVMSerialPortCollection est défini en tant que dd3c6175-1f04-4341-9f85-104074880289<br/>    |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**IVMSerialPort**](ivmserialport.md)
</dt> <dt>

[**IVMVirtualMachine::SerialPorts**](ivmvirtualmachine-serialports.md)
</dt> </dl>

 

