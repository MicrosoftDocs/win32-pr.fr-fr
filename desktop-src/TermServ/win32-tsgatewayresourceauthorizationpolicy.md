---
title: Classe Win32_TSGatewayResourceAuthorizationPolicy
description: Décrit une stratégie d’autorisation d’accès aux ressources Bureau à distance (RD \ 160 ; RAP). Un bureau à distance \ 160 ; RAP est utilisé pour déterminer si un utilisateur est autorisé à se connecter à une ressource spécifiée par le biais de Bureau à distance Gateway (passerelle des services Bureau à distance).
ms.assetid: 284a868d-7856-4a25-ba7b-b4beba8ffffc
ms.tgt_platform: multiple
keywords:
- Win32_TSGatewayResourceAuthorizationPolicy de la classe Services Bureau à distance
- Win32_TSGatewayResourceAuthorizationPolicy de la classe Services Bureau à distance, Description
topic_type:
- apiref
api_name:
- Win32_TSGatewayResourceAuthorizationPolicy
- Win32_TSGatewayResourceAuthorizationPolicy.Name
- Win32_TSGatewayResourceAuthorizationPolicy.Description
- Win32_TSGatewayResourceAuthorizationPolicy.Enabled
- Win32_TSGatewayResourceAuthorizationPolicy.ResourceGroupType
- Win32_TSGatewayResourceAuthorizationPolicy.ResourceGroupName
- Win32_TSGatewayResourceAuthorizationPolicy.UserGroupNames
- Win32_TSGatewayResourceAuthorizationPolicy.ProtocolNames
- Win32_TSGatewayResourceAuthorizationPolicy.PortNumbers
api_location:
- AagWmi.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0c262cb1ce3351c89dc5d7edf3b0d106116e83b7
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "126856653"
---
# <a name="win32_tsgatewayresourceauthorizationpolicy-class"></a>\_Classe TSGatewayResourceAuthorizationPolicy Win32

Décrit une stratégie d’autorisation des ressources Bureau à distance (RD RAP). Une connexion Bureau à distance est utilisée pour décider si un utilisateur est autorisé à se connecter à une ressource spécifiée Bureau à distance via la passerelle des services Bureau à distance.

## <a name="syntax"></a>Syntaxe

``` syntax
[dynamic, provider("AAGProvider"), AMENDMENT]
class Win32_TSGatewayResourceAuthorizationPolicy
{
  string  Name;
  string  Description;
  boolean Enabled;
  string  ResourceGroupType;
  string  ResourceGroupName;
  string  UserGroupNames;
  string  ProtocolNames;
  string  PortNumbers;
};
```

## <a name="members"></a>Membres

La classe **Win32 \_ TSGatewayResourceAuthorizationPolicy** possède les types de membres suivants :

-   [Méthodes](#methods)
-   [Propriétés](#properties)

### <a name="methods"></a>Méthodes

La classe **Win32 \_ TSGatewayResourceAuthorizationPolicy** possède ces méthodes.



| Méthode                                                                                          | Description                                                                                                         |
|:------------------------------------------------------------------------------------------------|:--------------------------------------------------------------------------------------------------------------------|
| [**AddUserGroupNames**](addusergroupnames-win32-tsgatewayresourceauthorizationpolicy.md)       | Ajoute les noms de groupes d’utilisateurs spécifiés aux groupes d’utilisateurs existants dans la propriété **UserGroupNames** .<br/>      |
| [**Créer**](create-win32-tsgatewayresourceauthorizationpolicy.md)                             | Crée un RAP.<br/>                                                                                       |
| [**DELETE**](delete-win32-tsgatewayresourceauthorizationpolicy.md)                             | Supprime le RAP (RD) actuel.<br/>                                                                              |
| [**RemoveUserGroupNames**](removeusergroupnames-win32-tsgatewayresourceauthorizationpolicy.md) | Supprime les noms de groupes d’utilisateurs spécifiés des groupes d’utilisateurs existants dans la propriété **UserGroupNames** .<br/> |
| [**SetDescription**](setdescription-win32-tsgatewayresourceauthorizationpolicy.md)             | Définit la propriété **Description** de la RD RAP.<br/>                                                        |
| [**SetEnabled**](setenabled-win32-tsgatewayresourceauthorizationpolicy.md)                     | Active ou désactive la RD RAP en définissant la propriété **Enabled** .<br/>                                      |
| [**SetName**](setname-win32-tsgatewayresourceauthorizationpolicy.md)                           | Définit la propriété de **nom** pour la RD RAP.<br/>                                                               |
| [**SetPortNumbers**](setportnumbers-win32-tsgatewayresourceauthorizationpolicy.md)             | Définit la propriété **PortNumbers** pour la RD RAP.<br/>                                                        |
| [**SetResourceGroup**](setresourcegroup-win32-tsgatewayresourceauthorizationpolicy.md)         | Définit les propriétés **ResourceGroupType** et **ResourceGroupName** .<br/>                                     |
| [**SetUserGroupNames**](setusergroupnames-win32-tsgatewayresourceauthorizationpolicy.md)       | Définit la propriété **UserGroupNames** pour la RD RAP.<br/>                                                     |
| [**Mise à jour**](update-win32-tsgatewayresourceauthorizationpolicy.md)                             | Met à jour le RAP RD actuel.<br/>                                                                              |



 

### <a name="properties"></a>Propriétés

La classe **Win32 \_ TSGatewayResourceAuthorizationPolicy** a ces propriétés.

<dl> <dt>

**Description**
</dt> <dd> <dl> <dt>

Type de données : **chaîne**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Description de la RD RAP. Cette propriété est modifiée à l’aide de la méthode [**SetDescription**](setdescription-win32-tsgatewayresourceauthorizationpolicy.md) .

</dd> <dt>

**Activé**
</dt> <dd> <dl> <dt>

Type de données : **booléen**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Indique si ce RAP est activé. Cette propriété est modifiée à l’aide de la méthode [**SetEnabled**](setenabled-win32-tsgatewayresourceauthorizationpolicy.md) .

</dd> <dt>

**Nom**
</dt> <dd> <dl> <dt>

Type de données : **chaîne**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : [ **clé**](/windows/desktop/WmiSdk/key-qualifier)
</dt> </dl>

Nom de la RD RAP. Cette propriété est modifiée à l’aide de la méthode [**SetName**](setname-win32-tsgatewayresourceauthorizationpolicy.md) .

</dd> <dt>

**PortNumbers**
</dt> <dd> <dl> <dt>

Type de données : **chaîne**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Liste des numéros de port séparés par des points-virgules autorisés pour cette stratégie. Pour autoriser n’importe quel numéro de port, définissez « \* ».

</dd> <dt>

**ProtocolNames**
</dt> <dd> <dl> <dt>

Type de données : **chaîne**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Liste des noms de protocole séparés par des points-virgules qui sont activés pour cette stratégie. Les noms doivent correspondre au retour de la méthode [**GetProtocolName**](getprotocolname-win32-tsgatewayserversettings.md) de la classe [**Win32 \_ TSGatewayServerSettings**](win32-tsgatewayserversettings.md) .

</dd> <dt>

**ResourceGroupName**
</dt> <dd> <dl> <dt>

Type de données : **chaîne**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Nom du groupe de ressources. Cette propriété est modifiée à l’aide de la méthode [**SetResourceGroup**](setresourcegroup-win32-tsgatewayresourceauthorizationpolicy.md) .

</dd> <dt>

**ResourceGroupType**
</dt> <dd> <dl> <dt>

Type de données : **chaîne**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Identifie le type du groupe de ressources. Cette propriété est modifiée à l’aide de la méthode [**SetResourceGroup**](setresourcegroup-win32-tsgatewayresourceauthorizationpolicy.md) .

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

</dd> </dl>

</dd> <dt>

**UserGroupNames**
</dt> <dd> <dl> <dt>

Type de données : **chaîne**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Liste de noms de groupes d’utilisateurs séparés par des points-virgules. Si l’utilisateur appartient à l’un de ces groupes d’utilisateurs, l’accès est autorisé. Cette propriété est modifiée à l’aide des méthodes [**SetUserGroupNames**](setusergroupnames-win32-tsgatewayresourceauthorizationpolicy.md), [**AddUserGroupNames**](addusergroupnames-win32-tsgatewayresourceauthorizationpolicy.md)et [**RemoveUserGroupNames**](removeusergroupnames-win32-tsgatewayresourceauthorizationpolicy.md) .

</dd> </dl>

## <a name="remarks"></a>Notes

Pour utiliser cette classe, vous devez être membre du groupe administrateurs.

les fichiers format MOF (MOF) contiennent les définitions des classes Windows Management Instrumentation (WMI). les fichiers MOF ne sont pas installés dans le cadre du kit de développement logiciel (SDK) Microsoft Windows. Ils sont installés sur le serveur lorsque vous ajoutez le rôle associé à l’aide de l’Gestionnaire de serveur. Pour plus d’informations sur les fichiers MOF, consultez [format MOF (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|-------------------------------------|------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Aucun pris en charge<br/>                                                                |
| Serveur minimal pris en charge<br/> | Windows Server 2008<br/>                                                           |
| Espace de noms<br/>                | Racine \\ cimv2 \\ licences TS<br/>                                                 |
| MOF<br/>                      | <dl> <dt>TSGateway. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>AagWmi.dll</dt> </dl>    |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**\_TSGatewayConnection Win32**](win32-tsgatewayconnection.md)
</dt> <dt>

[**\_TSGatewayConnectionAuthorizationPolicy Win32**](win32-tsgatewayconnectionauthorizationpolicy.md)
</dt> <dt>

[**\_TSGatewayLoadBalancer Win32**](win32-tsgatewayloadbalancer.md)
</dt> <dt>

[**\_TSGatewayRADIUSServer Win32**](win32-tsgatewayradiusserver.md)
</dt> <dt>

[**\_TSGatewayResourceGroup Win32**](win32-tsgatewayresourcegroup.md)
</dt> <dt>

[**\_TSGatewayServerSettings Win32**](win32-tsgatewayserversettings.md)
</dt> </dl>

 

