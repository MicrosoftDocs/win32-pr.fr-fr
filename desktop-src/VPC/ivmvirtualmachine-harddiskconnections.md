---
title: IVMVirtualMachine HardDiskConnections, propriété (VPCCOMInterfaces. h)
description: Récupère une collection énumérable de connexions de disque dur.
ms.assetid: 167eb8af-bbc1-49a8-83fd-8d946b50530d
keywords:
- HardDiskConnections propriété Virtual PC
- HardDiskConnections, propriété Virtual PC, IVMVirtualMachine, interface
- IVMVirtualMachine interface Virtual PC, propriété HardDiskConnections
topic_type:
- apiref
api_name:
- IVMVirtualMachine.HardDiskConnections
- IVMVirtualMachine.get_HardDiskConnections
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6b4a409337dc6fb437a98fe002f6e0d5d4da44b3
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103742045"
---
# <a name="ivmvirtualmachineharddiskconnections-property"></a>IVMVirtualMachine :: HardDiskConnections, propriété

\[Windows Virtual PC n’est plus disponible pour une utilisation à partir de Windows 8. Au lieu de cela, utilisez le [fournisseur WMI Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]

Récupère une collection énumérable de connexions de disque dur.

Cette propriété est en lecture seule.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT get_HardDiskConnections(
  [out, retval] IVMHardDiskConnectionCollection **hardDiskConnectionCollection
);
```



## <a name="property-value"></a>Valeur de la propriété

Objet [**IVMHardDiskConnectionCollection**](ivmharddiskconnectioncollection.md) .

## <a name="error-codes"></a>Codes d’erreur



| Nom/valeur                                                                                                                                                    | Signification                                      |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------|
| <dl> <dt>S \_ OK</dt> <dt>0</dt> </dl>                       | L'opération a réussi.<br/>     |
| <dl> <dt>E \_ POINTEUR</dt> <dt>0x80004003</dt> </dl>         | Le paramètre a la **valeur null**.<br/>        |
| <dl> <dt>Ordinateur virtuel \_ \_Machine virtuelle \_ </dt> <dt>0xA0040207</dt> inconnue </dl> | La configuration est inconnue.<br/>     |
| <dl> <dt>DISP \_ E \_ exception</dt> <dt>0x80020009</dt> </dl> | Une erreur inattendue s’est produite.<br/> |



## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Applications de \[ Bureau Windows 7 uniquement\]<br/>                                                    |
| Serveur minimal pris en charge<br/> | Aucun pris en charge<br/>                                                                     |
| Fin de la prise en charge des clients<br/>    | Windows 7<br/>                                                                          |
| Produit<br/>                  | Windows Virtual PC<br/>                                                                 |
| En-tête<br/>                   | <dl> <dt>VPCCOMInterfaces. h</dt> </dl> |
| IID<br/>                      | IID \_ IVMVirtualMachine est défini en tant que f7092aa1-33ed-4f78-a59f-c00adfc2edd7<br/>          |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**IVMVirtualMachine**](ivmvirtualmachine.md)
</dt> </dl>

 

