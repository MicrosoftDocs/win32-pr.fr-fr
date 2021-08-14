---
title: Méthode DisableClipboard de la classe Win32_TSGatewayConnectionAuthorizationPolicy
description: Définit la propriété ClipboardDisabled. Si la propriété DeviceRedirectionType a la valeur \ 0034 ; 2 \ 0034 ;, la propriété ClipboardDisabled contrôle la redirection du presse-papiers pour les sessions établies par le biais du serveur de passerelle Bureau à distance (passerelle Bureau à distance).
ms.assetid: c53fc802-958b-452d-9af9-0ce89ed46079
ms.tgt_platform: multiple
keywords:
- Services Bureau à distance de la méthode DisableClipboard
- Services Bureau à distance de la méthode DisableClipboard, classe Win32_TSGatewayConnectionAuthorizationPolicy
- Win32_TSGatewayConnectionAuthorizationPolicy de la classe Services Bureau à distance, méthode DisableClipboard
topic_type:
- apiref
api_name:
- Win32_TSGatewayConnectionAuthorizationPolicy.DisableClipboard
api_location:
- AagWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 01b5e8d2449bae2ee7f344c78b54850eb9ae300f4233c36b6eb2d84ad0b6132f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118609614"
---
# <a name="disableclipboard-method-of-the-win32_tsgatewayconnectionauthorizationpolicy-class"></a>Méthode DisableClipboard de la \_ classe Win32 TSGatewayConnectionAuthorizationPolicy

Définit la propriété **ClipboardDisabled** . Si la propriété **DeviceRedirectionType** a la valeur « 2 », la propriété **ClipboardDisabled** contrôle la redirection du presse-papiers pour les sessions établies par le biais du serveur de passerelle Bureau à distance (passerelle Bureau à distance).

## <a name="syntax"></a>Syntaxe


```mof
uint32 DisableClipboard(
  [in] boolean Disabled
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*Désactivé* \[ dans\]
</dt> <dd>

Nouvelle valeur de la propriété **ClipboardDisabled** .

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

 

