---
description: La \_ classe WMI de l’Association DependentService Win32 associe deux services de base interdépendants.
ms.assetid: ba21fce3-f8f9-4886-b09d-a9e830376364
ms.tgt_platform: multiple
title: Classe Win32_DependentService
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_DependentService
- Win32_DependentService.TypeOfDependency
- Win32_DependentService.Antecedent
- Win32_DependentService.Dependent
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 047ec3411186f09f3d0e76da27158aa8ee91d4cc
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104111607"
---
# <a name="win32_dependentservice-class"></a><span data-ttu-id="7e51d-103">\_Classe DependentService Win32</span><span class="sxs-lookup"><span data-stu-id="7e51d-103">Win32\_DependentService class</span></span>

<span data-ttu-id="7e51d-104">La [classe WMI](/windows/desktop/WmiSdk/retrieving-a-class) de l’Association **\_ DependentService Win32** associe deux services de base interdépendants.</span><span class="sxs-lookup"><span data-stu-id="7e51d-104">The **Win32\_DependentService** association [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) relates two interdependent base services.</span></span>

<span data-ttu-id="7e51d-105">La syntaxe suivante est simplifiée par rapport au code MOF (Managed Object Format) et inclut toutes les propriétés héritées.</span><span class="sxs-lookup"><span data-stu-id="7e51d-105">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span> <span data-ttu-id="7e51d-106">Les propriétés sont répertoriées par ordre alphabétique, et non par ordre MOF.</span><span class="sxs-lookup"><span data-stu-id="7e51d-106">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="7e51d-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="7e51d-107">Syntax</span></span>

``` syntax
[Dynamic, Provider("CIMWin32"), UUID("{8502C4FA-5FBB-11D2-AAC1-006008C78BC7}"), AMENDMENT]
class Win32_DependentService : CIM_ServiceServiceDependency
{
  uint16                TypeOfDependency;
  Win32_BaseService REF Antecedent;
  Win32_BaseService REF Dependent;
};
```

## <a name="members"></a><span data-ttu-id="7e51d-108">Membres</span><span class="sxs-lookup"><span data-stu-id="7e51d-108">Members</span></span>

<span data-ttu-id="7e51d-109">La classe **Win32 \_ DependentService** possède les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="7e51d-109">The **Win32\_DependentService** class has these types of members:</span></span>

-   [<span data-ttu-id="7e51d-110">Propriétés</span><span class="sxs-lookup"><span data-stu-id="7e51d-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="7e51d-111">Propriétés</span><span class="sxs-lookup"><span data-stu-id="7e51d-111">Properties</span></span>

<span data-ttu-id="7e51d-112">La classe **Win32 \_ DependentService** a ces propriétés.</span><span class="sxs-lookup"><span data-stu-id="7e51d-112">The **Win32\_DependentService** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="7e51d-113">**Antécédent**</span><span class="sxs-lookup"><span data-stu-id="7e51d-113">**Antecedent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7e51d-114">Type de données : **Win32 \_ BaseService**</span><span class="sxs-lookup"><span data-stu-id="7e51d-114">Data type: **Win32\_BaseService**</span></span>
</dt> <dt>

<span data-ttu-id="7e51d-115">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="7e51d-115">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="7e51d-116">Qualificateurs : [**clé**](/windows/desktop/WmiSdk/key-qualifier), [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Antecedent"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("WMI \| Win32 \_ BaseService")</span><span class="sxs-lookup"><span data-stu-id="7e51d-116">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier), [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Antecedent"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("WMI\|Win32\_BaseService")</span></span>
</dt> </dl>

<span data-ttu-id="7e51d-117">[**\_ BaseService Win32**](win32-baseservice.md) qui représente le service de base reposant sur la propriété **dépendante** de cette classe.</span><span class="sxs-lookup"><span data-stu-id="7e51d-117">A [**Win32\_BaseService**](win32-baseservice.md) representing the base service relied upon by the **Dependent** property of this class.</span></span>

</dd> <dt>

<span data-ttu-id="7e51d-118">**Charge**</span><span class="sxs-lookup"><span data-stu-id="7e51d-118">**Dependent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7e51d-119">Type de données : **Win32 \_ BaseService**</span><span class="sxs-lookup"><span data-stu-id="7e51d-119">Data type: **Win32\_BaseService**</span></span>
</dt> <dt>

<span data-ttu-id="7e51d-120">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="7e51d-120">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="7e51d-121">Qualificateurs : [**clé**](/windows/desktop/WmiSdk/key-qualifier), [**remplacement**](/windows/desktop/WmiSdk/standard-qualifiers) (« dépendant »), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) (« WMI \| Win32 \_ BaseService »)</span><span class="sxs-lookup"><span data-stu-id="7e51d-121">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier), [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Dependent"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("WMI\|Win32\_BaseService")</span></span>
</dt> </dl>

<span data-ttu-id="7e51d-122">[**\_ BaseService Win32**](win32-baseservice.md) représentant le service de base qui est dépendant de la propriété **Antecedent** de cette classe.</span><span class="sxs-lookup"><span data-stu-id="7e51d-122">A [**Win32\_BaseService**](win32-baseservice.md) representing the base service that is dependent on the **Antecedent** property of this class.</span></span>

</dd> <dt>

<span data-ttu-id="7e51d-123">**TypeOfDependency**</span><span class="sxs-lookup"><span data-stu-id="7e51d-123">**TypeOfDependency**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7e51d-124">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="7e51d-124">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="7e51d-125">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="7e51d-125">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="7e51d-126">Nature de la dépendance de service à service.</span><span class="sxs-lookup"><span data-stu-id="7e51d-126">Nature of the service-to-service dependency.</span></span> <span data-ttu-id="7e51d-127">Cette propriété indique que le service associé doit avoir terminé, qu’il doit être démarré ou qu’il ne doit pas être démarré pour que le service fonctionne.</span><span class="sxs-lookup"><span data-stu-id="7e51d-127">This property indicates that the associated service must have completed, must be started, or must not be started for the service to function.</span></span>

<span data-ttu-id="7e51d-128">Cette propriété est héritée de la [**\_ ServiceServiceDependency CIM**](cim-serviceservicedependency.md).</span><span class="sxs-lookup"><span data-stu-id="7e51d-128">This property is inherited from [**CIM\_ServiceServiceDependency**](cim-serviceservicedependency.md).</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="7e51d-129"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Inconnu** (0)</span><span class="sxs-lookup"><span data-stu-id="7e51d-129"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="7e51d-130"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Autre** (1)</span><span class="sxs-lookup"><span data-stu-id="7e51d-130"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Service_Must_Have_Completed"></span><span id="service_must_have_completed"></span><span id="SERVICE_MUST_HAVE_COMPLETED"></span>

<span data-ttu-id="7e51d-131"><span id="Service_Must_Have_Completed"></span><span id="service_must_have_completed"></span><span id="SERVICE_MUST_HAVE_COMPLETED"></span>Le **service doit avoir terminé** (2)</span><span class="sxs-lookup"><span data-stu-id="7e51d-131"><span id="Service_Must_Have_Completed"></span><span id="service_must_have_completed"></span><span id="SERVICE_MUST_HAVE_COMPLETED"></span>**Service Must Have Completed** (2)</span></span>


</dt> <dd>

<span data-ttu-id="7e51d-132">Le service doit être terminé.</span><span class="sxs-lookup"><span data-stu-id="7e51d-132">Service must have completed.</span></span>

</dd> <dt>

<span id="Service_Must_Be_Started"></span><span id="service_must_be_started"></span><span id="SERVICE_MUST_BE_STARTED"></span>

<span data-ttu-id="7e51d-133"><span id="Service_Must_Be_Started"></span><span id="service_must_be_started"></span><span id="SERVICE_MUST_BE_STARTED"></span>Le **service doit être démarré** (3)</span><span class="sxs-lookup"><span data-stu-id="7e51d-133"><span id="Service_Must_Be_Started"></span><span id="service_must_be_started"></span><span id="SERVICE_MUST_BE_STARTED"></span>**Service Must Be Started** (3)</span></span>


</dt> <dd>

<span data-ttu-id="7e51d-134">Le service doit être démarré.</span><span class="sxs-lookup"><span data-stu-id="7e51d-134">Service must be started.</span></span>

</dd> <dt>

<span id="Service_Must_Not_Be_Started"></span><span id="service_must_not_be_started"></span><span id="SERVICE_MUST_NOT_BE_STARTED"></span>

<span data-ttu-id="7e51d-135"><span id="Service_Must_Not_Be_Started"></span><span id="service_must_not_be_started"></span><span id="SERVICE_MUST_NOT_BE_STARTED"></span>Le **service ne doit pas être démarré** (4)</span><span class="sxs-lookup"><span data-stu-id="7e51d-135"><span id="Service_Must_Not_Be_Started"></span><span id="service_must_not_be_started"></span><span id="SERVICE_MUST_NOT_BE_STARTED"></span>**Service Must Not Be Started** (4)</span></span>


</dt> <dd>

<span data-ttu-id="7e51d-136">Le service ne doit pas être démarré.</span><span class="sxs-lookup"><span data-stu-id="7e51d-136">Service must not be started.</span></span>

</dd> </dl>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="7e51d-137">Notes</span><span class="sxs-lookup"><span data-stu-id="7e51d-137">Remarks</span></span>

<span data-ttu-id="7e51d-138">La classe **Win32 \_ DependentService** est dérivée de [**CIM \_ ServiceServiceDependency**](cim-serviceservicedependency.md).</span><span class="sxs-lookup"><span data-stu-id="7e51d-138">The **Win32\_DependentService** class is derived from [**CIM\_ServiceServiceDependency**](cim-serviceservicedependency.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="7e51d-139">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="7e51d-139">Requirements</span></span>



| <span data-ttu-id="7e51d-140">Condition requise</span><span class="sxs-lookup"><span data-stu-id="7e51d-140">Requirement</span></span> | <span data-ttu-id="7e51d-141">Valeur</span><span class="sxs-lookup"><span data-stu-id="7e51d-141">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="7e51d-142">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="7e51d-142">Minimum supported client</span></span><br/> | <span data-ttu-id="7e51d-143">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="7e51d-143">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="7e51d-144">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="7e51d-144">Minimum supported server</span></span><br/> | <span data-ttu-id="7e51d-145">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="7e51d-145">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="7e51d-146">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="7e51d-146">Namespace</span></span><br/>                | <span data-ttu-id="7e51d-147">\\Cimv2 racine</span><span class="sxs-lookup"><span data-stu-id="7e51d-147">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="7e51d-148">MOF</span><span class="sxs-lookup"><span data-stu-id="7e51d-148">MOF</span></span><br/>                      | <dl> <span data-ttu-id="7e51d-149"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="7e51d-149"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="7e51d-150">DLL</span><span class="sxs-lookup"><span data-stu-id="7e51d-150">DLL</span></span><br/>                      | <dl> <span data-ttu-id="7e51d-151"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="7e51d-151"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7e51d-152">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="7e51d-152">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7e51d-153">**\_SERVICESERVICEDEPENDENCY CIM**</span><span class="sxs-lookup"><span data-stu-id="7e51d-153">**CIM\_ServiceServiceDependency**</span></span>](cim-serviceservicedependency.md)
</dt> <dt>

<span data-ttu-id="7e51d-154">[Classes du système d’exploitation](/previous-versions//aa392727(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="7e51d-154">[Operating System Classes](/previous-versions//aa392727(v=vs.85))</span></span>
</dt> </dl>

 

