---
description: Représente une association entre un travail et l’élément managé responsable de la création du travail.
ms.assetid: 1a100c7e-7e17-47dd-b730-c05c5e4dccda
title: Classe Msvm_OwningJobElement
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_OwningJobElement
- Msvm_OwningJobElement.OwningElement
- Msvm_OwningJobElement.OwnedElement
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 34aa6f390d21a37421e09f30f9a775784717be9e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106534125"
---
# <a name="msvm_owningjobelement-class"></a><span data-ttu-id="852cf-103">MSVM \_ OwningJobElement, classe</span><span class="sxs-lookup"><span data-stu-id="852cf-103">Msvm\_OwningJobElement class</span></span>

<span data-ttu-id="852cf-104">Représente une association entre un travail et l’élément managé responsable de la création du travail.</span><span class="sxs-lookup"><span data-stu-id="852cf-104">Represents an association between a job and the managed element responsible for the creation of the job.</span></span>

<span data-ttu-id="852cf-105">La syntaxe suivante est simplifiée format MOF (MOF) et comprend toutes les propriétés héritées.</span><span class="sxs-lookup"><span data-stu-id="852cf-105">The following syntax is simplified Managed Object Format (MOF) code, and it includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="852cf-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="852cf-106">Syntax</span></span>

``` syntax
[Association, Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_OwningJobElement : CIM_OwningJobElement
{
  CIM_ManagedElement REF OwningElement;
  Msvm_ConcreteJob   REF OwnedElement;
};
```

## <a name="members"></a><span data-ttu-id="852cf-107">Membres</span><span class="sxs-lookup"><span data-stu-id="852cf-107">Members</span></span>

<span data-ttu-id="852cf-108">La classe **MSVM \_ OwningJobElement** possède les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="852cf-108">The **Msvm\_OwningJobElement** class has these types of members:</span></span>

-   [<span data-ttu-id="852cf-109">Propriétés</span><span class="sxs-lookup"><span data-stu-id="852cf-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="852cf-110">Propriétés</span><span class="sxs-lookup"><span data-stu-id="852cf-110">Properties</span></span>

<span data-ttu-id="852cf-111">La classe **MSVM \_ OwningJobElement** possède les propriétés suivantes.</span><span class="sxs-lookup"><span data-stu-id="852cf-111">The **Msvm\_OwningJobElement** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="852cf-112">**OwnedElement**</span><span class="sxs-lookup"><span data-stu-id="852cf-112">**OwnedElement**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="852cf-113">Type de données : **[ **MSVM \_ ConcreteJob**](msvm-concretejob.md)**</span><span class="sxs-lookup"><span data-stu-id="852cf-113">Data type: **[**Msvm\_ConcreteJob**](msvm-concretejob.md)**</span></span>
</dt> <dt>

<span data-ttu-id="852cf-114">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="852cf-114">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="852cf-115">Travail créé par l’élément managé.</span><span class="sxs-lookup"><span data-stu-id="852cf-115">The job created by the managed element.</span></span>

</dd> <dt>

<span data-ttu-id="852cf-116">**OwningElement**</span><span class="sxs-lookup"><span data-stu-id="852cf-116">**OwningElement**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="852cf-117">Type de données : **[ **CIM \_ propriété ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)**</span><span class="sxs-lookup"><span data-stu-id="852cf-117">Data type: **[**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)**</span></span>
</dt> <dt>

<span data-ttu-id="852cf-118">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="852cf-118">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="852cf-119">Élément managé responsable de la création du travail.</span><span class="sxs-lookup"><span data-stu-id="852cf-119">The managed element responsible for the creation of the job.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="852cf-120">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="852cf-120">Requirements</span></span>



| <span data-ttu-id="852cf-121">Condition requise</span><span class="sxs-lookup"><span data-stu-id="852cf-121">Requirement</span></span> | <span data-ttu-id="852cf-122">Valeur</span><span class="sxs-lookup"><span data-stu-id="852cf-122">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="852cf-123">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="852cf-123">Minimum supported client</span></span><br/> | <span data-ttu-id="852cf-124">Applications de \[ Bureau Windows 8 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="852cf-124">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="852cf-125">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="852cf-125">Minimum supported server</span></span><br/> | <span data-ttu-id="852cf-126">Applications de bureau Windows Server 2012 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="852cf-126">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="852cf-127">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="852cf-127">Namespace</span></span><br/>                | <span data-ttu-id="852cf-128">\\Virtualisation racine \\ v2</span><span class="sxs-lookup"><span data-stu-id="852cf-128">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="852cf-129">MOF</span><span class="sxs-lookup"><span data-stu-id="852cf-129">MOF</span></span><br/>                      | <dl> <span data-ttu-id="852cf-130"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="852cf-130"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="852cf-131">DLL</span><span class="sxs-lookup"><span data-stu-id="852cf-131">DLL</span></span><br/>                      | <dl> <span data-ttu-id="852cf-132"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="852cf-132"><dt>Vmms.exe</dt></span></span> </dl>                     |



 

