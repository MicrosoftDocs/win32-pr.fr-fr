---
title: Méthode SetComputerGroupNames de la classe Win32_TSGatewayConnectionAuthorizationPolicy
description: Définit la propriété ComputerGroupNames.
ms.assetid: dd6747df-140f-4eeb-857b-d14f8713586c
ms.tgt_platform: multiple
keywords:
- Services Bureau à distance de la méthode SetComputerGroupNames
- Services Bureau à distance de la méthode SetComputerGroupNames, classe Win32_TSGatewayConnectionAuthorizationPolicy
- Win32_TSGatewayConnectionAuthorizationPolicy de la classe Services Bureau à distance, méthode SetComputerGroupNames
topic_type:
- apiref
api_name:
- Win32_TSGatewayConnectionAuthorizationPolicy.SetComputerGroupNames
api_location:
- AagWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a99c29ce37aeb8bfad0ae77197c7364b0135fa99
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104384564"
---
# <a name="setcomputergroupnames-method-of-the-win32_tsgatewayconnectionauthorizationpolicy-class"></a>Méthode SetComputerGroupNames de la \_ classe Win32 TSGatewayConnectionAuthorizationPolicy

Définit la propriété **ComputerGroupNames** .

## <a name="syntax"></a>Syntaxe


```mof
uint32 SetComputerGroupNames(
  [in] string ComputerGroupNames
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*ComputerGroupNames* \[ dans\]
</dt> <dd>

Liste des noms de groupes d’ordinateurs séparés par des points-virgules. Cette valeur peut être vide. Les noms sont au format *domaine \\ ComputerGroupName*. Si une valeur est spécifiée, l’ordinateur client doit appartenir à l’un de ces groupes d’ordinateurs pour que l’utilisateur accède au serveur de passerelle Bureau à distance.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Si la méthode est réussie, elle retourne zéro. Si la méthode échoue, elle retourne une valeur différente de zéro. Pour obtenir la liste des codes d’erreur, consultez [services Bureau à distance codes d’erreur du fournisseur WMI](terminal-services-wmi-provider-error-codes.md).

## <a name="remarks"></a>Notes

Si plusieurs noms de groupe d’ordinateurs se trouvent dans le paramètre *ComputerGroupNames* et que l’un des noms ne peut pas être traité, aucun nom ne sera traité.

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

[**\_TSGatewayConnectionAuthorizationPolicy Win32**](win32-tsgatewayconnectionauthorizationpolicy.md)
</dt> </dl>

 

