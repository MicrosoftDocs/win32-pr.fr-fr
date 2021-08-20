---
title: IVMSerialPort _ID, méthode (VPCCOMInterfaces. h)
description: Identificateur interne du port série.
ms.assetid: c26c18dc-5491-4edf-9338-e4f3bf431084
keywords:
- Méthode _ID Virtual PC
- _ID méthode Virtual PC, interface IVMSerialPort
- IVMSerialPort interface Virtual PC, méthode _ID
topic_type:
- apiref
api_name:
- IVMSerialPort._ID
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7b55974319e4af48ae1a6f3554ae79557feaa5c8455e47b66e82e4d4cf02a801
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118123733"
---
# <a name="ivmserialport_id-method"></a>IVMSerialPort :: \_ ID, méthode

\[Windows Virtual PC ne peut plus être utilisé à partir de Windows 8. Au lieu de cela, utilisez le [fournisseur WMI Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]

Récupère l’identificateur interne du port série.

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

Identificateur du port série.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Cette méthode peut retourner l’une de ces valeurs.



| Code/valeur de retour                                                                                                                                                 | Description                                                         |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> <dt>0</dt> </dl>                       | L'opération a réussi.<br/>                            |
| <dl> <dt>**E \_ POINTEUR**</dt> <dt>0x80004003</dt> </dl>         | Le paramètre a la **valeur null**.<br/>                               |
| <dl> <dt>**DISP \_ E \_ exception**</dt> <dt>0x80020009</dt> </dl> | Une erreur inattendue s’est produite.<br/>                        |
| <dl> <dt>**Ordinateur virtuel \_ \_Machine virtuelle \_**</dt> <dt>0xA0040207</dt> inconnue </dl> | La configuration de cet ordinateur virtuel n’est pas valide.<br/> |



 

## <a name="remarks"></a>Remarques

Cette propriété n’est pas utilisable par les langages de script.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | applications de \[ bureau Windows 7 uniquement\]<br/>                                                    |
| Serveur minimal pris en charge<br/> | Aucun pris en charge<br/>                                                                     |
| Fin de la prise en charge des clients<br/>    | Windows 7<br/>                                                                          |
| Produit<br/>                  | Windows Virtual PC<br/>                                                                 |
| En-tête<br/>                   | <dl> <dt>VPCCOMInterfaces. h</dt> </dl> |
| IID<br/>                      | IID \_ IVMSerialPort est défini en tant que 2ce4460d-1d3f-4458-BF8B-44084b816815<br/>              |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**IVMSerialPort**](ivmserialport.md)
</dt> </dl>

 

