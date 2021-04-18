---
description: Représente les fonctionnalités et la gestion d’un lecteur de bande.
ms.assetid: 8140fd9a-8a12-43b4-bc61-ec143e5d754c
title: Classe CIM_TapeDrive (gestion Hyper-V)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_TapeDrive
- CIM_TapeDrive.EOTWarningZoneSize
- CIM_TapeDrive.MaxPartitionCount
- CIM_TapeDrive.Padding
- CIM_TapeDrive.MaxRewindTime
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: b92360388b71abcb0b67d30fddea9b4f5ed7920f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106519048"
---
# <a name="cim_tapedrive-class-hyper-v-management"></a><span data-ttu-id="c0e80-103">Classe CIM_TapeDrive (gestion Hyper-V)</span><span class="sxs-lookup"><span data-stu-id="c0e80-103">CIM_TapeDrive class (Hyper-V management)</span></span>

<span data-ttu-id="c0e80-104">Représente les fonctionnalités et la gestion d’un lecteur de bande.</span><span class="sxs-lookup"><span data-stu-id="c0e80-104">Represents the capabilities and management of a tape drive.</span></span>

## <a name="syntax"></a><span data-ttu-id="c0e80-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="c0e80-105">Syntax</span></span>

``` syntax
[Abstract, Version("2.6.0"), UMLPackagePath("CIM::Device::StorageDevices")]
class CIM_TapeDrive : CIM_MediaAccessDevice
{
  uint32 EOTWarningZoneSize;
  uint32 MaxPartitionCount;
  uint32 Padding;
  uint64 MaxRewindTime;
};
```

## <a name="members"></a><span data-ttu-id="c0e80-106">Membres</span><span class="sxs-lookup"><span data-stu-id="c0e80-106">Members</span></span>

<span data-ttu-id="c0e80-107">La **classe \_ CIM CIM** possède les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="c0e80-107">The **CIM\_TapeDrive** class has these types of members:</span></span>

-   [<span data-ttu-id="c0e80-108">Propriétés</span><span class="sxs-lookup"><span data-stu-id="c0e80-108">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="c0e80-109">Propriétés</span><span class="sxs-lookup"><span data-stu-id="c0e80-109">Properties</span></span>

<span data-ttu-id="c0e80-110">La **classe \_ CIM CIM** possède ces propriétés.</span><span class="sxs-lookup"><span data-stu-id="c0e80-110">The **CIM\_TapeDrive** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="c0e80-111">**EOTWarningZoneSize**</span><span class="sxs-lookup"><span data-stu-id="c0e80-111">**EOTWarningZoneSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c0e80-112">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="c0e80-112">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="c0e80-113">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="c0e80-113">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c0e80-114">Qualificateurs : [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("bytes"), **punitif** ("Byte")</span><span class="sxs-lookup"><span data-stu-id="c0e80-114">Qualifiers: [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("Bytes"), **PUnit** ("byte")</span></span>
</dt> </dl>

<span data-ttu-id="c0e80-115">Taille, en octets, de la zone désignée comme « fin de bande ».</span><span class="sxs-lookup"><span data-stu-id="c0e80-115">The size, in bytes, of the area designated as "end of tape".</span></span> <span data-ttu-id="c0e80-116">L’accès dans cette zone génère un avertissement de fin de bande.</span><span class="sxs-lookup"><span data-stu-id="c0e80-116">Access in this area generates an "end of tape" warning.</span></span>

</dd> <dt>

<span data-ttu-id="c0e80-117">**MaxPartitionCount**</span><span class="sxs-lookup"><span data-stu-id="c0e80-117">**MaxPartitionCount**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c0e80-118">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="c0e80-118">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="c0e80-119">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="c0e80-119">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c0e80-120">Nombre maximal de partitions pour le lecteur de bande.</span><span class="sxs-lookup"><span data-stu-id="c0e80-120">The maximum partition count for the tape drive.</span></span>

</dd> <dt>

<span data-ttu-id="c0e80-121">**MaxRewindTime**</span><span class="sxs-lookup"><span data-stu-id="c0e80-121">**MaxRewindTime**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c0e80-122">Type de données : **UInt64**</span><span class="sxs-lookup"><span data-stu-id="c0e80-122">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="c0e80-123">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="c0e80-123">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c0e80-124">Qualificateurs : [**unités**](/windows/desktop/WmiSdk/standard-qualifiers) (« millisecondes »), **punitif** (« deuxième \* 10 ^-3 »)</span><span class="sxs-lookup"><span data-stu-id="c0e80-124">Qualifiers: [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("MilliSeconds"), **PUnit** ("second \* 10^-3")</span></span>
</dt> </dl>

<span data-ttu-id="c0e80-125">Durée, en millisecondes, du déplacement du point le plus éloigné physiquement de la bande vers le début.</span><span class="sxs-lookup"><span data-stu-id="c0e80-125">The time, in milliseconds, to move from the most physically distant point on the tape to the beginning.</span></span>

</dd> <dt>

<span data-ttu-id="c0e80-126">**Remplissage**</span><span class="sxs-lookup"><span data-stu-id="c0e80-126">**Padding**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c0e80-127">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="c0e80-127">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="c0e80-128">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="c0e80-128">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c0e80-129">Qualificateurs : [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("bytes"), **punitif** ("Byte")</span><span class="sxs-lookup"><span data-stu-id="c0e80-129">Qualifiers: [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("Bytes"), **PUnit** ("byte")</span></span>
</dt> </dl>

<span data-ttu-id="c0e80-130">Nombre d’octets insérés entre les blocs sur le support de bande.</span><span class="sxs-lookup"><span data-stu-id="c0e80-130">The number of bytes inserted between blocks on tape media.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="c0e80-131">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="c0e80-131">Requirements</span></span>



| <span data-ttu-id="c0e80-132">Condition requise</span><span class="sxs-lookup"><span data-stu-id="c0e80-132">Requirement</span></span> | <span data-ttu-id="c0e80-133">Valeur</span><span class="sxs-lookup"><span data-stu-id="c0e80-133">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c0e80-134">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="c0e80-134">Minimum supported client</span></span><br/> | <span data-ttu-id="c0e80-135">Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="c0e80-135">Windows 8.1</span></span><br/>                                                                                  |
| <span data-ttu-id="c0e80-136">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="c0e80-136">Minimum supported server</span></span><br/> | <span data-ttu-id="c0e80-137">Windows Server 2012 R2</span><span class="sxs-lookup"><span data-stu-id="c0e80-137">Windows Server 2012 R2</span></span><br/>                                                                       |
| <span data-ttu-id="c0e80-138">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="c0e80-138">Namespace</span></span><br/>                | <span data-ttu-id="c0e80-139">\\Virtualisation racine \\ v2</span><span class="sxs-lookup"><span data-stu-id="c0e80-139">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="c0e80-140">MOF</span><span class="sxs-lookup"><span data-stu-id="c0e80-140">MOF</span></span><br/>                      | <dl> <span data-ttu-id="c0e80-141"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="c0e80-141"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="c0e80-142">DLL</span><span class="sxs-lookup"><span data-stu-id="c0e80-142">DLL</span></span><br/>                      | <dl> <span data-ttu-id="c0e80-143"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="c0e80-143"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="c0e80-144">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="c0e80-144">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c0e80-145">**\_MEDIAACCESSDEVICE CIM**</span><span class="sxs-lookup"><span data-stu-id="c0e80-145">**CIM\_MediaAccessDevice**</span></span>](cim-mediaaccessdevice.md)
</dt> </dl>

 

