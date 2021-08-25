---
title: Méthode SetUserGroupNames de la classe Win32_TSGatewayResourceAuthorizationPolicy
description: Définit la propriété UserGroupNames pour la stratégie d’autorisation d’accès aux ressources Bureau à distance (RD \ 160 ; RAP).
ms.assetid: 91b77cd6-779e-460a-88a3-eda7a6fe99e5
ms.tgt_platform: multiple
keywords:
- Services Bureau à distance de la méthode SetUserGroupNames
- Services Bureau à distance de la méthode SetUserGroupNames, classe Win32_TSGatewayResourceAuthorizationPolicy
- Win32_TSGatewayResourceAuthorizationPolicy de la classe Services Bureau à distance, méthode SetUserGroupNames
topic_type:
- apiref
api_name:
- Win32_TSGatewayResourceAuthorizationPolicy.SetUserGroupNames
api_location:
- AagWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 18d4a54f042ebf99ff5a3b1bf16081ce0719578ef7fc2fd272e9ccc07a832822
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120008569"
---
# <a name="setusergroupnames-method-of-the-win32_tsgatewayresourceauthorizationpolicy-class"></a>Méthode SetUserGroupNames de la \_ classe Win32 TSGatewayResourceAuthorizationPolicy

Définit la propriété **UserGroupNames** pour la stratégie d’autorisation des ressources Bureau À distance (RD RAP).

## <a name="syntax"></a>Syntaxe


```mof
uint32 SetUserGroupNames(
  [in] string UserGroupNames
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*UserGroupNames* \[ dans\]
</dt> <dd>

Liste de noms de groupes d’utilisateurs séparés par des points-virgules. Les noms sont au format *domaine \\ UserGroupName*. Si l’utilisateur appartient à l’un de ces groupes d’utilisateurs, l’accès est autorisé.

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

 

