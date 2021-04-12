---
description: Établit une &\# 0034 ; partie de&\# 0034 ; relation entre un système et tout élément système géré dont il est composé.
ms.assetid: 6BF72E36-9B6C-4853-A553-DDAF65991C86
title: Classe Msvm_SystemComponent
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_SystemComponent
- Msvm_SystemComponent.GroupComponent
- Msvm_SystemComponent.PartComponent
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: ee150793143b549c90d280eef287ee6a5afb66b9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104393427"
---
# <a name="msvm_systemcomponent-class"></a><span data-ttu-id="3b269-103">MSVM \_ SystemComponent, classe</span><span class="sxs-lookup"><span data-stu-id="3b269-103">Msvm\_SystemComponent class</span></span>

<span data-ttu-id="3b269-104">Établit une relation « partie de » entre un système et tout élément système géré dont il est composé.</span><span class="sxs-lookup"><span data-stu-id="3b269-104">Establishes a "part of" relationship between a system and any managed system element of which it is composed.</span></span>

<span data-ttu-id="3b269-105">La syntaxe suivante est simplifiée format MOF (MOF) et comprend toutes les propriétés héritées.</span><span class="sxs-lookup"><span data-stu-id="3b269-105">The following syntax is simplified Managed Object Format (MOF) code, and it includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="3b269-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="3b269-106">Syntax</span></span>

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), Association, Aggregation]
class Msvm_SystemComponent : CIM_SystemComponent
{
  CIM_System               REF GroupComponent;
  CIM_ManagedSystemElement REF PartComponent;
};
```

## <a name="members"></a><span data-ttu-id="3b269-107">Membres</span><span class="sxs-lookup"><span data-stu-id="3b269-107">Members</span></span>

<span data-ttu-id="3b269-108">La classe **MSVM \_ SystemComponent** possède les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="3b269-108">The **Msvm\_SystemComponent** class has these types of members:</span></span>

-   [<span data-ttu-id="3b269-109">Propriétés</span><span class="sxs-lookup"><span data-stu-id="3b269-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="3b269-110">Propriétés</span><span class="sxs-lookup"><span data-stu-id="3b269-110">Properties</span></span>

<span data-ttu-id="3b269-111">La classe **MSVM \_ SystemComponent** possède les propriétés suivantes.</span><span class="sxs-lookup"><span data-stu-id="3b269-111">The **Msvm\_SystemComponent** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="3b269-112">**GroupComponent**</span><span class="sxs-lookup"><span data-stu-id="3b269-112">**GroupComponent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3b269-113">Type de données : **[ **\_ système CIM**](/windows/desktop/CIMWin32Prov/cim-system)**</span><span class="sxs-lookup"><span data-stu-id="3b269-113">Data type: **[**CIM\_System**](/windows/desktop/CIMWin32Prov/cim-system)**</span></span>
</dt> <dt>

<span data-ttu-id="3b269-114">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="3b269-114">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="3b269-115">Élément parent dans l’Association.</span><span class="sxs-lookup"><span data-stu-id="3b269-115">The parent element in the association.</span></span> <span data-ttu-id="3b269-116">Cette propriété est héritée de la [**\_ SystemComponent CIM**](/windows/desktop/CIMWin32Prov/cim-systemcomponent).</span><span class="sxs-lookup"><span data-stu-id="3b269-116">This property is inherited from [**CIM\_SystemComponent**](/windows/desktop/CIMWin32Prov/cim-systemcomponent).</span></span>

</dd> <dt>

<span data-ttu-id="3b269-117">**PartComponent**</span><span class="sxs-lookup"><span data-stu-id="3b269-117">**PartComponent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3b269-118">Type de données : **[ **CIM CIM \_**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)**</span><span class="sxs-lookup"><span data-stu-id="3b269-118">Data type: **[**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)**</span></span>
</dt> <dt>

<span data-ttu-id="3b269-119">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="3b269-119">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="3b269-120">Élément enfant dans l’Association.</span><span class="sxs-lookup"><span data-stu-id="3b269-120">The child element in the association.</span></span> <span data-ttu-id="3b269-121">Cette propriété est héritée de la [**\_ SystemComponent CIM**](/windows/desktop/CIMWin32Prov/cim-systemcomponent).</span><span class="sxs-lookup"><span data-stu-id="3b269-121">This property is inherited from [**CIM\_SystemComponent**](/windows/desktop/CIMWin32Prov/cim-systemcomponent).</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="3b269-122">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="3b269-122">Requirements</span></span>



| <span data-ttu-id="3b269-123">Condition requise</span><span class="sxs-lookup"><span data-stu-id="3b269-123">Requirement</span></span> | <span data-ttu-id="3b269-124">Valeur</span><span class="sxs-lookup"><span data-stu-id="3b269-124">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3b269-125">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="3b269-125">Minimum supported client</span></span><br/> | <span data-ttu-id="3b269-126">Windows 8.1 les \[ applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="3b269-126">Windows 8.1 \[desktop apps only\]</span></span><br/>                                                            |
| <span data-ttu-id="3b269-127">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="3b269-127">Minimum supported server</span></span><br/> | <span data-ttu-id="3b269-128">Applications de bureau Windows Server 2012 R2 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="3b269-128">Windows Server 2012 R2 \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="3b269-129">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="3b269-129">Namespace</span></span><br/>                | <span data-ttu-id="3b269-130">\\Virtualisation racine \\ v2</span><span class="sxs-lookup"><span data-stu-id="3b269-130">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="3b269-131">MOF</span><span class="sxs-lookup"><span data-stu-id="3b269-131">MOF</span></span><br/>                      | <dl> <span data-ttu-id="3b269-132"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="3b269-132"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="3b269-133">DLL</span><span class="sxs-lookup"><span data-stu-id="3b269-133">DLL</span></span><br/>                      | <dl> <span data-ttu-id="3b269-134"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="3b269-134"><dt>Vmms.exe</dt></span></span> </dl>                     |



 

