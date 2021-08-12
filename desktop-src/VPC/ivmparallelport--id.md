---
title: IVMParallelPort _ID, méthode (VPCCOMInterfaces. h)
description: Récupère l’identificateur interne du port parallèle.
ms.assetid: a0de74da-0e23-489e-8a89-8deba974e548
keywords:
- Méthode _ID Virtual PC
- _ID méthode Virtual PC, interface IVMParallelPort
- IVMParallelPort interface Virtual PC, méthode _ID
topic_type:
- apiref
api_name:
- IVMParallelPort._ID
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: df0c7b3eab7de47d182c94aa9b5fb35aef04e98495ef3e7b39d4547967f3438b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118593217"
---
# <a name="ivmparallelport_id-method"></a>IVMParallelPort :: \_ ID, méthode

\[Windows Virtual PC ne peut plus être utilisé à partir de Windows 8. Au lieu de cela, utilisez le [fournisseur WMI Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]

Récupère l’identificateur interne du port parallèle.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT _ID(
  [out] long *portID
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*port* \[ à\]
</dt> <dd>

Identificateur de port parallèle.

</dd> </dl>

## <a name="return-value"></a>Valeur renvoyée

Cette méthode peut retourner l’une de ces valeurs.



| Code/valeur de retour                                                                                                                                                 | Description                                                         |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> <dt>0</dt> </dl>                       | L'opération a réussi.<br/>                            |
| <dl> <dt>**E \_ POINTEUR**</dt> <dt>0x80004003</dt> </dl>         | Le paramètre a la **valeur null**.<br/>                               |
| <dl> <dt>**DISP \_ E \_ exception**</dt> <dt>0x80020009</dt> </dl> | Une erreur inattendue s’est produite.<br/>                        |
| <dl> <dt>**Ordinateur virtuel \_ \_Machine virtuelle \_**</dt> <dt>0xA0040207</dt> inconnue </dl> | La configuration de cet ordinateur virtuel n’est pas valide.<br/> |



 

## <a name="remarks"></a>Notes

Cette propriété n’est pas utilisable par les langages de script.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | applications de \[ bureau Windows 7 uniquement\]<br/>                                                    |
| Serveur minimal pris en charge<br/> | Aucun pris en charge<br/>                                                                     |
| Fin de la prise en charge des clients<br/>    | Windows 7<br/>                                                                          |
| Produit<br/>                  | Windows Virtual PC<br/>                                                                 |
| En-tête<br/>                   | <dl> <dt>VPCCOMInterfaces. h</dt> </dl> |
| IID<br/>                      | IID \_ IVMParallelPort est défini en tant que 097beecb-0a02-474F-abd6-298b22293fc6<br/>            |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**IVMParallelPort**](ivmparallelport.md)
</dt> </dl>

 

