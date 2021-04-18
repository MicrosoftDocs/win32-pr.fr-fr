---
title: Méthode IVMGuestOS IsUserLoggedOn (VPCCOMInterfaces. h)
description: Détermine si la session demandée est présente.
ms.assetid: 28035e30-023a-4ec2-88ef-43fe22f6d14e
keywords:
- Méthode IsUserLoggedOn Virtual PC
- Méthode IsUserLoggedOn Virtual PC, interface IVMGuestOS
- IVMGuestOS interface Virtual PC, méthode IsUserLoggedOn
topic_type:
- apiref
api_name:
- IVMGuestOS.IsUserLoggedOn
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4eeb0482d7d3ac45b67a863948526b57d6c6e412
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "106527155"
---
# <a name="ivmguestosisuserloggedon-method"></a>IVMGuestOS :: IsUserLoggedOn, méthode

\[Windows Virtual PC n’est plus disponible pour une utilisation à partir de Windows 8. Au lieu de cela, utilisez le [fournisseur WMI Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]

Détermine si la session demandée est présente.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT IsUserLoggedOn(
  [in]          long         inRailSession,
  [out, retval] VARIANT_BOOL *outSessionPresent
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*inRailSession* \[ dans\]
</dt> <dd>

Définissez la valeur 0 pour une session de rail ou 1 pour une session RDP.

</dd> <dt>

*outSessionPresent* \[ out, retval\]
</dt> <dd>

A la valeur **Variant \_ true** si la session est présente **et \_ false** dans le cas contraire.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Cette méthode peut retourner l’une de ces valeurs.



| Code/valeur de retour                                                                                                                                                                       | Description                                                                |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> <dt>0</dt> </dl>                                             | L'opération a réussi.<br/>                                   |
| <dl> <dt>**E \_ POINTEUR**</dt> <dt>0x80004003</dt> </dl>                               | Le paramètre a la **valeur null**.<br/>                                      |
| <dl> <dt>**E \_ INVALIDARG**</dt> <dt>0x80000003</dt> </dl>                            | Le paramètre *outSessionPresent* n’est pas valide ou a la **valeur null**.<br/>  |
| <dl> <dt>**DISP \_ E \_ exception**</dt> <dt>0x80020009</dt> </dl>                       | Une erreur inattendue s’est produite.<br/>                               |
| <dl> Valeur <dt>**HRESULT \_ À partir de \_ Win32 (erreur \_ OUTOFMEMORY)**</dt> <dt>0x8007000E</dt> </dl> | La mémoire disponible est insuffisante pour effectuer cette requête.<br/>  |
| <dl> <dt>**Ordinateur virtuel \_ E \_ a \_ expiré**</dt> <dt>0xA0040202</dt> </dl>                        | L’opération ne s’est pas terminée en temps opportun.<br/>              |
| <dl> <dt>**Ordinateur virtuel \_ \_Machine virtuelle \_ non \_ exécutée**</dt> <dt>0xA0040206</dt> </dl>                  | L’ordinateur virtuel (VM) doit être en cours d’exécution pour cette opération.<br/>    |
| <dl> <dt>**Ordinateur virtuel \_ La \_ fonctionnalité d’ajouts E \_ \_ n’est pas disponible \_**</dt> <dt>0xA0040505</dt> </dl>    | La fonctionnalité composants d’intégration n’est pas installée sur cette machine virtuelle.<br/> |
| <dl> <dt>**Ordinateur virtuel \_ 0xA00400507 \_ en \_ pause de la machine virtuelle E**</dt> <dt></dt> </dl>                       | La machine virtuelle est suspendue.<br/>                                               |



 

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Applications de \[ Bureau Windows 7 uniquement\]<br/>                                                    |
| Serveur minimal pris en charge<br/> | Aucun pris en charge<br/>                                                                     |
| Fin de la prise en charge des clients<br/>    | Windows 7<br/>                                                                          |
| Produit<br/>                  | Windows Virtual PC<br/>                                                                 |
| En-tête<br/>                   | <dl> <dt>VPCCOMInterfaces. h</dt> </dl> |
| IID<br/>                      | IID \_ IVMGuestOS est défini en tant que 99fea0db-4880-499a-B6D8-73dff9bc91be<br/>                 |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**IVMGuestOS**](ivmguestos.md)
</dt> </dl>

 

