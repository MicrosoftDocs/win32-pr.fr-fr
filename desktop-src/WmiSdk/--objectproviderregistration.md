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
ms.openlocfilehash: a60b24278fb235cec38c127e7ebbbb481e49a140
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104319337"
---
# <a name="__objectproviderregistration-class"></a><span data-ttu-id="5b87f-103">\_\_ObjectProviderRegistration, classe</span><span class="sxs-lookup"><span data-stu-id="5b87f-103">\_\_ObjectProviderRegistration class</span></span>

<span data-ttu-id="5b87f-104">La classe système abstraite **\_ \_ ObjectProviderRegistration** sert de classe parente pour les classes utilisées pour inscrire des fournisseurs de classes et d’instances dans WMI.</span><span class="sxs-lookup"><span data-stu-id="5b87f-104">The **\_\_ObjectProviderRegistration** abstract system class serves as the parent class for classes that are used to register class and instance providers in WMI.</span></span>

<span data-ttu-id="5b87f-105">La syntaxe suivante est simplifiée à partir de code au format MOF (Managed Object Format) et inclut toutes les propriétés héritées.</span><span class="sxs-lookup"><span data-stu-id="5b87f-105">The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.</span></span> <span data-ttu-id="5b87f-106">Les propriétés sont répertoriées par ordre alphabétique, et non par ordre MOF.</span><span class="sxs-lookup"><span data-stu-id="5b87f-106">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="5b87f-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="5b87f-107">Syntax</span></span>

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

## <a name="members"></a><span data-ttu-id="5b87f-108">Membres</span><span class="sxs-lookup"><span data-stu-id="5b87f-108">Members</span></span>

<span data-ttu-id="5b87f-109">La classe **\_ \_ ObjectProviderRegistration** possède les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="5b87f-109">The **\_\_ObjectProviderRegistration** class has these types of members:</span></span>

-   [<span data-ttu-id="5b87f-110">Propriétés</span><span class="sxs-lookup"><span data-stu-id="5b87f-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="5b87f-111">Propriétés</span><span class="sxs-lookup"><span data-stu-id="5b87f-111">Properties</span></span>

<span data-ttu-id="5b87f-112">La classe **\_ \_ ObjectProviderRegistration** possède les propriétés suivantes.</span><span class="sxs-lookup"><span data-stu-id="5b87f-112">The **\_\_ObjectProviderRegistration** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="5b87f-113">**InteractionType**</span><span class="sxs-lookup"><span data-stu-id="5b87f-113">**InteractionType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5b87f-114">Type de données : **sint32**</span><span class="sxs-lookup"><span data-stu-id="5b87f-114">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="5b87f-115">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="5b87f-115">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="5b87f-116">Indique si le fournisseur de classes ou d’instances fournit ses propres données, ou s’appuie sur WMI et le référentiel Common Information Model (CIM).</span><span class="sxs-lookup"><span data-stu-id="5b87f-116">Indicates whether or not the class or instance provider supplies its own data, or relies on WMI and the Common Information Model (CIM) repository.</span></span> <span data-ttu-id="5b87f-117">Les fournisseurs d’extraction prennent en charge l’accès dynamique à leurs données, et les fournisseurs de notifications push stockent leurs données dans le référentiel CIM et s’appuient sur WMI pour y accéder.</span><span class="sxs-lookup"><span data-stu-id="5b87f-117">Pull providers support dynamic access to their data, and push providers store their data in the CIM repository, and rely on WMI to provide access to it.</span></span> <span data-ttu-id="5b87f-118">Pour plus d’informations, consultez Détermination de l' [État d’envoi ou d’extraction](determining-push-or-pull-status.md).</span><span class="sxs-lookup"><span data-stu-id="5b87f-118">For more information, see [Determining Push or Pull Status](determining-push-or-pull-status.md).</span></span> <span data-ttu-id="5b87f-119">La valeur par défaut est 0 (zéro).</span><span class="sxs-lookup"><span data-stu-id="5b87f-119">The default value is 0 (zero).</span></span>

<dt>

<span id="Pull"></span><span id="pull"></span><span id="PULL"></span>

<span data-ttu-id="5b87f-120"><span id="Pull"></span><span id="pull"></span><span id="PULL"></span>**Pull** (0)</span><span class="sxs-lookup"><span data-stu-id="5b87f-120"><span id="Pull"></span><span id="pull"></span><span id="PULL"></span>**Pull** (0)</span></span>


</dt> <dd>

<span data-ttu-id="5b87f-121">Le fournisseur est un fournisseur d’extraction.</span><span class="sxs-lookup"><span data-stu-id="5b87f-121">Provider is a pull provider.</span></span>

</dd> <dt>

<span id="Push"></span><span id="push"></span><span id="PUSH"></span>

<span data-ttu-id="5b87f-122"><span id="Push"></span><span id="push"></span><span id="PUSH"></span>**Push** (1)</span><span class="sxs-lookup"><span data-stu-id="5b87f-122"><span id="Push"></span><span id="push"></span><span id="PUSH"></span>**Push** (1)</span></span>


</dt> <dd>

<span data-ttu-id="5b87f-123">Le fournisseur est un fournisseur push.</span><span class="sxs-lookup"><span data-stu-id="5b87f-123">Provider is a push provider.</span></span>

</dd> <dt>

<span id="PushVerify"></span><span id="pushverify"></span><span id="PUSHVERIFY"></span>

<span data-ttu-id="5b87f-124"><span id="PushVerify"></span><span id="pushverify"></span><span id="PUSHVERIFY"></span>**PushVerify** (2)</span><span class="sxs-lookup"><span data-stu-id="5b87f-124"><span id="PushVerify"></span><span id="pushverify"></span><span id="PUSHVERIFY"></span>**PushVerify** (2)</span></span>


</dt> <dd>

<span data-ttu-id="5b87f-125">Le fournisseur est un fournisseur de vérification de push.</span><span class="sxs-lookup"><span data-stu-id="5b87f-125">Provider is a push-verify provider.</span></span> <span data-ttu-id="5b87f-126">Notez que Push-Verify n’est pas pris en charge pour l’instant.</span><span class="sxs-lookup"><span data-stu-id="5b87f-126">Note that push-verify is not supported at this time.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="5b87f-127">**moteur**</span><span class="sxs-lookup"><span data-stu-id="5b87f-127">**provider**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5b87f-128">Type de données : **\_ \_ fournisseur**</span><span class="sxs-lookup"><span data-stu-id="5b87f-128">Data type: **\_\_Provider**</span></span>
</dt> <dt>

<span data-ttu-id="5b87f-129">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="5b87f-129">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="5b87f-130">Référence à une instance de [**\_ \_ fournisseur**](--provider.md) qui représente un chemin d’accès d’objet au fournisseur d’objets.</span><span class="sxs-lookup"><span data-stu-id="5b87f-130">Reference to an instance of [**\_\_Provider**](--provider.md) that represents an object path to the object provider.</span></span> <span data-ttu-id="5b87f-131">Cette propriété est héritée de [**\_ \_ ProviderRegistration**](--providerregistration.md).</span><span class="sxs-lookup"><span data-stu-id="5b87f-131">This property is inherited from [**\_\_ProviderRegistration**](--providerregistration.md).</span></span>

</dd> <dt>

<span data-ttu-id="5b87f-132">**QuerySupportLevels**</span><span class="sxs-lookup"><span data-stu-id="5b87f-132">**QuerySupportLevels**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5b87f-133">Type de données : tableau de **chaînes**</span><span class="sxs-lookup"><span data-stu-id="5b87f-133">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="5b87f-134">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="5b87f-134">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="5b87f-135">Tableau des types de prise en charge par le fournisseur du traitement des requêtes.</span><span class="sxs-lookup"><span data-stu-id="5b87f-135">Array of the types of provider-included support for query processing.</span></span> <span data-ttu-id="5b87f-136">Les fournisseurs de classes ne prennent en charge aucun type de requête.</span><span class="sxs-lookup"><span data-stu-id="5b87f-136">Class providers do not support any type of queries.</span></span> <span data-ttu-id="5b87f-137">Les fournisseurs d’instances peuvent affecter à **QuerySupportLevels** la **valeur null** s’ils ne prennent pas en charge le traitement des requêtes.</span><span class="sxs-lookup"><span data-stu-id="5b87f-137">Instance providers can set **QuerySupportLevels** to **NULL** if they do not support query processing.</span></span> <span data-ttu-id="5b87f-138">Les fournisseurs qui prennent en charge les requêtes implémentent la méthode [**IWbemServices :: ExecQueryAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-execqueryasync) et définissent cette propriété sur une ou plusieurs des valeurs suivantes (le type de propriété est un tableau).</span><span class="sxs-lookup"><span data-stu-id="5b87f-138">Providers that support queries implement the [**IWbemServices::ExecQueryAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-execqueryasync) method, and set this property to one or more of the following values (the property type is an array).</span></span>

<span data-ttu-id="5b87f-139">« WQL : UnarySelect »</span><span class="sxs-lookup"><span data-stu-id="5b87f-139">"WQL:UnarySelect"</span></span>

<span data-ttu-id="5b87f-140">« WQL : References »</span><span class="sxs-lookup"><span data-stu-id="5b87f-140">"WQL:References"</span></span>

<span data-ttu-id="5b87f-141">« WQL : ASSOCIATORS »</span><span class="sxs-lookup"><span data-stu-id="5b87f-141">"WQL:Associators"</span></span>

<span data-ttu-id="5b87f-142">« WQL : V1ProviderDefined »</span><span class="sxs-lookup"><span data-stu-id="5b87f-142">"WQL:V1ProviderDefined"</span></span>

</dd> <dt>

<span data-ttu-id="5b87f-143">**SupportsBatching**</span><span class="sxs-lookup"><span data-stu-id="5b87f-143">**SupportsBatching**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5b87f-144">Type de données : **booléen**</span><span class="sxs-lookup"><span data-stu-id="5b87f-144">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="5b87f-145">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="5b87f-145">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="5b87f-146">Non utilisé.</span><span class="sxs-lookup"><span data-stu-id="5b87f-146">Not used.</span></span>

</dd> <dt>

<span data-ttu-id="5b87f-147">**SupportsDelete**</span><span class="sxs-lookup"><span data-stu-id="5b87f-147">**SupportsDelete**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5b87f-148">Type de données : **booléen**</span><span class="sxs-lookup"><span data-stu-id="5b87f-148">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="5b87f-149">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="5b87f-149">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="5b87f-150">Si la **valeur est true**, le fournisseur prend en charge la suppression des données.</span><span class="sxs-lookup"><span data-stu-id="5b87f-150">If **True**, the provider supports data deletion.</span></span>

<dt>

<span data-ttu-id="5b87f-151">Vrai</span><span class="sxs-lookup"><span data-stu-id="5b87f-151">True</span></span>
</dt> <dd>

<span data-ttu-id="5b87f-152">Le fournisseur prend en charge la suppression de classe ou d’instance en implémentant l’un des [**Eleteclassasync IWbemServices ::D**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-deleteclassasync) (fournisseurs de classes) ou [**IWbemServices ::D eleteinstanceasync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-deleteinstanceasync) (fournisseurs d’instances).</span><span class="sxs-lookup"><span data-stu-id="5b87f-152">The provider supports class or instance deletion by implementing one of either [**IWbemServices::DeleteClassAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-deleteclassasync) (class providers), or [**IWbemServices::DeleteInstanceAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-deleteinstanceasync) (instance providers).</span></span>

</dd> <dt>

<span data-ttu-id="5b87f-153">Faux</span><span class="sxs-lookup"><span data-stu-id="5b87f-153">False</span></span>
</dt> <dd>

<span data-ttu-id="5b87f-154">Le fournisseur ne prend pas en charge la suppression des données et retourne le **\_ fournisseur WBEM E \_ \_ non \_ compatible** à partir de [**DeleteClassAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-deleteclassasync) ou [**DeleteInstanceAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-deleteinstanceasync).</span><span class="sxs-lookup"><span data-stu-id="5b87f-154">The provider does not support data deletion, and returns **WBEM\_E\_PROVIDER\_NOT\_CAPABLE** from [**DeleteClassAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-deleteclassasync) or [**DeleteInstanceAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-deleteinstanceasync).</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="5b87f-155">**SupportsEnumeration**</span><span class="sxs-lookup"><span data-stu-id="5b87f-155">**SupportsEnumeration**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5b87f-156">Type de données : **booléen**</span><span class="sxs-lookup"><span data-stu-id="5b87f-156">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="5b87f-157">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="5b87f-157">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="5b87f-158">Si la **valeur est true**, le fournisseur prend en charge l’énumération des données.</span><span class="sxs-lookup"><span data-stu-id="5b87f-158">If **True**, the provider supports data enumeration.</span></span>

<dt>

<span data-ttu-id="5b87f-159">Vrai</span><span class="sxs-lookup"><span data-stu-id="5b87f-159">True</span></span>
</dt> <dd>

<span data-ttu-id="5b87f-160">Le fournisseur prend en charge l’énumération des données en implémentant l’une des classes [**IWbemServices :: CreateClassEnumAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-createclassenumasync) (fournisseurs de classes) ou [**IWbemServices :: CreateInstanceEnumAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-createinstanceenumasync) (fournisseurs d’instances).</span><span class="sxs-lookup"><span data-stu-id="5b87f-160">The provider supports data enumeration by implementing one of either [**IWbemServices::CreateClassEnumAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-createclassenumasync) (class providers), or [**IWbemServices::CreateInstanceEnumAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-createinstanceenumasync) (instance providers).</span></span>

</dd> <dt>

<span data-ttu-id="5b87f-161">Faux</span><span class="sxs-lookup"><span data-stu-id="5b87f-161">False</span></span>
</dt> <dd>

<span data-ttu-id="5b87f-162">Le fournisseur ne prend pas en charge l’énumération des données et retourne le **\_ fournisseur WBEM E \_ \_ non \_ compatible** à partir de [**CreateClassEnumAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-createclassenumasync) ou [**CreateInstanceEnumAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-createinstanceenumasync).</span><span class="sxs-lookup"><span data-stu-id="5b87f-162">The provider does not support data enumeration, and returns **WBEM\_E\_PROVIDER\_NOT\_CAPABLE** from [**CreateClassEnumAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-createclassenumasync) or [**CreateInstanceEnumAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-createinstanceenumasync).</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="5b87f-163">**SupportsGet**</span><span class="sxs-lookup"><span data-stu-id="5b87f-163">**SupportsGet**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5b87f-164">Type de données : **booléen**</span><span class="sxs-lookup"><span data-stu-id="5b87f-164">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="5b87f-165">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="5b87f-165">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="5b87f-166">Si la **valeur est true**, la classe ou le fournisseur d’instance prend en charge la récupération des données.</span><span class="sxs-lookup"><span data-stu-id="5b87f-166">If **True**, the class or instance provider supports data retrieval.</span></span>

<dt>

<span data-ttu-id="5b87f-167">Vrai</span><span class="sxs-lookup"><span data-stu-id="5b87f-167">True</span></span>
</dt> <dd>

<span data-ttu-id="5b87f-168">Le fournisseur prend en charge la récupération de données en implémentant [**IWbemServices :: GetObjectAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-getobjectasync).</span><span class="sxs-lookup"><span data-stu-id="5b87f-168">The provider supports data retrieval by implementing [**IWbemServices::GetObjectAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-getobjectasync).</span></span>

</dd> <dt>

<span data-ttu-id="5b87f-169">Faux</span><span class="sxs-lookup"><span data-stu-id="5b87f-169">False</span></span>
</dt> <dd>

<span data-ttu-id="5b87f-170">Le fournisseur ne prend pas en charge la récupération de données et retourne le **\_ fournisseur WBEM E \_ \_ non \_ compatible** à partir de [**GetObjectAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-getobjectasync).</span><span class="sxs-lookup"><span data-stu-id="5b87f-170">The provider does not support data retrieval, and returns **WBEM\_E\_PROVIDER\_NOT\_CAPABLE** from [**GetObjectAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-getobjectasync).</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="5b87f-171">**SupportsPut**</span><span class="sxs-lookup"><span data-stu-id="5b87f-171">**SupportsPut**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5b87f-172">Type de données : **booléen**</span><span class="sxs-lookup"><span data-stu-id="5b87f-172">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="5b87f-173">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="5b87f-173">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="5b87f-174">Si la **valeur est true**, la classe ou le fournisseur d’instance prend en charge la modification des données.</span><span class="sxs-lookup"><span data-stu-id="5b87f-174">If **True**, the class or instance provider supports data modification.</span></span>

<dt>

<span data-ttu-id="5b87f-175">Vrai</span><span class="sxs-lookup"><span data-stu-id="5b87f-175">True</span></span>
</dt> <dd>

<span data-ttu-id="5b87f-176">Le fournisseur prend en charge la modification de classe ou d’instance en implémentant l’un des [**Utclassasync IWbemServices ::P**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-putclassasync) (fournisseurs de classes) ou [**IWbemServices ::P utinstanceasync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-putinstanceasync) (fournisseurs de classes).</span><span class="sxs-lookup"><span data-stu-id="5b87f-176">The provider supports class or instance modification by implementing one of either [**IWbemServices::PutClassAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-putclassasync) (class providers), or [**IWbemServices::PutInstanceAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-putinstanceasync) (class providers).</span></span>

</dd> <dt>

<span data-ttu-id="5b87f-177">Faux</span><span class="sxs-lookup"><span data-stu-id="5b87f-177">False</span></span>
</dt> <dd>

<span data-ttu-id="5b87f-178">Le fournisseur ne prend pas en charge la modification des données et retourne le **\_ fournisseur WBEM E \_ \_ non \_ compatible** à partir de [**PutClassAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-putclassasync) ou [**PutInstanceAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-putinstanceasync).</span><span class="sxs-lookup"><span data-stu-id="5b87f-178">The provider does not support data modification and returns **WBEM\_E\_PROVIDER\_NOT\_CAPABLE** from [**PutClassAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-putclassasync) or [**PutInstanceAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-putinstanceasync).</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="5b87f-179">**SupportsTransactions**</span><span class="sxs-lookup"><span data-stu-id="5b87f-179">**SupportsTransactions**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5b87f-180">Type de données : **booléen**</span><span class="sxs-lookup"><span data-stu-id="5b87f-180">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="5b87f-181">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="5b87f-181">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="5b87f-182">Non utilisé.</span><span class="sxs-lookup"><span data-stu-id="5b87f-182">Not used.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="5b87f-183">Notes</span><span class="sxs-lookup"><span data-stu-id="5b87f-183">Remarks</span></span>

<span data-ttu-id="5b87f-184">La classe **\_ \_ ObjectProviderRegistration** est dérivée de [**\_ \_ ProviderRegistration**](--providerregistration.md).</span><span class="sxs-lookup"><span data-stu-id="5b87f-184">The **\_\_ObjectProviderRegistration** class is derived from [**\_\_ProviderRegistration**](--providerregistration.md).</span></span>

<span data-ttu-id="5b87f-185">Les fournisseurs de classes doivent définir la propriété **SupportsEnumeration** sur **true** , car les fournisseurs doivent être en mesure de fournir WMI avec une liste de leurs classes.</span><span class="sxs-lookup"><span data-stu-id="5b87f-185">Class providers must set the **SupportsEnumeration** property to **True** because the providers must be able to supply WMI with a list of their classes.</span></span> <span data-ttu-id="5b87f-186">Si un fournisseur de classe tente d’affecter la valeur **false** à cette propriété, WMI signale l’inscription comme non conforme.</span><span class="sxs-lookup"><span data-stu-id="5b87f-186">If a class provider attempts to set this property to **False**, WMI flags the registration as illegal.</span></span> <span data-ttu-id="5b87f-187">Les fournisseurs d’instances ne sont pas requis pour prendre en charge l’énumération et peuvent choisir de définir **SupportsEnumeration** sur **true** ou **false**.</span><span class="sxs-lookup"><span data-stu-id="5b87f-187">Instance providers are not required to support enumeration, and can choose to set **SupportsEnumeration** to either **True** or **False**.</span></span>

<span data-ttu-id="5b87f-188">Un fournisseur qui définit **QuerySupportLevels** sur « WQL : UnarySelect » peut accepter une requête qui se compose de l’instruction SELECT de base telle qu’elle est prise en charge dans la version 1,0 de WMI.</span><span class="sxs-lookup"><span data-stu-id="5b87f-188">A provider that sets **QuerySupportLevels** to "WQL:UnarySelect" can accept a query that consists of the basic SELECT statement as supported in WMI version 1.0.</span></span> <span data-ttu-id="5b87f-189">Les fournisseurs de classes et d’instances sont censés être en mesure de gérer la propriété système de **\_ \_ classe** .</span><span class="sxs-lookup"><span data-stu-id="5b87f-189">Both class and instance providers are expected to be able to handle the **\_\_CLASS** system property.</span></span> <span data-ttu-id="5b87f-190">Les fournisseurs de classes sont également censés traiter la propriété système de la **\_ \_ superclasse** et l’opérateur ISA.</span><span class="sxs-lookup"><span data-stu-id="5b87f-190">Class providers are also expected to process the **\_\_SUPERCLASS** system property and the ISA operator.</span></span> <span data-ttu-id="5b87f-191">L’opérateur ISA est utilisé pour étendre un jeu de résultats aux classes dérivées.</span><span class="sxs-lookup"><span data-stu-id="5b87f-191">The ISA operator is used to expand a result set to derived classes.</span></span> <span data-ttu-id="5b87f-192">Si un fournisseur reçoit une requête qu’il ne peut pas interpréter, il demande que WMI le gère en retournant la valeur d’erreur **WBEM \_ E \_ trop \_ complexe** .</span><span class="sxs-lookup"><span data-stu-id="5b87f-192">If a provider is given a query that it cannot interpret, it requests that WMI handle it by returning the **WBEM\_E\_TOO\_COMPLEX** error value.</span></span> <span data-ttu-id="5b87f-193">Pour obtenir une description de la syntaxe WQL valide, consultez [interrogation avec WQL](querying-with-wql.md).</span><span class="sxs-lookup"><span data-stu-id="5b87f-193">For a description of valid WQL syntax, see [Querying with WQL](querying-with-wql.md).</span></span>

<span data-ttu-id="5b87f-194">Un fournisseur qui affecte à **QuerySupportLevels** la valeur **WQL : V1ProviderDefined** peut essayer de prendre en charge un plus grand ensemble de syntaxe SQL à son propre risque, par exemple la `ORDER BY` clause.</span><span class="sxs-lookup"><span data-stu-id="5b87f-194">A provider that sets **QuerySupportLevels** to **WQL:V1ProviderDefined** can try to support a larger set of the SQL syntax at its own risk, such as the `ORDER BY` clause.</span></span> <span data-ttu-id="5b87f-195">WMI n’interprète pas les clauses supplémentaires ou ne tente pas de s’assurer que le jeu de résultats est correct.</span><span class="sxs-lookup"><span data-stu-id="5b87f-195">WMI does not interpret the additional clauses, or attempt to ensure that the result set is correct.</span></span>

<span data-ttu-id="5b87f-196">Seuls les administrateurs peuvent inscrire ou supprimer un fournisseur en créant une instance de [**\_ \_ Win32Provider**](--win32provider.md) et en l’inscrivant.</span><span class="sxs-lookup"><span data-stu-id="5b87f-196">Only administrators can register or delete a provider by creating an instance of [**\_\_Win32Provider**](--win32provider.md) and registering it.</span></span>

## <a name="requirements"></a><span data-ttu-id="5b87f-197">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="5b87f-197">Requirements</span></span>



| <span data-ttu-id="5b87f-198">Condition requise</span><span class="sxs-lookup"><span data-stu-id="5b87f-198">Requirement</span></span> | <span data-ttu-id="5b87f-199">Valeur</span><span class="sxs-lookup"><span data-stu-id="5b87f-199">Value</span></span> |
|-------------------------------------|--------------------------------|
| <span data-ttu-id="5b87f-200">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="5b87f-200">Minimum supported client</span></span><br/> | <span data-ttu-id="5b87f-201">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="5b87f-201">Windows Vista</span></span><br/>       |
| <span data-ttu-id="5b87f-202">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="5b87f-202">Minimum supported server</span></span><br/> | <span data-ttu-id="5b87f-203">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="5b87f-203">Windows Server 2008</span></span><br/> |
| <span data-ttu-id="5b87f-204">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="5b87f-204">Namespace</span></span><br/>                | <span data-ttu-id="5b87f-205">Tous les espaces de noms WMI</span><span class="sxs-lookup"><span data-stu-id="5b87f-205">All WMI namespaces</span></span><br/>  |



## <a name="see-also"></a><span data-ttu-id="5b87f-206">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="5b87f-206">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5b87f-207">**\_\_ProviderRegistration**</span><span class="sxs-lookup"><span data-stu-id="5b87f-207">**\_\_ProviderRegistration**</span></span>](/windows/desktop/WmiSdk/--providerregistration)
</dt> <dt>

[<span data-ttu-id="5b87f-208">Classes système WMI</span><span class="sxs-lookup"><span data-stu-id="5b87f-208">WMI System Classes</span></span>](wmi-system-classes.md)
</dt> <dt>

[<span data-ttu-id="5b87f-209">Inscription d’un fournisseur</span><span class="sxs-lookup"><span data-stu-id="5b87f-209">Registering a Provider</span></span>](registering-a-provider.md)
</dt> </dl>

 

