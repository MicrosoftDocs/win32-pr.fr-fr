---
title: Méthode GetTStoLSConnectivityStatus de la classe Win32_TerminalServiceSetting
description: Détermine l’état de la connectivité entre Services Bureau à distance et un serveur de licences.
ms.assetid: 11fc5865-47e8-4be8-a526-53e29f72d0a4
ms.tgt_platform: multiple
keywords:
- Services Bureau à distance de la méthode GetTStoLSConnectivityStatus
- Services Bureau à distance de la méthode GetTStoLSConnectivityStatus, classe Win32_TerminalServiceSetting
- Win32_TerminalServiceSetting de la classe Services Bureau à distance, méthode GetTStoLSConnectivityStatus
topic_type:
- apiref
api_name:
- Win32_TerminalServiceSetting.GetTStoLSConnectivityStatus
api_location:
- TSCfgWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0fb73cd62c5ab5c343f44f24bbbd8de7f6343a21
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104465795"
---
# <a name="gettstolsconnectivitystatus-method-of-the-win32_terminalservicesetting-class"></a>Méthode GetTStoLSConnectivityStatus de la \_ classe Win32 TerminalServiceSetting

Détermine l’état de la connectivité entre Services Bureau à distance et un serveur de licences.

## <a name="syntax"></a>Syntaxe


```mof
uint32 GetTStoLSConnectivityStatus(
  [in]  string ServerName,
  [out] uint32 TStoLSConnectivityStatus
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*Nom du serveur* \[ dans\]
</dt> <dd>

Nom du serveur de licences dont l’état de connectivité doit être vérifié.

</dd> <dt>

*TStoLSConnectivityStatus* \[ à\]
</dt> <dd>

Valeur qui indique l’état de connectivité du serveur de licences. Il peut s’agir de l’une des valeurs suivantes.

<dt>

<span id="LS_CONNECTABLE_UNKNOWN"></span><span id="ls_connectable_unknown"></span>

<span id="LS_CONNECTABLE_UNKNOWN"></span><span id="ls_connectable_unknown"></span>**Ls \_ CONNECTable \_ inconnu** (0)


</dt> <dd>

Impossible de déterminer l’état de la connectivité.

</dd> <dt>

<span id="LS_CONNECTABLE_VALID_WS08R2"></span><span id="ls_connectable_valid_ws08r2"></span>

<span id="LS_CONNECTABLE_VALID_WS08R2"></span><span id="ls_connectable_valid_ws08r2"></span>**Ls \_ \_ \_ WS08R2 valide connectable** (1)


</dt> <dd>

Services Bureau à distance pouvez vous connecter au serveur de licences Windows Server 2008 R2.

</dd> <dt>

<span id="LS_CONNECTABLE_VALID_WS08"></span><span id="ls_connectable_valid_ws08"></span>

<span id="LS_CONNECTABLE_VALID_WS08"></span><span id="ls_connectable_valid_ws08"></span>**Ls \_ \_ \_ WS08 valide connectable** (2)


</dt> <dd>

Services Bureau à distance pouvez vous connecter au serveur de licences Windows Server 2008.

</dd> <dt>

<span id="LS_CONNECTABLE_BETA_RTM_MISMATCH"></span><span id="ls_connectable_beta_rtm_mismatch"></span>

<span id="LS_CONNECTABLE_BETA_RTM_MISMATCH"></span><span id="ls_connectable_beta_rtm_mismatch"></span>**Ls \_ Incompatibilité \_ beta \_ RTM \_ connectable** (3)


</dt> <dd>

Services Bureau à distance peut se connecter au serveur de licences, mais l’un des serveurs exécute une version bêta du système d’exploitation.

</dd> <dt>

<span id="LS_CONNECTABLE_LOWER_VERSION"></span><span id="ls_connectable_lower_version"></span>

<span id="LS_CONNECTABLE_LOWER_VERSION"></span><span id="ls_connectable_lower_version"></span>**Ls \_ \_ \_ Version inférieure connectable** (4)


</dt> <dd>

Services Bureau à distance peut se connecter au serveur de licences, mais il existe une incompatibilité entre le serveur de licences et le serveur hôte Services Bureau à distance.

</dd> <dt>

<span id="LS_CONNECTABLE_NOT_IN_TSCGROUP"></span><span id="ls_connectable_not_in_tscgroup"></span>

<span id="LS_CONNECTABLE_NOT_IN_TSCGROUP"></span><span id="ls_connectable_not_in_tscgroup"></span>**Ls \_ CONNEXION \_ non \_ dans \_ TSCGROUP** (5)


</dt> <dd>

La stratégie de groupe de sécurité est activée dans le serveur de licences, mais Services Bureau à distance ne fait pas partie de la stratégie de groupe.

</dd> <dt>

<span id="LS_NOT_CONNECTABLE"></span><span id="ls_not_connectable"></span>

<span id="LS_NOT_CONNECTABLE"></span><span id="ls_not_connectable"></span>**Ls \_ NON \_ connectable** (6)


</dt> <dd>

Services Bureau à distance ne peut pas se connecter au serveur de licences.

</dd> <dt>

<span id="LS_CONNECTABLE_UNKNOWN_VALIDITY"></span><span id="ls_connectable_unknown_validity"></span>

<span id="LS_CONNECTABLE_UNKNOWN_VALIDITY"></span><span id="ls_connectable_unknown_validity"></span>**Ls \_ \_ \_ Validité inconnue connectable** (7)


</dt> <dd>

Le serveur de licences peut être connecté à, mais la validité de la connexion ne peut pas être déterminée.

</dd> <dt>

<span id="LS_CONNECTABLE_BUT_ACCESS_DENIED"></span><span id="ls_connectable_but_access_denied"></span>

<span id="LS_CONNECTABLE_BUT_ACCESS_DENIED"></span><span id="ls_connectable_but_access_denied"></span>**Ls \_ CONNECTable \_ mais \_ accès \_ refusé** (8)


</dt> <dd>

Services Bureau à distance peut se connecter au serveur de licences, mais le compte d’utilisateur ne dispose pas de privilèges d’administrateur sur le serveur de licences.

</dd> <dt>

<span id="LS_CONNECTABLE_VALID_WS08R2_VDI"></span><span id="ls_connectable_valid_ws08r2_vdi"></span>

<span id="LS_CONNECTABLE_VALID_WS08R2_VDI"></span><span id="ls_connectable_valid_ws08r2_vdi"></span>**Ls \_ \_ \_ WS08R2 \_ VDI valide connectable** (9)


</dt> <dd>

Services Bureau à distance pouvez vous connecter au serveur VDI (Virtual Desktop Infrastructure) de Windows Server 2008 R2.

**Windows Server 2008 R2 :** Cette valeur n’est pas prise en charge avant Windows Server 2012.

</dd> <dt>

<span id="LS_CONNECTABLE_FEATURE_NOT_SUPPORTED"></span><span id="ls_connectable_feature_not_supported"></span>

<span id="LS_CONNECTABLE_FEATURE_NOT_SUPPORTED"></span><span id="ls_connectable_feature_not_supported"></span>**Ls \_ \_Fonctionnalité connectable \_ non \_ prise en charge** (10)


</dt> <dd>

La fonctionnalité n’est pas prise en charge.

**Windows server 2008 R2 et Windows server 2008 R2 avec SP1 :** Cette valeur n’est pas prise en charge avant Windows Server 2012.

</dd> <dt>

<span id="LS_CONNECTABLE_VALID_LS"></span><span id="ls_connectable_valid_ls"></span>

<span id="LS_CONNECTABLE_VALID_LS"></span><span id="ls_connectable_valid_ls"></span>**Ls \_ CONNECTable \_ valide \_ ls** (11)


</dt> <dd>

Le serveur de licences est valide.

**Windows server 2008 R2 et Windows server 2008 R2 avec SP1 :** Cette valeur n’est pas prise en charge avant Windows Server 2012.

</dd> </dl> </dd> </dl>

## <a name="return-value"></a>Valeur retournée

Retourne 0 en cas de réussite, sinon retourne un code d’erreur WMI. Pour obtenir la liste de ces valeurs, reportez-vous à [services Bureau à distance codes d’erreur du fournisseur WMI](terminal-services-wmi-provider-error-codes.md) .

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Aucun pris en charge<br/>                                                               |
| Serveur minimal pris en charge<br/> | Windows Server 2008 R2<br/>                                                       |
| Espace de noms<br/>                | Racine \\ cimv2 \\ licences TS<br/>                                                |
| MOF<br/>                      | <dl> <dt>TSCfgWmi. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>TSCfgWmi.dll</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**\_TerminalServiceSetting Win32**](win32-terminalservicesetting.md)
</dt> </dl>

 

 





