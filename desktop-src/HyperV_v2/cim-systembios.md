---
description: Associe un BIOS à un système informatique.
ms.assetid: a06af789-75c8-4d58-8a25-572dcf1091e2
title: Classe CIM_SystemBIOS
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_SystemBIOS
- CIM_SystemBIOS.GroupComponent
- CIM_SystemBIOS.PartComponent
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: faa3130544fdb97bdf216fa266bc9e8cfe1815bf
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104034327"
---
# <a name="cim_systembios-class"></a><span data-ttu-id="a2791-103">\_Classe CIM SystemBIOS</span><span class="sxs-lookup"><span data-stu-id="a2791-103">CIM\_SystemBIOS class</span></span>

<span data-ttu-id="a2791-104">Associe un BIOS à un système informatique.</span><span class="sxs-lookup"><span data-stu-id="a2791-104">Associates a BIOS with a computer system.</span></span>

## <a name="syntax"></a><span data-ttu-id="a2791-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="a2791-105">Syntax</span></span>

``` syntax
[Association, Aggregation, Abstract, Version("2.7.0"), UMLPackagePath("CIM::Application::BIOS"), AMENDMENT]
class CIM_SystemBIOS : CIM_SystemComponent
{
  CIM_ComputerSystem REF GroupComponent;
  CIM_BIOSElement    REF PartComponent;
};
```

## <a name="members"></a><span data-ttu-id="a2791-106">Membres</span><span class="sxs-lookup"><span data-stu-id="a2791-106">Members</span></span>

<span data-ttu-id="a2791-107">La classe **CIM \_ SystemBIOS** possède les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="a2791-107">The **CIM\_SystemBIOS** class has these types of members:</span></span>

-   [<span data-ttu-id="a2791-108">Propriétés</span><span class="sxs-lookup"><span data-stu-id="a2791-108">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="a2791-109">Propriétés</span><span class="sxs-lookup"><span data-stu-id="a2791-109">Properties</span></span>

<span data-ttu-id="a2791-110">La classe **CIM \_ SystemBIOS** possède les propriétés suivantes.</span><span class="sxs-lookup"><span data-stu-id="a2791-110">The **CIM\_SystemBIOS** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="a2791-111">**GroupComponent**</span><span class="sxs-lookup"><span data-stu-id="a2791-111">**GroupComponent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a2791-112">Type de données **: \_ CIM CIM**</span><span class="sxs-lookup"><span data-stu-id="a2791-112">Data type: **CIM\_ComputerSystem**</span></span>
</dt> <dt>

<span data-ttu-id="a2791-113">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="a2791-113">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a2791-114">Qualificateurs : [**Aggregate**](/windows/desktop/WmiSdk/standard-qualifiers), [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("GroupComponent"), [**Max**](/windows/desktop/WmiSdk/standard-qualifiers) (1)</span><span class="sxs-lookup"><span data-stu-id="a2791-114">Qualifiers: [**Aggregate**](/windows/desktop/WmiSdk/standard-qualifiers), [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("GroupComponent"), [**Max**](/windows/desktop/WmiSdk/standard-qualifiers) (1)</span></span>
</dt> </dl>

<span data-ttu-id="a2791-115">Système informatique qui démarre à partir du BIOS.</span><span class="sxs-lookup"><span data-stu-id="a2791-115">The computer system that boots from the BIOS.</span></span>

</dd> <dt>

<span data-ttu-id="a2791-116">**PartComponent**</span><span class="sxs-lookup"><span data-stu-id="a2791-116">**PartComponent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a2791-117">Type de données : **CIM \_ BIOSElement**</span><span class="sxs-lookup"><span data-stu-id="a2791-117">Data type: **CIM\_BIOSElement**</span></span>
</dt> <dt>

<span data-ttu-id="a2791-118">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="a2791-118">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a2791-119">Qualificateurs : [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("PartComponent")</span><span class="sxs-lookup"><span data-stu-id="a2791-119">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("PartComponent")</span></span>
</dt> </dl>

<span data-ttu-id="a2791-120">BIOS.</span><span class="sxs-lookup"><span data-stu-id="a2791-120">The BIOS.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="a2791-121">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="a2791-121">Requirements</span></span>



| <span data-ttu-id="a2791-122">Condition requise</span><span class="sxs-lookup"><span data-stu-id="a2791-122">Requirement</span></span> | <span data-ttu-id="a2791-123">Valeur</span><span class="sxs-lookup"><span data-stu-id="a2791-123">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a2791-124">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="a2791-124">Minimum supported client</span></span><br/> | <span data-ttu-id="a2791-125">Windows 8</span><span class="sxs-lookup"><span data-stu-id="a2791-125">Windows 8</span></span><br/>                                                                                    |
| <span data-ttu-id="a2791-126">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="a2791-126">Minimum supported server</span></span><br/> | <span data-ttu-id="a2791-127">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="a2791-127">Windows Server 2012</span></span><br/>                                                                          |
| <span data-ttu-id="a2791-128">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="a2791-128">Namespace</span></span><br/>                | <span data-ttu-id="a2791-129">\\Virtualisation racine \\ v2</span><span class="sxs-lookup"><span data-stu-id="a2791-129">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="a2791-130">MOF</span><span class="sxs-lookup"><span data-stu-id="a2791-130">MOF</span></span><br/>                      | <dl> <span data-ttu-id="a2791-131"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="a2791-131"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="a2791-132">DLL</span><span class="sxs-lookup"><span data-stu-id="a2791-132">DLL</span></span><br/>                      | <dl> <span data-ttu-id="a2791-133"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="a2791-133"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="a2791-134">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="a2791-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a2791-135">**\_SYSTEMCOMPONENT CIM**</span><span class="sxs-lookup"><span data-stu-id="a2791-135">**CIM\_SystemComponent**</span></span>](cim-systemcomponent.md)
</dt> </dl>

 

