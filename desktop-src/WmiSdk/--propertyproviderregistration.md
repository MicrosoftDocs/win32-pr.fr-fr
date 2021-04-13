---
description: Inscrit les fournisseurs de propriétés dans WMI.
ms.assetid: 24792884-3fb9-4974-83d5-1c5fc1fa72a1
ms.tgt_platform: multiple
title: Classe __PropertyProviderRegistration
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- __PropertyProviderRegistration
- All
- All
- All
api_type:
- Schema
api_location:
- All
ms.openlocfilehash: 6d618a62eab4ba799a2d0e152763fcef6567fd42
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104529307"
---
# <a name="__propertyproviderregistration-class"></a><span data-ttu-id="4559e-103">\_\_PropertyProviderRegistration, classe</span><span class="sxs-lookup"><span data-stu-id="4559e-103">\_\_PropertyProviderRegistration class</span></span>

<span data-ttu-id="4559e-104">La classe système **\_ \_ PropertyProviderRegistration** inscrit des fournisseurs de propriétés dans WMI.</span><span class="sxs-lookup"><span data-stu-id="4559e-104">The **\_\_PropertyProviderRegistration** system class registers property providers in WMI.</span></span>

<span data-ttu-id="4559e-105">La syntaxe suivante est simplifiée à partir de code au format MOF (Managed Object Format) et inclut toutes les propriétés héritées.</span><span class="sxs-lookup"><span data-stu-id="4559e-105">The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.</span></span> <span data-ttu-id="4559e-106">Les propriétés sont répertoriées par ordre alphabétique, et non par ordre MOF.</span><span class="sxs-lookup"><span data-stu-id="4559e-106">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="4559e-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="4559e-107">Syntax</span></span>

``` syntax
class __PropertyProviderRegistration : __ProviderRegistration
{
  __Provider REF provider;
  boolean        SupportsPut = False;
  boolean        SupportsGet = False;
};
```

## <a name="members"></a><span data-ttu-id="4559e-108">Membres</span><span class="sxs-lookup"><span data-stu-id="4559e-108">Members</span></span>

<span data-ttu-id="4559e-109">La classe **\_ \_ PropertyProviderRegistration** possède les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="4559e-109">The **\_\_PropertyProviderRegistration** class has these types of members:</span></span>

-   [<span data-ttu-id="4559e-110">Propriétés</span><span class="sxs-lookup"><span data-stu-id="4559e-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="4559e-111">Propriétés</span><span class="sxs-lookup"><span data-stu-id="4559e-111">Properties</span></span>

<span data-ttu-id="4559e-112">La classe **\_ \_ PropertyProviderRegistration** possède les propriétés suivantes.</span><span class="sxs-lookup"><span data-stu-id="4559e-112">The **\_\_PropertyProviderRegistration** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="4559e-113">**moteur**</span><span class="sxs-lookup"><span data-stu-id="4559e-113">**provider**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4559e-114">Type de données : **\_ \_ fournisseur**</span><span class="sxs-lookup"><span data-stu-id="4559e-114">Data type: **\_\_Provider**</span></span>
</dt> <dt>

<span data-ttu-id="4559e-115">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="4559e-115">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="4559e-116">Référence à une instance du [**\_ \_ fournisseur**](--provider.md) qui représente le chemin d’accès de l’objet du fournisseur de propriétés.</span><span class="sxs-lookup"><span data-stu-id="4559e-116">Reference to an instance of [**\_\_Provider**](--provider.md) that represents the object path of the property provider.</span></span> <span data-ttu-id="4559e-117">Cette propriété est héritée de [**\_ \_ ProviderRegistration**](--providerregistration.md).</span><span class="sxs-lookup"><span data-stu-id="4559e-117">This property is inherited from [**\_\_ProviderRegistration**](--providerregistration.md).</span></span>

</dd> <dt>

<span data-ttu-id="4559e-118">**SupportsGet**</span><span class="sxs-lookup"><span data-stu-id="4559e-118">**SupportsGet**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4559e-119">Type de données : **booléen**</span><span class="sxs-lookup"><span data-stu-id="4559e-119">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="4559e-120">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="4559e-120">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="4559e-121">Indique si le fournisseur de classes ou d’instances prend en charge la récupération de données.</span><span class="sxs-lookup"><span data-stu-id="4559e-121">Describes whether the class or instance provider supports data retrieval.</span></span>

<dt>

<span data-ttu-id="4559e-122">Vrai</span><span class="sxs-lookup"><span data-stu-id="4559e-122">True</span></span>
</dt> <dd>

<span data-ttu-id="4559e-123">Le fournisseur prend en charge la récupération de données en implémentant [**IWbemServices :: GetObjectAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-getobjectasync).</span><span class="sxs-lookup"><span data-stu-id="4559e-123">The provider supports data retrieval by implementing [**IWbemServices::GetObjectAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-getobjectasync).</span></span>

</dd> <dt>

<span data-ttu-id="4559e-124">Faux</span><span class="sxs-lookup"><span data-stu-id="4559e-124">False</span></span>
</dt> <dd>

<span data-ttu-id="4559e-125">Le fournisseur ne prend pas en charge la récupération de données et retourne le **\_ fournisseur WBEM E \_ \_ non \_ compatible** à partir de [**GetObjectAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-getobjectasync).</span><span class="sxs-lookup"><span data-stu-id="4559e-125">The provider does not support data retrieval, and returns **WBEM\_E\_PROVIDER\_NOT\_CAPABLE** from [**GetObjectAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-getobjectasync).</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="4559e-126">**SupportsPut**</span><span class="sxs-lookup"><span data-stu-id="4559e-126">**SupportsPut**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4559e-127">Type de données : **booléen**</span><span class="sxs-lookup"><span data-stu-id="4559e-127">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="4559e-128">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="4559e-128">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="4559e-129">Indique si le fournisseur de classes ou d’instances prend en charge la modification des données.</span><span class="sxs-lookup"><span data-stu-id="4559e-129">Describes whether the class or instance provider supports data modification.</span></span>

<dt>

<span data-ttu-id="4559e-130">Vrai</span><span class="sxs-lookup"><span data-stu-id="4559e-130">True</span></span>
</dt> <dd>

<span data-ttu-id="4559e-131">Le fournisseur prend en charge la modification de classe ou d’instance en implémentant l’une des méthodes suivantes :</span><span class="sxs-lookup"><span data-stu-id="4559e-131">The provider supports class or instance modification by implementing one of the following methods:</span></span>

-   <span data-ttu-id="4559e-132">[**IWbemServices ::P utclassasync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-putclassasync) (fournisseurs de classes)</span><span class="sxs-lookup"><span data-stu-id="4559e-132">[**IWbemServices::PutClassAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-putclassasync) (class providers)</span></span>
-   <span data-ttu-id="4559e-133">[**IWbemServices ::P utinstanceasync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-putinstanceasync) (fournisseurs de classes)</span><span class="sxs-lookup"><span data-stu-id="4559e-133">[**IWbemServices::PutInstanceAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-putinstanceasync) (class providers)</span></span>

</dd> <dt>

<span data-ttu-id="4559e-134">Faux</span><span class="sxs-lookup"><span data-stu-id="4559e-134">False</span></span>
</dt> <dd>

<span data-ttu-id="4559e-135">Le fournisseur ne prend pas en charge la modification des données et retourne le **\_ fournisseur WBEM E \_ \_ non \_ compatible** à partir de [**PutClassAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-putclassasync) ou [**PutInstanceAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-putinstanceasync).</span><span class="sxs-lookup"><span data-stu-id="4559e-135">The provider does not support data modification and returns **WBEM\_E\_PROVIDER\_NOT\_CAPABLE** from [**PutClassAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-putclassasync) or [**PutInstanceAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-putinstanceasync).</span></span>

</dd> </dl>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="4559e-136">Notes</span><span class="sxs-lookup"><span data-stu-id="4559e-136">Remarks</span></span>

<span data-ttu-id="4559e-137">La classe **\_ \_ PropertyProviderRegistration** est dérivée de [**\_ \_ ProviderRegistration**](--providerregistration.md).</span><span class="sxs-lookup"><span data-stu-id="4559e-137">The **\_\_PropertyProviderRegistration** class is derived from [**\_\_ProviderRegistration**](--providerregistration.md).</span></span> <span data-ttu-id="4559e-138">Seuls les administrateurs peuvent inscrire un fournisseur de propriétés en créant une instance de [**\_ \_ Win32Provider**](--win32provider.md) et **\_ \_ PropertyProviderRegistration**.</span><span class="sxs-lookup"><span data-stu-id="4559e-138">Only administrators can register a property provider by creating an instance of [**\_\_Win32Provider**](--win32provider.md) and **\_\_PropertyProviderRegistration**.</span></span> <span data-ttu-id="4559e-139">Seuls les administrateurs peuvent supprimer un fournisseur de propriétés.</span><span class="sxs-lookup"><span data-stu-id="4559e-139">Only administrators can delete a property provider.</span></span>

## <a name="requirements"></a><span data-ttu-id="4559e-140">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="4559e-140">Requirements</span></span>



| <span data-ttu-id="4559e-141">Condition requise</span><span class="sxs-lookup"><span data-stu-id="4559e-141">Requirement</span></span> | <span data-ttu-id="4559e-142">Valeur</span><span class="sxs-lookup"><span data-stu-id="4559e-142">Value</span></span> |
|-------------------------------------|--------------------------------|
| <span data-ttu-id="4559e-143">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="4559e-143">Minimum supported client</span></span><br/> | <span data-ttu-id="4559e-144">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="4559e-144">Windows Vista</span></span><br/>       |
| <span data-ttu-id="4559e-145">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="4559e-145">Minimum supported server</span></span><br/> | <span data-ttu-id="4559e-146">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="4559e-146">Windows Server 2008</span></span><br/> |
| <span data-ttu-id="4559e-147">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="4559e-147">Namespace</span></span><br/>                | <span data-ttu-id="4559e-148">Tous les espaces de noms WMI</span><span class="sxs-lookup"><span data-stu-id="4559e-148">All WMI namespaces</span></span><br/>  |



## <a name="see-also"></a><span data-ttu-id="4559e-149">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="4559e-149">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4559e-150">**\_\_ProviderRegistration**</span><span class="sxs-lookup"><span data-stu-id="4559e-150">**\_\_ProviderRegistration**</span></span>](/windows/desktop/WmiSdk/--providerregistration)
</dt> <dt>

[<span data-ttu-id="4559e-151">Classes système WMI</span><span class="sxs-lookup"><span data-stu-id="4559e-151">WMI System Classes</span></span>](wmi-system-classes.md)
</dt> <dt>

[<span data-ttu-id="4559e-152">Inscription d’un fournisseur de propriétés</span><span class="sxs-lookup"><span data-stu-id="4559e-152">Registering a Property Provider</span></span>](registering-a-property-provider.md)
</dt> </dl>

 

