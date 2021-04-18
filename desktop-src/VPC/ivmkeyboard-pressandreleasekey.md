---
title: Méthode IVMKeyboard PressAndReleaseKey (VPCCOMInterfaces. h)
description: Simule une touche enfoncée, puis relâchée.
ms.assetid: 2a7fc36f-f1bf-4f1d-b8f7-ea5b167c82a7
keywords:
- Méthode PressAndReleaseKey Virtual PC
- Méthode PressAndReleaseKey Virtual PC, interface IVMKeyboard
- IVMKeyboard interface Virtual PC, méthode PressAndReleaseKey
topic_type:
- apiref
api_name:
- IVMKeyboard.PressAndReleaseKey
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a4adbcac2c79c02ce69584bbfdf21a6b08b350a3
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "106543053"
---
# <a name="ivmkeyboardpressandreleasekey-method"></a>IVMKeyboard ::P méthode ressAndReleaseKey

\[Windows Virtual PC n’est plus disponible pour une utilisation à partir de Windows 8. Au lieu de cela, utilisez le [fournisseur WMI Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]

Simule une touche enfoncée, puis relâchée.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT PressAndReleaseKey(
  [in] BSTR key
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*clé* \[ dans\]
</dt> <dd>

Code clé pour la touche à enfoncer et à libérer.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Cette méthode peut retourner l’une de ces valeurs.



| Code/valeur de retour                                                                                                                                                 | Description                                                                |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> <dt>0</dt> </dl>                       | L'opération a réussi.<br/>                                   |
| <dl> <dt>**E \_ POINTEUR**</dt> <dt>0x80004003</dt> </dl>         | Le paramètre a la **valeur null**.<br/>                                      |
| <dl> <dt>**E \_ INVALIDARG**</dt> <dt>0x80000003</dt> </dl>      | La chaîne spécifiée est vide ou contient un code de clé non valide.<br/> |
| <dl> <dt>**DISP \_ E \_ exception**</dt> <dt>0x80020009</dt> </dl> | Une erreur inattendue s’est produite.<br/>                               |



 

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Applications de \[ Bureau Windows 7 uniquement\]<br/>                                                    |
| Serveur minimal pris en charge<br/> | Aucun pris en charge<br/>                                                                     |
| Fin de la prise en charge des clients<br/>    | Windows 7<br/>                                                                          |
| Produit<br/>                  | Windows Virtual PC<br/>                                                                 |
| En-tête<br/>                   | <dl> <dt>VPCCOMInterfaces. h</dt> </dl> |
| IID<br/>                      | IID \_ IVMKeyboard est défini en tant que 00695f2e-c5ad-4d6e-B1ab-336ed121f8c4<br/>                |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**IVMKeyboard**](ivmkeyboard.md)
</dt> </dl>

 

