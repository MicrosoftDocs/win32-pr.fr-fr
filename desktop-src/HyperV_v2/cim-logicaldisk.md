---
description: Représente une plage contiguë de blocs logiques qui est identifiable par un système de fichiers par le biais du champ de l’ID de périphérique (clé) de disques.
ms.assetid: a70b4bee-7f5d-43b1-a7cc-7f0593bc8a11
title: Classe CIM_LogicalDisk (gestion Hyper-V)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_LogicalDisk
- CIM_LogicalDisk.NameFormat
- CIM_LogicalDisk.NameNamespace
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: b7305d0fa6ef45b5a97eb0fb6ab9ea740c98a392
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103952525"
---
# <a name="cim_logicaldisk-class-hyper-v-management"></a><span data-ttu-id="81d46-103">Classe CIM_LogicalDisk (gestion Hyper-V)</span><span class="sxs-lookup"><span data-stu-id="81d46-103">CIM_LogicalDisk class (Hyper-V management)</span></span>

<span data-ttu-id="81d46-104">Représente une plage contiguë de blocs logiques qui est identifiable par un système de fichiers par le biais du champ **DeviceID** (Key) du disque.</span><span class="sxs-lookup"><span data-stu-id="81d46-104">Represents a contiguous range of logical blocks that is identifiable by a file system through the disk's **DeviceID** (key) field.</span></span> <span data-ttu-id="81d46-105">Par exemple, dans un environnement Windows, le champ **DeviceID** contient une lettre de lecteur. dans un environnement UNIX, elle contient le chemin d’accès ; dans un environnement NetWare, il contient le nom du volume.</span><span class="sxs-lookup"><span data-stu-id="81d46-105">For example, in a Windows environment, the **DeviceID** field contains a drive letter; in a UNIX environment, it contains the access path; and in a NetWare environment, it contains the volume name.</span></span>

## <a name="syntax"></a><span data-ttu-id="81d46-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="81d46-106">Syntax</span></span>

``` syntax
[Abstract, Version("2.15.0"), UMLPackagePath("CIM::Device::StorageExtents"), AMENDMENT]
class CIM_LogicalDisk : CIM_StorageExtent
{
  uint16 NameFormat = 12;
  uint16 NameNamespace = 8;
};
```

## <a name="members"></a><span data-ttu-id="81d46-107">Membres</span><span class="sxs-lookup"><span data-stu-id="81d46-107">Members</span></span>

<span data-ttu-id="81d46-108">La classe de **\_ disque logique CIM** possède les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="81d46-108">The **CIM\_LogicalDisk** class has these types of members:</span></span>

-   [<span data-ttu-id="81d46-109">Propriétés</span><span class="sxs-lookup"><span data-stu-id="81d46-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="81d46-110">Propriétés</span><span class="sxs-lookup"><span data-stu-id="81d46-110">Properties</span></span>

<span data-ttu-id="81d46-111">La classe de **\_ disque logique CIM** possède ces propriétés.</span><span class="sxs-lookup"><span data-stu-id="81d46-111">The **CIM\_LogicalDisk** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="81d46-112">**NameFormat**</span><span class="sxs-lookup"><span data-stu-id="81d46-112">**NameFormat**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="81d46-113">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="81d46-113">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="81d46-114">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="81d46-114">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="81d46-115">Qualificateurs : [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("NameFormat")</span><span class="sxs-lookup"><span data-stu-id="81d46-115">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("NameFormat")</span></span>
</dt> </dl>

<span data-ttu-id="81d46-116">Indique si l’appareil logique utilise le format de nom du système d’exploitation.</span><span class="sxs-lookup"><span data-stu-id="81d46-116">Indicates whether the logical device uses the name format of the OS.</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="81d46-117">**Autre** (1)</span><span class="sxs-lookup"><span data-stu-id="81d46-117">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="OS_Device_Name"></span><span id="os_device_name"></span><span id="OS_DEVICE_NAME"></span>

<span data-ttu-id="81d46-118">**Nom du périphérique du système d’exploitation** (12)</span><span class="sxs-lookup"><span data-stu-id="81d46-118">**OS Device Name** (12)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="81d46-119">**NameNamespace**</span><span class="sxs-lookup"><span data-stu-id="81d46-119">**NameNamespace**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="81d46-120">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="81d46-120">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="81d46-121">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="81d46-121">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="81d46-122">Qualificateurs : [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("NameNamespace")</span><span class="sxs-lookup"><span data-stu-id="81d46-122">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("NameNamespace")</span></span>
</dt> </dl>

<span data-ttu-id="81d46-123">Indique si l’unité logique a le même espace de noms que le système d’exploitation.</span><span class="sxs-lookup"><span data-stu-id="81d46-123">Indicates whether the logical device has the same namespace as the OS.</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="81d46-124">**Autre** (1)</span><span class="sxs-lookup"><span data-stu-id="81d46-124">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="OS_Device_Namespace"></span><span id="os_device_namespace"></span><span id="OS_DEVICE_NAMESPACE"></span>

<span data-ttu-id="81d46-125">**Espace de noms du périphérique du système d’exploitation** (8)</span><span class="sxs-lookup"><span data-stu-id="81d46-125">**OS Device Namespace** (8)</span></span>


<span data-ttu-id="81d46-126"></dt> <dd></dd> </dl>

</dd> </dl></span><span class="sxs-lookup"><span data-stu-id="81d46-126"></dt> <dd></dd> </dl>

</dd> </dl></span></span>

## <a name="requirements"></a><span data-ttu-id="81d46-127">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="81d46-127">Requirements</span></span>



| <span data-ttu-id="81d46-128">Condition requise</span><span class="sxs-lookup"><span data-stu-id="81d46-128">Requirement</span></span> | <span data-ttu-id="81d46-129">Valeur</span><span class="sxs-lookup"><span data-stu-id="81d46-129">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="81d46-130">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="81d46-130">Minimum supported client</span></span><br/> | <span data-ttu-id="81d46-131">Windows 8</span><span class="sxs-lookup"><span data-stu-id="81d46-131">Windows 8</span></span><br/>                                                                                    |
| <span data-ttu-id="81d46-132">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="81d46-132">Minimum supported server</span></span><br/> | <span data-ttu-id="81d46-133">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="81d46-133">Windows Server 2012</span></span><br/>                                                                          |
| <span data-ttu-id="81d46-134">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="81d46-134">Namespace</span></span><br/>                | <span data-ttu-id="81d46-135">\\Virtualisation racine \\ v2</span><span class="sxs-lookup"><span data-stu-id="81d46-135">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="81d46-136">MOF</span><span class="sxs-lookup"><span data-stu-id="81d46-136">MOF</span></span><br/>                      | <dl> <span data-ttu-id="81d46-137"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="81d46-137"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="81d46-138">DLL</span><span class="sxs-lookup"><span data-stu-id="81d46-138">DLL</span></span><br/>                      | <dl> <span data-ttu-id="81d46-139"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="81d46-139"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="81d46-140">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="81d46-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="81d46-141">**\_STORAGEEXTENT CIM**</span><span class="sxs-lookup"><span data-stu-id="81d46-141">**CIM\_StorageExtent**</span></span>](cim-storageextent.md)
</dt> </dl>

 

