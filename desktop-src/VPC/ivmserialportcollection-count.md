---
title: Propriété Count IVMSerialPortCollection (VPCCOMInterfaces. h)
description: Récupère le nombre de ports série de cette collection.
ms.assetid: 94ff6c9d-17bc-4aa5-a486-d4428c829d02
keywords:
- Propriété Count Virtual PC
- Propriété Count Virtual PC, IVMSerialPortCollection, interface
- IVMSerialPortCollection interface Virtual PC, propriété Count
topic_type:
- apiref
api_name:
- IVMSerialPortCollection.Count
- IVMSerialPortCollection.get_Count
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bbf0503f00fd1df7d27a8eeafedd3efe42619b98
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103843834"
---
# <a name="ivmserialportcollectioncount-property"></a>IVMSerialPortCollection :: Count, propriété

\[Windows Virtual PC n’est plus disponible pour une utilisation à partir de Windows 8. Au lieu de cela, utilisez le [fournisseur WMI Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]

Récupère le nombre de ports série de cette collection.

Cette propriété est en lecture seule.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT get_Count(
  [out, retval] long *count
);
```



## <a name="property-value"></a>Valeur de la propriété

Nombre de ports série.

## <a name="error-codes"></a>Codes d’erreur



| Nom/valeur                                                                                                                                            | Signification                                  |
|-------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------|
| <dl> <dt>S \_ OK</dt> <dt>0</dt> </dl>               | L'opération a réussi.<br/> |
| <dl> <dt>E \_ POINTEUR</dt> <dt>0x80004003</dt> </dl> | Le paramètre a la **valeur null**.<br/>    |



## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Applications de \[ Bureau Windows 7 uniquement\]<br/>                                                    |
| Serveur minimal pris en charge<br/> | Aucun pris en charge<br/>                                                                     |
| Fin de la prise en charge des clients<br/>    | Windows 7<br/>                                                                          |
| Produit<br/>                  | Windows Virtual PC<br/>                                                                 |
| En-tête<br/>                   | <dl> <dt>VPCCOMInterfaces. h</dt> </dl> |
| IID<br/>                      | IID \_ IVMSerialPortCollection est défini en tant que dd3c6175-1f04-4341-9f85-104074880289<br/>    |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**IVMSerialPortCollection**](ivmserialportcollection.md)
</dt> </dl>

 

