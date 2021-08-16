---
title: MoveDown, méthode de la classe Win32_TSGatewayConnectionAuthorizationPolicy
description: Déplace la stratégie d’autorisation de connexion Bureau à distance actuelle (RD \ 160 ; CAP) une position dans l’ordre dans lequel RD \ 160 ; Les majuscules sont évaluées.
ms.assetid: 57349e59-e200-4789-bbcb-d474eacde39d
ms.tgt_platform: multiple
keywords:
- MoveDown, méthode Services Bureau à distance
- MoveDown, méthode Services Bureau à distance, classe Win32_TSGatewayConnectionAuthorizationPolicy
- Win32_TSGatewayConnectionAuthorizationPolicy de la classe Services Bureau à distance, méthode MoveDown
topic_type:
- apiref
api_name:
- Win32_TSGatewayConnectionAuthorizationPolicy.MoveDown
api_location:
- AagWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 54f401a87445a16fd07d77480bd56bdc904240784d3a7a41e4f7a76a3847f723
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119058737"
---
# <a name="movedown-method-of-the-win32_tsgatewayconnectionauthorizationpolicy-class"></a>MoveDown, méthode de la \_ classe TSGatewayConnectionAuthorizationPolicy Win32

Déplace la stratégie d’autorisation des connexions Bureau à distance en cours d’une position vers le dessous dans l’ordre dans lequel les majuscules Bureau à distance sont évaluées. Cette méthode incrémente la propriété **Order** de la stratégie d’autorisation des connexions aux services Bureau à distance actuelle et décrémente la propriété **Order** de la stratégie d’autorisation des connexions aux services Bureau à distance qui a suivi la stratégie Bureau à distance actuelle.

## <a name="syntax"></a>Syntaxe


```mof
uint32 MoveDown();
```



## <a name="parameters"></a>Paramètres

Cette méthode n’a aucun paramètre.

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
</dt> <dt>

[**MoveUp**](moveup-win32-tsgatewayconnectionauthorizationpolicy.md)
</dt> </dl>

 

