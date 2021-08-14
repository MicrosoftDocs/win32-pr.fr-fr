---
title: Méthode DeleteAllServers de la classe Win32_TSGatewayLoadBalancer
description: Supprime tous les serveurs d’équilibrage de charge de la passerelle des services Bureau à distance de Bureau à distance qui participent à la batterie d’équilibrage de charge.
ms.assetid: 091ed866-8f2b-47b8-990b-e9a6d7e1194c
ms.tgt_platform: multiple
keywords:
- Services Bureau à distance de la méthode DeleteAllServers
- Services Bureau à distance de la méthode DeleteAllServers, classe Win32_TSGatewayLoadBalancer
- Win32_TSGatewayLoadBalancer de la classe Services Bureau à distance, méthode DeleteAllServers
topic_type:
- apiref
api_name:
- Win32_TSGatewayLoadBalancer.DeleteAllServers
api_location:
- AagWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7098bfac95c80baad59c163581d1cbb26f73df0234a0f67d1d07c587ff6e06bc
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118131041"
---
# <a name="deleteallservers-method-of-the-win32_tsgatewayloadbalancer-class"></a>Méthode DeleteAllServers de la \_ classe Win32 TSGatewayLoadBalancer

Supprime tous les serveurs d’équilibrage de charge de la passerelle des services Bureau à distance de Bureau à distance qui participent à la batterie d’équilibrage de charge.

## <a name="syntax"></a>Syntaxe


```mof
uint32 DeleteAllServers();
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

[**\_TSGatewayLoadBalancer Win32**](win32-tsgatewayloadbalancer.md)
</dt> </dl>

 

