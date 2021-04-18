---
description: Représente une association entre un système informatique et sa capture instantanée de système virtuel la plus récemment appliquée.
ms.assetid: 722491a3-1c46-4d37-8bd6-7c7d6648a806
title: Classe CIM_LastAppliedSnapshot
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_LastAppliedSnapshot
- CIM_LastAppliedSnapshot.Antecedent
- CIM_LastAppliedSnapshot.Dependent
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 38efa9c5f02cd0ea40d993cc39ba05ac0b6fde3b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106520206"
---
# <a name="cim_lastappliedsnapshot-class"></a><span data-ttu-id="b51da-103">\_Classe CIM LastAppliedSnapshot</span><span class="sxs-lookup"><span data-stu-id="b51da-103">CIM\_LastAppliedSnapshot class</span></span>

<span data-ttu-id="b51da-104">Représente une association entre un système informatique et sa capture instantanée de système virtuel la plus récemment appliquée.</span><span class="sxs-lookup"><span data-stu-id="b51da-104">Represents an association between a computer system and its most recently applied virtual system snapshot.</span></span>

## <a name="syntax"></a><span data-ttu-id="b51da-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="b51da-105">Syntax</span></span>

``` syntax
[Association, Abstract, Version("2.22.0"), AMENDMENT]
class CIM_LastAppliedSnapshot : CIM_Dependency
{
  CIM_VirtualSystemSettingData REF Antecedent;
  CIM_ComputerSystem           REF Dependent;
};
```

## <a name="members"></a><span data-ttu-id="b51da-106">Membres</span><span class="sxs-lookup"><span data-stu-id="b51da-106">Members</span></span>

<span data-ttu-id="b51da-107">La classe **CIM \_ LastAppliedSnapshot** possède les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="b51da-107">The **CIM\_LastAppliedSnapshot** class has these types of members:</span></span>

-   [<span data-ttu-id="b51da-108">Propriétés</span><span class="sxs-lookup"><span data-stu-id="b51da-108">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="b51da-109">Propriétés</span><span class="sxs-lookup"><span data-stu-id="b51da-109">Properties</span></span>

<span data-ttu-id="b51da-110">La classe **CIM \_ LastAppliedSnapshot** possède les propriétés suivantes.</span><span class="sxs-lookup"><span data-stu-id="b51da-110">The **CIM\_LastAppliedSnapshot** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="b51da-111">**Antécédent**</span><span class="sxs-lookup"><span data-stu-id="b51da-111">**Antecedent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b51da-112">Type de données : **CIM \_ VirtualSystemSettingData**</span><span class="sxs-lookup"><span data-stu-id="b51da-112">Data type: **CIM\_VirtualSystemSettingData**</span></span>
</dt> <dt>

<span data-ttu-id="b51da-113">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="b51da-113">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b51da-114">Qualificateurs : [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Antecedent"), [**min**](/windows/desktop/WmiSdk/standard-qualifiers) (0), [**Max**](/windows/desktop/WmiSdk/standard-qualifiers) (1)</span><span class="sxs-lookup"><span data-stu-id="b51da-114">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Antecedent"), [**Min**](/windows/desktop/WmiSdk/standard-qualifiers) (0), [**Max**](/windows/desktop/WmiSdk/standard-qualifiers) (1)</span></span>
</dt> </dl>

<span data-ttu-id="b51da-115">La capture instantanée du système virtuel qui a été appliquée pour la dernière fois au système informatique.</span><span class="sxs-lookup"><span data-stu-id="b51da-115">The virtual system snapshot that was last applied to the computer system.</span></span>

</dd> <dt>

<span data-ttu-id="b51da-116">**Charge**</span><span class="sxs-lookup"><span data-stu-id="b51da-116">**Dependent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b51da-117">Type de données **: \_ CIM CIM**</span><span class="sxs-lookup"><span data-stu-id="b51da-117">Data type: **CIM\_ComputerSystem**</span></span>
</dt> <dt>

<span data-ttu-id="b51da-118">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="b51da-118">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b51da-119">Qualificateurs : [**override**](/windows/desktop/WmiSdk/standard-qualifiers) (« Dependent »), [**min**](/windows/desktop/WmiSdk/standard-qualifiers) (0), [**Max**](/windows/desktop/WmiSdk/standard-qualifiers) (1)</span><span class="sxs-lookup"><span data-stu-id="b51da-119">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Dependent"), [**Min**](/windows/desktop/WmiSdk/standard-qualifiers) (0), [**Max**](/windows/desktop/WmiSdk/standard-qualifiers) (1)</span></span>
</dt> </dl>

<span data-ttu-id="b51da-120">Système informatique.</span><span class="sxs-lookup"><span data-stu-id="b51da-120">The computer system.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="b51da-121">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="b51da-121">Requirements</span></span>



| <span data-ttu-id="b51da-122">Condition requise</span><span class="sxs-lookup"><span data-stu-id="b51da-122">Requirement</span></span> | <span data-ttu-id="b51da-123">Valeur</span><span class="sxs-lookup"><span data-stu-id="b51da-123">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b51da-124">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="b51da-124">Minimum supported client</span></span><br/> | <span data-ttu-id="b51da-125">Windows 8</span><span class="sxs-lookup"><span data-stu-id="b51da-125">Windows 8</span></span><br/>                                                                                    |
| <span data-ttu-id="b51da-126">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="b51da-126">Minimum supported server</span></span><br/> | <span data-ttu-id="b51da-127">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="b51da-127">Windows Server 2012</span></span><br/>                                                                          |
| <span data-ttu-id="b51da-128">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="b51da-128">Namespace</span></span><br/>                | <span data-ttu-id="b51da-129">\\Virtualisation racine \\ v2</span><span class="sxs-lookup"><span data-stu-id="b51da-129">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="b51da-130">MOF</span><span class="sxs-lookup"><span data-stu-id="b51da-130">MOF</span></span><br/>                      | <dl> <span data-ttu-id="b51da-131"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="b51da-131"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="b51da-132">DLL</span><span class="sxs-lookup"><span data-stu-id="b51da-132">DLL</span></span><br/>                      | <dl> <span data-ttu-id="b51da-133"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="b51da-133"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="b51da-134">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="b51da-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b51da-135">**\_Dépendance CIM**</span><span class="sxs-lookup"><span data-stu-id="b51da-135">**CIM\_Dependency**</span></span>](cim-dependency.md)
</dt> </dl>

 

