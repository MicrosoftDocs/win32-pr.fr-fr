---
title: Méthode AddServers de la classe Win32_TSGatewayLoadBalancer
description: Ajoute des serveurs aux serveurs d’équilibrage de charge de la passerelle Bureau à distance (passerelle des services Bureau à distance) dans la propriété serveurs.
ms.assetid: ffcbe14b-5ada-4951-bf51-95db14af41d7
ms.tgt_platform: multiple
keywords:
- Services Bureau à distance de la méthode AddServers
- Services Bureau à distance de la méthode AddServers, classe Win32_TSGatewayLoadBalancer
- Win32_TSGatewayLoadBalancer de la classe Services Bureau à distance, méthode AddServers
topic_type:
- apiref
api_name:
- Win32_TSGatewayLoadBalancer.AddServers
api_location:
- AagWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a510fd6ecee12b5251ec84773327d6217463240f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104103176"
---
# <a name="addservers-method-of-the-win32_tsgatewayloadbalancer-class"></a>Méthode AddServers de la \_ classe Win32 TSGatewayLoadBalancer

Ajoute des serveurs aux serveurs d’équilibrage de charge de la passerelle Bureau à distance (passerelle des services Bureau à distance) dans la propriété **serveurs** .

## <a name="syntax"></a>Syntaxe


```mof
uint32 AddServers(
  [in] string Servers
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*Serveurs* \[ dans\]
</dt> <dd>

Liste séparée par des points-virgules des serveurs d’équilibrage de charge de la passerelle des services Bureau à distance à ajouter à la propriété **serveurs** .

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Si la méthode est réussie, elle retourne zéro. Si la méthode échoue, elle retourne une valeur différente de zéro. Pour obtenir la liste des codes d’erreur, consultez [services Bureau à distance codes d’erreur du fournisseur WMI](terminal-services-wmi-provider-error-codes.md).

## <a name="remarks"></a>Notes

Si plusieurs serveurs se trouvent dans le paramètre *serveurs* et que l’un des serveurs ne peut pas être traité, aucun des serveurs ne sera traité.

Vous devez être membre du groupe administrateurs pour appeler cette méthode.

Les fichiers format MOF (MOF) contiennent les définitions des classes Windows Management Instrumentation (WMI). Les fichiers MOF ne sont pas installés dans le cadre du kit de développement logiciel (SDK) Microsoft Windows. Ils sont installés sur le serveur lorsque vous ajoutez le rôle associé à l’aide de l’Gestionnaire de serveur. Pour plus d’informations sur les fichiers MOF, consultez [format MOF (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).

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

 

