---
title: Méthode SetDefaultPluginsAndRecycleRpcApplicationPools de la classe Win32_TSGatewayServerSettings
description: Définit les plug-ins d’authentification et d’autorisation actuels pour le serveur de passerelle Bureau à distance (passerelle des services Bureau à distance) et recycle les pools d’applications RPC dans IIS.
ms.assetid: 1eac9e42-e533-4020-b2b6-571063f18c3c
ms.tgt_platform: multiple
keywords:
- Services Bureau à distance de la méthode SetDefaultPluginsAndRecycleRpcApplicationPools
- Services Bureau à distance de la méthode SetDefaultPluginsAndRecycleRpcApplicationPools, classe Win32_TSGatewayServerSettings
- Win32_TSGatewayServerSettings de la classe Services Bureau à distance, méthode SetDefaultPluginsAndRecycleRpcApplicationPools
topic_type:
- apiref
api_name:
- Win32_TSGatewayServerSettings.SetDefaultPluginsAndRecycleRpcApplicationPools
api_location:
- AagWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3b9ead29e987b68ec3f041010be5dde64d8a2b54
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127324438"
---
# <a name="setdefaultpluginsandrecyclerpcapplicationpools-method-of-the-win32_tsgatewayserversettings-class"></a>Méthode SetDefaultPluginsAndRecycleRpcApplicationPools de la \_ classe Win32 TSGatewayServerSettings

Définit les plug-ins d’authentification et d’autorisation actuels pour le serveur de passerelle Bureau à distance (passerelle des services Bureau à distance) et recycle les pools d’applications RPC dans IIS.

## <a name="syntax"></a>Syntaxe


```mof
uint32 SetDefaultPluginsAndRecycleRpcApplicationPools();
```



## <a name="parameters"></a>Paramètres

Cette méthode n’a aucun paramètre.

## <a name="return-value"></a>Valeur de retour

Type : **UInt32**

Si la méthode est réussie, elle retourne zéro. Si la méthode échoue, elle retourne une valeur différente de zéro. Pour obtenir la liste des codes d’erreur, consultez [services Bureau à distance codes d’erreur du fournisseur WMI](terminal-services-wmi-provider-error-codes.md).

## <a name="remarks"></a>Notes

L’appel de cette méthode entraîne la déconnexion de toutes les connexions existantes.

Vous devez être membre du groupe administrateurs pour appeler cette méthode.

les fichiers format MOF (MOF) contiennent les définitions des classes Windows Management Instrumentation (WMI). les fichiers MOF ne sont pas installés dans le cadre du kit de développement logiciel (SDK) Microsoft Windows. Ils sont installés sur le serveur lorsque vous ajoutez le rôle associé à l’aide de l’Gestionnaire de serveur. Pour plus d’informations sur les fichiers MOF, consultez [format MOF (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).

## <a name="requirements"></a>Spécifications



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

 

