---
title: Méthode RemoveUserGroupNames de la classe Win32_TSGatewayResourceAuthorizationPolicy
description: Supprime les noms de groupes d’utilisateurs spécifiés des groupes d’utilisateurs existants dans la propriété UserGroupNames.
ms.assetid: 8538e41a-b9ae-43ce-b19a-40a40f9a12f5
ms.tgt_platform: multiple
keywords:
- Services Bureau à distance de la méthode RemoveUserGroupNames
- Services Bureau à distance de la méthode RemoveUserGroupNames, classe Win32_TSGatewayResourceAuthorizationPolicy
- Win32_TSGatewayResourceAuthorizationPolicy de la classe Services Bureau à distance, méthode RemoveUserGroupNames
topic_type:
- apiref
api_name:
- Win32_TSGatewayResourceAuthorizationPolicy.RemoveUserGroupNames
api_location:
- AagWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c7c20051451d95b4c93b3ca23120acec9302aa5bc2bf1362cad818c993d1105d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120009209"
---
# <a name="removeusergroupnames-method-of-the-win32_tsgatewayresourceauthorizationpolicy-class"></a>Méthode RemoveUserGroupNames de la \_ classe Win32 TSGatewayResourceAuthorizationPolicy

Supprime les noms de groupes d’utilisateurs spécifiés des groupes d’utilisateurs existants dans la propriété **UserGroupNames** .

## <a name="syntax"></a>Syntaxe


```mof
uint32 RemoveUserGroupNames(
  [in] string UserGroupNames
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*UserGroupNames* \[ dans\]
</dt> <dd>

Liste de noms de groupes d’utilisateurs séparés par des points-virgules.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Si la méthode est réussie, elle retourne zéro. Si la méthode échoue, elle retourne une valeur différente de zéro. Pour obtenir la liste des codes d’erreur, consultez [services Bureau à distance codes d’erreur du fournisseur WMI](terminal-services-wmi-provider-error-codes.md).

## <a name="remarks"></a>Remarques

Si plusieurs noms de groupes d’utilisateurs se trouvent dans le paramètre *UserGroupNames* et que l’un des noms ne peut pas être traité, aucun nom ne sera traité.

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

[**\_TSGatewayResourceAuthorizationPolicy Win32**](win32-tsgatewayresourceauthorizationpolicy.md)
</dt> </dl>

 

