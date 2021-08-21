---
title: Méthode AddAccount de la classe Win32_TSPermissionsSetting (Faxcomex. h)
description: La méthode AddAccount prépare l’ajout d’un compte au terminal avec le jeu d’autorisations spécifié. Vous pouvez ajouter des utilisateurs, des groupes ou des ordinateurs.
ms.assetid: da4d8f5b-7aa2-4b55-bf0f-b3e98b70a06b
ms.tgt_platform: multiple
keywords:
- Services Bureau à distance de la méthode AddAccount
- Services Bureau à distance de la méthode AddAccount, classe Win32_TSPermissionsSetting
- Win32_TSPermissionsSetting de la classe Services Bureau à distance, méthode AddAccount
topic_type:
- apiref
api_name:
- Win32_TSPermissionsSetting.AddAccount
api_location:
- TSCfgWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c3bd1862dfde955d782527ca60fc0fb43ca31431ccb307574e875fe84a640655
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118348554"
---
# <a name="addaccount-method-of-the-win32_tspermissionssetting-class"></a>Méthode AddAccount de la \_ classe Win32 TSPermissionsSetting

La méthode **AddAccount** prépare l’ajout d’un compte au terminal avec le jeu d’autorisations spécifié. Vous pouvez ajouter des utilisateurs, des groupes ou des ordinateurs.

## <a name="syntax"></a>Syntaxe


```mof
uint32 AddAccount(
  [in] string AccountName,
  [in] uint32 PermissionPreSet
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*AccountName* \[ dans\]
</dt> <dd>

Nom du compte à ajouter au terminal.

</dd> <dt>

*PermissionPreSet* \[ dans\]
</dt> <dd>

Jeu d’autorisations à associer au compte spécifié. Ce paramètre peut avoir une ou plusieurs des valeurs suivantes. Pour plus d’informations, consultez [services Bureau à distance autorisations](terminal-services-permissions.md).

<dt>

<span id="WINSTATION_GUEST_ACCESS"></span><span id="winstation_guest_access"></span>

<span id="WINSTATION_GUEST_ACCESS"></span><span id="winstation_guest_access"></span>**Station \_ de \_Accès invité** (0)


</dt> <dd>

Le compte dispose d’une autorisation d’ouverture de session.

</dd> <dt>

<span id="WINSTATION_USER_ACCESS"></span><span id="winstation_user_access"></span>

<span id="WINSTATION_USER_ACCESS"></span><span id="winstation_user_access"></span>**Station \_ de \_Accès utilisateur** (1)


</dt> <dd>

Le compte dispose des autorisations suivantes : ouverture de session, informations sur les requêtes, envoi de messages et Connecter.

</dd> <dt>

<span id="WINSTATION_ALL_ACCESS"></span><span id="winstation_all_access"></span>

<span id="WINSTATION_ALL_ACCESS"></span><span id="winstation_all_access"></span>**Station \_ de TOUT \_ accès** (2)


</dt> <dd>

Le compte dispose de toutes les autorisations de Services Bureau à distance.

</dd> </dl> </dd> </dl>

## <a name="return-value"></a>Valeur retournée

Retourne 0 en cas de réussite, sinon retourne un code d’erreur WMI. Pour obtenir la liste de ces valeurs, reportez-vous à [services Bureau à distance codes d’erreur du fournisseur WMI](terminal-services-wmi-provider-error-codes.md) .

## <a name="remarks"></a>Remarques

les fichiers format MOF (MOF) contiennent les définitions des classes Windows Management Instrumentation (WMI). les fichiers MOF ne sont pas installés dans le cadre du kit de développement logiciel (SDK) Microsoft Windows. Ils sont installés sur le serveur lorsque vous ajoutez le rôle associé à l’aide de l’Gestionnaire de serveur. Pour plus d’informations sur les fichiers MOF, consultez [format MOF (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows Vista<br/>                                                                |
| Serveur minimal pris en charge<br/> | Windows Server 2008<br/>                                                          |
| Espace de noms<br/>                | Racine \\ cimv2 \\ licences TS<br/>                                                |
| En-tête<br/>                   | <dl> <dt>Faxcomex. h</dt> </dl>   |
| MOF<br/>                      | <dl> <dt>TSCfgWmi. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>TSCfgWmi.dll</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**\_TSPermissionsSetting Win32**](win32-tspermissionssetting.md)
</dt> </dl>

 

