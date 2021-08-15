---
title: Propriété IVMHostInfo OperatingSystem (VPCCOMInterfaces. h)
description: Récupère le système d’exploitation en cours d’exécution sur l’ordinateur.
ms.assetid: 1164bb7d-cdce-4649-86d6-22e3ea7bad98
keywords:
- Propriété OperatingSystem Virtual PC
- Propriété OperatingSystem Virtual PC, interface IVMHostInfo
- IVMHostInfo interface Virtual PC, OperatingSystem, propriété
topic_type:
- apiref
api_name:
- IVMHostInfo.OperatingSystem
- IVMHostInfo.get_OperatingSystem
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9ba380311633d62f766fc0c18c82782b482556b51cea6a7c85c7c98f3478ec16
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117753237"
---
# <a name="ivmhostinfooperatingsystem-property"></a>IVMHostInfo :: OperatingSystem, propriété

\[Windows Virtual PC ne peut plus être utilisé à partir de Windows 8. Au lieu de cela, utilisez le [fournisseur WMI Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]

Récupère le système d’exploitation en cours d’exécution sur l’ordinateur.

Cette propriété est en lecture seule.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT get_OperatingSystem(
  [out, retval] BSTR *operatingSystem
);
```



## <a name="property-value"></a>Valeur de la propriété

Nom du système d’exploitation.

## <a name="error-codes"></a>Codes d’erreur



| Nom/valeur                                                                                                                                                    | Signification                                      |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------|
| <dl> <dt>S \_ OK</dt> <dt>0</dt> </dl>                       | L'opération a réussi.<br/>     |
| <dl> <dt>E \_ POINTEUR</dt> <dt>0x80004003</dt> </dl>         | Le paramètre a la **valeur null**.<br/>        |
| <dl> <dt>DISP \_ E \_ exception</dt> <dt>0x80020009</dt> </dl> | Une erreur inattendue s’est produite.<br/> |



## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | applications de \[ bureau Windows 7 uniquement\]<br/>                                                    |
| Serveur minimal pris en charge<br/> | Aucun pris en charge<br/>                                                                     |
| Fin de la prise en charge des clients<br/>    | Windows 7<br/>                                                                          |
| Produit<br/>                  | Windows Virtual PC<br/>                                                                 |
| En-tête<br/>                   | <dl> <dt>VPCCOMInterfaces. h</dt> </dl> |
| IID<br/>                      | IID \_ IVMHostInfo est défini en tant que 5b5cf343-05ad-453B-BE99-adf4e27b2ebc<br/>                |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**IVMHostInfo**](ivmhostinfo.md)
</dt> </dl>

 

