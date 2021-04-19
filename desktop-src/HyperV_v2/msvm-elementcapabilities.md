---
description: Représente l’association entre les éléments managés et leurs fonctionnalités.
ms.assetid: F083E6D2-CC74-4DAD-8FF7-3FE3CA4EEFFF
title: Classe Msvm_ElementCapabilities
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_ElementCapabilities
- Msvm_ElementCapabilities.ManagedElement
- Msvm_ElementCapabilities.Capabilities
- Msvm_ElementCapabilities.Characteristics
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: d7602de569a51aec73130a4b5f4d3ba339cb29c6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106519386"
---
# <a name="msvm_elementcapabilities-class"></a><span data-ttu-id="375a3-103">MSVM \_ ElementCapabilities, classe</span><span class="sxs-lookup"><span data-stu-id="375a3-103">Msvm\_ElementCapabilities class</span></span>

<span data-ttu-id="375a3-104">Représente l’association entre les éléments managés et leurs fonctionnalités.</span><span class="sxs-lookup"><span data-stu-id="375a3-104">Represents the association between managed elements and their capabilities.</span></span>

<span data-ttu-id="375a3-105">La syntaxe suivante est simplifiée format MOF (MOF) et comprend toutes les propriétés héritées.</span><span class="sxs-lookup"><span data-stu-id="375a3-105">The following syntax is simplified Managed Object Format (MOF) code, and it includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="375a3-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="375a3-106">Syntax</span></span>

``` syntax
[Association, Aggregation, Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_ElementCapabilities : CIM_ElementCapabilities
{
  CIM_ManagedElement REF ManagedElement;
  CIM_Capabilities   REF Capabilities;
  uint16                 Characteristics[];
};
```

## <a name="members"></a><span data-ttu-id="375a3-107">Membres</span><span class="sxs-lookup"><span data-stu-id="375a3-107">Members</span></span>

<span data-ttu-id="375a3-108">La classe **MSVM \_ ElementCapabilities** possède les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="375a3-108">The **Msvm\_ElementCapabilities** class has these types of members:</span></span>

-   [<span data-ttu-id="375a3-109">Propriétés</span><span class="sxs-lookup"><span data-stu-id="375a3-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="375a3-110">Propriétés</span><span class="sxs-lookup"><span data-stu-id="375a3-110">Properties</span></span>

<span data-ttu-id="375a3-111">La classe **MSVM \_ ElementCapabilities** possède les propriétés suivantes.</span><span class="sxs-lookup"><span data-stu-id="375a3-111">The **Msvm\_ElementCapabilities** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="375a3-112">**Capabilities**</span><span class="sxs-lookup"><span data-stu-id="375a3-112">**Capabilities**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="375a3-113">Type de données : **[ **\_ fonctionnalités CIM**](/previous-versions//cc136806(v=vs.85))**</span><span class="sxs-lookup"><span data-stu-id="375a3-113">Data type: **[**CIM\_Capabilities**](/previous-versions//cc136806(v=vs.85))**</span></span>
</dt> <dt>

<span data-ttu-id="375a3-114">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="375a3-114">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="375a3-115">Qualificateurs : **clé**</span><span class="sxs-lookup"><span data-stu-id="375a3-115">Qualifiers: **Key**</span></span>
</dt> </dl>

<span data-ttu-id="375a3-116">Objet de fonctionnalités associé à l’élément.</span><span class="sxs-lookup"><span data-stu-id="375a3-116">The capabilities object associated with the element.</span></span> <span data-ttu-id="375a3-117">Cette propriété est héritée de la [**\_ ElementCapabilities CIM**](/previous-versions/windows/desktop/iscsitarg/cim-elementcapabilities).</span><span class="sxs-lookup"><span data-stu-id="375a3-117">This property is inherited from [**CIM\_ElementCapabilities**](/previous-versions/windows/desktop/iscsitarg/cim-elementcapabilities).</span></span>

</dd> <dt>

<span data-ttu-id="375a3-118">**Caractéristiques**</span><span class="sxs-lookup"><span data-stu-id="375a3-118">**Characteristics**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="375a3-119">Type de données : tableau **UInt16**</span><span class="sxs-lookup"><span data-stu-id="375a3-119">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="375a3-120">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="375a3-120">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="375a3-121">Fournit des informations descriptives sur les fonctionnalités de.</span><span class="sxs-lookup"><span data-stu-id="375a3-121">Provides descriptive information about the capabilities.</span></span> <span data-ttu-id="375a3-122">Cette propriété est héritée de la [**\_ ElementCapabilities CIM**](/previous-versions/windows/desktop/iscsitarg/cim-elementcapabilities).</span><span class="sxs-lookup"><span data-stu-id="375a3-122">This property is inherited from [**CIM\_ElementCapabilities**](/previous-versions/windows/desktop/iscsitarg/cim-elementcapabilities).</span></span>



| <span data-ttu-id="375a3-123">Valeur</span><span class="sxs-lookup"><span data-stu-id="375a3-123">Value</span></span>                                                                                                                                                                                                                       | <span data-ttu-id="375a3-124">Signification</span><span class="sxs-lookup"><span data-stu-id="375a3-124">Meaning</span></span>                                                                                           |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------|
| <span id="Default"></span><span id="default"></span><span id="DEFAULT"></span><dl> <span data-ttu-id="375a3-125"><dt>**Par défaut**</dt> <dt>2</dt></span><span class="sxs-lookup"><span data-stu-id="375a3-125"><dt>**Default**</dt> <dt>2</dt></span></span> </dl> | <span data-ttu-id="375a3-126">Les fonctionnalités associées représentent les fonctionnalités par défaut de l’élément géré.</span><span class="sxs-lookup"><span data-stu-id="375a3-126">The associated capabilities represent the default capabilities of the managed element.</span></span><br/> |
| <span id="Current"></span><span id="current"></span><span id="CURRENT"></span><dl> <span data-ttu-id="375a3-127"><dt>**Actuel**</dt> <dt>3</dt></span><span class="sxs-lookup"><span data-stu-id="375a3-127"><dt>**Current**</dt> <dt>3</dt></span></span> </dl> | <span data-ttu-id="375a3-128">Les fonctionnalités associées représentent les fonctionnalités actuelles de l’élément managé.</span><span class="sxs-lookup"><span data-stu-id="375a3-128">The associated capabilities represent the current capabilities of the managed element.</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="375a3-129">**Propriété ManagedElement**</span><span class="sxs-lookup"><span data-stu-id="375a3-129">**ManagedElement**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="375a3-130">Type de données : **[ **CIM \_ propriété ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)**</span><span class="sxs-lookup"><span data-stu-id="375a3-130">Data type: **[**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)**</span></span>
</dt> <dt>

<span data-ttu-id="375a3-131">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="375a3-131">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="375a3-132">Qualificateurs : **clé**, **min** (1)</span><span class="sxs-lookup"><span data-stu-id="375a3-132">Qualifiers: **Key**, **Min** ( 1 )</span></span>
</dt> </dl>

<span data-ttu-id="375a3-133">Élément managé.</span><span class="sxs-lookup"><span data-stu-id="375a3-133">The managed element.</span></span> <span data-ttu-id="375a3-134">Cette propriété est héritée de la [**\_ ElementCapabilities CIM**](/previous-versions/windows/desktop/iscsitarg/cim-elementcapabilities).</span><span class="sxs-lookup"><span data-stu-id="375a3-134">This property is inherited from [**CIM\_ElementCapabilities**](/previous-versions/windows/desktop/iscsitarg/cim-elementcapabilities).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="375a3-135">Notes</span><span class="sxs-lookup"><span data-stu-id="375a3-135">Remarks</span></span>

<span data-ttu-id="375a3-136">L’accès à la classe **MSVM \_ ElementCapabilities** peut être limité par le filtrage UAC.</span><span class="sxs-lookup"><span data-stu-id="375a3-136">Access to the **Msvm\_ElementCapabilities** class might be restricted by UAC Filtering.</span></span> <span data-ttu-id="375a3-137">Pour plus d’informations, consultez [contrôle de compte d’utilisateur et WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span><span class="sxs-lookup"><span data-stu-id="375a3-137">For more information, see [User Account Control and WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span></span>

## <a name="requirements"></a><span data-ttu-id="375a3-138">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="375a3-138">Requirements</span></span>



| <span data-ttu-id="375a3-139">Condition requise</span><span class="sxs-lookup"><span data-stu-id="375a3-139">Requirement</span></span> | <span data-ttu-id="375a3-140">Valeur</span><span class="sxs-lookup"><span data-stu-id="375a3-140">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="375a3-141">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="375a3-141">Minimum supported client</span></span><br/> | <span data-ttu-id="375a3-142">Applications de \[ Bureau Windows 8 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="375a3-142">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="375a3-143">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="375a3-143">Minimum supported server</span></span><br/> | <span data-ttu-id="375a3-144">Applications de bureau Windows Server 2012 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="375a3-144">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="375a3-145">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="375a3-145">Namespace</span></span><br/>                | <span data-ttu-id="375a3-146">\\Virtualisation racine \\ v2</span><span class="sxs-lookup"><span data-stu-id="375a3-146">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="375a3-147">MOF</span><span class="sxs-lookup"><span data-stu-id="375a3-147">MOF</span></span><br/>                      | <dl> <span data-ttu-id="375a3-148"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="375a3-148"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="375a3-149">DLL</span><span class="sxs-lookup"><span data-stu-id="375a3-149">DLL</span></span><br/>                      | <dl> <span data-ttu-id="375a3-150"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="375a3-150"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="375a3-151">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="375a3-151">See also</span></span>

<dl> <dt>

[<span data-ttu-id="375a3-152">**\_ELEMENTCAPABILITIES CIM**</span><span class="sxs-lookup"><span data-stu-id="375a3-152">**CIM\_ElementCapabilities**</span></span>](cim-elementcapabilities.md)
</dt> <dt>

[<span data-ttu-id="375a3-153">**\_ELEMENTCAPABILITIES CIM**</span><span class="sxs-lookup"><span data-stu-id="375a3-153">**CIM\_ElementCapabilities**</span></span>](/previous-versions/windows/desktop/iscsitarg/cim-elementcapabilities)
</dt> <dt>

[<span data-ttu-id="375a3-154">**MSVM \_ ElementCapabilities (v1)**</span><span class="sxs-lookup"><span data-stu-id="375a3-154">**Msvm\_ElementCapabilities (V1)**</span></span>](/previous-versions/windows/desktop/virtual/msvm-elementcapabilities)
</dt> </dl>

 

