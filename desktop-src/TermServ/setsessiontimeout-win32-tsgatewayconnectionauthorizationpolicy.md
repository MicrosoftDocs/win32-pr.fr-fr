---
title: Méthode SetSessionTimeout de la classe Win32_TSGatewayConnectionAuthorizationPolicy
description: Définit les propriétés SessionTimeout et SessionTimeoutAction.
ms.assetid: 11491c97-3ef8-46c1-9504-696c613e374e
ms.tgt_platform: multiple
keywords:
- Services Bureau à distance de la méthode SetSessionTimeout
- Services Bureau à distance de la méthode SetSessionTimeout, classe Win32_TSGatewayConnectionAuthorizationPolicy
- Win32_TSGatewayConnectionAuthorizationPolicy de la classe Services Bureau à distance, méthode SetSessionTimeout
topic_type:
- apiref
api_name:
- Win32_TSGatewayConnectionAuthorizationPolicy.SetSessionTimeout
api_location:
- AagWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c786372628fa272f9d3f2a3486034a6339b94e3b658b184b74a5a31fc11f492e
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119865099"
---
# <a name="setsessiontimeout-method-of-the-win32_tsgatewayconnectionauthorizationpolicy-class"></a>Méthode SetSessionTimeout de la \_ classe Win32 TSGatewayConnectionAuthorizationPolicy

Définit les propriétés **SessionTimeout** et **SessionTimeoutAction** .

## <a name="syntax"></a>Syntaxe


```mof
uint32 SetSessionTimeout(
  [in] uint32 SessionTimeout,
  [in] uint32 SessionTimeoutAction
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*SessionTimeout* \[ dans\]
</dt> <dd>

Type : **UInt32**

Nouvelle valeur du délai d’attente, en minutes. La valeur 0 signifie qu’il n’y a aucun délai d’attente.

</dd> <dt>

*SessionTimeoutAction* \[ dans\]
</dt> <dd>

Type : **UInt32**

Spécifie l’action à entreprendre en cas de délai d’expiration de session. Il peut s’agir de l’une des valeurs suivantes.

<dt>

0
</dt> <dd>

Déconnectez la session.

</dd> <dt>

1
</dt> <dd>

Essayez de réautoriser la session.

</dd> </dl> </dd> </dl>

## <a name="return-value"></a>Valeur retournée

Type : **UInt32**

Si la méthode est réussie, elle retourne zéro. Si la méthode échoue, elle retourne une valeur différente de zéro. Pour obtenir la liste des codes d’erreur, consultez [services Bureau à distance codes d’erreur du fournisseur WMI](terminal-services-wmi-provider-error-codes.md).

## <a name="remarks"></a>Remarques

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

[**\_TSGatewayConnectionAuthorizationPolicy Win32**](win32-tsgatewayconnectionauthorizationpolicy.md)
</dt> </dl>

 

