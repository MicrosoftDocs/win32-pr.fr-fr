---
description: Représente la valeur d’instance d’une métrique.
ms.assetid: 6b272ae8-7684-45bb-bff8-6559680cc8b6
title: Classe CIM_BaseMetricValue
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_BaseMetricValue
- CIM_BaseMetricValue.InstanceID
- CIM_BaseMetricValue.MetricDefinitionId
- CIM_BaseMetricValue.MeasuredElementName
- CIM_BaseMetricValue.TimeStamp
- CIM_BaseMetricValue.Duration
- CIM_BaseMetricValue.MetricValue
- CIM_BaseMetricValue.BreakdownDimension
- CIM_BaseMetricValue.BreakdownValue
- CIM_BaseMetricValue.Volatile
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 107dc3721ee32ca7f51efd563cdd6af14af483a69a5990e0b107a153b79b9351
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119014697"
---
# <a name="cim_basemetricvalue-class"></a>\_Classe CIM BaseMetricValue

Représente la valeur d’instance d’une métrique.

## <a name="syntax"></a>Syntaxe

``` syntax
[Abstract, Version("2.19.0"), UMLPackagePath("CIM::Metrics::BaseMetric"), AMENDMENT]
class CIM_BaseMetricValue : CIM_ManagedElement
{
  string   InstanceID;
  string   MetricDefinitionId;
  string   MeasuredElementName;
  datetime TimeStamp;
  datetime Duration;
  string   MetricValue;
  string   BreakdownDimension;
  string   BreakdownValue;
  boolean  Volatile;
};
```

## <a name="members"></a>Membres

La classe **CIM \_ BaseMetricValue** possède les types de membres suivants :

-   [Propriétés](#properties)

### <a name="properties"></a>Propriétés

La classe **CIM \_ BaseMetricValue** possède les propriétés suivantes.

<dl> <dt>

**BreakdownDimension**
</dt> <dd> <dl> <dt>

Type de données : **chaîne**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Dimension pour laquelle cet ensemble de valeurs de métriques est divisé en fonction de la propriété **BreakdownDimensions** de l’objet [**\_ BaseMetricDefinition CIM**](cim-basemetricdefinition.md) associé.

</dd> <dt>

**BreakdownValue**
</dt> <dd> <dl> <dt>

Type de données : **chaîne**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Valeur de la propriété **BreakdownDimension** définie pour cette valeur d’instance. Par exemple, si **BreakdownDimension** contient « TransactionName », cette propriété peut nommer la transaction réelle à laquelle s’applique cette valeur de mesure particulière.

</dd> <dt>

**Durée**
</dt> <dd> <dl> <dt>

Type de données : **DateTime**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM \_ BaseMetricDefinition**](cim-basemetricdefinition.md).**TimeScope**","**CIM \_ BaseMetricValue**.**TimeStamp**»)
</dt> </dl>

Durée pendant laquelle cette valeur de mesure est valide. Cette propriété ne doit pas exister pour les horodatages qui s’appliquent uniquement à un point dans le temps, mais doivent être définies pour les valeurs considérées comme valides pour une certaine période (par exemple, échantillonnage). Si la propriété **Duration** existe et n’est pas null, la valeur **timestamp** doit être la fin de l’intervalle.

</dd> <dt>

**InstanceID**
</dt> <dd> <dl> <dt>

Type de données : **chaîne**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : [**clé**](/windows/desktop/WmiSdk/key-qualifier), [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("InstanceId")
</dt> </dl>

Identifie de façon unique une instance de cette classe dans la portée de l’espace de noms conteneur.

> [!IMPORTANT]
>
> Pour garantir l’unicité au sein de l’espace de noms, la valeur de la propriété **InstanceID** doit être construite au format suivant : *identifiant OrgID*:*LocalID*
>
> *Identifiant OrgID* doit inclure un nom de droits d’auteur, de marque déposée ou d’autre nom unique qui est détenu par l’entité métier qui définit l' **InstanceID**, ou être un ID inscrit qui est affecté par une autorité globale reconnue. Ce modèle est similaire à la structure des noms de classes de schéma. En outre, pour garantir l’unicité, les premiers deux-points dans **InstanceID** doivent être compris entre *identifiant OrgID* et *LocalID*. Par conséquent, le *identifiant OrgID* ne doit pas contenir de signe deux-points («  : »).
>
> *LocalID* est choisi par l’entité métier et ne doit pas être réutilisé pour identifier des éléments réels sous-jacents différents.
>
> Si le modèle ci-dessus n’est pas utilisé, l’entité de définition doit s’assurer que la valeur **InstanceID** obtenue n’est pas réutilisée dans les propriétés **InstanceID** produites par ce fournisseur ou d’autres fournisseurs pour cet espace de noms.
>
> Pour les instances définies pour Distributed Management Task Force (DMTF), le modèle doit être utilisé avec le *identifiant OrgID* défini sur CIM.

 

</dd> <dt>

**MeasuredElementName**
</dt> <dd> <dl> <dt>

Type de données : **chaîne**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Nom descriptif de l’élément qui est mesuré par la métrique.

Cette propriété est obligatoire si la définition de métrique n’est pas associée à un objet [**CIM \_ propriété ManagedElement**](cim-managedelement.md) et peut être utilisée dans d’autres cas pour fournir des informations supplémentaires. Cela permet de capturer les métriques indépendamment de tout objet **CIM \_ propriété ManagedElement** .

Si plusieurs objets [**CIM \_ propriété ManagedElement**](cim-managedelement.md) sont associés à la valeur de métrique, vous pouvez choisir l’un des éléments gérés pour créer les informations supplémentaires pour la mesure. La propriété n’est pas destinée à être utilisée comme clé étrangère pour interroger l’élément mesuré. Au lieu de cela, vous devez utiliser l’Association à l' **\_ propriété ManagedElement CIM** .

</dd> <dt>

**MetricDefinitionId**
</dt> <dd> <dl> <dt>

Type de données : **chaîne**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : [**obligatoire**](/windows/desktop/WmiSdk/standard-qualifiers), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM \_ BaseMetricDefinition**](cim-basemetricdefinition.md).**ID**»)
</dt> </dl>

Clé de l’instance [**CIM \_ BaseMetricDefinition**](cim-basemetricdefinition.md) associée à cette valeur d’instance.

</dd> <dt>

**MetricValue**
</dt> <dd> <dl> <dt>

Type de données : **chaîne**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : [ **requis**](/windows/desktop/WmiSdk/standard-qualifiers)
</dt> </dl>

Représentation sous forme de chaîne de la valeur de métrique. Le type de données d’origine de la valeur de métrique est spécifié dans l’objet [**CIM \_ BaseMetricDefinition**](cim-basemetricdefinition.md) associé.

</dd> <dt>

**Confirmé**
</dt> <dd> <dl> <dt>

Type de données : **DateTime**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM \_ BaseMetricDefinition**](cim-basemetricdefinition.md).**TimeScope**","**CIM \_ BaseMetricValue**.**Duration**»)
</dt> </dl>

Heure à laquelle la valeur d’une instance de mesure est calculée. Cela diffère de l’heure de création de l’instance. Si la propriété **volatile** a la valeur true, cette valeur change chaque fois qu’un nouvel instantané de mesure est pris.

Une application de gestion peut établir une série chronologique de données de métriques en extrayant les instances de **\_ BaseMetricValue CIM** et en les triant en fonction de leur valeur **timestamp** .

</dd> <dt>

**Volatile**
</dt> <dd> <dl> <dt>

Type de données : **booléen**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

True si la valeur **timestamp** change chaque fois que la valeur de l’instance Metric change. False si cet objet doit rester inchangé et un nouvel objet créé pour la nouvelle valeur d' **horodatage** .

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

[**\_Propriété MANAGEDELEMENT CIM**](cim-managedelement.md)
</dt> </dl>

 

