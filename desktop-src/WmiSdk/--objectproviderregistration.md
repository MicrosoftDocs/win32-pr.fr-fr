---
description: Sert de classe parente pour les classes utilisées pour inscrire des fournisseurs de classes et d’instances dans WMI.
ms.assetid: f7c569be-8927-42a4-b96a-abe4b7e3e23c
ms.tgt_platform: multiple
title: Classe __ObjectProviderRegistration
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- __ObjectProviderRegistration
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
ms.openlocfilehash: 88b611e4e1a58fb045f13b75a10c84199c936da68bb3c9bbc8f1c556f8b9937d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117926167"
---
# <a name="__objectproviderregistration-class"></a>\_\_ObjectProviderRegistration, classe

La classe système abstraite **\_ \_ ObjectProviderRegistration** sert de classe parente pour les classes utilisées pour inscrire des fournisseurs de classes et d’instances dans WMI.

La syntaxe suivante est simplifiée à partir de code au format MOF (Managed Object Format) et inclut toutes les propriétés héritées. Les propriétés sont répertoriées par ordre alphabétique, et non par ordre MOF.

## <a name="syntax"></a>Syntaxe

``` syntax
[abstract]
class __ObjectProviderRegistration : __ProviderRegistration
{
  sint32         InteractionType = 0;
  __Provider REF provider;
  string         QuerySupportLevels[];
  boolean        SupportsBatching;
  boolean        SupportsDelete = False;
  boolean        SupportsEnumeration = False;
  boolean        SupportsGet = False;
  boolean        SupportsPut = False;
  boolean        SupportsTransactions;
};
```

## <a name="members"></a>Membres

La classe **\_ \_ ObjectProviderRegistration** possède les types de membres suivants :

-   [Propriétés](#properties)

### <a name="properties"></a>Propriétés

La classe **\_ \_ ObjectProviderRegistration** possède les propriétés suivantes.

<dl> <dt>

**InteractionType**
</dt> <dd> <dl> <dt>

Type de données : **sint32**
</dt> <dt>

Type d’accès : lecture/écriture
</dt> </dl>

Indique si le fournisseur de classes ou d’instances fournit ses propres données, ou s’appuie sur WMI et le référentiel Common Information Model (CIM). Les fournisseurs d’extraction prennent en charge l’accès dynamique à leurs données, et les fournisseurs de notifications push stockent leurs données dans le référentiel CIM et s’appuient sur WMI pour y accéder. Pour plus d’informations, consultez Détermination de l' [État d’envoi ou d’extraction](determining-push-or-pull-status.md). La valeur par défaut est 0 (zéro).

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

Le fournisseur est un fournisseur de vérification de push. Notez que Push-Verify n’est pas pris en charge pour l’instant.

</dd> </dl>

</dd> <dt>

**moteur**
</dt> <dd> <dl> <dt>

Type de données : **\_ \_ fournisseur**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Référence à une instance de [**\_ \_ fournisseur**](--provider.md) qui représente un chemin d’accès d’objet au fournisseur d’objets. Cette propriété est héritée de [**\_ \_ ProviderRegistration**](--providerregistration.md).

</dd> <dt>

**QuerySupportLevels**
</dt> <dd> <dl> <dt>

Type de données : tableau de **chaînes**
</dt> <dt>

Type d’accès : lecture/écriture
</dt> </dl>

Tableau des types de prise en charge par le fournisseur du traitement des requêtes. Les fournisseurs de classes ne prennent en charge aucun type de requête. Les fournisseurs d’instances peuvent affecter à **QuerySupportLevels** la **valeur null** s’ils ne prennent pas en charge le traitement des requêtes. Les fournisseurs qui prennent en charge les requêtes implémentent la méthode [**IWbemServices :: ExecQueryAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-execqueryasync) et définissent cette propriété sur une ou plusieurs des valeurs suivantes (le type de propriété est un tableau).

« WQL : UnarySelect »

« WQL : References »

« WQL : ASSOCIATORS »

« WQL : V1ProviderDefined »

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

True
</dt> <dd>

Le fournisseur prend en charge la suppression de classe ou d’instance en implémentant l’un des [**Eleteclassasync IWbemServices ::D**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-deleteclassasync) (fournisseurs de classes) ou [**IWbemServices ::D eleteinstanceasync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-deleteinstanceasync) (fournisseurs d’instances).

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

True
</dt> <dd>

Le fournisseur prend en charge l’énumération des données en implémentant l’une des classes [**IWbemServices :: CreateClassEnumAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-createclassenumasync) (fournisseurs de classes) ou [**IWbemServices :: CreateInstanceEnumAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-createinstanceenumasync) (fournisseurs d’instances).

</dd> <dt>

Faux
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

True
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

Vrai
</dt> <dd>

Le fournisseur prend en charge la modification de classe ou d’instance en implémentant l’un des [**Utclassasync IWbemServices ::P**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-putclassasync) (fournisseurs de classes) ou [**IWbemServices ::P utinstanceasync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-putinstanceasync) (fournisseurs de classes).

</dd> <dt>

Faux
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

## <a name="remarks"></a>Remarques

La classe **\_ \_ ObjectProviderRegistration** est dérivée de [**\_ \_ ProviderRegistration**](--providerregistration.md).

Les fournisseurs de classes doivent définir la propriété **SupportsEnumeration** sur **true** , car les fournisseurs doivent être en mesure de fournir WMI avec une liste de leurs classes. Si un fournisseur de classe tente d’affecter la valeur **false** à cette propriété, WMI signale l’inscription comme non conforme. Les fournisseurs d’instances ne sont pas requis pour prendre en charge l’énumération et peuvent choisir de définir **SupportsEnumeration** sur **true** ou **false**.

Un fournisseur qui définit **QuerySupportLevels** sur « WQL : UnarySelect » peut accepter une requête qui se compose de l’instruction SELECT de base telle qu’elle est prise en charge dans la version 1,0 de WMI. Les fournisseurs de classes et d’instances sont censés être en mesure de gérer la propriété système de **\_ \_ classe** . Les fournisseurs de classes sont également censés traiter la propriété système de la **\_ \_ superclasse** et l’opérateur ISA. L’opérateur ISA est utilisé pour étendre un jeu de résultats aux classes dérivées. Si un fournisseur reçoit une requête qu’il ne peut pas interpréter, il demande que WMI le gère en retournant la valeur d’erreur **WBEM \_ E \_ trop \_ complexe** . Pour obtenir une description de la syntaxe WQL valide, consultez [interrogation avec WQL](querying-with-wql.md).

un fournisseur qui affecte à **QuerySupportLevels** la valeur **WQL : V1ProviderDefined** peut essayer de prendre en charge un plus grand ensemble de la syntaxe SQL à son propre risque, par exemple la `ORDER BY` clause. WMI n’interprète pas les clauses supplémentaires ou ne tente pas de s’assurer que le jeu de résultats est correct.

Seuls les administrateurs peuvent inscrire ou supprimer un fournisseur en créant une instance de [**\_ \_ Win32Provider**](--win32provider.md) et en l’inscrivant.

## <a name="requirements"></a>Conditions requises



| Condition requise | Valeur |
|-------------------------------------|--------------------------------|
| Client minimal pris en charge<br/> | Windows Vista<br/>       |
| Serveur minimal pris en charge<br/> | Windows Server 2008<br/> |
| Espace de noms<br/>                | Tous les espaces de noms WMI<br/>  |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**\_\_ProviderRegistration**](/windows/desktop/WmiSdk/--providerregistration)
</dt> <dt>

[Classes système WMI](wmi-system-classes.md)
</dt> <dt>

[Inscription d’un fournisseur](registering-a-provider.md)
</dt> </dl>

 

