---
title: IVMNetworkAdapterCollection, propriété d’élément (VPCCOMInterfaces. h)
description: Objet IVMNetworkAdapter qui correspond à l’index spécifié.
ms.assetid: 3de76e24-3315-473f-870b-074be8bcfe70
keywords:
- Propriété de l’élément Virtual PC
- Propriété d’élément Virtual PC, interface IVMNetworkAdapterCollection
- IVMNetworkAdapterCollection interface Virtual PC, propriété Item
topic_type:
- apiref
api_name:
- IVMNetworkAdapterCollection.Item
- IVMNetworkAdapterCollection.get_Item
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ee1c84eb28eb0af583fd18db21ef13c9345caf6c03838d0b11c2af0a80e164bd
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119973967"
---
# <a name="ivmnetworkadaptercollectionitem-property"></a>IVMNetworkAdapterCollection :: Item, propriété

\[Windows Virtual PC ne peut plus être utilisé à partir de Windows 8. Au lieu de cela, utilisez le [fournisseur WMI Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]

Récupère l’objet [**IVMNetworkAdapter**](ivmnetworkadapter.md) qui correspond à l’index spécifié.

Cette propriété est en lecture seule.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT get_Item(
  [in]          long              index,
  [out, retval] IVMNetworkAdapter **networkInterface
);
```



## <a name="property-value"></a>Valeur de la propriété

Objet [**IVMNetworkAdapter**](ivmnetworkadapter.md) .

## <a name="error-codes"></a>Codes d’erreur



| Nom/valeur                                                                                                                                                    | Signification                                                                                        |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------|
| <dl> <dt>S \_ OK</dt> <dt>0</dt> </dl>                       | L'opération a réussi. <br/>                                                      |
| <dl> <dt>E \_ POINTEUR</dt> <dt>0x80004003</dt> </dl>         | Le paramètre *l’interface réseau* a la **valeur null**. <br/>                                      |
| <dl> <dt>DISP \_ \_BADINDEX</dt> <dt>0x8002000B</dt> </dl>  | L’index de l’élément demandé ne correspond pas à un élément de cette collection. <br/> |
| <dl> <dt>DISP \_ E \_ exception</dt> <dt>0x80020009</dt> </dl> | Une erreur inattendue s’est produite.<br/>                                                   |



## <a name="requirements"></a>Conditions requises



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

[**IVMNetworkAdapterCollection**](ivmnetworkadaptercollection.md)
</dt> </dl>

 

