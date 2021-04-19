---
description: Représente une association dans laquelle une entrée d’une base de données de transfert s’applique à un port de commutateur.
ms.assetid: e63ac61d-ed0c-49e9-b056-4fcb6d1d5455
title: Classe CIM_SwitchPortDynamicForwarding
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_SwitchPortDynamicForwarding
- CIM_SwitchPortDynamicForwarding.Antecedent
- CIM_SwitchPortDynamicForwarding.Dependent
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 0e0d87e2ee5df6a7564d92fd1f8421dfa09abe20
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106518630"
---
# <a name="cim_switchportdynamicforwarding-class"></a><span data-ttu-id="38c0e-103">\_Classe CIM SwitchPortDynamicForwarding</span><span class="sxs-lookup"><span data-stu-id="38c0e-103">CIM\_SwitchPortDynamicForwarding class</span></span>

<span data-ttu-id="38c0e-104">Représente une association dans laquelle une entrée d’une base de données de transfert s’applique à un port de commutateur.</span><span class="sxs-lookup"><span data-stu-id="38c0e-104">Represents an association in which an entry of a forwarding database applies to a switch port.</span></span>

## <a name="syntax"></a><span data-ttu-id="38c0e-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="38c0e-105">Syntax</span></span>

``` syntax
[Association, Abstract, Version("2.7.0"), UMLPackagePath("CIM::Network::SwitchingBridging"), AMENDMENT]
class CIM_SwitchPortDynamicForwarding : CIM_Dependency
{
  CIM_SwitchPort             REF Antecedent;
  CIM_DynamicForwardingEntry REF Dependent;
};
```

## <a name="members"></a><span data-ttu-id="38c0e-106">Membres</span><span class="sxs-lookup"><span data-stu-id="38c0e-106">Members</span></span>

<span data-ttu-id="38c0e-107">La classe **CIM \_ SwitchPortDynamicForwarding** possède les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="38c0e-107">The **CIM\_SwitchPortDynamicForwarding** class has these types of members:</span></span>

-   [<span data-ttu-id="38c0e-108">Propriétés</span><span class="sxs-lookup"><span data-stu-id="38c0e-108">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="38c0e-109">Propriétés</span><span class="sxs-lookup"><span data-stu-id="38c0e-109">Properties</span></span>

<span data-ttu-id="38c0e-110">La classe **CIM \_ SwitchPortDynamicForwarding** possède les propriétés suivantes.</span><span class="sxs-lookup"><span data-stu-id="38c0e-110">The **CIM\_SwitchPortDynamicForwarding** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="38c0e-111">**Antécédent**</span><span class="sxs-lookup"><span data-stu-id="38c0e-111">**Antecedent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="38c0e-112">Type de données : **CIM \_ switchport**</span><span class="sxs-lookup"><span data-stu-id="38c0e-112">Data type: **CIM\_SwitchPort**</span></span>
</dt> <dt>

<span data-ttu-id="38c0e-113">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="38c0e-113">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="38c0e-114">Qualificateurs : [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Antecedent"), [**min**](/windows/desktop/WmiSdk/standard-qualifiers) (1)</span><span class="sxs-lookup"><span data-stu-id="38c0e-114">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Antecedent"), [**Min**](/windows/desktop/WmiSdk/standard-qualifiers) (1)</span></span>
</dt> </dl>

<span data-ttu-id="38c0e-115">Référence [**CIM \_ switchport**](cim-switchport.md) au port commuté.</span><span class="sxs-lookup"><span data-stu-id="38c0e-115">A [**CIM\_SwitchPort**](cim-switchport.md) reference to the switch port.</span></span>

</dd> <dt>

<span data-ttu-id="38c0e-116">**Charge**</span><span class="sxs-lookup"><span data-stu-id="38c0e-116">**Dependent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="38c0e-117">Type de données : **CIM \_ DynamicForwardingEntry**</span><span class="sxs-lookup"><span data-stu-id="38c0e-117">Data type: **CIM\_DynamicForwardingEntry**</span></span>
</dt> <dt>

<span data-ttu-id="38c0e-118">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="38c0e-118">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="38c0e-119">Qualificateurs : [**override**](/windows/desktop/WmiSdk/standard-qualifiers) (« Dependent »)</span><span class="sxs-lookup"><span data-stu-id="38c0e-119">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Dependent")</span></span>
</dt> </dl>

<span data-ttu-id="38c0e-120">Référence [**CIM \_ DynamicForwardingEntry**](cim-dynamicforwardingentry.md) à l’entrée de la base de données de transfert.</span><span class="sxs-lookup"><span data-stu-id="38c0e-120">A [**CIM\_DynamicForwardingEntry**](cim-dynamicforwardingentry.md) reference to the entry of the forwarding database.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="38c0e-121">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="38c0e-121">Requirements</span></span>



| <span data-ttu-id="38c0e-122">Condition requise</span><span class="sxs-lookup"><span data-stu-id="38c0e-122">Requirement</span></span> | <span data-ttu-id="38c0e-123">Valeur</span><span class="sxs-lookup"><span data-stu-id="38c0e-123">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="38c0e-124">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="38c0e-124">Minimum supported client</span></span><br/> | <span data-ttu-id="38c0e-125">Windows 8</span><span class="sxs-lookup"><span data-stu-id="38c0e-125">Windows 8</span></span><br/>                                                                                    |
| <span data-ttu-id="38c0e-126">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="38c0e-126">Minimum supported server</span></span><br/> | <span data-ttu-id="38c0e-127">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="38c0e-127">Windows Server 2012</span></span><br/>                                                                          |
| <span data-ttu-id="38c0e-128">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="38c0e-128">Namespace</span></span><br/>                | <span data-ttu-id="38c0e-129">\\Virtualisation racine \\ v2</span><span class="sxs-lookup"><span data-stu-id="38c0e-129">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="38c0e-130">MOF</span><span class="sxs-lookup"><span data-stu-id="38c0e-130">MOF</span></span><br/>                      | <dl> <span data-ttu-id="38c0e-131"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="38c0e-131"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="38c0e-132">DLL</span><span class="sxs-lookup"><span data-stu-id="38c0e-132">DLL</span></span><br/>                      | <dl> <span data-ttu-id="38c0e-133"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="38c0e-133"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="38c0e-134">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="38c0e-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="38c0e-135">**\_Dépendance CIM**</span><span class="sxs-lookup"><span data-stu-id="38c0e-135">**CIM\_Dependency**</span></span>](cim-dependency.md)
</dt> </dl>

 

