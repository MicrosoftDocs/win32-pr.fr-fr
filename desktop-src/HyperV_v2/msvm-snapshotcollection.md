---
description: Représente une collection de captures instantanées de système virtuel.
ms.assetid: c9b64421-232c-4f32-a088-6b98602ca3f4
title: Classe Msvm_SnapshotCollection
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_SnapshotCollection
- Msvm_SnapshotCollection.CollectionID
- Msvm_SnapshotCollection.ElementName
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 1e24566f1f5c5500258f14f88cbe2b7c4fa29e27
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104114578"
---
# <a name="msvm_snapshotcollection-class"></a><span data-ttu-id="70f23-103">MSVM \_ SnapshotCollection, classe</span><span class="sxs-lookup"><span data-stu-id="70f23-103">Msvm\_SnapshotCollection class</span></span>

<span data-ttu-id="70f23-104">Représente une collection de captures instantanées de système virtuel.</span><span class="sxs-lookup"><span data-stu-id="70f23-104">Represents a collection of virtual system snapshots.</span></span>

<span data-ttu-id="70f23-105">La syntaxe suivante est simplifiée par rapport au code MOF (Managed Object Format) et inclut toutes les propriétés héritées.</span><span class="sxs-lookup"><span data-stu-id="70f23-105">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="70f23-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="70f23-106">Syntax</span></span>

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_SnapshotCollection : CIM_Collection
{
  string CollectionID;
  string ElementName;
};
```

## <a name="members"></a><span data-ttu-id="70f23-107">Membres</span><span class="sxs-lookup"><span data-stu-id="70f23-107">Members</span></span>

<span data-ttu-id="70f23-108">La classe **MSVM \_ SnapshotCollection** possède les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="70f23-108">The **Msvm\_SnapshotCollection** class has these types of members:</span></span>

-   [<span data-ttu-id="70f23-109">Propriétés</span><span class="sxs-lookup"><span data-stu-id="70f23-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="70f23-110">Propriétés</span><span class="sxs-lookup"><span data-stu-id="70f23-110">Properties</span></span>

<span data-ttu-id="70f23-111">La classe **MSVM \_ SnapshotCollection** possède les propriétés suivantes.</span><span class="sxs-lookup"><span data-stu-id="70f23-111">The **Msvm\_SnapshotCollection** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="70f23-112">**CollectionID**</span><span class="sxs-lookup"><span data-stu-id="70f23-112">**CollectionID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="70f23-113">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="70f23-113">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="70f23-114">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="70f23-114">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="70f23-115">Qualificateurs : [**clé**](/windows/desktop/WmiSdk/key-qualifier), [**remplacement**](/windows/desktop/WmiSdk/standard-qualifiers) (« porte »), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span><span class="sxs-lookup"><span data-stu-id="70f23-115">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("CollectionID"), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span></span>
</dt> </dl>

<span data-ttu-id="70f23-116">Identification unique de l’objet de collection.</span><span class="sxs-lookup"><span data-stu-id="70f23-116">The unique identification of the collection object.</span></span>

</dd> <dt>

<span data-ttu-id="70f23-117">**ElementName**</span><span class="sxs-lookup"><span data-stu-id="70f23-117">**ElementName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="70f23-118">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="70f23-118">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="70f23-119">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="70f23-119">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="70f23-120">Qualificateurs : [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("ElementName")</span><span class="sxs-lookup"><span data-stu-id="70f23-120">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("ElementName")</span></span>
</dt> </dl>

<span data-ttu-id="70f23-121">Nom défini par l’utilisateur pour la collection.</span><span class="sxs-lookup"><span data-stu-id="70f23-121">An user-defined name for the collection.</span></span> <span data-ttu-id="70f23-122">Notez qu’il n’est pas garanti qu’il soit unique.</span><span class="sxs-lookup"><span data-stu-id="70f23-122">Note this is not guaranteed to be unique.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="70f23-123">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="70f23-123">Requirements</span></span>



| <span data-ttu-id="70f23-124">Condition requise</span><span class="sxs-lookup"><span data-stu-id="70f23-124">Requirement</span></span> | <span data-ttu-id="70f23-125">Valeur</span><span class="sxs-lookup"><span data-stu-id="70f23-125">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="70f23-126">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="70f23-126">Minimum supported client</span></span><br/> | <span data-ttu-id="70f23-127">Applications de \[ Bureau Windows 10 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="70f23-127">Windows 10 \[desktop apps only\]</span></span><br/>                                                             |
| <span data-ttu-id="70f23-128">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="70f23-128">Minimum supported server</span></span><br/> | <span data-ttu-id="70f23-129">Windows Server 2016</span><span class="sxs-lookup"><span data-stu-id="70f23-129">Windows Server 2016</span></span><br/>                                                                          |
| <span data-ttu-id="70f23-130">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="70f23-130">Namespace</span></span><br/>                | <span data-ttu-id="70f23-131">\\Virtualisation racine \\ v2</span><span class="sxs-lookup"><span data-stu-id="70f23-131">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="70f23-132">MOF</span><span class="sxs-lookup"><span data-stu-id="70f23-132">MOF</span></span><br/>                      | <dl> <span data-ttu-id="70f23-133"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="70f23-133"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="70f23-134">DLL</span><span class="sxs-lookup"><span data-stu-id="70f23-134">DLL</span></span><br/>                      | <dl> <span data-ttu-id="70f23-135"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="70f23-135"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="70f23-136">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="70f23-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="70f23-137">**\_Collection CIM**</span><span class="sxs-lookup"><span data-stu-id="70f23-137">**CIM\_Collection**</span></span>](cim-collection.md)
</dt> </dl>

 

