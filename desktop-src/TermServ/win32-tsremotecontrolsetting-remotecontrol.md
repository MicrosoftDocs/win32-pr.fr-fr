---
title: Méthode RemoteControl de la classe Win32_TSRemoteControlSetting
description: La méthode RemoteControl définit la propriété LevelOfControl.
ms.assetid: 341f4f8d-17be-4482-834a-b771e041cfec
ms.tgt_platform: multiple
keywords:
- Services Bureau à distance de la méthode RemoteControl
- Services Bureau à distance de la méthode RemoteControl, classe Win32_TSRemoteControlSetting
- Win32_TSRemoteControlSetting de la classe Services Bureau à distance, méthode RemoteControl
topic_type:
- apiref
api_name:
- Win32_TSRemoteControlSetting.RemoteControl
api_location:
- TSCfgWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 73de3f92171f688a9c0dc611552a061a3f2de7bf573fa41dab8606395eafe228
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119769419"
---
# <a name="remotecontrol-method-of-the-win32_tsremotecontrolsetting-class"></a>Méthode RemoteControl de la \_ classe Win32 TSRemoteControlSetting

La méthode **RemoteControl** définit la propriété **LevelOfControl** .

## <a name="syntax"></a>Syntaxe


```mof
uint32 RemoteControl(
  [in] uint32 LevelOfControl
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*LevelOfControl* \[ dans\]
</dt> <dd>

Nouvelle valeur de la propriété **LevelOfControl** , qui spécifie si la session est uniquement affichée par l’utilisateur distant ou affichée et contrôlée par le biais d’un clavier et d’une souris. Pour plus d'informations, consultez la section Notes. Les valeurs suivantes sont admises :

<dt>

<span id="Disable"></span><span id="disable"></span><span id="DISABLE"></span>

<span id="Disable"></span><span id="disable"></span><span id="DISABLE"></span>**Désactiver** (0)


</dt> <dd>

Le contrôle à distance est désactivé.

</dd> <dt>

<span id="EnableInputNotify"></span><span id="enableinputnotify"></span><span id="ENABLEINPUTNOTIFY"></span>

<span id="EnableInputNotify"></span><span id="enableinputnotify"></span><span id="ENABLEINPUTNOTIFY"></span>**EnableInputNotify** (1)


</dt> <dd>

L’utilisateur du contrôle à distance a le contrôle total de la session de l’utilisateur, avec l’autorisation de l’utilisateur.

</dd> <dt>

<span id="EnableInputNoNotify"></span><span id="enableinputnonotify"></span><span id="ENABLEINPUTNONOTIFY"></span>

<span id="EnableInputNoNotify"></span><span id="enableinputnonotify"></span><span id="ENABLEINPUTNONOTIFY"></span>**EnableInputNoNotify** (2)


</dt> <dd>

L’utilisateur du contrôle à distance a le contrôle total de la session de l’utilisateur ; l’autorisation de l’utilisateur n’est pas obligatoire.

</dd> <dt>

<span id="EnableNoInputNotify"></span><span id="enablenoinputnotify"></span><span id="ENABLENOINPUTNOTIFY"></span>

<span id="EnableNoInputNotify"></span><span id="enablenoinputnotify"></span><span id="ENABLENOINPUTNOTIFY"></span>**EnableNoInputNotify** (3)


</dt> <dd>

L’utilisateur du contrôle à distance peut afficher la session à distance, avec l’autorisation de l’utilisateur. l’utilisateur distant ne peut pas contrôler activement la session.

</dd> <dt>

<span id="EnableNoInputNoNotify"></span><span id="enablenoinputnonotify"></span><span id="ENABLENOINPUTNONOTIFY"></span>

<span id="EnableNoInputNoNotify"></span><span id="enablenoinputnonotify"></span><span id="ENABLENOINPUTNONOTIFY"></span>**EnableNoInputNoNotify** (4)


</dt> <dd>

L’utilisateur du contrôle à distance peut afficher la session à distance, mais ne contrôle pas activement la session ; l’autorisation de l’utilisateur n’est pas obligatoire.

</dd> </dl> </dd> </dl>

## <a name="return-value"></a>Valeur retournée

Retourne 0 en cas de réussite, sinon retourne un code d’erreur WMI. Pour obtenir la liste de ces valeurs, reportez-vous à [services Bureau à distance codes d’erreur du fournisseur WMI](terminal-services-wmi-provider-error-codes.md) . La méthode retourne une erreur si le paramètre est sous contrôle de stratégie de groupe.

## <a name="remarks"></a>Remarques

Le contrôle total d’une session signifie que l’utilisateur distant peut contrôler activement la session de l’utilisateur à l’aide d’un clavier et d’une souris.

Lorsqu’un utilisateur tente d’établir une connexion de contrôle à distance, le système affiche un message au client distant, en demandant l’autorisation d’afficher ou de participer activement à la session à distance.

les fichiers format MOF (MOF) contiennent les définitions des classes Windows Management Instrumentation (WMI). les fichiers MOF ne sont pas installés dans le cadre du kit de développement logiciel (SDK) Microsoft Windows. Ils sont installés sur le serveur lorsque vous ajoutez le rôle associé à l’aide de l’Gestionnaire de serveur. Pour plus d’informations sur les fichiers MOF, consultez [format MOF (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).

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

[**\_TSRemoteControlSetting Win32**](win32-tsremotecontrolsetting.md)
</dt> </dl>

 

