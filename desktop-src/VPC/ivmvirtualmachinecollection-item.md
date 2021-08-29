---
title: IVMVirtualMachineCollection, propriété d’élément (VPCCOMInterfaces. h)
description: Récupère l’objet ordinateur virtuel qui correspond à l’index spécifié.
ms.assetid: b3afe211-5d97-4ccf-96b7-e074deb320fb
keywords:
- Propriété de l’élément Virtual PC
- Propriété d’élément Virtual PC, interface IVMVirtualMachineCollection
- IVMVirtualMachineCollection interface Virtual PC, propriété Item
topic_type:
- apiref
api_name:
- IVMVirtualMachineCollection.Item
- IVMVirtualMachineCollection.get_Item
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2b8cc689e3e86163e8cade3ea28261db598c38436db7fae6c0fd23c7e4128598
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119958669"
---
# <a name="ivmvirtualmachinecollectionitem-property"></a>IVMVirtualMachineCollection :: Item, propriété

\[Windows Virtual PC ne peut plus être utilisé à partir de Windows 8. Au lieu de cela, utilisez le [fournisseur WMI Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]

Récupère l’objet ordinateur virtuel qui correspond à l’index spécifié.

Cette propriété est en lecture seule.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT get_Item(
  [in]          long              index,
  [out, retval] IVMVirtualMachine **virtualMachine
);
```



## <a name="property-value"></a>Valeur de la propriété

Objet [**IVMVirtualMachine**](ivmvirtualmachine.md) .

## <a name="error-codes"></a>Codes d’erreur



| Nom/valeur                                                                                                                                                    | Signification                                                                                        |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------|
| <dl> <dt>S \_ OK</dt> <dt>0</dt> </dl>                       | L'opération a réussi. <br/>                                                      |
| <dl> <dt>E \_ POINTEUR</dt> <dt>0x80004003</dt> </dl>         | Le paramètre *VirtualMachine* a la **valeur null**. <br/>                                        |
| <dl> <dt>DISP \_ \_BADINDEX</dt> <dt>0x8002000B</dt> </dl>  | L’index de l’élément demandé ne correspond pas à un élément de cette collection. <br/> |
| <dl> <dt>DISP \_ E \_ exception</dt> <dt>0x80020009</dt> </dl> | Une erreur inattendue s’est produite.<br/>                                                   |



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

[**IVMVirtualMachineCollection**](ivmvirtualmachinecollection.md)
</dt> </dl>

 

