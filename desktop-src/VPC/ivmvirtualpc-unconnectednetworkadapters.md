---
title: IVMVirtualPC UnconnectedNetworkAdapters, propriété (VPCCOMInterfaces. h)
description: Récupère une collection énumérable d’interfaces réseau non connectées.
ms.assetid: 2d95f289-083a-4388-b842-0a11b4e1a06f
keywords:
- UnconnectedNetworkAdapters propriété Virtual PC
- UnconnectedNetworkAdapters, propriété Virtual PC, IVMVirtualPC, interface
- IVMVirtualPC interface Virtual PC, propriété UnconnectedNetworkAdapters
topic_type:
- apiref
api_name:
- IVMVirtualPC.UnconnectedNetworkAdapters
- IVMVirtualPC.get_UnconnectedNetworkAdapters
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 327a05a659db479816ec29f1c15673aa2eb20d2e4828c07e3bd4a85687337bb6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118998499"
---
# <a name="ivmvirtualpcunconnectednetworkadapters-property"></a>IVMVirtualPC :: UnconnectedNetworkAdapters, propriété

\[Windows Virtual PC ne peut plus être utilisé à partir de Windows 8. Au lieu de cela, utilisez le [fournisseur WMI Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]

Récupère une collection énumérable d’interfaces réseau non connectées.

Cette propriété est en lecture seule.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT get_UnconnectedNetworkAdapters(
  [out, retval] IVMNetworkAdapterCollection **unconnectedNetworkAdapterCollection
);
```



## <a name="property-value"></a>Valeur de la propriété

Collection d’objets [**IVMNetworkAdapter**](ivmnetworkadapter.md) non connectés. Consultez [**IVMNetworkAdapterCollection**](ivmnetworkadaptercollection.md).

## <a name="error-codes"></a>Codes d’erreur



| Nom/valeur                                                                                                                                                                           | Signification                                                                                         |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------|
| <dl> <dt>S \_ OK</dt> <dt>0</dt> </dl>                                              | L'opération a réussi.<br/>                                                        |
| <dl> <dt>E \_ POINTEUR</dt> <dt>0x80004003</dt> </dl>                                | Le paramètre a la **valeur null**.<br/>                                                           |
| <dl> <dt>DISP \_ E \_ exception</dt> <dt>0x80020009</dt> </dl>                        | Une erreur inattendue s’est produite.<br/>                                                    |
| <dl> <dt>Ordinateur virtuel \_ \_Virtualisation matérielle E \_ \_ désactivée</dt> <dt>0xA0040951</dt> </dl> | Le processeur ne prend pas en charge les extensions avez (Hardware Accelerated Virtualization).<br/> |



## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | applications de \[ bureau Windows 7 uniquement\]<br/>                                                    |
| Serveur minimal pris en charge<br/> | Aucun pris en charge<br/>                                                                     |
| Fin de la prise en charge des clients<br/>    | Windows 7<br/>                                                                          |
| Produit<br/>                  | Windows Virtual PC<br/>                                                                 |
| En-tête<br/>                   | <dl> <dt>VPCCOMInterfaces. h</dt> </dl> |
| IID<br/>                      | IID \_ IVMVirtualPC est défini en tant que 236ba0d9-a24a-4292-A132-27c1421dfd01<br/>               |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**IVMVirtualPC**](ivmvirtualpc.md)
</dt> </dl>

 

