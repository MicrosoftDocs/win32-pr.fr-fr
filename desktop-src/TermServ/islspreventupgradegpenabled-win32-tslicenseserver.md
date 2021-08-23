---
title: Méthode IsLSPreventUpgradeGPEnabled de la classe Win32_TSLicenseServer
description: Récupère les valeur indiquant si \ 0034 ; empêcher la mise à niveau de licence \ 0034 ; le paramètre de stratégie de groupe est activé sur le serveur de licences Bureau à distance.
ms.assetid: f78585b8-a50c-402b-ab20-f405eba0c079
ms.tgt_platform: multiple
keywords:
- Services Bureau à distance de la méthode IsLSPreventUpgradeGPEnabled
- Services Bureau à distance de la méthode IsLSPreventUpgradeGPEnabled, classe Win32_TSLicenseServer
- Win32_TSLicenseServer de la classe Services Bureau à distance, méthode IsLSPreventUpgradeGPEnabled
topic_type:
- apiref
api_name:
- Win32_TSLicenseServer.IsLSPreventUpgradeGPEnabled
api_location:
- TlsWmiProv.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7958df7d153db0abafd8e463f22a181f2e5a639afa5c21cb7529a9cd5c005c5b
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119511693"
---
# <a name="islspreventupgradegpenabled-method-of-the-win32_tslicenseserver-class"></a>Méthode IsLSPreventUpgradeGPEnabled de la \_ classe Win32 TSLicenseServer

Récupère si le paramètre de stratégie de groupe « empêcher la mise à niveau de licence » est activé sur le serveur de licences Bureau à distance.

## <a name="syntax"></a>Syntaxe


```mof
uint32 IsLSPreventUpgradeGPEnabled(
  [out] boolean Enabled
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*Activé* \[ à\]
</dt> <dd>

Valeur booléenne qui indique si le paramètre de stratégie « empêcher la mise à niveau de licence » est activé.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Si la méthode est réussie, elle retourne zéro. Si la méthode échoue, elle retourne une valeur différente de zéro. Pour obtenir la liste des codes d’erreur, consultez [services Bureau à distance codes d’erreur du fournisseur WMI](terminal-services-wmi-provider-error-codes.md).

## <a name="remarks"></a>Remarques

Vous devez être membre du groupe administrateurs pour appeler cette méthode.

Si le paramètre de stratégie « empêcher la mise à niveau de licence » est activé, le serveur de licences émet une licence d’accès client aux services Bureau à distance temporaire au client uniquement si une licence d’accès client aux services Bureau à distance appropriée pour le serveur hôte de session Bureau à distance (hôte de session Bureau à distance) n’est pas disponible.

Le paramètre de stratégie se trouve dans le nœud suivant de l’éditeur d’une stratégie de groupe locale :

Configuration de l’ordinateur \\ Modèles d’administration \\ composants Windows \\ gestionnaire de licences TS Services terminal server \\

les fichiers format MOF (MOF) contiennent les définitions des classes Windows Management Instrumentation (WMI). les fichiers MOF ne sont pas installés dans le cadre du kit de développement logiciel (SDK) Microsoft Windows. Ils sont installés sur le serveur lorsque vous ajoutez le rôle associé à l’aide de l’Gestionnaire de serveur. Pour plus d’informations sur les fichiers MOF, consultez [format MOF (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Aucun pris en charge<br/>                                                                 |
| Serveur minimal pris en charge<br/> | Windows Server 2008<br/>                                                            |
| Espace de noms<br/>                | Racine\\CIMv2<br/>                                                                    |
| MOF<br/>                      | <dl> <dt>TlsWmiProv. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>TlsWmiProv.dll</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**\_TSLicenseServer Win32**](win32-tslicenseserver.md)
</dt> </dl>

 

