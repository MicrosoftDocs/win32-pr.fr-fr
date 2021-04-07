---
description: Inscrit les fournisseurs de classe dans WMI.
ms.assetid: 1af7d9ed-c5e4-47e4-839d-53d579ef7cea
ms.tgt_platform: multiple
title: Classe __ClassProviderRegistration
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- __ClassProviderRegistration
- All
- All
- All
- All
- All
- All
- All
- All
- All
- All
- All
- All
- All
- All
- All
- All
- All
api_type:
- Schema
api_location:
- All
ms.openlocfilehash: 32442122624035ec376bed3be8b3ef20c80f8524
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103760461"
---
# <a name="__classproviderregistration-class"></a>\_\_ClassProviderRegistration, classe

La classe système **\_ \_ ClassProviderRegistration** inscrit les fournisseurs de classe dans WMI.

La syntaxe suivante est simplifiée à partir de code au format MOF (Managed Object Format) et inclut toutes les propriétés héritées. Les propriétés sont répertoriées par ordre alphabétique, et non par ordre MOF.

## <a name="syntax"></a>Syntaxe

``` syntax
class __ClassProviderRegistration : __ObjectProviderRegistration
{
  boolean        SupportsBatching;
  datetime       CacheRefreshInterval;
  sint32         InteractionType = 0;
  __Provider REF provider;
  boolean        PerUserSchema;
  string         QuerySupportLevels[];
  string         ReferencedSetQueries[];
  string         ResultSetQueries[];
  boolean        ReSynchroniseOnNamespaceOpen;
  boolean        SuppportsBatching;
  boolean        SupportsEnumeration = False;
  boolean        SupportsDelete = False;
  boolean        SupportsGet = False;
  boolean        SupportsPut = False;
  boolean        SupportsTransactions;
  string         UnsupportedQueries[];
  uint32         Version;
};
```

## <a name="members"></a>Membres

La classe **\_ \_ ClassProviderRegistration** possède les types de membres suivants :

-   [Propriétés](#properties)

### <a name="properties"></a>Propriétés

La classe **\_ \_ ClassProviderRegistration** possède les propriétés suivantes.

<dl> <dt>

**CacheRefreshInterval**
</dt> <dd> <dl> <dt>

Type de données : **DateTime**
</dt> <dt>

Type d’accès : lecture/écriture
</dt> </dl>

Non utilisé.

</dd> <dt>

**InteractionType**
</dt> <dd> <dl> <dt>

Type de données : **sint32**
</dt> <dt>

Type d’accès : lecture/écriture
</dt> </dl>

Indique si la classe ou le fournisseur d’instance fournit des données, ou s’appuie sur WMI et le référentiel Common Information Model (CIM). Les fournisseurs d’extraction prennent en charge l’accès dynamique aux données, et les fournisseurs de notifications push stockent les données dans le référentiel CIM et s’appuient sur WMI pour y accéder. La valeur par défaut est 0 (zéro). Cette propriété est héritée de [**\_ \_ ObjectProviderRegistration**](--objectproviderregistration.md). Pour plus d’informations, consultez Détermination de l' [État d’envoi ou d’extraction](determining-push-or-pull-status.md).

<dt>

<span id="Pull"></span><span id="pull"></span><span id="PULL"></span>

<span id="Pull"></span><span id="pull"></span><span id="PULL"></span>**Pull** (0)


</dt> <dd>

Le fournisseur est un fournisseur d’extraction.

</dd> <dt>

<span id="Push"></span><span id="push"></span><span id="PUSH"></span>

<span id="Push"></span><span id="push"></span><span id="PUSH"></span>**Push** (1)


</dt> <dd>

Le fournisseur est un fournisseur push.

</dd> <dt>

<span id="PushVerify"></span><span id="pushverify"></span><span id="PUSHVERIFY"></span>

<span id="PushVerify"></span><span id="pushverify"></span><span id="PUSHVERIFY"></span>**PushVerify** (2)


</dt> <dd>

Le fournisseur est un fournisseur de vérification de push. Notez que les fournisseurs **PushVerify** ne sont pas pris en charge pour l’instant.

</dd> </dl>

</dd> <dt>

**PerUserSchema**
</dt> <dd> <dl> <dt>

Type de données : **booléen**
</dt> <dt>

Type d’accès : lecture/écriture
</dt> </dl>

Non utilisé.

</dd> <dt>

**moteur**
</dt> <dd> <dl> <dt>

Type de données : **\_ \_ fournisseur**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Chemin d’accès de l’objet à un fournisseur de classe. Cette propriété est héritée de [**\_ \_ ProviderRegistration**](--providerregistration.md).

</dd> <dt>

**QuerySupportLevels**
</dt> <dd> <dl> <dt>

Type de données : tableau de **chaînes**
</dt> <dt>

Type d’accès : lecture/écriture
</dt> </dl>

Tableau des types de prise en charge par le fournisseur du traitement des requêtes. Cette propriété est héritée de [**\_ \_ ObjectProviderRegistration**](--objectproviderregistration.md). Les fournisseurs de classes sont requis pour prendre en charge au moins un type de requête. Les fournisseurs d’instances peuvent affecter à **QuerySupportLevels** la **valeur null** s’ils ne prennent pas en charge le traitement des requêtes. Les fournisseurs qui prennent en charge les requêtes implémentent la méthode [**IWbemServices :: ExecQueryAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-execqueryasync) et définissent cette propriété sur une ou plusieurs des valeurs suivantes :

<dt>



 ("WQL : UnarySelect")


</dt> <dd></dd> <dt>



 ("WQL : References")


</dt> <dd></dd> <dt>



 (« WQL : ASSOCIATORS »)


</dt> <dd></dd> <dt>



 ("WQL : V1ProviderDefined")


</dt> <dd></dd> </dl>

</dd> <dt>

**ReferencedSetQueries**
</dt> <dd> <dl> <dt>

Type de données : tableau de **chaînes**
</dt> <dt>

Type d’accès : lecture/écriture
</dt> </dl>

Une ou plusieurs requêtes qui décrivent l’ensemble des classes référencées prises en charge par un fournisseur de classe. Les fournisseurs qui peuvent fournir des classes d’association doivent inclure au moins une requête dans cette propriété.

</dd> <dt>

**ResultSetQueries**
</dt> <dd> <dl> <dt>

Type de données : tableau de **chaînes**
</dt> <dt>

Type d’accès : lecture/écriture
</dt> </dl>

Une ou plusieurs requêtes qui décrivent l’ensemble de toutes les classes qui peuvent être fournies par le fournisseur de classe, ou un sur-ensemble de ces classes. Cette propriété ne spécifie jamais un sous-ensemble de classes prises en charge.

</dd> <dt>

**ReSynchroniseOnNamespaceOpen**
</dt> <dd> <dl> <dt>

Type de données : **booléen**
</dt> <dt>

Type d’accès : lecture/écriture
</dt> </dl>

Non utilisé.

</dd> <dt>

**SupportsBatching**
</dt> <dd> <dl> <dt>

Type de données : **booléen**
</dt> <dt>

Type d’accès : lecture/écriture
</dt> </dl>

Non utilisé.

Cette propriété est héritée de [**\_ \_ ObjectProviderRegistration**](--objectproviderregistration.md).

</dd> <dt>

**SupportsDelete**
</dt> <dd> <dl> <dt>

Type de données : **booléen**
</dt> <dt>

Type d’accès : lecture/écriture
</dt> </dl>

Si la **valeur est true**, le fournisseur prend en charge la suppression des données. Cette propriété est héritée de [**\_ \_ ObjectProviderRegistration**](--objectproviderregistration.md).

<dt>



 :


</dt> <dd>

Le fournisseur prend en charge la suppression de classe ou d’instance en implémentant l’un des [**Eleteclassasync IWbemServices ::D**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-deleteclassasync) (fournisseurs de classes) ou [**IWbemServices ::D eleteinstanceasync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-deleteinstanceasync) (fournisseurs d’instances).

</dd> <dt>



 Fausses


</dt> <dd>

Le fournisseur ne prend pas en charge la suppression des données et retourne le **\_ fournisseur WBEM E \_ \_ non \_ compatible** à partir de [**DeleteClassAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-deleteclassasync) ou [**DeleteInstanceAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-deleteinstanceasync).

</dd> </dl>

</dd> <dt>

**SupportsEnumeration**
</dt> <dd> <dl> <dt>

Type de données : **booléen**
</dt> <dt>

Type d’accès : lecture/écriture
</dt> </dl>

Si la **valeur est true**, le fournisseur prend en charge l’énumération des données. Cette propriété est héritée de [**\_ \_ ObjectProviderRegistration**](--objectproviderregistration.md).

<dt>



 :


</dt> <dd>

Le fournisseur prend en charge l’énumération des données en implémentant l’une des classes [**IWbemServices :: CreateClassEnumAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-createclassenumasync) (fournisseurs de classes) ou [**IWbemServices :: CreateInstanceEnumAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-createinstanceenumasync) (fournisseurs d’instances).

</dd> <dt>



 Fausses


</dt> <dd>

Le fournisseur ne prend pas en charge l’énumération des données et retourne le **\_ fournisseur WBEM E \_ \_ non \_ compatible** à partir de [**CreateClassEnumAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-createclassenumasync) ou [**CreateInstanceEnumAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-createinstanceenumasync).

</dd> </dl>

</dd> <dt>

**SupportsGet**
</dt> <dd> <dl> <dt>

Type de données : **booléen**
</dt> <dt>

Type d’accès : lecture/écriture
</dt> </dl>

Si la **valeur est true**, la classe ou le fournisseur d’instance prend en charge la récupération des données. Cette propriété est héritée de [**\_ \_ ObjectProviderRegistration**](--objectproviderregistration.md).

<dt>



 :


</dt> <dd>

Le fournisseur prend en charge la récupération de données en implémentant [**IWbemServices :: GetObjectAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-getobjectasync).

</dd> <dt>



 Fausses


</dt> <dd>

Le fournisseur ne prend pas en charge la récupération de données et retourne le **\_ fournisseur WBEM E \_ \_ non \_ compatible** à partir de [**GetObjectAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-getobjectasync).

</dd> </dl>

</dd> <dt>

**SupportsPut**
</dt> <dd> <dl> <dt>

Type de données : **booléen**
</dt> <dt>

Type d’accès : lecture/écriture
</dt> </dl>

Si la **valeur est true**, la classe ou le fournisseur d’instance prend en charge la modification des données. Cette propriété est héritée de [**\_ \_ ObjectProviderRegistration**](--objectproviderregistration.md).

<dt>



 :


</dt> <dd>

Le fournisseur prend en charge la modification de classe ou d’instance en implémentant l’un des [**Utclassasync IWbemServices ::P**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-putclassasync) (fournisseurs de classes) ou [**IWbemServices ::P utinstanceasync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-putinstanceasync) (fournisseurs de classes).

</dd> <dt>



 Fausses


</dt> <dd>

Le fournisseur ne prend pas en charge la modification des données et retourne le **\_ fournisseur WBEM E \_ \_ non \_ compatible** à partir de [**PutClassAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-putclassasync) ou [**PutInstanceAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-putinstanceasync).

</dd> </dl>

</dd> <dt>

**SupportsTransactions**
</dt> <dd> <dl> <dt>

Type de données : **booléen**
</dt> <dt>

Type d’accès : lecture/écriture
</dt> </dl>

Non utilisé.

</dd> <dt>

**SuppportsBatching**
</dt> <dd> <dl> <dt>

Type de données : **booléen**
</dt> <dt>

Type d’accès : lecture/écriture
</dt> </dl>

Non utilisé.

</dd> <dt>

**UnsupportedQueries**
</dt> <dd> <dl> <dt>

Type de données : tableau de **chaînes**
</dt> <dt>

Type d’accès : lecture/écriture
</dt> </dl>

Une ou plusieurs requêtes qui décrivent l’ensemble de classes que le fournisseur de classes ne prend pas en charge. Utilisez cette propriété pour soustraire de l’ensemble de classes impliqué par **ResultSetQueries**.

</dd> <dt>

**Version**
</dt> <dd> <dl> <dt>

Type de données : **UInt32**
</dt> <dt>

Type d’accès : lecture/écriture
</dt> </dl>

Version de ce fournisseur de classe.

</dd> </dl>

## <a name="remarks"></a>Notes

La classe **\_ \_ ClassProviderRegistration** est dérivée de [**\_ \_ ObjectProviderRegistration**](--objectproviderregistration.md), qui est dérivée de [**\_ \_ ProviderRegistration**](--providerregistration.md).

Les propriétés héritées de [**\_ \_ ObjectProviderRegistration**](--objectproviderregistration.md) indiquent si le fournisseur de classe prend en charge la récupération des données, la modification, la suppression, l’énumération et le traitement des requêtes. La propriété **InteractionType** spécifie si le fournisseur de classes est conçu en tant que fournisseur d’extraction ou de transmission push. Pour plus d’informations, consultez Détermination de l' [État d’envoi ou d’extraction](determining-push-or-pull-status.md).

La classe [**\_ \_ ProviderRegistration**](--providerregistration.md) définit la propriété du [**fournisseur**](/windows/desktop/api/Provider/nl-provider-provider) . Seuls les administrateurs peuvent inscrire un fournisseur en créant une instance de [**\_ \_ Win32Provider**](--win32provider.md) et **\_ \_ ClassProviderRegistration**. Seuls les administrateurs peuvent supprimer un fournisseur.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|--------------------------------|
| Client minimal pris en charge<br/> | Windows Vista<br/>       |
| Serveur minimal pris en charge<br/> | Windows Server 2008<br/> |
| Espace de noms<br/>                | Tous les espaces de noms WMI<br/>  |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**\_\_ObjectProviderRegistration**](/windows/desktop/WmiSdk/--objectproviderregistration)
</dt> <dt>

[Classes système WMI](wmi-system-classes.md)
</dt> <dt>

[Inscription d’un fournisseur de classe](registering-a-class-provider.md)
</dt> <dt>

[Inscription d’un fournisseur d’instances](registering-an-instance-provider.md)
</dt> <dt>

[**\_\_Win32Provider**](--win32provider.md)
</dt> </dl>

 

