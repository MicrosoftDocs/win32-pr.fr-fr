---
title: Méthode IsLoadBalancingServer de la classe Win32_TSGatewayLoadBalancer
description: Détermine si le serveur de passerelle Bureau à distance (passerelle des services Bureau à distance) peut effectuer l’équilibrage de charge.
ms.assetid: ae1a91c1-0b8b-4bd0-83f9-41c973247f27
ms.tgt_platform: multiple
keywords:
- Services Bureau à distance de la méthode IsLoadBalancingServer
- Services Bureau à distance de la méthode IsLoadBalancingServer, classe Win32_TSGatewayLoadBalancer
- Win32_TSGatewayLoadBalancer de la classe Services Bureau à distance, méthode IsLoadBalancingServer
topic_type:
- apiref
api_name:
- Win32_TSGatewayLoadBalancer.IsLoadBalancingServer
api_location:
- AagWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: eb03abc90dfe0f1a289eacd5a3ae49e5276892bdb34b65ff3f86e4e8da2c593a
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119421319"
---
# <a name="isloadbalancingserver-method-of-the-win32_tsgatewayloadbalancer-class"></a>Méthode IsLoadBalancingServer de la \_ classe Win32 TSGatewayLoadBalancer

Détermine si le serveur de passerelle Bureau à distance (passerelle des services Bureau à distance) peut effectuer l’équilibrage de charge.

## <a name="syntax"></a>Syntaxe


```mof
uint32 IsLoadBalancingServer(
  [out] boolean LoadBalancing
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*LoadBalancing* \[ à\]
</dt> <dd>

**True** si le serveur peut effectuer l’équilibrage de charge et **false** dans le cas contraire.

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

[**\_TSGatewayLoadBalancer Win32**](win32-tsgatewayloadbalancer.md)
</dt> </dl>

 

