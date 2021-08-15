---
title: Méthode SetAuthenticationPlugin de la classe Win32_TSGatewayServerSettings
description: Définit le plug-in d’authentification actuel pour le serveur de passerelle Bureau à distance (passerelle des services Bureau à distance).
ms.assetid: b79a5e7c-bf55-48f6-a6c0-5338e7eee2a1
ms.tgt_platform: multiple
keywords:
- Services Bureau à distance de la méthode SetAuthenticationPlugin
- Services Bureau à distance de la méthode SetAuthenticationPlugin, classe Win32_TSGatewayServerSettings
- Win32_TSGatewayServerSettings de la classe Services Bureau à distance, méthode SetAuthenticationPlugin
topic_type:
- apiref
api_name:
- Win32_TSGatewayServerSettings.SetAuthenticationPlugin
api_location:
- AagWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1be1da91b281e8a47c2663fe09f6b7f172dca8d4d246f0fe708139fe859955a7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119058547"
---
# <a name="setauthenticationplugin-method-of-the-win32_tsgatewayserversettings-class"></a>Méthode SetAuthenticationPlugin de la \_ classe Win32 TSGatewayServerSettings

Définit le plug-in d’authentification actuel pour le serveur de passerelle Bureau à distance (passerelle des services Bureau à distance).

## <a name="syntax"></a>Syntaxe


```mof
uint32 SetAuthenticationPlugin(
  [in] string PluginName
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*PluginName* \[ dans\]
</dt> <dd>

Type : **chaîne**

Nom du nouveau plug-in d’authentification actuel.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Type : **UInt32**

Si la méthode est réussie, elle retourne zéro. Si la méthode échoue, elle retourne une valeur différente de zéro. Pour obtenir la liste des codes d’erreur, consultez [services Bureau à distance codes d’erreur du fournisseur WMI](terminal-services-wmi-provider-error-codes.md).

## <a name="remarks"></a>Remarques

Vous devez appeler la méthode [**RecycleRpcApplicationPools**](recyclerpcapplicationpools-win32-tsgatewayserversettings.md) pour autoriser le plug-in d’authentification à fonctionner.

Vous devez être membre du groupe administrateurs pour appeler cette méthode.

les fichiers format MOF (MOF) contiennent les définitions des classes Windows Management Instrumentation (WMI). les fichiers MOF ne sont pas installés dans le cadre du kit de développement logiciel (SDK) Microsoft Windows. Ils sont installés sur le serveur lorsque vous ajoutez le rôle associé à l’aide de l’Gestionnaire de serveur. Pour plus d’informations sur les fichiers MOF, consultez [format MOF (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).

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
</dt> <dt>

[**RecycleRpcApplicationPools**](recyclerpcapplicationpools-win32-tsgatewayserversettings.md)
</dt> </dl>

 

