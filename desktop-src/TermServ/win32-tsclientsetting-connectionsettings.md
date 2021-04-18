---
title: Méthode ConnectionSettings de la classe Win32_TSClientSetting
description: La méthode ConnectionSettings définit les paramètres de session qui s’appliquent au processus de connexion et d’ouverture de session.
ms.assetid: 603807fe-f341-4358-a3b0-0300785cbdb1
ms.tgt_platform: multiple
keywords:
- Services Bureau à distance de la méthode ConnectionSettings
- Services Bureau à distance de la méthode ConnectionSettings, classe Win32_TSClientSetting
- Win32_TSClientSetting de la classe Services Bureau à distance, méthode ConnectionSettings
topic_type:
- apiref
api_name:
- Win32_TSClientSetting.ConnectionSettings
api_location:
- TSCfgWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ec255f00656684751b750e92d7a3df8290e3573e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104508506"
---
# <a name="connectionsettings-method-of-the-win32_tsclientsetting-class"></a>Méthode ConnectionSettings de la \_ classe Win32 TSClientSetting

La méthode **ConnectionSettings** définit les paramètres de session qui s’appliquent au processus de connexion et d’ouverture de session.

## <a name="syntax"></a>Syntaxe


```mof
uint32 ConnectionSettings(
  [in] uint32 ConnectClientDrivesAtLogon,
  [in] uint32 ConnectPrinterAtLogon,
  [in] uint32 DefaultToClientPrinter
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*ConnectClientDrivesAtLogon* \[ dans\]
</dt> <dd>

Indicateur d’activation ou de désactivation de la propriété **ConnectClientDrivesAtLogon** qui spécifie si les lecteurs du client sont connectés automatiquement au cours de la procédure d’ouverture de session.

<dt>

<span id="0"></span>

<span id="0"></span>**entre**


</dt> <dd>

Les lecteurs du client ne sont pas automatiquement connectés.

</dd> <dt>

<span id="1"></span>

<span id="1"></span>**1**


</dt> <dd>

Les lecteurs du client sont automatiquement connectés.

</dd> </dl> </dd> <dt>

*ConnectPrinterAtLogon* \[ dans\]
</dt> <dd>

Indicateur d’activation ou de désactivation de la propriété **ConnectPrinterAtLogon** , qui spécifie si toutes les imprimantes clientes locales mappées sont automatiquement connectées lors de la procédure d’ouverture de session.

<dt>

<span id="0"></span>

<span id="0"></span>**entre**


</dt> <dd>

Toutes les imprimantes locales mappées ne sont pas automatiquement connectées.

</dd> <dt>

<span id="1"></span>

<span id="1"></span>**1**


</dt> <dd>

Toutes les imprimantes locales mappées sont automatiquement connectées.

</dd> </dl> </dd> <dt>

*DefaultToClientPrinter* \[ dans\]
</dt> <dd>

Indicateur d’activation ou de désactivation de la propriété **DefaultToClientPrinter** qui spécifie si les travaux d’impression sont envoyés automatiquement à l’imprimante locale du client.

<dt>

<span id="0"></span>

<span id="0"></span>**entre**


</dt> <dd>

Les travaux d’impression ne sont pas envoyés automatiquement.

</dd> <dt>

<span id="1"></span>

<span id="1"></span>**1**


</dt> <dd>

Les travaux d’impression sont envoyés automatiquement.

</dd> </dl> </dd> </dl>

## <a name="return-value"></a>Valeur retournée

Retourne 0 en cas de réussite, sinon retourne un code d’erreur WMI. Pour obtenir la liste de ces valeurs, reportez-vous à [services Bureau à distance codes d’erreur du fournisseur WMI](terminal-services-wmi-provider-error-codes.md) . La méthode retourne une erreur si les paramètres de connexion de l’utilisateur sont remplacés par le serveur.

## <a name="remarks"></a>Notes

Les fichiers format MOF (MOF) contiennent les définitions des classes Windows Management Instrumentation (WMI). Les fichiers MOF ne sont pas installés dans le cadre du kit de développement logiciel (SDK) Microsoft Windows. Ils sont installés sur le serveur lorsque vous ajoutez le rôle associé à l’aide de l’Gestionnaire de serveur. Pour plus d’informations sur les fichiers MOF, consultez [format MOF (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows Vista<br/>                                                                |
| Serveur minimal pris en charge<br/> | Windows Server 2008<br/>                                                          |
| Espace de noms<br/>                | Racine \\ cimv2 \\ licences TS<br/>                                                |
| MOF<br/>                      | <dl> <dt>TSCfgWmi. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>TSCfgWmi.dll</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**\_TSClientSetting Win32**](win32-tsclientsetting.md)
</dt> </dl>

 

