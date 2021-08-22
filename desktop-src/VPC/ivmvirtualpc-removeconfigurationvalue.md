---
title: Méthode IVMVirtualPC RemoveConfigurationValue (VPCCOMInterfaces. h)
description: Supprime la valeur du paramètre de configuration spécifié.
ms.assetid: 07bafa5e-bf62-45bf-af4e-a66050f5afad
keywords:
- Méthode RemoveConfigurationValue Virtual PC
- Méthode RemoveConfigurationValue Virtual PC, interface IVMVirtualPC
- IVMVirtualPC interface Virtual PC, méthode RemoveConfigurationValue
topic_type:
- apiref
api_name:
- IVMVirtualPC.RemoveConfigurationValue
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 281837394967a15bce40173ead0ca02be66eb046bf7c15b63fdded57c2ecef84
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118998535"
---
# <a name="ivmvirtualpcremoveconfigurationvalue-method"></a>IVMVirtualPC :: RemoveConfigurationValue, méthode

\[Windows Virtual PC ne peut plus être utilisé à partir de Windows 8. Au lieu de cela, utilisez le [fournisseur WMI Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]

Supprime la valeur du paramètre de configuration spécifié.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT RemoveConfigurationValue(
  [in] BSTR preferenceKey
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*preferenceKey* \[ dans\]
</dt> <dd>

Clé utilisée pour identifier la préférence, telle qu’elle est stockée dans le fichier de configuration.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Cette méthode peut retourner l’une de ces valeurs.



| Code/valeur de retour                                                                                                                                                                        | Description                                                                                     |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> <dt>0</dt> </dl>                                              | L'opération a réussi.<br/>                                                        |
| <dl> <dt>**E \_ POINTEUR**</dt> <dt>0x80004003</dt> </dl>                                | Le paramètre *preferenceKey* a la **valeur null**.<br/>                                           |
| <dl> <dt>**E \_ INVALIDARG**</dt> <dt>0x80000003</dt> </dl>                             | Le paramètre *preferenceKey* n’est pas valide ou est une chaîne vide.<br/>                    |
| <dl> <dt>**Ordinateur virtuel \_ E \_ Préférences \_ \_ introuvables**</dt> <dt>0xA0040300</dt> </dl>                   | La préférence est introuvable.<br/>                                                        |
| <dl> <dt>**Ordinateur virtuel \_ \_Virtualisation matérielle E \_ \_ désactivée**</dt> <dt>0xA0040951</dt> </dl> | Le processeur ne prend pas en charge les extensions avez (Hardware Accelerated Virtualization).<br/> |
| <dl> <dt>**DISP \_ E \_ exception**</dt> <dt>0x80020009</dt> </dl>                        | Une erreur inattendue s’est produite.<br/>                                                    |



 

## <a name="remarks"></a>Remarques

Cette méthode fournit un accès de bas niveau à toute valeur de préférence pour l’utilisateur actuel. Il peut être utilisé pour supprimer des valeurs de préférence pour les clés définies par le client.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | applications de \[ bureau Windows 7 uniquement\]<br/>                                                    |
| Serveur minimal pris en charge<br/> | Aucun pris en charge<br/>                                                                     |
| Fin de la prise en charge des clients<br/>    | Windows 7<br/>                                                                          |
| Produit<br/>                  | Windows Virtual PC<br/>                                                                 |
| En-tête<br/>                   | <dl> <dt>VPCCOMInterfaces. h</dt> </dl> |
| IID<br/>                      | IID \_ IVMVirtualPC est défini en tant que 236ba0d9-a24a-4292-A132-27c1421dfd01<br/>               |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**IVMVirtualPC**](ivmvirtualpc.md)
</dt> </dl>

 

