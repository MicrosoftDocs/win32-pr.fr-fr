---
description: Contient des informations sur une unité de traitement graphique (GPU) physique RemoteFX.
ms.assetid: 86B47AAE-DBFF-43EF-88C6-44836D6C3AFA
title: Classe Msvm_PhysicalGPUInfo
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_PhysicalGPUInfo
- Msvm_PhysicalGPUInfo.InstanceID
- Msvm_PhysicalGPUInfo.Caption
- Msvm_PhysicalGPUInfo.Description
- Msvm_PhysicalGPUInfo.ElementName
- Msvm_PhysicalGPUInfo.Name
- Msvm_PhysicalGPUInfo.ID
- Msvm_PhysicalGPUInfo.TotalVideoMemory
- Msvm_PhysicalGPUInfo.AvailableVideoMemory
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: cd4ccf65b364620e84063ea6398c59dd0e467f67
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106524686"
---
# <a name="msvm_physicalgpuinfo-class"></a><span data-ttu-id="6bcb1-103">MSVM \_ PhysicalGPUInfo, classe</span><span class="sxs-lookup"><span data-stu-id="6bcb1-103">Msvm\_PhysicalGPUInfo class</span></span>

<span data-ttu-id="6bcb1-104">Contient des informations sur une unité de traitement graphique (GPU) physique RemoteFX.</span><span class="sxs-lookup"><span data-stu-id="6bcb1-104">Contains information about a RemoteFX physical graphics processing unit (GPU).</span></span>

<span data-ttu-id="6bcb1-105">La syntaxe suivante est simplifiée format MOF (MOF) et comprend toutes les propriétés héritées.</span><span class="sxs-lookup"><span data-stu-id="6bcb1-105">The following syntax is simplified Managed Object Format (MOF) code, and it includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="6bcb1-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="6bcb1-106">Syntax</span></span>

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_PhysicalGPUInfo : CIM_ManagedElement
{
  string InstanceID;
  string Caption;
  string Description;
  string ElementName;
  string Name;
  string ID;
  uint64 TotalVideoMemory;
  uint64 AvailableVideoMemory;
};
```

## <a name="members"></a><span data-ttu-id="6bcb1-107">Membres</span><span class="sxs-lookup"><span data-stu-id="6bcb1-107">Members</span></span>

<span data-ttu-id="6bcb1-108">La classe **MSVM \_ PhysicalGPUInfo** possède les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="6bcb1-108">The **Msvm\_PhysicalGPUInfo** class has these types of members:</span></span>

-   [<span data-ttu-id="6bcb1-109">Propriétés</span><span class="sxs-lookup"><span data-stu-id="6bcb1-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="6bcb1-110">Propriétés</span><span class="sxs-lookup"><span data-stu-id="6bcb1-110">Properties</span></span>

<span data-ttu-id="6bcb1-111">La classe **MSVM \_ PhysicalGPUInfo** possède les propriétés suivantes.</span><span class="sxs-lookup"><span data-stu-id="6bcb1-111">The **Msvm\_PhysicalGPUInfo** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="6bcb1-112">**AvailableVideoMemory**</span><span class="sxs-lookup"><span data-stu-id="6bcb1-112">**AvailableVideoMemory**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6bcb1-113">Type de données : **UInt64**</span><span class="sxs-lookup"><span data-stu-id="6bcb1-113">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="6bcb1-114">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="6bcb1-114">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="6bcb1-115">Quantité de mémoire vidéo inutilisée, en octets, sur le GPU physique qui peut être utilisé par RemoteFX.</span><span class="sxs-lookup"><span data-stu-id="6bcb1-115">The amount of unused video memory, in bytes, on the physical GPU that can be used by RemoteFX.</span></span>

</dd> <dt>

<span data-ttu-id="6bcb1-116">**Caption**</span><span class="sxs-lookup"><span data-stu-id="6bcb1-116">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6bcb1-117">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="6bcb1-117">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="6bcb1-118">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="6bcb1-118">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="6bcb1-119">Brève description de l’objet.</span><span class="sxs-lookup"><span data-stu-id="6bcb1-119">A short description of the object.</span></span> <span data-ttu-id="6bcb1-120">Cette propriété est héritée de la [**\_ propriété ManagedElement CIM**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="6bcb1-120">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="6bcb1-121">**Description**</span><span class="sxs-lookup"><span data-stu-id="6bcb1-121">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6bcb1-122">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="6bcb1-122">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="6bcb1-123">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="6bcb1-123">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="6bcb1-124">Description de l'objet .</span><span class="sxs-lookup"><span data-stu-id="6bcb1-124">A description of the object.</span></span> <span data-ttu-id="6bcb1-125">Cette propriété est héritée de la [**\_ propriété ManagedElement CIM**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="6bcb1-125">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="6bcb1-126">**ElementName**</span><span class="sxs-lookup"><span data-stu-id="6bcb1-126">**ElementName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6bcb1-127">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="6bcb1-127">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="6bcb1-128">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="6bcb1-128">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="6bcb1-129">Nom complet de l’objet.</span><span class="sxs-lookup"><span data-stu-id="6bcb1-129">A display name for the object.</span></span> <span data-ttu-id="6bcb1-130">Cette propriété est héritée de la [**\_ propriété ManagedElement CIM**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="6bcb1-130">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="6bcb1-131">**Identifiant**</span><span class="sxs-lookup"><span data-stu-id="6bcb1-131">**ID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6bcb1-132">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="6bcb1-132">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="6bcb1-133">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="6bcb1-133">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="6bcb1-134">Qualificateurs : [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (1024)</span><span class="sxs-lookup"><span data-stu-id="6bcb1-134">Qualifiers: [**MAXLEN**](/windows/desktop/WmiSdk/standard-qualifiers) (1024)</span></span>
</dt> </dl>

<span data-ttu-id="6bcb1-135">Identificateur unique du GPU physique.</span><span class="sxs-lookup"><span data-stu-id="6bcb1-135">The unique identifier of the physical GPU.</span></span>

</dd> <dt>

<span data-ttu-id="6bcb1-136">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="6bcb1-136">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6bcb1-137">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="6bcb1-137">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="6bcb1-138">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="6bcb1-138">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="6bcb1-139">Qualificateurs : **clé**</span><span class="sxs-lookup"><span data-stu-id="6bcb1-139">Qualifiers: **Key**</span></span>
</dt> </dl>

<span data-ttu-id="6bcb1-140">Chaîne qui identifie de façon unique une instance de cette classe.</span><span class="sxs-lookup"><span data-stu-id="6bcb1-140">A string that uniquely identifies an instance of this class.</span></span> <span data-ttu-id="6bcb1-141">Cette propriété est héritée de la [**\_ propriété ManagedElement CIM**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="6bcb1-141">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="6bcb1-142">**Nom**</span><span class="sxs-lookup"><span data-stu-id="6bcb1-142">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6bcb1-143">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="6bcb1-143">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="6bcb1-144">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="6bcb1-144">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="6bcb1-145">Qualificateurs : [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (1024)</span><span class="sxs-lookup"><span data-stu-id="6bcb1-145">Qualifiers: [**MAXLEN**](/windows/desktop/WmiSdk/standard-qualifiers) (1024)</span></span>
</dt> </dl>

<span data-ttu-id="6bcb1-146">Nom complet du GPU physique.</span><span class="sxs-lookup"><span data-stu-id="6bcb1-146">The display name of the physical GPU.</span></span>

</dd> <dt>

<span data-ttu-id="6bcb1-147">**TotalVideoMemory**</span><span class="sxs-lookup"><span data-stu-id="6bcb1-147">**TotalVideoMemory**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6bcb1-148">Type de données : **UInt64**</span><span class="sxs-lookup"><span data-stu-id="6bcb1-148">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="6bcb1-149">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="6bcb1-149">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="6bcb1-150">Quantité totale de mémoire vidéo, en octets, sur le GPU physique qui peut être utilisé par RemoteFX.</span><span class="sxs-lookup"><span data-stu-id="6bcb1-150">The total amount of video memory, in bytes, on the physical GPU that can be used by RemoteFX.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="6bcb1-151">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="6bcb1-151">Requirements</span></span>



| <span data-ttu-id="6bcb1-152">Condition requise</span><span class="sxs-lookup"><span data-stu-id="6bcb1-152">Requirement</span></span> | <span data-ttu-id="6bcb1-153">Valeur</span><span class="sxs-lookup"><span data-stu-id="6bcb1-153">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6bcb1-154">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="6bcb1-154">Minimum supported client</span></span><br/> | <span data-ttu-id="6bcb1-155">Applications de \[ Bureau Windows 8 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="6bcb1-155">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="6bcb1-156">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="6bcb1-156">Minimum supported server</span></span><br/> | <span data-ttu-id="6bcb1-157">Applications de bureau Windows Server 2012 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="6bcb1-157">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="6bcb1-158">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="6bcb1-158">Namespace</span></span><br/>                | <span data-ttu-id="6bcb1-159">\\Virtualisation racine \\ v2</span><span class="sxs-lookup"><span data-stu-id="6bcb1-159">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="6bcb1-160">MOF</span><span class="sxs-lookup"><span data-stu-id="6bcb1-160">MOF</span></span><br/>                      | <dl> <span data-ttu-id="6bcb1-161"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="6bcb1-161"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="6bcb1-162">DLL</span><span class="sxs-lookup"><span data-stu-id="6bcb1-162">DLL</span></span><br/>                      | <dl> <span data-ttu-id="6bcb1-163"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="6bcb1-163"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="6bcb1-164">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="6bcb1-164">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6bcb1-165">**\_Propriété MANAGEDELEMENT CIM**</span><span class="sxs-lookup"><span data-stu-id="6bcb1-165">**CIM\_ManagedElement**</span></span>](cim-managedelement.md)
</dt> </dl>

 

