---
description: Définit l’association entre une extension de commutateur Ethernet installée et une extension de commutateur Ethernet.
ms.assetid: 306658ed-03a4-49fa-8704-f4b83a4bdd4f
title: Classe Msvm_ConcreteDependency
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_ConcreteDependency
- Msvm_ConcreteDependency.Antecedent
- Msvm_ConcreteDependency.Dependent
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: c74a8431b03389a106cd127933a2c78b842385f8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104202213"
---
# <a name="msvm_concretedependency-class"></a><span data-ttu-id="fa089-103">MSVM \_ ConcreteDependency, classe</span><span class="sxs-lookup"><span data-stu-id="fa089-103">Msvm\_ConcreteDependency class</span></span>

<span data-ttu-id="fa089-104">Définit l’association entre une extension de commutateur Ethernet installée et une extension de commutateur Ethernet.</span><span class="sxs-lookup"><span data-stu-id="fa089-104">Defines the association between an installed Ethernet switch extension and an Ethernet switch extension.</span></span>

<span data-ttu-id="fa089-105">La syntaxe suivante est simplifiée format MOF (MOF) et comprend toutes les propriétés héritées.</span><span class="sxs-lookup"><span data-stu-id="fa089-105">The following syntax is simplified Managed Object Format (MOF) code, and it includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="fa089-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="fa089-106">Syntax</span></span>

``` syntax
[Association, Aggregation, Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_ConcreteDependency : CIM_ConcreteDependency
{
  Msvm_InstalledEthernetSwitchExtension REF Antecedent;
  Msvm_EthernetSwitchExtension          REF Dependent;
};
```

## <a name="members"></a><span data-ttu-id="fa089-107">Membres</span><span class="sxs-lookup"><span data-stu-id="fa089-107">Members</span></span>

<span data-ttu-id="fa089-108">La classe **MSVM \_ ConcreteDependency** possède les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="fa089-108">The **Msvm\_ConcreteDependency** class has these types of members:</span></span>

-   [<span data-ttu-id="fa089-109">Propriétés</span><span class="sxs-lookup"><span data-stu-id="fa089-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="fa089-110">Propriétés</span><span class="sxs-lookup"><span data-stu-id="fa089-110">Properties</span></span>

<span data-ttu-id="fa089-111">La classe **MSVM \_ ConcreteDependency** possède les propriétés suivantes.</span><span class="sxs-lookup"><span data-stu-id="fa089-111">The **Msvm\_ConcreteDependency** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="fa089-112">**Antécédent**</span><span class="sxs-lookup"><span data-stu-id="fa089-112">**Antecedent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fa089-113">Type de données : **[ **MSVM \_ InstalledEthernetSwitchExtension**](msvm-installedethernetswitchextension.md)**</span><span class="sxs-lookup"><span data-stu-id="fa089-113">Data type: **[**Msvm\_InstalledEthernetSwitchExtension**](msvm-installedethernetswitchextension.md)**</span></span>
</dt> <dt>

<span data-ttu-id="fa089-114">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="fa089-114">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="fa089-115">Qualificateurs : [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Antecedent")</span><span class="sxs-lookup"><span data-stu-id="fa089-115">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Antecedent")</span></span>
</dt> </dl>

<span data-ttu-id="fa089-116">Référence à une instance de la classe [**MSVM \_ InstalledEthernetSwitchExtension**](msvm-installedethernetswitchextension.md) qui représente un composant d’extension de commutateur Ethernet virtuel installé sur le système.</span><span class="sxs-lookup"><span data-stu-id="fa089-116">A reference to an instance of the [**Msvm\_InstalledEthernetSwitchExtension**](msvm-installedethernetswitchextension.md) class that represents a virtual Ethernet switch extension component installed on the system.</span></span>

</dd> <dt>

<span data-ttu-id="fa089-117">**Charge**</span><span class="sxs-lookup"><span data-stu-id="fa089-117">**Dependent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fa089-118">Type de données : **[ **MSVM \_ EthernetSwitchExtension**](msvm-ethernetswitchextension.md)**</span><span class="sxs-lookup"><span data-stu-id="fa089-118">Data type: **[**Msvm\_EthernetSwitchExtension**](msvm-ethernetswitchextension.md)**</span></span>
</dt> <dt>

<span data-ttu-id="fa089-119">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="fa089-119">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="fa089-120">Qualificateurs : [**override**](/windows/desktop/WmiSdk/standard-qualifiers) (« Dependent »)</span><span class="sxs-lookup"><span data-stu-id="fa089-120">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Dependent")</span></span>
</dt> </dl>

<span data-ttu-id="fa089-121">Référence à une instance de la classe [**MSVM \_ EthernetSwitchExtension**](msvm-ethernetswitchextension.md) qui représente l’occurrence de l' **antécédent** lié à un commutateur Ethernet virtuel spécifique.</span><span class="sxs-lookup"><span data-stu-id="fa089-121">A reference to an instance of the [**Msvm\_EthernetSwitchExtension**](msvm-ethernetswitchextension.md) class that represents the occurrence of the **Antecedent** bound to a specific virtual Ethernet switch.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="fa089-122">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="fa089-122">Requirements</span></span>



| <span data-ttu-id="fa089-123">Condition requise</span><span class="sxs-lookup"><span data-stu-id="fa089-123">Requirement</span></span> | <span data-ttu-id="fa089-124">Valeur</span><span class="sxs-lookup"><span data-stu-id="fa089-124">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="fa089-125">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="fa089-125">Minimum supported client</span></span><br/> | <span data-ttu-id="fa089-126">Applications de \[ Bureau Windows 8 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="fa089-126">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="fa089-127">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="fa089-127">Minimum supported server</span></span><br/> | <span data-ttu-id="fa089-128">Applications de bureau Windows Server 2012 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="fa089-128">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="fa089-129">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="fa089-129">Namespace</span></span><br/>                | <span data-ttu-id="fa089-130">\\Virtualisation racine \\ v2</span><span class="sxs-lookup"><span data-stu-id="fa089-130">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="fa089-131">MOF</span><span class="sxs-lookup"><span data-stu-id="fa089-131">MOF</span></span><br/>                      | <dl> <span data-ttu-id="fa089-132"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="fa089-132"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="fa089-133">DLL</span><span class="sxs-lookup"><span data-stu-id="fa089-133">DLL</span></span><br/>                      | <dl> <span data-ttu-id="fa089-134"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="fa089-134"><dt>Vmms.exe</dt></span></span> </dl>                     |



 

