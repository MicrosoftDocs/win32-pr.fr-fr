---
title: Méthode TSGStoreAdminMsg de la classe Win32_TSGatewayServerSettings
description: Met à jour le message d’administration pour le serveur de passerelle.
ms.assetid: 84e5b967-12fd-47a7-93e4-2550c15c4491
ms.tgt_platform: multiple
keywords:
- Services Bureau à distance de la méthode TSGStoreAdminMsg
- Services Bureau à distance de la méthode TSGStoreAdminMsg, classe Win32_TSGatewayServerSettings
- Win32_TSGatewayServerSettings de la classe Services Bureau à distance, méthode TSGStoreAdminMsg
topic_type:
- apiref
api_name:
- Win32_TSGatewayServerSettings.TSGStoreAdminMsg
api_location:
- AagWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 398a027d28970b28b4a1e7db37b5fbfee06e881e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103843693"
---
# <a name="tsgstoreadminmsg-method-of-the-win32_tsgatewayserversettings-class"></a>Méthode TSGStoreAdminMsg de la \_ classe Win32 TSGatewayServerSettings

Met à jour le message d’administration pour le serveur de passerelle.

## <a name="syntax"></a>Syntaxe


```mof
uint32 TSGStoreAdminMsg(
  [in] string TSGAdmMsg,
  [in] string MsgStartTime,
  [in] string MsgEndTime
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*TSGAdmMsg* \[ dans\]
</dt> <dd>

Type : **chaîne**

Texte du message administratif.

</dd> <dt>

*MsgStartTime* \[ dans\]
</dt> <dd>

Type : **chaîne**

Heure de début du message d’administration.

</dd> <dt>

*MsgEndTime* \[ dans\]
</dt> <dd>

Type : **chaîne**

Heure de fin du message d’administration.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Type : **UInt32**

Si la méthode est réussie, elle retourne zéro. Si la méthode échoue, elle retourne une valeur différente de zéro. Pour obtenir la liste des codes d’erreur, consultez [services Bureau à distance codes d’erreur du fournisseur WMI](terminal-services-wmi-provider-error-codes.md).

## <a name="remarks"></a>Notes

Vous devez être membre du groupe administrateurs pour appeler cette méthode.

Les fichiers format MOF (MOF) contiennent les définitions des classes Windows Management Instrumentation (WMI). Les fichiers MOF ne sont pas installés dans le cadre du kit de développement logiciel (SDK) Microsoft Windows. Ils sont installés sur le serveur lorsque vous ajoutez le rôle associé à l’aide de l’Gestionnaire de serveur. Pour plus d’informations sur les fichiers MOF, consultez [format MOF (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Aucun pris en charge<br/>                                                                |
| Serveur minimal pris en charge<br/> | Windows Server 2008 R2<br/>                                                        |
| Espace de noms<br/>                | Racine \\ cimv2 \\ licences TS<br/>                                                 |
| MOF<br/>                      | <dl> <dt>TSGateway. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>AagWmi.dll</dt> </dl>    |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**\_TSGatewayServerSettings Win32**](win32-tsgatewayserversettings.md)
</dt> </dl>

 

