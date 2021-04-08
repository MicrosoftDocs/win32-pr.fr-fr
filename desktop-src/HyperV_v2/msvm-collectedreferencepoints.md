---
description: Associe le \_ ReferencePointCollection MSVM aux objets MSVM \_ VirtualSystemReferencePoint contenus.
ms.assetid: 826125c3-0a89-4573-ac28-88588eac248d
title: Classe Msvm_CollectedReferencePoints
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_CollectedReferencePoints
- Msvm_CollectedReferencePoints.Collection
- Msvm_CollectedReferencePoints.Member
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 4891d4ec4c613c92c3b5d5a090f2683bfc77dc5e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103753021"
---
# <a name="msvm_collectedreferencepoints-class"></a><span data-ttu-id="7616e-103">MSVM \_ CollectedReferencePoints, classe</span><span class="sxs-lookup"><span data-stu-id="7616e-103">Msvm\_CollectedReferencePoints class</span></span>

<span data-ttu-id="7616e-104">Associe [**le \_ ReferencePointCollection MSVM**](msvm-referencepointcollection.md) aux objets [**MSVM \_ VirtualSystemReferencePoint**](msvm-virtualsystemreferencepoint.md) contenus.</span><span class="sxs-lookup"><span data-stu-id="7616e-104">Associates the [**Msvm\_ReferencePointCollection**](msvm-referencepointcollection.md) to the contained [**Msvm\_VirtualSystemReferencePoint**](msvm-virtualsystemreferencepoint.md) objects.</span></span>

<span data-ttu-id="7616e-105">La syntaxe suivante est simplifiée par rapport au code MOF (Managed Object Format) et inclut toutes les propriétés héritées.</span><span class="sxs-lookup"><span data-stu-id="7616e-105">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="7616e-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="7616e-106">Syntax</span></span>

``` syntax
[Association, Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_CollectedReferencePoints : CIM_CollectedMSEs
{
  Msvm_ReferencePointCollection    REF Collection;
  Msvm_VirtualSystemReferencePoint REF Member;
};
```

## <a name="members"></a><span data-ttu-id="7616e-107">Membres</span><span class="sxs-lookup"><span data-stu-id="7616e-107">Members</span></span>

<span data-ttu-id="7616e-108">La classe **MSVM \_ CollectedReferencePoints** possède les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="7616e-108">The **Msvm\_CollectedReferencePoints** class has these types of members:</span></span>

-   [<span data-ttu-id="7616e-109">Propriétés</span><span class="sxs-lookup"><span data-stu-id="7616e-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="7616e-110">Propriétés</span><span class="sxs-lookup"><span data-stu-id="7616e-110">Properties</span></span>

<span data-ttu-id="7616e-111">La classe **MSVM \_ CollectedReferencePoints** possède les propriétés suivantes.</span><span class="sxs-lookup"><span data-stu-id="7616e-111">The **Msvm\_CollectedReferencePoints** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="7616e-112">**Collection**</span><span class="sxs-lookup"><span data-stu-id="7616e-112">**Collection**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7616e-113">Type de données : **MSVM \_ ReferencePointCollection**</span><span class="sxs-lookup"><span data-stu-id="7616e-113">Data type: **Msvm\_ReferencePointCollection**</span></span>
</dt> <dt>

<span data-ttu-id="7616e-114">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="7616e-114">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="7616e-115">Qualificateurs : [**Aggregate**](/windows/desktop/WmiSdk/standard-qualifiers), [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("collection")</span><span class="sxs-lookup"><span data-stu-id="7616e-115">Qualifiers: [**Aggregate**](/windows/desktop/WmiSdk/standard-qualifiers), [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Collection")</span></span>
</dt> </dl>

<span data-ttu-id="7616e-116">Un regroupement [**MSVM \_ ReferencePointCollection**](msvm-referencepointcollection.md) ou un objet « Bag » qui représente la collection.</span><span class="sxs-lookup"><span data-stu-id="7616e-116">An [**Msvm\_ReferencePointCollection**](msvm-referencepointcollection.md) grouping or 'bag' object that represents the collection.</span></span>

</dd> <dt>

<span data-ttu-id="7616e-117">**Membre**</span><span class="sxs-lookup"><span data-stu-id="7616e-117">**Member**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7616e-118">Type de données : **MSVM \_ VirtualSystemReferencePoint**</span><span class="sxs-lookup"><span data-stu-id="7616e-118">Data type: **Msvm\_VirtualSystemReferencePoint**</span></span>
</dt> <dt>

<span data-ttu-id="7616e-119">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="7616e-119">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="7616e-120">Qualificateurs : [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Member")</span><span class="sxs-lookup"><span data-stu-id="7616e-120">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Member")</span></span>
</dt> </dl>

<span data-ttu-id="7616e-121">[**MSVM \_ VirtualSystemReferencePoint**](msvm-virtualsystemreferencepoint.md) contenant les membres de la collection.</span><span class="sxs-lookup"><span data-stu-id="7616e-121">An [**Msvm\_VirtualSystemReferencePoint**](msvm-virtualsystemreferencepoint.md) containing the members of the collection.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="7616e-122">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="7616e-122">Requirements</span></span>



| <span data-ttu-id="7616e-123">Condition requise</span><span class="sxs-lookup"><span data-stu-id="7616e-123">Requirement</span></span> | <span data-ttu-id="7616e-124">Valeur</span><span class="sxs-lookup"><span data-stu-id="7616e-124">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7616e-125">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="7616e-125">Minimum supported client</span></span><br/> | <span data-ttu-id="7616e-126">Applications de \[ Bureau Windows 10 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="7616e-126">Windows 10 \[desktop apps only\]</span></span><br/>                                                             |
| <span data-ttu-id="7616e-127">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="7616e-127">Minimum supported server</span></span><br/> | <span data-ttu-id="7616e-128">Windows Server 2016</span><span class="sxs-lookup"><span data-stu-id="7616e-128">Windows Server 2016</span></span><br/>                                                                          |
| <span data-ttu-id="7616e-129">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="7616e-129">Namespace</span></span><br/>                | <span data-ttu-id="7616e-130">\\Virtualisation racine \\ v2</span><span class="sxs-lookup"><span data-stu-id="7616e-130">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="7616e-131">MOF</span><span class="sxs-lookup"><span data-stu-id="7616e-131">MOF</span></span><br/>                      | <dl> <span data-ttu-id="7616e-132"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="7616e-132"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="7616e-133">DLL</span><span class="sxs-lookup"><span data-stu-id="7616e-133">DLL</span></span><br/>                      | <dl> <span data-ttu-id="7616e-134"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="7616e-134"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="7616e-135">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="7616e-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7616e-136">**\_COLLECTEDMSES CIM**</span><span class="sxs-lookup"><span data-stu-id="7616e-136">**CIM\_CollectedMSEs**</span></span>](cim-collectedmses.md)
</dt> </dl>

 

