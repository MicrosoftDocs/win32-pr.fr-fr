---
title: Méthode IMsTscAxEvents OnLogonError
description: Appelée lorsqu’une erreur d’ouverture de session ou un autre événement d’ouverture de session se produit.
ms.assetid: 5af9656b-f99b-4535-ab83-6ecc9bc41808
ms.tgt_platform: multiple
keywords:
- Services Bureau à distance de la méthode OnLogonError
- Méthode OnLogonError Services Bureau à distance, interface IMsTscAxEvents
- Services Bureau à distance de l’interface IMsTscAxEvents, méthode OnLogonError
topic_type:
- apiref
api_name:
- IMsTscAxEvents.OnLogonError
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 29e2b7e13b4471b476ae00ff4cd810a7955c4e3224744435d37f5a962db834cd
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120125099"
---
# <a name="imstscaxeventsonlogonerror-method"></a>IMsTscAxEvents :: OnLogonError, méthode

Appelée lorsqu’une erreur d’ouverture de session ou un autre événement d’ouverture de session se produit.

## <a name="syntax"></a>Syntaxe


```C++
void OnLogonError(
  [in] LONG lError
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*lError* \[ dans\]
</dt> <dd>

Code d’erreur d’ouverture de session. Cette liste de codes n’est pas exhaustive.

<dt>

<span id="ARBITRATION_CODE_BUMP_OPTIONS"></span><span id="arbitration_code_bump_options"></span>

<span id="ARBITRATION_CODE_BUMP_OPTIONS"></span><span id="arbitration_code_bump_options"></span>**Arbitrage \_ \_ \_ Options de BOSSELAGE du code** (-5 (0xFFFFFFFB))


</dt> <dd>

Winlogon affiche la boîte de dialogue **conflit de session** .

</dd> <dt>

<span id="ARBITRATION_CODE_CONTINUE_LOGON"></span><span id="arbitration_code_continue_logon"></span>

<span id="ARBITRATION_CODE_CONTINUE_LOGON"></span><span id="arbitration_code_continue_logon"></span>**Arbitrage \_ L' \_ \_ ouverture de session du code continue** (-2 (0xfffffffe))


</dt> <dd>

Winlogon continue avec le processus d’ouverture de session.

</dd> <dt>

<span id="ARBITRATION_CODE_CONTINUE_TERMINATE"></span><span id="arbitration_code_continue_terminate"></span>

<span id="ARBITRATION_CODE_CONTINUE_TERMINATE"></span><span id="arbitration_code_continue_terminate"></span>**Arbitrage \_ \_ \_ Fin** de la poursuite du code (-3 (0xFFFFFFFD))


</dt> <dd>

Winlogon se termine en mode silencieux.

</dd> <dt>

<span id="ARBITRATION_CODE_NOPERM_DIALOG"></span><span id="arbitration_code_noperm_dialog"></span>

<span id="ARBITRATION_CODE_NOPERM_DIALOG"></span><span id="arbitration_code_noperm_dialog"></span>**Arbitrage \_ \_ \_ Boîte de dialogue code noperm** (-6 (0xFFFFFFFA))


</dt> <dd>

Winlogon affiche la boîte de dialogue **aucune autorisation** .

</dd> <dt>

<span id="ARBITRATION_CODE_REFUSED_DIALOG"></span><span id="arbitration_code_refused_dialog"></span>

<span id="ARBITRATION_CODE_REFUSED_DIALOG"></span><span id="arbitration_code_refused_dialog"></span>**Arbitrage \_ \_Boîte de \_ dialogue code refusé** (-7 (0xFFFFFFF9))


</dt> <dd>

Winlogon affiche la boîte de dialogue **déconnexion refusée** .

</dd> <dt>

<span id="ARBITRATION_CODE_RECONN_OPTIONS"></span><span id="arbitration_code_reconn_options"></span>

<span id="ARBITRATION_CODE_RECONN_OPTIONS"></span><span id="arbitration_code_reconn_options"></span>**Arbitrage \_ \_ \_ Options de rapprochement de code** (-4 (0xFFFFFFFC))


</dt> <dd>

Winlogon affiche la boîte de dialogue **reconnexion** .

</dd> <dt>

<span id="ERROR_CODE_ACCESS_DENIED"></span><span id="error_code_access_denied"></span>

<span id="ERROR_CODE_ACCESS_DENIED"></span><span id="error_code_access_denied"></span>**Erreur \_ \_Accès au code \_ refusé** (-1 (0xFFFFFFFF))


</dt> <dd>

L’accès a été refusé à l’utilisateur.

</dd> <dt>

<span id="LOGON_FAILED_BAD_PASSWORD"></span><span id="logon_failed_bad_password"></span>

<span id="LOGON_FAILED_BAD_PASSWORD"></span><span id="logon_failed_bad_password"></span>**Ouverture de session \_ \_ \_ Mot de passe incorrect en échec** (0 (0x0))


</dt> <dd>

L’ouverture de session a échoué car les informations d’identification d’ouverture de session ne sont pas valides.

</dd> <dt>

<span id="LOGON_FAILED_OTHER"></span><span id="logon_failed_other"></span>

<span id="LOGON_FAILED_OTHER"></span><span id="logon_failed_other"></span>**Ouverture de session \_ \_Autre échec** (2 (0X2))


</dt> <dd>

Une autre erreur d’ouverture de session ou de postconnexion s’est produite. Le client Bureau à distance affiche un écran d’ouverture de session pour l’utilisateur.

</dd> <dt>

<span id="LOGON_FAILED_UPDATE_PASSWORD"></span><span id="logon_failed_update_password"></span>

<span id="LOGON_FAILED_UPDATE_PASSWORD"></span><span id="logon_failed_update_password"></span>**Ouverture de session \_ ÉCHEC \_ de la mise à jour du \_ mot de passe** (1 (0x1))


</dt> <dd>

Le mot de passe a expiré. L’utilisateur doit mettre à jour son mot de passe pour continuer à se connecter.

</dd> <dt>

<span id="LOGON_WARNING"></span><span id="logon_warning"></span>

<span id="LOGON_WARNING"></span><span id="logon_warning"></span>**Ouverture de session \_ AVERTISSEMENT** (3 (0x3))


</dt> <dd>

Le client Bureau à distance affiche une boîte de dialogue qui contient des informations importantes pour l’utilisateur.

</dd> <dt>

<span id="STATUS_ACCOUNT_RESTRICTION"></span><span id="status_account_restriction"></span>

<span id="STATUS_ACCOUNT_RESTRICTION"></span><span id="status_account_restriction"></span>**État \_ \_Restriction de compte** (-1073741714 (0xC000006E))


</dt> <dd>

Le nom d’utilisateur et les informations d’authentification sont valides, mais l’authentification a été bloquée en raison de restrictions sur le compte d’utilisateur, telles que les restrictions de l’heure de la journée.

</dd> <dt>

<span id="STATUS_LOGON_FAILURE"></span><span id="status_logon_failure"></span>

<span id="STATUS_LOGON_FAILURE"></span><span id="status_logon_failure"></span>**État \_ \_Échec d’ouverture de session** (-1073741715 (0xC000006D))


</dt> <dd>

La tentative d’ouverture de session n’est pas valide. Cela est dû à un nom d’utilisateur incorrect ou à des informations d’authentification incorrectes.

</dd> <dt>

<span id="STATUS_PASSWORD_MUST_CHANGE"></span><span id="status_password_must_change"></span>

<span id="STATUS_PASSWORD_MUST_CHANGE"></span><span id="status_password_must_change"></span>**État \_ Le mot de passe \_ doit être \_ modifié** (-1073741276 (0xC0000224))


</dt> <dd>

Le mot de passe a expiré. L’utilisateur doit mettre à jour son mot de passe pour continuer à se connecter.

</dd> </dl> </dd> </dl>

## <a name="return-value"></a>Valeur retournée

Cette méthode ne retourne pas de valeur.

## <a name="remarks"></a>Remarques

Implémentez cette méthode dans votre récepteur d’événements pour recevoir une notification indiquant qu’une erreur d’ouverture de session s’est produite.

Cette liste de codes n’est pas exhaustive.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows Vista<br/>                                                               |
| Serveur minimal pris en charge<br/> | Windows Server 2008<br/>                                                         |
| Bibliothèque de types<br/>             | <dl> <dt>MsTscAx.dll</dt> </dl> |
| DLL<br/>                      | <dl> <dt>MsTscAx.dll</dt> </dl> |
| IID<br/>                      | IMsTscAxEvents est défini en tant que 336d5562-efa8-482e-8cb3-c5c0fc7a7db6<br/>           |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**IMsTscAxEvents**](imstscaxevents-interface.md)
</dt> </dl>

 

 





