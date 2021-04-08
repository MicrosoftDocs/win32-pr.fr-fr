---
description: Associe le \_ SnapshotCollection MSVM aux objets MSVM \_ VirtualSystemCollection correspondants.
ms.assetid: 4dbfe21f-e700-4266-aedb-236c57c424f6
title: Classe Msvm_SnapshotOfVirtualSystemCollection
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_SnapshotOfVirtualSystemCollection
- Msvm_SnapshotOfVirtualSystemCollection.Antecedent
- Msvm_SnapshotOfVirtualSystemCollection.Dependent
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: ae3c9c146cea8a8af98f4d3071ee7339d53eb6b1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103863561"
---
# <a name="msvm_snapshotofvirtualsystemcollection-class"></a><span data-ttu-id="c9937-103">MSVM \_ SnapshotOfVirtualSystemCollection, classe</span><span class="sxs-lookup"><span data-stu-id="c9937-103">Msvm\_SnapshotOfVirtualSystemCollection class</span></span>

<span data-ttu-id="c9937-104">Associe [**le \_ SnapshotCollection MSVM**](msvm-snapshotcollection.md) aux objets [**MSVM \_ VirtualSystemCollection**](msvm-virtualsystemcollection.md) correspondants.</span><span class="sxs-lookup"><span data-stu-id="c9937-104">Associates the [**Msvm\_SnapshotCollection**](msvm-snapshotcollection.md) to the corresponding [**Msvm\_VirtualSystemCollection**](msvm-virtualsystemcollection.md) objects.</span></span>

<span data-ttu-id="c9937-105">La syntaxe suivante est simplifiée par rapport au code MOF (Managed Object Format) et inclut toutes les propriétés héritées.</span><span class="sxs-lookup"><span data-stu-id="c9937-105">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="c9937-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="c9937-106">Syntax</span></span>

``` syntax
[Association, Aggregation, Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_SnapshotOfVirtualSystemCollection : CIM_Dependency
{
  CIM_CollectionOfMSEs REF Antecedent;
  CIM_Collection       REF Dependent;
};
```

## <a name="members"></a><span data-ttu-id="c9937-107">Membres</span><span class="sxs-lookup"><span data-stu-id="c9937-107">Members</span></span>

<span data-ttu-id="c9937-108">La classe **MSVM \_ SnapshotOfVirtualSystemCollection** possède les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="c9937-108">The **Msvm\_SnapshotOfVirtualSystemCollection** class has these types of members:</span></span>

-   [<span data-ttu-id="c9937-109">Propriétés</span><span class="sxs-lookup"><span data-stu-id="c9937-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="c9937-110">Propriétés</span><span class="sxs-lookup"><span data-stu-id="c9937-110">Properties</span></span>

<span data-ttu-id="c9937-111">La classe **MSVM \_ SnapshotOfVirtualSystemCollection** possède les propriétés suivantes.</span><span class="sxs-lookup"><span data-stu-id="c9937-111">The **Msvm\_SnapshotOfVirtualSystemCollection** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="c9937-112">**Antécédent**</span><span class="sxs-lookup"><span data-stu-id="c9937-112">**Antecedent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c9937-113">Type de données : **CIM \_ CollectionOfMSEs**</span><span class="sxs-lookup"><span data-stu-id="c9937-113">Data type: **CIM\_CollectionOfMSEs**</span></span>
</dt> <dt>

<span data-ttu-id="c9937-114">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="c9937-114">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c9937-115">Qualificateurs : [**clé**](/windows/desktop/WmiSdk/key-qualifier), [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Antecedent")</span><span class="sxs-lookup"><span data-stu-id="c9937-115">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Antecedent")</span></span>
</dt> </dl>

<span data-ttu-id="c9937-116">[**CIM \_ CollectionOfMSEs**](cim-collectionofmses.md) qui représente l’objet indépendant dans cette association.</span><span class="sxs-lookup"><span data-stu-id="c9937-116">A [**CIM\_CollectionOfMSEs**](cim-collectionofmses.md) that represents the independent object in this association.</span></span>

</dd> <dt>

<span data-ttu-id="c9937-117">**Charge**</span><span class="sxs-lookup"><span data-stu-id="c9937-117">**Dependent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c9937-118">Type de données **: \_ collecte CIM**</span><span class="sxs-lookup"><span data-stu-id="c9937-118">Data type: **CIM\_Collection**</span></span>
</dt> <dt>

<span data-ttu-id="c9937-119">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="c9937-119">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c9937-120">Qualificateurs : [**clé**](/windows/desktop/WmiSdk/key-qualifier), [**remplacement**](/windows/desktop/WmiSdk/standard-qualifiers) (« dépendant »)</span><span class="sxs-lookup"><span data-stu-id="c9937-120">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Dependent")</span></span>
</dt> </dl>

<span data-ttu-id="c9937-121">[**\_ Collection CIM**](cim-collection.md) qui représente l’objet qui dépend de l' **antécédent.**</span><span class="sxs-lookup"><span data-stu-id="c9937-121">A [**CIM\_Collection**](cim-collection.md) that represents the object that is dependent on the **Antecedent.**</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="c9937-122">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="c9937-122">Requirements</span></span>



| <span data-ttu-id="c9937-123">Condition requise</span><span class="sxs-lookup"><span data-stu-id="c9937-123">Requirement</span></span> | <span data-ttu-id="c9937-124">Valeur</span><span class="sxs-lookup"><span data-stu-id="c9937-124">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c9937-125">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="c9937-125">Minimum supported client</span></span><br/> | <span data-ttu-id="c9937-126">Applications de \[ Bureau Windows 10 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="c9937-126">Windows 10 \[desktop apps only\]</span></span><br/>                                                             |
| <span data-ttu-id="c9937-127">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="c9937-127">Minimum supported server</span></span><br/> | <span data-ttu-id="c9937-128">Windows Server 2016</span><span class="sxs-lookup"><span data-stu-id="c9937-128">Windows Server 2016</span></span><br/>                                                                          |
| <span data-ttu-id="c9937-129">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="c9937-129">Namespace</span></span><br/>                | <span data-ttu-id="c9937-130">\\Virtualisation racine \\ v2</span><span class="sxs-lookup"><span data-stu-id="c9937-130">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="c9937-131">MOF</span><span class="sxs-lookup"><span data-stu-id="c9937-131">MOF</span></span><br/>                      | <dl> <span data-ttu-id="c9937-132"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="c9937-132"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="c9937-133">DLL</span><span class="sxs-lookup"><span data-stu-id="c9937-133">DLL</span></span><br/>                      | <dl> <span data-ttu-id="c9937-134"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="c9937-134"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="c9937-135">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="c9937-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c9937-136">**\_Dépendance CIM**</span><span class="sxs-lookup"><span data-stu-id="c9937-136">**CIM\_Dependency**</span></span>](cim-dependency.md)
</dt> </dl>

 

