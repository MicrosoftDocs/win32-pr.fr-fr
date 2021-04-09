---
description: L' \_ Association CIM PackageAlarm représente la relation dans laquelle un appareil d’alarme est installé dans le cadre d’un package. L’installation indique des problèmes avec l’environnement du package&\# 8212 ; son état de sécurité ou son intégrité globale.
ms.assetid: 4911502a-de9c-46b4-91f6-a042c69fd052
ms.tgt_platform: multiple
title: Classe CIM_PackageAlarm
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_PackageAlarm
- CIM_PackageAlarm.Dependent
- CIM_PackageAlarm.Antecedent
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 29aae3a2c1093e026356ea7a096f8b673673f67d
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104110263"
---
# <a name="cim_packagealarm-class"></a><span data-ttu-id="b51b9-104">\_Classe CIM PackageAlarm</span><span class="sxs-lookup"><span data-stu-id="b51b9-104">CIM\_PackageAlarm class</span></span>

<span data-ttu-id="b51b9-105">L’Association [**CIM \_ PackageAlarm**](/windows/desktop/SecCrypto/extendedproperties-newenum) représente la relation dans laquelle un appareil d’alarme est installé dans le cadre d’un package.</span><span class="sxs-lookup"><span data-stu-id="b51b9-105">The [**CIM\_PackageAlarm**](/windows/desktop/SecCrypto/extendedproperties-newenum) association represents the relationship in which an alarm device is installed as part of a package.</span></span> <span data-ttu-id="b51b9-106">L’installation indique des problèmes liés à l’état de sécurité de l’environnement du package ou à son état d’intégrité global.</span><span class="sxs-lookup"><span data-stu-id="b51b9-106">The installation indicates issues with the package's environment its security state or its overall health.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="b51b9-107">Les classes de la DMTF (Distributed Management Task Force) CIM (Common Information Model) sont les classes parentes sur lesquelles les classes WMI sont générées.</span><span class="sxs-lookup"><span data-stu-id="b51b9-107">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="b51b9-108">WMI ne prend actuellement en charge que les [schémas de version CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="b51b9-108">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="b51b9-109">La syntaxe suivante est simplifiée du code format MOF (MOF) et comprend toutes ses propriétés héritées.</span><span class="sxs-lookup"><span data-stu-id="b51b9-109">The following syntax is simplified from Managed Object Format (MOF) code and includes all of its inherited properties.</span></span> <span data-ttu-id="b51b9-110">Les propriétés sont répertoriées par ordre alphabétique, et non par ordre MOF.</span><span class="sxs-lookup"><span data-stu-id="b51b9-110">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="b51b9-111">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="b51b9-111">Syntax</span></span>

``` syntax
[Abstract, Aggregation, UUID("{FAF76B90-798C-11D2-AAD1-006008C78BC7}"), AMENDMENT]
class CIM_PackageAlarm : CIM_Dependency
{
  CIM_PhysicalPackage REF Dependent;
  CIM_AlarmDevice     REF Antecedent;
};
```

## <a name="members"></a><span data-ttu-id="b51b9-112">Membres</span><span class="sxs-lookup"><span data-stu-id="b51b9-112">Members</span></span>

<span data-ttu-id="b51b9-113">La classe **CIM \_ PackageAlarm** possède les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="b51b9-113">The **CIM\_PackageAlarm** class has these types of members:</span></span>

-   [<span data-ttu-id="b51b9-114">Propriétés</span><span class="sxs-lookup"><span data-stu-id="b51b9-114">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="b51b9-115">Propriétés</span><span class="sxs-lookup"><span data-stu-id="b51b9-115">Properties</span></span>

<span data-ttu-id="b51b9-116">La classe **CIM \_ PackageAlarm** possède les propriétés suivantes.</span><span class="sxs-lookup"><span data-stu-id="b51b9-116">The **CIM\_PackageAlarm** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="b51b9-117">**Antécédent**</span><span class="sxs-lookup"><span data-stu-id="b51b9-117">**Antecedent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b51b9-118">Type de données : **CIM \_ AlarmDevice**</span><span class="sxs-lookup"><span data-stu-id="b51b9-118">Data type: **CIM\_AlarmDevice**</span></span>
</dt> <dt>

<span data-ttu-id="b51b9-119">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="b51b9-119">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b51b9-120">Qualificateurs : [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Antecedent")</span><span class="sxs-lookup"><span data-stu-id="b51b9-120">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Antecedent")</span></span>
</dt> </dl>

<span data-ttu-id="b51b9-121">[**\_ AlarmDevice CIM**](cim-alarmdevice.md) qui décrit l’appareil d’alarme pour le package.</span><span class="sxs-lookup"><span data-stu-id="b51b9-121">A [**CIM\_AlarmDevice**](cim-alarmdevice.md) that describes the alarm device for the package.</span></span>

</dd> <dt>

<span data-ttu-id="b51b9-122">**Charge**</span><span class="sxs-lookup"><span data-stu-id="b51b9-122">**Dependent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b51b9-123">Type de données : **CIM \_ PhysicalPackage**</span><span class="sxs-lookup"><span data-stu-id="b51b9-123">Data type: **CIM\_PhysicalPackage**</span></span>
</dt> <dt>

<span data-ttu-id="b51b9-124">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="b51b9-124">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b51b9-125">Qualificateurs : [**override**](/windows/desktop/WmiSdk/standard-qualifiers) (« Dependent »)</span><span class="sxs-lookup"><span data-stu-id="b51b9-125">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Dependent")</span></span>
</dt> </dl>

<span data-ttu-id="b51b9-126">[**\_ PhysicalPackage CIM**](cim-physicalpackage.md) décrivant le package physique dont l’intégrité, la sécurité, l’environnement, etc. sont alarmements.</span><span class="sxs-lookup"><span data-stu-id="b51b9-126">A [**CIM\_PhysicalPackage**](cim-physicalpackage.md) describing the physical package whose health, security, environment, etc. is alarmed.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="b51b9-127">Notes</span><span class="sxs-lookup"><span data-stu-id="b51b9-127">Remarks</span></span>

<span data-ttu-id="b51b9-128">**CIM \_ PackageAlarm** est dérivé de [**la \_ dépendance CIM**](cim-dependency.md).</span><span class="sxs-lookup"><span data-stu-id="b51b9-128">**CIM\_PackageAlarm** is derived from [**CIM\_Dependency**](cim-dependency.md).</span></span>

<span data-ttu-id="b51b9-129">WMI n’implémente pas cette classe.</span><span class="sxs-lookup"><span data-stu-id="b51b9-129">WMI does not implement this class.</span></span>

<span data-ttu-id="b51b9-130">Cette documentation est dérivée des descriptions de classe CIM publiées par le DMTF.</span><span class="sxs-lookup"><span data-stu-id="b51b9-130">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="b51b9-131">Microsoft peut avoir apporté des modifications pour corriger les erreurs mineures, se conformer aux normes de documentation du kit de développement logiciel (SDK) Microsoft ou fournir plus d’informations.</span><span class="sxs-lookup"><span data-stu-id="b51b9-131">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="b51b9-132">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="b51b9-132">Requirements</span></span>



| <span data-ttu-id="b51b9-133">Condition requise</span><span class="sxs-lookup"><span data-stu-id="b51b9-133">Requirement</span></span> | <span data-ttu-id="b51b9-134">Valeur</span><span class="sxs-lookup"><span data-stu-id="b51b9-134">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="b51b9-135">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="b51b9-135">Minimum supported client</span></span><br/> | <span data-ttu-id="b51b9-136">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="b51b9-136">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="b51b9-137">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="b51b9-137">Minimum supported server</span></span><br/> | <span data-ttu-id="b51b9-138">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="b51b9-138">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="b51b9-139">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="b51b9-139">Namespace</span></span><br/>                | <span data-ttu-id="b51b9-140">\\Cimv2 racine</span><span class="sxs-lookup"><span data-stu-id="b51b9-140">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="b51b9-141">MOF</span><span class="sxs-lookup"><span data-stu-id="b51b9-141">MOF</span></span><br/>                      | <dl> <span data-ttu-id="b51b9-142"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="b51b9-142"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="b51b9-143">DLL</span><span class="sxs-lookup"><span data-stu-id="b51b9-143">DLL</span></span><br/>                      | <dl> <span data-ttu-id="b51b9-144"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="b51b9-144"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b51b9-145">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="b51b9-145">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b51b9-146">**\_Dépendance CIM**</span><span class="sxs-lookup"><span data-stu-id="b51b9-146">**CIM\_Dependency**</span></span>](cim-dependency.md)
</dt> </dl>

 

