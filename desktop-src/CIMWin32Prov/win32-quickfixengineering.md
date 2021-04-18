---
description: Le \_ QuickFixEngineering Win32&\# 8194 ; La classe WMI représente une petite mise à jour à l’échelle du système, communément appelée mise à jour du correctif QFE (rapide), appliquée au système d’exploitation actuel.
ms.assetid: 84aed428-7620-4f7a-941f-f9d683020d8a
ms.tgt_platform: multiple
title: Classe Win32_QuickFixEngineering
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_QuickFixEngineering
- Win32_QuickFixEngineering.Caption
- Win32_QuickFixEngineering.Description
- Win32_QuickFixEngineering.InstallDate
- Win32_QuickFixEngineering.Name
- Win32_QuickFixEngineering.Status
- Win32_QuickFixEngineering.CSName
- Win32_QuickFixEngineering.FixComments
- Win32_QuickFixEngineering.HotFixID
- Win32_QuickFixEngineering.InstalledBy
- Win32_QuickFixEngineering.InstalledOn
- Win32_QuickFixEngineering.ServicePackInEffect
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 0e9db31dd452161a31575b6f7184a34c35dea71e
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106540799"
---
# <a name="win32_quickfixengineering-class"></a><span data-ttu-id="71f25-103">\_Classe QuickFixEngineering Win32</span><span class="sxs-lookup"><span data-stu-id="71f25-103">Win32\_QuickFixEngineering class</span></span>

<span data-ttu-id="71f25-104">La  [classe WMI](../wmisdk/retrieving-a-class.md) **\_ QuickFixEngineering** WMI représente une petite mise à jour à l’échelle du système, communément appelée mise à jour du correctif QFE (rapide), appliquée au système d’exploitation actuel.</span><span class="sxs-lookup"><span data-stu-id="71f25-104">The **Win32\_QuickFixEngineering** [WMI class](../wmisdk/retrieving-a-class.md) represents a small system-wide update, commonly referred to as a quick-fix engineering (QFE) update, applied to the current operating system.</span></span> <span data-ttu-id="71f25-105">Cette classe retourne uniquement les mises à jour fournies par la fonction de maintenance basée sur les composants (CBS).</span><span class="sxs-lookup"><span data-stu-id="71f25-105">This class returns only the updates supplied by Component Based Servicing (CBS).</span></span> <span data-ttu-id="71f25-106">Ces mises à jour ne sont pas répertoriées dans le registre.</span><span class="sxs-lookup"><span data-stu-id="71f25-106">These updates are not listed in the registry.</span></span> <span data-ttu-id="71f25-107">Les mises à jour fournies par Microsoft Windows Installer (MSI) ou le site Windows Update ( [https://update.microsoft.com](https://update.microsoft.com/) ) ne sont pas retournées par **Win32 \_ QuickFixEngineering**.</span><span class="sxs-lookup"><span data-stu-id="71f25-107">Updates supplied by Microsoft Windows Installer (MSI) or the Windows update site ([https://update.microsoft.com](https://update.microsoft.com/)) are not returned by **Win32\_QuickFixEngineering**.</span></span>

<span data-ttu-id="71f25-108">La syntaxe suivante est simplifiée par rapport au code MOF (Managed Object Format) et inclut toutes les propriétés héritées.</span><span class="sxs-lookup"><span data-stu-id="71f25-108">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span> <span data-ttu-id="71f25-109">Les propriétés et les méthodes sont classées par ordre alphabétique, et non par ordre MOF.</span><span class="sxs-lookup"><span data-stu-id="71f25-109">Properties and methods are in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="71f25-110">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="71f25-110">Syntax</span></span>

``` syntax
[Dynamic, Provider("CIMWin32"), UUID("{0827250D-BA3E-11d2-B361-00105A1F77A1}"), AMENDMENT]
class Win32_QuickFixEngineering : CIM_LogicalElement
{
  string   Caption;
  string   Description;
  datetime InstallDate;
  string   Name;
  string   Status;
  string   CSName;
  string   FixComments;
  string   HotFixID;
  string   InstalledBy;
  string   InstalledOn;
  string   ServicePackInEffect;
};
```

## <a name="members"></a><span data-ttu-id="71f25-111">Membres</span><span class="sxs-lookup"><span data-stu-id="71f25-111">Members</span></span>

<span data-ttu-id="71f25-112">La classe **Win32 \_ QuickFixEngineering** possède les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="71f25-112">The **Win32\_QuickFixEngineering** class has these types of members:</span></span>

-   [<span data-ttu-id="71f25-113">Propriétés</span><span class="sxs-lookup"><span data-stu-id="71f25-113">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="71f25-114">Propriétés</span><span class="sxs-lookup"><span data-stu-id="71f25-114">Properties</span></span>

<span data-ttu-id="71f25-115">La classe **Win32 \_ QuickFixEngineering** a ces propriétés.</span><span class="sxs-lookup"><span data-stu-id="71f25-115">The **Win32\_QuickFixEngineering** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="71f25-116">**Caption**</span><span class="sxs-lookup"><span data-stu-id="71f25-116">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="71f25-117">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="71f25-117">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="71f25-118">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="71f25-118">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="71f25-119">Qualificateurs : [**MaxLen**](../wmisdk/standard-qualifiers.md) (64), [**DisplayName**](../wmisdk/standard-qualifiers.md) (« Caption »)</span><span class="sxs-lookup"><span data-stu-id="71f25-119">Qualifiers: [**MaxLen**](../wmisdk/standard-qualifiers.md) (64), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Caption")</span></span>
</dt> </dl>

<span data-ttu-id="71f25-120">Brève description textuelle de l’objet.</span><span class="sxs-lookup"><span data-stu-id="71f25-120">A short textual description of the object.</span></span>

<span data-ttu-id="71f25-121">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="71f25-121">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="71f25-122">**CSName**</span><span class="sxs-lookup"><span data-stu-id="71f25-122">**CSName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="71f25-123">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="71f25-123">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="71f25-124">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="71f25-124">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="71f25-125">Qualificateurs : [**\_ clé CIM**](../wmisdk/standard-wmi-qualifiers.md), [**MaxLen**](../wmisdk/standard-qualifiers.md) (256), [**propagée**](../wmisdk/standard-qualifiers.md) («[**CIMOM \_ CIM**](cim-computersystem.md).**Name**"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) (" WMI ")</span><span class="sxs-lookup"><span data-stu-id="71f25-125">Qualifiers: [**CIM\_Key**](../wmisdk/standard-wmi-qualifiers.md), [**MaxLen**](../wmisdk/standard-qualifiers.md) (256), [**Propagated**](../wmisdk/standard-qualifiers.md) ("[**CIM\_ComputerSystem**](cim-computersystem.md).**Name**"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("WMI")</span></span>
</dt> </dl>

<span data-ttu-id="71f25-126">Nom local du système informatique.</span><span class="sxs-lookup"><span data-stu-id="71f25-126">Local name of the computer system.</span></span> <span data-ttu-id="71f25-127">La valeur de cette propriété provient de la [**classe \_ ComputerSystem CIM**](cim-computersystem.md) .</span><span class="sxs-lookup"><span data-stu-id="71f25-127">The value for this property comes from the [**CIM\_ComputerSystem**](cim-computersystem.md) class.</span></span>

</dd> <dt>

<span data-ttu-id="71f25-128">**Description**</span><span class="sxs-lookup"><span data-stu-id="71f25-128">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="71f25-129">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="71f25-129">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="71f25-130">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="71f25-130">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="71f25-131">Qualificateurs : [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Description")</span><span class="sxs-lookup"><span data-stu-id="71f25-131">Qualifiers: [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Description")</span></span>
</dt> </dl>

<span data-ttu-id="71f25-132">Description textuelle de l’objet.</span><span class="sxs-lookup"><span data-stu-id="71f25-132">A textual description of the object.</span></span>

<span data-ttu-id="71f25-133">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="71f25-133">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="71f25-134">**FixComments**</span><span class="sxs-lookup"><span data-stu-id="71f25-134">**FixComments**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="71f25-135">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="71f25-135">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="71f25-136">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="71f25-136">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="71f25-137">Qualificateurs : [**MappingStrings**](../wmisdk/standard-qualifiers.md) (« Win32Registry \| Software \\ \\ Microsoft \\ \\ Windows NT \\ \\ CurrentVersion \\ \\ HotFix »)</span><span class="sxs-lookup"><span data-stu-id="71f25-137">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry\|SOFTWARE\\\\Microsoft\\\\Windows NT\\\\CurrentVersion\\\\Hotfix")</span></span>
</dt> </dl>

<span data-ttu-id="71f25-138">Commentaires supplémentaires liés à la mise à jour.</span><span class="sxs-lookup"><span data-stu-id="71f25-138">Additional comments that relate to the update.</span></span>

</dd> <dt>

<span data-ttu-id="71f25-139">**HotFixID.**</span><span class="sxs-lookup"><span data-stu-id="71f25-139">**HotFixID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="71f25-140">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="71f25-140">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="71f25-141">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="71f25-141">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="71f25-142">Qualificateurs : [**clé**](../wmisdk/key-qualifier.md), [**MaxLen**](../wmisdk/standard-qualifiers.md) (260), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| Software \\ \\ Microsoft \\ \\ Windows NT \\ \\ CurrentVersion \\ \\ Hotfix")</span><span class="sxs-lookup"><span data-stu-id="71f25-142">Qualifiers: [**key**](../wmisdk/key-qualifier.md), [**MaxLen**](../wmisdk/standard-qualifiers.md) (260), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry\|SOFTWARE\\\\Microsoft\\\\Windows NT\\\\CurrentVersion\\\\Hotfix")</span></span>
</dt> </dl>

<span data-ttu-id="71f25-143">Identificateur unique associé à une mise à jour particulière.</span><span class="sxs-lookup"><span data-stu-id="71f25-143">Unique identifier associated with a particular update.</span></span>

</dd> <dt>

<span data-ttu-id="71f25-144">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="71f25-144">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="71f25-145">Type de données : **DateTime**</span><span class="sxs-lookup"><span data-stu-id="71f25-145">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="71f25-146">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="71f25-146">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="71f25-147">Qualificateurs : [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF. DMTF \| ComponentID \| 001,5 "), [**DisplayName**](../wmisdk/standard-qualifiers.md) (" date d’installation ")</span><span class="sxs-lookup"><span data-stu-id="71f25-147">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF.DMTF\|ComponentID\|001.5"), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Install Date")</span></span>
</dt> </dl>

<span data-ttu-id="71f25-148">Indique le moment où l’objet a été installé.</span><span class="sxs-lookup"><span data-stu-id="71f25-148">Indicates when the object was installed.</span></span> <span data-ttu-id="71f25-149">L’absence de valeur n’indique pas que l’objet n’est pas installé.</span><span class="sxs-lookup"><span data-stu-id="71f25-149">Lack of a value does not indicate that the object is not installed.</span></span>

<span data-ttu-id="71f25-150">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="71f25-150">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="71f25-151">**InstalledBy**</span><span class="sxs-lookup"><span data-stu-id="71f25-151">**InstalledBy**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="71f25-152">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="71f25-152">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="71f25-153">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="71f25-153">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="71f25-154">Qualificateurs : [**MappingStrings**](../wmisdk/standard-qualifiers.md) (« Win32Registry \| Software \\ \\ Microsoft \\ \\ Windows NT \\ \\ CurrentVersion \\ \\ HotFix »)</span><span class="sxs-lookup"><span data-stu-id="71f25-154">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry\|SOFTWARE\\\\Microsoft\\\\Windows NT\\\\CurrentVersion\\\\Hotfix")</span></span>
</dt> </dl>

<span data-ttu-id="71f25-155">Personne qui a installé la mise à jour.</span><span class="sxs-lookup"><span data-stu-id="71f25-155">Person who installed the update.</span></span> <span data-ttu-id="71f25-156">Si cette valeur est inconnue, la propriété est vide.</span><span class="sxs-lookup"><span data-stu-id="71f25-156">If this value is unknown, the property is empty.</span></span>

</dd> <dt>

<span data-ttu-id="71f25-157">**InstalledOn**</span><span class="sxs-lookup"><span data-stu-id="71f25-157">**InstalledOn**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="71f25-158">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="71f25-158">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="71f25-159">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="71f25-159">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="71f25-160">Qualificateurs : [**MappingStrings**](../wmisdk/standard-qualifiers.md) (« Win32Registry \| Software \\ \\ Microsoft \\ \\ Windows NT \\ \\ CurrentVersion \\ \\ HotFix »)</span><span class="sxs-lookup"><span data-stu-id="71f25-160">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry\|SOFTWARE\\\\Microsoft\\\\Windows NT\\\\CurrentVersion\\\\Hotfix")</span></span>
</dt> </dl>

<span data-ttu-id="71f25-161">Date à laquelle la mise à jour a été installée.</span><span class="sxs-lookup"><span data-stu-id="71f25-161">Date that the update was installed.</span></span> <span data-ttu-id="71f25-162">Si cette valeur est inconnue, la propriété est vide.</span><span class="sxs-lookup"><span data-stu-id="71f25-162">If this value is unknown, the property is empty.</span></span>

> [!Note]  
> <span data-ttu-id="71f25-163">Cette propriété peut utiliser des formats différents, en fonction du moment où le QuickFix a été installé.</span><span class="sxs-lookup"><span data-stu-id="71f25-163">This property may use different formats, depending on when the QuickFix was installed.</span></span> <span data-ttu-id="71f25-164">La plupart des systèmes utilisent un format de date standard, tel que « 23-10-2013 ».</span><span class="sxs-lookup"><span data-stu-id="71f25-164">Most systems use a standard date format, such as "23-10-2013".</span></span> <span data-ttu-id="71f25-165">Toutefois, certains systèmes peuvent retourner une valeur hexadécimale 64 bits au format [**fileTime**](/windows/win32/api/minwinbase/ns-minwinbase-filetime) Win32.</span><span class="sxs-lookup"><span data-stu-id="71f25-165">However, some systems may return a 64-bit hexidecimal value in the Win32 [**FILETIME**](/windows/win32/api/minwinbase/ns-minwinbase-filetime) format.</span></span>

 

</dd> <dt>

<span data-ttu-id="71f25-166">**Nom**</span><span class="sxs-lookup"><span data-stu-id="71f25-166">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="71f25-167">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="71f25-167">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="71f25-168">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="71f25-168">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="71f25-169">Qualificateurs : [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Name")</span><span class="sxs-lookup"><span data-stu-id="71f25-169">Qualifiers: [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Name")</span></span>
</dt> </dl>

<span data-ttu-id="71f25-170">Étiquette par laquelle l’objet est connu.</span><span class="sxs-lookup"><span data-stu-id="71f25-170">Label by which the object is known.</span></span> <span data-ttu-id="71f25-171">Lorsqu’elle est sous-classée, cette propriété peut être substituée pour être une propriété de clé.</span><span class="sxs-lookup"><span data-stu-id="71f25-171">When subclassed, this property can be overridden to be a key property.</span></span>

<span data-ttu-id="71f25-172">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="71f25-172">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="71f25-173">**ServicePackInEffect**</span><span class="sxs-lookup"><span data-stu-id="71f25-173">**ServicePackInEffect**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="71f25-174">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="71f25-174">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="71f25-175">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="71f25-175">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="71f25-176">Qualificateurs : [**clé**](../wmisdk/key-qualifier.md), [**MaxLen**](../wmisdk/standard-qualifiers.md) (260), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| Software \\ \\ Microsoft \\ \\ Windows NT \\ \\ CurrentVersion \\ \\ Hotfix")</span><span class="sxs-lookup"><span data-stu-id="71f25-176">Qualifiers: [**key**](../wmisdk/key-qualifier.md), [**MaxLen**](../wmisdk/standard-qualifiers.md) (260), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry\|SOFTWARE\\\\Microsoft\\\\Windows NT\\\\CurrentVersion\\\\Hotfix")</span></span>
</dt> </dl>

<span data-ttu-id="71f25-177">Service Pack en vigueur lorsque la mise à jour a été appliquée.</span><span class="sxs-lookup"><span data-stu-id="71f25-177">Service pack in effect when the update was applied.</span></span> <span data-ttu-id="71f25-178">Si aucun Service Pack n’a été appliqué, la propriété prend la valeur SP0.</span><span class="sxs-lookup"><span data-stu-id="71f25-178">If no service pack has been applied, the property takes on the value SP0.</span></span> <span data-ttu-id="71f25-179">S’il n’est pas possible de déterminer ce que Service Pack était en vigueur, cette propriété a la **valeur null**.</span><span class="sxs-lookup"><span data-stu-id="71f25-179">If it cannot be determined what service pack was in effect, this property is **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="71f25-180">**État**</span><span class="sxs-lookup"><span data-stu-id="71f25-180">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="71f25-181">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="71f25-181">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="71f25-182">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="71f25-182">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="71f25-183">Qualificateurs : [**MaxLen**](../wmisdk/standard-qualifiers.md) (10), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Status")</span><span class="sxs-lookup"><span data-stu-id="71f25-183">Qualifiers: [**MaxLen**](../wmisdk/standard-qualifiers.md) (10), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Status")</span></span>
</dt> </dl>

<span data-ttu-id="71f25-184">Chaîne qui indique l’état actuel de l’objet.</span><span class="sxs-lookup"><span data-stu-id="71f25-184">String that indicates the current status of the object.</span></span> <span data-ttu-id="71f25-185">L’état opérationnel et non opérationnel peut être défini.</span><span class="sxs-lookup"><span data-stu-id="71f25-185">Operational and non-operational status can be defined.</span></span> <span data-ttu-id="71f25-186">L’état opérationnel peut inclure « OK », « détérioré » et « échec prédit ».</span><span class="sxs-lookup"><span data-stu-id="71f25-186">Operational status can include "OK", "Degraded", and "Pred Fail".</span></span> <span data-ttu-id="71f25-187">« Échec prédit » indique qu’un élément fonctionne correctement, mais prédit un échec (par exemple, un lecteur de disque dur intelligent).</span><span class="sxs-lookup"><span data-stu-id="71f25-187">"Pred Fail" indicates that an element is functioning properly, but is predicting a failure (for example, a SMART-enabled hard disk drive).</span></span>

<span data-ttu-id="71f25-188">L’état non opérationnel peut inclure « erreur », « démarrage », « arrêt » et « service ».</span><span class="sxs-lookup"><span data-stu-id="71f25-188">Non-operational status can include "Error", "Starting", "Stopping", and "Service".</span></span> <span data-ttu-id="71f25-189">Le « service » peut s’appliquer pendant la mise en miroir de disques, en rechargeant une liste d’autorisations utilisateur ou d’autres tâches administratives.</span><span class="sxs-lookup"><span data-stu-id="71f25-189">"Service" can apply during disk mirror-resilvering, reloading a user permissions list, or other administrative work.</span></span> <span data-ttu-id="71f25-190">Tous les travaux de ce type ne sont pas en ligne, mais l’élément géré n’est ni « OK », ni l’un des autres États.</span><span class="sxs-lookup"><span data-stu-id="71f25-190">Not all such work is online, but the managed element is neither "OK" nor in one of the other states.</span></span>

<span data-ttu-id="71f25-191">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="71f25-191">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<span data-ttu-id="71f25-192">Les valeurs sont notamment les suivantes :</span><span class="sxs-lookup"><span data-stu-id="71f25-192">Values include the following:</span></span>

<dt>

<span id="OK"></span><span id="ok"></span>

<span data-ttu-id="71f25-193">**OK** (« OK »)</span><span class="sxs-lookup"><span data-stu-id="71f25-193">**OK** ("OK")</span></span>


</dt> <dd></dd> <dt>

<span id="Error"></span><span id="error"></span><span id="ERROR"></span>

<span data-ttu-id="71f25-194">**Erreur** (« erreur »)</span><span class="sxs-lookup"><span data-stu-id="71f25-194">**Error** ("Error")</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="71f25-195">**Détérioré** (« détérioré »)</span><span class="sxs-lookup"><span data-stu-id="71f25-195">**Degraded** ("Degraded")</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="71f25-196">**Inconnu** ("inconnu")</span><span class="sxs-lookup"><span data-stu-id="71f25-196">**Unknown** ("Unknown")</span></span>


</dt> <dd></dd> <dt>

<span id="Pred_Fail"></span><span id="pred_fail"></span><span id="PRED_FAIL"></span>

<span data-ttu-id="71f25-197">**Échec** prévu (« échec prédit »)</span><span class="sxs-lookup"><span data-stu-id="71f25-197">**Pred Fail** ("Pred Fail")</span></span>


</dt> <dd></dd> <dt>

<span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>

<span data-ttu-id="71f25-198">**Démarrage** en cours (« démarrage »)</span><span class="sxs-lookup"><span data-stu-id="71f25-198">**Starting** ("Starting")</span></span>


</dt> <dd></dd> <dt>

<span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>

<span data-ttu-id="71f25-199">**Arrêt** en cours (« arrêt »)</span><span class="sxs-lookup"><span data-stu-id="71f25-199">**Stopping** ("Stopping")</span></span>


</dt> <dd></dd> <dt>

<span id="Service"></span><span id="service"></span><span id="SERVICE"></span>

<span data-ttu-id="71f25-200">**Service** (« service »)</span><span class="sxs-lookup"><span data-stu-id="71f25-200">**Service** ("Service")</span></span>


</dt> <dd></dd> <dt>

<span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>

<span data-ttu-id="71f25-201">**Stressed** (« stressed »)</span><span class="sxs-lookup"><span data-stu-id="71f25-201">**Stressed** ("Stressed")</span></span>


</dt> <dd></dd> <dt>

<span id="NonRecover"></span><span id="nonrecover"></span><span id="NONRECOVER"></span>

<span data-ttu-id="71f25-202">Non **récupéré** (« non récupéré »)</span><span class="sxs-lookup"><span data-stu-id="71f25-202">**NonRecover** ("NonRecover")</span></span>


</dt> <dd></dd> <dt>

<span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>

<span data-ttu-id="71f25-203">**Aucun contact** (« aucun contact »)</span><span class="sxs-lookup"><span data-stu-id="71f25-203">**No Contact** ("No Contact")</span></span>


</dt> <dd></dd> <dt>

<span id="Lost_Comm"></span><span id="lost_comm"></span><span id="LOST_COMM"></span>

<span data-ttu-id="71f25-204">**Communication perdue** (« inversée comm »)</span><span class="sxs-lookup"><span data-stu-id="71f25-204">**Lost Comm** ("Lost Comm")</span></span>


<span data-ttu-id="71f25-205"></dt> <dd></dd> </dl>

</dd> </dl></span><span class="sxs-lookup"><span data-stu-id="71f25-205"></dt> <dd></dd> </dl>

</dd> </dl></span></span>

## <a name="remarks"></a><span data-ttu-id="71f25-206">Notes</span><span class="sxs-lookup"><span data-stu-id="71f25-206">Remarks</span></span>

<span data-ttu-id="71f25-207">La classe **Win32 \_ QuickFixEngineering** est dérivée de [**CIM \_ LogicalElement**](cim-logicalelement.md).</span><span class="sxs-lookup"><span data-stu-id="71f25-207">The **Win32\_QuickFixEngineering** class is derived from [**CIM\_LogicalElement**](cim-logicalelement.md).</span></span>

<span data-ttu-id="71f25-208">Étant donné que les mises à jour sont stockées à deux emplacements, une énumération de cette classe peut entraîner des doublons.</span><span class="sxs-lookup"><span data-stu-id="71f25-208">Because updates are stored in two places, an enumeration of this class can result in duplicates.</span></span>

<span data-ttu-id="71f25-209">Un correctif est un correctif de système d’exploitation temporaire produit par le groupe d’ingénierie de correction rapide chez Microsoft.</span><span class="sxs-lookup"><span data-stu-id="71f25-209">A hot fix is a temporary operating system patch produced by the Quick Fix Engineering group at Microsoft.</span></span> <span data-ttu-id="71f25-210">À l’instar des service packs, les correctifs représentent les modifications apportées à une version de Windows après la sortie du système d’exploitation.</span><span class="sxs-lookup"><span data-stu-id="71f25-210">Like service packs, hot fixes represent changes that have been made to a version of Windows after the operating system has been released.</span></span>

<span data-ttu-id="71f25-211">Contrairement aux service packs, les correctifs ne sont pas destinés à une installation permanente sur tous les ordinateurs.</span><span class="sxs-lookup"><span data-stu-id="71f25-211">Unlike service packs, hot fixes are not intended for blanket installation on all computers.</span></span> <span data-ttu-id="71f25-212">Au lieu de cela, ils sont développés pour résoudre des problèmes très spécifiques, souvent pour des configurations d’ordinateur spécifiques.</span><span class="sxs-lookup"><span data-stu-id="71f25-212">Instead, they are developed to address very specific problems, often for specific computer configurations.</span></span>

<span data-ttu-id="71f25-213">En outre, les correctifs représentent des installations indépendantes qui ne dépendent pas d’autres correctifs publiés.</span><span class="sxs-lookup"><span data-stu-id="71f25-213">In addition, hot fixes represent independent installations that do not depend on other released hot fixes.</span></span> <span data-ttu-id="71f25-214">Par exemple, un hypothétique correctif 4 n’inclut pas les correctifs de bogues et les fonctionnalités incluses dans les correctifs à chaud 1, 2 et 3.</span><span class="sxs-lookup"><span data-stu-id="71f25-214">For example, a hypothetical hot fix 4 would not include the bug fixes and functionality included in hot fixes 1, 2, and 3.</span></span> <span data-ttu-id="71f25-215">Dans la plupart des cas, il n’y aurait pas non plus besoin d’installer les correctifs 1, 2 et 3 avant d’installer le correctif 4 à chaud.</span><span class="sxs-lookup"><span data-stu-id="71f25-215">In most cases, there would also be no requirement that you install hot fixes 1, 2, and 3 before installing hot fix 4.</span></span> <span data-ttu-id="71f25-216">Cela permet à l’énumération des correctifs individuels d’effectuer une tâche administrative importante : pour connaître la configuration exacte d’un ordinateur, vous devez savoir non seulement quels service packs ont été installés, mais également quels correctifs ont été installés.</span><span class="sxs-lookup"><span data-stu-id="71f25-216">This makes enumeration of individual hot fixes an important administrative task: to know the exact configuration of a computer, you need to know not only which service packs have been installed but also which individual hot fixes have been installed.</span></span>

<span data-ttu-id="71f25-217">La **classe \_ QuickFixEngineering Win32** vous permet d’énumérer tous les correctifs logiciels qui ont été installés sur un ordinateur</span><span class="sxs-lookup"><span data-stu-id="71f25-217">The **Win32\_QuickFixEngineering** class enables you to enumerate all the hot fixes that have been installed on a computer</span></span>

## <a name="examples"></a><span data-ttu-id="71f25-218">Exemples</span><span class="sxs-lookup"><span data-stu-id="71f25-218">Examples</span></span>

<span data-ttu-id="71f25-219">L’exemple d' [extraction de programmes installés](https://Gallery.TechNet.Microsoft.Com/Get-Installed-Programs-fae091ed) dans PowerShell retourne la liste complète des programmes installés.</span><span class="sxs-lookup"><span data-stu-id="71f25-219">The [Get Installed Programs](https://Gallery.TechNet.Microsoft.Com/Get-Installed-Programs-fae091ed) PowerShell example returns a full list of installed programs.</span></span>

<span data-ttu-id="71f25-220">L’exemple VBScript suivant énumère les correctifs logiciels installés sur un ordinateur</span><span class="sxs-lookup"><span data-stu-id="71f25-220">The following VBScript sample enumerates the installed hot fixes on a computer</span></span>


```VB
strComputer = "."
Set objWMIService = GetObject("winmgmts:{impersonationLevel=impersonate}!\\" & strComputer & "\root\cimv2")
Set colQuickFixes = objWMIService.ExecQuery("SELECT * FROM Win32_QuickFixEngineering")
For Each objQuickFix in colQuickFixes
 Wscript.Echo "Computer: " & objQuickFix.CSName
 Wscript.Echo "Description: " & objQuickFix.Description
 Wscript.Echo "Hot Fix ID: " & objQuickFix.HotFixID
 Wscript.Echo "Installation Date: " & objQuickFix.InstallDate
 Wscript.Echo "Installed By: " & objQuickFix.InstalledBy
Next
```



## <a name="requirements"></a><span data-ttu-id="71f25-221">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="71f25-221">Requirements</span></span>



| <span data-ttu-id="71f25-222">Condition requise</span><span class="sxs-lookup"><span data-stu-id="71f25-222">Requirement</span></span> | <span data-ttu-id="71f25-223">Valeur</span><span class="sxs-lookup"><span data-stu-id="71f25-223">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="71f25-224">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="71f25-224">Minimum supported client</span></span><br/> | <span data-ttu-id="71f25-225">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="71f25-225">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="71f25-226">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="71f25-226">Minimum supported server</span></span><br/> | <span data-ttu-id="71f25-227">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="71f25-227">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="71f25-228">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="71f25-228">Namespace</span></span><br/>                | <span data-ttu-id="71f25-229">\\Cimv2 racine</span><span class="sxs-lookup"><span data-stu-id="71f25-229">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="71f25-230">MOF</span><span class="sxs-lookup"><span data-stu-id="71f25-230">MOF</span></span><br/>                      | <dl> <span data-ttu-id="71f25-231"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="71f25-231"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="71f25-232">DLL</span><span class="sxs-lookup"><span data-stu-id="71f25-232">DLL</span></span><br/>                      | <dl> <span data-ttu-id="71f25-233"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="71f25-233"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="71f25-234">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="71f25-234">See also</span></span>

<dl> <dt>

[<span data-ttu-id="71f25-235">**\_LOGICALELEMENT CIM**</span><span class="sxs-lookup"><span data-stu-id="71f25-235">**CIM\_LogicalElement**</span></span>](cim-logicalelement.md)
</dt> <dt>

[<span data-ttu-id="71f25-236">Classes du système d’exploitation</span><span class="sxs-lookup"><span data-stu-id="71f25-236">Operating System Classes</span></span>](./operating-system-classes.md)
</dt> <dt>

[<span data-ttu-id="71f25-237">Tâches WMI : systèmes d’exploitation</span><span class="sxs-lookup"><span data-stu-id="71f25-237">WMI Tasks: Operating Systems</span></span>](../wmisdk/wmi-tasks--operating-systems.md)
</dt> </dl>

 

 
