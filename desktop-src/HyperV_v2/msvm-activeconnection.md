---
description: Connecte un port commuté au point de terminaison LAN auquel le port est connecté.
ms.assetid: 963EC004-6A67-4F75-BD93-1BCD17F32490
title: Classe Msvm_ActiveConnection
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_ActiveConnection
- Msvm_ActiveConnection.Antecedent
- Msvm_ActiveConnection.Dependent
- Msvm_ActiveConnection.TrafficType
- Msvm_ActiveConnection.OtherTrafficDescription
- Msvm_ActiveConnection.IsUnidirectional
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: cf682fac419658785cfe7594aa6fc17e4b2dd28e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103867306"
---
# <a name="msvm_activeconnection-class"></a><span data-ttu-id="4046d-103">MSVM, \_ classe ActiveConnection</span><span class="sxs-lookup"><span data-stu-id="4046d-103">Msvm\_ActiveConnection class</span></span>

<span data-ttu-id="4046d-104">Connecte un port commuté au point de terminaison LAN auquel le port est connecté.</span><span class="sxs-lookup"><span data-stu-id="4046d-104">Connects a switch port to the LAN endpoint to which the port is connected.</span></span> <span data-ttu-id="4046d-105">L’existence de cet objet signifie que le port commuté et le point de terminaison LAN sont activement connectés et que le port Ethernet associé au point de terminaison LAN peut communiquer avec le réseau via le port commuté.</span><span class="sxs-lookup"><span data-stu-id="4046d-105">The existence of this object means that the switch port and the LAN endpoint are actively connected and the Ethernet port associated with the LAN endpoint can communicate with the network through the switch port.</span></span>

<span data-ttu-id="4046d-106">La syntaxe suivante est simplifiée format MOF (MOF) et comprend toutes les propriétés héritées.</span><span class="sxs-lookup"><span data-stu-id="4046d-106">The following syntax is simplified Managed Object Format (MOF) code, and it includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="4046d-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="4046d-107">Syntax</span></span>

``` syntax
[Association, Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_ActiveConnection : CIM_ActiveConnection
{
  Msvm_LANEndpoint REF Antecedent;
  CIM_LANEndpoint  REF Dependent;
  uint16               TrafficType;
  string               OtherTrafficDescription;
  boolean              IsUnidirectional;
};
```

## <a name="members"></a><span data-ttu-id="4046d-108">Membres</span><span class="sxs-lookup"><span data-stu-id="4046d-108">Members</span></span>

<span data-ttu-id="4046d-109">La classe **MSVM \_ ActiveConnection** possède les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="4046d-109">The **Msvm\_ActiveConnection** class has these types of members:</span></span>

-   [<span data-ttu-id="4046d-110">Propriétés</span><span class="sxs-lookup"><span data-stu-id="4046d-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="4046d-111">Propriétés</span><span class="sxs-lookup"><span data-stu-id="4046d-111">Properties</span></span>

<span data-ttu-id="4046d-112">La classe **MSVM \_ ActiveConnection** a ces propriétés.</span><span class="sxs-lookup"><span data-stu-id="4046d-112">The **Msvm\_ActiveConnection** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="4046d-113">**Antécédent**</span><span class="sxs-lookup"><span data-stu-id="4046d-113">**Antecedent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4046d-114">Type de données : **[ **MSVM \_ LANEndpoint**](msvm-lanendpoint.md)**</span><span class="sxs-lookup"><span data-stu-id="4046d-114">Data type: **[**Msvm\_LANEndpoint**](msvm-lanendpoint.md)**</span></span>
</dt> <dt>

<span data-ttu-id="4046d-115">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="4046d-115">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="4046d-116">Qualificateurs : [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Antecedent")</span><span class="sxs-lookup"><span data-stu-id="4046d-116">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Antecedent")</span></span>
</dt> </dl>

<span data-ttu-id="4046d-117">Référence à une instance de la classe [**MSVM \_ LANEndpoint**](msvm-lanendpoint.md) qui représente le point d’accès au service (SAP) qui est configuré pour communiquer ou qui communique activement avec le SAP dépendant.</span><span class="sxs-lookup"><span data-stu-id="4046d-117">A reference to an instance of the [**Msvm\_LANEndpoint**](msvm-lanendpoint.md) class that represents the service access point (SAP) that is configured to communicate or is actively communicating with the dependent SAP.</span></span> <span data-ttu-id="4046d-118">Dans une connexion unidirectionnelle, ce SAP est celui qui transmet.</span><span class="sxs-lookup"><span data-stu-id="4046d-118">In an unidirectional connection, this SAP is the one that is transmitting.</span></span>

</dd> <dt>

<span data-ttu-id="4046d-119">**Charge**</span><span class="sxs-lookup"><span data-stu-id="4046d-119">**Dependent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4046d-120">Type de données : **[ **CIM \_ LANEndpoint**](cim-lanendpoint.md)**</span><span class="sxs-lookup"><span data-stu-id="4046d-120">Data type: **[**CIM\_LANEndpoint**](cim-lanendpoint.md)**</span></span>
</dt> <dt>

<span data-ttu-id="4046d-121">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="4046d-121">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="4046d-122">Qualificateurs : [**override**](/windows/desktop/WmiSdk/standard-qualifiers) (« Dependent »)</span><span class="sxs-lookup"><span data-stu-id="4046d-122">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Dependent")</span></span>
</dt> </dl>

<span data-ttu-id="4046d-123">Référence à une instance de la classe [**MSVM \_ LANEndpoint**](cim-lanendpoint.md) qui représente le SAP configuré pour communiquer ou qui communique activement avec l’antécédent SAP.</span><span class="sxs-lookup"><span data-stu-id="4046d-123">A reference to an instance of the [**Msvm\_LANEndpoint**](cim-lanendpoint.md) class that represents the SAP that is configured to communicate or is actively communicating with the antecedent SAP.</span></span> <span data-ttu-id="4046d-124">Dans une connexion unidirectionnelle, ce SAP est celui qui reçoit.</span><span class="sxs-lookup"><span data-stu-id="4046d-124">In an unidirectional connection, this SAP is the one that is receiving.</span></span>

</dd> <dt>

<span data-ttu-id="4046d-125">**IsUnidirectional**</span><span class="sxs-lookup"><span data-stu-id="4046d-125">**IsUnidirectional**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4046d-126">Type de données : **booléen**</span><span class="sxs-lookup"><span data-stu-id="4046d-126">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="4046d-127">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="4046d-127">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="4046d-128">Si cette propriété a la **valeur true**, cette connexion est unidirectionnelle ; dans le cas contraire, cette connexion est bidirectionnelle.</span><span class="sxs-lookup"><span data-stu-id="4046d-128">If this property is **True**, this connection is unidirectional; otherwise, this connection is bidirectional.</span></span> <span data-ttu-id="4046d-129">Lorsqu’une connexion est unidirectionnelle, la « Speaker » doit être définie comme référence **Antecedent** .</span><span class="sxs-lookup"><span data-stu-id="4046d-129">When a connection is unidirectional, the "speaker" should be defined as the **Antecedent** reference.</span></span> <span data-ttu-id="4046d-130">Dans une connexion bidirectionnelle, il n’est pas important de savoir si le point d’accès sélectionné est l' **antécédent** ou le **dépendant**.</span><span class="sxs-lookup"><span data-stu-id="4046d-130">In a bidirectional connection, it does not matter whether the selected access point is the **Antecedent** or **Dependent**.</span></span> <span data-ttu-id="4046d-131">Cette propriété est héritée de [**CIM \_ ActiveConnection**](/previous-versions//cc136779(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="4046d-131">This property is inherited from [**CIM\_ActiveConnection**](/previous-versions//cc136779(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="4046d-132">**OtherTrafficDescription**</span><span class="sxs-lookup"><span data-stu-id="4046d-132">**OtherTrafficDescription**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4046d-133">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="4046d-133">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="4046d-134">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="4046d-134">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="4046d-135">Cette propriété est héritée de [**CIM \_ ActiveConnection**](/previous-versions//cc136779(v=vs.85)), mais elle n’est pas utilisée.</span><span class="sxs-lookup"><span data-stu-id="4046d-135">This property is inherited from [**CIM\_ActiveConnection**](/previous-versions//cc136779(v=vs.85)), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="4046d-136">**TrafficType**</span><span class="sxs-lookup"><span data-stu-id="4046d-136">**TrafficType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4046d-137">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="4046d-137">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="4046d-138">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="4046d-138">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="4046d-139">Cette propriété est héritée de [**CIM \_ ActiveConnection**](/previous-versions//cc136779(v=vs.85)), mais elle n’est pas utilisée.</span><span class="sxs-lookup"><span data-stu-id="4046d-139">This property is inherited from [**CIM\_ActiveConnection**](/previous-versions//cc136779(v=vs.85)), but it is not used.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="4046d-140">Notes</span><span class="sxs-lookup"><span data-stu-id="4046d-140">Remarks</span></span>

<span data-ttu-id="4046d-141">L’accès à la classe **MSVM \_ ActiveConnection** peut être limité par le filtrage UAC.</span><span class="sxs-lookup"><span data-stu-id="4046d-141">Access to the **Msvm\_ActiveConnection** class might be restricted by UAC Filtering.</span></span> <span data-ttu-id="4046d-142">Pour plus d’informations, consultez [contrôle de compte d’utilisateur et WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span><span class="sxs-lookup"><span data-stu-id="4046d-142">For more information, see [User Account Control and WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span></span>

## <a name="examples"></a><span data-ttu-id="4046d-143">Exemples</span><span class="sxs-lookup"><span data-stu-id="4046d-143">Examples</span></span>

<span data-ttu-id="4046d-144">Consultez [interrogation d’objets de mise en réseau](querying-networking-objects.md).</span><span class="sxs-lookup"><span data-stu-id="4046d-144">See [Querying networking objects](querying-networking-objects.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="4046d-145">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="4046d-145">Requirements</span></span>



| <span data-ttu-id="4046d-146">Condition requise</span><span class="sxs-lookup"><span data-stu-id="4046d-146">Requirement</span></span> | <span data-ttu-id="4046d-147">Valeur</span><span class="sxs-lookup"><span data-stu-id="4046d-147">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4046d-148">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="4046d-148">Minimum supported client</span></span><br/> | <span data-ttu-id="4046d-149">Applications de \[ Bureau Windows 8 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="4046d-149">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="4046d-150">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="4046d-150">Minimum supported server</span></span><br/> | <span data-ttu-id="4046d-151">Applications de bureau Windows Server 2012 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="4046d-151">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="4046d-152">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="4046d-152">Namespace</span></span><br/>                | <span data-ttu-id="4046d-153">\\Virtualisation racine \\ v2</span><span class="sxs-lookup"><span data-stu-id="4046d-153">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="4046d-154">MOF</span><span class="sxs-lookup"><span data-stu-id="4046d-154">MOF</span></span><br/>                      | <dl> <span data-ttu-id="4046d-155"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="4046d-155"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="4046d-156">DLL</span><span class="sxs-lookup"><span data-stu-id="4046d-156">DLL</span></span><br/>                      | <dl> <span data-ttu-id="4046d-157"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="4046d-157"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="4046d-158">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="4046d-158">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4046d-159">**\_ACTIVECONNECTION CIM**</span><span class="sxs-lookup"><span data-stu-id="4046d-159">**CIM\_ActiveConnection**</span></span>](cim-activeconnection.md)
</dt> <dt>

<span data-ttu-id="4046d-160">[**\_ACTIVECONNECTION CIM**](/previous-versions//cc136779(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="4046d-160">[**CIM\_ActiveConnection**](/previous-versions//cc136779(v=vs.85))</span></span>
</dt> </dl>

 

