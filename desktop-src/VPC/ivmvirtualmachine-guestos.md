---
title: Propriété Invitéos IVMVirtualMachine (VPCCOMInterfaces. h)
description: Récupère le système d’exploitation invité de cet ordinateur virtuel.
ms.assetid: 9cca2a4a-e3bb-4c41-873c-e5bc4863c415
keywords:
- Virtual PC de la propriété invitéos
- Propriété invitée Virtual PC, interface IVMVirtualMachine
- IVMVirtualMachine interface Virtual PC, propriété Invitéos
topic_type:
- apiref
api_name:
- IVMVirtualMachine.GuestOS
- IVMVirtualMachine.get_GuestOS
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1042d63ebfbd62192cfbf97ff44d2226b6e4ac40
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103843721"
---
# <a name="ivmvirtualmachineguestos-property"></a>IVMVirtualMachine :: Guestos, propriété

\[Windows Virtual PC n’est plus disponible pour une utilisation à partir de Windows 8. Au lieu de cela, utilisez le [fournisseur WMI Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]

Récupère le système d’exploitation invité de cet ordinateur virtuel.

Cette propriété est en lecture seule.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT get_GuestOS(
  [out, retval] IVMGuestOS **guestOS
);
```



## <a name="property-value"></a>Valeur de la propriété

Objet [**IVMGuestOS**](ivmguestos.md) .

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

 

