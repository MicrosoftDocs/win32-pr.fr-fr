---
title: Propriété IVMVirtualMachine Name (VPCCOMInterfaces. h)
description: Nom de la configuration de la machine virtuelle.
ms.assetid: 90acedbf-4159-48a3-a9e9-6f1ee00dab8b
keywords:
- Propriété de nom Virtual PC
- Propriété de nom Virtual PC, interface IVMVirtualMachine
- IVMVirtualMachine interface Virtual PC, propriété Name
topic_type:
- apiref
api_name:
- IVMVirtualMachine.Name
- IVMVirtualMachine.get_Name
- IVMVirtualMachine.put_Name
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5219e6fcb24805feb0370bd157d014767a9348e87e500d8c94fa26ff502b6597
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120006799"
---
# <a name="ivmvirtualmachinename-property"></a>IVMVirtualMachine :: Name, propriété

\[Windows Virtual PC ne peut plus être utilisé à partir de Windows 8. Au lieu de cela, utilisez le [fournisseur WMI Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]

Récupère et définit le nom de la configuration de l’ordinateur virtuel.

Cette propriété est en lecture/écriture.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT put_Name(
  [in]          BSTR virtualMachineName
);

HRESULT get_Name(
  [out, retval] BSTR *virtualMachineName
);
```



## <a name="property-value"></a>Valeur de la propriété

Spécifie le nom de la configuration de l’ordinateur virtuel. La longueur du nom ne peut pas dépasser 80 caractères et la longueur totale du chemin d’accès complet qui comprend le fichier de configuration du nom de l’ordinateur virtuel ne peut pas dépasser le **\_ chemin d’accès maximal** (260) caractères.

## <a name="error-codes"></a>Codes d’erreur



| Nom/valeur                                                                                                                                                                    | Signification                                                                                         |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------|
| <dl> <dt>S \_ OK</dt> <dt>0</dt> </dl>                                       | L'opération a réussi.<br/>                                                        |
| <dl> <dt>E \_ POINTEUR</dt> <dt>0x80004003</dt> </dl>                         | Le paramètre a la **valeur null**.<br/>                                                           |
| <dl> <dt>E \_ INVALIDARG</dt> <dt>0x80000003</dt> </dl>                      | Le paramètre n’est pas valide ou est une chaîne vide.<br/>                                    |
| <dl> <dt>Ordinateur virtuel \_ \_Machine virtuelle \_ </dt> <dt>0xA0040207</dt> inconnue </dl>                 | La configuration est inconnue.<br/>                                                        |
| <dl> <dt>Ordinateur virtuel \_ E/r 0xA0040302 \_ \_ \_ active VM</dt> <dt></dt> </dl>            | L’ordinateur virtuel est en cours d’exécution ou enregistré.<br/>                                             |
| <dl> <dt>Ordinateur virtuel \_ E \_ config \_ sans \_ nom</dt> <dt>0xA0040400</dt> </dl>            | Le paramètre *virtualMachineName* est vide.<br/>                                         |
| <dl> <dt>Ordinateur virtuel \_ Nom de la \_ configuration E \_ \_ trop \_ long</dt> <dt>0xA00400401</dt> </dl>    | Le paramètre contient trop de caractères.<br/>                                          |
| <dl> <dt>Ordinateur virtuel \_ Nom de la configuration E 0xA0040402 \_ \_ \_ \_ char non valide</dt> <dt></dt> </dl> | Le paramètre contient l’un des caractères non valides suivants : « \* ?: <>/ \| \\ ».<br/> |
| <dl> <dt>Ordinateur virtuel \_ \_ \_ \_ Nom en double de la configuration E</dt> <dt>0xA0040403</dt> </dl>     | Le nom spécifié existe déjà en tant que nom d’un autre ordinateur virtuel.<br/>            |
| <dl> <dt>DISP \_ E \_ exception</dt> <dt>0x80020009</dt> </dl>                 | Une erreur inattendue s’est produite.<br/>                                                    |



## <a name="remarks"></a>Remarques

Les noms de machine virtuelle ne respectent pas la casse, par exemple « MyVM » et « MyVM » font référence à la même machine virtuelle. Il s’agit de la propriété par défaut pour [**IVMVirtualMachine**](ivmvirtualmachine.md).

Si VPC.exe est en cours d’exécution et que la machine virtuelle est enregistrée, la définition de la propriété **Name** échouera. Si VPC.exe n’est pas en cours d’exécution et que la machine virtuelle est enregistrée, la définition de la propriété **Name** est réussie lors du prochain démarrage de VPC.exe.

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

 

