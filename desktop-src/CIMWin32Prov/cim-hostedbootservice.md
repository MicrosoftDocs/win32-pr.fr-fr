---
description: La \_ classe CIM HostedBootService associe un système d’hébergement et un service de démarrage. Étant donné que cette relation est sous-classée à partir de CIM \_ service hébergé, elle hérite du schéma d’étendue/d’attribution de noms défini pour le service, où un service s’en remet au système d’hébergement.
ms.assetid: 91621288-a231-4423-94df-7601bdf2ebe1
ms.tgt_platform: multiple
title: Classe CIM_HostedBootService
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_HostedBootService
- CIM_HostedBootService.Antecedent
- CIM_HostedBootService.Dependent
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 12baa364653feda1400ad15d658e6739859b2521
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104110854"
---
# <a name="cim_hostedbootservice-class"></a><span data-ttu-id="29588-104">\_Classe CIM HostedBootService</span><span class="sxs-lookup"><span data-stu-id="29588-104">CIM\_HostedBootService class</span></span>

<span data-ttu-id="29588-105">La classe **CIM \_ HostedBootService** associe un système d’hébergement et un service de démarrage.</span><span class="sxs-lookup"><span data-stu-id="29588-105">The **CIM\_HostedBootService** class associates a hosting system and a boot service.</span></span> <span data-ttu-id="29588-106">Étant donné que cette relation est sous-classée à partir de [**CIM \_ service hébergé**](cim-hostedservice.md), elle hérite du schéma d’étendue/d’attribution de noms défini pour le service, où un service s’en remet au système d’hébergement.</span><span class="sxs-lookup"><span data-stu-id="29588-106">Since this relationship is subclassed from [**CIM\_HostedService**](cim-hostedservice.md), it inherits the scoping/naming scheme defined for service, where a service defers to its hosting system.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="29588-107">Les classes de la DMTF (Distributed Management Task Force) CIM (Common Information Model) sont les classes parentes sur lesquelles les classes WMI sont générées.</span><span class="sxs-lookup"><span data-stu-id="29588-107">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="29588-108">WMI ne prend actuellement en charge que les [schémas de version CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="29588-108">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="29588-109">La syntaxe suivante est simplifiée à partir de code au format MOF (Managed Object Format) et inclut toutes les propriétés héritées.</span><span class="sxs-lookup"><span data-stu-id="29588-109">The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.</span></span> <span data-ttu-id="29588-110">Les propriétés sont répertoriées par ordre alphabétique, et non par ordre MOF.</span><span class="sxs-lookup"><span data-stu-id="29588-110">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="29588-111">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="29588-111">Syntax</span></span>

``` syntax
[Abstract, UUID("{6DAE7092-DB36-11d2-85FC-0000F8102E5F}"), AMENDMENT]
class CIM_HostedBootService : CIM_HostedService
{
  CIM_System      REF Antecedent;
  CIM_BootService REF Dependent;
};
```

## <a name="members"></a><span data-ttu-id="29588-112">Membres</span><span class="sxs-lookup"><span data-stu-id="29588-112">Members</span></span>

<span data-ttu-id="29588-113">La classe **CIM \_ HostedBootService** possède les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="29588-113">The **CIM\_HostedBootService** class has these types of members:</span></span>

-   [<span data-ttu-id="29588-114">Propriétés</span><span class="sxs-lookup"><span data-stu-id="29588-114">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="29588-115">Propriétés</span><span class="sxs-lookup"><span data-stu-id="29588-115">Properties</span></span>

<span data-ttu-id="29588-116">La classe **CIM \_ HostedBootService** possède les propriétés suivantes.</span><span class="sxs-lookup"><span data-stu-id="29588-116">The **CIM\_HostedBootService** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="29588-117">**Antécédent**</span><span class="sxs-lookup"><span data-stu-id="29588-117">**Antecedent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="29588-118">Type de données **: \_ système CIM**</span><span class="sxs-lookup"><span data-stu-id="29588-118">Data type: **CIM\_System**</span></span>
</dt> <dt>

<span data-ttu-id="29588-119">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="29588-119">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="29588-120">Qualificateurs : [**override**](/windows/desktop/WmiSdk/standard-qualifiers) (Antecedent)</span><span class="sxs-lookup"><span data-stu-id="29588-120">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) (Antecedent)</span></span>
</dt> </dl>

<span data-ttu-id="29588-121">[**\_ Système CIM**](cim-system.md) qui décrit le système d’hébergement.</span><span class="sxs-lookup"><span data-stu-id="29588-121">A [**CIM\_System**](cim-system.md) that describes the hosting system.</span></span>

</dd> <dt>

<span data-ttu-id="29588-122">**Charge**</span><span class="sxs-lookup"><span data-stu-id="29588-122">**Dependent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="29588-123">Type de données : **CIM \_ BootService**</span><span class="sxs-lookup"><span data-stu-id="29588-123">Data type: **CIM\_BootService**</span></span>
</dt> <dt>

<span data-ttu-id="29588-124">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="29588-124">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="29588-125">Qualificateurs : [**override**](/windows/desktop/WmiSdk/standard-qualifiers) (« Dependent »)</span><span class="sxs-lookup"><span data-stu-id="29588-125">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Dependent")</span></span>
</dt> </dl>

<span data-ttu-id="29588-126">[**\_ BootService CIM**](cim-bootservice.md) qui décrit le service de démarrage hébergé sur le système.</span><span class="sxs-lookup"><span data-stu-id="29588-126">A [**CIM\_BootService**](cim-bootservice.md) that describes the boot service hosted on the system.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="29588-127">Notes</span><span class="sxs-lookup"><span data-stu-id="29588-127">Remarks</span></span>

<span data-ttu-id="29588-128">La classe **CIM \_ HostedBootService** est dérivée de [**CIM \_ service hébergé**](cim-hostedservice.md).</span><span class="sxs-lookup"><span data-stu-id="29588-128">The **CIM\_HostedBootService** class is derived from [**CIM\_HostedService**](cim-hostedservice.md).</span></span>

<span data-ttu-id="29588-129">WMI n’implémente pas cette classe.</span><span class="sxs-lookup"><span data-stu-id="29588-129">WMI does not implement this class.</span></span>

<span data-ttu-id="29588-130">Cette documentation est dérivée des descriptions de classe CIM publiées par le DMTF.</span><span class="sxs-lookup"><span data-stu-id="29588-130">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="29588-131">Microsoft peut avoir apporté des modifications pour corriger les erreurs mineures, se conformer aux normes de documentation du kit de développement logiciel (SDK) Microsoft ou fournir plus d’informations.</span><span class="sxs-lookup"><span data-stu-id="29588-131">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="29588-132">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="29588-132">Requirements</span></span>



| <span data-ttu-id="29588-133">Condition requise</span><span class="sxs-lookup"><span data-stu-id="29588-133">Requirement</span></span> | <span data-ttu-id="29588-134">Valeur</span><span class="sxs-lookup"><span data-stu-id="29588-134">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="29588-135">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="29588-135">Minimum supported client</span></span><br/> | <span data-ttu-id="29588-136">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="29588-136">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="29588-137">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="29588-137">Minimum supported server</span></span><br/> | <span data-ttu-id="29588-138">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="29588-138">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="29588-139">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="29588-139">Namespace</span></span><br/>                | <span data-ttu-id="29588-140">\\Cimv2 racine</span><span class="sxs-lookup"><span data-stu-id="29588-140">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="29588-141">MOF</span><span class="sxs-lookup"><span data-stu-id="29588-141">MOF</span></span><br/>                      | <dl> <span data-ttu-id="29588-142"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="29588-142"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="29588-143">DLL</span><span class="sxs-lookup"><span data-stu-id="29588-143">DLL</span></span><br/>                      | <dl> <span data-ttu-id="29588-144"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="29588-144"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="29588-145">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="29588-145">See also</span></span>

<dl> <dt>

[<span data-ttu-id="29588-146">**\_Service hébergé CIM**</span><span class="sxs-lookup"><span data-stu-id="29588-146">**CIM\_HostedService**</span></span>](cim-hostedservice.md)
</dt> </dl>

 

