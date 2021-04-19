---
description: Représente une association entre un travail et l’élément managé qui a créé le travail.
ms.assetid: 08c33a81-0a3f-4545-9812-96a854a7509e
title: Classe CIM_OwningJobElement
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_OwningJobElement
- CIM_OwningJobElement.OwningElement
- CIM_OwningJobElement.OwnedElement
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 9d3879104a8f7406ff24dc2f63b79b51eb2fa58c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106521149"
---
# <a name="cim_owningjobelement-class"></a><span data-ttu-id="79aff-103">\_Classe CIM OwningJobElement</span><span class="sxs-lookup"><span data-stu-id="79aff-103">CIM\_OwningJobElement class</span></span>

<span data-ttu-id="79aff-104">Représente une association entre un travail et l’élément managé qui a créé le travail.</span><span class="sxs-lookup"><span data-stu-id="79aff-104">Represents an association between a job and the managed element that created the job.</span></span> <span data-ttu-id="79aff-105">Étant donné qu’un travail peut se déplacer entre les systèmes et que l’élément géré peut ne pas exister pendant toute la durée du travail, dans certains cas, cette association peut ne pas être possible ou ne peut exister que pour une partie de l’existence du travail.</span><span class="sxs-lookup"><span data-stu-id="79aff-105">Since a job might move between systems, and the managed element might not exist for the entire duration of the job, in some cases, this association might not be possible or might only exist for a portion of the existence of the job.</span></span>

## <a name="syntax"></a><span data-ttu-id="79aff-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="79aff-106">Syntax</span></span>

``` syntax
[Association, Abstract, Version("2.7.0"), UMLPackagePath("CIM::System::Processing"), ModelCorrespondence("CIM_Job.Owner"), AMENDMENT]
class CIM_OwningJobElement
{
  CIM_ManagedElement REF OwningElement;
  CIM_Job            REF OwnedElement;
};
```

## <a name="members"></a><span data-ttu-id="79aff-107">Membres</span><span class="sxs-lookup"><span data-stu-id="79aff-107">Members</span></span>

<span data-ttu-id="79aff-108">La classe **CIM \_ OwningJobElement** possède les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="79aff-108">The **CIM\_OwningJobElement** class has these types of members:</span></span>

-   [<span data-ttu-id="79aff-109">Propriétés</span><span class="sxs-lookup"><span data-stu-id="79aff-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="79aff-110">Propriétés</span><span class="sxs-lookup"><span data-stu-id="79aff-110">Properties</span></span>

<span data-ttu-id="79aff-111">La classe **CIM \_ OwningJobElement** possède les propriétés suivantes.</span><span class="sxs-lookup"><span data-stu-id="79aff-111">The **CIM\_OwningJobElement** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="79aff-112">**OwnedElement**</span><span class="sxs-lookup"><span data-stu-id="79aff-112">**OwnedElement**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="79aff-113">Type de données **: \_ travail CIM**</span><span class="sxs-lookup"><span data-stu-id="79aff-113">Data type: **CIM\_Job**</span></span>
</dt> <dt>

<span data-ttu-id="79aff-114">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="79aff-114">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="79aff-115">Qualificateurs : [ **clé**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="79aff-115">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="79aff-116">Référence au travail créé par l’élément managé.</span><span class="sxs-lookup"><span data-stu-id="79aff-116">A reference to the job created by the managed element.</span></span>

</dd> <dt>

<span data-ttu-id="79aff-117">**OwningElement**</span><span class="sxs-lookup"><span data-stu-id="79aff-117">**OwningElement**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="79aff-118">Type de données : **CIM \_ propriété ManagedElement**</span><span class="sxs-lookup"><span data-stu-id="79aff-118">Data type: **CIM\_ManagedElement**</span></span>
</dt> <dt>

<span data-ttu-id="79aff-119">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="79aff-119">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="79aff-120">Qualificateurs : [**clé**](/windows/desktop/WmiSdk/key-qualifier), [**Max**](/windows/desktop/WmiSdk/standard-qualifiers) (1)</span><span class="sxs-lookup"><span data-stu-id="79aff-120">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**Max**](/windows/desktop/WmiSdk/standard-qualifiers) (1)</span></span>
</dt> </dl>

<span data-ttu-id="79aff-121">Référence à l’élément managé qui A créé le travail.</span><span class="sxs-lookup"><span data-stu-id="79aff-121">A reference to the managed element that created the job.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="79aff-122">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="79aff-122">Requirements</span></span>



| <span data-ttu-id="79aff-123">Condition requise</span><span class="sxs-lookup"><span data-stu-id="79aff-123">Requirement</span></span> | <span data-ttu-id="79aff-124">Valeur</span><span class="sxs-lookup"><span data-stu-id="79aff-124">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="79aff-125">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="79aff-125">Minimum supported client</span></span><br/> | <span data-ttu-id="79aff-126">Windows 8</span><span class="sxs-lookup"><span data-stu-id="79aff-126">Windows 8</span></span><br/>                                                                                    |
| <span data-ttu-id="79aff-127">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="79aff-127">Minimum supported server</span></span><br/> | <span data-ttu-id="79aff-128">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="79aff-128">Windows Server 2012</span></span><br/>                                                                          |
| <span data-ttu-id="79aff-129">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="79aff-129">Namespace</span></span><br/>                | <span data-ttu-id="79aff-130">\\Virtualisation racine \\ v2</span><span class="sxs-lookup"><span data-stu-id="79aff-130">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="79aff-131">MOF</span><span class="sxs-lookup"><span data-stu-id="79aff-131">MOF</span></span><br/>                      | <dl> <span data-ttu-id="79aff-132"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="79aff-132"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="79aff-133">DLL</span><span class="sxs-lookup"><span data-stu-id="79aff-133">DLL</span></span><br/>                      | <dl> <span data-ttu-id="79aff-134"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="79aff-134"><dt>Vmms.exe</dt></span></span> </dl>                     |



 

