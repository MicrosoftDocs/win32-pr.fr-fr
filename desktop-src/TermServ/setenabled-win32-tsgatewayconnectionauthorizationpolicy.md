---
title: Méthode SetEnabled de la classe Win32_TSGatewayConnectionAuthorizationPolicy
description: Définit la propriété Enabled, qui active ou désactive la stratégie d’autorisation de connexion Services Bureau à distance actuelle (RD \ 160 ; CAP).
ms.assetid: f8c0b39e-95d4-46cf-83fb-e91b650fbb4d
ms.tgt_platform: multiple
keywords:
- Services Bureau à distance de la méthode SetEnabled
- Services Bureau à distance de la méthode SetEnabled, classe Win32_TSGatewayConnectionAuthorizationPolicy
- Win32_TSGatewayConnectionAuthorizationPolicy de la classe Services Bureau à distance, méthode SetEnabled
topic_type:
- apiref
api_name:
- Win32_TSGatewayConnectionAuthorizationPolicy.SetEnabled
api_location:
- AagWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: eb25fff49962d019a01605c8392c3a09f1029152f6aed0ec8809302a81895408
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119000469"
---
# <a name="setenabled-method-of-the-win32_tsgatewayconnectionauthorizationpolicy-class"></a>Méthode SetEnabled de la \_ classe Win32 TSGatewayConnectionAuthorizationPolicy

Définit la propriété **Enabled** , qui active ou désactive la stratégie d’autorisation des connexions services Bureau à distance en cours.

## <a name="syntax"></a>Syntaxe


```mof
uint32 SetEnabled(
  [in] boolean Enabled
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*Activé* \[ dans\]
</dt> <dd>

**True** **si la** stratégie d’autorisation des connexions aux services Bureau à distance doit être activée.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Si la méthode est réussie, elle retourne zéro. Si la méthode échoue, elle retourne une valeur différente de zéro. Pour obtenir la liste des codes d’erreur, consultez [services Bureau à distance codes d’erreur du fournisseur WMI](terminal-services-wmi-provider-error-codes.md).

## <a name="remarks"></a>Remarques

Vous devez être membre du groupe administrateurs pour appeler cette méthode.

les fichiers format MOF (MOF) contiennent les définitions des classes Windows Management Instrumentation (WMI). les fichiers MOF ne sont pas installés dans le cadre du kit de développement logiciel (SDK) Microsoft Windows. Ils sont installés sur le serveur lorsque vous ajoutez le rôle associé à l’aide de l’Gestionnaire de serveur. Pour plus d’informations sur les fichiers MOF, consultez [format MOF (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Aucun pris en charge<br/>                                                                |
| Serveur minimal pris en charge<br/> | Windows Server 2008<br/>                                                           |
| Espace de noms<br/>                | Racine \\ cimv2 \\ licences TS<br/>                                                 |
| MOF<br/>                      | <dl> <dt>TSGateway. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>AagWmi.dll</dt> </dl>    |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**\_TSGatewayConnectionAuthorizationPolicy Win32**](win32-tsgatewayconnectionauthorizationpolicy.md)
</dt> </dl>

 

