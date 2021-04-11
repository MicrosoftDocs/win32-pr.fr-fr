---
description: Associe une instance de machine virtuelle au service de gestion qui contrôle son état.
ms.assetid: 12EB3951-74D4-477F-8B55-69FAA3B14631
title: Classe Msvm_ServiceAffectsElement
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_ServiceAffectsElement
- Msvm_ServiceAffectsElement.AffectedElement
- Msvm_ServiceAffectsElement.AffectingElement
- Msvm_ServiceAffectsElement.ElementEffects
- Msvm_ServiceAffectsElement.OtherElementEffectsDescriptions
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: eadb9f33015091999776b73c83d792ccd29396b0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104113883"
---
# <a name="msvm_serviceaffectselement-class"></a><span data-ttu-id="7c3a8-103">MSVM \_ ServiceAffectsElement, classe</span><span class="sxs-lookup"><span data-stu-id="7c3a8-103">Msvm\_ServiceAffectsElement class</span></span>

<span data-ttu-id="7c3a8-104">Associe une instance de machine virtuelle au service de gestion qui contrôle son état.</span><span class="sxs-lookup"><span data-stu-id="7c3a8-104">Associates a virtual machine instance with the management service that controls its state.</span></span>

<span data-ttu-id="7c3a8-105">La syntaxe suivante est simplifiée format MOF (MOF) et comprend toutes les propriétés héritées.</span><span class="sxs-lookup"><span data-stu-id="7c3a8-105">The following syntax is simplified Managed Object Format (MOF) code, and it includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="7c3a8-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="7c3a8-106">Syntax</span></span>

``` syntax
[Association, Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_ServiceAffectsElement : CIM_ServiceAffectsElement
{
  CIM_ManagedElement REF AffectedElement;
  CIM_Service        REF AffectingElement;
  uint16                 ElementEffects[] = 5;
  string                 OtherElementEffectsDescriptions[];
};
```

## <a name="members"></a><span data-ttu-id="7c3a8-107">Membres</span><span class="sxs-lookup"><span data-stu-id="7c3a8-107">Members</span></span>

<span data-ttu-id="7c3a8-108">La classe **MSVM \_ ServiceAffectsElement** possède les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="7c3a8-108">The **Msvm\_ServiceAffectsElement** class has these types of members:</span></span>

-   [<span data-ttu-id="7c3a8-109">Propriétés</span><span class="sxs-lookup"><span data-stu-id="7c3a8-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="7c3a8-110">Propriétés</span><span class="sxs-lookup"><span data-stu-id="7c3a8-110">Properties</span></span>

<span data-ttu-id="7c3a8-111">La classe **MSVM \_ ServiceAffectsElement** possède les propriétés suivantes.</span><span class="sxs-lookup"><span data-stu-id="7c3a8-111">The **Msvm\_ServiceAffectsElement** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="7c3a8-112">**AffectedElement**</span><span class="sxs-lookup"><span data-stu-id="7c3a8-112">**AffectedElement**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7c3a8-113">Type de données : **[ **CIM \_ propriété ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)**</span><span class="sxs-lookup"><span data-stu-id="7c3a8-113">Data type: **[**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)**</span></span>
</dt> <dt>

<span data-ttu-id="7c3a8-114">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="7c3a8-114">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="7c3a8-115">Référence à l’ordinateur virtuel.</span><span class="sxs-lookup"><span data-stu-id="7c3a8-115">A reference to the virtual machine.</span></span> <span data-ttu-id="7c3a8-116">Cette propriété est héritée de la [**\_ ServiceAffectsElement CIM**](/previous-versions//cc136907(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="7c3a8-116">This property is inherited from [**CIM\_ServiceAffectsElement**](/previous-versions//cc136907(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="7c3a8-117">**AffectingElement**</span><span class="sxs-lookup"><span data-stu-id="7c3a8-117">**AffectingElement**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7c3a8-118">Type de données : **[ **\_ service CIM**](/windows/desktop/CIMWin32Prov/cim-service)**</span><span class="sxs-lookup"><span data-stu-id="7c3a8-118">Data type: **[**CIM\_Service**](/windows/desktop/CIMWin32Prov/cim-service)**</span></span>
</dt> <dt>

<span data-ttu-id="7c3a8-119">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="7c3a8-119">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="7c3a8-120">Référence au service qui contrôle l’ordinateur virtuel.</span><span class="sxs-lookup"><span data-stu-id="7c3a8-120">A reference to the service that controls the virtual machine.</span></span> <span data-ttu-id="7c3a8-121">Cette propriété est héritée de la [**\_ ServiceAffectsElement CIM**](/previous-versions//cc136907(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="7c3a8-121">This property is inherited from [**CIM\_ServiceAffectsElement**](/previous-versions//cc136907(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="7c3a8-122">**ElementEffects**</span><span class="sxs-lookup"><span data-stu-id="7c3a8-122">**ElementEffects**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7c3a8-123">Type de données : tableau **UInt16**</span><span class="sxs-lookup"><span data-stu-id="7c3a8-123">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="7c3a8-124">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="7c3a8-124">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="7c3a8-125">Spécifie le type de contrôle représenté par l’Association.</span><span class="sxs-lookup"><span data-stu-id="7c3a8-125">Specifies the type of control that the association represents.</span></span> <span data-ttu-id="7c3a8-126">Cette propriété est héritée de la [**\_ ServiceAffectsElement CIM**](/previous-versions//cc136907(v=vs.85))et est toujours définie sur la valeur suivante.</span><span class="sxs-lookup"><span data-stu-id="7c3a8-126">This property is inherited from [**CIM\_ServiceAffectsElement**](/previous-versions//cc136907(v=vs.85)), and it is always set to the following value.</span></span>



| <span data-ttu-id="7c3a8-127">Valeur</span><span class="sxs-lookup"><span data-stu-id="7c3a8-127">Value</span></span>                                                                        | <span data-ttu-id="7c3a8-128">Signification</span><span class="sxs-lookup"><span data-stu-id="7c3a8-128">Meaning</span></span>            |
|------------------------------------------------------------------------------|--------------------|
| <dl> <span data-ttu-id="7c3a8-129"><dt>5</dt></span><span class="sxs-lookup"><span data-stu-id="7c3a8-129"><dt>5</dt></span></span> </dl> | <span data-ttu-id="7c3a8-130">Gère</span><span class="sxs-lookup"><span data-stu-id="7c3a8-130">Manages</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="7c3a8-131">**OtherElementEffectsDescriptions**</span><span class="sxs-lookup"><span data-stu-id="7c3a8-131">**OtherElementEffectsDescriptions**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7c3a8-132">Type de données : tableau de **chaînes**</span><span class="sxs-lookup"><span data-stu-id="7c3a8-132">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="7c3a8-133">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="7c3a8-133">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="7c3a8-134">Détails du type d’association à la position de tableau correspondante dans le tableau de propriétés **ElementAffects** .</span><span class="sxs-lookup"><span data-stu-id="7c3a8-134">The details for the type of association at the corresponding array position in the **ElementAffects** property array.</span></span> <span data-ttu-id="7c3a8-135">Ces informations sont requises si **ElementAffects** a la valeur 1 (autre).</span><span class="sxs-lookup"><span data-stu-id="7c3a8-135">This information is required if **ElementAffects** is set to 1 (Other).</span></span> <span data-ttu-id="7c3a8-136">Cette propriété est héritée de [**CIM \_ ServiceAffectsElement**](/previous-versions//cc136907(v=vs.85))et est toujours définie sur **null**.</span><span class="sxs-lookup"><span data-stu-id="7c3a8-136">This property is inherited from [**CIM\_ServiceAffectsElement**](/previous-versions//cc136907(v=vs.85)), and it is always set to **Null**.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="7c3a8-137">Notes</span><span class="sxs-lookup"><span data-stu-id="7c3a8-137">Remarks</span></span>

<span data-ttu-id="7c3a8-138">L’accès à la classe **MSVM \_ ServiceAffectsElement** peut être limité par le filtrage UAC.</span><span class="sxs-lookup"><span data-stu-id="7c3a8-138">Access to the **Msvm\_ServiceAffectsElement** class might be restricted by UAC Filtering.</span></span> <span data-ttu-id="7c3a8-139">Pour plus d’informations, consultez [contrôle de compte d’utilisateur et WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span><span class="sxs-lookup"><span data-stu-id="7c3a8-139">For more information, see [User Account Control and WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span></span>

## <a name="requirements"></a><span data-ttu-id="7c3a8-140">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="7c3a8-140">Requirements</span></span>



| <span data-ttu-id="7c3a8-141">Condition requise</span><span class="sxs-lookup"><span data-stu-id="7c3a8-141">Requirement</span></span> | <span data-ttu-id="7c3a8-142">Valeur</span><span class="sxs-lookup"><span data-stu-id="7c3a8-142">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7c3a8-143">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="7c3a8-143">Minimum supported client</span></span><br/> | <span data-ttu-id="7c3a8-144">Applications de \[ Bureau Windows 8 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="7c3a8-144">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="7c3a8-145">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="7c3a8-145">Minimum supported server</span></span><br/> | <span data-ttu-id="7c3a8-146">Applications de bureau Windows Server 2012 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="7c3a8-146">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="7c3a8-147">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="7c3a8-147">Namespace</span></span><br/>                | <span data-ttu-id="7c3a8-148">\\Virtualisation racine \\ v2</span><span class="sxs-lookup"><span data-stu-id="7c3a8-148">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="7c3a8-149">MOF</span><span class="sxs-lookup"><span data-stu-id="7c3a8-149">MOF</span></span><br/>                      | <dl> <span data-ttu-id="7c3a8-150"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="7c3a8-150"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="7c3a8-151">DLL</span><span class="sxs-lookup"><span data-stu-id="7c3a8-151">DLL</span></span><br/>                      | <dl> <span data-ttu-id="7c3a8-152"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="7c3a8-152"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="7c3a8-153">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="7c3a8-153">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7c3a8-154">**\_SERVICEAFFECTSELEMENT CIM**</span><span class="sxs-lookup"><span data-stu-id="7c3a8-154">**CIM\_ServiceAffectsElement**</span></span>](cim-serviceaffectselement.md)
</dt> <dt>

<span data-ttu-id="7c3a8-155">[**\_SERVICEAFFECTSELEMENT CIM**](/previous-versions//cc136907(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="7c3a8-155">[**CIM\_ServiceAffectsElement**](/previous-versions//cc136907(v=vs.85))</span></span>
</dt> </dl>

 

