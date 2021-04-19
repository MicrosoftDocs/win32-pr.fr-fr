---
description: Représente l’état configuré d’un port PCI Express.
ms.assetid: adb03dd7-5a47-47e6-a4e4-28224164150c
title: Classe Msvm_PciExpressSettingData
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_PciExpressSettingData
- Msvm_PciExpressSettingData.VirtualFunctions
- Msvm_PciExpressSettingData.VirtualSystemIdentifiers
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: c092cbc119506c4c52bc0565cd969426feffc481
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106530756"
---
# <a name="msvm_pciexpresssettingdata-class"></a><span data-ttu-id="67bed-103">MSVM \_ PciExpressSettingData, classe</span><span class="sxs-lookup"><span data-stu-id="67bed-103">Msvm\_PciExpressSettingData class</span></span>

<span data-ttu-id="67bed-104">Représente l’état configuré d’un port PCI Express.</span><span class="sxs-lookup"><span data-stu-id="67bed-104">Represents the configured state of a PCI Express port.</span></span>

<span data-ttu-id="67bed-105">La syntaxe suivante est simplifiée par rapport au code MOF (Managed Object Format) et inclut toutes les propriétés héritées.</span><span class="sxs-lookup"><span data-stu-id="67bed-105">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="67bed-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="67bed-106">Syntax</span></span>

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_PciExpressSettingData : CIM_ResourceAllocationSettingData
{
  uint16 VirtualFunctions[];
  string VirtualSystemIdentifiers[];
};
```

## <a name="members"></a><span data-ttu-id="67bed-107">Membres</span><span class="sxs-lookup"><span data-stu-id="67bed-107">Members</span></span>

<span data-ttu-id="67bed-108">La classe **MSVM \_ PciExpressSettingData** possède les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="67bed-108">The **Msvm\_PciExpressSettingData** class has these types of members:</span></span>

-   [<span data-ttu-id="67bed-109">Propriétés</span><span class="sxs-lookup"><span data-stu-id="67bed-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="67bed-110">Propriétés</span><span class="sxs-lookup"><span data-stu-id="67bed-110">Properties</span></span>

<span data-ttu-id="67bed-111">La classe **MSVM \_ PciExpressSettingData** possède les propriétés suivantes.</span><span class="sxs-lookup"><span data-stu-id="67bed-111">The **Msvm\_PciExpressSettingData** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="67bed-112">**VirtualFunctions**</span><span class="sxs-lookup"><span data-stu-id="67bed-112">**VirtualFunctions**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="67bed-113">Type de données : tableau **UInt16**</span><span class="sxs-lookup"><span data-stu-id="67bed-113">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="67bed-114">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="67bed-114">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="67bed-115">Numéro de fonction virtuelle à assigner à la machine virtuelle.</span><span class="sxs-lookup"><span data-stu-id="67bed-115">The virtual function number to assign to the VM.</span></span>

</dd> <dt>

<span data-ttu-id="67bed-116">**VirtualSystemIdentifiers**</span><span class="sxs-lookup"><span data-stu-id="67bed-116">**VirtualSystemIdentifiers**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="67bed-117">Type de données : tableau de **chaînes**</span><span class="sxs-lookup"><span data-stu-id="67bed-117">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="67bed-118">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="67bed-118">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="67bed-119">Qualificateurs : [**arrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("indexé")</span><span class="sxs-lookup"><span data-stu-id="67bed-119">Qualifiers: [**ArrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("Indexed")</span></span>
</dt> </dl>

<span data-ttu-id="67bed-120">Tableau de chaînes de forme libre des identificateurs de cette ressource présentée au système d’exploitation du système de l’ordinateur virtuel.</span><span class="sxs-lookup"><span data-stu-id="67bed-120">A free-form string array of identifiers of this resource presented to the virtual computer system's operating system.</span></span> <span data-ttu-id="67bed-121">Les index et valeurs par index sont définis par ressource (c’est-à-dire, pour chaque valeur de **resourceType** énumérée).</span><span class="sxs-lookup"><span data-stu-id="67bed-121">The indexes and values per index are defined on a per resource basis (that is, for each enumerated **ResourceType** value).</span></span> <span data-ttu-id="67bed-122">Cette propriété est définie sur « GUID ».</span><span class="sxs-lookup"><span data-stu-id="67bed-122">This property is set to "GUID".</span></span>

<span data-ttu-id="67bed-123">Il s’agit d’une propriété en lecture seule, mais elle peut être modifiée à l’aide de la méthode [**ModifyVirtualSystemResources**](/previous-versions/windows/desktop/virtual/modifyvirtualsystemresources-msvm-virtualsystemmanagementservice) de la classe SD.</span><span class="sxs-lookup"><span data-stu-id="67bed-123">This is a read-only property, but it can be changed using the [**ModifyVirtualSystemResources**](/previous-versions/windows/desktop/virtual/modifyvirtualsystemresources-msvm-virtualsystemmanagementservice) method of the sd class.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="67bed-124">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="67bed-124">Requirements</span></span>



| <span data-ttu-id="67bed-125">Condition requise</span><span class="sxs-lookup"><span data-stu-id="67bed-125">Requirement</span></span> | <span data-ttu-id="67bed-126">Valeur</span><span class="sxs-lookup"><span data-stu-id="67bed-126">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="67bed-127">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="67bed-127">Minimum supported client</span></span><br/> | <span data-ttu-id="67bed-128">Applications de bureau Windows 10, version 1703 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="67bed-128">Windows 10, version 1703 \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="67bed-129">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="67bed-129">Minimum supported server</span></span><br/> | <span data-ttu-id="67bed-130">Windows Server 2016</span><span class="sxs-lookup"><span data-stu-id="67bed-130">Windows Server 2016</span></span><br/>                                                                          |
| <span data-ttu-id="67bed-131">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="67bed-131">Namespace</span></span><br/>                | <span data-ttu-id="67bed-132">\\Virtualisation racine \\ v2</span><span class="sxs-lookup"><span data-stu-id="67bed-132">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="67bed-133">MOF</span><span class="sxs-lookup"><span data-stu-id="67bed-133">MOF</span></span><br/>                      | <dl> <span data-ttu-id="67bed-134"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="67bed-134"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="67bed-135">DLL</span><span class="sxs-lookup"><span data-stu-id="67bed-135">DLL</span></span><br/>                      | <dl> <span data-ttu-id="67bed-136"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="67bed-136"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="67bed-137">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="67bed-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="67bed-138">**\_RESOURCEALLOCATIONSETTINGDATA CIM**</span><span class="sxs-lookup"><span data-stu-id="67bed-138">**CIM\_ResourceAllocationSettingData**</span></span>](cim-resourceallocationsettingdata.md)
</dt> </dl>

 

