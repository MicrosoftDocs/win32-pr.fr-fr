---
description: La \_ classe CIM ServiceServiceDependency représente une association entre deux services.
ms.assetid: 0fb43fb3-2c05-4762-b339-2dcc090ed38d
ms.tgt_platform: multiple
title: Classe CIM_ServiceServiceDependency
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_ServiceServiceDependency
- CIM_ServiceServiceDependency.Dependent
- CIM_ServiceServiceDependency.Antecedent
- CIM_ServiceServiceDependency.TypeOfDependency
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: fdc8ea1a3324395e5230ca6d47487b61c8c02ba9
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106514742"
---
# <a name="cim_serviceservicedependency-class"></a><span data-ttu-id="8257c-103">\_Classe CIM ServiceServiceDependency</span><span class="sxs-lookup"><span data-stu-id="8257c-103">CIM\_ServiceServiceDependency class</span></span>

<span data-ttu-id="8257c-104">La classe **CIM \_ ServiceServiceDependency** représente une association entre deux services.</span><span class="sxs-lookup"><span data-stu-id="8257c-104">The **CIM\_ServiceServiceDependency** class represents an association between two services.</span></span> <span data-ttu-id="8257c-105">Le service associé doit être présent, doit être terminé, ou il doit être absent pour que l’autre service fonctionne.</span><span class="sxs-lookup"><span data-stu-id="8257c-105">The associated service must be present, must have completed, or must be absent for the other service to function.</span></span> <span data-ttu-id="8257c-106">Par exemple, les services de démarrage peuvent dépendre du BIOS, du disque et des services d’initialisation sous-jacents.</span><span class="sxs-lookup"><span data-stu-id="8257c-106">For example, boot services can be dependent on underlying BIOS, disk, and initialization services.</span></span> <span data-ttu-id="8257c-107">Pour les services d’initialisation, le service de démarrage dépend des services d’initialisation en cours d’exécution.</span><span class="sxs-lookup"><span data-stu-id="8257c-107">For initialization services, the boot service is dependent on the initialization services completing.</span></span> <span data-ttu-id="8257c-108">Pour les services de disque, les services de démarrage peuvent réellement utiliser les SAP de ce service.</span><span class="sxs-lookup"><span data-stu-id="8257c-108">For disk services, boot services can actually use the SAPs of this service.</span></span> <span data-ttu-id="8257c-109">Cette dépendance d’utilisation est modélisée sur l’Association [**CIM \_ ServiceSAPDependency**](cim-servicesapdependency.md) .</span><span class="sxs-lookup"><span data-stu-id="8257c-109">This usage dependency is modeled on the [**CIM\_ServiceSAPDependency**](cim-servicesapdependency.md) association.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="8257c-110">Les classes de la DMTF (Distributed Management Task Force) CIM (Common Information Model) sont les classes parentes sur lesquelles les classes WMI sont générées.</span><span class="sxs-lookup"><span data-stu-id="8257c-110">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="8257c-111">WMI ne prend actuellement en charge que les [schémas de version CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="8257c-111">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="8257c-112">La syntaxe suivante est simplifiée à partir de code au format MOF (Managed Object Format) et inclut toutes les propriétés héritées.</span><span class="sxs-lookup"><span data-stu-id="8257c-112">The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.</span></span> <span data-ttu-id="8257c-113">Les propriétés sont répertoriées par ordre alphabétique, et non par ordre MOF.</span><span class="sxs-lookup"><span data-stu-id="8257c-113">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="8257c-114">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="8257c-114">Syntax</span></span>

``` syntax
[Abstract, UUID("{8502C53B-5FBB-11D2-AAC1-006008C78BC7}"), AMENDMENT]
class CIM_ServiceServiceDependency : CIM_Dependency
{
  CIM_Service REF Dependent;
  CIM_Service REF Antecedent;
  uint16          TypeOfDependency;
};
```

## <a name="members"></a><span data-ttu-id="8257c-115">Membres</span><span class="sxs-lookup"><span data-stu-id="8257c-115">Members</span></span>

<span data-ttu-id="8257c-116">La classe **CIM \_ ServiceServiceDependency** possède les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="8257c-116">The **CIM\_ServiceServiceDependency** class has these types of members:</span></span>

-   [<span data-ttu-id="8257c-117">Propriétés</span><span class="sxs-lookup"><span data-stu-id="8257c-117">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="8257c-118">Propriétés</span><span class="sxs-lookup"><span data-stu-id="8257c-118">Properties</span></span>

<span data-ttu-id="8257c-119">La classe **CIM \_ ServiceServiceDependency** possède les propriétés suivantes.</span><span class="sxs-lookup"><span data-stu-id="8257c-119">The **CIM\_ServiceServiceDependency** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="8257c-120">**Antécédent**</span><span class="sxs-lookup"><span data-stu-id="8257c-120">**Antecedent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8257c-121">Type de données **: \_ service CIM**</span><span class="sxs-lookup"><span data-stu-id="8257c-121">Data type: **CIM\_Service**</span></span>
</dt> <dt>

<span data-ttu-id="8257c-122">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="8257c-122">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="8257c-123">Qualificateurs : [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Antecedent")</span><span class="sxs-lookup"><span data-stu-id="8257c-123">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Antecedent")</span></span>
</dt> </dl>

<span data-ttu-id="8257c-124">[**\_ Service CIM**](cim-service.md) qui décrit le service requis.</span><span class="sxs-lookup"><span data-stu-id="8257c-124">A [**CIM\_Service**](cim-service.md) that describes the required service.</span></span>

</dd> <dt>

<span data-ttu-id="8257c-125">**Charge**</span><span class="sxs-lookup"><span data-stu-id="8257c-125">**Dependent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8257c-126">Type de données **: \_ service CIM**</span><span class="sxs-lookup"><span data-stu-id="8257c-126">Data type: **CIM\_Service**</span></span>
</dt> <dt>

<span data-ttu-id="8257c-127">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="8257c-127">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="8257c-128">Qualificateurs : [**override**](/windows/desktop/WmiSdk/standard-qualifiers) (« Dependent »)</span><span class="sxs-lookup"><span data-stu-id="8257c-128">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Dependent")</span></span>
</dt> </dl>

<span data-ttu-id="8257c-129">[**\_ Service CIM**](cim-service.md) qui décrit le service qui dépend d’un service sous-jacent.</span><span class="sxs-lookup"><span data-stu-id="8257c-129">A [**CIM\_Service**](cim-service.md) that describes the service that is dependent on an underlying service.</span></span>

</dd> <dt>

<span data-ttu-id="8257c-130">**TypeOfDependency**</span><span class="sxs-lookup"><span data-stu-id="8257c-130">**TypeOfDependency**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8257c-131">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="8257c-131">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="8257c-132">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="8257c-132">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="8257c-133">Nature de la dépendance de service à service.</span><span class="sxs-lookup"><span data-stu-id="8257c-133">Nature of the service-to-service dependency.</span></span> <span data-ttu-id="8257c-134">Cette propriété indique que le service associé doit avoir terminé, qu’il doit être démarré ou qu’il ne doit pas être démarré pour que le service fonctionne.</span><span class="sxs-lookup"><span data-stu-id="8257c-134">This property indicates that the associated service must have completed, must be started, or must not be started for the service to function.</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="8257c-135"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Inconnu** (0)</span><span class="sxs-lookup"><span data-stu-id="8257c-135"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="8257c-136"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Autre** (1)</span><span class="sxs-lookup"><span data-stu-id="8257c-136"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Service_Must_Have_Completed"></span><span id="service_must_have_completed"></span><span id="SERVICE_MUST_HAVE_COMPLETED"></span>

<span data-ttu-id="8257c-137"><span id="Service_Must_Have_Completed"></span><span id="service_must_have_completed"></span><span id="SERVICE_MUST_HAVE_COMPLETED"></span>Le **service doit avoir terminé** (2)</span><span class="sxs-lookup"><span data-stu-id="8257c-137"><span id="Service_Must_Have_Completed"></span><span id="service_must_have_completed"></span><span id="SERVICE_MUST_HAVE_COMPLETED"></span>**Service Must Have Completed** (2)</span></span>


</dt> <dd>

<span data-ttu-id="8257c-138">Le service doit être terminé.</span><span class="sxs-lookup"><span data-stu-id="8257c-138">Service must have completed.</span></span>

</dd> <dt>

<span id="Service_Must_Be_Started"></span><span id="service_must_be_started"></span><span id="SERVICE_MUST_BE_STARTED"></span>

<span data-ttu-id="8257c-139"><span id="Service_Must_Be_Started"></span><span id="service_must_be_started"></span><span id="SERVICE_MUST_BE_STARTED"></span>Le **service doit être démarré** (3)</span><span class="sxs-lookup"><span data-stu-id="8257c-139"><span id="Service_Must_Be_Started"></span><span id="service_must_be_started"></span><span id="SERVICE_MUST_BE_STARTED"></span>**Service Must Be Started** (3)</span></span>


</dt> <dd>

<span data-ttu-id="8257c-140">Le service doit être démarré.</span><span class="sxs-lookup"><span data-stu-id="8257c-140">Service must be started.</span></span>

</dd> <dt>

<span id="Service_Must_Not_Be_Started"></span><span id="service_must_not_be_started"></span><span id="SERVICE_MUST_NOT_BE_STARTED"></span>

<span data-ttu-id="8257c-141"><span id="Service_Must_Not_Be_Started"></span><span id="service_must_not_be_started"></span><span id="SERVICE_MUST_NOT_BE_STARTED"></span>Le **service ne doit pas être démarré** (4)</span><span class="sxs-lookup"><span data-stu-id="8257c-141"><span id="Service_Must_Not_Be_Started"></span><span id="service_must_not_be_started"></span><span id="SERVICE_MUST_NOT_BE_STARTED"></span>**Service Must Not Be Started** (4)</span></span>


</dt> <dd>

<span data-ttu-id="8257c-142">Le service ne doit pas être démarré.</span><span class="sxs-lookup"><span data-stu-id="8257c-142">Service must not be started.</span></span>

</dd> </dl>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="8257c-143">Notes</span><span class="sxs-lookup"><span data-stu-id="8257c-143">Remarks</span></span>

<span data-ttu-id="8257c-144">WMI n’implémente pas cette classe.</span><span class="sxs-lookup"><span data-stu-id="8257c-144">WMI does not implement this class.</span></span> <span data-ttu-id="8257c-145">Pour les classes WMI dérivées de **CIM \_ ServiceServiceDependency**, consultez [classes Win32](win32-provider.md).</span><span class="sxs-lookup"><span data-stu-id="8257c-145">For WMI classes derived from **CIM\_ServiceServiceDependency**, see [Win32 Classes](win32-provider.md).</span></span>

<span data-ttu-id="8257c-146">La classe **CIM \_ ServiceServiceDependency** est dérivée de la [**\_ dépendance CIM**](cim-dependency.md).</span><span class="sxs-lookup"><span data-stu-id="8257c-146">The **CIM\_ServiceServiceDependency** class is derived from [**CIM\_Dependency**](cim-dependency.md).</span></span>

<span data-ttu-id="8257c-147">Cette documentation est dérivée des descriptions de classe CIM publiées par le DMTF.</span><span class="sxs-lookup"><span data-stu-id="8257c-147">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="8257c-148">Microsoft peut avoir apporté des modifications pour corriger les erreurs mineures, se conformer aux normes de documentation du kit de développement logiciel (SDK) Microsoft ou fournir plus d’informations.</span><span class="sxs-lookup"><span data-stu-id="8257c-148">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="8257c-149">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="8257c-149">Requirements</span></span>



| <span data-ttu-id="8257c-150">Condition requise</span><span class="sxs-lookup"><span data-stu-id="8257c-150">Requirement</span></span> | <span data-ttu-id="8257c-151">Valeur</span><span class="sxs-lookup"><span data-stu-id="8257c-151">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="8257c-152">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="8257c-152">Minimum supported client</span></span><br/> | <span data-ttu-id="8257c-153">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="8257c-153">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="8257c-154">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="8257c-154">Minimum supported server</span></span><br/> | <span data-ttu-id="8257c-155">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="8257c-155">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="8257c-156">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="8257c-156">Namespace</span></span><br/>                | <span data-ttu-id="8257c-157">\\Cimv2 racine</span><span class="sxs-lookup"><span data-stu-id="8257c-157">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="8257c-158">MOF</span><span class="sxs-lookup"><span data-stu-id="8257c-158">MOF</span></span><br/>                      | <dl> <span data-ttu-id="8257c-159"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="8257c-159"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="8257c-160">DLL</span><span class="sxs-lookup"><span data-stu-id="8257c-160">DLL</span></span><br/>                      | <dl> <span data-ttu-id="8257c-161"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="8257c-161"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8257c-162">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="8257c-162">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8257c-163">**\_Dépendance CIM**</span><span class="sxs-lookup"><span data-stu-id="8257c-163">**CIM\_Dependency**</span></span>](cim-dependency.md)
</dt> </dl>

 

