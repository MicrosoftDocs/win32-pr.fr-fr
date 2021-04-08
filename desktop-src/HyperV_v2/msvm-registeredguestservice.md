---
description: Représente une association entre une instance de MSVM \_ GuestServiceInterfaceComponent et une instance de MSVM \_ GuestService, qui représente un service s’exécutant dans l’invité.
ms.assetid: 246CFAC1-7D83-4DE7-B9D3-96326511E08B
title: Classe Msvm_RegisteredGuestService
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_RegisteredGuestService
- Msvm_RegisteredGuestService.Antecedent
- Msvm_RegisteredGuestService.Dependent
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 850d7f081b070fd34ef11bc56e8cd1f914e498b0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103756892"
---
# <a name="msvm_registeredguestservice-class"></a><span data-ttu-id="5f7d1-103">MSVM \_ RegisteredGuestService, classe</span><span class="sxs-lookup"><span data-stu-id="5f7d1-103">Msvm\_RegisteredGuestService class</span></span>

<span data-ttu-id="5f7d1-104">Représente une association entre une instance de [**MSVM \_ GuestServiceInterfaceComponent**](msvm-guestserviceinterfacecomponent.md) et une instance de [**MSVM \_ GuestService**](msvm-guestservice.md), qui représente un service s’exécutant dans l’invité.</span><span class="sxs-lookup"><span data-stu-id="5f7d1-104">Represents an association between an instance of [**Msvm\_GuestServiceInterfaceComponent**](msvm-guestserviceinterfacecomponent.md) and an instance of [**Msvm\_GuestService**](msvm-guestservice.md), which represents a service running in the guest.</span></span> <span data-ttu-id="5f7d1-105">Cette classe dérive de la classe de [**\_ dépendance CIM**](/windows/desktop/CIMWin32Prov/cim-dependency) .</span><span class="sxs-lookup"><span data-stu-id="5f7d1-105">This class derives from the [**CIM\_Dependency**](/windows/desktop/CIMWin32Prov/cim-dependency) class.</span></span>

<span data-ttu-id="5f7d1-106">La syntaxe suivante issue du code MOF est simplifiée et inclut toutes les propriétés héritées.</span><span class="sxs-lookup"><span data-stu-id="5f7d1-106">The following syntax is simplified from MOF code and includes all inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="5f7d1-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="5f7d1-107">Syntax</span></span>

``` syntax
[Association, Aggregation, Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_RegisteredGuestService : CIM_Dependency
{
  Msvm_GuestServiceInterfaceComponent REF Antecedent;
  Msvm_GuestService                   REF Dependent;
};
```

## <a name="members"></a><span data-ttu-id="5f7d1-108">Membres</span><span class="sxs-lookup"><span data-stu-id="5f7d1-108">Members</span></span>

<span data-ttu-id="5f7d1-109">La classe **MSVM \_ RegisteredGuestService** possède les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="5f7d1-109">The **Msvm\_RegisteredGuestService** class has these types of members:</span></span>

-   [<span data-ttu-id="5f7d1-110">Propriétés</span><span class="sxs-lookup"><span data-stu-id="5f7d1-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="5f7d1-111">Propriétés</span><span class="sxs-lookup"><span data-stu-id="5f7d1-111">Properties</span></span>

<span data-ttu-id="5f7d1-112">La classe **MSVM \_ RegisteredGuestService** possède les propriétés suivantes.</span><span class="sxs-lookup"><span data-stu-id="5f7d1-112">The **Msvm\_RegisteredGuestService** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="5f7d1-113">**Antécédent**</span><span class="sxs-lookup"><span data-stu-id="5f7d1-113">**Antecedent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5f7d1-114">Type de données : **[ **MSVM \_ GuestServiceInterfaceComponent**](msvm-guestserviceinterfacecomponent.md)**</span><span class="sxs-lookup"><span data-stu-id="5f7d1-114">Data type: **[**Msvm\_GuestServiceInterfaceComponent**](msvm-guestserviceinterfacecomponent.md)**</span></span>
</dt> <dt>

<span data-ttu-id="5f7d1-115">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="5f7d1-115">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="5f7d1-116">Qualificateurs : [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("CIM \_ dependency. Antecedent")</span><span class="sxs-lookup"><span data-stu-id="5f7d1-116">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("CIM\_Dependency.Antecedent")</span></span>
</dt> </dl>

<span data-ttu-id="5f7d1-117">Référence au composant de l’interface de service invité dans cette association.</span><span class="sxs-lookup"><span data-stu-id="5f7d1-117">Reference to the guest service interface component in this association.</span></span>

</dd> <dt>

<span data-ttu-id="5f7d1-118">**Charge**</span><span class="sxs-lookup"><span data-stu-id="5f7d1-118">**Dependent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5f7d1-119">Type de données : **[ **MSVM \_ GuestService**](msvm-guestservice.md)**</span><span class="sxs-lookup"><span data-stu-id="5f7d1-119">Data type: **[**Msvm\_GuestService**](msvm-guestservice.md)**</span></span>
</dt> <dt>

<span data-ttu-id="5f7d1-120">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="5f7d1-120">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="5f7d1-121">Qualificateurs : [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("dépendance CIM \_ . dependent")</span><span class="sxs-lookup"><span data-stu-id="5f7d1-121">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("CIM\_Dependency.Dependent")</span></span>
</dt> </dl>

<span data-ttu-id="5f7d1-122">Référence au service invité inscrit qui dépend de la propriété **Antecedent** .</span><span class="sxs-lookup"><span data-stu-id="5f7d1-122">Reference to the registered guest service that is dependent on the **Antecedent** property.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="5f7d1-123">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="5f7d1-123">Requirements</span></span>



| <span data-ttu-id="5f7d1-124">Condition requise</span><span class="sxs-lookup"><span data-stu-id="5f7d1-124">Requirement</span></span> | <span data-ttu-id="5f7d1-125">Valeur</span><span class="sxs-lookup"><span data-stu-id="5f7d1-125">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5f7d1-126">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="5f7d1-126">Minimum supported client</span></span><br/> | <span data-ttu-id="5f7d1-127">Windows 8.1 les \[ applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="5f7d1-127">Windows 8.1 \[desktop apps only\]</span></span><br/>                                                            |
| <span data-ttu-id="5f7d1-128">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="5f7d1-128">Minimum supported server</span></span><br/> | <span data-ttu-id="5f7d1-129">Applications de bureau Windows Server 2012 R2 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="5f7d1-129">Windows Server 2012 R2 \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="5f7d1-130">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="5f7d1-130">Namespace</span></span><br/>                | <span data-ttu-id="5f7d1-131">\\Virtualisation racine \\ v2</span><span class="sxs-lookup"><span data-stu-id="5f7d1-131">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="5f7d1-132">MOF</span><span class="sxs-lookup"><span data-stu-id="5f7d1-132">MOF</span></span><br/>                      | <dl> <span data-ttu-id="5f7d1-133"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="5f7d1-133"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="5f7d1-134">DLL</span><span class="sxs-lookup"><span data-stu-id="5f7d1-134">DLL</span></span><br/>                      | <dl> <span data-ttu-id="5f7d1-135"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="5f7d1-135"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="5f7d1-136">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="5f7d1-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5f7d1-137">**\_Dépendance CIM**</span><span class="sxs-lookup"><span data-stu-id="5f7d1-137">**CIM\_Dependency**</span></span>](cim-dependency.md)
</dt> <dt>

[<span data-ttu-id="5f7d1-138">**\_Dépendance CIM**</span><span class="sxs-lookup"><span data-stu-id="5f7d1-138">**CIM\_Dependency**</span></span>](/windows/desktop/CIMWin32Prov/cim-dependency)
</dt> </dl>

 

