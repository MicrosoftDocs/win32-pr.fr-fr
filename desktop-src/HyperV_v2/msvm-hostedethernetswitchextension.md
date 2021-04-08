---
description: Associe un commutateur Ethernet virtuel aux extensions actuellement liées.
ms.assetid: d8c87fa2-6859-49ed-abd5-32a836b00e5a
title: Classe Msvm_HostedEthernetSwitchExtension
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_HostedEthernetSwitchExtension
- Msvm_HostedEthernetSwitchExtension.Antecedent
- Msvm_HostedEthernetSwitchExtension.Dependent
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: cb952d42864fb6130ad6cbec09ef5eb68439f6a7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103752381"
---
# <a name="msvm_hostedethernetswitchextension-class"></a><span data-ttu-id="37ecf-103">MSVM \_ HostedEthernetSwitchExtension, classe</span><span class="sxs-lookup"><span data-stu-id="37ecf-103">Msvm\_HostedEthernetSwitchExtension class</span></span>

<span data-ttu-id="37ecf-104">Associe un commutateur Ethernet virtuel aux extensions actuellement liées.</span><span class="sxs-lookup"><span data-stu-id="37ecf-104">Associates a virtual Ethernet switch to the extensions currently bound to it.</span></span>

<span data-ttu-id="37ecf-105">La syntaxe suivante est simplifiée format MOF (MOF) et comprend toutes les propriétés héritées.</span><span class="sxs-lookup"><span data-stu-id="37ecf-105">The following syntax is simplified Managed Object Format (MOF) code, and it includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="37ecf-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="37ecf-106">Syntax</span></span>

``` syntax
[Association, Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_HostedEthernetSwitchExtension : CIM_HostedDependency
{
  Msvm_VirtualEthernetSwitch   REF Antecedent;
  Msvm_EthernetSwitchExtension REF Dependent;
};
```

## <a name="members"></a><span data-ttu-id="37ecf-107">Membres</span><span class="sxs-lookup"><span data-stu-id="37ecf-107">Members</span></span>

<span data-ttu-id="37ecf-108">La classe **MSVM \_ HostedEthernetSwitchExtension** possède les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="37ecf-108">The **Msvm\_HostedEthernetSwitchExtension** class has these types of members:</span></span>

-   [<span data-ttu-id="37ecf-109">Propriétés</span><span class="sxs-lookup"><span data-stu-id="37ecf-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="37ecf-110">Propriétés</span><span class="sxs-lookup"><span data-stu-id="37ecf-110">Properties</span></span>

<span data-ttu-id="37ecf-111">La classe **MSVM \_ HostedEthernetSwitchExtension** possède les propriétés suivantes.</span><span class="sxs-lookup"><span data-stu-id="37ecf-111">The **Msvm\_HostedEthernetSwitchExtension** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="37ecf-112">**Antécédent**</span><span class="sxs-lookup"><span data-stu-id="37ecf-112">**Antecedent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="37ecf-113">Type de données : **[ **MSVM \_ VirtualEthernetSwitch**](msvm-virtualethernetswitch.md)**</span><span class="sxs-lookup"><span data-stu-id="37ecf-113">Data type: **[**Msvm\_VirtualEthernetSwitch**](msvm-virtualethernetswitch.md)**</span></span>
</dt> <dt>

<span data-ttu-id="37ecf-114">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="37ecf-114">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="37ecf-115">Qualificateurs : [**clé**](/windows/desktop/WmiSdk/key-qualifier), [**remplacement**](/windows/desktop/WmiSdk/standard-qualifiers) (« Antecedent »), [**min**](/windows/desktop/WmiSdk/standard-qualifiers) (1), [**Max**](/windows/desktop/WmiSdk/standard-qualifiers) (1)</span><span class="sxs-lookup"><span data-stu-id="37ecf-115">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Antecedent"), [**Min**](/windows/desktop/WmiSdk/standard-qualifiers) (1), [**Max**](/windows/desktop/WmiSdk/standard-qualifiers) (1)</span></span>
</dt> </dl>

<span data-ttu-id="37ecf-116">Référence à une instance de la classe [**MSVM \_ VirtualEthernetSwitch**](msvm-virtualethernetswitch.md) qui représente le commutateur virtuel.</span><span class="sxs-lookup"><span data-stu-id="37ecf-116">A reference to an instance of the [**Msvm\_VirtualEthernetSwitch**](msvm-virtualethernetswitch.md) class that represents the virtual switch.</span></span>

</dd> <dt>

<span data-ttu-id="37ecf-117">**Charge**</span><span class="sxs-lookup"><span data-stu-id="37ecf-117">**Dependent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="37ecf-118">Type de données : **[ **MSVM \_ EthernetSwitchExtension**](msvm-ethernetswitchextension.md)**</span><span class="sxs-lookup"><span data-stu-id="37ecf-118">Data type: **[**Msvm\_EthernetSwitchExtension**](msvm-ethernetswitchextension.md)**</span></span>
</dt> <dt>

<span data-ttu-id="37ecf-119">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="37ecf-119">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="37ecf-120">Qualificateurs : [**clé**](/windows/desktop/WmiSdk/key-qualifier), [**remplacement**](/windows/desktop/WmiSdk/standard-qualifiers) (« dépendant »), [**faible**](/windows/desktop/WmiSdk/standard-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="37ecf-120">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Dependent"), [**Weak**](/windows/desktop/WmiSdk/standard-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="37ecf-121">Référence à une instance de la classe [**MSVM \_ EthernetSwitchExtension**](msvm-ethernetswitchextension.md) qui représente l’instance d’extension de commutateur liée au commutateur virtuel.</span><span class="sxs-lookup"><span data-stu-id="37ecf-121">A reference to an instance of the [**Msvm\_EthernetSwitchExtension**](msvm-ethernetswitchextension.md) class that represents the switch extension instance bound to the virtual switch.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="37ecf-122">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="37ecf-122">Requirements</span></span>



| <span data-ttu-id="37ecf-123">Condition requise</span><span class="sxs-lookup"><span data-stu-id="37ecf-123">Requirement</span></span> | <span data-ttu-id="37ecf-124">Valeur</span><span class="sxs-lookup"><span data-stu-id="37ecf-124">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="37ecf-125">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="37ecf-125">Minimum supported client</span></span><br/> | <span data-ttu-id="37ecf-126">Applications de \[ Bureau Windows 8 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="37ecf-126">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="37ecf-127">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="37ecf-127">Minimum supported server</span></span><br/> | <span data-ttu-id="37ecf-128">Applications de bureau Windows Server 2012 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="37ecf-128">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="37ecf-129">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="37ecf-129">Namespace</span></span><br/>                | <span data-ttu-id="37ecf-130">\\Virtualisation racine \\ v2</span><span class="sxs-lookup"><span data-stu-id="37ecf-130">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="37ecf-131">MOF</span><span class="sxs-lookup"><span data-stu-id="37ecf-131">MOF</span></span><br/>                      | <dl> <span data-ttu-id="37ecf-132"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="37ecf-132"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="37ecf-133">DLL</span><span class="sxs-lookup"><span data-stu-id="37ecf-133">DLL</span></span><br/>                      | <dl> <span data-ttu-id="37ecf-134"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="37ecf-134"><dt>Vmms.exe</dt></span></span> </dl>                     |



 

