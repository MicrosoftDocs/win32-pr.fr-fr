---
title: Méthode IVMVirtualPC GetConfigurationValue (VPCCOMInterfaces. h)
description: Récupère la valeur du paramètre de configuration spécifié.
ms.assetid: 4598b57c-9942-4b40-97b5-41ad9ec74bfa
keywords:
- Méthode GetConfigurationValue Virtual PC
- Méthode GetConfigurationValue Virtual PC, interface IVMVirtualPC
- IVMVirtualPC interface Virtual PC, méthode GetConfigurationValue
topic_type:
- apiref
api_name:
- IVMVirtualPC.GetConfigurationValue
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 11851e2dc2e51c0dc5eed876fc755655ed488554
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104105199"
---
# <a name="ivmvirtualpcgetconfigurationvalue-method"></a>IVMVirtualPC :: GetConfigurationValue, méthode

\[Windows Virtual PC n’est plus disponible pour une utilisation à partir de Windows 8. Au lieu de cela, utilisez le [fournisseur WMI Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]

Récupère la valeur du paramètre de configuration spécifié.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT GetConfigurationValue(
  [in]          BSTR    preferenceKey,
  [out, retval] VARIANT *preferenceValue
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*preferenceKey* \[ dans\]
</dt> <dd>

Clé utilisée pour identifier la préférence, telle qu’elle est stockée dans le fichier de configuration.

</dd> <dt>

*preferenceValue* \[ out, retval\]
</dt> <dd>

Valeur de préférence. Ce paramètre peut être l’un des types de **variantes** suivants : VT **\_ Array** \| **VT \_ UI1** (RAW bytes), **VT \_ BSTR** (String), **VT \_ I4** (Integer) ou **VT \_ bool** (Boolean).

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Cette méthode peut retourner l’une de ces valeurs.



| Code/valeur de retour                                                                                                                                                                        | Description                                                                                     |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> <dt>0</dt> </dl>                                              | L'opération a réussi.<br/>                                                        |
| <dl> <dt>**E \_ POINTEUR**</dt> <dt>0x80004003</dt> </dl>                                | Le paramètre *preferenceKey* ou *PreferenceValue* a la **valeur null**.<br/>                      |
| <dl> <dt>**Ordinateur virtuel \_ E \_ Préférences \_ \_ introuvables**</dt> <dt>0xa0040300</dt> </dl>                   | La préférence est introuvable.<br/>                                                        |
| <dl> <dt>**Ordinateur virtuel \_ \_Virtualisation matérielle E \_ \_ désactivée**</dt> <dt>0xA0040951</dt> </dl> | Le processeur ne prend pas en charge les extensions avez (Hardware Accelerated Virtualization).<br/> |
| <dl> <dt>**DISP \_ E \_ exception**</dt> <dt>0x80020009</dt> </dl>                        | Une erreur inattendue s’est produite.<br/>                                                    |



 

## <a name="remarks"></a>Notes

Cette méthode fournit un accès de bas niveau à toute valeur de préférence pour l’utilisateur actuel. Il peut être utilisé pour récupérer les valeurs de préférence pour les clés définies par le client.

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

 

