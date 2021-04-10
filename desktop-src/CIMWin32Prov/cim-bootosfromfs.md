---
description: La \_ classe CIM BootOSFromFS associe le système d’exploitation et les systèmes de fichiers à partir desquels le système d’exploitation est chargé.
ms.assetid: c5697e9c-9031-4787-a03d-cf713c961cdf
ms.tgt_platform: multiple
title: Classe CIM_BootOSFromFS
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_BootOSFromFS
- CIM_BootOSFromFS.Dependent
- CIM_BootOSFromFS.Antecedent
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 993ee7a66ef9f8b0cbb47285e38b78e4fd4dd61b
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103950706"
---
# <a name="cim_bootosfromfs-class"></a><span data-ttu-id="28fb9-103">\_Classe CIM BootOSFromFS</span><span class="sxs-lookup"><span data-stu-id="28fb9-103">CIM\_BootOSFromFS class</span></span>

<span data-ttu-id="28fb9-104">La classe **CIM \_ BootOSFromFS** associe le système d’exploitation et les systèmes de fichiers à partir desquels le système d’exploitation est chargé.</span><span class="sxs-lookup"><span data-stu-id="28fb9-104">The **CIM\_BootOSFromFS** class associates the operating system and the file systems from which the operating system is loaded.</span></span> <span data-ttu-id="28fb9-105">L’Association est de plusieurs-à-plusieurs ; un système d’exploitation distribué peut dépendre de plusieurs systèmes de fichiers pour se charger correctement et complètement.</span><span class="sxs-lookup"><span data-stu-id="28fb9-105">The association is many-to-many; a distributed operating system can depend on several file systems to load correctly and completely.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="28fb9-106">Les classes de la DMTF (Distributed Management Task Force) CIM (Common Information Model) sont les classes parentes sur lesquelles les classes WMI sont générées.</span><span class="sxs-lookup"><span data-stu-id="28fb9-106">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="28fb9-107">WMI ne prend actuellement en charge que les [schémas de version CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="28fb9-107">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="28fb9-108">La syntaxe suivante est simplifiée à partir de code au format MOF (Managed Object Format) et inclut toutes les propriétés héritées.</span><span class="sxs-lookup"><span data-stu-id="28fb9-108">The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.</span></span> <span data-ttu-id="28fb9-109">Les propriétés sont répertoriées par ordre alphabétique, et non par ordre MOF.</span><span class="sxs-lookup"><span data-stu-id="28fb9-109">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="28fb9-110">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="28fb9-110">Syntax</span></span>

``` syntax
[Abstract, UUID("{5F5B101E-DB35-11d2-85FC-0000F8102E5F}"), AMENDMENT]
class CIM_BootOSFromFS : CIM_Dependency
{
  CIM_OperatingSystem REF Dependent;
  CIM_FileSystem      REF Antecedent;
};
```

## <a name="members"></a><span data-ttu-id="28fb9-111">Membres</span><span class="sxs-lookup"><span data-stu-id="28fb9-111">Members</span></span>

<span data-ttu-id="28fb9-112">La classe **CIM \_ BootOSFromFS** possède les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="28fb9-112">The **CIM\_BootOSFromFS** class has these types of members:</span></span>

-   [<span data-ttu-id="28fb9-113">Propriétés</span><span class="sxs-lookup"><span data-stu-id="28fb9-113">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="28fb9-114">Propriétés</span><span class="sxs-lookup"><span data-stu-id="28fb9-114">Properties</span></span>

<span data-ttu-id="28fb9-115">La classe **CIM \_ BootOSFromFS** possède les propriétés suivantes.</span><span class="sxs-lookup"><span data-stu-id="28fb9-115">The **CIM\_BootOSFromFS** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="28fb9-116">**Antécédent**</span><span class="sxs-lookup"><span data-stu-id="28fb9-116">**Antecedent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="28fb9-117">Type de données **: \_ système de fichiers CIM**</span><span class="sxs-lookup"><span data-stu-id="28fb9-117">Data type: **CIM\_FileSystem**</span></span>
</dt> <dt>

<span data-ttu-id="28fb9-118">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="28fb9-118">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="28fb9-119">Qualificateurs : [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Antecedent")</span><span class="sxs-lookup"><span data-stu-id="28fb9-119">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Antecedent")</span></span>
</dt> </dl>

<span data-ttu-id="28fb9-120">Système de fichiers à partir duquel le système d’exploitation est chargé.</span><span class="sxs-lookup"><span data-stu-id="28fb9-120">The file system from which the operating system is loaded.</span></span>

</dd> <dt>

<span data-ttu-id="28fb9-121">**Charge**</span><span class="sxs-lookup"><span data-stu-id="28fb9-121">**Dependent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="28fb9-122">Type de données : **CIM \_ OperatingSystem**</span><span class="sxs-lookup"><span data-stu-id="28fb9-122">Data type: **CIM\_OperatingSystem**</span></span>
</dt> <dt>

<span data-ttu-id="28fb9-123">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="28fb9-123">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="28fb9-124">Qualificateurs : [**override**](/windows/desktop/WmiSdk/standard-qualifiers) (« Dependent »)</span><span class="sxs-lookup"><span data-stu-id="28fb9-124">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Dependent")</span></span>
</dt> </dl>

<span data-ttu-id="28fb9-125">Système d'exploitation.</span><span class="sxs-lookup"><span data-stu-id="28fb9-125">The operating system.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="28fb9-126">Notes</span><span class="sxs-lookup"><span data-stu-id="28fb9-126">Remarks</span></span>

<span data-ttu-id="28fb9-127">La classe **CIM \_ BootOSFromFS** est dérivée de la [**\_ dépendance CIM**](cim-dependency.md).</span><span class="sxs-lookup"><span data-stu-id="28fb9-127">The **CIM\_BootOSFromFS** class is derived from [**CIM\_Dependency**](cim-dependency.md).</span></span>

<span data-ttu-id="28fb9-128">WMI n’implémente pas cette classe.</span><span class="sxs-lookup"><span data-stu-id="28fb9-128">WMI does not implement this class.</span></span>

<span data-ttu-id="28fb9-129">Cette documentation est dérivée des descriptions de classe CIM publiées par le DMTF.</span><span class="sxs-lookup"><span data-stu-id="28fb9-129">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="28fb9-130">Microsoft peut avoir apporté des modifications pour corriger les erreurs mineures, se conformer aux normes de documentation du kit de développement logiciel (SDK) Microsoft ou fournir plus d’informations.</span><span class="sxs-lookup"><span data-stu-id="28fb9-130">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="28fb9-131">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="28fb9-131">Requirements</span></span>



| <span data-ttu-id="28fb9-132">Condition requise</span><span class="sxs-lookup"><span data-stu-id="28fb9-132">Requirement</span></span> | <span data-ttu-id="28fb9-133">Valeur</span><span class="sxs-lookup"><span data-stu-id="28fb9-133">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="28fb9-134">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="28fb9-134">Minimum supported client</span></span><br/> | <span data-ttu-id="28fb9-135">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="28fb9-135">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="28fb9-136">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="28fb9-136">Minimum supported server</span></span><br/> | <span data-ttu-id="28fb9-137">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="28fb9-137">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="28fb9-138">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="28fb9-138">Namespace</span></span><br/>                | <span data-ttu-id="28fb9-139">\\Cimv2 racine</span><span class="sxs-lookup"><span data-stu-id="28fb9-139">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="28fb9-140">MOF</span><span class="sxs-lookup"><span data-stu-id="28fb9-140">MOF</span></span><br/>                      | <dl> <span data-ttu-id="28fb9-141"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="28fb9-141"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="28fb9-142">DLL</span><span class="sxs-lookup"><span data-stu-id="28fb9-142">DLL</span></span><br/>                      | <dl> <span data-ttu-id="28fb9-143"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="28fb9-143"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="28fb9-144">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="28fb9-144">See also</span></span>

<dl> <dt>

[<span data-ttu-id="28fb9-145">**\_Dépendance CIM**</span><span class="sxs-lookup"><span data-stu-id="28fb9-145">**CIM\_Dependency**</span></span>](cim-dependency.md)
</dt> </dl>

 

