---
title: Méthode de déconnexion IVMGuestOS (VPCCOMInterfaces. h)
description: Déconnecte tous les utilisateurs du système d’exploitation invité.
ms.assetid: 224aa7cb-0892-4e8a-84bd-78dd5cb724df
keywords:
- Méthode de fermeture de session Virtual PC
- Méthode de déconnexion Virtual PC, interface IVMGuestOS
- IVMGuestOS interface Virtual PC, méthode Logoff
topic_type:
- apiref
api_name:
- IVMGuestOS.Logoff
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 20c67e917cc9ff93d162bc340185f426fe9eee3d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104033219"
---
# <a name="ivmguestoslogoff-method"></a>IVMGuestOS :: Logoff, méthode

\[Windows Virtual PC n’est plus disponible pour une utilisation à partir de Windows 8. Au lieu de cela, utilisez le [fournisseur WMI Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]

Déconnecte tous les utilisateurs du système d’exploitation invité.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT Logoff(
  [out, retval] IVMTask **outLogoffTask
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*outLogoffTask* \[ out, retval\]
</dt> <dd>

Objet [**IVMTask**](ivmtask.md) utilisé pour suivre la progression de l’exécution de la séquence de fermeture de session.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Cette méthode peut retourner l’une de ces valeurs.



| Code/valeur de retour                                                                                                                                                                          | Description                                                                             |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> <dt>0</dt> </dl>                                                | L'opération a réussi.<br/>                                                |
| <dl> <dt>**DISP \_ E \_ exception**</dt> <dt>0x80020009</dt> </dl>                          | Une erreur inattendue s’est produite.<br/>                                            |
| <dl> <dt>**E \_ POINTEUR**</dt> <dt>0x80004003</dt> </dl>                                  | Le paramètre a la **valeur null**.<br/>                                                   |
| <dl> Valeur <dt>**HRESULT \_ À partir de \_ Win32 ( \_ accès à l’erreur \_ refusé)**</dt> <dt>0x80070005</dt> </dl> | L’appelant doit disposer des autorisations d’accès en exécution pour cette machine virtuelle.<br/>                 |
| <dl> <dt>**Ordinateur virtuel \_ E \_ a \_ expiré**</dt> <dt>0xA0040202</dt> </dl>                           | L’opération ne s’est pas terminée en temps opportun.<br/>                           |
| <dl> <dt>**Ordinateur virtuel \_ La \_ fonctionnalité d’ajouts E \_ \_ n’est pas disponible \_**</dt> <dt>0xA0040505</dt> </dl>       | La fonctionnalité composants d’intégration n’est pas installée sur cette machine virtuelle.<br/> |
| <dl> <dt>**Ordinateur virtuel \_ \_Machine virtuelle \_ non \_ exécutée**</dt> <dt>0xA0040206</dt> </dl>                     | L’ordinateur virtuel (VM) doit être en cours d’exécution pour cette opération.<br/>                 |
| <dl> <dt>**Ordinateur virtuel \_ \_Machine virtuelle \_**</dt> <dt>0xA0040207</dt> inconnue </dl>                          | La configuration est inconnue.<br/>                                                |



 

## <a name="remarks"></a>Notes

`HRESULT_FROM_WIN32(ERROR_NO_SUCH_LOGON_SESSION)` (0x80070520) est retourné via la propriété [**Error**](ivmtask-error.md) de l’objet [**IVMTask**](ivmtask.md) retourné il n’y a aucune session de connexion dans le système d’exploitation invité.

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

 

