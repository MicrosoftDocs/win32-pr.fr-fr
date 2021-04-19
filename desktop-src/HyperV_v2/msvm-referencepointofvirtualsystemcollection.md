---
description: Associe le \_ ReferencePointCollection MSVM aux objets MSVM \_ VirtualSystemCollection correspondants.
ms.assetid: 847f1f46-364f-4c91-b9e8-4740d3da1947
title: Classe Msvm_ReferencePointOfVirtualSystemCollection
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_ReferencePointOfVirtualSystemCollection
- Msvm_ReferencePointOfVirtualSystemCollection.Antecedent
- Msvm_ReferencePointOfVirtualSystemCollection.Dependent
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 0919b8666915817d8475908b0305e90ea39e60f8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106522024"
---
# <a name="msvm_referencepointofvirtualsystemcollection-class"></a><span data-ttu-id="97168-103">MSVM \_ ReferencePointOfVirtualSystemCollection, classe</span><span class="sxs-lookup"><span data-stu-id="97168-103">Msvm\_ReferencePointOfVirtualSystemCollection class</span></span>

<span data-ttu-id="97168-104">Associe [**le \_ ReferencePointCollection MSVM**](msvm-referencepointcollection.md) aux objets [**MSVM \_ VirtualSystemCollection**](msvm-virtualsystemcollection.md) correspondants.</span><span class="sxs-lookup"><span data-stu-id="97168-104">Associates the [**Msvm\_ReferencePointCollection**](msvm-referencepointcollection.md) to the corresponding [**Msvm\_VirtualSystemCollection**](msvm-virtualsystemcollection.md) objects.</span></span>

<span data-ttu-id="97168-105">La syntaxe suivante est simplifiée par rapport au code MOF (Managed Object Format) et inclut toutes les propriétés héritées.</span><span class="sxs-lookup"><span data-stu-id="97168-105">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="97168-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="97168-106">Syntax</span></span>

``` syntax
[Association, Aggregation, Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_ReferencePointOfVirtualSystemCollection : CIM_Dependency
{
  CIM_CollectionOfMSEs REF Antecedent;
  CIM_Collection       REF Dependent;
};
```

## <a name="members"></a><span data-ttu-id="97168-107">Membres</span><span class="sxs-lookup"><span data-stu-id="97168-107">Members</span></span>

<span data-ttu-id="97168-108">La classe **MSVM \_ ReferencePointOfVirtualSystemCollection** possède les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="97168-108">The **Msvm\_ReferencePointOfVirtualSystemCollection** class has these types of members:</span></span>

-   [<span data-ttu-id="97168-109">Propriétés</span><span class="sxs-lookup"><span data-stu-id="97168-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="97168-110">Propriétés</span><span class="sxs-lookup"><span data-stu-id="97168-110">Properties</span></span>

<span data-ttu-id="97168-111">La classe **MSVM \_ ReferencePointOfVirtualSystemCollection** possède les propriétés suivantes.</span><span class="sxs-lookup"><span data-stu-id="97168-111">The **Msvm\_ReferencePointOfVirtualSystemCollection** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="97168-112">**Antécédent**</span><span class="sxs-lookup"><span data-stu-id="97168-112">**Antecedent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="97168-113">Type de données : **CIM \_ CollectionOfMSEs**</span><span class="sxs-lookup"><span data-stu-id="97168-113">Data type: **CIM\_CollectionOfMSEs**</span></span>
</dt> <dt>

<span data-ttu-id="97168-114">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="97168-114">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="97168-115">Qualificateurs : [**clé**](/windows/desktop/WmiSdk/key-qualifier), [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Antecedent")</span><span class="sxs-lookup"><span data-stu-id="97168-115">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Antecedent")</span></span>
</dt> </dl>

<span data-ttu-id="97168-116">[**CIM \_ CollectionOfMSEs**](cim-collectionofmses.md) qui représente l’objet indépendant dans cette association.</span><span class="sxs-lookup"><span data-stu-id="97168-116">A [**CIM\_CollectionOfMSEs**](cim-collectionofmses.md) that represents the independent object in this association.</span></span>

</dd> <dt>

<span data-ttu-id="97168-117">**Charge**</span><span class="sxs-lookup"><span data-stu-id="97168-117">**Dependent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="97168-118">Type de données **: \_ collecte CIM**</span><span class="sxs-lookup"><span data-stu-id="97168-118">Data type: **CIM\_Collection**</span></span>
</dt> <dt>

<span data-ttu-id="97168-119">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="97168-119">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="97168-120">Qualificateurs : [**clé**](/windows/desktop/WmiSdk/key-qualifier), [**remplacement**](/windows/desktop/WmiSdk/standard-qualifiers) (« dépendant »)</span><span class="sxs-lookup"><span data-stu-id="97168-120">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Dependent")</span></span>
</dt> </dl>

<span data-ttu-id="97168-121">[**\_ Collection CIM**](cim-collection.md) qui représente l’objet qui dépend de l' **antécédent**.</span><span class="sxs-lookup"><span data-stu-id="97168-121">A [**CIM\_Collection**](cim-collection.md) that represents the object that is dependent on the **Antecedent**.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="97168-122">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="97168-122">Requirements</span></span>



| <span data-ttu-id="97168-123">Condition requise</span><span class="sxs-lookup"><span data-stu-id="97168-123">Requirement</span></span> | <span data-ttu-id="97168-124">Valeur</span><span class="sxs-lookup"><span data-stu-id="97168-124">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="97168-125">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="97168-125">Minimum supported client</span></span><br/> | <span data-ttu-id="97168-126">Applications de \[ Bureau Windows 10 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="97168-126">Windows 10 \[desktop apps only\]</span></span><br/>                                                             |
| <span data-ttu-id="97168-127">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="97168-127">Minimum supported server</span></span><br/> | <span data-ttu-id="97168-128">Windows Server 2016</span><span class="sxs-lookup"><span data-stu-id="97168-128">Windows Server 2016</span></span><br/>                                                                          |
| <span data-ttu-id="97168-129">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="97168-129">Namespace</span></span><br/>                | <span data-ttu-id="97168-130">\\Virtualisation racine \\ v2</span><span class="sxs-lookup"><span data-stu-id="97168-130">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="97168-131">MOF</span><span class="sxs-lookup"><span data-stu-id="97168-131">MOF</span></span><br/>                      | <dl> <span data-ttu-id="97168-132"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="97168-132"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="97168-133">DLL</span><span class="sxs-lookup"><span data-stu-id="97168-133">DLL</span></span><br/>                      | <dl> <span data-ttu-id="97168-134"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="97168-134"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="97168-135">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="97168-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="97168-136">**\_Dépendance CIM**</span><span class="sxs-lookup"><span data-stu-id="97168-136">**CIM\_Dependency**</span></span>](cim-dependency.md)
</dt> </dl>

 

