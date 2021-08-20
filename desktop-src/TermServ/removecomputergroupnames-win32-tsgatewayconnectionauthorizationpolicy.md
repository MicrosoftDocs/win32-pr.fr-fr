---
title: Méthode RemoveComputerGroupNames de la classe Win32_TSGatewayConnectionAuthorizationPolicy
description: Supprime les noms de groupes d’ordinateurs spécifiés de la propriété ComputerGroupNames.
ms.assetid: 5f4e566a-1a2e-459d-ab6c-53ffd42271d8
ms.tgt_platform: multiple
keywords:
- Services Bureau à distance de la méthode RemoveComputerGroupNames
- Services Bureau à distance de la méthode RemoveComputerGroupNames, classe Win32_TSGatewayConnectionAuthorizationPolicy
- Win32_TSGatewayConnectionAuthorizationPolicy de la classe Services Bureau à distance, méthode RemoveComputerGroupNames
topic_type:
- apiref
api_name:
- Win32_TSGatewayConnectionAuthorizationPolicy.RemoveComputerGroupNames
api_location:
- AagWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c2df87623ff9a6fe4ee7596b21db3fc03957473c1be8b0bff421aa342864edfc
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118127619"
---
# <a name="removecomputergroupnames-method-of-the-win32_tsgatewayconnectionauthorizationpolicy-class"></a>Méthode RemoveComputerGroupNames de la \_ classe Win32 TSGatewayConnectionAuthorizationPolicy

Supprime les noms de groupes d’ordinateurs spécifiés de la propriété **ComputerGroupNames** .

## <a name="syntax"></a>Syntaxe


```mof
uint32 RemoveComputerGroupNames(
  [in] string ComputerGroupNames
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*ComputerGroupNames* \[ dans\]
</dt> <dd>

Liste de noms de groupes d’ordinateurs séparés par des points-virgules à supprimer de la propriété **ComputerGroupNames** . Les noms des groupes d’ordinateurs doivent être au format *domaine \\ ComputerGroupName*.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Si la méthode est réussie, elle retourne zéro. Si la méthode échoue, elle retourne une valeur différente de zéro. Pour obtenir la liste des codes d’erreur, consultez [services Bureau à distance codes d’erreur du fournisseur WMI](terminal-services-wmi-provider-error-codes.md).

## <a name="remarks"></a>Remarques

Si plusieurs noms de groupe d’ordinateurs se trouvent dans le paramètre *ComputerGroupNames* et que l’un des noms ne peut pas être traité, aucun nom ne sera traité.

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

 

