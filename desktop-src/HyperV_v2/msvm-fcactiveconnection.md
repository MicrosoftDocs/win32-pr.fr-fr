---
description: Connecte un port de commutateur au point de terminaison Fibre Channel auquel le port est connecté.
ms.assetid: e2762e0c-2f78-4159-a67c-31213e311072
title: Classe Msvm_FcActiveConnection
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_FcActiveConnection
- Msvm_FcActiveConnection.Antecedent
- Msvm_FcActiveConnection.Dependent
- Msvm_FcActiveConnection.TrafficType
- Msvm_FcActiveConnection.OtherTrafficDescription
- Msvm_FcActiveConnection.IsUnidirectional
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 7e29330e073266f2f2a8749ec3c70d9e26b35ff7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106516901"
---
# <a name="msvm_fcactiveconnection-class"></a><span data-ttu-id="0372a-103">MSVM \_ FcActiveConnection, classe</span><span class="sxs-lookup"><span data-stu-id="0372a-103">Msvm\_FcActiveConnection class</span></span>

<span data-ttu-id="0372a-104">Connecte un port de commutateur au point de terminaison Fibre Channel auquel le port est connecté.</span><span class="sxs-lookup"><span data-stu-id="0372a-104">Connects a switch port to the Fibre Channel endpoint to which the port is connected.</span></span> <span data-ttu-id="0372a-105">L’existence de cet objet signifie que le port de commutateur et le point de terminaison Fibre Channel sont connectés activement, et que le port Fibre Channel associé au point de terminaison Fibre Channel peut communiquer avec le réseau via le port commuté.</span><span class="sxs-lookup"><span data-stu-id="0372a-105">The existence of this object means that the switch port and the Fibre Channel endpoint are actively connected, and the Fibre Channel port associated with the Fibre Channel endpoint can communicate with the network through the switch port.</span></span>

<span data-ttu-id="0372a-106">La syntaxe suivante est simplifiée format MOF (MOF) et comprend toutes les propriétés héritées.</span><span class="sxs-lookup"><span data-stu-id="0372a-106">The following syntax is simplified Managed Object Format (MOF) code, and it includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="0372a-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="0372a-107">Syntax</span></span>

``` syntax
[Association, Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_FcActiveConnection : CIM_ActiveConnection
{
  Msvm_FcEndpoint REF Antecedent;
  Msvm_FcEndpoint REF Dependent;
  uint16              TrafficType;
  string              OtherTrafficDescription;
  boolean             IsUnidirectional;
};
```

## <a name="members"></a><span data-ttu-id="0372a-108">Membres</span><span class="sxs-lookup"><span data-stu-id="0372a-108">Members</span></span>

<span data-ttu-id="0372a-109">La classe **MSVM \_ FcActiveConnection** possède les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="0372a-109">The **Msvm\_FcActiveConnection** class has these types of members:</span></span>

-   [<span data-ttu-id="0372a-110">Propriétés</span><span class="sxs-lookup"><span data-stu-id="0372a-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="0372a-111">Propriétés</span><span class="sxs-lookup"><span data-stu-id="0372a-111">Properties</span></span>

<span data-ttu-id="0372a-112">La classe **MSVM \_ FcActiveConnection** possède les propriétés suivantes.</span><span class="sxs-lookup"><span data-stu-id="0372a-112">The **Msvm\_FcActiveConnection** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="0372a-113">**Antécédent**</span><span class="sxs-lookup"><span data-stu-id="0372a-113">**Antecedent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0372a-114">Type de données : **MSVM \_ FcEndpoint**</span><span class="sxs-lookup"><span data-stu-id="0372a-114">Data type: **Msvm\_FcEndpoint**</span></span>
</dt> <dt>

<span data-ttu-id="0372a-115">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="0372a-115">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0372a-116">Qualificateurs : [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Antecedent")</span><span class="sxs-lookup"><span data-stu-id="0372a-116">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Antecedent")</span></span>
</dt> </dl>

<span data-ttu-id="0372a-117">Référence à une instance de la classe [**MSVM \_ FcEndpoint**](msvm-fcendpoint.md) qui représente le point d’accès au service (SAP) qui est configuré pour communiquer ou qui communique activement avec le SAP dépendant.</span><span class="sxs-lookup"><span data-stu-id="0372a-117">A reference to an instance of the [**Msvm\_FcEndpoint**](msvm-fcendpoint.md) class that represents the service access point (SAP) that is configured to communicate or is actively communicating with the dependent SAP.</span></span> <span data-ttu-id="0372a-118">Dans une connexion unidirectionnelle, ce SAP est celui qui transmet.</span><span class="sxs-lookup"><span data-stu-id="0372a-118">In a unidirectional connection, this SAP is the one that is transmitting.</span></span>

</dd> <dt>

<span data-ttu-id="0372a-119">**Charge**</span><span class="sxs-lookup"><span data-stu-id="0372a-119">**Dependent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0372a-120">Type de données : **MSVM \_ FcEndpoint**</span><span class="sxs-lookup"><span data-stu-id="0372a-120">Data type: **Msvm\_FcEndpoint**</span></span>
</dt> <dt>

<span data-ttu-id="0372a-121">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="0372a-121">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0372a-122">Qualificateurs : [**override**](/windows/desktop/WmiSdk/standard-qualifiers) (« Dependent »)</span><span class="sxs-lookup"><span data-stu-id="0372a-122">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Dependent")</span></span>
</dt> </dl>

<span data-ttu-id="0372a-123">Référence à une instance de la classe [**MSVM \_ FcEndpoint**](msvm-fcendpoint.md) qui représente le SAP configuré pour communiquer ou qui communique activement avec l’antécédent SAP.</span><span class="sxs-lookup"><span data-stu-id="0372a-123">A reference to an instance of the [**Msvm\_FcEndpoint**](msvm-fcendpoint.md) class that represents the SAP that is configured to communicate or is actively communicating with the antecedent SAP.</span></span> <span data-ttu-id="0372a-124">Dans une connexion unidirectionnelle, ce SAP est celui qui reçoit.</span><span class="sxs-lookup"><span data-stu-id="0372a-124">In a unidirectional connection, this SAP is the one that is receiving.</span></span>

</dd> <dt>

<span data-ttu-id="0372a-125">**IsUnidirectional**</span><span class="sxs-lookup"><span data-stu-id="0372a-125">**IsUnidirectional**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0372a-126">Type de données : **booléen**</span><span class="sxs-lookup"><span data-stu-id="0372a-126">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="0372a-127">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="0372a-127">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="0372a-128">Si cette propriété a la **valeur true**, cette connexion est unidirectionnelle ; dans le cas contraire, cette connexion est bidirectionnelle.</span><span class="sxs-lookup"><span data-stu-id="0372a-128">If this property is **True**, this connection is unidirectional; otherwise, this connection is bidirectional.</span></span> <span data-ttu-id="0372a-129">Lorsqu’une connexion est unidirectionnelle, la « Speaker » doit être définie comme référence **Antecedent** .</span><span class="sxs-lookup"><span data-stu-id="0372a-129">When a connection is unidirectional, the "speaker" should be defined as the **Antecedent** reference.</span></span> <span data-ttu-id="0372a-130">Dans une connexion bidirectionnelle, il n’est pas important de savoir si le point d’accès sélectionné est l' **antécédent** ou le **dépendant**.</span><span class="sxs-lookup"><span data-stu-id="0372a-130">In a bidirectional connection, it does not matter whether the selected access point is the **Antecedent** or **Dependent**.</span></span> <span data-ttu-id="0372a-131">Cette propriété est héritée de [**CIM \_ ActiveConnection**](/previous-versions//cc136779(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="0372a-131">This property is inherited from [**CIM\_ActiveConnection**](/previous-versions//cc136779(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="0372a-132">**OtherTrafficDescription**</span><span class="sxs-lookup"><span data-stu-id="0372a-132">**OtherTrafficDescription**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0372a-133">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="0372a-133">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0372a-134">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="0372a-134">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="0372a-135">Cette propriété est héritée de [**CIM \_ ActiveConnection**](/previous-versions//cc136779(v=vs.85)), mais elle n’est pas utilisée.</span><span class="sxs-lookup"><span data-stu-id="0372a-135">This property is inherited from [**CIM\_ActiveConnection**](/previous-versions//cc136779(v=vs.85)), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="0372a-136">**TrafficType**</span><span class="sxs-lookup"><span data-stu-id="0372a-136">**TrafficType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0372a-137">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="0372a-137">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="0372a-138">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="0372a-138">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="0372a-139">Cette propriété est héritée de [**CIM \_ ActiveConnection**](/previous-versions//cc136779(v=vs.85)), mais elle n’est pas utilisée.</span><span class="sxs-lookup"><span data-stu-id="0372a-139">This property is inherited from [**CIM\_ActiveConnection**](/previous-versions//cc136779(v=vs.85)), but it is not used.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="0372a-140">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="0372a-140">Requirements</span></span>



| <span data-ttu-id="0372a-141">Condition requise</span><span class="sxs-lookup"><span data-stu-id="0372a-141">Requirement</span></span> | <span data-ttu-id="0372a-142">Valeur</span><span class="sxs-lookup"><span data-stu-id="0372a-142">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0372a-143">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="0372a-143">Minimum supported client</span></span><br/> | <span data-ttu-id="0372a-144">Applications de \[ Bureau Windows 8 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="0372a-144">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="0372a-145">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="0372a-145">Minimum supported server</span></span><br/> | <span data-ttu-id="0372a-146">Applications de bureau Windows Server 2012 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="0372a-146">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="0372a-147">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="0372a-147">Namespace</span></span><br/>                | <span data-ttu-id="0372a-148">\\Virtualisation racine \\ v2</span><span class="sxs-lookup"><span data-stu-id="0372a-148">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="0372a-149">MOF</span><span class="sxs-lookup"><span data-stu-id="0372a-149">MOF</span></span><br/>                      | <dl> <span data-ttu-id="0372a-150"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="0372a-150"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="0372a-151">DLL</span><span class="sxs-lookup"><span data-stu-id="0372a-151">DLL</span></span><br/>                      | <dl> <span data-ttu-id="0372a-152"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="0372a-152"><dt>Vmms.exe</dt></span></span> </dl>                     |



 

