---
description: Connecte un port de commutateur à une entrée de transfert dynamique (adresse MAC apprise).
ms.assetid: 70687D56-1282-46C7-AB4E-60E32B9DBA14
title: Classe Msvm_SwitchPortDynamicForwarding
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_SwitchPortDynamicForwarding
- Msvm_SwitchPortDynamicForwarding.Antecedent
- Msvm_SwitchPortDynamicForwarding.Dependent
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 9e6dda46302e9e8c58710bad1f4221e14e2c3f4b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106520505"
---
# <a name="msvm_switchportdynamicforwarding-class"></a><span data-ttu-id="3bbb5-103">MSVM \_ SwitchPortDynamicForwarding, classe</span><span class="sxs-lookup"><span data-stu-id="3bbb5-103">Msvm\_SwitchPortDynamicForwarding class</span></span>

<span data-ttu-id="3bbb5-104">Connecte un port de commutateur à une entrée de transfert dynamique (adresse MAC apprise).</span><span class="sxs-lookup"><span data-stu-id="3bbb5-104">Connects a switch port to a dynamic forward entry (learned MAC address).</span></span> <span data-ttu-id="3bbb5-105">Cela est utile pour rechercher toutes les adresses MAC apprises pour un port spécifié.</span><span class="sxs-lookup"><span data-stu-id="3bbb5-105">This is useful in finding all of the learned MAC addresses for a specified port.</span></span>

<span data-ttu-id="3bbb5-106">La syntaxe suivante est simplifiée format MOF (MOF) et comprend toutes les propriétés héritées.</span><span class="sxs-lookup"><span data-stu-id="3bbb5-106">The following syntax is simplified Managed Object Format (MOF) code, and it includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="3bbb5-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="3bbb5-107">Syntax</span></span>

``` syntax
[Association, Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_SwitchPortDynamicForwarding : CIM_SwitchPortDynamicForwarding
{
  Msvm_EthernetSwitchPort     REF Antecedent;
  Msvm_DynamicForwardingEntry REF Dependent;
};
```

## <a name="members"></a><span data-ttu-id="3bbb5-108">Membres</span><span class="sxs-lookup"><span data-stu-id="3bbb5-108">Members</span></span>

<span data-ttu-id="3bbb5-109">La classe **MSVM \_ SwitchPortDynamicForwarding** possède les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="3bbb5-109">The **Msvm\_SwitchPortDynamicForwarding** class has these types of members:</span></span>

-   [<span data-ttu-id="3bbb5-110">Propriétés</span><span class="sxs-lookup"><span data-stu-id="3bbb5-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="3bbb5-111">Propriétés</span><span class="sxs-lookup"><span data-stu-id="3bbb5-111">Properties</span></span>

<span data-ttu-id="3bbb5-112">La classe **MSVM \_ SwitchPortDynamicForwarding** possède les propriétés suivantes.</span><span class="sxs-lookup"><span data-stu-id="3bbb5-112">The **Msvm\_SwitchPortDynamicForwarding** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="3bbb5-113">**Antécédent**</span><span class="sxs-lookup"><span data-stu-id="3bbb5-113">**Antecedent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3bbb5-114">Type de données : **[ **MSVM \_ EthernetSwitchPort**](msvm-ethernetswitchport.md)**</span><span class="sxs-lookup"><span data-stu-id="3bbb5-114">Data type: **[**Msvm\_EthernetSwitchPort**](msvm-ethernetswitchport.md)**</span></span>
</dt> <dt>

<span data-ttu-id="3bbb5-115">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="3bbb5-115">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="3bbb5-116">Qualificateurs : [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Antecedent")</span><span class="sxs-lookup"><span data-stu-id="3bbb5-116">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Antecedent")</span></span>
</dt> </dl>

<span data-ttu-id="3bbb5-117">Référence à une instance de la classe [**MSVM \_ EthernetSwitchPort**](msvm-ethernetswitchport.md) qui représente le port commuté.</span><span class="sxs-lookup"><span data-stu-id="3bbb5-117">A reference to an instance of the [**Msvm\_EthernetSwitchPort**](msvm-ethernetswitchport.md) class that represents the switch port.</span></span>

</dd> <dt>

<span data-ttu-id="3bbb5-118">**Charge**</span><span class="sxs-lookup"><span data-stu-id="3bbb5-118">**Dependent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3bbb5-119">Type de données : **[ **MSVM \_ DynamicForwardingEntry**](msvm-dynamicforwardingentry.md)**</span><span class="sxs-lookup"><span data-stu-id="3bbb5-119">Data type: **[**Msvm\_DynamicForwardingEntry**](msvm-dynamicforwardingentry.md)**</span></span>
</dt> <dt>

<span data-ttu-id="3bbb5-120">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="3bbb5-120">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="3bbb5-121">Qualificateurs : [**override**](/windows/desktop/WmiSdk/standard-qualifiers) (« Dependent »)</span><span class="sxs-lookup"><span data-stu-id="3bbb5-121">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Dependent")</span></span>
</dt> </dl>

<span data-ttu-id="3bbb5-122">Référence à une instance de la classe [**MSVM \_ DynamicForwardingEntry**](msvm-dynamicforwardingentry.md) qui représente l’entrée de transfert dynamique de la base de données de transfert.</span><span class="sxs-lookup"><span data-stu-id="3bbb5-122">A reference to an instance of the [**Msvm\_DynamicForwardingEntry**](msvm-dynamicforwardingentry.md) class that represents the dynamic forwarding entry of the forwarding database.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="3bbb5-123">Notes</span><span class="sxs-lookup"><span data-stu-id="3bbb5-123">Remarks</span></span>

<span data-ttu-id="3bbb5-124">L’accès à la classe **MSVM \_ SwitchPortDynamicForwarding** peut être limité par le filtrage UAC.</span><span class="sxs-lookup"><span data-stu-id="3bbb5-124">Access to the **Msvm\_SwitchPortDynamicForwarding** class might be restricted by UAC Filtering.</span></span> <span data-ttu-id="3bbb5-125">Pour plus d’informations, consultez [contrôle de compte d’utilisateur et WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span><span class="sxs-lookup"><span data-stu-id="3bbb5-125">For more information, see [User Account Control and WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span></span>

## <a name="examples"></a><span data-ttu-id="3bbb5-126">Exemples</span><span class="sxs-lookup"><span data-stu-id="3bbb5-126">Examples</span></span>

<span data-ttu-id="3bbb5-127">Consultez [interrogation d’objets de mise en réseau](querying-networking-objects.md).</span><span class="sxs-lookup"><span data-stu-id="3bbb5-127">See [Querying networking objects](querying-networking-objects.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="3bbb5-128">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="3bbb5-128">Requirements</span></span>



| <span data-ttu-id="3bbb5-129">Condition requise</span><span class="sxs-lookup"><span data-stu-id="3bbb5-129">Requirement</span></span> | <span data-ttu-id="3bbb5-130">Valeur</span><span class="sxs-lookup"><span data-stu-id="3bbb5-130">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3bbb5-131">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="3bbb5-131">Minimum supported client</span></span><br/> | <span data-ttu-id="3bbb5-132">Applications de \[ Bureau Windows 8 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="3bbb5-132">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="3bbb5-133">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="3bbb5-133">Minimum supported server</span></span><br/> | <span data-ttu-id="3bbb5-134">Applications de bureau Windows Server 2012 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="3bbb5-134">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="3bbb5-135">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="3bbb5-135">Namespace</span></span><br/>                | <span data-ttu-id="3bbb5-136">\\Virtualisation racine \\ v2</span><span class="sxs-lookup"><span data-stu-id="3bbb5-136">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="3bbb5-137">MOF</span><span class="sxs-lookup"><span data-stu-id="3bbb5-137">MOF</span></span><br/>                      | <dl> <span data-ttu-id="3bbb5-138"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="3bbb5-138"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="3bbb5-139">DLL</span><span class="sxs-lookup"><span data-stu-id="3bbb5-139">DLL</span></span><br/>                      | <dl> <span data-ttu-id="3bbb5-140"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="3bbb5-140"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="3bbb5-141">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="3bbb5-141">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3bbb5-142">**\_SWITCHPORTDYNAMICFORWARDING CIM**</span><span class="sxs-lookup"><span data-stu-id="3bbb5-142">**CIM\_SwitchPortDynamicForwarding**</span></span>](cim-switchportdynamicforwarding.md)
</dt> <dt>

<span data-ttu-id="3bbb5-143">[**\_SWITCHPORTDYNAMICFORWARDING CIM**](/previous-versions//cc136921(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="3bbb5-143">[**CIM\_SwitchPortDynamicForwarding**](/previous-versions//cc136921(v=vs.85))</span></span>
</dt> </dl>

 

