---
description: Cette association établit un point d’accès de service (SAP) comme demandeur de services de protocole à partir d’un point de terminaison de protocole.
ms.assetid: 14edefd8-d59b-4925-8b78-a979fb9a975f
title: Classe Msvm_BindsToLANEndpoint
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_BindsToLANEndpoint
- Msvm_BindsToLANEndpoint.Antecedent
- Msvm_BindsToLANEndpoint.Dependent
- Msvm_BindsToLANEndpoint.FrameType
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: c2fa01c8e9e7df40a2907e6e43a9cb4b507a53d3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103952822"
---
# <a name="msvm_bindstolanendpoint-class"></a><span data-ttu-id="c9dfa-103">MSVM \_ BindsToLANEndpoint, classe</span><span class="sxs-lookup"><span data-stu-id="c9dfa-103">Msvm\_BindsToLANEndpoint class</span></span>

<span data-ttu-id="c9dfa-104">Cette association établit un point d’accès de service (SAP) comme demandeur de services de protocole à partir d’un point de terminaison de protocole.</span><span class="sxs-lookup"><span data-stu-id="c9dfa-104">This association establishes a service access point (SAP) as a requester of protocol services from a protocol endpoint.</span></span> <span data-ttu-id="c9dfa-105">En général, cette association s’exécute entre SAP et les points de terminaison sur un seul système.</span><span class="sxs-lookup"><span data-stu-id="c9dfa-105">Typically, this association runs between SAPs and endpoints on a single system.</span></span> <span data-ttu-id="c9dfa-106">Étant donné qu’un point de terminaison de protocole est un type de SAP, cette liaison peut être utilisée pour établir une superposition de deux protocoles, avec la couche supérieure représentée par le **dépendant** et la couche inférieure représentée par l' **antécédent**.</span><span class="sxs-lookup"><span data-stu-id="c9dfa-106">Because a protocol endpoint is a kind of SAP, this binding can be used to establish a layering of two protocols, with the upper layer represented by the **Dependent** and the lower layer represented by the **Antecedent**.</span></span>

<span data-ttu-id="c9dfa-107">La syntaxe suivante est simplifiée format MOF (MOF) et comprend toutes les propriétés héritées.</span><span class="sxs-lookup"><span data-stu-id="c9dfa-107">The following syntax is simplified Managed Object Format (MOF) code, and it includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="c9dfa-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="c9dfa-108">Syntax</span></span>

``` syntax
[Association, Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_BindsToLANEndpoint : CIM_BindsToLANEndpoint
{
  Msvm_LANEndpoint  REF Antecedent;
  Msvm_VLANEndpoint REF Dependent;
  uint16                FrameType;
};
```

## <a name="members"></a><span data-ttu-id="c9dfa-109">Membres</span><span class="sxs-lookup"><span data-stu-id="c9dfa-109">Members</span></span>

<span data-ttu-id="c9dfa-110">La classe **MSVM \_ BindsToLANEndpoint** possède les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="c9dfa-110">The **Msvm\_BindsToLANEndpoint** class has these types of members:</span></span>

-   [<span data-ttu-id="c9dfa-111">Propriétés</span><span class="sxs-lookup"><span data-stu-id="c9dfa-111">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="c9dfa-112">Propriétés</span><span class="sxs-lookup"><span data-stu-id="c9dfa-112">Properties</span></span>

<span data-ttu-id="c9dfa-113">La classe **MSVM \_ BindsToLANEndpoint** possède les propriétés suivantes.</span><span class="sxs-lookup"><span data-stu-id="c9dfa-113">The **Msvm\_BindsToLANEndpoint** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="c9dfa-114">**Antécédent**</span><span class="sxs-lookup"><span data-stu-id="c9dfa-114">**Antecedent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c9dfa-115">Type de données : **[ **MSVM \_ LANEndpoint**](msvm-lanendpoint.md)**</span><span class="sxs-lookup"><span data-stu-id="c9dfa-115">Data type: **[**Msvm\_LANEndpoint**](msvm-lanendpoint.md)**</span></span>
</dt> <dt>

<span data-ttu-id="c9dfa-116">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="c9dfa-116">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c9dfa-117">Qualificateurs : [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Antecedent")</span><span class="sxs-lookup"><span data-stu-id="c9dfa-117">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Antecedent")</span></span>
</dt> </dl>

<span data-ttu-id="c9dfa-118">Référence à une classe [**MSVM \_ LANEndpoint**](msvm-lanendpoint.md) qui représente le port commuté.</span><span class="sxs-lookup"><span data-stu-id="c9dfa-118">A reference to an [**Msvm\_LANEndpoint**](msvm-lanendpoint.md) class that represents the switch port.</span></span> <span data-ttu-id="c9dfa-119">Cette propriété est héritée de la [**\_ dépendance CIM**](/windows/desktop/CIMWin32Prov/cim-dependency).</span><span class="sxs-lookup"><span data-stu-id="c9dfa-119">This property is inherited from [**CIM\_Dependency**](/windows/desktop/CIMWin32Prov/cim-dependency).</span></span>

</dd> <dt>

<span data-ttu-id="c9dfa-120">**Charge**</span><span class="sxs-lookup"><span data-stu-id="c9dfa-120">**Dependent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c9dfa-121">Type de données : **[ **MSVM \_ VLANEndpoint**](msvm-vlanendpoint.md)**</span><span class="sxs-lookup"><span data-stu-id="c9dfa-121">Data type: **[**Msvm\_VLANEndpoint**](msvm-vlanendpoint.md)**</span></span>
</dt> <dt>

<span data-ttu-id="c9dfa-122">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="c9dfa-122">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c9dfa-123">Qualificateurs : [**override**](/windows/desktop/WmiSdk/standard-qualifiers) (« Dependent »)</span><span class="sxs-lookup"><span data-stu-id="c9dfa-123">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Dependent")</span></span>
</dt> </dl>

<span data-ttu-id="c9dfa-124">Référence au [**\_ VLANEndpoint MSVM**](msvm-vlanendpoint.md) associé au port commuté.</span><span class="sxs-lookup"><span data-stu-id="c9dfa-124">A reference to the [**Msvm\_VLANEndpoint**](msvm-vlanendpoint.md) associated with the switch port.</span></span> <span data-ttu-id="c9dfa-125">Cette propriété est héritée de la [**\_ dépendance CIM**](/windows/desktop/CIMWin32Prov/cim-dependency).</span><span class="sxs-lookup"><span data-stu-id="c9dfa-125">This property is inherited from [**CIM\_Dependency**](/windows/desktop/CIMWin32Prov/cim-dependency).</span></span>

</dd> <dt>

<span data-ttu-id="c9dfa-126">**Frame**</span><span class="sxs-lookup"><span data-stu-id="c9dfa-126">**FrameType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c9dfa-127">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="c9dfa-127">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="c9dfa-128">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="c9dfa-128">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c9dfa-129">Décrit la méthode de tramage pour la couche supérieure SAP ou le point de terminaison lié au point de terminaison LAN.</span><span class="sxs-lookup"><span data-stu-id="c9dfa-129">Describes the framing method for the upper layer SAP or endpoint that is bound to the LAN endpoint.</span></span> <span data-ttu-id="c9dfa-130">Cette propriété est héritée de **CIM \_ BindsToLANEndpoint** et est toujours définie sur **null**.</span><span class="sxs-lookup"><span data-stu-id="c9dfa-130">This property is inherited from **CIM\_BindsToLANEndpoint**, and it is always set to **Null**.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="c9dfa-131">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="c9dfa-131">Requirements</span></span>



| <span data-ttu-id="c9dfa-132">Condition requise</span><span class="sxs-lookup"><span data-stu-id="c9dfa-132">Requirement</span></span> | <span data-ttu-id="c9dfa-133">Valeur</span><span class="sxs-lookup"><span data-stu-id="c9dfa-133">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c9dfa-134">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="c9dfa-134">Minimum supported client</span></span><br/> | <span data-ttu-id="c9dfa-135">Applications de \[ Bureau Windows 8 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="c9dfa-135">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="c9dfa-136">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="c9dfa-136">Minimum supported server</span></span><br/> | <span data-ttu-id="c9dfa-137">Applications de bureau Windows Server 2012 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="c9dfa-137">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="c9dfa-138">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="c9dfa-138">Namespace</span></span><br/>                | <span data-ttu-id="c9dfa-139">\\Virtualisation racine \\ v2</span><span class="sxs-lookup"><span data-stu-id="c9dfa-139">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="c9dfa-140">MOF</span><span class="sxs-lookup"><span data-stu-id="c9dfa-140">MOF</span></span><br/>                      | <dl> <span data-ttu-id="c9dfa-141"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="c9dfa-141"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="c9dfa-142">DLL</span><span class="sxs-lookup"><span data-stu-id="c9dfa-142">DLL</span></span><br/>                      | <dl> <span data-ttu-id="c9dfa-143"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="c9dfa-143"><dt>Vmms.exe</dt></span></span> </dl>                     |



 

