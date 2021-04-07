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
# <a name="__classproviderregistration-class"></a><span data-ttu-id="4867a-103">\_\_ClassProviderRegistration, classe</span><span class="sxs-lookup"><span data-stu-id="4867a-103">\_\_ClassProviderRegistration class</span></span>

<span data-ttu-id="4867a-104">La classe système **\_ \_ ClassProviderRegistration** inscrit les fournisseurs de classe dans WMI.</span><span class="sxs-lookup"><span data-stu-id="4867a-104">The **\_\_ClassProviderRegistration** system class registers class providers in WMI.</span></span>

<span data-ttu-id="4867a-105">La syntaxe suivante est simplifiée à partir de code au format MOF (Managed Object Format) et inclut toutes les propriétés héritées.</span><span class="sxs-lookup"><span data-stu-id="4867a-105">The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.</span></span> <span data-ttu-id="4867a-106">Les propriétés sont répertoriées par ordre alphabétique, et non par ordre MOF.</span><span class="sxs-lookup"><span data-stu-id="4867a-106">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="4867a-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="4867a-107">Syntax</span></span>

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

## <a name="members"></a><span data-ttu-id="4867a-108">Membres</span><span class="sxs-lookup"><span data-stu-id="4867a-108">Members</span></span>

<span data-ttu-id="4867a-109">La classe **\_ \_ ClassProviderRegistration** possède les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="4867a-109">The **\_\_ClassProviderRegistration** class has these types of members:</span></span>

-   [<span data-ttu-id="4867a-110">Propriétés</span><span class="sxs-lookup"><span data-stu-id="4867a-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="4867a-111">Propriétés</span><span class="sxs-lookup"><span data-stu-id="4867a-111">Properties</span></span>

<span data-ttu-id="4867a-112">La classe **\_ \_ ClassProviderRegistration** possède les propriétés suivantes.</span><span class="sxs-lookup"><span data-stu-id="4867a-112">The **\_\_ClassProviderRegistration** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="4867a-113">**CacheRefreshInterval**</span><span class="sxs-lookup"><span data-stu-id="4867a-113">**CacheRefreshInterval**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4867a-114">Type de données : **DateTime**</span><span class="sxs-lookup"><span data-stu-id="4867a-114">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="4867a-115">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="4867a-115">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="4867a-116">Non utilisé.</span><span class="sxs-lookup"><span data-stu-id="4867a-116">Not used.</span></span>

</dd> <dt>

<span data-ttu-id="4867a-117">**InteractionType**</span><span class="sxs-lookup"><span data-stu-id="4867a-117">**InteractionType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4867a-118">Type de données : **sint32**</span><span class="sxs-lookup"><span data-stu-id="4867a-118">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="4867a-119">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="4867a-119">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="4867a-120">Indique si la classe ou le fournisseur d’instance fournit des données, ou s’appuie sur WMI et le référentiel Common Information Model (CIM).</span><span class="sxs-lookup"><span data-stu-id="4867a-120">Indicates whether or not the class or instance provider supplies data, or relies on WMI and the Common Information Model (CIM) repository.</span></span> <span data-ttu-id="4867a-121">Les fournisseurs d’extraction prennent en charge l’accès dynamique aux données, et les fournisseurs de notifications push stockent les données dans le référentiel CIM et s’appuient sur WMI pour y accéder.</span><span class="sxs-lookup"><span data-stu-id="4867a-121">Pull providers support dynamic access to data, and push providers store data in the CIM repository, and rely on WMI to provide access to it.</span></span> <span data-ttu-id="4867a-122">La valeur par défaut est 0 (zéro).</span><span class="sxs-lookup"><span data-stu-id="4867a-122">The default value is 0 (zero).</span></span> <span data-ttu-id="4867a-123">Cette propriété est héritée de [**\_ \_ ObjectProviderRegistration**](--objectproviderregistration.md).</span><span class="sxs-lookup"><span data-stu-id="4867a-123">This property is inherited from [**\_\_ObjectProviderRegistration**](--objectproviderregistration.md).</span></span> <span data-ttu-id="4867a-124">Pour plus d’informations, consultez Détermination de l' [État d’envoi ou d’extraction](determining-push-or-pull-status.md).</span><span class="sxs-lookup"><span data-stu-id="4867a-124">For more information, see [Determining Push or Pull Status](determining-push-or-pull-status.md).</span></span>

<dt>

<span id="Pull"></span><span id="pull"></span><span id="PULL"></span>

<span data-ttu-id="4867a-125"><span id="Pull"></span><span id="pull"></span><span id="PULL"></span>**Pull** (0)</span><span class="sxs-lookup"><span data-stu-id="4867a-125"><span id="Pull"></span><span id="pull"></span><span id="PULL"></span>**Pull** (0)</span></span>


</dt> <dd>

<span data-ttu-id="4867a-126">Le fournisseur est un fournisseur d’extraction.</span><span class="sxs-lookup"><span data-stu-id="4867a-126">Provider is a pull provider.</span></span>

</dd> <dt>

<span id="Push"></span><span id="push"></span><span id="PUSH"></span>

<span data-ttu-id="4867a-127"><span id="Push"></span><span id="push"></span><span id="PUSH"></span>**Push** (1)</span><span class="sxs-lookup"><span data-stu-id="4867a-127"><span id="Push"></span><span id="push"></span><span id="PUSH"></span>**Push** (1)</span></span>


</dt> <dd>

<span data-ttu-id="4867a-128">Le fournisseur est un fournisseur push.</span><span class="sxs-lookup"><span data-stu-id="4867a-128">Provider is a push provider.</span></span>

</dd> <dt>

<span id="PushVerify"></span><span id="pushverify"></span><span id="PUSHVERIFY"></span>

<span data-ttu-id="4867a-129"><span id="PushVerify"></span><span id="pushverify"></span><span id="PUSHVERIFY"></span>**PushVerify** (2)</span><span class="sxs-lookup"><span data-stu-id="4867a-129"><span id="PushVerify"></span><span id="pushverify"></span><span id="PUSHVERIFY"></span>**PushVerify** (2)</span></span>


</dt> <dd>

<span data-ttu-id="4867a-130">Le fournisseur est un fournisseur de vérification de push.</span><span class="sxs-lookup"><span data-stu-id="4867a-130">Provider is a push-verify provider.</span></span> <span data-ttu-id="4867a-131">Notez que les fournisseurs **PushVerify** ne sont pas pris en charge pour l’instant.</span><span class="sxs-lookup"><span data-stu-id="4867a-131">Note that **PushVerify** providers are not supported at this time.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="4867a-132">**PerUserSchema**</span><span class="sxs-lookup"><span data-stu-id="4867a-132">**PerUserSchema**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4867a-133">Type de données : **booléen**</span><span class="sxs-lookup"><span data-stu-id="4867a-133">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="4867a-134">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="4867a-134">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="4867a-135">Non utilisé.</span><span class="sxs-lookup"><span data-stu-id="4867a-135">Not used.</span></span>

</dd> <dt>

<span data-ttu-id="4867a-136">**moteur**</span><span class="sxs-lookup"><span data-stu-id="4867a-136">**provider**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4867a-137">Type de données : **\_ \_ fournisseur**</span><span class="sxs-lookup"><span data-stu-id="4867a-137">Data type: **\_\_Provider**</span></span>
</dt> <dt>

<span data-ttu-id="4867a-138">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="4867a-138">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="4867a-139">Chemin d’accès de l’objet à un fournisseur de classe.</span><span class="sxs-lookup"><span data-stu-id="4867a-139">Object path to a class provider.</span></span> <span data-ttu-id="4867a-140">Cette propriété est héritée de [**\_ \_ ProviderRegistration**](--providerregistration.md).</span><span class="sxs-lookup"><span data-stu-id="4867a-140">This property is inherited from [**\_\_ProviderRegistration**](--providerregistration.md).</span></span>

</dd> <dt>

<span data-ttu-id="4867a-141">**QuerySupportLevels**</span><span class="sxs-lookup"><span data-stu-id="4867a-141">**QuerySupportLevels**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4867a-142">Type de données : tableau de **chaînes**</span><span class="sxs-lookup"><span data-stu-id="4867a-142">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="4867a-143">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="4867a-143">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="4867a-144">Tableau des types de prise en charge par le fournisseur du traitement des requêtes.</span><span class="sxs-lookup"><span data-stu-id="4867a-144">Array of the types of provider-included support for query processing.</span></span> <span data-ttu-id="4867a-145">Cette propriété est héritée de [**\_ \_ ObjectProviderRegistration**](--objectproviderregistration.md).</span><span class="sxs-lookup"><span data-stu-id="4867a-145">This property is inherited from [**\_\_ObjectProviderRegistration**](--objectproviderregistration.md).</span></span> <span data-ttu-id="4867a-146">Les fournisseurs de classes sont requis pour prendre en charge au moins un type de requête.</span><span class="sxs-lookup"><span data-stu-id="4867a-146">Class providers are required to support at least one type of query.</span></span> <span data-ttu-id="4867a-147">Les fournisseurs d’instances peuvent affecter à **QuerySupportLevels** la **valeur null** s’ils ne prennent pas en charge le traitement des requêtes.</span><span class="sxs-lookup"><span data-stu-id="4867a-147">Instance providers can set **QuerySupportLevels** to **NULL** if they do not support query processing.</span></span> <span data-ttu-id="4867a-148">Les fournisseurs qui prennent en charge les requêtes implémentent la méthode [**IWbemServices :: ExecQueryAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-execqueryasync) et définissent cette propriété sur une ou plusieurs des valeurs suivantes :</span><span class="sxs-lookup"><span data-stu-id="4867a-148">Providers that support queries implement the [**IWbemServices::ExecQueryAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-execqueryasync) method, and set this property to one or more of the following values:</span></span>

<dt>



 <span data-ttu-id="4867a-149">("WQL : UnarySelect")</span><span class="sxs-lookup"><span data-stu-id="4867a-149">("WQL:UnarySelect")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="4867a-150">("WQL : References")</span><span class="sxs-lookup"><span data-stu-id="4867a-150">("WQL:References")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="4867a-151">(« WQL : ASSOCIATORS »)</span><span class="sxs-lookup"><span data-stu-id="4867a-151">("WQL:Associators")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="4867a-152">("WQL : V1ProviderDefined")</span><span class="sxs-lookup"><span data-stu-id="4867a-152">("WQL:V1ProviderDefined")</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="4867a-153">**ReferencedSetQueries**</span><span class="sxs-lookup"><span data-stu-id="4867a-153">**ReferencedSetQueries**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4867a-154">Type de données : tableau de **chaînes**</span><span class="sxs-lookup"><span data-stu-id="4867a-154">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="4867a-155">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="4867a-155">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="4867a-156">Une ou plusieurs requêtes qui décrivent l’ensemble des classes référencées prises en charge par un fournisseur de classe.</span><span class="sxs-lookup"><span data-stu-id="4867a-156">One or more queries that describe the set of referenced classes that a class provider supports.</span></span> <span data-ttu-id="4867a-157">Les fournisseurs qui peuvent fournir des classes d’association doivent inclure au moins une requête dans cette propriété.</span><span class="sxs-lookup"><span data-stu-id="4867a-157">Providers that can supply association classes must include at least one query in this property.</span></span>

</dd> <dt>

<span data-ttu-id="4867a-158">**ResultSetQueries**</span><span class="sxs-lookup"><span data-stu-id="4867a-158">**ResultSetQueries**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4867a-159">Type de données : tableau de **chaînes**</span><span class="sxs-lookup"><span data-stu-id="4867a-159">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="4867a-160">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="4867a-160">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="4867a-161">Une ou plusieurs requêtes qui décrivent l’ensemble de toutes les classes qui peuvent être fournies par le fournisseur de classe, ou un sur-ensemble de ces classes.</span><span class="sxs-lookup"><span data-stu-id="4867a-161">One or more queries that describe the set of all classes that can be supplied by the class provider, or a superset of those classes.</span></span> <span data-ttu-id="4867a-162">Cette propriété ne spécifie jamais un sous-ensemble de classes prises en charge.</span><span class="sxs-lookup"><span data-stu-id="4867a-162">This property never specifies a subset of supported classes.</span></span>

</dd> <dt>

<span data-ttu-id="4867a-163">**ReSynchroniseOnNamespaceOpen**</span><span class="sxs-lookup"><span data-stu-id="4867a-163">**ReSynchroniseOnNamespaceOpen**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4867a-164">Type de données : **booléen**</span><span class="sxs-lookup"><span data-stu-id="4867a-164">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="4867a-165">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="4867a-165">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="4867a-166">Non utilisé.</span><span class="sxs-lookup"><span data-stu-id="4867a-166">Not used.</span></span>

</dd> <dt>

<span data-ttu-id="4867a-167">**SupportsBatching**</span><span class="sxs-lookup"><span data-stu-id="4867a-167">**SupportsBatching**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4867a-168">Type de données : **booléen**</span><span class="sxs-lookup"><span data-stu-id="4867a-168">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="4867a-169">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="4867a-169">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="4867a-170">Non utilisé.</span><span class="sxs-lookup"><span data-stu-id="4867a-170">Not used.</span></span>

<span data-ttu-id="4867a-171">Cette propriété est héritée de [**\_ \_ ObjectProviderRegistration**](--objectproviderregistration.md).</span><span class="sxs-lookup"><span data-stu-id="4867a-171">This property is inherited from [**\_\_ObjectProviderRegistration**](--objectproviderregistration.md).</span></span>

</dd> <dt>

<span data-ttu-id="4867a-172">**SupportsDelete**</span><span class="sxs-lookup"><span data-stu-id="4867a-172">**SupportsDelete**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4867a-173">Type de données : **booléen**</span><span class="sxs-lookup"><span data-stu-id="4867a-173">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="4867a-174">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="4867a-174">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="4867a-175">Si la **valeur est true**, le fournisseur prend en charge la suppression des données.</span><span class="sxs-lookup"><span data-stu-id="4867a-175">If **TRUE**, the provider supports data deletion.</span></span> <span data-ttu-id="4867a-176">Cette propriété est héritée de [**\_ \_ ObjectProviderRegistration**](--objectproviderregistration.md).</span><span class="sxs-lookup"><span data-stu-id="4867a-176">This property is inherited from [**\_\_ObjectProviderRegistration**](--objectproviderregistration.md).</span></span>

<dt>



 <span data-ttu-id="4867a-177">:</span><span class="sxs-lookup"><span data-stu-id="4867a-177">(True)</span></span>


</dt> <dd>

<span data-ttu-id="4867a-178">Le fournisseur prend en charge la suppression de classe ou d’instance en implémentant l’un des [**Eleteclassasync IWbemServices ::D**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-deleteclassasync) (fournisseurs de classes) ou [**IWbemServices ::D eleteinstanceasync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-deleteinstanceasync) (fournisseurs d’instances).</span><span class="sxs-lookup"><span data-stu-id="4867a-178">The provider supports class or instance deletion by implementing one of either [**IWbemServices::DeleteClassAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-deleteclassasync) (class providers), or [**IWbemServices::DeleteInstanceAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-deleteinstanceasync) (instance providers).</span></span>

</dd> <dt>



 <span data-ttu-id="4867a-179">Fausses</span><span class="sxs-lookup"><span data-stu-id="4867a-179">(False)</span></span>


</dt> <dd>

<span data-ttu-id="4867a-180">Le fournisseur ne prend pas en charge la suppression des données et retourne le **\_ fournisseur WBEM E \_ \_ non \_ compatible** à partir de [**DeleteClassAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-deleteclassasync) ou [**DeleteInstanceAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-deleteinstanceasync).</span><span class="sxs-lookup"><span data-stu-id="4867a-180">The provider does not support data deletion, and returns **WBEM\_E\_PROVIDER\_NOT\_CAPABLE** from [**DeleteClassAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-deleteclassasync) or [**DeleteInstanceAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-deleteinstanceasync).</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="4867a-181">**SupportsEnumeration**</span><span class="sxs-lookup"><span data-stu-id="4867a-181">**SupportsEnumeration**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4867a-182">Type de données : **booléen**</span><span class="sxs-lookup"><span data-stu-id="4867a-182">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="4867a-183">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="4867a-183">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="4867a-184">Si la **valeur est true**, le fournisseur prend en charge l’énumération des données.</span><span class="sxs-lookup"><span data-stu-id="4867a-184">If **TRUE**, the provider supports data enumeration.</span></span> <span data-ttu-id="4867a-185">Cette propriété est héritée de [**\_ \_ ObjectProviderRegistration**](--objectproviderregistration.md).</span><span class="sxs-lookup"><span data-stu-id="4867a-185">This property is inherited from [**\_\_ObjectProviderRegistration**](--objectproviderregistration.md).</span></span>

<dt>



 <span data-ttu-id="4867a-186">:</span><span class="sxs-lookup"><span data-stu-id="4867a-186">(True)</span></span>


</dt> <dd>

<span data-ttu-id="4867a-187">Le fournisseur prend en charge l’énumération des données en implémentant l’une des classes [**IWbemServices :: CreateClassEnumAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-createclassenumasync) (fournisseurs de classes) ou [**IWbemServices :: CreateInstanceEnumAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-createinstanceenumasync) (fournisseurs d’instances).</span><span class="sxs-lookup"><span data-stu-id="4867a-187">The provider supports data enumeration by implementing one of either [**IWbemServices::CreateClassEnumAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-createclassenumasync) (class providers), or [**IWbemServices::CreateInstanceEnumAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-createinstanceenumasync) (instance providers).</span></span>

</dd> <dt>



 <span data-ttu-id="4867a-188">Fausses</span><span class="sxs-lookup"><span data-stu-id="4867a-188">(False)</span></span>


</dt> <dd>

<span data-ttu-id="4867a-189">Le fournisseur ne prend pas en charge l’énumération des données et retourne le **\_ fournisseur WBEM E \_ \_ non \_ compatible** à partir de [**CreateClassEnumAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-createclassenumasync) ou [**CreateInstanceEnumAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-createinstanceenumasync).</span><span class="sxs-lookup"><span data-stu-id="4867a-189">The provider does not support data enumeration, and returns **WBEM\_E\_PROVIDER\_NOT\_CAPABLE** from [**CreateClassEnumAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-createclassenumasync) or [**CreateInstanceEnumAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-createinstanceenumasync).</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="4867a-190">**SupportsGet**</span><span class="sxs-lookup"><span data-stu-id="4867a-190">**SupportsGet**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4867a-191">Type de données : **booléen**</span><span class="sxs-lookup"><span data-stu-id="4867a-191">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="4867a-192">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="4867a-192">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="4867a-193">Si la **valeur est true**, la classe ou le fournisseur d’instance prend en charge la récupération des données.</span><span class="sxs-lookup"><span data-stu-id="4867a-193">If **TRUE**, the class or instance provider supports data retrieval.</span></span> <span data-ttu-id="4867a-194">Cette propriété est héritée de [**\_ \_ ObjectProviderRegistration**](--objectproviderregistration.md).</span><span class="sxs-lookup"><span data-stu-id="4867a-194">This property is inherited from [**\_\_ObjectProviderRegistration**](--objectproviderregistration.md).</span></span>

<dt>



 <span data-ttu-id="4867a-195">:</span><span class="sxs-lookup"><span data-stu-id="4867a-195">(True)</span></span>


</dt> <dd>

<span data-ttu-id="4867a-196">Le fournisseur prend en charge la récupération de données en implémentant [**IWbemServices :: GetObjectAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-getobjectasync).</span><span class="sxs-lookup"><span data-stu-id="4867a-196">The provider supports data retrieval by implementing [**IWbemServices::GetObjectAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-getobjectasync).</span></span>

</dd> <dt>



 <span data-ttu-id="4867a-197">Fausses</span><span class="sxs-lookup"><span data-stu-id="4867a-197">(False)</span></span>


</dt> <dd>

<span data-ttu-id="4867a-198">Le fournisseur ne prend pas en charge la récupération de données et retourne le **\_ fournisseur WBEM E \_ \_ non \_ compatible** à partir de [**GetObjectAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-getobjectasync).</span><span class="sxs-lookup"><span data-stu-id="4867a-198">The provider does not support data retrieval, and returns **WBEM\_E\_PROVIDER\_NOT\_CAPABLE** from [**GetObjectAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-getobjectasync).</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="4867a-199">**SupportsPut**</span><span class="sxs-lookup"><span data-stu-id="4867a-199">**SupportsPut**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4867a-200">Type de données : **booléen**</span><span class="sxs-lookup"><span data-stu-id="4867a-200">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="4867a-201">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="4867a-201">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="4867a-202">Si la **valeur est true**, la classe ou le fournisseur d’instance prend en charge la modification des données.</span><span class="sxs-lookup"><span data-stu-id="4867a-202">If **TRUE**, the class or instance provider supports data modification.</span></span> <span data-ttu-id="4867a-203">Cette propriété est héritée de [**\_ \_ ObjectProviderRegistration**](--objectproviderregistration.md).</span><span class="sxs-lookup"><span data-stu-id="4867a-203">This property is inherited from [**\_\_ObjectProviderRegistration**](--objectproviderregistration.md).</span></span>

<dt>



 <span data-ttu-id="4867a-204">:</span><span class="sxs-lookup"><span data-stu-id="4867a-204">(True)</span></span>


</dt> <dd>

<span data-ttu-id="4867a-205">Le fournisseur prend en charge la modification de classe ou d’instance en implémentant l’un des [**Utclassasync IWbemServices ::P**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-putclassasync) (fournisseurs de classes) ou [**IWbemServices ::P utinstanceasync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-putinstanceasync) (fournisseurs de classes).</span><span class="sxs-lookup"><span data-stu-id="4867a-205">The provider supports class or instance modification by implementing one of either [**IWbemServices::PutClassAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-putclassasync) (class providers), or [**IWbemServices::PutInstanceAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-putinstanceasync) (class providers).</span></span>

</dd> <dt>



 <span data-ttu-id="4867a-206">Fausses</span><span class="sxs-lookup"><span data-stu-id="4867a-206">(False)</span></span>


</dt> <dd>

<span data-ttu-id="4867a-207">Le fournisseur ne prend pas en charge la modification des données et retourne le **\_ fournisseur WBEM E \_ \_ non \_ compatible** à partir de [**PutClassAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-putclassasync) ou [**PutInstanceAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-putinstanceasync).</span><span class="sxs-lookup"><span data-stu-id="4867a-207">The provider does not support data modification and returns **WBEM\_E\_PROVIDER\_NOT\_CAPABLE** from [**PutClassAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-putclassasync) or [**PutInstanceAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-putinstanceasync).</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="4867a-208">**SupportsTransactions**</span><span class="sxs-lookup"><span data-stu-id="4867a-208">**SupportsTransactions**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4867a-209">Type de données : **booléen**</span><span class="sxs-lookup"><span data-stu-id="4867a-209">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="4867a-210">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="4867a-210">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="4867a-211">Non utilisé.</span><span class="sxs-lookup"><span data-stu-id="4867a-211">Not used.</span></span>

</dd> <dt>

<span data-ttu-id="4867a-212">**SuppportsBatching**</span><span class="sxs-lookup"><span data-stu-id="4867a-212">**SuppportsBatching**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4867a-213">Type de données : **booléen**</span><span class="sxs-lookup"><span data-stu-id="4867a-213">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="4867a-214">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="4867a-214">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="4867a-215">Non utilisé.</span><span class="sxs-lookup"><span data-stu-id="4867a-215">Not used.</span></span>

</dd> <dt>

<span data-ttu-id="4867a-216">**UnsupportedQueries**</span><span class="sxs-lookup"><span data-stu-id="4867a-216">**UnsupportedQueries**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4867a-217">Type de données : tableau de **chaînes**</span><span class="sxs-lookup"><span data-stu-id="4867a-217">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="4867a-218">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="4867a-218">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="4867a-219">Une ou plusieurs requêtes qui décrivent l’ensemble de classes que le fournisseur de classes ne prend pas en charge.</span><span class="sxs-lookup"><span data-stu-id="4867a-219">One or more queries that describe the set of classes that the class provider does not support.</span></span> <span data-ttu-id="4867a-220">Utilisez cette propriété pour soustraire de l’ensemble de classes impliqué par **ResultSetQueries**.</span><span class="sxs-lookup"><span data-stu-id="4867a-220">Use this property to subtract from the set of classes implied by **ResultSetQueries**.</span></span>

</dd> <dt>

<span data-ttu-id="4867a-221">**Version**</span><span class="sxs-lookup"><span data-stu-id="4867a-221">**Version**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4867a-222">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="4867a-222">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="4867a-223">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="4867a-223">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="4867a-224">Version de ce fournisseur de classe.</span><span class="sxs-lookup"><span data-stu-id="4867a-224">Version of this class provider.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="4867a-225">Notes</span><span class="sxs-lookup"><span data-stu-id="4867a-225">Remarks</span></span>

<span data-ttu-id="4867a-226">La classe **\_ \_ ClassProviderRegistration** est dérivée de [**\_ \_ ObjectProviderRegistration**](--objectproviderregistration.md), qui est dérivée de [**\_ \_ ProviderRegistration**](--providerregistration.md).</span><span class="sxs-lookup"><span data-stu-id="4867a-226">The **\_\_ClassProviderRegistration** class is derived from [**\_\_ObjectProviderRegistration**](--objectproviderregistration.md), which is derived from [**\_\_ProviderRegistration**](--providerregistration.md).</span></span>

<span data-ttu-id="4867a-227">Les propriétés héritées de [**\_ \_ ObjectProviderRegistration**](--objectproviderregistration.md) indiquent si le fournisseur de classe prend en charge la récupération des données, la modification, la suppression, l’énumération et le traitement des requêtes.</span><span class="sxs-lookup"><span data-stu-id="4867a-227">The properties inherited from [**\_\_ObjectProviderRegistration**](--objectproviderregistration.md) indicate whether or not the class provider supports data retrieval, modification, deletion, enumeration and query processing.</span></span> <span data-ttu-id="4867a-228">La propriété **InteractionType** spécifie si le fournisseur de classes est conçu en tant que fournisseur d’extraction ou de transmission push.</span><span class="sxs-lookup"><span data-stu-id="4867a-228">The **InteractionType** property specifies whether or not the class provider is designed as a pull or push provider.</span></span> <span data-ttu-id="4867a-229">Pour plus d’informations, consultez Détermination de l' [État d’envoi ou d’extraction](determining-push-or-pull-status.md).</span><span class="sxs-lookup"><span data-stu-id="4867a-229">For more information, see [Determining Push or Pull Status](determining-push-or-pull-status.md).</span></span>

<span data-ttu-id="4867a-230">La classe [**\_ \_ ProviderRegistration**](--providerregistration.md) définit la propriété du [**fournisseur**](/windows/desktop/api/Provider/nl-provider-provider) .</span><span class="sxs-lookup"><span data-stu-id="4867a-230">The [**\_\_ProviderRegistration**](--providerregistration.md) class defines the [**Provider**](/windows/desktop/api/Provider/nl-provider-provider) property.</span></span> <span data-ttu-id="4867a-231">Seuls les administrateurs peuvent inscrire un fournisseur en créant une instance de [**\_ \_ Win32Provider**](--win32provider.md) et **\_ \_ ClassProviderRegistration**.</span><span class="sxs-lookup"><span data-stu-id="4867a-231">Only administrators can register a provider by creating an instance of [**\_\_Win32Provider**](--win32provider.md) and **\_\_ClassProviderRegistration**.</span></span> <span data-ttu-id="4867a-232">Seuls les administrateurs peuvent supprimer un fournisseur.</span><span class="sxs-lookup"><span data-stu-id="4867a-232">Only administrators can delete a provider.</span></span>

## <a name="requirements"></a><span data-ttu-id="4867a-233">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="4867a-233">Requirements</span></span>



| <span data-ttu-id="4867a-234">Condition requise</span><span class="sxs-lookup"><span data-stu-id="4867a-234">Requirement</span></span> | <span data-ttu-id="4867a-235">Valeur</span><span class="sxs-lookup"><span data-stu-id="4867a-235">Value</span></span> |
|-------------------------------------|--------------------------------|
| <span data-ttu-id="4867a-236">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="4867a-236">Minimum supported client</span></span><br/> | <span data-ttu-id="4867a-237">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="4867a-237">Windows Vista</span></span><br/>       |
| <span data-ttu-id="4867a-238">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="4867a-238">Minimum supported server</span></span><br/> | <span data-ttu-id="4867a-239">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="4867a-239">Windows Server 2008</span></span><br/> |
| <span data-ttu-id="4867a-240">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="4867a-240">Namespace</span></span><br/>                | <span data-ttu-id="4867a-241">Tous les espaces de noms WMI</span><span class="sxs-lookup"><span data-stu-id="4867a-241">All WMI namespaces</span></span><br/>  |



## <a name="see-also"></a><span data-ttu-id="4867a-242">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="4867a-242">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4867a-243">**\_\_ObjectProviderRegistration**</span><span class="sxs-lookup"><span data-stu-id="4867a-243">**\_\_ObjectProviderRegistration**</span></span>](/windows/desktop/WmiSdk/--objectproviderregistration)
</dt> <dt>

[<span data-ttu-id="4867a-244">Classes système WMI</span><span class="sxs-lookup"><span data-stu-id="4867a-244">WMI System Classes</span></span>](wmi-system-classes.md)
</dt> <dt>

[<span data-ttu-id="4867a-245">Inscription d’un fournisseur de classe</span><span class="sxs-lookup"><span data-stu-id="4867a-245">Registering a Class Provider</span></span>](registering-a-class-provider.md)
</dt> <dt>

[<span data-ttu-id="4867a-246">Inscription d’un fournisseur d’instances</span><span class="sxs-lookup"><span data-stu-id="4867a-246">Registering an Instance Provider</span></span>](registering-an-instance-provider.md)
</dt> <dt>

[<span data-ttu-id="4867a-247">**\_\_Win32Provider**</span><span class="sxs-lookup"><span data-stu-id="4867a-247">**\_\_Win32Provider**</span></span>](--win32provider.md)
</dt> </dl>

 

