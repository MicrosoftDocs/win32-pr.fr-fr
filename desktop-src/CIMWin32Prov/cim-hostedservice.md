---
description: La \_ classe CIM service hébergé représente une association entre un service et le système sur lequel la fonctionnalité réside.
ms.assetid: 23bb385d-dd22-4126-aea9-d2f22527223e
ms.tgt_platform: multiple
title: CIM_HostedService, classe (fournisseurs WMI CIMWin32)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_HostedService
- CIM_HostedService.Dependent
- CIM_HostedService.Antecedent
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: c63b28fed7977c9fce78fe1030afbe66d5b2d75e
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106514535"
---
# <a name="cim_hostedservice-class-cimwin32-wmi-providers"></a><span data-ttu-id="a43e8-103">CIM_HostedService, classe (fournisseurs WMI CIMWin32)</span><span class="sxs-lookup"><span data-stu-id="a43e8-103">CIM_HostedService class (CIMWin32 WMI Providers)</span></span>

<span data-ttu-id="a43e8-104">La classe **CIM \_ service hébergé** représente une association entre un service et le système sur lequel la fonctionnalité réside.</span><span class="sxs-lookup"><span data-stu-id="a43e8-104">The **CIM\_HostedService** class represents an association between a service and the system on which the functionality resides.</span></span> <span data-ttu-id="a43e8-105">Un système peut héberger de nombreux services, qui retardent le système d’hébergement.</span><span class="sxs-lookup"><span data-stu-id="a43e8-105">A system may host many services, which defer to the hosting system.</span></span> <span data-ttu-id="a43e8-106">Le modèle ne représente pas les services hébergés sur plusieurs systèmes.</span><span class="sxs-lookup"><span data-stu-id="a43e8-106">The model does not represent services hosted across multiple systems.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="a43e8-107">Les classes de la DMTF (Distributed Management Task Force) CIM (Common Information Model) sont les classes parentes sur lesquelles les classes WMI sont générées.</span><span class="sxs-lookup"><span data-stu-id="a43e8-107">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="a43e8-108">WMI ne prend actuellement en charge que les [schémas de version CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="a43e8-108">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="a43e8-109">La syntaxe suivante est simplifiée à partir de code au format MOF (Managed Object Format) et inclut toutes les propriétés héritées.</span><span class="sxs-lookup"><span data-stu-id="a43e8-109">The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.</span></span> <span data-ttu-id="a43e8-110">Les propriétés sont répertoriées par ordre alphabétique, et non par ordre MOF.</span><span class="sxs-lookup"><span data-stu-id="a43e8-110">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="a43e8-111">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="a43e8-111">Syntax</span></span>

``` syntax
[Abstract, UUID("{83B2A7AA-DB36-11d2-85FC-0000F8102E5F}"), AMENDMENT]
class CIM_HostedService : CIM_Dependency
{
  CIM_Service REF Dependent;
  CIM_System  REF Antecedent;
};
```

## <a name="members"></a><span data-ttu-id="a43e8-112">Membres</span><span class="sxs-lookup"><span data-stu-id="a43e8-112">Members</span></span>

<span data-ttu-id="a43e8-113">La classe **CIM \_ service hébergé** possède les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="a43e8-113">The **CIM\_HostedService** class has these types of members:</span></span>

-   [<span data-ttu-id="a43e8-114">Propriétés</span><span class="sxs-lookup"><span data-stu-id="a43e8-114">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="a43e8-115">Propriétés</span><span class="sxs-lookup"><span data-stu-id="a43e8-115">Properties</span></span>

<span data-ttu-id="a43e8-116">La classe **CIM \_ service hébergé** possède les propriétés suivantes.</span><span class="sxs-lookup"><span data-stu-id="a43e8-116">The **CIM\_HostedService** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="a43e8-117">**Antécédent**</span><span class="sxs-lookup"><span data-stu-id="a43e8-117">**Antecedent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a43e8-118">Type de données **: \_ système CIM**</span><span class="sxs-lookup"><span data-stu-id="a43e8-118">Data type: **CIM\_System**</span></span>
</dt> <dt>

<span data-ttu-id="a43e8-119">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="a43e8-119">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a43e8-120">Qualificateurs : [**Max**](/windows/desktop/WmiSdk/standard-qualifiers) (1), [**min**](/windows/desktop/WmiSdk/standard-qualifiers) (1), [**override**](/windows/desktop/WmiSdk/standard-qualifiers) (« Antecedent »)</span><span class="sxs-lookup"><span data-stu-id="a43e8-120">Qualifiers: [**Max**](/windows/desktop/WmiSdk/standard-qualifiers) (1), [**Min**](/windows/desktop/WmiSdk/standard-qualifiers) (1), [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Antecedent")</span></span>
</dt> </dl>

<span data-ttu-id="a43e8-121">[**\_ Système CIM**](cim-system.md) qui décrit le système d’hébergement.</span><span class="sxs-lookup"><span data-stu-id="a43e8-121">A [**CIM\_System**](cim-system.md) that describes the hosting system.</span></span>

</dd> <dt>

<span data-ttu-id="a43e8-122">**Charge**</span><span class="sxs-lookup"><span data-stu-id="a43e8-122">**Dependent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a43e8-123">Type de données **: \_ service CIM**</span><span class="sxs-lookup"><span data-stu-id="a43e8-123">Data type: **CIM\_Service**</span></span>
</dt> <dt>

<span data-ttu-id="a43e8-124">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="a43e8-124">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a43e8-125">Qualificateurs : [**override**](/windows/desktop/WmiSdk/standard-qualifiers) (« Dependent »), [**Weak**](/windows/desktop/WmiSdk/standard-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="a43e8-125">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Dependent"), [**Weak**](/windows/desktop/WmiSdk/standard-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="a43e8-126">[**\_ Service CIM**](cim-service.md) qui décrit le service hébergé sur le système.</span><span class="sxs-lookup"><span data-stu-id="a43e8-126">A [**CIM\_Service**](cim-service.md) that describes the service hosted on the system.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="a43e8-127">Notes</span><span class="sxs-lookup"><span data-stu-id="a43e8-127">Remarks</span></span>

<span data-ttu-id="a43e8-128">**CIM \_ Service hébergé** est dérivé de [**la \_ dépendance CIM**](cim-dependency.md).</span><span class="sxs-lookup"><span data-stu-id="a43e8-128">**CIM\_HostedService** is derived from [**CIM\_Dependency**](cim-dependency.md).</span></span>

<span data-ttu-id="a43e8-129">WMI n’implémente pas cette classe.</span><span class="sxs-lookup"><span data-stu-id="a43e8-129">WMI does not implement this class.</span></span>

<span data-ttu-id="a43e8-130">Cette documentation est dérivée des descriptions de classe CIM publiées par le DMTF.</span><span class="sxs-lookup"><span data-stu-id="a43e8-130">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="a43e8-131">Microsoft peut avoir apporté des modifications pour corriger les erreurs mineures, se conformer aux normes de documentation du kit de développement logiciel (SDK) Microsoft ou fournir plus d’informations.</span><span class="sxs-lookup"><span data-stu-id="a43e8-131">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="a43e8-132">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="a43e8-132">Requirements</span></span>



| <span data-ttu-id="a43e8-133">Condition requise</span><span class="sxs-lookup"><span data-stu-id="a43e8-133">Requirement</span></span> | <span data-ttu-id="a43e8-134">Valeur</span><span class="sxs-lookup"><span data-stu-id="a43e8-134">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="a43e8-135">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="a43e8-135">Minimum supported client</span></span><br/> | <span data-ttu-id="a43e8-136">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="a43e8-136">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="a43e8-137">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="a43e8-137">Minimum supported server</span></span><br/> | <span data-ttu-id="a43e8-138">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="a43e8-138">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="a43e8-139">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="a43e8-139">Namespace</span></span><br/>                | <span data-ttu-id="a43e8-140">\\Cimv2 racine</span><span class="sxs-lookup"><span data-stu-id="a43e8-140">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="a43e8-141">MOF</span><span class="sxs-lookup"><span data-stu-id="a43e8-141">MOF</span></span><br/>                      | <dl> <span data-ttu-id="a43e8-142"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="a43e8-142"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="a43e8-143">DLL</span><span class="sxs-lookup"><span data-stu-id="a43e8-143">DLL</span></span><br/>                      | <dl> <span data-ttu-id="a43e8-144"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="a43e8-144"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a43e8-145">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="a43e8-145">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a43e8-146">**\_Dépendance CIM**</span><span class="sxs-lookup"><span data-stu-id="a43e8-146">**CIM\_Dependency**</span></span>](cim-dependency.md)
</dt> </dl>

 

