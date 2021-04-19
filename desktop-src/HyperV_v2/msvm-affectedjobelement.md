---
description: Représente une association entre un travail et l’élément managé qui peut être affecté par son exécution.
ms.assetid: 125A4976-A4E3-4D7A-A43B-86045C3B00AE
title: Classe Msvm_AffectedJobElement
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_AffectedJobElement
- Msvm_AffectedJobElement.AffectedElement
- Msvm_AffectedJobElement.AffectingElement
- Msvm_AffectedJobElement.ElementEffects
- Msvm_AffectedJobElement.OtherElementEffectsDescriptions
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: bef667872a7afa4c726ee1b2c77a36c29649114d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106521313"
---
# <a name="msvm_affectedjobelement-class"></a><span data-ttu-id="4ae57-103">MSVM \_ AffectedJobElement, classe</span><span class="sxs-lookup"><span data-stu-id="4ae57-103">Msvm\_AffectedJobElement class</span></span>

<span data-ttu-id="4ae57-104">Représente une association entre un travail et l’élément managé qui peut être affecté par son exécution.</span><span class="sxs-lookup"><span data-stu-id="4ae57-104">Represents an association between a job and the managed element that may be affected by its execution.</span></span>

<span data-ttu-id="4ae57-105">La syntaxe suivante est simplifiée format MOF (MOF) et comprend toutes les propriétés héritées.</span><span class="sxs-lookup"><span data-stu-id="4ae57-105">The following syntax is simplified Managed Object Format (MOF) code, and it includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="4ae57-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="4ae57-106">Syntax</span></span>

``` syntax
[Association, Aggregation, Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_AffectedJobElement : CIM_AffectedJobElement
{
  CIM_ManagedElement REF AffectedElement;
  Msvm_ConcreteJob   REF AffectingElement;
  uint16                 ElementEffects[];
  string                 OtherElementEffectsDescriptions[];
};
```

## <a name="members"></a><span data-ttu-id="4ae57-107">Membres</span><span class="sxs-lookup"><span data-stu-id="4ae57-107">Members</span></span>

<span data-ttu-id="4ae57-108">La classe **MSVM \_ AffectedJobElement** possède les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="4ae57-108">The **Msvm\_AffectedJobElement** class has these types of members:</span></span>

-   [<span data-ttu-id="4ae57-109">Propriétés</span><span class="sxs-lookup"><span data-stu-id="4ae57-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="4ae57-110">Propriétés</span><span class="sxs-lookup"><span data-stu-id="4ae57-110">Properties</span></span>

<span data-ttu-id="4ae57-111">La classe **MSVM \_ AffectedJobElement** possède les propriétés suivantes.</span><span class="sxs-lookup"><span data-stu-id="4ae57-111">The **Msvm\_AffectedJobElement** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="4ae57-112">**AffectedElement**</span><span class="sxs-lookup"><span data-stu-id="4ae57-112">**AffectedElement**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4ae57-113">Type de données : **[ **CIM \_ propriété ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)**</span><span class="sxs-lookup"><span data-stu-id="4ae57-113">Data type: **[**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)**</span></span>
</dt> <dt>

<span data-ttu-id="4ae57-114">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="4ae57-114">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="4ae57-115">Élément managé affecté par l’exécution du travail.</span><span class="sxs-lookup"><span data-stu-id="4ae57-115">The managed element affected by the execution of the job.</span></span> <span data-ttu-id="4ae57-116">Cette propriété est héritée de la [**\_ AffectedJobElement CIM**](/previous-versions//cc150663(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="4ae57-116">This property is inherited from [**CIM\_AffectedJobElement**](/previous-versions//cc150663(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="4ae57-117">**AffectingElement**</span><span class="sxs-lookup"><span data-stu-id="4ae57-117">**AffectingElement**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4ae57-118">Type de données : **[ **MSVM \_ ConcreteJob**](msvm-concretejob.md)**</span><span class="sxs-lookup"><span data-stu-id="4ae57-118">Data type: **[**Msvm\_ConcreteJob**](msvm-concretejob.md)**</span></span>
</dt> <dt>

<span data-ttu-id="4ae57-119">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="4ae57-119">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="4ae57-120">Travail qui affecte l’élément géré.</span><span class="sxs-lookup"><span data-stu-id="4ae57-120">The job that is affecting the managed element.</span></span> <span data-ttu-id="4ae57-121">Cette propriété est héritée de la [**\_ AffectedJobElement CIM**](/previous-versions//cc150663(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="4ae57-121">This property is inherited from [**CIM\_AffectedJobElement**](/previous-versions//cc150663(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="4ae57-122">**ElementEffects**</span><span class="sxs-lookup"><span data-stu-id="4ae57-122">**ElementEffects**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4ae57-123">Type de données : tableau **UInt16**</span><span class="sxs-lookup"><span data-stu-id="4ae57-123">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="4ae57-124">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="4ae57-124">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="4ae57-125">Énumération qui décrit l’effet sur l’élément managé.</span><span class="sxs-lookup"><span data-stu-id="4ae57-125">An enumeration that describes the effect on the managed element.</span></span> <span data-ttu-id="4ae57-126">Cette propriété est héritée de la [**\_ AffectedJobElement CIM**](/previous-versions//cc150663(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="4ae57-126">This property is inherited from [**CIM\_AffectedJobElement**](/previous-versions//cc150663(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="4ae57-127">**OtherElementEffectsDescriptions**</span><span class="sxs-lookup"><span data-stu-id="4ae57-127">**OtherElementEffectsDescriptions**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4ae57-128">Type de données : tableau de **chaînes**</span><span class="sxs-lookup"><span data-stu-id="4ae57-128">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="4ae57-129">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="4ae57-129">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="4ae57-130">Fournit des détails sur l’effet à la position de tableau correspondante dans **ElementEffects**.</span><span class="sxs-lookup"><span data-stu-id="4ae57-130">Provides details for the effect at the corresponding array position in **ElementEffects**.</span></span> <span data-ttu-id="4ae57-131">Cette propriété est héritée de la [**\_ AffectedJobElement CIM**](/previous-versions//cc150663(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="4ae57-131">This property is inherited from [**CIM\_AffectedJobElement**](/previous-versions//cc150663(v=vs.85)).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="4ae57-132">Notes</span><span class="sxs-lookup"><span data-stu-id="4ae57-132">Remarks</span></span>

<span data-ttu-id="4ae57-133">L’accès à la classe **MSVM \_ AffectedJobElement** peut être limité par le filtrage UAC.</span><span class="sxs-lookup"><span data-stu-id="4ae57-133">Access to the **Msvm\_AffectedJobElement** class might be restricted by UAC Filtering.</span></span> <span data-ttu-id="4ae57-134">Pour plus d’informations, consultez [contrôle de compte d’utilisateur et WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span><span class="sxs-lookup"><span data-stu-id="4ae57-134">For more information, see [User Account Control and WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span></span>

## <a name="requirements"></a><span data-ttu-id="4ae57-135">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="4ae57-135">Requirements</span></span>



| <span data-ttu-id="4ae57-136">Condition requise</span><span class="sxs-lookup"><span data-stu-id="4ae57-136">Requirement</span></span> | <span data-ttu-id="4ae57-137">Valeur</span><span class="sxs-lookup"><span data-stu-id="4ae57-137">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4ae57-138">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="4ae57-138">Minimum supported client</span></span><br/> | <span data-ttu-id="4ae57-139">Applications de \[ Bureau Windows 8 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="4ae57-139">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="4ae57-140">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="4ae57-140">Minimum supported server</span></span><br/> | <span data-ttu-id="4ae57-141">Applications de bureau Windows Server 2012 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="4ae57-141">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="4ae57-142">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="4ae57-142">Namespace</span></span><br/>                | <span data-ttu-id="4ae57-143">\\Virtualisation racine \\ v2</span><span class="sxs-lookup"><span data-stu-id="4ae57-143">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="4ae57-144">MOF</span><span class="sxs-lookup"><span data-stu-id="4ae57-144">MOF</span></span><br/>                      | <dl> <span data-ttu-id="4ae57-145"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="4ae57-145"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="4ae57-146">DLL</span><span class="sxs-lookup"><span data-stu-id="4ae57-146">DLL</span></span><br/>                      | <dl> <span data-ttu-id="4ae57-147"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="4ae57-147"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="4ae57-148">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="4ae57-148">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4ae57-149">**\_AFFECTEDJOBELEMENT CIM**</span><span class="sxs-lookup"><span data-stu-id="4ae57-149">**CIM\_AffectedJobElement**</span></span>](cim-affectedjobelement.md)
</dt> <dt>

<span data-ttu-id="4ae57-150">[**\_AFFECTEDJOBELEMENT CIM**](/previous-versions//cc150663(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="4ae57-150">[**CIM\_AffectedJobElement**](/previous-versions//cc150663(v=vs.85))</span></span>
</dt> <dt>

[<span data-ttu-id="4ae57-151">Classes de gestion du système virtuel</span><span class="sxs-lookup"><span data-stu-id="4ae57-151">Virtual System Management Classes</span></span>](virtual-system-management-classes.md)
</dt> </dl>

 

