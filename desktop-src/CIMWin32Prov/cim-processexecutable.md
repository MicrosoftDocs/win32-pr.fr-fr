---
description: La \_ classe CIM ProcessExecutable représente un lien entre un processus et un fichier de données, et indique que le fichier participe à l’exécution du processus.
ms.assetid: 6db69bf3-b28e-4d0b-8878-558e12052767
ms.tgt_platform: multiple
title: Classe CIM_ProcessExecutable
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_ProcessExecutable
- CIM_ProcessExecutable.Dependent
- CIM_ProcessExecutable.Antecedent
- CIM_ProcessExecutable.BaseAddress
- CIM_ProcessExecutable.GlobalProcessCount
- CIM_ProcessExecutable.ModuleInstance
- CIM_ProcessExecutable.ProcessCount
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: aedb1e79ad842e4cb04746ff47bfab142a536f43
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104033776"
---
# <a name="cim_processexecutable-class"></a><span data-ttu-id="ad177-103">\_Classe CIM ProcessExecutable</span><span class="sxs-lookup"><span data-stu-id="ad177-103">CIM\_ProcessExecutable class</span></span>

<span data-ttu-id="ad177-104">La classe **CIM \_ ProcessExecutable** représente un lien entre un processus et un fichier de données, et indique que le fichier participe à l’exécution du processus.</span><span class="sxs-lookup"><span data-stu-id="ad177-104">The **CIM\_ProcessExecutable** class represents a link between a process and data file, and indicates that the file participates in the execution of the process.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="ad177-105">Les classes de la DMTF (Distributed Management Task Force) CIM (Common Information Model) sont les classes parentes sur lesquelles les classes WMI sont générées.</span><span class="sxs-lookup"><span data-stu-id="ad177-105">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="ad177-106">WMI ne prend actuellement en charge que les [schémas de version CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="ad177-106">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="ad177-107">La syntaxe suivante est simplifiée du code format MOF (MOF) et comprend toutes ses propriétés héritées.</span><span class="sxs-lookup"><span data-stu-id="ad177-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all of its inherited properties.</span></span> <span data-ttu-id="ad177-108">Les propriétés sont répertoriées par ordre alphabétique, et non par ordre MOF.</span><span class="sxs-lookup"><span data-stu-id="ad177-108">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="ad177-109">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="ad177-109">Syntax</span></span>

``` syntax
[Privileges("SeDebugPrivilege"), Dynamic, Provider("CIMWin32"), UUID("{8502C542-5FBB-11D2-AAC1-006008C78BC7}"), AMENDMENT]
class CIM_ProcessExecutable : CIM_Dependency
{
  CIM_Process  REF Dependent;
  CIM_DataFile REF Antecedent;
  uint64           BaseAddress;
  uint32           GlobalProcessCount;
  uint32           ModuleInstance;
  uint32           ProcessCount;
};
```

## <a name="members"></a><span data-ttu-id="ad177-110">Membres</span><span class="sxs-lookup"><span data-stu-id="ad177-110">Members</span></span>

<span data-ttu-id="ad177-111">La classe **CIM \_ ProcessExecutable** possède les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="ad177-111">The **CIM\_ProcessExecutable** class has these types of members:</span></span>

-   [<span data-ttu-id="ad177-112">Propriétés</span><span class="sxs-lookup"><span data-stu-id="ad177-112">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="ad177-113">Propriétés</span><span class="sxs-lookup"><span data-stu-id="ad177-113">Properties</span></span>

<span data-ttu-id="ad177-114">La classe **CIM \_ ProcessExecutable** possède les propriétés suivantes.</span><span class="sxs-lookup"><span data-stu-id="ad177-114">The **CIM\_ProcessExecutable** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="ad177-115">**Antécédent**</span><span class="sxs-lookup"><span data-stu-id="ad177-115">**Antecedent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ad177-116">Type de données **: \_ fichier** de données CIM</span><span class="sxs-lookup"><span data-stu-id="ad177-116">Data type: **CIM\_DataFile**</span></span>
</dt> <dt>

<span data-ttu-id="ad177-117">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="ad177-117">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ad177-118">Qualificateurs : [**override**](/windows/desktop/WmiSdk/standard-qualifiers) (Antecedent), [**Key**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="ad177-118">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) (Antecedent), [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="ad177-119">Un fichier de données CIM qui décrit le fichier de données qui participe à l’exécution du processus. [**\_**](cim-datafile.md)</span><span class="sxs-lookup"><span data-stu-id="ad177-119">A [**CIM\_DataFile**](cim-datafile.md) that describes the data file participating in the execution of the process.</span></span>

</dd> <dt>

<span data-ttu-id="ad177-120">**BaseAddress**</span><span class="sxs-lookup"><span data-stu-id="ad177-120">**BaseAddress**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ad177-121">Type de données : **UInt64**</span><span class="sxs-lookup"><span data-stu-id="ad177-121">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="ad177-122">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="ad177-122">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ad177-123">Qualificateurs : [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span><span class="sxs-lookup"><span data-stu-id="ad177-123">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="ad177-124">Adresse de base du module dans l’espace d’adressage du processus associé.</span><span class="sxs-lookup"><span data-stu-id="ad177-124">Base address of the module in the address space of the associated process.</span></span>

<span data-ttu-id="ad177-125">Pour plus d’informations sur l’utilisation des valeurs **UInt64** dans les scripts, consultez [scripts dans WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span><span class="sxs-lookup"><span data-stu-id="ad177-125">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

</dd> <dt>

<span data-ttu-id="ad177-126">**Charge**</span><span class="sxs-lookup"><span data-stu-id="ad177-126">**Dependent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ad177-127">Type de données **: \_ processus CIM**</span><span class="sxs-lookup"><span data-stu-id="ad177-127">Data type: **CIM\_Process**</span></span>
</dt> <dt>

<span data-ttu-id="ad177-128">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="ad177-128">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ad177-129">Qualificateurs : [**remplacement**](/windows/desktop/WmiSdk/standard-qualifiers) (dépendant), [**clé**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="ad177-129">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) (Dependent), [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="ad177-130">[**\_ Processus CIM**](cim-process.md) qui décrit le processus.</span><span class="sxs-lookup"><span data-stu-id="ad177-130">A [**CIM\_Process**](cim-process.md) that describes the process.</span></span>

</dd> <dt>

<span data-ttu-id="ad177-131">**GlobalProcessCount**</span><span class="sxs-lookup"><span data-stu-id="ad177-131">**GlobalProcessCount**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ad177-132">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="ad177-132">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="ad177-133">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="ad177-133">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ad177-134">Qualificateurs : [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span><span class="sxs-lookup"><span data-stu-id="ad177-134">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="ad177-135">Nombre actuel de processus sur lesquels le fichier est chargé en mémoire.</span><span class="sxs-lookup"><span data-stu-id="ad177-135">Current number of processes that have the file loaded in memory.</span></span>

</dd> <dt>

<span data-ttu-id="ad177-136">**ModuleInstance**</span><span class="sxs-lookup"><span data-stu-id="ad177-136">**ModuleInstance**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ad177-137">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="ad177-137">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="ad177-138">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="ad177-138">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ad177-139">Qualificateurs : [**déconseillé**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**schéma**](/windows/desktop/WmiSdk/standard-qualifiers) (« Win32 »)</span><span class="sxs-lookup"><span data-stu-id="ad177-139">Qualifiers: [**DEPRECATED**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="ad177-140">Handle d’instance Win32.</span><span class="sxs-lookup"><span data-stu-id="ad177-140">Win32 instance handle.</span></span> <span data-ttu-id="ad177-141">Cette propriété est obsolète et il n’y a aucune valeur de remplacement.</span><span class="sxs-lookup"><span data-stu-id="ad177-141">This property is obsolete, and there is no replacement value.</span></span>

</dd> <dt>

<span data-ttu-id="ad177-142">**ProcessCount**</span><span class="sxs-lookup"><span data-stu-id="ad177-142">**ProcessCount**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ad177-143">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="ad177-143">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="ad177-144">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="ad177-144">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ad177-145">Qualificateurs : [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span><span class="sxs-lookup"><span data-stu-id="ad177-145">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="ad177-146">Nombre de références du fichier dans le processus associé.</span><span class="sxs-lookup"><span data-stu-id="ad177-146">Reference count of the file in the associated process.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="ad177-147">Notes</span><span class="sxs-lookup"><span data-stu-id="ad177-147">Remarks</span></span>

<span data-ttu-id="ad177-148">La classe **CIM \_ ProcessExecutable** est dérivée de la [**\_ dépendance CIM**](cim-dependency.md).</span><span class="sxs-lookup"><span data-stu-id="ad177-148">The **CIM\_ProcessExecutable** class is derived from [**CIM\_Dependency**](cim-dependency.md).</span></span>

<span data-ttu-id="ad177-149">WMI implémente la classe **CIM \_ ProcessExecutable** .</span><span class="sxs-lookup"><span data-stu-id="ad177-149">WMI implements the **CIM\_ProcessExecutable** class.</span></span> <span data-ttu-id="ad177-150">La **classe \_ ProcessExecutable CIM** est une classe dynamique.</span><span class="sxs-lookup"><span data-stu-id="ad177-150">The **CIM\_ProcessExecutable** class is a dynamic class.</span></span>

<span data-ttu-id="ad177-151">Cette documentation est dérivée des descriptions de classe CIM publiées par le DMTF.</span><span class="sxs-lookup"><span data-stu-id="ad177-151">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="ad177-152">Microsoft peut avoir apporté des modifications pour corriger les erreurs mineures, se conformer aux normes de documentation du kit de développement logiciel (SDK) Microsoft ou fournir plus d’informations.</span><span class="sxs-lookup"><span data-stu-id="ad177-152">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="ad177-153">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="ad177-153">Requirements</span></span>



| <span data-ttu-id="ad177-154">Condition requise</span><span class="sxs-lookup"><span data-stu-id="ad177-154">Requirement</span></span> | <span data-ttu-id="ad177-155">Valeur</span><span class="sxs-lookup"><span data-stu-id="ad177-155">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="ad177-156">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="ad177-156">Minimum supported client</span></span><br/> | <span data-ttu-id="ad177-157">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="ad177-157">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="ad177-158">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="ad177-158">Minimum supported server</span></span><br/> | <span data-ttu-id="ad177-159">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="ad177-159">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="ad177-160">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="ad177-160">Namespace</span></span><br/>                | <span data-ttu-id="ad177-161">\\Cimv2 racine</span><span class="sxs-lookup"><span data-stu-id="ad177-161">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="ad177-162">MOF</span><span class="sxs-lookup"><span data-stu-id="ad177-162">MOF</span></span><br/>                      | <dl> <span data-ttu-id="ad177-163"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="ad177-163"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="ad177-164">DLL</span><span class="sxs-lookup"><span data-stu-id="ad177-164">DLL</span></span><br/>                      | <dl> <span data-ttu-id="ad177-165"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="ad177-165"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ad177-166">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="ad177-166">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ad177-167">**\_Dépendance CIM**</span><span class="sxs-lookup"><span data-stu-id="ad177-167">**CIM\_Dependency**</span></span>](cim-dependency.md)
</dt> </dl>

 

