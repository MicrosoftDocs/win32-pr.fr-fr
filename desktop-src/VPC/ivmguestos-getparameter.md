---
title: IVMGuestOS GetParameter, méthode (VPCCOMInterfaces. h)
description: Récupère un paramètre nommé dans le système d’exploitation invité.
ms.assetid: d4d5acbd-fa19-4eb2-af75-2c94e5f6f7f0
keywords:
- Méthode GetParameter Virtual PC
- Méthode GetParameter Virtual PC, interface IVMGuestOS
- IVMGuestOS interface Virtual PC, GetParameter, méthode
topic_type:
- apiref
api_name:
- IVMGuestOS.GetParameter
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 955b70986640fab8cefe9f02b28b02015397c964f1b10fc26057533fc79a3809
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117753561"
---
# <a name="ivmguestosgetparameter-method"></a>IVMGuestOS :: GetParameter, méthode

\[Windows Virtual PC ne peut plus être utilisé à partir de Windows 8. Au lieu de cela, utilisez le [fournisseur WMI Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]

Récupère un paramètre nommé dans le système d’exploitation invité.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT GetParameter(
  [in]          BSTR inParameterName,
  [out, retval] BSTR *outParameterValue
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*inParameterName* \[ dans\]
</dt> <dd>

Nom du paramètre. Sa longueur doit être comprise entre 1 et 255 caractères et ne peut pas contenir de barre oblique inverse ( \\ ).

</dd> <dt>

*outParameterValue* \[ out, retval\]
</dt> <dd>

Valeur du paramètre.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Cette méthode peut retourner l’une de ces valeurs.



| Code/valeur de retour                                                                                                                                                                    | Description                                                                  |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> <dt>0</dt> </dl>                                          | L'opération a réussi.<br/>                                     |
| <dl> <dt>**E \_ INVALIDARG**</dt> <dt>0x80000003</dt> </dl>                         | Un paramètre n’est pas valide ou n’est pas spécifié.<br/>                        |
| <dl> <dt>**E \_ POINTEUR**</dt> <dt>0x80004003</dt> </dl>                            | Le paramètre a la **valeur null**.<br/>                                        |
| <dl> <dt>**Ordinateur virtuel \_ E \_ a \_ expiré**</dt> <dt>0xA0040202</dt> </dl>                     | L’opération ne s’est pas terminée en temps opportun.<br/>                |
| <dl> <dt>**Ordinateur virtuel \_ \_Machine virtuelle \_ non \_ exécutée**</dt> <dt>0xA0040206</dt> </dl>               | L’ordinateur virtuel n’est pas en cours d’exécution.<br/>                               |
| <dl> <dt>**Ordinateur virtuel \_ 0xA00400507 \_ en \_ pause de la machine virtuelle E**</dt> <dt></dt> </dl>                    | L’ordinateur virtuel est en pause.<br/>                                    |
| <dl> <dt>**Ordinateur virtuel \_ La \_ fonctionnalité d’ajouts E \_ \_ n’est pas disponible \_**</dt> <dt>0xA0040505</dt> </dl> | Les composants d’intégration ne sont pas installés sur cet ordinateur virtuel.<br/> |
| <dl> <dt>**DISP \_ E \_ exception**</dt> <dt>0x80020009</dt> </dl>                    | Une erreur inattendue s’est produite.<br/>                                 |



 

## <a name="remarks"></a>Remarques

L’ordinateur virtuel doit être en cours d’exécution et les composants d’intégration doivent être installés lorsque cette méthode est appelée. cette méthode est uniquement prise en charge pour les systèmes d’exploitation invités basés sur Windows.

Avec les composants d’intégration installés, la clé suivante est automatiquement ajoutée au registre du système d’exploitation invité :

**HKEY \_ local \_ machine \\ Software logiciel \\ Microsoft \\ Virtual \\ machine \\ paramètres invité**

Lorsque le système d’exploitation invité démarre, les valeurs de chaîne de Registre suivantes sont renseignées dans la clé des **paramètres** :

-   **HostName**
-   **PhysicalHostName**
-   **PhysicalHostNameFullyQualified**
-   **VirtualMachineName**

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | applications de \[ bureau Windows 7 uniquement\]<br/>                                                    |
| Serveur minimal pris en charge<br/> | Aucun pris en charge<br/>                                                                     |
| Fin de la prise en charge des clients<br/>    | Windows 7<br/>                                                                          |
| Produit<br/>                  | Windows Virtual PC<br/>                                                                 |
| En-tête<br/>                   | <dl> <dt>VPCCOMInterfaces. h</dt> </dl> |
| IID<br/>                      | IID \_ IVMGuestOS est défini en tant que 99fea0db-4880-499a-B6D8-73dff9bc91be<br/>                 |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**IVMGuestOS**](ivmguestos.md)
</dt> </dl>

 

