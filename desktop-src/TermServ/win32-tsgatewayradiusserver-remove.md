---
title: Méthode Remove de la classe Win32_TSGatewayRADIUSServer
description: Supprime le serveur de protocole RADIUS (Remote Authentication Dial-In User Service) (RADIUS) actuel.
ms.assetid: 915f6d38-ba6a-4994-8bb9-bfddb9aa6ff8
ms.tgt_platform: multiple
keywords:
- Supprimer la méthode Services Bureau à distance
- Supprimer la méthode Services Bureau à distance, Win32_TSGatewayRADIUSServer interface
- Win32_TSGatewayRADIUSServer Services Bureau à distance de l’interface, Remove, méthode
topic_type:
- apiref
api_name:
- Win32_TSGatewayRADIUSServer.Remove
api_location:
- AagWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 446a9ea6a9f2bdb4fada3fed38952988c0284b5bc4055503784c232255586407
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118126573"
---
# <a name="remove-method-of-the-win32_tsgatewayradiusserver-class"></a>Méthode Remove de la \_ classe TSGatewayRADIUSServer Win32

Supprime le serveur de protocole RADIUS (Remote Authentication Dial-In User Service) (RADIUS) actuel.

## <a name="syntax"></a>Syntaxe


```mof
uint32 Remove();
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

[**\_TSGatewayRADIUSServer Win32**](win32-tsgatewayradiusserver.md)
</dt> </dl>

 

