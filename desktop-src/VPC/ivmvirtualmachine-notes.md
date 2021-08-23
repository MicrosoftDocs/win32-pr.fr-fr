---
title: Propriété notes IVMVirtualMachine (VPCCOMInterfaces. h)
description: Remarques relatives à la machine virtuelle.
ms.assetid: 4be6842b-31b2-4619-a6ab-b728be1e2174
keywords:
- Propriété notes Virtual PC
- Propriété notes Virtual PC, interface IVMVirtualMachine
- IVMVirtualMachine interface Virtual PC, propriété notes
topic_type:
- apiref
api_name:
- IVMVirtualMachine.Notes
- IVMVirtualMachine.get_Notes
- IVMVirtualMachine.put_Notes
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b6e5e492330286bd60175983895a39ad7b0c91997f7fd36c966647d530a91c9d
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119471509"
---
# <a name="ivmvirtualmachinenotes-property"></a>IVMVirtualMachine :: notes, propriété

\[Windows Virtual PC ne peut plus être utilisé à partir de Windows 8. Au lieu de cela, utilisez le [fournisseur WMI Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]

Récupère et définit les notes pour l’ordinateur virtuel.

Cette propriété est en lecture/écriture.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT put_Notes(
  [in]          BSTR virtualMachineNotes
);

HRESULT get_Notes(
  [out, retval] BSTR *virtualMachineNotes
);
```



## <a name="property-value"></a>Valeur de la propriété

Spécifie les remarques pour l’ordinateur virtuel. La longueur maximale de la chaîne est de 65 536 caractères.

Pour supprimer des notes, transmettez une chaîne vide.

## <a name="error-codes"></a>Codes d’erreur



| Nom/valeur                                                                                                                                                    | Signification                                                                        |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------|
| <dl> <dt>S \_ OK</dt> <dt>0</dt> </dl>                       | L'opération a réussi.<br/>                                       |
| <dl> <dt>E \_ POINTEUR</dt> <dt>0x80004003</dt> </dl>         | Le paramètre a la **valeur null**.<br/>                                          |
| <dl> <dt>E \_ INVALIDARG</dt> <dt>0x80000003</dt> </dl>      | Le paramètre n’est pas valide ou contient plus de 65 536 caractères.<br/> |
| <dl> <dt>Ordinateur virtuel \_ \_Machine virtuelle \_ </dt> <dt>0xA0040207</dt> inconnue </dl> | La configuration est inconnue.<br/>                                       |
| <dl> <dt>DISP \_ E \_ exception</dt> <dt>0x80020009</dt> </dl> | Une erreur inattendue s’est produite.<br/>                                   |



## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | applications de \[ bureau Windows 7 uniquement\]<br/>                                                    |
| Serveur minimal pris en charge<br/> | Aucun pris en charge<br/>                                                                     |
| Fin de la prise en charge des clients<br/>    | Windows 7<br/>                                                                          |
| Produit<br/>                  | Windows Virtual PC<br/>                                                                 |
| En-tête<br/>                   | <dl> <dt>VPCCOMInterfaces. h</dt> </dl> |
| IID<br/>                      | IID \_ IVMVirtualMachine est défini en tant que f7092aa1-33ed-4f78-a59f-c00adfc2edd7<br/>          |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**IVMVirtualMachine**](ivmvirtualmachine.md)
</dt> </dl>

 

