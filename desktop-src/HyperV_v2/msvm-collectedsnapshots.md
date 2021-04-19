---
description: Associe le \_ SnapshotCollection MSVM aux objets MSVM \_ VirtualSystemSettingData contenus.
ms.assetid: 21005e8a-0bc6-4ea7-8f6f-d79803b43bc0
title: Classe Msvm_CollectedSnapshots
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_CollectedSnapshots
- Msvm_CollectedSnapshots.Collection
- Msvm_CollectedSnapshots.Member
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 9c89e7c7390cc1f2cc0c3217fca93e3f2d2d01ec
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106536987"
---
# <a name="msvm_collectedsnapshots-class"></a><span data-ttu-id="abeff-103">MSVM \_ CollectedSnapshots, classe</span><span class="sxs-lookup"><span data-stu-id="abeff-103">Msvm\_CollectedSnapshots class</span></span>

<span data-ttu-id="abeff-104">Associe [**le \_ SnapshotCollection MSVM**](msvm-snapshotcollection.md) aux objets [**MSVM \_ VirtualSystemSettingData**](msvm-virtualsystemsettingdata.md) contenus.</span><span class="sxs-lookup"><span data-stu-id="abeff-104">Associates the [**Msvm\_SnapshotCollection**](msvm-snapshotcollection.md) to the contained [**Msvm\_VirtualSystemSettingData**](msvm-virtualsystemsettingdata.md) objects.</span></span>

<span data-ttu-id="abeff-105">La syntaxe suivante est simplifiée par rapport au code MOF (Managed Object Format) et inclut toutes les propriétés héritées.</span><span class="sxs-lookup"><span data-stu-id="abeff-105">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="abeff-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="abeff-106">Syntax</span></span>

``` syntax
[Association, Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_CollectedSnapshots : CIM_CollectedMSEs
{
  Msvm_SnapshotCollection       REF Collection;
  Msvm_VirtualSystemSettingData REF Member;
};
```

## <a name="members"></a><span data-ttu-id="abeff-107">Membres</span><span class="sxs-lookup"><span data-stu-id="abeff-107">Members</span></span>

<span data-ttu-id="abeff-108">La classe **MSVM \_ CollectedSnapshots** possède les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="abeff-108">The **Msvm\_CollectedSnapshots** class has these types of members:</span></span>

-   [<span data-ttu-id="abeff-109">Propriétés</span><span class="sxs-lookup"><span data-stu-id="abeff-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="abeff-110">Propriétés</span><span class="sxs-lookup"><span data-stu-id="abeff-110">Properties</span></span>

<span data-ttu-id="abeff-111">La classe **MSVM \_ CollectedSnapshots** possède les propriétés suivantes.</span><span class="sxs-lookup"><span data-stu-id="abeff-111">The **Msvm\_CollectedSnapshots** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="abeff-112">**Collection**</span><span class="sxs-lookup"><span data-stu-id="abeff-112">**Collection**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="abeff-113">Type de données : **MSVM \_ SnapshotCollection**</span><span class="sxs-lookup"><span data-stu-id="abeff-113">Data type: **Msvm\_SnapshotCollection**</span></span>
</dt> <dt>

<span data-ttu-id="abeff-114">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="abeff-114">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="abeff-115">Qualificateurs : [**Aggregate**](/windows/desktop/WmiSdk/standard-qualifiers), [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("collection")</span><span class="sxs-lookup"><span data-stu-id="abeff-115">Qualifiers: [**Aggregate**](/windows/desktop/WmiSdk/standard-qualifiers), [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Collection")</span></span>
</dt> </dl>

<span data-ttu-id="abeff-116">Un regroupement [**MSVM \_ SnapshotCollection**](msvm-snapshotcollection.md) ou un objet « Bag » qui représente la collection.</span><span class="sxs-lookup"><span data-stu-id="abeff-116">An [**Msvm\_SnapshotCollection**](msvm-snapshotcollection.md) grouping or 'bag' object that represents the collection.</span></span>

</dd> <dt>

<span data-ttu-id="abeff-117">**Membre**</span><span class="sxs-lookup"><span data-stu-id="abeff-117">**Member**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="abeff-118">Type de données : **MSVM \_ VirtualSystemSettingData**</span><span class="sxs-lookup"><span data-stu-id="abeff-118">Data type: **Msvm\_VirtualSystemSettingData**</span></span>
</dt> <dt>

<span data-ttu-id="abeff-119">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="abeff-119">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="abeff-120">Qualificateurs : [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Member")</span><span class="sxs-lookup"><span data-stu-id="abeff-120">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Member")</span></span>
</dt> </dl>

<span data-ttu-id="abeff-121">[**MSVM \_ VirtualSystemSettingData**](msvm-virtualsystemsettingdata.md) contenant les membres de la collection.</span><span class="sxs-lookup"><span data-stu-id="abeff-121">An [**Msvm\_VirtualSystemSettingData**](msvm-virtualsystemsettingdata.md) containing the members of the collection.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="abeff-122">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="abeff-122">Requirements</span></span>



| <span data-ttu-id="abeff-123">Condition requise</span><span class="sxs-lookup"><span data-stu-id="abeff-123">Requirement</span></span> | <span data-ttu-id="abeff-124">Valeur</span><span class="sxs-lookup"><span data-stu-id="abeff-124">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="abeff-125">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="abeff-125">Minimum supported client</span></span><br/> | <span data-ttu-id="abeff-126">Applications de \[ Bureau Windows 10 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="abeff-126">Windows 10 \[desktop apps only\]</span></span><br/>                                                             |
| <span data-ttu-id="abeff-127">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="abeff-127">Minimum supported server</span></span><br/> | <span data-ttu-id="abeff-128">Windows Server 2016</span><span class="sxs-lookup"><span data-stu-id="abeff-128">Windows Server 2016</span></span><br/>                                                                          |
| <span data-ttu-id="abeff-129">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="abeff-129">Namespace</span></span><br/>                | <span data-ttu-id="abeff-130">\\Virtualisation racine \\ v2</span><span class="sxs-lookup"><span data-stu-id="abeff-130">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="abeff-131">MOF</span><span class="sxs-lookup"><span data-stu-id="abeff-131">MOF</span></span><br/>                      | <dl> <span data-ttu-id="abeff-132"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="abeff-132"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="abeff-133">DLL</span><span class="sxs-lookup"><span data-stu-id="abeff-133">DLL</span></span><br/>                      | <dl> <span data-ttu-id="abeff-134"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="abeff-134"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="abeff-135">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="abeff-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="abeff-136">**\_COLLECTEDMSES CIM**</span><span class="sxs-lookup"><span data-stu-id="abeff-136">**CIM\_CollectedMSEs**</span></span>](cim-collectedmses.md)
</dt> </dl>

 

