---
title: Méthode IVMVirtualPC DeleteVirtualMachine (VPCCOMInterfaces. h)
description: Supprime une configuration d’ordinateur virtuel.
ms.assetid: fc2562f3-6a83-4a40-b800-0bc2692beae8
keywords:
- Méthode DeleteVirtualMachine Virtual PC
- Méthode DeleteVirtualMachine Virtual PC, interface IVMVirtualPC
- IVMVirtualPC interface Virtual PC, méthode DeleteVirtualMachine
topic_type:
- apiref
api_name:
- IVMVirtualPC.DeleteVirtualMachine
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ee9c1591ccd736099fab04cce31c8a8b77b5fb06
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "106515075"
---
# <a name="ivmvirtualpcdeletevirtualmachine-method"></a>IVMVirtualPC ::D méthode eleteVirtualMachine

\[Windows Virtual PC n’est plus disponible pour une utilisation à partir de Windows 8. Au lieu de cela, utilisez le [fournisseur WMI Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]

Supprime une configuration d’ordinateur virtuel.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT DeleteVirtualMachine(
  [in] IVMVirtualMachine *virtualMachine
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*VirtualMachine* \[ dans\]
</dt> <dd>

Pointeur vers un objet [**IVMVirtualMachine**](ivmvirtualmachine.md) représentant la configuration de l’ordinateur virtuel à supprimer.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Cette méthode peut retourner l’une de ces valeurs.



| Code/valeur de retour                                                                                                                                                                        | Description                                                                                     |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> <dt>0</dt> </dl>                                              | L'opération a réussi.<br/>                                                        |
| <dl> <dt>**S \_ FALSe**</dt> <dt>1</dt> </dl>                                           | La configuration spécifiée est introuvable.<br/>                                      |
| <dl> <dt>**E \_ POINTEUR**</dt> <dt>0x80004003</dt> </dl>                                | Le paramètre *VirtualMachine* a la **valeur null**.<br/>                                         |
| <dl> <dt>**Ordinateur virtuel \_ \_Machine virtuelle E \_ exécutant**</dt> <dt>0xA0040500</dt> </dl>                        | La machine virtuelle est en cours d’exécution.<br/>                                                      |
| <dl> <dt>**Ordinateur virtuel \_ \_Virtualisation matérielle E \_ \_ désactivée**</dt> <dt>0xA0040951</dt> </dl> | Le processeur ne prend pas en charge les extensions avez (Hardware Accelerated Virtualization).<br/> |
| <dl> <dt>**DISP \_ E \_ exception**</dt> <dt>0x80020009</dt> </dl>                        | Une erreur inattendue s’est produite.<br/>                                                    |



 

## <a name="remarks"></a>Notes

Seules les machines virtuelles arrêtées peuvent être supprimées. Notez que les données d’état enregistré ou de lecteur d’annulation existantes pour cette configuration seront supprimées en plus du fichier de configuration.

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

 

