---
title: Créer une méthode de la classe Win32_TSGatewayResourceAuthorizationPolicy
description: Crée une stratégie d’autorisation d’accès aux ressources Bureau à distance (RD \ 160 ; RAP).
ms.assetid: 3301a543-cdf9-4528-a29e-691054ef81c9
ms.tgt_platform: multiple
keywords:
- Créer une méthode Services Bureau à distance
- Create Method Services Bureau à distance, Win32_TSGatewayResourceAuthorizationPolicy Class
- Win32_TSGatewayResourceAuthorizationPolicy de la classe Services Bureau à distance, Create, méthode
topic_type:
- apiref
api_name:
- Win32_TSGatewayResourceAuthorizationPolicy.Create
api_location:
- AagWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2a85055ed9c8930a47e9a9949693457456fd8f261e1cb458e1092eb570532231
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118131183"
---
# <a name="create-method-of-the-win32_tsgatewayresourceauthorizationpolicy-class"></a>Créer une méthode de la \_ classe TSGatewayResourceAuthorizationPolicy Win32

Crée une stratégie d’autorisation des ressources Bureau à distance (RD RAP).

## <a name="syntax"></a>Syntaxe


```mof
uint32 Create(
  [in] string  Name,
  [in] string  Description,
  [in] boolean Enabled,
  [in] string  ResourceGroupType,
  [in] string  ResourceGroupName,
  [in] string  UserGroupNames,
  [in] string  ProtocolNames,
  [in] string  PortNumbers
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*Nom* \[ dans\]
</dt> <dd>

Nom de la RD RAP.

</dd> <dt>

*Description* \[ dans\]
</dt> <dd>

Description de la RD RAP.

</dd> <dt>

*Activé* \[ dans\]
</dt> <dd>

Indique si le RAP (RD) doit être activé.

</dd> <dt>

*ResourceGroupType* \[ dans\]
</dt> <dd>

Type de groupe de ressources.

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

</dd> </dl> </dd> <dt>

*ResourceGroupName* \[ dans\]
</dt> <dd>

Nom du groupe de ressources.

</dd> <dt>

*UserGroupNames* \[ dans\]
</dt> <dd>

Liste de noms de groupes d’utilisateurs séparés par des points-virgules. Si l’utilisateur appartient à l’un de ces groupes d’utilisateurs, l’accès est autorisé. Les noms des groupes d’utilisateurs doivent être au format *domaine \\ UserGroupName*.

</dd> <dt>

*ProtocolNames* \[ dans\]
</dt> <dd>

Liste délimitée par des points-virgules des noms de protocole qui sont activés pour cette stratégie. Les noms doivent correspondre au retour de la méthode [**GetProtocolName**](getprotocolname-win32-tsgatewayserversettings.md) de la classe [**Win32 \_ TSGatewayServerSettings**](win32-tsgatewayserversettings.md) .

</dd> <dt>

*PortNumbers* \[ dans\]
</dt> <dd>

Liste délimitée par des points-virgules des numéros de port activés pour cette stratégie. Pour autoriser n’importe quel numéro de port, définissez « \* ».

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

[**\_TSGatewayResourceAuthorizationPolicy Win32**](win32-tsgatewayresourceauthorizationpolicy.md)
</dt> </dl>

 

