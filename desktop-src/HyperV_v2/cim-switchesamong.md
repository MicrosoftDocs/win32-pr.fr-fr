---
description: Représente un service de commutation qui bascule les images entre les ports de commutateur.
ms.assetid: ee2d4831-df00-408c-b350-26d2d1d3e8aa
title: Classe CIM_SwitchesAmong
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_SwitchesAmong
- CIM_SwitchesAmong.Antecedent
- CIM_SwitchesAmong.Dependent
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 16a87797b4a138ef79be3d5ea8c6304d2ce4a942
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104113574"
---
# <a name="cim_switchesamong-class"></a><span data-ttu-id="467ad-103">\_Classe CIM SwitchesAmong</span><span class="sxs-lookup"><span data-stu-id="467ad-103">CIM\_SwitchesAmong class</span></span>

<span data-ttu-id="467ad-104">Représente un service de commutation qui bascule les images entre les ports de commutateur.</span><span class="sxs-lookup"><span data-stu-id="467ad-104">Represents a switch service, which switches frames between switch ports.</span></span>

## <a name="syntax"></a><span data-ttu-id="467ad-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="467ad-105">Syntax</span></span>

``` syntax
[Association, Abstract, Version("2.6.0"), UMLPackagePath("CIM::Network::SwitchingBridging")]
class CIM_SwitchesAmong : CIM_ForwardsAmong
{
  CIM_SwitchPort    REF Antecedent;
  CIM_SwitchService REF Dependent;
};
```

## <a name="members"></a><span data-ttu-id="467ad-106">Membres</span><span class="sxs-lookup"><span data-stu-id="467ad-106">Members</span></span>

<span data-ttu-id="467ad-107">La classe **CIM \_ SwitchesAmong** possède les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="467ad-107">The **CIM\_SwitchesAmong** class has these types of members:</span></span>

-   [<span data-ttu-id="467ad-108">Propriétés</span><span class="sxs-lookup"><span data-stu-id="467ad-108">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="467ad-109">Propriétés</span><span class="sxs-lookup"><span data-stu-id="467ad-109">Properties</span></span>

<span data-ttu-id="467ad-110">La classe **CIM \_ SwitchesAmong** possède les propriétés suivantes.</span><span class="sxs-lookup"><span data-stu-id="467ad-110">The **CIM\_SwitchesAmong** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="467ad-111">**Antécédent**</span><span class="sxs-lookup"><span data-stu-id="467ad-111">**Antecedent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="467ad-112">Type de données : **CIM \_ switchport**</span><span class="sxs-lookup"><span data-stu-id="467ad-112">Data type: **CIM\_SwitchPort**</span></span>
</dt> <dt>

<span data-ttu-id="467ad-113">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="467ad-113">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="467ad-114">Qualificateurs : [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Antecedent")</span><span class="sxs-lookup"><span data-stu-id="467ad-114">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Antecedent")</span></span>
</dt> </dl>

<span data-ttu-id="467ad-115">Référence [**CIM \_ switchport**](cim-switchport.md) au port commuté.</span><span class="sxs-lookup"><span data-stu-id="467ad-115">A [**CIM\_SwitchPort**](cim-switchport.md) reference to the switch port.</span></span>

</dd> <dt>

<span data-ttu-id="467ad-116">**Charge**</span><span class="sxs-lookup"><span data-stu-id="467ad-116">**Dependent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="467ad-117">Type de données : **CIM \_ SwitchService**</span><span class="sxs-lookup"><span data-stu-id="467ad-117">Data type: **CIM\_SwitchService**</span></span>
</dt> <dt>

<span data-ttu-id="467ad-118">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="467ad-118">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="467ad-119">Qualificateurs : [**override**](/windows/desktop/WmiSdk/standard-qualifiers) (« Dependent »), [**Max**](/windows/desktop/WmiSdk/standard-qualifiers) (1)</span><span class="sxs-lookup"><span data-stu-id="467ad-119">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Dependent"), [**Max**](/windows/desktop/WmiSdk/standard-qualifiers) (1)</span></span>
</dt> </dl>

<span data-ttu-id="467ad-120">Référence [**CIM \_ SwitchService**](cim-switchservice.md) au service de commutation.</span><span class="sxs-lookup"><span data-stu-id="467ad-120">A [**CIM\_SwitchService**](cim-switchservice.md) reference to the switching service.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="467ad-121">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="467ad-121">Requirements</span></span>



| <span data-ttu-id="467ad-122">Condition requise</span><span class="sxs-lookup"><span data-stu-id="467ad-122">Requirement</span></span> | <span data-ttu-id="467ad-123">Valeur</span><span class="sxs-lookup"><span data-stu-id="467ad-123">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="467ad-124">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="467ad-124">Minimum supported client</span></span><br/> | <span data-ttu-id="467ad-125">Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="467ad-125">Windows 8.1</span></span><br/>                                                                                  |
| <span data-ttu-id="467ad-126">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="467ad-126">Minimum supported server</span></span><br/> | <span data-ttu-id="467ad-127">Windows Server 2012 R2</span><span class="sxs-lookup"><span data-stu-id="467ad-127">Windows Server 2012 R2</span></span><br/>                                                                       |
| <span data-ttu-id="467ad-128">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="467ad-128">Namespace</span></span><br/>                | <span data-ttu-id="467ad-129">\\Virtualisation racine \\ v2</span><span class="sxs-lookup"><span data-stu-id="467ad-129">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="467ad-130">MOF</span><span class="sxs-lookup"><span data-stu-id="467ad-130">MOF</span></span><br/>                      | <dl> <span data-ttu-id="467ad-131"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="467ad-131"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="467ad-132">DLL</span><span class="sxs-lookup"><span data-stu-id="467ad-132">DLL</span></span><br/>                      | <dl> <span data-ttu-id="467ad-133"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="467ad-133"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="467ad-134">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="467ad-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="467ad-135">**\_FORWARDSAMONG CIM**</span><span class="sxs-lookup"><span data-stu-id="467ad-135">**CIM\_ForwardsAmong**</span></span>](cim-forwardsamong.md)
</dt> </dl>

 

