---
description: Associe deux éléments managés qui représentent différents aspects de la même entité sous-jacente.
ms.assetid: 107A2B15-09F2-490A-8AB2-F9FE5F6FEE60
title: Classe Msvm_LogicalIdentity
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_LogicalIdentity
- Msvm_LogicalIdentity.SameElement
- Msvm_LogicalIdentity.SystemElement
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: c2f8d2ee522fde3769c08bcbb78611b99eed8e16
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104529049"
---
# <a name="msvm_logicalidentity-class"></a><span data-ttu-id="880c3-103">MSVM \_ LogicalIdentity, classe</span><span class="sxs-lookup"><span data-stu-id="880c3-103">Msvm\_LogicalIdentity class</span></span>

<span data-ttu-id="880c3-104">Associe deux éléments managés qui représentent différents aspects de la même entité sous-jacente.</span><span class="sxs-lookup"><span data-stu-id="880c3-104">Associates two managed elements that represent different aspects of the same underlying entity.</span></span> <span data-ttu-id="880c3-105">Cette classe dérive de [**\_ LogicalIdentity CIM**](/windows/desktop/CIMWin32Prov/cim-logicalidentity).</span><span class="sxs-lookup"><span data-stu-id="880c3-105">This class derives from [**CIM\_LogicalIdentity**](/windows/desktop/CIMWin32Prov/cim-logicalidentity).</span></span>

<span data-ttu-id="880c3-106">La syntaxe suivante issue du code MOF est simplifiée et inclut toutes les propriétés héritées.</span><span class="sxs-lookup"><span data-stu-id="880c3-106">The following syntax is simplified from MOF code and includes all inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="880c3-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="880c3-107">Syntax</span></span>

``` syntax
[Association, Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_LogicalIdentity : CIM_LogicalIdentity
{
  CIM_LogicalElement REF SameElement;
  CIM_LogicalElement REF SystemElement;
};
```

## <a name="members"></a><span data-ttu-id="880c3-108">Membres</span><span class="sxs-lookup"><span data-stu-id="880c3-108">Members</span></span>

<span data-ttu-id="880c3-109">La classe **MSVM \_ LogicalIdentity** possède les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="880c3-109">The **Msvm\_LogicalIdentity** class has these types of members:</span></span>

-   [<span data-ttu-id="880c3-110">Propriétés</span><span class="sxs-lookup"><span data-stu-id="880c3-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="880c3-111">Propriétés</span><span class="sxs-lookup"><span data-stu-id="880c3-111">Properties</span></span>

<span data-ttu-id="880c3-112">La classe **MSVM \_ LogicalIdentity** possède les propriétés suivantes.</span><span class="sxs-lookup"><span data-stu-id="880c3-112">The **Msvm\_LogicalIdentity** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="880c3-113">**SameElement**</span><span class="sxs-lookup"><span data-stu-id="880c3-113">**SameElement**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="880c3-114">Type de données : **CIM \_ LogicalElement**</span><span class="sxs-lookup"><span data-stu-id="880c3-114">Data type: **CIM\_LogicalElement**</span></span>
</dt> <dt>

<span data-ttu-id="880c3-115">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="880c3-115">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="880c3-116">Référence à un autre aspect de l’entité système.</span><span class="sxs-lookup"><span data-stu-id="880c3-116">Reference to an alternate aspect of the system entity.</span></span>

</dd> <dt>

<span data-ttu-id="880c3-117">**SYSTEME**</span><span class="sxs-lookup"><span data-stu-id="880c3-117">**SystemElement**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="880c3-118">Type de données : **CIM \_ LogicalElement**</span><span class="sxs-lookup"><span data-stu-id="880c3-118">Data type: **CIM\_LogicalElement**</span></span>
</dt> <dt>

<span data-ttu-id="880c3-119">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="880c3-119">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="880c3-120">Référence à un aspect de l’élément logique.</span><span class="sxs-lookup"><span data-stu-id="880c3-120">Reference to one aspect of the logical element.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="880c3-121">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="880c3-121">Requirements</span></span>



| <span data-ttu-id="880c3-122">Condition requise</span><span class="sxs-lookup"><span data-stu-id="880c3-122">Requirement</span></span> | <span data-ttu-id="880c3-123">Valeur</span><span class="sxs-lookup"><span data-stu-id="880c3-123">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="880c3-124">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="880c3-124">Minimum supported client</span></span><br/> | <span data-ttu-id="880c3-125">Windows 8.1 les \[ applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="880c3-125">Windows 8.1 \[desktop apps only\]</span></span><br/>                                                            |
| <span data-ttu-id="880c3-126">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="880c3-126">Minimum supported server</span></span><br/> | <span data-ttu-id="880c3-127">Applications de bureau Windows Server 2012 R2 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="880c3-127">Windows Server 2012 R2 \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="880c3-128">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="880c3-128">Namespace</span></span><br/>                | <span data-ttu-id="880c3-129">\\Virtualisation racine \\ v2</span><span class="sxs-lookup"><span data-stu-id="880c3-129">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="880c3-130">MOF</span><span class="sxs-lookup"><span data-stu-id="880c3-130">MOF</span></span><br/>                      | <dl> <span data-ttu-id="880c3-131"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="880c3-131"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="880c3-132">DLL</span><span class="sxs-lookup"><span data-stu-id="880c3-132">DLL</span></span><br/>                      | <dl> <span data-ttu-id="880c3-133"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="880c3-133"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="880c3-134">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="880c3-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="880c3-135">**\_LOGICALIDENTITY CIM**</span><span class="sxs-lookup"><span data-stu-id="880c3-135">**CIM\_LogicalIdentity**</span></span>](cim-logicalidentity.md)
</dt> <dt>

[<span data-ttu-id="880c3-136">**\_LOGICALIDENTITY CIM**</span><span class="sxs-lookup"><span data-stu-id="880c3-136">**CIM\_LogicalIdentity**</span></span>](/windows/desktop/CIMWin32Prov/cim-logicalidentity)
</dt> </dl>

 

