---
title: Classe Win32_TSGatewayRADIUSServer
description: Décrit un serveur protocole RADIUS (Remote Authentication Dial-In User Service) (RADIUS), qui dispose d’un ensemble de stratégies d’autorisation de connexion Services Bureau à distance (RD \ 160 ; Majuscules).
ms.assetid: 40254354-f446-4e17-b7ec-649c98dd94f9
ms.tgt_platform: multiple
keywords:
- Win32_TSGatewayRADIUSServer de la classe Services Bureau à distance
- Win32_TSGatewayRADIUSServer de la classe Services Bureau à distance, Description
topic_type:
- apiref
api_name:
- Win32_TSGatewayRADIUSServer
- Win32_TSGatewayRADIUSServer.Name
- Win32_TSGatewayRADIUSServer.Priority
- Win32_TSGatewayRADIUSServer.SharedSecret
api_location:
- AagWmi.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4157d89dc942a1c2f8ff7d778f9f8048971902ba
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "126856672"
---
# <a name="win32_tsgatewayradiusserver-class"></a>\_Classe TSGatewayRADIUSServer Win32

Décrit un serveur protocole RADIUS (Remote Authentication Dial-In User Service) (RADIUS), qui dispose d’un ensemble de stratégies d’autorisation de connexion Services Bureau à distance.

RADIUS est un protocole standard utilisé pour transmettre les informations d’authentification, d’autorisation et de configuration entre un ordinateur serveur et un serveur d’authentification, appelé serveur RADIUS, avec une base de données qui stocke les informations utilisateur. Pour plus d’informations, consultez [protocole Radius](/previous-versions/windows/it-pro/windows-server-2003/cc781821(v=ws.10)).

## <a name="syntax"></a>Syntaxe

``` syntax
[dynamic, provider("AAGProvider"), AMENDMENT]
class Win32_TSGatewayRADIUSServer
{
  string Name;
  uint32 Priority;
  string SharedSecret;
};
```

## <a name="members"></a>Membres

La classe **Win32 \_ TSGatewayRADIUSServer** possède les types de membres suivants :

-   [Méthodes](#methods)
-   [Propriétés](#properties)

### <a name="methods"></a>Méthodes

La classe **Win32 \_ TSGatewayRADIUSServer** possède ces méthodes.



| Méthode                                                                 | Description                                                                  |
|:-----------------------------------------------------------------------|:-----------------------------------------------------------------------------|
| [**Complémentaires**](win32-tsgatewayradiusserver-add.md)                         | Ajoute un nouveau serveur RADIUS.<br/>                                         |
| [**Descendre**](movedown-win32-tsgatewayradiusserver.md)               | Déplace ce serveur RADIUS d’une position vers le dessous dans l’ordre de priorité.<br/> |
| [**MoveUp**](moveup-win32-tsgatewayradiusserver.md)                   | Déplace ce serveur RADIUS d’une position vers le haut dans l’ordre de priorité.<br/>   |
| [**Remove**](win32-tsgatewayradiusserver-remove.md)                   | Supprime le serveur RADIUS actuel.<br/>                                |
| [**SetName**](setname-win32-tsgatewayradiusserver.md)                 | Définit la propriété de **nom** pour ce serveur RADIUS.<br/>                |
| [**SetSharedSecret**](setsharedsecret-win32-tsgatewayradiusserver.md) | Définit la **propriété de serveur** à la une pour ce serveur RADIUS.<br/>        |
| [**Mise à jour**](update-win32-tsgatewayradiusserver.md)                   | Met à jour le serveur RADIUS actuel.<br/>                                |



 

### <a name="properties"></a>Propriétés

La classe **Win32 \_ TSGatewayRADIUSServer** a ces propriétés.

<dl> <dt>

**Nom**
</dt> <dd> <dl> <dt>

Type de données : **chaîne**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : [ **clé**](/windows/desktop/WmiSdk/key-qualifier)
</dt> </dl>

Nom du serveur RADIUS. Cette propriété peut être modifiée à l’aide de la méthode [**SetName**](setname-win32-tsgatewayradiusserver.md) .

</dd> <dt>

**Priorité**
</dt> <dd> <dl> <dt>

Type de données : **UInt32**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Priorité du serveur RADIUS. Le serveur de passerelle Bureau à distance recherche les Cap des services Bureau à distance sur les serveurs RADIUS en fonction de la priorité. Cette propriété peut être modifiée avec les méthodes [**MoveUp**](moveup-win32-tsgatewayradiusserver.md), [**MoveDown**](movedown-win32-tsgatewayradiusserver.md), [**Add**](win32-tsgatewayradiusserver-add.md)et [**Remove**](win32-tsgatewayradiusserver-remove.md) .

</dd> <dt>

**SharedSecret**
</dt> <dd> <dl> <dt>

Type de données : **chaîne**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Secret partagé pour le serveur RADIUS. Cette propriété peut être modifiée à l’aide de la méthode [**SetSharedSecret**](setsharedsecret-win32-tsgatewayradiusserver.md) .

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

[**\_TSGatewayResourceAuthorizationPolicy Win32**](win32-tsgatewayresourceauthorizationpolicy.md)
</dt> <dt>

[**\_TSGatewayResourceGroup Win32**](win32-tsgatewayresourcegroup.md)
</dt> <dt>

[**\_TSGatewayServerSettings Win32**](win32-tsgatewayserversettings.md)
</dt> </dl>

 

