---
description: Cette classe est déconseillée. Au lieu de cela, nous vous recommandons de dériver de la \_ classe de service CIM.
ms.assetid: 67b3a96e-4549-41e0-8097-f8d145df0c49
title: Classe CIM_NetworkService
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_NetworkService
- CIM_NetworkService.Keywords
- CIM_NetworkService.ServiceURL
- CIM_NetworkService.StartupConditions
- CIM_NetworkService.StartupParameters
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: cfb2ea7b122516cc3b62f675684649e22577171f713856638f97985d9713e8d5
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119694689"
---
# <a name="cim_networkservice-class"></a>\_Classe CIM NetworkService

Cette classe est déconseillée. Au lieu de cela, nous vous recommandons de dériver de la classe de [**\_ service CIM**](cim-service.md) .

## <a name="syntax"></a>Syntaxe

``` syntax
[Deprecated("CIM_Service"), Abstract, Version("2.7.0"), UMLPackagePath("CIM::Network::RoutingForwarding"), AMENDMENT]
class CIM_NetworkService : CIM_Service
{
  string Keywords[];
  string ServiceURL;
  string StartupConditions[];
  string StartupParameters[];
};
```

## <a name="members"></a>Membres

La classe **CIM \_ NetworkService** possède les types de membres suivants :

-   [Propriétés](#properties)

### <a name="properties"></a>Propriétés

La classe **CIM \_ NetworkService** possède ces propriétés.

<dl> <dt>

**Mots clés**
</dt> <dd> <dl> <dt>

Type de données : tableau de **chaînes**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : [**déconseillé**](/windows/desktop/WmiSdk/standard-wmi-qualifiers) (« aucune valeur »)
</dt> </dl>

Cette propriété est déconseillée et ne doit pas être utilisée.

> [!Note]  
> Description déconseillée : un tableau de mots clés qui peuvent être utilisés dans les requêtes.

 

</dd> <dt>

**ServiceURL**
</dt> <dd> <dl> <dt>

Type de données : **chaîne**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : [**déconseillé**](/windows/desktop/WmiSdk/standard-wmi-qualifiers) ("CIM \_ ServiceAccessURI")
</dt> </dl>

Cette propriété est déconseillée. Au lieu de cela, nous vous recommandons la classe **CIM \_ ServiceAccessURI** .

> [!Note]  
> Description déconseillée : URL qui fournit le protocole, l’emplacement réseau et d’autres informations spécifiques au service nécessaires pour accéder au service.

 

</dd> <dt>

**StartupConditions**
</dt> <dd> <dl> <dt>

Type de données : tableau de **chaînes**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : [**déconseillé**](/windows/desktop/WmiSdk/standard-wmi-qualifiers) (« aucune valeur »)
</dt> </dl>

Cette propriété est déconseillée et ne doit pas être utilisée.

> [!Note]  
> Description déconseillée : conditions préalables qui doivent être remplies pour que ce service démarre correctement.

 

</dd> <dt>

**StartupParameters**
</dt> <dd> <dl> <dt>

Type de données : tableau de **chaînes**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : [**déconseillé**](/windows/desktop/WmiSdk/standard-wmi-qualifiers) (« aucune valeur »)
</dt> </dl>

Cette propriété est déconseillée et ne doit pas être utilisée.

> [!Note]  
> Description déconseillée : les paramètres qui doivent être fournis à la méthode **StartService** pour que ce service démarre correctement.

 

</dd> </dl>

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows 8<br/>                                                                                    |
| Serveur minimal pris en charge<br/> | Windows Server 2012<br/>                                                                          |
| Espace de noms<br/>                | \\Virtualisation racine \\ v2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>WindowsVirtualization. v2. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**\_Service CIM**](cim-service.md)
</dt> </dl>

 

