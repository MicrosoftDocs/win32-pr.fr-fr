---
title: IVMNetworkAdapter VirtualNetwork, propriété (VPCCOMInterfaces. h)
description: Récupère le réseau virtuel auquel l’interface réseau est attachée.
ms.assetid: 7f52fd86-5f83-41d8-ba48-7db65e9c357c
keywords:
- VirtualNetwork propriété Virtual PC
- VirtualNetwork, propriété Virtual PC, IVMNetworkAdapter, interface
- IVMNetworkAdapter interface Virtual PC, propriété VirtualNetwork
topic_type:
- apiref
api_name:
- IVMNetworkAdapter.VirtualNetwork
- IVMNetworkAdapter.get_VirtualNetwork
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b932ef553d3952fbc69edba3416ac20049984810
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104032298"
---
# <a name="ivmnetworkadaptervirtualnetwork-property"></a>IVMNetworkAdapter :: VirtualNetwork, propriété

\[Windows Virtual PC n’est plus disponible pour une utilisation à partir de Windows 8. Au lieu de cela, utilisez le [fournisseur WMI Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]

Récupère le réseau virtuel auquel l’interface réseau est attachée.

Cette propriété est en lecture seule.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT get_VirtualNetwork(
  [out, retval] IVMVirtualNetwork **virtualNetwork
);
```



## <a name="property-value"></a>Valeur de la propriété

Interface [**IVMVirtualNetwork**](ivmvirtualnetwork.md) qui représente le réseau virtuel auquel cette interface réseau virtuelle est attachée.

## <a name="error-codes"></a>Codes d’erreur



| Nom/valeur                                                                                                                                                                       | Signification                                                                                   |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------|
| <dl> <dt>S \_ OK</dt> <dt>0</dt> </dl>                                          | L'opération a réussi.<br/>                                                  |
| <dl> <dt>E \_ POINTEUR</dt> <dt>0x80004003</dt> </dl>                            | Le paramètre a la **valeur null**.<br/>                                                     |
| <dl> <dt>S \_ FALSe</dt> <dt>1</dt> </dl>                                       | Cette interface réseau est déconnectée et n’est pas connectée à un réseau virtuel.<br/> |
| <dl> <dt>Ordinateur virtuel \_ E \_ \_ ID de \_ réseau \_ virtuel non valide</dt> <dt>0xA00400702</dt> </dl> | Cette interface est connectée à un réseau virtuel avec un ID non valide.<br/>           |
| <dl> <dt>DISP \_ E \_ exception</dt> <dt>0x80020009</dt> </dl>                    | Une erreur inattendue s’est produite.<br/>                                              |



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

 

