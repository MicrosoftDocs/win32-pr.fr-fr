---
title: Méthode SetTimeZoneRedirection de la classe Win32_TerminalServiceSetting
description: La méthode SetTimeZoneRedirection définit la propriété TimeZoneRedirection, qui permet à l’ordinateur client de rediriger ses paramètres de fuseau horaire vers la session Services Bureau à distance.
ms.assetid: 4ae149b7-b7de-4530-a142-7253dd1e0d07
ms.tgt_platform: multiple
keywords:
- Services Bureau à distance de la méthode SetTimeZoneRedirection
- Services Bureau à distance de la méthode SetTimeZoneRedirection, classe Win32_TerminalServiceSetting
- Win32_TerminalServiceSetting de la classe Services Bureau à distance, méthode SetTimeZoneRedirection
topic_type:
- apiref
api_name:
- Win32_TerminalServiceSetting.SetTimeZoneRedirection
api_location:
- TSCfgWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2761567c724abf129ac881188bc468b228d7fd11
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "126919592"
---
# <a name="settimezoneredirection-method-of-the-win32_terminalservicesetting-class"></a>Méthode SetTimeZoneRedirection de la \_ classe Win32 TerminalServiceSetting

La méthode **SetTimeZoneRedirection** définit la propriété **TimeZoneRedirection** , qui permet à l’ordinateur client de rediriger ses paramètres de fuseau horaire vers la session services Bureau à distance.

## <a name="syntax"></a>Syntaxe


```mof
uint32 SetTimeZoneRedirection(
  [in] uint32 TimeZoneRedirection
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*TimeZoneRedirection* \[ dans\]
</dt> <dd>

Nouvelle valeur de la propriété **TimeZoneRedirection** .

<dt>

<span id="0"></span>

<span id="0"></span>**entre**


</dt> <dd>

Désactive la propriété **TimeZoneRedirection** . Aucune redirection de fuseau horaire n’a lieu.

</dd> <dt>

<span id="1"></span>

<span id="1"></span>**1**


</dt> <dd>

Active la propriété **TimeZoneRedirection** . Le fuseau horaire du client est redirigé vers le fuseau horaire de la session.

</dd> </dl> </dd> </dl>

## <a name="return-value"></a>Valeur de retour

Retourne 0 en cas de réussite ; Sinon, retourne un code d’erreur WMI. Pour obtenir la liste de ces valeurs, reportez-vous à [services Bureau à distance codes d’erreur du fournisseur WMI](terminal-services-wmi-provider-error-codes.md) .

## <a name="remarks"></a>Notes

Par défaut, le fuseau horaire de la session de Services Bureau à distance est le même que celui du serveur hôte de session Bureau à distance (hôte de session Bureau à distance). Les ordinateurs clients ne peuvent pas rediriger les informations de fuseau horaire.

Si la redirection de fuseau horaire est désactivée, les nouvelles sessions héritent du fuseau horaire du serveur. Lorsqu’une session se reconnecte, la session conserve le fuseau horaire qu’elle avait avant la déconnexion.

les fichiers format MOF (MOF) contiennent les définitions des classes Windows Management Instrumentation (WMI). les fichiers MOF ne sont pas installés dans le cadre du kit de développement logiciel (SDK) Microsoft Windows. Ils sont installés sur le serveur lorsque vous ajoutez le rôle associé à l’aide de l’Gestionnaire de serveur. Pour plus d’informations sur les fichiers MOF, consultez [format MOF (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows Vista<br/>                                                                |
| Serveur minimal pris en charge<br/> | Windows Server 2008<br/>                                                          |
| Espace de noms<br/>                | Racine \\ cimv2 \\ licences TS<br/>                                                |
| MOF<br/>                      | <dl> <dt>TSCfgWmi. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>TSCfgWmi.dll</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**\_TerminalServiceSetting Win32**](win32-terminalservicesetting.md)
</dt> </dl>

 

