---
title: Méthode SetResourceGroup de la classe Win32_TSGatewayResourceAuthorizationPolicy
description: Définit le type et le nom du groupe de ressources.
ms.assetid: a3dd0ffa-a39b-46f9-8317-fcc90a8afcd1
ms.tgt_platform: multiple
keywords:
- Services Bureau à distance de la méthode SetResourceGroup
- Services Bureau à distance de la méthode SetResourceGroup, classe Win32_TSGatewayResourceAuthorizationPolicy
- Win32_TSGatewayResourceAuthorizationPolicy de la classe Services Bureau à distance, méthode SetResourceGroup
topic_type:
- apiref
api_name:
- Win32_TSGatewayResourceAuthorizationPolicy.SetResourceGroup
api_location:
- AagWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c29c4ca301a26fb3199891f3d25141f69402ecfe55bc46a2f3581c31e99b9445
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119058447"
---
# <a name="setresourcegroup-method-of-the-win32_tsgatewayresourceauthorizationpolicy-class"></a>Méthode SetResourceGroup de la \_ classe Win32 TSGatewayResourceAuthorizationPolicy

Définit le type et le nom du groupe de ressources.

## <a name="syntax"></a>Syntaxe


```mof
uint32 SetResourceGroup(
  [in] string ResourceGroupName,
  [in] string ResourceGroupType
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*ResourceGroupName* \[ dans\]
</dt> <dd>

Nom du groupe de ressources. Cette valeur remplace la propriété **ResourceGroupName** existante.

</dd> <dt>

*ResourceGroupType* \[ dans\]
</dt> <dd>

Identifie le type du groupe de ressources. Cette valeur remplace la propriété **ResourceGroupType** existante.

<dt>

ROUTAGE
</dt> <dd>

Groupe de ressources.

</dd> <dt>

CG
</dt> <dd>

Groupe d’ordinateurs, tel qu’il est stocké dans Active Directory Domain Services.

</dd> <dt>

TOUS les
</dt> <dd>

Toutes les ressources.

</dd> </dl> </dd> </dl>

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

[**\_TSGatewayResourceAuthorizationPolicy Win32**](win32-tsgatewayresourceauthorizationpolicy.md)
</dt> </dl>

 

