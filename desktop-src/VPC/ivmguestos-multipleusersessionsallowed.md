---
title: IVMGuestOS propriété MultipleUserSessionsAllowed
description: Détermine si plusieurs sessions utilisateur simultanées sont autorisées dans le système d’exploitation invité.
ms.assetid: 8a4163bf-b805-4cf0-b785-ee82e8374ef6
keywords:
- MultipleUserSessionsAllowed propriété Virtual PC
- MultipleUserSessionsAllowed, propriété Virtual PC, IVMGuestOS, interface
- IVMGuestOS interface Virtual PC, propriété MultipleUserSessionsAllowed
topic_type:
- apiref
api_name:
- IVMGuestOS.MultipleUserSessionsAllowed
- IVMGuestOS.get_MultipleUserSessionsAllowed
api_location:
- IVMGuestOS.idl
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f725a626ae13caaa36acd598694fef2f3b03e697
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104103969"
---
# <a name="ivmguestosmultipleusersessionsallowed-property"></a>IVMGuestOS :: MultipleUserSessionsAllowed, propriété

\[Windows Virtual PC n’est plus disponible pour une utilisation à partir de Windows 8. Au lieu de cela, utilisez le [fournisseur WMI Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]

Détermine si plusieurs sessions utilisateur simultanées sont autorisées dans le système d’exploitation invité.

Cette propriété est en lecture seule.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT get_MultipleUserSessionsAllowed(
  [out, retval] VARIANT_BOOL *sessionStatus
);
```



## <a name="property-value"></a>Valeur de la propriété

**Variante \_ TRUE** si plusieurs sessions utilisateur simultanées sont autorisées dans le système d’exploitation invité, **variante \_ false** dans le cas contraire.

## <a name="error-codes"></a>Codes d’erreur



| Nom/valeur                                                                                                                                                                       | Signification                                                                                                                        |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>S \_ OK</dt> <dt>0</dt> </dl>                                          | L'opération a réussi.<br/>                                                                                       |
| <dl> <dt>S \_ FALSe</dt> <dt>1</dt> </dl>                                       | Services Bureau à distance (anciennement « services Terminal Server ») n’est pas encore initialisé dans le système d’exploitation invité.<br/> |
| <dl> <dt>E \_ POINTEUR</dt> <dt>0x80004003</dt> </dl>                            | Le paramètre *sessionStatus* a la **valeur null**.<br/>                                                                          |
| <dl> <dt>Ordinateur virtuel \_ \_Machine virtuelle \_ non \_ exécutée</dt> <dt>0xA0040206</dt> </dl>               | L’ordinateur virtuel n’est pas en cours d’exécution.<br/>                                                                                 |
| <dl> <dt>Ordinateur virtuel \_ La \_ fonctionnalité d’ajouts E \_ \_ n’est pas disponible \_ </dt> <dt>0xA0040505</dt> </dl> | Les composants d’intégration ne sont pas installés sur cet ordinateur virtuel.<br/>                                                   |
| <dl> <dt>DISP \_ E \_ exception</dt> <dt>0x80020009</dt> </dl>                    | Une erreur inattendue s’est produite.<br/>                                                                                   |



## <a name="remarks"></a>Notes

La valeur de cette propriété n’est pas valide, sauf si la propriété [**TerminalServicesInitialized**](ivmguestos-terminalservicesinitialized.md) est définie sur **\_ true**.

Pour les systèmes d’exploitation clients Windows, **MultipleUserSessionsAllowed** a la **\_ valeur true** si le changement rapide d’utilisateur est pris en charge. Pour les systèmes d’exploitation Windows Server, **MultipleUserSessionsAllowed** a la **\_ valeur true** si services Bureau à distance (autrefois appelé « services Terminal Server ») est installé et activé.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Applications de \[ Bureau Windows 7 uniquement\]<br/>                                                |
| Serveur minimal pris en charge<br/> | Aucun pris en charge<br/>                                                                 |
| Fin de la prise en charge des clients<br/>    | Windows 7<br/>                                                                      |
| MIDL<br/>                      | <dl> <dt>IVMGuestOS. idl</dt> </dl> |
| IID<br/>                      | IID \_ IVMGuestOS est défini en tant que 99fea0db-4880-499a-B6D8-73dff9bc91be<br/>             |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**IVMGuestOS**](ivmguestos.md)
</dt> </dl>

 

