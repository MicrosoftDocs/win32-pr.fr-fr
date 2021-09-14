---
title: Méthode BrokenConnection de la classe Win32_TSSessionSetting (Wtsprotocol. h)
description: Définit la propriété BrokenConnectionAction, qui est l’action prise par le serveur si la limite de durée de session est atteinte ou si la connexion est interrompue.
ms.assetid: 2422e314-9e1c-4bed-a958-eedd2daeca66
ms.tgt_platform: multiple
keywords:
- Services Bureau à distance de la méthode BrokenConnection
- Services Bureau à distance de la méthode BrokenConnection, classe Win32_TSSessionSetting
- Win32_TSSessionSetting de la classe Services Bureau à distance, méthode BrokenConnection
topic_type:
- apiref
api_name:
- Win32_TSSessionSetting.BrokenConnection
api_location:
- TSCfgWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a90b3f6bada75812b37df014cedadfb4e7ff2e83
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127008559"
---
# <a name="brokenconnection-method-of-the-win32_tssessionsetting-class"></a>Méthode BrokenConnection de la \_ classe Win32 TSSessionSetting

Définit la propriété **BrokenConnectionAction** , qui est l’action prise par le serveur si la limite de durée de session est atteinte ou si la connexion est interrompue.

## <a name="syntax"></a>Syntaxe


```mof
uint32 BrokenConnection(
  [in] uint32 BrokenConnectionAction
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*BrokenConnectionAction* \[ dans\]
</dt> <dd>

Action à entreprendre.

<dt>

<span id="Disconnect"></span><span id="disconnect"></span><span id="DISCONNECT"></span>

<span id="Disconnect"></span><span id="disconnect"></span><span id="DISCONNECT"></span>**Déconnecter** (0)


</dt> <dd>

L’utilisateur est déconnecté de la session.

</dd> <dt>

<span id="Terminate"></span><span id="terminate"></span><span id="TERMINATE"></span>

<span id="Terminate"></span><span id="terminate"></span><span id="TERMINATE"></span>**Terminate** (1)


</dt> <dd>

La session est définitivement supprimée du serveur.

</dd> </dl> </dd> </dl>

## <a name="return-value"></a>Valeur de retour

Retourne 0 en cas de réussite, sinon retourne un code d’erreur WMI. Pour obtenir la liste de ces valeurs, reportez-vous à [services Bureau à distance codes d’erreur du fournisseur WMI](terminal-services-wmi-provider-error-codes.md) . La méthode retourne une erreur si le paramètre est sous stratégie de groupe contrôle.

## <a name="remarks"></a>Notes

les fichiers format MOF (MOF) contiennent les définitions des classes Windows Management Instrumentation (WMI). les fichiers MOF ne sont pas installés dans le cadre du kit de développement logiciel (SDK) Microsoft Windows. Ils sont installés sur le serveur lorsque vous ajoutez le rôle associé à l’aide de l’Gestionnaire de serveur. Pour plus d’informations sur les fichiers MOF, consultez [format MOF (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows Vista<br/>                                                                 |
| Serveur minimal pris en charge<br/> | Windows Server 2008<br/>                                                           |
| Espace de noms<br/>                | Racine \\ cimv2 \\ licences TS<br/>                                                 |
| En-tête<br/>                   | <dl> <dt>Wtsprotocol. h</dt> </dl> |
| MOF<br/>                      | <dl> <dt>TSCfgWmi. mof</dt> </dl>  |
| DLL<br/>                      | <dl> <dt>TSCfgWmi.dll</dt> </dl>  |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**\_TSSessionSetting Win32**](win32-tssessionsetting.md)
</dt> </dl>

 

