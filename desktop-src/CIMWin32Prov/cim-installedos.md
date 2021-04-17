---
description: La \_ classe d’association CIM installos représente un lien entre le système de l’ordinateur et le système d’exploitation installé.
ms.assetid: 6db5b5a2-91b6-4540-83b8-bb9c86c7f94e
ms.tgt_platform: multiple
title: Classe CIM_InstalledOS
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_InstalledOS
- CIM_InstalledOS.PartComponent
- CIM_InstalledOS.GroupComponent
- CIM_InstalledOS.PrimaryOS
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 53e01be6a87fa6e5ef91ad6e8a81dbbddff4a576
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104523764"
---
# <a name="cim_installedos-class"></a><span data-ttu-id="b3d1b-103">\_Classe CIM installée</span><span class="sxs-lookup"><span data-stu-id="b3d1b-103">CIM\_InstalledOS class</span></span>

<span data-ttu-id="b3d1b-104">La classe d’association **CIM \_ installos** représente un lien entre le système de l’ordinateur et le système d’exploitation installé.</span><span class="sxs-lookup"><span data-stu-id="b3d1b-104">The **CIM\_InstalledOS** association class represents a link between the computer system and the installed operating system.</span></span> <span data-ttu-id="b3d1b-105">Un système d’exploitation est installé lorsqu’il se trouve dans l’extension de stockage d’un système d’ordinateur (par exemple, copié sur un lecteur de disque ou téléchargé en mémoire).</span><span class="sxs-lookup"><span data-stu-id="b3d1b-105">An operating system is installed when it is in a computer system's storage extent (for example, copied to a disk drive or downloaded to memory).</span></span>

> [!IMPORTANT]
> <span data-ttu-id="b3d1b-106">Les classes de la DMTF (Distributed Management Task Force) CIM (Common Information Model) sont les classes parentes sur lesquelles les classes WMI sont générées.</span><span class="sxs-lookup"><span data-stu-id="b3d1b-106">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="b3d1b-107">WMI ne prend actuellement en charge que les [schémas de version CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="b3d1b-107">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="b3d1b-108">La syntaxe suivante est simplifiée à partir de code au format MOF (Managed Object Format) et inclut toutes les propriétés héritées.</span><span class="sxs-lookup"><span data-stu-id="b3d1b-108">The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.</span></span> <span data-ttu-id="b3d1b-109">Les propriétés sont répertoriées par ordre alphabétique, et non par ordre MOF.</span><span class="sxs-lookup"><span data-stu-id="b3d1b-109">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="b3d1b-110">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="b3d1b-110">Syntax</span></span>

``` syntax
[Abstract, UUID("{8502C575-5FBB-11D2-AAC1-006008C78BC7}"), AMENDMENT]
class CIM_InstalledOS : CIM_SystemComponent
{
  CIM_OperatingSystem REF PartComponent;
  CIM_ComputerSystem  REF GroupComponent;
  boolean                 PrimaryOS;
};
```

## <a name="members"></a><span data-ttu-id="b3d1b-111">Membres</span><span class="sxs-lookup"><span data-stu-id="b3d1b-111">Members</span></span>

<span data-ttu-id="b3d1b-112">La classe **CIM \_ installed** possède les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="b3d1b-112">The **CIM\_InstalledOS** class has these types of members:</span></span>

-   [<span data-ttu-id="b3d1b-113">Propriétés</span><span class="sxs-lookup"><span data-stu-id="b3d1b-113">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="b3d1b-114">Propriétés</span><span class="sxs-lookup"><span data-stu-id="b3d1b-114">Properties</span></span>

<span data-ttu-id="b3d1b-115">La classe **CIM \_ installed** possède ces propriétés.</span><span class="sxs-lookup"><span data-stu-id="b3d1b-115">The **CIM\_InstalledOS** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="b3d1b-116">**GroupComponent**</span><span class="sxs-lookup"><span data-stu-id="b3d1b-116">**GroupComponent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b3d1b-117">Type de données **: \_ CIM CIM**</span><span class="sxs-lookup"><span data-stu-id="b3d1b-117">Data type: **CIM\_ComputerSystem**</span></span>
</dt> <dt>

<span data-ttu-id="b3d1b-118">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="b3d1b-118">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b3d1b-119">Qualificateurs : [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("GroupComponent"), [**min**](/windows/desktop/WmiSdk/standard-qualifiers) (1), [**Max**](/windows/desktop/WmiSdk/standard-qualifiers) (1)</span><span class="sxs-lookup"><span data-stu-id="b3d1b-119">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("GroupComponent"), [**Min**](/windows/desktop/WmiSdk/standard-qualifiers) (1), [**Max**](/windows/desktop/WmiSdk/standard-qualifiers) (1)</span></span>
</dt> </dl>

<span data-ttu-id="b3d1b-120">Un [**\_ ComputerSystem CIM**](cim-computersystem.md) décrivant le système informatique.</span><span class="sxs-lookup"><span data-stu-id="b3d1b-120">A [**CIM\_ComputerSystem**](cim-computersystem.md) describing the computer system.</span></span>

</dd> <dt>

<span data-ttu-id="b3d1b-121">**PartComponent**</span><span class="sxs-lookup"><span data-stu-id="b3d1b-121">**PartComponent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b3d1b-122">Type de données : **CIM \_ OperatingSystem**</span><span class="sxs-lookup"><span data-stu-id="b3d1b-122">Data type: **CIM\_OperatingSystem**</span></span>
</dt> <dt>

<span data-ttu-id="b3d1b-123">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="b3d1b-123">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b3d1b-124">Qualificateurs : [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("PartComponent"), [**Weak**](/windows/desktop/WmiSdk/standard-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="b3d1b-124">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("PartComponent"), [**Weak**](/windows/desktop/WmiSdk/standard-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="b3d1b-125">Un système d’exploitation [**CIM \_**](cim-operatingsystem.md) qui décrit le système d’exploitation installé sur le système informatique.</span><span class="sxs-lookup"><span data-stu-id="b3d1b-125">A [**CIM\_OperatingSystem**](cim-operatingsystem.md) that describes the operating system installed on the computer system.</span></span>

</dd> <dt>

<span data-ttu-id="b3d1b-126">**Serveur primaire**</span><span class="sxs-lookup"><span data-stu-id="b3d1b-126">**PrimaryOS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b3d1b-127">Type de données : **booléen**</span><span class="sxs-lookup"><span data-stu-id="b3d1b-127">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="b3d1b-128">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="b3d1b-128">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b3d1b-129">Qualificateurs : [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Système d’exploitation DMTF \| 001,4»)</span><span class="sxs-lookup"><span data-stu-id="b3d1b-129">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Operating System\|001.4")</span></span>
</dt> </dl>

<span data-ttu-id="b3d1b-130">Si la **valeur est true**, le système d’exploitation installé est le système d’exploitation par défaut pour le système informatique.</span><span class="sxs-lookup"><span data-stu-id="b3d1b-130">If **TRUE**, the installed operating system is the default operating system for the computer system.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="b3d1b-131">Notes</span><span class="sxs-lookup"><span data-stu-id="b3d1b-131">Remarks</span></span>

<span data-ttu-id="b3d1b-132">La classe **CIM \_ installed** est dérivée de [**la \_ SystemComponent CIM**](cim-systemcomponent.md).</span><span class="sxs-lookup"><span data-stu-id="b3d1b-132">The **CIM\_InstalledOS** class is derived from [**CIM\_SystemComponent**](cim-systemcomponent.md).</span></span>

<span data-ttu-id="b3d1b-133">WMI n’implémente pas cette classe.</span><span class="sxs-lookup"><span data-stu-id="b3d1b-133">WMI does not implement this class.</span></span> <span data-ttu-id="b3d1b-134">Pour les classes dérivées de **CIM \_ installed**, consultez [classes Win32](win32-provider.md).</span><span class="sxs-lookup"><span data-stu-id="b3d1b-134">For classes derived from **CIM\_InstalledOS**, see [Win32 Classes](win32-provider.md).</span></span>

<span data-ttu-id="b3d1b-135">Cette documentation est dérivée des descriptions de classe CIM publiées par le DMTF.</span><span class="sxs-lookup"><span data-stu-id="b3d1b-135">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="b3d1b-136">Microsoft peut avoir apporté des modifications pour corriger les erreurs mineures, se conformer aux normes de documentation du kit de développement logiciel (SDK) Microsoft ou fournir plus d’informations.</span><span class="sxs-lookup"><span data-stu-id="b3d1b-136">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="b3d1b-137">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="b3d1b-137">Requirements</span></span>



| <span data-ttu-id="b3d1b-138">Condition requise</span><span class="sxs-lookup"><span data-stu-id="b3d1b-138">Requirement</span></span> | <span data-ttu-id="b3d1b-139">Valeur</span><span class="sxs-lookup"><span data-stu-id="b3d1b-139">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="b3d1b-140">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="b3d1b-140">Minimum supported client</span></span><br/> | <span data-ttu-id="b3d1b-141">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="b3d1b-141">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="b3d1b-142">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="b3d1b-142">Minimum supported server</span></span><br/> | <span data-ttu-id="b3d1b-143">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="b3d1b-143">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="b3d1b-144">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="b3d1b-144">Namespace</span></span><br/>                | <span data-ttu-id="b3d1b-145">\\Cimv2 racine</span><span class="sxs-lookup"><span data-stu-id="b3d1b-145">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="b3d1b-146">MOF</span><span class="sxs-lookup"><span data-stu-id="b3d1b-146">MOF</span></span><br/>                      | <dl> <span data-ttu-id="b3d1b-147"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="b3d1b-147"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="b3d1b-148">DLL</span><span class="sxs-lookup"><span data-stu-id="b3d1b-148">DLL</span></span><br/>                      | <dl> <span data-ttu-id="b3d1b-149"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="b3d1b-149"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b3d1b-150">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="b3d1b-150">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b3d1b-151">**\_SYSTEMCOMPONENT CIM**</span><span class="sxs-lookup"><span data-stu-id="b3d1b-151">**CIM\_SystemComponent**</span></span>](cim-systemcomponent.md)
</dt> </dl>

 

