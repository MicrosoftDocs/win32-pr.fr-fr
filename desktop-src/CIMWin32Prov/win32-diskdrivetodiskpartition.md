---
description: La \_ classe WMI de l’Association DiskDriveToDiskPartition Win32 associe un lecteur de disque et une partition existante.
ms.assetid: 82953097-ebfb-42b8-84b4-fb4ed19f3525
ms.tgt_platform: multiple
title: Classe Win32_DiskDriveToDiskPartition
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_DiskDriveToDiskPartition
- Win32_DiskDriveToDiskPartition.Antecedent
- Win32_DiskDriveToDiskPartition.Dependent
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: b2bd5472bd4ad92ddde47f7d6a492916006a80cb
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106513326"
---
# <a name="win32_diskdrivetodiskpartition-class"></a><span data-ttu-id="459e3-103">\_Classe DiskDriveToDiskPartition Win32</span><span class="sxs-lookup"><span data-stu-id="459e3-103">Win32\_DiskDriveToDiskPartition class</span></span>

<span data-ttu-id="459e3-104">La [classe WMI](/windows/desktop/WmiSdk/retrieving-a-class) de l’Association **\_ DiskDriveToDiskPartition Win32** associe un lecteur de disque et une partition existante.</span><span class="sxs-lookup"><span data-stu-id="459e3-104">The **Win32\_DiskDriveToDiskPartition** association [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) relates a disk drive and a partition existing on it.</span></span>

<span data-ttu-id="459e3-105">La syntaxe suivante est simplifiée par rapport au code MOF (Managed Object Format) et inclut toutes les propriétés héritées.</span><span class="sxs-lookup"><span data-stu-id="459e3-105">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span> <span data-ttu-id="459e3-106">Les propriétés sont répertoriées par ordre alphabétique, et non par ordre MOF.</span><span class="sxs-lookup"><span data-stu-id="459e3-106">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="459e3-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="459e3-107">Syntax</span></span>

``` syntax
[Dynamic, Provider("CIMWin32"), UUID("{8502C4F9-5FBB-11D2-AAC1-006008C78BC7}"), AMENDMENT]
class Win32_DiskDriveToDiskPartition : CIM_MediaPresent
{
  Win32_DiskDrive     REF Antecedent;
  Win32_DiskPartition REF Dependent;
};
```

## <a name="members"></a><span data-ttu-id="459e3-108">Membres</span><span class="sxs-lookup"><span data-stu-id="459e3-108">Members</span></span>

<span data-ttu-id="459e3-109">La classe **Win32 \_ DiskDriveToDiskPartition** possède les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="459e3-109">The **Win32\_DiskDriveToDiskPartition** class has these types of members:</span></span>

-   [<span data-ttu-id="459e3-110">Propriétés</span><span class="sxs-lookup"><span data-stu-id="459e3-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="459e3-111">Propriétés</span><span class="sxs-lookup"><span data-stu-id="459e3-111">Properties</span></span>

<span data-ttu-id="459e3-112">La classe **Win32 \_ DiskDriveToDiskPartition** a ces propriétés.</span><span class="sxs-lookup"><span data-stu-id="459e3-112">The **Win32\_DiskDriveToDiskPartition** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="459e3-113">**Antécédent**</span><span class="sxs-lookup"><span data-stu-id="459e3-113">**Antecedent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="459e3-114">Type de données : **Win32 \_ DiskDrive**</span><span class="sxs-lookup"><span data-stu-id="459e3-114">Data type: **Win32\_DiskDrive**</span></span>
</dt> <dt>

<span data-ttu-id="459e3-115">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="459e3-115">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="459e3-116">Qualificateurs : [**clé**](/windows/desktop/WmiSdk/key-qualifier), [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Antecedent"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("WMI \| Win32 \_ DiskDrive")</span><span class="sxs-lookup"><span data-stu-id="459e3-116">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier), [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Antecedent"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("WMI\|Win32\_DiskDrive")</span></span>
</dt> </dl>

<span data-ttu-id="459e3-117">Référence à l’instance de qui représente les propriétés du lecteur de disque où se trouve la partition.</span><span class="sxs-lookup"><span data-stu-id="459e3-117">Reference to the instance representing the properties of the disk drive where the partition exists.</span></span>

</dd> <dt>

<span data-ttu-id="459e3-118">**Charge**</span><span class="sxs-lookup"><span data-stu-id="459e3-118">**Dependent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="459e3-119">Type de données : **Win32 \_ DiskPartition**</span><span class="sxs-lookup"><span data-stu-id="459e3-119">Data type: **Win32\_DiskPartition**</span></span>
</dt> <dt>

<span data-ttu-id="459e3-120">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="459e3-120">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="459e3-121">Qualificateurs : [**clé**](/windows/desktop/WmiSdk/key-qualifier), [**remplacement**](/windows/desktop/WmiSdk/standard-qualifiers) (« dépendant »), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) (« WMI \| Win32 \_ DiskPartition »)</span><span class="sxs-lookup"><span data-stu-id="459e3-121">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier), [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Dependent"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("WMI\|Win32\_DiskPartition")</span></span>
</dt> </dl>

<span data-ttu-id="459e3-122">Référence à l’instance de qui représente la partition de disque résidant sur le lecteur de disque.</span><span class="sxs-lookup"><span data-stu-id="459e3-122">Reference to the instance representing the disk partition residing on the disk drive.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="459e3-123">Notes</span><span class="sxs-lookup"><span data-stu-id="459e3-123">Remarks</span></span>

<span data-ttu-id="459e3-124">La classe **Win32 \_ DiskDriveToDiskPartition** est dérivée de [**CIM \_ MediaPresent**](cim-mediapresent.md).</span><span class="sxs-lookup"><span data-stu-id="459e3-124">The **Win32\_DiskDriveToDiskPartition** class is derived from [**CIM\_MediaPresent**](cim-mediapresent.md).</span></span>

<span data-ttu-id="459e3-125">Pour plus d’informations sur l’utilisation de cette classe, consultez les articles comment [Utiliser PowerShell pour mapper des lecteurs de disque et des partitions](https://blogs.technet.com/b/heyscriptingguy/archive/2012/12/17/use-powershell-to-map-disk-drives-and-partitions.aspx) et [Comment mettre en corrélation des lecteurs logiques et des disques physiques ?](https://blogs.technet.com/b/heyscriptingguy/archive/2005/05/23/how-can-i-correlate-logical-drives-and-physical-disks.aspx) .</span><span class="sxs-lookup"><span data-stu-id="459e3-125">For a discussion on how to use this class, see the [Use PowerShell to Map Disk Drives and Partitions](https://blogs.technet.com/b/heyscriptingguy/archive/2012/12/17/use-powershell-to-map-disk-drives-and-partitions.aspx) and the [How Can I Correlate Logical Drives and Physical Disks?](https://blogs.technet.com/b/heyscriptingguy/archive/2005/05/23/how-can-i-correlate-logical-drives-and-physical-disks.aspx) blog articles.</span></span>

## <a name="examples"></a><span data-ttu-id="459e3-126">Exemples</span><span class="sxs-lookup"><span data-stu-id="459e3-126">Examples</span></span>

<span data-ttu-id="459e3-127">L’exemple PowerShell [use PowerShell to gather disk/partition/point de montage](https://Gallery.TechNet.Microsoft.Com/Use-Powershell-to-Gather-b5c746d0) utilise **Win32 \_ DiskDriveToDiskPartition** pour retourner des informations sur les disques/partitions locaux et les points de montage.</span><span class="sxs-lookup"><span data-stu-id="459e3-127">The [Use Powershell to Gather Disk/Partition/Mount Point Information](https://Gallery.TechNet.Microsoft.Com/Use-Powershell-to-Gather-b5c746d0) PowerShell sample uses **Win32\_DiskDriveToDiskPartition** to return information about local disks/partitions and mount points.</span></span>

## <a name="requirements"></a><span data-ttu-id="459e3-128">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="459e3-128">Requirements</span></span>



| <span data-ttu-id="459e3-129">Condition requise</span><span class="sxs-lookup"><span data-stu-id="459e3-129">Requirement</span></span> | <span data-ttu-id="459e3-130">Valeur</span><span class="sxs-lookup"><span data-stu-id="459e3-130">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="459e3-131">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="459e3-131">Minimum supported client</span></span><br/> | <span data-ttu-id="459e3-132">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="459e3-132">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="459e3-133">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="459e3-133">Minimum supported server</span></span><br/> | <span data-ttu-id="459e3-134">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="459e3-134">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="459e3-135">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="459e3-135">Namespace</span></span><br/>                | <span data-ttu-id="459e3-136">\\Cimv2 racine</span><span class="sxs-lookup"><span data-stu-id="459e3-136">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="459e3-137">MOF</span><span class="sxs-lookup"><span data-stu-id="459e3-137">MOF</span></span><br/>                      | <dl> <span data-ttu-id="459e3-138"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="459e3-138"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="459e3-139">DLL</span><span class="sxs-lookup"><span data-stu-id="459e3-139">DLL</span></span><br/>                      | <dl> <span data-ttu-id="459e3-140"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="459e3-140"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="459e3-141">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="459e3-141">See also</span></span>

<dl> <dt>

[<span data-ttu-id="459e3-142">**\_MEDIAPRESENT CIM**</span><span class="sxs-lookup"><span data-stu-id="459e3-142">**CIM\_MediaPresent**</span></span>](cim-mediapresent.md)
</dt> <dt>

<span data-ttu-id="459e3-143">[Classes du système d’exploitation](/previous-versions//aa392727(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="459e3-143">[Operating System Classes](/previous-versions//aa392727(v=vs.85))</span></span>
</dt> <dt>

[<span data-ttu-id="459e3-144">Tâches WMI : disques et systèmes de fichiers</span><span class="sxs-lookup"><span data-stu-id="459e3-144">WMI Tasks: Disks and File Systems</span></span>](/windows/desktop/WmiSdk/wmi-tasks--disks-and-file-systems)
</dt> </dl>

 

