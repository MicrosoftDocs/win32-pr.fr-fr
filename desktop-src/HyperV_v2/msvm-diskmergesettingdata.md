---
description: Représente l’état de configuration des paramètres de fusion de disque pour un ordinateur virtuel.
ms.assetid: b4c0afeb-ce37-4eec-8aba-0d74115c463f
title: Classe Msvm_DiskMergeSettingData
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_DiskMergeSettingData
- Msvm_DiskMergeSettingData.InstanceID
- Msvm_DiskMergeSettingData.Caption
- Msvm_DiskMergeSettingData.Description
- Msvm_DiskMergeSettingData.ElementName
- Msvm_DiskMergeSettingData.EnabledState
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: fe702c382fb0636579a8ab1355bfd1299657b214
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106524418"
---
# <a name="msvm_diskmergesettingdata-class"></a><span data-ttu-id="f84d2-103">MSVM \_ DiskMergeSettingData, classe</span><span class="sxs-lookup"><span data-stu-id="f84d2-103">Msvm\_DiskMergeSettingData class</span></span>

<span data-ttu-id="f84d2-104">Représente l’état de configuration des paramètres de fusion de disque pour un ordinateur virtuel.</span><span class="sxs-lookup"><span data-stu-id="f84d2-104">Represents the configuration state of the disk merge settings for a virtual machine.</span></span>

<span data-ttu-id="f84d2-105">La syntaxe suivante est simplifiée format MOF (MOF) et comprend toutes les propriétés héritées.</span><span class="sxs-lookup"><span data-stu-id="f84d2-105">The following syntax is simplified Managed Object Format (MOF) code, and it includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="f84d2-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="f84d2-106">Syntax</span></span>

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_DiskMergeSettingData : CIM_SettingData
{
  string InstanceID = "Microsoft:GUID\DeviceSpecificData";
  string Caption = "Disk Merge Setting Data";
  string Description = "Microsoft Disk Merge Setting Data";
  string ElementName = "Disk Merge Setting Data";
  uint32 EnabledState = 1;
};
```

## <a name="members"></a><span data-ttu-id="f84d2-107">Membres</span><span class="sxs-lookup"><span data-stu-id="f84d2-107">Members</span></span>

<span data-ttu-id="f84d2-108">La classe **MSVM \_ DiskMergeSettingData** possède les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="f84d2-108">The **Msvm\_DiskMergeSettingData** class has these types of members:</span></span>

-   [<span data-ttu-id="f84d2-109">Propriétés</span><span class="sxs-lookup"><span data-stu-id="f84d2-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="f84d2-110">Propriétés</span><span class="sxs-lookup"><span data-stu-id="f84d2-110">Properties</span></span>

<span data-ttu-id="f84d2-111">La classe **MSVM \_ DiskMergeSettingData** possède les propriétés suivantes.</span><span class="sxs-lookup"><span data-stu-id="f84d2-111">The **Msvm\_DiskMergeSettingData** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="f84d2-112">**Caption**</span><span class="sxs-lookup"><span data-stu-id="f84d2-112">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f84d2-113">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="f84d2-113">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f84d2-114">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="f84d2-114">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="f84d2-115">Brève description de l’objet.</span><span class="sxs-lookup"><span data-stu-id="f84d2-115">A short description of the object.</span></span> <span data-ttu-id="f84d2-116">Cette propriété est héritée de la classe [**CIM \_ propriété ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement) et a toujours la valeur « données de paramètre de fusion sur disque ».</span><span class="sxs-lookup"><span data-stu-id="f84d2-116">This property is inherited from the [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement) class and is always set to "Disk Merge Setting Data".</span></span>

</dd> <dt>

<span data-ttu-id="f84d2-117">**Description**</span><span class="sxs-lookup"><span data-stu-id="f84d2-117">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f84d2-118">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="f84d2-118">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f84d2-119">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="f84d2-119">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="f84d2-120">Description de l'objet .</span><span class="sxs-lookup"><span data-stu-id="f84d2-120">A description of the object.</span></span> <span data-ttu-id="f84d2-121">Cette propriété est héritée de [**CIM \_ propriété ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)et est toujours définie sur « données de paramètre de fusion de disque Microsoft ».</span><span class="sxs-lookup"><span data-stu-id="f84d2-121">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement), and it is always set to "Microsoft Disk Merge Setting Data".</span></span>

</dd> <dt>

<span data-ttu-id="f84d2-122">**ElementName**</span><span class="sxs-lookup"><span data-stu-id="f84d2-122">**ElementName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f84d2-123">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="f84d2-123">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f84d2-124">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="f84d2-124">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="f84d2-125">Nom complet de l’objet.</span><span class="sxs-lookup"><span data-stu-id="f84d2-125">A display name for the object.</span></span> <span data-ttu-id="f84d2-126">Cette propriété est héritée de [**CIM \_ SettingData**](/previous-versions//cc136911(v=vs.85))et est toujours définie sur « données de paramètre de fusion sur disque ».</span><span class="sxs-lookup"><span data-stu-id="f84d2-126">This property is inherited from [**CIM\_SettingData**](/previous-versions//cc136911(v=vs.85)), and it is always set to "Disk Merge Setting Data".</span></span> <span data-ttu-id="f84d2-127">La modification de cette propriété entraînera la modification de la propriété **ElementName** de la dérivée [**CIM CIM \_**](/windows/desktop/CIMWin32Prov/cim-logicaldevice) associée.</span><span class="sxs-lookup"><span data-stu-id="f84d2-127">Changing this property will change the **ElementName** property of the associated [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice) derivative.</span></span>

<span data-ttu-id="f84d2-128">Il s’agit d’une propriété en lecture seule, mais elle peut être modifiée à l’aide de la méthode [**ModifyResourceSettings**](modifyresourcesettings-msvm-virtualsystemmanagementservice.md) de la classe [**MSVM \_ VirtualSystemManagementService**](msvm-virtualsystemmanagementservice.md) .</span><span class="sxs-lookup"><span data-stu-id="f84d2-128">This is a read-only property, but it can be changed by using the [**ModifyResourceSettings**](modifyresourcesettings-msvm-virtualsystemmanagementservice.md) method of the [**Msvm\_VirtualSystemManagementService**](msvm-virtualsystemmanagementservice.md) class.</span></span>

</dd> <dt>

<span data-ttu-id="f84d2-129">**EnabledState**</span><span class="sxs-lookup"><span data-stu-id="f84d2-129">**EnabledState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f84d2-130">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="f84d2-130">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="f84d2-131">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="f84d2-131">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="f84d2-132">Spécifie l’état activé de la fonctionnalité de fusion de disque.</span><span class="sxs-lookup"><span data-stu-id="f84d2-132">Specifies the enabled state of the disk merge functionality.</span></span>

<dt>

<span id="Temporarily_disabled"></span><span id="temporarily_disabled"></span><span id="TEMPORARILY_DISABLED"></span>

<span data-ttu-id="f84d2-133">**Désactivé temporairement** (0)</span><span class="sxs-lookup"><span data-stu-id="f84d2-133">**Temporarily disabled** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>

<span data-ttu-id="f84d2-134">**Activé** (1)</span><span class="sxs-lookup"><span data-stu-id="f84d2-134">**Enabled** (1)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="f84d2-135">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="f84d2-135">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f84d2-136">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="f84d2-136">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f84d2-137">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="f84d2-137">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f84d2-138">Qualificateurs : **clé**</span><span class="sxs-lookup"><span data-stu-id="f84d2-138">Qualifiers: **Key**</span></span>
</dt> </dl>

<span data-ttu-id="f84d2-139">Identifie de façon unique une instance de cette classe.</span><span class="sxs-lookup"><span data-stu-id="f84d2-139">Uniquely identifies an instance of this class.</span></span> <span data-ttu-id="f84d2-140">Cette propriété est héritée de la [**\_ SettingData CIM**](/previous-versions//cc136911(v=vs.85)) et est toujours définie sur « Microsoft :*GUID* \\ *DeviceSpecificData*».</span><span class="sxs-lookup"><span data-stu-id="f84d2-140">This property is inherited from [**CIM\_SettingData**](/previous-versions//cc136911(v=vs.85)) and is always set to "Microsoft:*GUID*\\*DeviceSpecificData*".</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="f84d2-141">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="f84d2-141">Requirements</span></span>



| <span data-ttu-id="f84d2-142">Condition requise</span><span class="sxs-lookup"><span data-stu-id="f84d2-142">Requirement</span></span> | <span data-ttu-id="f84d2-143">Valeur</span><span class="sxs-lookup"><span data-stu-id="f84d2-143">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f84d2-144">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="f84d2-144">Minimum supported client</span></span><br/> | <span data-ttu-id="f84d2-145">Applications de \[ Bureau Windows 8 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="f84d2-145">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="f84d2-146">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="f84d2-146">Minimum supported server</span></span><br/> | <span data-ttu-id="f84d2-147">Applications de bureau Windows Server 2012 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="f84d2-147">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="f84d2-148">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="f84d2-148">Namespace</span></span><br/>                | <span data-ttu-id="f84d2-149">\\Virtualisation racine \\ v2</span><span class="sxs-lookup"><span data-stu-id="f84d2-149">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="f84d2-150">MOF</span><span class="sxs-lookup"><span data-stu-id="f84d2-150">MOF</span></span><br/>                      | <dl> <span data-ttu-id="f84d2-151"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="f84d2-151"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="f84d2-152">DLL</span><span class="sxs-lookup"><span data-stu-id="f84d2-152">DLL</span></span><br/>                      | <dl> <span data-ttu-id="f84d2-153"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="f84d2-153"><dt>Vmms.exe</dt></span></span> </dl>                     |



 

