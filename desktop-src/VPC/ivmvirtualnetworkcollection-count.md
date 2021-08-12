---
title: Propriété Count IVMVirtualNetworkCollection (VPCCOMInterfaces. h)
description: Récupère le nombre de réseaux virtuels de ce regroupement.
ms.assetid: a9a3ab48-74a0-498e-936e-a99c7b027a85
keywords:
- Propriété Count Virtual PC
- Propriété Count Virtual PC, IVMVirtualNetworkCollection, interface
- IVMVirtualNetworkCollection interface Virtual PC, propriété Count
topic_type:
- apiref
api_name:
- IVMVirtualNetworkCollection.Count
- IVMVirtualNetworkCollection.get_Count
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fbe472ee2e81495284377bab4a59a55bdf07ccf43f636769abcab391fe97ad60
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118592327"
---
# <a name="ivmvirtualnetworkcollectioncount-property"></a>IVMVirtualNetworkCollection :: Count, propriété

\[Windows Virtual PC ne peut plus être utilisé à partir de Windows 8. Au lieu de cela, utilisez le [fournisseur WMI Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]

Récupère le nombre de réseaux virtuels de ce regroupement.

Cette propriété est en lecture seule.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT get_Count(
  [out, retval] long *count
);
```



## <a name="property-value"></a>Valeur de la propriété

Nombre de réseaux virtuels.

## <a name="error-codes"></a>Codes d’erreur



| Nom/valeur                                                                                                                                                    | Signification                                      |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------|
| <dl> <dt>S \_ OK</dt> <dt>0</dt> </dl>                       | L'opération a réussi.<br/>     |
| <dl> <dt>E \_ POINTEUR</dt> <dt>0x80004003</dt> </dl>         | Le paramètre a la **valeur null**.<br/>        |
| <dl> <dt>DISP \_ E \_ exception</dt> <dt>0x80020009</dt> </dl> | Une erreur inattendue s’est produite.<br/> |



## <a name="requirements"></a>Configuration requise



| Condition requise | Value |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | applications de \[ bureau Windows 7 uniquement\]<br/>                                                     |
| Serveur minimal pris en charge<br/> | Aucun pris en charge<br/>                                                                      |
| Fin de la prise en charge des clients<br/>    | Windows 7<br/>                                                                           |
| Produit<br/>                  | Windows Virtual PC<br/>                                                                  |
| En-tête<br/>                   | <dl> <dt>VPCCOMInterfaces. h</dt> </dl>  |
| IID<br/>                      | IID \_ IVMVirtualNetworkCollection est défini en tant que 8ed680be-4242-4B2A-A21C-1982d8b0f675<br/> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**IVMVirtualNetworkCollection**](ivmvirtualnetworkcollection.md)
</dt> </dl>

 

