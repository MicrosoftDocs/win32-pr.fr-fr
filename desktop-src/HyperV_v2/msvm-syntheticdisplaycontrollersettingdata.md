---
description: Décrit les données de paramètre d’un contrôleur d’affichage synthétique virtuel.
ms.assetid: cea79b24-4175-49db-a8b4-a9efb1fd0b96
title: Classe Msvm_SyntheticDisplayControllerSettingData
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_SyntheticDisplayControllerSettingData
- Msvm_SyntheticDisplayControllerSettingData.ResolutionType
- Msvm_SyntheticDisplayControllerSettingData.HorizontalResolution
- Msvm_SyntheticDisplayControllerSettingData.VerticalResolution
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 52935800eda641eb9015247e9320f33f22b40251
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104202210"
---
# <a name="msvm_syntheticdisplaycontrollersettingdata-class"></a><span data-ttu-id="8b92a-103">MSVM \_ SyntheticDisplayControllerSettingData, classe</span><span class="sxs-lookup"><span data-stu-id="8b92a-103">Msvm\_SyntheticDisplayControllerSettingData class</span></span>

<span data-ttu-id="8b92a-104">Décrit les données de paramètre d’un contrôleur d’affichage synthétique virtuel.</span><span class="sxs-lookup"><span data-stu-id="8b92a-104">Describes the setting data for a virtual synthetic display controller.</span></span>

<span data-ttu-id="8b92a-105">La syntaxe suivante issue du code MOF est simplifiée et inclut toutes les propriétés héritées.</span><span class="sxs-lookup"><span data-stu-id="8b92a-105">The following syntax is simplified from MOF code and includes all inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="8b92a-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="8b92a-106">Syntax</span></span>

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_SyntheticDisplayControllerSettingData : CIM_ResourceAllocationSettingData
{
  uint8  ResolutionType;
  uint16 HorizontalResolution;
  uint16 VerticalResolution;
};
```

## <a name="members"></a><span data-ttu-id="8b92a-107">Membres</span><span class="sxs-lookup"><span data-stu-id="8b92a-107">Members</span></span>

<span data-ttu-id="8b92a-108">La classe **MSVM \_ SyntheticDisplayControllerSettingData** possède les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="8b92a-108">The **Msvm\_SyntheticDisplayControllerSettingData** class has these types of members:</span></span>

-   [<span data-ttu-id="8b92a-109">Propriétés</span><span class="sxs-lookup"><span data-stu-id="8b92a-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="8b92a-110">Propriétés</span><span class="sxs-lookup"><span data-stu-id="8b92a-110">Properties</span></span>

<span data-ttu-id="8b92a-111">La classe **MSVM \_ SyntheticDisplayControllerSettingData** possède les propriétés suivantes.</span><span class="sxs-lookup"><span data-stu-id="8b92a-111">The **Msvm\_SyntheticDisplayControllerSettingData** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="8b92a-112">**HorizontalResolution**</span><span class="sxs-lookup"><span data-stu-id="8b92a-112">**HorizontalResolution**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8b92a-113">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="8b92a-113">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="8b92a-114">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="8b92a-114">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="8b92a-115">Résolution horizontale.</span><span class="sxs-lookup"><span data-stu-id="8b92a-115">The horizontal resolution.</span></span>

</dd> <dt>

<span data-ttu-id="8b92a-116">**ResolutionType**</span><span class="sxs-lookup"><span data-stu-id="8b92a-116">**ResolutionType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8b92a-117">Type de données : **UInt8**</span><span class="sxs-lookup"><span data-stu-id="8b92a-117">Data type: **uint8**</span></span>
</dt> <dt>

<span data-ttu-id="8b92a-118">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="8b92a-118">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="8b92a-119">Type de résolution.</span><span class="sxs-lookup"><span data-stu-id="8b92a-119">The resolution type.</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="8b92a-120"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Inconnu** (0)</span><span class="sxs-lookup"><span data-stu-id="8b92a-120"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="8b92a-121"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Autre** (1)</span><span class="sxs-lookup"><span data-stu-id="8b92a-121"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Maximum"></span><span id="maximum"></span><span id="MAXIMUM"></span>

<span data-ttu-id="8b92a-122"><span id="Maximum"></span><span id="maximum"></span><span id="MAXIMUM"></span>**Maximum** (2)</span><span class="sxs-lookup"><span data-stu-id="8b92a-122"><span id="Maximum"></span><span id="maximum"></span><span id="MAXIMUM"></span>**Maximum** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Single"></span><span id="single"></span><span id="SINGLE"></span>

<span data-ttu-id="8b92a-123"><span id="Single"></span><span id="single"></span><span id="SINGLE"></span>**Unique** (3)</span><span class="sxs-lookup"><span data-stu-id="8b92a-123"><span id="Single"></span><span id="single"></span><span id="SINGLE"></span>**Single** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Default"></span><span id="default"></span><span id="DEFAULT"></span>

<span data-ttu-id="8b92a-124"><span id="Default"></span><span id="default"></span><span id="DEFAULT"></span>**Valeur par défaut** (4)</span><span class="sxs-lookup"><span data-stu-id="8b92a-124"><span id="Default"></span><span id="default"></span><span id="DEFAULT"></span>**Default** (4)</span></span>


</dt> <dd>

> [!Note]  
> <span data-ttu-id="8b92a-125">Ajouté dans Windows 10, version 1703.</span><span class="sxs-lookup"><span data-stu-id="8b92a-125">Added in Windows 10, version 1703.</span></span>

 

</dd> </dl>

</dd> <dt>

<span data-ttu-id="8b92a-126">**VerticalResolution**</span><span class="sxs-lookup"><span data-stu-id="8b92a-126">**VerticalResolution**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8b92a-127">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="8b92a-127">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="8b92a-128">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="8b92a-128">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="8b92a-129">Résolution verticale.</span><span class="sxs-lookup"><span data-stu-id="8b92a-129">The vertical resolution.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="8b92a-130">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="8b92a-130">Requirements</span></span>



| <span data-ttu-id="8b92a-131">Condition requise</span><span class="sxs-lookup"><span data-stu-id="8b92a-131">Requirement</span></span> | <span data-ttu-id="8b92a-132">Valeur</span><span class="sxs-lookup"><span data-stu-id="8b92a-132">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8b92a-133">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="8b92a-133">Minimum supported client</span></span><br/> | <span data-ttu-id="8b92a-134">Applications de \[ Bureau Windows 10 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="8b92a-134">Windows 10 \[desktop apps only\]</span></span><br/>                                                             |
| <span data-ttu-id="8b92a-135">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="8b92a-135">Minimum supported server</span></span><br/> | <span data-ttu-id="8b92a-136">Windows Server 2016</span><span class="sxs-lookup"><span data-stu-id="8b92a-136">Windows Server 2016</span></span><br/>                                                                          |
| <span data-ttu-id="8b92a-137">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="8b92a-137">Namespace</span></span><br/>                | <span data-ttu-id="8b92a-138">\\Virtualisation racine \\ v2</span><span class="sxs-lookup"><span data-stu-id="8b92a-138">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="8b92a-139">MOF</span><span class="sxs-lookup"><span data-stu-id="8b92a-139">MOF</span></span><br/>                      | <dl> <span data-ttu-id="8b92a-140"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="8b92a-140"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="8b92a-141">DLL</span><span class="sxs-lookup"><span data-stu-id="8b92a-141">DLL</span></span><br/>                      | <dl> <span data-ttu-id="8b92a-142"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="8b92a-142"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="8b92a-143">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="8b92a-143">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8b92a-144">**\_RESOURCEALLOCATIONSETTINGDATA CIM**</span><span class="sxs-lookup"><span data-stu-id="8b92a-144">**CIM\_ResourceAllocationSettingData**</span></span>](cim-resourceallocationsettingdata.md)
</dt> </dl>

 

 




