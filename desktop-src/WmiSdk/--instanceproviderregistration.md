---
description: Inscrit des fournisseurs d’instances dans WMI.
ms.assetid: 6eba9bff-a5b9-4741-94ef-7d65b33d9aff
ms.tgt_platform: multiple
title: Classe __InstanceProviderRegistration
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- __InstanceProviderRegistration
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
ms.openlocfilehash: 45923c0c3ea3bfc28e67634e3b447e46b62765f3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106540880"
---
# <a name="__instanceproviderregistration-class"></a>\_\_InstanceProviderRegistration, classe

La classe système **\_ \_ InstanceProviderRegistration** inscrit des fournisseurs d’instances dans WMI.

La syntaxe suivante est simplifiée à partir de code au format MOF (Managed Object Format) et inclut toutes les propriétés héritées. Les propriétés sont répertoriées par ordre alphabétique, et non par ordre MOF.

## <a name="syntax"></a>Syntaxe

``` syntax
class __InstanceProviderRegistration : __ObjectProviderRegistration
{
  sint32         InteractionType = 0;
  __Provider REF provider;
  string         QuerySupportLevels[];
  boolean        SupportsBatching;
  boolean        SupportsDelete = False;
  boolean        SupportsEnumeration = True;
  boolean        SupportsGet = False;
  boolean        SupportsPut = False;
  boolean        SupportsTransactions;
};
```

## <a name="members"></a>Membres

La classe **\_ \_ InstanceProviderRegistration** possède les types de membres suivants :

-   [Propriétés](#properties)

### <a name="properties"></a>Propriétés

La classe **\_ \_ InstanceProviderRegistration** possède les propriétés suivantes.

<dl> <dt>

**InteractionType**
</dt> <dd> <dl> <dt>

Type de données : **sint32**
</dt> <dt>

Type d’accès : lecture/écriture
</dt> </dl>

Indique qu’un fournisseur de classes ou d’instances fournit des données, ou récupère des données à partir de WMI et du référentiel Common Information Model (CIM). Les fournisseurs d’extraction prennent en charge l’accès dynamique à leurs données ; et les fournisseurs de notifications push stockent leurs données dans le référentiel CIM et utilisent WMI pour y accéder. Pour plus d’informations, consultez Détermination de l' [État d’envoi ou d’extraction](determining-push-or-pull-status.md). La valeur par défaut est 0 (zéro).

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

Le fournisseur est un fournisseur de vérification de push. Notez que les fournisseurs de vérification de Push ne sont pas pris en charge actuellement.

</dd> </dl>

</dd> <dt>

**moteur**
</dt> <dd> <dl> <dt>

Type de données : **\_ \_ fournisseur**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Référence à une instance du [**\_ \_ fournisseur**](--provider.md) qui représente le chemin d’accès de l’objet au fournisseur d’instance. Cette propriété est héritée de [**\_ \_ ProviderRegistration**](--providerregistration.md).

</dd> <dt>

**QuerySupportLevels**
</dt> <dd> <dl> <dt>

Type de données : tableau de **chaînes**
</dt> <dt>

Type d’accès : lecture/écriture
</dt> </dl>

Tableau des types de prise en charge par le fournisseur du traitement des requêtes. Les fournisseurs de classes ne prennent pas en charge tous les types de requêtes. Les fournisseurs d’instances peuvent affecter à **QuerySupportLevels** la **valeur null** s’ils ne prennent pas en charge le traitement des requêtes. Les fournisseurs qui prennent en charge les requêtes implémentent la méthode [**IWbemServices :: ExecQueryAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-execqueryasync) et définissent cette propriété sur une ou plusieurs des valeurs suivantes.

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

**SupportsBatching**
</dt> <dd> <dl> <dt>

Type de données : **booléen**
</dt> <dt>

Type d’accès : lecture/écriture
</dt> </dl>

Non utilisé.

</dd> <dt>

**SupportsDelete**
</dt> <dd> <dl> <dt>

Type de données : **booléen**
</dt> <dt>

Type d’accès : lecture/écriture
</dt> </dl>

Si la **valeur est true**, le fournisseur prend en charge la suppression des données.

<dt>

Vrai
</dt> <dd>

Le fournisseur prend en charge la suppression d’une classe ou d’une instance en implémentant [**IWbemServices ::D eleteclassasync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-deleteclassasync) (fournisseurs de classes) ou [**IWbemServices ::D eleteinstanceasync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-deleteinstanceasync) (fournisseurs d’instances).

</dd> <dt>

Faux
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

Si la **valeur est true**, le fournisseur prend en charge l’énumération des données.

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

Si la **valeur est true**, la classe ou le fournisseur d’instance prend en charge la récupération des données.

<dt>

Vrai
</dt> <dd>

Le fournisseur prend en charge la récupération de données en implémentant [**IWbemServices :: GetObjectAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-getobjectasync).

</dd> <dt>

Faux
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

Si la **valeur est true**, la classe ou le fournisseur d’instance prend en charge la modification des données.

<dt>



 :


</dt> <dd>

Le fournisseur prend en charge la modification de classe ou d’instance en implémentant l’une des méthodes suivantes : [**IWbemServices ::P utclassasync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-putclassasync) (fournisseurs de classes) ou [**IWbemServices ::P utinstanceasync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-putinstanceasync) (fournisseurs de classes).

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

</dd> </dl>

## <a name="remarks"></a>Notes

La classe **\_ \_ InstanceProviderRegistration** est dérivée de [**\_ \_ ObjectProviderRegistration**](--objectproviderregistration.md), qui est dérivée de [**\_ \_ ProviderRegistration**](--providerregistration.md). Seuls les administrateurs peuvent inscrire un fournisseur d’instances en créant une instance de [**\_ \_ Win32Provider**](--win32provider.md) et **\_ \_ InstanceProviderRegistration**. Seuls les administrateurs peuvent supprimer un fournisseur.

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
</dt> </dl>

 

