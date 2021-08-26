---
description: Définit une connexion actuellement activée et configurée pour fournir une communication entre deux \_ objets SERVICEACCESSPOINT CIM.
ms.assetid: 03f8e43f-a77b-46e2-bb7d-c29758c65aee
title: Classe CIM_ActiveConnection
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_ActiveConnection
- CIM_ActiveConnection.Antecedent
- CIM_ActiveConnection.Dependent
- CIM_ActiveConnection.TrafficType
- CIM_ActiveConnection.OtherTrafficDescription
- CIM_ActiveConnection.IsUnidirectional
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: a2961779744e90d0e4281e53c3d78c92081993027deb6c435846abbffb41b110
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120041759"
---
# <a name="cim_activeconnection-class"></a>\_Classe ACTIVECONNECTION CIM

Définit une connexion actuellement activée et configurée pour fournir une communication entre deux objets **\_ ServiceAccessPoint CIM** . **CIM \_ ActiveConnection** est utilisé lorsque la connexion n’est pas traitée comme un objet **CIM \_ propriété ManagedElement** . Les points d’accès de service qui sont connectés par une connexion active sont généralement au même niveau réseau ou couche application.

## <a name="syntax"></a>Syntaxe

``` syntax
[Association, Abstract, Version("2.10.0"), UMLPackagePath("CIM::Core::Service"), AMENDMENT]
class CIM_ActiveConnection : CIM_SAPSAPDependency
{
  CIM_ServiceAccessPoint REF Antecedent;
  CIM_ServiceAccessPoint REF Dependent;
  uint16                     TrafficType;
  string                     OtherTrafficDescription;
  boolean                    IsUnidirectional;
};
```

## <a name="members"></a>Membres

La classe **CIM \_ ActiveConnection** possède les types de membres suivants :

-   [Propriétés](#properties)

### <a name="properties"></a>Propriétés

La classe **CIM \_ ActiveConnection** possède ces propriétés.

<dl> <dt>

**Antécédent**
</dt> <dd> <dl> <dt>

Type de données : **CIM ( \_ ServiceAccessPoint** )
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Antecedent")
</dt> </dl>

Point d’accès au service connecté à l’autre point d’accès de service via la connexion active. **CIM \_ Objet ServiceAccessPoint** . Dans une connexion unidirectionnelle, ce point d’accès est celui qui transmet les données.

</dd> <dt>

**Charge**
</dt> <dd> <dl> <dt>

Type de données : **CIM ( \_ ServiceAccessPoint** )
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : [**override**](/windows/desktop/WmiSdk/standard-qualifiers) (« Dependent »)
</dt> </dl>

Point d’accès au service qui est configuré pour communiquer ou qui communique activement avec le point d’accès au service spécifié dans la propriété **Antecedent** . Dans une connexion unidirectionnelle, ce point d’accès est celui qui reçoit des données.

</dd> <dt>

**IsUnidirectional**
</dt> <dd> <dl> <dt>

Type de données : **booléen**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

True si la connexion est unidirectionnelle ; false si la connexion est bidirectionnelle. Lorsque la connexion est unidirectionnelle, la propriété **Antecedent** spécifie le point d’accès qui transmet les données. Dans une connexion bidirectionnelle, l' **antécédent** peut spécifier un point d’accès affecté à la connexion.

</dd> <dt>

**OtherTrafficDescription**
</dt> <dd> <dl> <dt>

Type de données : **chaîne**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : [**déconseillé**](/windows/desktop/WmiSdk/standard-wmi-qualifiers) (« aucune valeur »), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) («**CIM \_ ActiveConnection**.**TrafficType**")
</dt> </dl>

> [!Note]  
> Cette propriété est déconseillée. Au lieu de cela, nous vous recommandons de spécifier ces informations dans l’adressage, le protocole et les fonctionnalités de base des points de terminaison.

 

Description du type de trafic qui est spécifié lorsque la propriété **TrafficType** est définie sur « 1 » (autre).

</dd> <dt>

**TrafficType**
</dt> <dd> <dl> <dt>

Type de données : **UInt16**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : [**déconseillé**](/windows/desktop/WmiSdk/standard-wmi-qualifiers) (« aucune valeur »), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) («**CIM \_ ActiveConnection**.**OtherTrafficDescription**")
</dt> </dl>

> [!Note]  
> Cette propriété est déconseillée. Au lieu de cela, nous vous recommandons de spécifier ces informations dans l’adressage, le protocole et les fonctionnalités de base des points de terminaison.

 

Type de trafic transmis sur cette connexion.

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

**Inconnu** (0)


</dt> <dd></dd> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

**Autre** (1)


</dt> <dd></dd> <dt>

<span id="Unicast"></span><span id="unicast"></span><span id="UNICAST"></span>

**Monodiffusion** (2)


</dt> <dd></dd> <dt>

<span id="Broadcast"></span><span id="broadcast"></span><span id="BROADCAST"></span>

**Diffusion** (3)


</dt> <dd></dd> <dt>

<span id="Multicast"></span><span id="multicast"></span><span id="MULTICAST"></span>

**Multidiffusion** (4)


</dt> <dd></dd> <dt>

<span id="Anycast"></span><span id="anycast"></span><span id="ANYCAST"></span>

**Anycast** (5)


</dt> <dd></dd> </dl>

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

[**\_SAPSAPDEPENDENCY CIM**](cim-sapsapdependency.md)
</dt> </dl>

 

