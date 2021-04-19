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
# <a name="__instanceproviderregistration-class"></a><span data-ttu-id="dbf68-103">\_\_InstanceProviderRegistration, classe</span><span class="sxs-lookup"><span data-stu-id="dbf68-103">\_\_InstanceProviderRegistration class</span></span>

<span data-ttu-id="dbf68-104">La classe système **\_ \_ InstanceProviderRegistration** inscrit des fournisseurs d’instances dans WMI.</span><span class="sxs-lookup"><span data-stu-id="dbf68-104">The **\_\_InstanceProviderRegistration** system class registers instance providers in WMI.</span></span>

<span data-ttu-id="dbf68-105">La syntaxe suivante est simplifiée à partir de code au format MOF (Managed Object Format) et inclut toutes les propriétés héritées.</span><span class="sxs-lookup"><span data-stu-id="dbf68-105">The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.</span></span> <span data-ttu-id="dbf68-106">Les propriétés sont répertoriées par ordre alphabétique, et non par ordre MOF.</span><span class="sxs-lookup"><span data-stu-id="dbf68-106">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="dbf68-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="dbf68-107">Syntax</span></span>

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

## <a name="members"></a><span data-ttu-id="dbf68-108">Membres</span><span class="sxs-lookup"><span data-stu-id="dbf68-108">Members</span></span>

<span data-ttu-id="dbf68-109">La classe **\_ \_ InstanceProviderRegistration** possède les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="dbf68-109">The **\_\_InstanceProviderRegistration** class has these types of members:</span></span>

-   [<span data-ttu-id="dbf68-110">Propriétés</span><span class="sxs-lookup"><span data-stu-id="dbf68-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="dbf68-111">Propriétés</span><span class="sxs-lookup"><span data-stu-id="dbf68-111">Properties</span></span>

<span data-ttu-id="dbf68-112">La classe **\_ \_ InstanceProviderRegistration** possède les propriétés suivantes.</span><span class="sxs-lookup"><span data-stu-id="dbf68-112">The **\_\_InstanceProviderRegistration** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="dbf68-113">**InteractionType**</span><span class="sxs-lookup"><span data-stu-id="dbf68-113">**InteractionType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="dbf68-114">Type de données : **sint32**</span><span class="sxs-lookup"><span data-stu-id="dbf68-114">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="dbf68-115">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="dbf68-115">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="dbf68-116">Indique qu’un fournisseur de classes ou d’instances fournit des données, ou récupère des données à partir de WMI et du référentiel Common Information Model (CIM).</span><span class="sxs-lookup"><span data-stu-id="dbf68-116">Indicates that a class or instance provider supplies data, or retrieves data from WMI and the Common Information Model (CIM) repository.</span></span> <span data-ttu-id="dbf68-117">Les fournisseurs d’extraction prennent en charge l’accès dynamique à leurs données ; et les fournisseurs de notifications push stockent leurs données dans le référentiel CIM et utilisent WMI pour y accéder.</span><span class="sxs-lookup"><span data-stu-id="dbf68-117">Pull providers support dynamic access to their data; and push providers store their data in the CIM repository, and use WMI to provide access to it.</span></span> <span data-ttu-id="dbf68-118">Pour plus d’informations, consultez Détermination de l' [État d’envoi ou d’extraction](determining-push-or-pull-status.md).</span><span class="sxs-lookup"><span data-stu-id="dbf68-118">For more information, see [Determining Push or Pull Status](determining-push-or-pull-status.md).</span></span> <span data-ttu-id="dbf68-119">La valeur par défaut est 0 (zéro).</span><span class="sxs-lookup"><span data-stu-id="dbf68-119">The default value is 0 (zero).</span></span>

<dt>

<span id="Pull"></span><span id="pull"></span><span id="PULL"></span>

<span data-ttu-id="dbf68-120"><span id="Pull"></span><span id="pull"></span><span id="PULL"></span>**Pull** (0)</span><span class="sxs-lookup"><span data-stu-id="dbf68-120"><span id="Pull"></span><span id="pull"></span><span id="PULL"></span>**Pull** (0)</span></span>


</dt> <dd>

<span data-ttu-id="dbf68-121">Le fournisseur est un fournisseur d’extraction.</span><span class="sxs-lookup"><span data-stu-id="dbf68-121">Provider is a pull provider.</span></span>

</dd> <dt>

<span id="Push"></span><span id="push"></span><span id="PUSH"></span>

<span data-ttu-id="dbf68-122"><span id="Push"></span><span id="push"></span><span id="PUSH"></span>**Push** (1)</span><span class="sxs-lookup"><span data-stu-id="dbf68-122"><span id="Push"></span><span id="push"></span><span id="PUSH"></span>**Push** (1)</span></span>


</dt> <dd>

<span data-ttu-id="dbf68-123">Le fournisseur est un fournisseur push.</span><span class="sxs-lookup"><span data-stu-id="dbf68-123">Provider is a push provider.</span></span>

</dd> <dt>

<span id="PushVerify"></span><span id="pushverify"></span><span id="PUSHVERIFY"></span>

<span data-ttu-id="dbf68-124"><span id="PushVerify"></span><span id="pushverify"></span><span id="PUSHVERIFY"></span>**PushVerify** (2)</span><span class="sxs-lookup"><span data-stu-id="dbf68-124"><span id="PushVerify"></span><span id="pushverify"></span><span id="PUSHVERIFY"></span>**PushVerify** (2)</span></span>


</dt> <dd>

<span data-ttu-id="dbf68-125">Le fournisseur est un fournisseur de vérification de push.</span><span class="sxs-lookup"><span data-stu-id="dbf68-125">Provider is a push-verify provider.</span></span> <span data-ttu-id="dbf68-126">Notez que les fournisseurs de vérification de Push ne sont pas pris en charge actuellement.</span><span class="sxs-lookup"><span data-stu-id="dbf68-126">Note that push-verify providers are not currently supported.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="dbf68-127">**moteur**</span><span class="sxs-lookup"><span data-stu-id="dbf68-127">**provider**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="dbf68-128">Type de données : **\_ \_ fournisseur**</span><span class="sxs-lookup"><span data-stu-id="dbf68-128">Data type: **\_\_Provider**</span></span>
</dt> <dt>

<span data-ttu-id="dbf68-129">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="dbf68-129">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="dbf68-130">Référence à une instance du [**\_ \_ fournisseur**](--provider.md) qui représente le chemin d’accès de l’objet au fournisseur d’instance.</span><span class="sxs-lookup"><span data-stu-id="dbf68-130">Reference to an instance of [**\_\_Provider**](--provider.md) that represents the object path to the instance provider.</span></span> <span data-ttu-id="dbf68-131">Cette propriété est héritée de [**\_ \_ ProviderRegistration**](--providerregistration.md).</span><span class="sxs-lookup"><span data-stu-id="dbf68-131">This property is inherited from [**\_\_ProviderRegistration**](--providerregistration.md).</span></span>

</dd> <dt>

<span data-ttu-id="dbf68-132">**QuerySupportLevels**</span><span class="sxs-lookup"><span data-stu-id="dbf68-132">**QuerySupportLevels**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="dbf68-133">Type de données : tableau de **chaînes**</span><span class="sxs-lookup"><span data-stu-id="dbf68-133">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="dbf68-134">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="dbf68-134">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="dbf68-135">Tableau des types de prise en charge par le fournisseur du traitement des requêtes.</span><span class="sxs-lookup"><span data-stu-id="dbf68-135">Array of the types of provider-included support for query processing.</span></span> <span data-ttu-id="dbf68-136">Les fournisseurs de classes ne prennent pas en charge tous les types de requêtes.</span><span class="sxs-lookup"><span data-stu-id="dbf68-136">Class providers do not support all types of queries.</span></span> <span data-ttu-id="dbf68-137">Les fournisseurs d’instances peuvent affecter à **QuerySupportLevels** la **valeur null** s’ils ne prennent pas en charge le traitement des requêtes.</span><span class="sxs-lookup"><span data-stu-id="dbf68-137">Instance providers can set **QuerySupportLevels** to **NULL** if they do not support query processing.</span></span> <span data-ttu-id="dbf68-138">Les fournisseurs qui prennent en charge les requêtes implémentent la méthode [**IWbemServices :: ExecQueryAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-execqueryasync) et définissent cette propriété sur une ou plusieurs des valeurs suivantes.</span><span class="sxs-lookup"><span data-stu-id="dbf68-138">Providers that support queries implement the [**IWbemServices::ExecQueryAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-execqueryasync) method, and set this property to one or more of the following values.</span></span>

<dt>



 <span data-ttu-id="dbf68-139">("WQL : UnarySelect")</span><span class="sxs-lookup"><span data-stu-id="dbf68-139">("WQL:UnarySelect")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="dbf68-140">("WQL : References")</span><span class="sxs-lookup"><span data-stu-id="dbf68-140">("WQL:References")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="dbf68-141">(« WQL : ASSOCIATORS »)</span><span class="sxs-lookup"><span data-stu-id="dbf68-141">("WQL:Associators")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="dbf68-142">("WQL : V1ProviderDefined")</span><span class="sxs-lookup"><span data-stu-id="dbf68-142">("WQL:V1ProviderDefined")</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="dbf68-143">**SupportsBatching**</span><span class="sxs-lookup"><span data-stu-id="dbf68-143">**SupportsBatching**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="dbf68-144">Type de données : **booléen**</span><span class="sxs-lookup"><span data-stu-id="dbf68-144">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="dbf68-145">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="dbf68-145">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="dbf68-146">Non utilisé.</span><span class="sxs-lookup"><span data-stu-id="dbf68-146">Not used.</span></span>

</dd> <dt>

<span data-ttu-id="dbf68-147">**SupportsDelete**</span><span class="sxs-lookup"><span data-stu-id="dbf68-147">**SupportsDelete**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="dbf68-148">Type de données : **booléen**</span><span class="sxs-lookup"><span data-stu-id="dbf68-148">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="dbf68-149">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="dbf68-149">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="dbf68-150">Si la **valeur est true**, le fournisseur prend en charge la suppression des données.</span><span class="sxs-lookup"><span data-stu-id="dbf68-150">If **True**, the provider supports data deletion.</span></span>

<dt>

<span data-ttu-id="dbf68-151">Vrai</span><span class="sxs-lookup"><span data-stu-id="dbf68-151">True</span></span>
</dt> <dd>

<span data-ttu-id="dbf68-152">Le fournisseur prend en charge la suppression d’une classe ou d’une instance en implémentant [**IWbemServices ::D eleteclassasync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-deleteclassasync) (fournisseurs de classes) ou [**IWbemServices ::D eleteinstanceasync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-deleteinstanceasync) (fournisseurs d’instances).</span><span class="sxs-lookup"><span data-stu-id="dbf68-152">The provider supports class or instance deletion by implementing either [**IWbemServices::DeleteClassAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-deleteclassasync) (class providers), or [**IWbemServices::DeleteInstanceAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-deleteinstanceasync) (instance providers).</span></span>

</dd> <dt>

<span data-ttu-id="dbf68-153">Faux</span><span class="sxs-lookup"><span data-stu-id="dbf68-153">False</span></span>
</dt> <dd>

<span data-ttu-id="dbf68-154">Le fournisseur ne prend pas en charge la suppression des données et retourne le **\_ fournisseur WBEM E \_ \_ non \_ compatible** à partir de [**DeleteClassAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-deleteclassasync) ou [**DeleteInstanceAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-deleteinstanceasync).</span><span class="sxs-lookup"><span data-stu-id="dbf68-154">The provider does not support data deletion, and returns **WBEM\_E\_PROVIDER\_NOT\_CAPABLE** from [**DeleteClassAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-deleteclassasync) or [**DeleteInstanceAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-deleteinstanceasync).</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="dbf68-155">**SupportsEnumeration**</span><span class="sxs-lookup"><span data-stu-id="dbf68-155">**SupportsEnumeration**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="dbf68-156">Type de données : **booléen**</span><span class="sxs-lookup"><span data-stu-id="dbf68-156">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="dbf68-157">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="dbf68-157">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="dbf68-158">Si la **valeur est true**, le fournisseur prend en charge l’énumération des données.</span><span class="sxs-lookup"><span data-stu-id="dbf68-158">If **True**, the provider supports data enumeration.</span></span>

<dt>



 <span data-ttu-id="dbf68-159">:</span><span class="sxs-lookup"><span data-stu-id="dbf68-159">(True)</span></span>


</dt> <dd>

<span data-ttu-id="dbf68-160">Le fournisseur prend en charge l’énumération des données en implémentant l’une des classes [**IWbemServices :: CreateClassEnumAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-createclassenumasync) (fournisseurs de classes) ou [**IWbemServices :: CreateInstanceEnumAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-createinstanceenumasync) (fournisseurs d’instances).</span><span class="sxs-lookup"><span data-stu-id="dbf68-160">The provider supports data enumeration by implementing one of either [**IWbemServices::CreateClassEnumAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-createclassenumasync) (class providers), or [**IWbemServices::CreateInstanceEnumAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-createinstanceenumasync) (instance providers).</span></span>

</dd> <dt>



 <span data-ttu-id="dbf68-161">Fausses</span><span class="sxs-lookup"><span data-stu-id="dbf68-161">(False)</span></span>


</dt> <dd>

<span data-ttu-id="dbf68-162">Le fournisseur ne prend pas en charge l’énumération des données et retourne le **\_ fournisseur WBEM E \_ \_ non \_ compatible** à partir de [**CreateClassEnumAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-createclassenumasync) ou [**CreateInstanceEnumAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-createinstanceenumasync).</span><span class="sxs-lookup"><span data-stu-id="dbf68-162">The provider does not support data enumeration, and returns **WBEM\_E\_PROVIDER\_NOT\_CAPABLE** from [**CreateClassEnumAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-createclassenumasync) or [**CreateInstanceEnumAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-createinstanceenumasync).</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="dbf68-163">**SupportsGet**</span><span class="sxs-lookup"><span data-stu-id="dbf68-163">**SupportsGet**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="dbf68-164">Type de données : **booléen**</span><span class="sxs-lookup"><span data-stu-id="dbf68-164">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="dbf68-165">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="dbf68-165">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="dbf68-166">Si la **valeur est true**, la classe ou le fournisseur d’instance prend en charge la récupération des données.</span><span class="sxs-lookup"><span data-stu-id="dbf68-166">If **True**, the class or instance provider supports data retrieval.</span></span>

<dt>

<span data-ttu-id="dbf68-167">Vrai</span><span class="sxs-lookup"><span data-stu-id="dbf68-167">True</span></span>
</dt> <dd>

<span data-ttu-id="dbf68-168">Le fournisseur prend en charge la récupération de données en implémentant [**IWbemServices :: GetObjectAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-getobjectasync).</span><span class="sxs-lookup"><span data-stu-id="dbf68-168">The provider supports data retrieval by implementing [**IWbemServices::GetObjectAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-getobjectasync).</span></span>

</dd> <dt>

<span data-ttu-id="dbf68-169">Faux</span><span class="sxs-lookup"><span data-stu-id="dbf68-169">False</span></span>
</dt> <dd>

<span data-ttu-id="dbf68-170">Le fournisseur ne prend pas en charge la récupération de données et retourne le **\_ fournisseur WBEM E \_ \_ non \_ compatible** à partir de [**GetObjectAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-getobjectasync).</span><span class="sxs-lookup"><span data-stu-id="dbf68-170">The provider does not support data retrieval, and returns **WBEM\_E\_PROVIDER\_NOT\_CAPABLE** from [**GetObjectAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-getobjectasync).</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="dbf68-171">**SupportsPut**</span><span class="sxs-lookup"><span data-stu-id="dbf68-171">**SupportsPut**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="dbf68-172">Type de données : **booléen**</span><span class="sxs-lookup"><span data-stu-id="dbf68-172">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="dbf68-173">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="dbf68-173">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="dbf68-174">Si la **valeur est true**, la classe ou le fournisseur d’instance prend en charge la modification des données.</span><span class="sxs-lookup"><span data-stu-id="dbf68-174">If **True**, the class or instance provider supports data modification.</span></span>

<dt>



 <span data-ttu-id="dbf68-175">:</span><span class="sxs-lookup"><span data-stu-id="dbf68-175">(True)</span></span>


</dt> <dd>

<span data-ttu-id="dbf68-176">Le fournisseur prend en charge la modification de classe ou d’instance en implémentant l’une des méthodes suivantes : [**IWbemServices ::P utclassasync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-putclassasync) (fournisseurs de classes) ou [**IWbemServices ::P utinstanceasync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-putinstanceasync) (fournisseurs de classes).</span><span class="sxs-lookup"><span data-stu-id="dbf68-176">The provider supports class or instance modification by implementing one of the following methods: [**IWbemServices::PutClassAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-putclassasync) (class providers), or [**IWbemServices::PutInstanceAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-putinstanceasync) (class providers).</span></span>

</dd> <dt>



 <span data-ttu-id="dbf68-177">Fausses</span><span class="sxs-lookup"><span data-stu-id="dbf68-177">(False)</span></span>


</dt> <dd>

<span data-ttu-id="dbf68-178">Le fournisseur ne prend pas en charge la modification des données et retourne le **\_ fournisseur WBEM E \_ \_ non \_ compatible** à partir de [**PutClassAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-putclassasync) ou [**PutInstanceAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-putinstanceasync).</span><span class="sxs-lookup"><span data-stu-id="dbf68-178">The provider does not support data modification and returns **WBEM\_E\_PROVIDER\_NOT\_CAPABLE** from [**PutClassAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-putclassasync) or [**PutInstanceAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-putinstanceasync).</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="dbf68-179">**SupportsTransactions**</span><span class="sxs-lookup"><span data-stu-id="dbf68-179">**SupportsTransactions**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="dbf68-180">Type de données : **booléen**</span><span class="sxs-lookup"><span data-stu-id="dbf68-180">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="dbf68-181">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="dbf68-181">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="dbf68-182">Non utilisé.</span><span class="sxs-lookup"><span data-stu-id="dbf68-182">Not used.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="dbf68-183">Notes</span><span class="sxs-lookup"><span data-stu-id="dbf68-183">Remarks</span></span>

<span data-ttu-id="dbf68-184">La classe **\_ \_ InstanceProviderRegistration** est dérivée de [**\_ \_ ObjectProviderRegistration**](--objectproviderregistration.md), qui est dérivée de [**\_ \_ ProviderRegistration**](--providerregistration.md).</span><span class="sxs-lookup"><span data-stu-id="dbf68-184">The **\_\_InstanceProviderRegistration** class is derived from [**\_\_ObjectProviderRegistration**](--objectproviderregistration.md), which is derived from [**\_\_ProviderRegistration**](--providerregistration.md).</span></span> <span data-ttu-id="dbf68-185">Seuls les administrateurs peuvent inscrire un fournisseur d’instances en créant une instance de [**\_ \_ Win32Provider**](--win32provider.md) et **\_ \_ InstanceProviderRegistration**.</span><span class="sxs-lookup"><span data-stu-id="dbf68-185">Only administrators can register an instance provider by creating an instance of [**\_\_Win32Provider**](--win32provider.md) and **\_\_InstanceProviderRegistration**.</span></span> <span data-ttu-id="dbf68-186">Seuls les administrateurs peuvent supprimer un fournisseur.</span><span class="sxs-lookup"><span data-stu-id="dbf68-186">Only administrators can delete a provider.</span></span>

## <a name="requirements"></a><span data-ttu-id="dbf68-187">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="dbf68-187">Requirements</span></span>



| <span data-ttu-id="dbf68-188">Condition requise</span><span class="sxs-lookup"><span data-stu-id="dbf68-188">Requirement</span></span> | <span data-ttu-id="dbf68-189">Valeur</span><span class="sxs-lookup"><span data-stu-id="dbf68-189">Value</span></span> |
|-------------------------------------|--------------------------------|
| <span data-ttu-id="dbf68-190">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="dbf68-190">Minimum supported client</span></span><br/> | <span data-ttu-id="dbf68-191">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="dbf68-191">Windows Vista</span></span><br/>       |
| <span data-ttu-id="dbf68-192">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="dbf68-192">Minimum supported server</span></span><br/> | <span data-ttu-id="dbf68-193">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="dbf68-193">Windows Server 2008</span></span><br/> |
| <span data-ttu-id="dbf68-194">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="dbf68-194">Namespace</span></span><br/>                | <span data-ttu-id="dbf68-195">Tous les espaces de noms WMI</span><span class="sxs-lookup"><span data-stu-id="dbf68-195">All WMI namespaces</span></span><br/>  |



## <a name="see-also"></a><span data-ttu-id="dbf68-196">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="dbf68-196">See also</span></span>

<dl> <dt>

[<span data-ttu-id="dbf68-197">**\_\_ObjectProviderRegistration**</span><span class="sxs-lookup"><span data-stu-id="dbf68-197">**\_\_ObjectProviderRegistration**</span></span>](/windows/desktop/WmiSdk/--objectproviderregistration)
</dt> <dt>

[<span data-ttu-id="dbf68-198">Classes système WMI</span><span class="sxs-lookup"><span data-stu-id="dbf68-198">WMI System Classes</span></span>](wmi-system-classes.md)
</dt> <dt>

[<span data-ttu-id="dbf68-199">Inscription d’un fournisseur de classe</span><span class="sxs-lookup"><span data-stu-id="dbf68-199">Registering a Class Provider</span></span>](registering-a-class-provider.md)
</dt> <dt>

[<span data-ttu-id="dbf68-200">Inscription d’un fournisseur d’instances</span><span class="sxs-lookup"><span data-stu-id="dbf68-200">Registering an Instance Provider</span></span>](registering-an-instance-provider.md)
</dt> </dl>

 

