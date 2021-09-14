---
title: Classe Win32_TSGatewayResourceGroup
description: Décrit un groupe de ressources, qui mappe un ensemble de ressources (noms d’ordinateur) à une entité unique.
ms.assetid: 5715a2ea-9bbc-4704-835e-ba6d93a72368
ms.tgt_platform: multiple
keywords:
- Win32_TSGatewayResourceGroup de la classe Services Bureau à distance
- Win32_TSGatewayResourceGroup de la classe Services Bureau à distance, Description
topic_type:
- apiref
api_name:
- Win32_TSGatewayResourceGroup
- Win32_TSGatewayResourceGroup.Name
- Win32_TSGatewayResourceGroup.Description
- Win32_TSGatewayResourceGroup.AssociatedRAPs
- Win32_TSGatewayResourceGroup.Resources
api_location:
- AagWmi.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9ffeda42abafd24526360f5e549f004cae0c3140
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "126856635"
---
# <a name="win32_tsgatewayresourcegroup-class"></a>\_Classe TSGatewayResourceGroup Win32

Décrit un groupe de ressources, qui mappe un ensemble de ressources (noms d’ordinateur) à une entité unique.

## <a name="syntax"></a>Syntaxe

``` syntax
[dynamic, provider("AAGProvider"), AMENDMENT]
class Win32_TSGatewayResourceGroup
{
  string Name;
  string Description;
  string AssociatedRAPs;
  string Resources;
};
```

## <a name="members"></a>Membres

La classe **Win32 \_ TSGatewayResourceGroup** possède les types de membres suivants :

-   [Méthodes](#methods)
-   [Propriétés](#properties)

### <a name="methods"></a>Méthodes

La classe **Win32 \_ TSGatewayResourceGroup** possède ces méthodes.



| Méthode                                                                  | Description                                                                           |
|:------------------------------------------------------------------------|:--------------------------------------------------------------------------------------|
| [**AddResources**](addresources-win32-tsgatewayresourcegroup.md)       | Ajoute des ressources à la propriété des **ressources** pour ce groupe de ressources.<br/>      |
| [**Créer**](create-win32-tsgatewayresourcegroup.md)                   | Crée un groupe de ressources.<br/>                                                  |
| [**DELETE**](delete-win32-tsgatewayresourcegroup.md)                   | Supprime ce groupe de ressources.<br/>                                               |
| [**RemoveResources**](removeresources-win32-tsgatewayresourcegroup.md) | Supprime les ressources de la propriété des **ressources** pour ce groupe de ressources.<br/> |
| [**SetDescription**](setdescription-win32-tsgatewayresourcegroup.md)   | Définit la propriété **Description** pour ce groupe de ressources.<br/>                 |
| [**SetName**](setname-win32-tsgatewayresourcegroup.md)                 | Définit la propriété de **nom** pour ce groupe de ressources.<br/>                        |
| [**SetResources**](setresources-win32-tsgatewayresourcegroup.md)       | Définit la propriété des **ressources** pour ce groupe de ressources.<br/>                   |
| [**Mise à jour**](update-win32-tsgatewayresourcegroup.md)                   | Met à jour ce groupe de ressources.<br/>                                               |



 

### <a name="properties"></a>Propriétés

La classe **Win32 \_ TSGatewayResourceGroup** a ces propriétés.

<dl> <dt>

**AssociatedRAPs**
</dt> <dd> <dl> <dt>

Type de données : **chaîne**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Liste délimitée par des points-virgules de Services Bureau à distance les stratégies d’autorisation des ressources (RD stratégies) associées à ce groupe de ressources.

</dd> <dt>

**Description**
</dt> <dd> <dl> <dt>

Type de données : **chaîne**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Description du groupe de ressources. Cette propriété peut être modifiée à l’aide de la méthode [**SetDescription**](setdescription-win32-tsgatewayresourcegroup.md) .

</dd> <dt>

**Nom**
</dt> <dd> <dl> <dt>

Type de données : **chaîne**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : [ **clé**](/windows/desktop/WmiSdk/key-qualifier)
</dt> </dl>

Nom du groupe de ressources. Cette propriété peut être modifiée à l’aide de la méthode [**SetName**](setname-win32-tsgatewayresourcegroup.md) .

</dd> <dt>

**Ressources**
</dt> <dd> <dl> <dt>

Type de données : **chaîne**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Liste de ressources séparées par des points-virgules dans ce groupe de ressources. « \* » Signifie toutes les ressources. Cette propriété peut être modifiée avec les méthodes [**SetResources**](setresources-win32-tsgatewayresourcegroup.md), [**AddResources**](addresources-win32-tsgatewayresourcegroup.md), [**RemoveResources**](removeresources-win32-tsgatewayresourcegroup.md)et [**Update**](update-win32-tsgatewayresourcegroup.md) .

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

[**\_TSGatewayResourceAuthorizationPolicy Win32**](win32-tsgatewayresourceauthorizationpolicy.md)
</dt> <dt>

[**\_TSGatewayServerSettings Win32**](win32-tsgatewayserversettings.md)
</dt> </dl>

 

