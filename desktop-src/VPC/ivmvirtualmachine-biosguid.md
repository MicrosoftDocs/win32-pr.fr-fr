---
title: IVMVirtualMachine BIOSGUID, propriété (VPCCOMInterfaces. h)
description: GUID du BIOS.
ms.assetid: d866838d-31e9-41f1-be57-43e778b9db95
keywords:
- BIOSGUID propriété Virtual PC
- BIOSGUID, propriété Virtual PC, IVMVirtualMachine, interface
- IVMVirtualMachine interface Virtual PC, propriété BIOSGUID
topic_type:
- apiref
api_name:
- IVMVirtualMachine.BIOSGUID
- IVMVirtualMachine.get_BIOSGUID
- IVMVirtualMachine.put_BIOSGUID
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 10263e32ab71c2a5b9533b3dde6547f774d6b302
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103843510"
---
# <a name="ivmvirtualmachinebiosguid-property"></a>IVMVirtualMachine :: BIOSGUID, propriété

\[Windows Virtual PC n’est plus disponible pour une utilisation à partir de Windows 8. Au lieu de cela, utilisez le [fournisseur WMI Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]

Récupère et définit le GUID du BIOS.

Cette propriété est en lecture/écriture.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT put_BIOSGUID(
  [in]          BSTR biosGUID
);

HRESULT get_BIOSGUID(
  [out, retval] BSTR *biosGUID
);
```



## <a name="property-value"></a>Valeur de la propriété

Spécifie le GUID du BIOS. Incluez les accolades gauche et droite autour des chiffres hexadécimaux.

## <a name="error-codes"></a>Codes d’erreur



| Nom/valeur                                                                                                                                                               | Signification                                                        |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------|
| <dl> <dt>S \_ OK</dt> <dt>0</dt> </dl>                                  | L'opération a réussi.<br/>                       |
| <dl> <dt>E \_ POINTEUR</dt> <dt>0x80004003</dt> </dl>                    | Le paramètre a la **valeur null**.<br/>                          |
| <dl> <dt>E \_ INVALIDARG</dt> <dt>0x80000003</dt> </dl>                 | Le paramètre n’est pas valide ou est une chaîne vide.<br/>   |
| <dl> <dt>Ordinateur virtuel \_ \_Machine virtuelle \_ </dt> <dt>0xA0040207</dt> inconnue </dl>            | La configuration est inconnue.<br/>                       |
| <dl> <dt>Ordinateur virtuel \_ \_Machine virtuelle \_ en cours d’exécution \_ ou \_ </dt> <dt>0xA004020B</dt> </dl> | L’ordinateur virtuel est dans un État en cours d’exécution ou enregistré.<br/> |
| <dl> <dt>DISP \_ E \_ exception</dt> <dt>0x80020009</dt> </dl>            | Une erreur inattendue s’est produite.<br/>                   |



## <a name="remarks"></a>Notes

Cette propriété ne contient pas d’informations valides tant que l’ordinateur virtuel n’a pas démarré pour la première fois. Une chaîne vide est retournée si elle est lue avant le démarrage initial.

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

 

