---
title: IVMNetworkAdapter VirtualMachine, propriété (VPCCOMInterfaces. h)
description: Récupère l’ordinateur virtuel associé à cette interface réseau.
ms.assetid: a3519041-0081-44e7-aa76-760d59ca8587
keywords:
- VirtualMachine propriété Virtual PC
- VirtualMachine, propriété Virtual PC, IVMNetworkAdapter, interface
- IVMNetworkAdapter interface Virtual PC, propriété VirtualMachine
topic_type:
- apiref
api_name:
- IVMNetworkAdapter.VirtualMachine
- IVMNetworkAdapter.get_VirtualMachine
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ea50e43bdcffcd16f668ef596a0f9db9d9bccfe2
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104032299"
---
# <a name="ivmnetworkadaptervirtualmachine-property"></a>IVMNetworkAdapter :: VirtualMachine, propriété

\[Windows Virtual PC n’est plus disponible pour une utilisation à partir de Windows 8. Au lieu de cela, utilisez le [fournisseur WMI Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]

Récupère l’ordinateur virtuel associé à cette interface réseau.

Cette propriété est en lecture seule.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT get_VirtualMachine(
  [out, retval] IVMVirtualMachine **virtualMachine
);
```



## <a name="property-value"></a>Valeur de la propriété

Interface [**IVMVirtualMachine**](ivmvirtualmachine.md) qui représente l’ordinateur virtuel.

## <a name="error-codes"></a>Codes d’erreur



| Nom/valeur                                                                                                                                                    | Signification                                         |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------|
| <dl> <dt>S \_ OK</dt> <dt>0</dt> </dl>                       | L'opération a réussi.<br/>        |
| <dl> <dt>E \_ POINTEUR</dt> <dt>0x80004003</dt> </dl>         | Le paramètre a la **valeur null**.<br/>           |
| <dl> <dt>Ordinateur virtuel \_ \_Machine virtuelle \_ </dt> <dt>0xA0040207</dt> inconnue </dl> | L’ordinateur virtuel est introuvable.<br/> |
| <dl> <dt>DISP \_ E \_ exception</dt> <dt>0x80020009</dt> </dl> | Une erreur inattendue s’est produite.<br/>    |



## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Applications de \[ Bureau Windows 7 uniquement\]<br/>                                                    |
| Serveur minimal pris en charge<br/> | Aucun pris en charge<br/>                                                                     |
| Fin de la prise en charge des clients<br/>    | Windows 7<br/>                                                                          |
| Produit<br/>                  | Windows Virtual PC<br/>                                                                 |
| En-tête<br/>                   | <dl> <dt>VPCCOMInterfaces. h</dt> </dl> |
| IID<br/>                      | IID \_ IVMNetworkAdapter est défini en tant que e32e4165-22b8-4DC0-8d57-850171ae207a<br/>          |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**IVMNetworkAdapter**](ivmnetworkadapter.md)
</dt> </dl>

 

