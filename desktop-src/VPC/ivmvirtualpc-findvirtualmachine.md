---
title: Méthode IVMVirtualPC FindVirtualMachine (VPCCOMInterfaces. h)
description: Récupère un objet ordinateur virtuel qui correspond à la configuration demandée.
ms.assetid: 1c73d6f7-5662-485e-a864-e8e48197f8e4
keywords:
- Méthode FindVirtualMachine Virtual PC
- Méthode FindVirtualMachine Virtual PC, interface IVMVirtualPC
- IVMVirtualPC interface Virtual PC, méthode FindVirtualMachine
topic_type:
- apiref
api_name:
- IVMVirtualPC.FindVirtualMachine
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bc5e5702738e16fa7b4f4a263264b0574966d1fd
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104105202"
---
# <a name="ivmvirtualpcfindvirtualmachine-method"></a>IVMVirtualPC :: FindVirtualMachine, méthode

\[Windows Virtual PC n’est plus disponible pour une utilisation à partir de Windows 8. Au lieu de cela, utilisez le [fournisseur WMI Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]

Récupère un objet ordinateur virtuel qui correspond à la configuration demandée.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT FindVirtualMachine(
  [in]          BSTR              configurationName,
  [out, retval] IVMVirtualMachine **virtualMachine
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*ConfigurationName* \[ dans\]
</dt> <dd>

Nom de l’ordinateur virtuel à trouver.

</dd> <dt>

*VirtualMachine* \[ out, retval\]
</dt> <dd>

Pointeur vers un nouvel objet [**IVMVirtualMachine**](ivmvirtualmachine.md) qui représente cet ordinateur virtuel.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Cette méthode peut retourner l’une de ces valeurs.



| Code/valeur de retour                                                                                                                                                                        | Description                                                                                     |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> <dt>0</dt> </dl>                                              | L'opération a réussi.<br/>                                                        |
| <dl> <dt>**S \_ FALSe**</dt> <dt>1</dt> </dl>                                           | La configuration spécifiée est introuvable.<br/>                                      |
| <dl> <dt>**E \_ POINTEUR**</dt> <dt>0x80004003</dt> </dl>                                | Le paramètre *ConfigurationName* n’est pas valide, ou *VirtualMachine* a la **valeur null**.<br/>       |
| <dl> <dt>**DISP \_ E \_ exception**</dt> <dt>0x80020009</dt> </dl>                        | Une erreur inattendue s’est produite.<br/>                                                    |
| <dl> <dt>**Ordinateur virtuel \_ \_Virtualisation matérielle E \_ \_ désactivée**</dt> <dt>0xA0040951</dt> </dl> | Le processeur ne prend pas en charge les extensions avez (Hardware Accelerated Virtualization).<br/> |



 

## <a name="remarks"></a>Notes

Les noms de machine virtuelle ne respectent pas la casse, par exemple, « MyVM » et « MyVM » font référence à la même machine virtuelle.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Applications de \[ Bureau Windows 7 uniquement\]<br/>                                                    |
| Serveur minimal pris en charge<br/> | Aucun pris en charge<br/>                                                                     |
| Fin de la prise en charge des clients<br/>    | Windows 7<br/>                                                                          |
| Produit<br/>                  | Windows Virtual PC<br/>                                                                 |
| En-tête<br/>                   | <dl> <dt>VPCCOMInterfaces. h</dt> </dl> |
| IID<br/>                      | IID \_ IVMVirtualPC est défini en tant que 236ba0d9-a24a-4292-A132-27c1421dfd01<br/>               |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**IVMVirtualPC**](ivmvirtualpc.md)
</dt> </dl>

 

