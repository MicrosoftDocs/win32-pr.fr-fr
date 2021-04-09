---
description: L' \_ objet CIM CollectionOfMSEs autorise le regroupement d' \_ objets ManagedSystemElement CIM afin d’associer les paramètres et les configurations. Il est abstrait d’exiger une définition et un affinage sémantique supplémentaires dans les sous-classes.
ms.assetid: 9448a7a1-defc-4bac-9ce6-29ec2406d573
ms.tgt_platform: multiple
title: CIM_CollectionOfMSEs, classe (fournisseurs WMI CIMWin32)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_CollectionOfMSEs
- CIM_CollectionOfMSEs.Caption
- CIM_CollectionOfMSEs.CollectionID
- CIM_CollectionOfMSEs.Description
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 57942dd6e00d819e4375ddd316e5e15126621b97
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104110994"
---
# <a name="cim_collectionofmses-class-cimwin32-wmi-providers"></a><span data-ttu-id="89f2b-104">CIM_CollectionOfMSEs, classe (fournisseurs WMI CIMWin32)</span><span class="sxs-lookup"><span data-stu-id="89f2b-104">CIM_CollectionOfMSEs class (CIMWin32 WMI Providers)</span></span>

<span data-ttu-id="89f2b-105">L’objet **CIM \_ CollectionOfMSEs** autorise le regroupement d’objets [**\_ ManagedSystemElement CIM**](cim-managedsystemelement.md) afin d’associer les paramètres et les configurations.</span><span class="sxs-lookup"><span data-stu-id="89f2b-105">The **CIM\_CollectionOfMSEs** object allows the grouping of [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md) objects for the purpose of associating settings and configurations.</span></span> <span data-ttu-id="89f2b-106">Il est abstrait d’exiger une définition et un affinage sémantique supplémentaires dans les sous-classes.</span><span class="sxs-lookup"><span data-stu-id="89f2b-106">It is abstract to require further definition and semantic refinement in subclasses.</span></span>

<span data-ttu-id="89f2b-107">L' **objet \_ CIMOM CIM** ne contient pas d’informations d’État ou d’État, mais il représente uniquement un regroupement d’éléments.</span><span class="sxs-lookup"><span data-stu-id="89f2b-107">The **CIM\_CollectionOfMSEs** object does not carry any state or status information, but only represents a grouping of elements.</span></span> <span data-ttu-id="89f2b-108">Pour cette raison, il est incorrect pour les groupes de sous-classes dont l’État/l’État est **CIM \_ CollectionOfMSEs**. un exemple est [**CIM \_ RedundancyGroup**](cim-redundancygroup.md) (qui est correctement sous-classé à partir de [**CIM \_ LogicalElement**](cim-logicalelement.md)).</span><span class="sxs-lookup"><span data-stu-id="89f2b-108">For this reason, it is incorrect to subclass groups that have state/status from **CIM\_CollectionOfMSEs**, An example is [**CIM\_RedundancyGroup**](cim-redundancygroup.md) (which is correctly subclassed from [**CIM\_LogicalElement**](cim-logicalelement.md)).</span></span> <span data-ttu-id="89f2b-109">En général, les collections agrègent des objets « like » et représentent une optimisation.</span><span class="sxs-lookup"><span data-stu-id="89f2b-109">Collections typically aggregate 'like' objects, and represent an optimization.</span></span> <span data-ttu-id="89f2b-110">Sans les collections, l’une est forcée de définir des associations [**CIM \_ ElementSetting**](cim-elementsetting.md) et [**CIM \_ ElementConfiguration**](cim-elementconfiguration.md) , pour lier des paramètres et des objets de configuration à des [**\_ ManagedSystemElements CIM**](cim-managedsystemelement.md)individuels.</span><span class="sxs-lookup"><span data-stu-id="89f2b-110">Without collections, one is forced to define individual [**CIM\_ElementSetting**](cim-elementsetting.md) and [**CIM\_ElementConfiguration**](cim-elementconfiguration.md) associations, to tie settings and configuration objects to individual [**CIM\_ManagedSystemElements**](cim-managedsystemelement.md).</span></span> <span data-ttu-id="89f2b-111">Il peut y avoir de nombreuses doublons pour attribuer le même paramètre à plusieurs objets.</span><span class="sxs-lookup"><span data-stu-id="89f2b-111">There may be much duplication in assigning the same setting to multiple objects.</span></span> <span data-ttu-id="89f2b-112">En outre, l’utilisation de l’objet de collection permet de déterminer que les associations de paramètres et de configuration sont identiques pour les membres de la collection.</span><span class="sxs-lookup"><span data-stu-id="89f2b-112">In addition, using the collection object allows the determination that the setting and configuration associations are indeed the same for the collection's members.</span></span> <span data-ttu-id="89f2b-113">Dans le cas contraire, ces informations seraient obtenues en définissant la collection de manière propriétaire, puis en interrogeant les associations **CIM \_ ElementSetting** et **CIM \_ ElementConfiguration** pour déterminer si le jeu d’collections est entièrement couvert.</span><span class="sxs-lookup"><span data-stu-id="89f2b-113">This information would otherwise be obtained by defining the collection in a proprietary manner, and then querying the **CIM\_ElementSetting** and **CIM\_ElementConfiguration** associations to determine if the collection set is completely covered.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="89f2b-114">Les classes de la DMTF (Distributed Management Task Force) CIM (Common Information Model) sont les classes parentes sur lesquelles les classes WMI sont générées.</span><span class="sxs-lookup"><span data-stu-id="89f2b-114">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="89f2b-115">WMI ne prend actuellement en charge que les [schémas de version CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="89f2b-115">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="89f2b-116">La syntaxe suivante est simplifiée à partir de code au format MOF (Managed Object Format) et inclut toutes les propriétés héritées.</span><span class="sxs-lookup"><span data-stu-id="89f2b-116">The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.</span></span> <span data-ttu-id="89f2b-117">Les propriétés sont répertoriées par ordre alphabétique, et non par ordre MOF.</span><span class="sxs-lookup"><span data-stu-id="89f2b-117">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="89f2b-118">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="89f2b-118">Syntax</span></span>

``` syntax
class CIM_CollectionOfMSEs
{
  string Caption;
  string CollectionID;
  string Description;
};
```

## <a name="members"></a><span data-ttu-id="89f2b-119">Membres</span><span class="sxs-lookup"><span data-stu-id="89f2b-119">Members</span></span>

<span data-ttu-id="89f2b-120">La classe **CIM \_ CollectionOfMSEs** possède les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="89f2b-120">The **CIM\_CollectionOfMSEs** class has these types of members:</span></span>

-   [<span data-ttu-id="89f2b-121">Propriétés</span><span class="sxs-lookup"><span data-stu-id="89f2b-121">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="89f2b-122">Propriétés</span><span class="sxs-lookup"><span data-stu-id="89f2b-122">Properties</span></span>

<span data-ttu-id="89f2b-123">La classe **CIM \_ CollectionOfMSEs** possède les propriétés suivantes.</span><span class="sxs-lookup"><span data-stu-id="89f2b-123">The **CIM\_CollectionOfMSEs** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="89f2b-124">**Caption**</span><span class="sxs-lookup"><span data-stu-id="89f2b-124">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="89f2b-125">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="89f2b-125">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="89f2b-126">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="89f2b-126">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="89f2b-127">Courte description textuelle de l’objet CollectionOfMSEs.</span><span class="sxs-lookup"><span data-stu-id="89f2b-127">Short textual description of the CollectionOfMSEs object.</span></span>

</dd> <dt>

<span data-ttu-id="89f2b-128">**CollectionID**</span><span class="sxs-lookup"><span data-stu-id="89f2b-128">**CollectionID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="89f2b-129">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="89f2b-129">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="89f2b-130">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="89f2b-130">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="89f2b-131">Identification de l’objet de collection.</span><span class="sxs-lookup"><span data-stu-id="89f2b-131">Identification of the Collection object.</span></span> <span data-ttu-id="89f2b-132">Lorsqu’elle est sous-classée, la propriété de l’un peut être substituée pour être une propriété de clé.</span><span class="sxs-lookup"><span data-stu-id="89f2b-132">When subclassed, the CollectionID property can be overridden to be a Key property.</span></span>

</dd> <dt>

<span data-ttu-id="89f2b-133">**Description**</span><span class="sxs-lookup"><span data-stu-id="89f2b-133">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="89f2b-134">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="89f2b-134">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="89f2b-135">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="89f2b-135">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="89f2b-136">Description textuelle de l’objet CollectionOfMSEs.</span><span class="sxs-lookup"><span data-stu-id="89f2b-136">Textual description of the CollectionOfMSEs object.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="89f2b-137">Notes</span><span class="sxs-lookup"><span data-stu-id="89f2b-137">Remarks</span></span>

<span data-ttu-id="89f2b-138">WMI n’implémente pas cette classe.</span><span class="sxs-lookup"><span data-stu-id="89f2b-138">WMI does not implement this class.</span></span> <span data-ttu-id="89f2b-139">Consultez [classes Win32](win32-provider.md) pour les classes WMI dérivées de **CIM \_ CollectionOfMSEs**.</span><span class="sxs-lookup"><span data-stu-id="89f2b-139">See [Win32 Classes](win32-provider.md) for WMI classes derived from **CIM\_CollectionOfMSEs**.</span></span>

<span data-ttu-id="89f2b-140">Cette documentation est dérivée des descriptions de classe CIM publiées par le DMTF.</span><span class="sxs-lookup"><span data-stu-id="89f2b-140">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="89f2b-141">Microsoft peut avoir apporté des modifications pour corriger les erreurs mineures, se conformer aux normes de documentation du kit de développement logiciel (SDK) Microsoft ou fournir plus d’informations.</span><span class="sxs-lookup"><span data-stu-id="89f2b-141">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="89f2b-142">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="89f2b-142">Requirements</span></span>



| <span data-ttu-id="89f2b-143">Condition requise</span><span class="sxs-lookup"><span data-stu-id="89f2b-143">Requirement</span></span> | <span data-ttu-id="89f2b-144">Valeur</span><span class="sxs-lookup"><span data-stu-id="89f2b-144">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="89f2b-145">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="89f2b-145">Minimum supported client</span></span><br/> | <span data-ttu-id="89f2b-146">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="89f2b-146">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="89f2b-147">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="89f2b-147">Minimum supported server</span></span><br/> | <span data-ttu-id="89f2b-148">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="89f2b-148">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="89f2b-149">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="89f2b-149">Namespace</span></span><br/>                | <span data-ttu-id="89f2b-150">\\Cimv2 racine</span><span class="sxs-lookup"><span data-stu-id="89f2b-150">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="89f2b-151">MOF</span><span class="sxs-lookup"><span data-stu-id="89f2b-151">MOF</span></span><br/>                      | <dl> <span data-ttu-id="89f2b-152"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="89f2b-152"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="89f2b-153">DLL</span><span class="sxs-lookup"><span data-stu-id="89f2b-153">DLL</span></span><br/>                      | <dl> <span data-ttu-id="89f2b-154"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="89f2b-154"><dt>CIMWin32.dll</dt></span></span> </dl> |



 

 




