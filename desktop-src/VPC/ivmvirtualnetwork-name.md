---
title: Propriété IVMVirtualNetwork Name (VPCCOMInterfaces. h)
description: Nom unique de l’instance de réseau virtuel.
ms.assetid: dd4807dc-abae-4bdb-ba27-597cf1337834
keywords:
- Propriété de nom Virtual PC
- Propriété de nom Virtual PC, interface IVMVirtualNetwork
- IVMVirtualNetwork interface Virtual PC, propriété Name
topic_type:
- apiref
api_name:
- IVMVirtualNetwork.Name
- IVMVirtualNetwork.get_Name
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c962d7b65bfddaf5293bd391ae84f04bae512ba9
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103942679"
---
# <a name="ivmvirtualnetworkname-property"></a>IVMVirtualNetwork :: Name, propriété

\[Windows Virtual PC n’est plus disponible pour une utilisation à partir de Windows 8. Au lieu de cela, utilisez le [fournisseur WMI Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]

Récupère le nom unique de l’instance de réseau virtuel.

Cette propriété est en lecture seule.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT get_Name(
  [out, retval] BSTR *virtualNetworkName
);
```



## <a name="property-value"></a>Valeur de la propriété

nom du réseau virtuel.

## <a name="error-codes"></a>Codes d’erreur



| Nom/valeur                                                                                                                                                    | Signification                                                                                 |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------|
| <dl> <dt>S \_ OK</dt> <dt>0</dt> </dl>                       | L'opération a réussi.<br/>                                                |
| <dl> <dt>E \_ POINTEUR</dt> <dt>0x80004003</dt> </dl>         | Le paramètre a la **valeur null**.<br/>                                                   |
| <dl> <dt>DISP \_ E \_ exception</dt> <dt>0x80020009</dt> </dl> | Une erreur inattendue s’est produite ou l’instance de réseau virtuel est inconnue.<br/> |



## <a name="remarks"></a>Notes

Les noms de réseaux virtuels ne respectent pas la casse, par exemple, « MyNetwork » et « mynetwork » font référence au même réseau virtuel.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Applications de \[ Bureau Windows 7 uniquement\]<br/>                                                    |
| Serveur minimal pris en charge<br/> | Aucun pris en charge<br/>                                                                     |
| Fin de la prise en charge des clients<br/>    | Windows 7<br/>                                                                          |
| Produit<br/>                  | Windows Virtual PC<br/>                                                                 |
| En-tête<br/>                   | <dl> <dt>VPCCOMInterfaces. h</dt> </dl> |
| IID<br/>                      | IID \_ IVMVirtualNetwork est défini en tant que 431cb7a1-2469-4563-b94e-38b987adca63<br/>          |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**IVMVirtualNetwork**](ivmvirtualnetwork.md)
</dt> </dl>

 

