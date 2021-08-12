---
title: IVMGuestOS, méthode de redémarrage (VPCCOMInterfaces. h)
description: Redémarre le système d’exploitation invité.
ms.assetid: 328c7aa1-d9bd-452d-95dd-9f6a03fa8c9e
keywords:
- Redémarrage de la méthode Virtual PC
- Méthode de redémarrage de Virtual PC, interface IVMGuestOS
- IVMGuestOS interface Virtual PC, restart, méthode
topic_type:
- apiref
api_name:
- IVMGuestOS.Restart
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0b25d5fc2bec8c8a0a10425f63b6abc7c6363e8562b84376af4d053ec710e709
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118594007"
---
# <a name="ivmguestosrestart-method"></a>IVMGuestOS :: Restart, méthode

\[Windows Virtual PC ne peut plus être utilisé à partir de Windows 8. Au lieu de cela, utilisez le [fournisseur WMI Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]

Redémarre le système d’exploitation invité.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT Restart(
  [in]          VARIANT_BOOL inForced,
  [out, retval] IVMTask      **outRestartTask
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*inappliqué* \[ dans\]
</dt> <dd>

**Variante \_ TRUE** si un redémarrage forcé est requis et **Variant \_ false** dans le cas contraire.

</dd> <dt>

*outRestartTask* \[ out, retval\]
</dt> <dd>

Objet [**IVMTask**](ivmtask.md) utilisé pour suivre la progression de l’exécution de la séquence de redémarrage.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Cette méthode peut retourner l’une de ces valeurs.



| Code/valeur de retour                                                                                                                                                                    | Description                                                                |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> <dt>0</dt> </dl>                                          | L'opération a réussi.<br/>                                   |
| <dl> <dt>**E \_ POINTEUR**</dt> <dt>0x80004003</dt> </dl>                            | Le paramètre *outRestartTask* a la **valeur null**.<br/>                     |
| <dl> <dt>**DISP \_ E \_ exception**</dt> <dt>0x80020009</dt> </dl>                    | Une erreur inattendue s’est produite.<br/>                               |
| <dl> <dt>**Ordinateur virtuel \_ E \_ a \_ expiré**</dt> <dt>0xA0040202</dt> </dl>                     | L’opération ne s’est pas terminée en temps opportun.<br/>              |
| <dl> <dt>**Ordinateur virtuel \_ \_Machine virtuelle \_ non \_ exécutée**</dt> <dt>0xA0040206</dt> </dl>               | L’ordinateur virtuel (VM) doit être en cours d’exécution pour cette opération.<br/>    |
| <dl> <dt>**Ordinateur virtuel \_ \_Machine virtuelle \_**</dt> <dt>0xA0040207</dt> inconnue </dl>                    | La configuration est inconnue.<br/>                                   |
| <dl> <dt>**Ordinateur virtuel \_ La \_ fonctionnalité d’ajouts E \_ \_ n’est pas disponible \_**</dt> <dt>0xA0040505</dt> </dl> | La fonctionnalité composants d’intégration n’est pas installée sur cette machine virtuelle.<br/> |



 

## <a name="remarks"></a>Remarques

Les valeurs suivantes peuvent être retournées par le biais de la propriété [**Error**](ivmtask-error.md) de l’objet [**IVMTask**](ivmtask.md) retourné.



| Code d' [**erreur**](ivmtask-error.md) /valeur                                                                                                                                                                                                                                                                          | Description                                                                         |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------|
| <span id="HRESULT_FROM_WIN32_ERROR_ACCESS_DENIED___0x80070005_"></span><span id="hresult_from_win32_error_access_denied___0x80070005_"></span><span id="HRESULT_FROM_WIN32_ERROR_ACCESS_DENIED___0X80070005_"></span>`HRESULT_FROM_WIN32(ERROR_ACCESS_DENIED)` 0x80070005<br/>                             | L’appelant doit disposer des autorisations d’accès en exécution pour cette machine virtuelle.<br/>             |
| <span id="HRESULT_FROM_WIN32_ERROR_MACHINE_LOCKED___0x800704f7_"></span><span id="hresult_from_win32_error_machine_locked___0x800704f7_"></span><span id="HRESULT_FROM_WIN32_ERROR_MACHINE_LOCKED___0X800704F7_"></span>`HRESULT_FROM_WIN32(ERROR_MACHINE_LOCKED)` (0x800704f7)<br/>                         | L’ordinateur est verrouillé et ne peut pas être arrêté sans l’option forcer.<br/> |
| <span id="HRESULT_FROM_WIN32_ERROR_NOT_READY___0x80070015_"></span><span id="hresult_from_win32_error_not_ready___0x80070015_"></span><span id="HRESULT_FROM_WIN32_ERROR_NOT_READY___0X80070015_"></span>`HRESULT_FROM_WIN32(ERROR_NOT_READY)` (0x80070015)<br/>                                             | Le périphérique n’est pas prêt.<br/>                                                 |
| <span id="HRESULT_FROM_WIN32_ERROR_SHUTDOWN_IN_PROGRESS___0x8007045b_"></span><span id="hresult_from_win32_error_shutdown_in_progress___0x8007045b_"></span><span id="HRESULT_FROM_WIN32_ERROR_SHUTDOWN_IN_PROGRESS___0X8007045B_"></span>`HRESULT_FROM_WIN32(ERROR_SHUTDOWN_IN_PROGRESS)` (0x8007045b)<br/> | Un arrêt du système est en cours.<br/>                                        |



 

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

 

