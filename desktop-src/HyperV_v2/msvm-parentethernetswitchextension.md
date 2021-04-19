---
description: Représente l’association entre une extension de commutateur Ethernet parente et une extension de commutateur Ethernet enfant.
ms.assetid: a0a60214-d85d-4c64-b720-1c34abc25287
title: Classe Msvm_ParentEthernetSwitchExtension
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_ParentEthernetSwitchExtension
- Msvm_ParentEthernetSwitchExtension.Antecedent
- Msvm_ParentEthernetSwitchExtension.Dependent
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 8e215a01c9de98baa545dbb32b8279db4555f9cf
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106521974"
---
# <a name="msvm_parentethernetswitchextension-class"></a><span data-ttu-id="3150c-103">MSVM \_ ParentEthernetSwitchExtension, classe</span><span class="sxs-lookup"><span data-stu-id="3150c-103">Msvm\_ParentEthernetSwitchExtension class</span></span>

<span data-ttu-id="3150c-104">Représente l’association entre une extension de commutateur Ethernet parente et une extension de commutateur Ethernet enfant.</span><span class="sxs-lookup"><span data-stu-id="3150c-104">Represents the association between a parent Ethernet switch extension and a child Ethernet switch extension.</span></span>

<span data-ttu-id="3150c-105">La syntaxe suivante est simplifiée format MOF (MOF) et comprend toutes les propriétés héritées.</span><span class="sxs-lookup"><span data-stu-id="3150c-105">The following syntax is simplified Managed Object Format (MOF) code, and it includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="3150c-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="3150c-106">Syntax</span></span>

``` syntax
[Association, Aggregation, Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_ParentEthernetSwitchExtension : CIM_Dependency
{
  Msvm_EthernetSwitchExtension REF Antecedent;
  Msvm_EthernetSwitchExtension REF Dependent;
};
```

## <a name="members"></a><span data-ttu-id="3150c-107">Membres</span><span class="sxs-lookup"><span data-stu-id="3150c-107">Members</span></span>

<span data-ttu-id="3150c-108">La classe **MSVM \_ ParentEthernetSwitchExtension** possède les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="3150c-108">The **Msvm\_ParentEthernetSwitchExtension** class has these types of members:</span></span>

-   [<span data-ttu-id="3150c-109">Propriétés</span><span class="sxs-lookup"><span data-stu-id="3150c-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="3150c-110">Propriétés</span><span class="sxs-lookup"><span data-stu-id="3150c-110">Properties</span></span>

<span data-ttu-id="3150c-111">La classe **MSVM \_ ParentEthernetSwitchExtension** possède les propriétés suivantes.</span><span class="sxs-lookup"><span data-stu-id="3150c-111">The **Msvm\_ParentEthernetSwitchExtension** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="3150c-112">**Antécédent**</span><span class="sxs-lookup"><span data-stu-id="3150c-112">**Antecedent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3150c-113">Type de données : **[ **MSVM \_ EthernetSwitchExtension**](msvm-ethernetswitchextension.md)**</span><span class="sxs-lookup"><span data-stu-id="3150c-113">Data type: **[**Msvm\_EthernetSwitchExtension**](msvm-ethernetswitchextension.md)**</span></span>
</dt> <dt>

<span data-ttu-id="3150c-114">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="3150c-114">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="3150c-115">Qualificateurs : [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Antecedent")</span><span class="sxs-lookup"><span data-stu-id="3150c-115">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Antecedent")</span></span>
</dt> </dl>

<span data-ttu-id="3150c-116">Référence à une instance de la classe [**MSVM \_ EthernetSwitchExtension**](msvm-ethernetswitchextension.md) qui représente l’extension de commutateur parent.</span><span class="sxs-lookup"><span data-stu-id="3150c-116">A reference to an instance of the [**Msvm\_EthernetSwitchExtension**](msvm-ethernetswitchextension.md) class that represents the parent switch extension.</span></span>

</dd> <dt>

<span data-ttu-id="3150c-117">**Charge**</span><span class="sxs-lookup"><span data-stu-id="3150c-117">**Dependent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3150c-118">Type de données : **[ **MSVM \_ EthernetSwitchExtension**](msvm-ethernetswitchextension.md)**</span><span class="sxs-lookup"><span data-stu-id="3150c-118">Data type: **[**Msvm\_EthernetSwitchExtension**](msvm-ethernetswitchextension.md)**</span></span>
</dt> <dt>

<span data-ttu-id="3150c-119">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="3150c-119">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="3150c-120">Qualificateurs : [**override**](/windows/desktop/WmiSdk/standard-qualifiers) (« Dependent »)</span><span class="sxs-lookup"><span data-stu-id="3150c-120">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Dependent")</span></span>
</dt> </dl>

<span data-ttu-id="3150c-121">Référence à une instance de la classe [**MSVM \_ EthernetSwitchExtension**](msvm-ethernetswitchextension.md) qui représente l’extension de commutateur enfant.</span><span class="sxs-lookup"><span data-stu-id="3150c-121">A reference to an instance of the [**Msvm\_EthernetSwitchExtension**](msvm-ethernetswitchextension.md) class that represents the child switch extension.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="3150c-122">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="3150c-122">Requirements</span></span>



| <span data-ttu-id="3150c-123">Condition requise</span><span class="sxs-lookup"><span data-stu-id="3150c-123">Requirement</span></span> | <span data-ttu-id="3150c-124">Valeur</span><span class="sxs-lookup"><span data-stu-id="3150c-124">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3150c-125">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="3150c-125">Minimum supported client</span></span><br/> | <span data-ttu-id="3150c-126">Applications de \[ Bureau Windows 8 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="3150c-126">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="3150c-127">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="3150c-127">Minimum supported server</span></span><br/> | <span data-ttu-id="3150c-128">Applications de bureau Windows Server 2012 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="3150c-128">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="3150c-129">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="3150c-129">Namespace</span></span><br/>                | <span data-ttu-id="3150c-130">\\Virtualisation racine \\ v2</span><span class="sxs-lookup"><span data-stu-id="3150c-130">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="3150c-131">MOF</span><span class="sxs-lookup"><span data-stu-id="3150c-131">MOF</span></span><br/>                      | <dl> <span data-ttu-id="3150c-132"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="3150c-132"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="3150c-133">DLL</span><span class="sxs-lookup"><span data-stu-id="3150c-133">DLL</span></span><br/>                      | <dl> <span data-ttu-id="3150c-134"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="3150c-134"><dt>Vmms.exe</dt></span></span> </dl>                     |



 

