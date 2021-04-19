---
description: Association entre une instance de la classe MSVM \_ EthernetSwitchPort et une instance de la classe MSVM \_ EthernetPortData qui représente les données collectées sur le port par une extension de commutateur.
ms.assetid: 08677914-af09-47b7-9d4d-406696e1f504
title: Classe Msvm_EthernetPortInfo
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_EthernetPortInfo
- Msvm_EthernetPortInfo.Antecedent
- Msvm_EthernetPortInfo.Dependent
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 7c78dca7adedcf52d93530efdab0da6113855c6d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106518503"
---
# <a name="msvm_ethernetportinfo-class"></a><span data-ttu-id="d7b7b-103">MSVM \_ EthernetPortInfo, classe</span><span class="sxs-lookup"><span data-stu-id="d7b7b-103">Msvm\_EthernetPortInfo class</span></span>

<span data-ttu-id="d7b7b-104">Association entre une instance de la classe [**MSVM \_ EthernetSwitchPort**](msvm-ethernetswitchport.md) et une instance de la classe [**MSVM \_ EthernetPortData**](msvm-ethernetportdata.md) qui représente les données collectées sur le port par une extension de commutateur.</span><span class="sxs-lookup"><span data-stu-id="d7b7b-104">An association between an instance of the [**Msvm\_EthernetSwitchPort**](msvm-ethernetswitchport.md) class and an instance of the [**Msvm\_EthernetPortData**](msvm-ethernetportdata.md) class that represents data gathered about the port by a switch extension.</span></span>

<span data-ttu-id="d7b7b-105">La syntaxe suivante est simplifiée format MOF (MOF) et comprend toutes les propriétés héritées.</span><span class="sxs-lookup"><span data-stu-id="d7b7b-105">The following syntax is simplified Managed Object Format (MOF) code, and it includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="d7b7b-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="d7b7b-106">Syntax</span></span>

``` syntax
[Association, Aggregation, Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_EthernetPortInfo : CIM_Dependency
{
  Msvm_EthernetSwitchPort REF Antecedent;
  Msvm_EthernetPortData   REF Dependent;
};
```

## <a name="members"></a><span data-ttu-id="d7b7b-107">Membres</span><span class="sxs-lookup"><span data-stu-id="d7b7b-107">Members</span></span>

<span data-ttu-id="d7b7b-108">La classe **MSVM \_ EthernetPortInfo** possède les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="d7b7b-108">The **Msvm\_EthernetPortInfo** class has these types of members:</span></span>

-   [<span data-ttu-id="d7b7b-109">Propriétés</span><span class="sxs-lookup"><span data-stu-id="d7b7b-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="d7b7b-110">Propriétés</span><span class="sxs-lookup"><span data-stu-id="d7b7b-110">Properties</span></span>

<span data-ttu-id="d7b7b-111">La classe **MSVM \_ EthernetPortInfo** possède les propriétés suivantes.</span><span class="sxs-lookup"><span data-stu-id="d7b7b-111">The **Msvm\_EthernetPortInfo** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="d7b7b-112">**Antécédent**</span><span class="sxs-lookup"><span data-stu-id="d7b7b-112">**Antecedent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d7b7b-113">Type de données : **MSVM \_ EthernetSwitchPort**</span><span class="sxs-lookup"><span data-stu-id="d7b7b-113">Data type: **Msvm\_EthernetSwitchPort**</span></span>
</dt> <dt>

<span data-ttu-id="d7b7b-114">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="d7b7b-114">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d7b7b-115">Qualificateurs : [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("CIM \_ dependency. Antecedent")</span><span class="sxs-lookup"><span data-stu-id="d7b7b-115">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("CIM\_Dependency.Antecedent")</span></span>
</dt> </dl>

<span data-ttu-id="d7b7b-116">Instance de la classe [**MSVM \_ EthernetSwitchPort**](msvm-ethernetswitchport.md) qui représente le port commuté.</span><span class="sxs-lookup"><span data-stu-id="d7b7b-116">An instance of the [**Msvm\_EthernetSwitchPort**](msvm-ethernetswitchport.md) class that represents the switch port.</span></span>

</dd> <dt>

<span data-ttu-id="d7b7b-117">**Charge**</span><span class="sxs-lookup"><span data-stu-id="d7b7b-117">**Dependent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d7b7b-118">Type de données : **MSVM \_ EthernetPortData**</span><span class="sxs-lookup"><span data-stu-id="d7b7b-118">Data type: **Msvm\_EthernetPortData**</span></span>
</dt> <dt>

<span data-ttu-id="d7b7b-119">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="d7b7b-119">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d7b7b-120">Qualificateurs : [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("dépendance CIM \_ . dependent")</span><span class="sxs-lookup"><span data-stu-id="d7b7b-120">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("CIM\_Dependency.Dependent")</span></span>
</dt> </dl>

<span data-ttu-id="d7b7b-121">Instance de la classe [**MSVM \_ EthernetPortData**](msvm-ethernetportdata.md) qui représente les données de port.</span><span class="sxs-lookup"><span data-stu-id="d7b7b-121">An instance of the [**Msvm\_EthernetPortData**](msvm-ethernetportdata.md) class that represents the port data.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="d7b7b-122">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="d7b7b-122">Requirements</span></span>



| <span data-ttu-id="d7b7b-123">Condition requise</span><span class="sxs-lookup"><span data-stu-id="d7b7b-123">Requirement</span></span> | <span data-ttu-id="d7b7b-124">Valeur</span><span class="sxs-lookup"><span data-stu-id="d7b7b-124">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d7b7b-125">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="d7b7b-125">Minimum supported client</span></span><br/> | <span data-ttu-id="d7b7b-126">Applications de \[ Bureau Windows 8 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="d7b7b-126">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="d7b7b-127">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="d7b7b-127">Minimum supported server</span></span><br/> | <span data-ttu-id="d7b7b-128">Applications de bureau Windows Server 2012 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="d7b7b-128">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="d7b7b-129">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="d7b7b-129">Namespace</span></span><br/>                | <span data-ttu-id="d7b7b-130">\\Virtualisation racine \\ v2</span><span class="sxs-lookup"><span data-stu-id="d7b7b-130">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="d7b7b-131">MOF</span><span class="sxs-lookup"><span data-stu-id="d7b7b-131">MOF</span></span><br/>                      | <dl> <span data-ttu-id="d7b7b-132"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="d7b7b-132"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="d7b7b-133">DLL</span><span class="sxs-lookup"><span data-stu-id="d7b7b-133">DLL</span></span><br/>                      | <dl> <span data-ttu-id="d7b7b-134"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="d7b7b-134"><dt>Vmms.exe</dt></span></span> </dl>                     |



 

