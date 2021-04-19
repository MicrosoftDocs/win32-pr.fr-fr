---
description: Associe un ordinateur virtuel à une connexion de terminal.
ms.assetid: 31979FB8-3870-44D9-9720-AD99237C5268
title: Classe Msvm_SystemTerminalConnection
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_SystemTerminalConnection
- Msvm_SystemTerminalConnection.Antecedent
- Msvm_SystemTerminalConnection.Dependent
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 368c25b8505ec7ddd29da3b95d95fc842602119e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106544214"
---
# <a name="msvm_systemterminalconnection-class"></a><span data-ttu-id="ebf84-103">MSVM \_ SystemTerminalConnection, classe</span><span class="sxs-lookup"><span data-stu-id="ebf84-103">Msvm\_SystemTerminalConnection class</span></span>

<span data-ttu-id="ebf84-104">Associe un ordinateur virtuel à une connexion de terminal.</span><span class="sxs-lookup"><span data-stu-id="ebf84-104">Associates a virtual machine with a terminal connection.</span></span>

<span data-ttu-id="ebf84-105">La syntaxe suivante est simplifiée format MOF (MOF) et comprend toutes les propriétés héritées.</span><span class="sxs-lookup"><span data-stu-id="ebf84-105">The following syntax is simplified Managed Object Format (MOF) code, and it includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="ebf84-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="ebf84-106">Syntax</span></span>

``` syntax
[Association, Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_SystemTerminalConnection : CIM_HostedDependency
{
  Msvm_ComputerSystem     REF Antecedent;
  Msvm_TerminalConnection REF Dependent;
};
```

## <a name="members"></a><span data-ttu-id="ebf84-107">Membres</span><span class="sxs-lookup"><span data-stu-id="ebf84-107">Members</span></span>

<span data-ttu-id="ebf84-108">La classe **MSVM \_ SystemTerminalConnection** possède les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="ebf84-108">The **Msvm\_SystemTerminalConnection** class has these types of members:</span></span>

-   [<span data-ttu-id="ebf84-109">Propriétés</span><span class="sxs-lookup"><span data-stu-id="ebf84-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="ebf84-110">Propriétés</span><span class="sxs-lookup"><span data-stu-id="ebf84-110">Properties</span></span>

<span data-ttu-id="ebf84-111">La classe **MSVM \_ SystemTerminalConnection** possède les propriétés suivantes.</span><span class="sxs-lookup"><span data-stu-id="ebf84-111">The **Msvm\_SystemTerminalConnection** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="ebf84-112">**Antécédent**</span><span class="sxs-lookup"><span data-stu-id="ebf84-112">**Antecedent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ebf84-113">Type de données : **[ **MSVM \_ ComputerSystem**](msvm-computersystem.md)**</span><span class="sxs-lookup"><span data-stu-id="ebf84-113">Data type: **[**Msvm\_ComputerSystem**](msvm-computersystem.md)**</span></span>
</dt> <dt>

<span data-ttu-id="ebf84-114">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="ebf84-114">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ebf84-115">Qualificateurs : [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Antecedent"), [**Max**](/windows/desktop/WmiSdk/standard-qualifiers) (1)</span><span class="sxs-lookup"><span data-stu-id="ebf84-115">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Antecedent"), [**Max**](/windows/desktop/WmiSdk/standard-qualifiers) (1)</span></span>
</dt> </dl>

<span data-ttu-id="ebf84-116">Ordinateur virtuel auquel la connexion est attachée.</span><span class="sxs-lookup"><span data-stu-id="ebf84-116">The virtual machine to which the connection is attached.</span></span>

</dd> <dt>

<span data-ttu-id="ebf84-117">**Charge**</span><span class="sxs-lookup"><span data-stu-id="ebf84-117">**Dependent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ebf84-118">Type de données : **[ **MSVM \_ TerminalConnection**](msvm-terminalconnection.md)**</span><span class="sxs-lookup"><span data-stu-id="ebf84-118">Data type: **[**Msvm\_TerminalConnection**](msvm-terminalconnection.md)**</span></span>
</dt> <dt>

<span data-ttu-id="ebf84-119">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="ebf84-119">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ebf84-120">Qualificateurs : [**override**](/windows/desktop/WmiSdk/standard-qualifiers) (« Dependent »)</span><span class="sxs-lookup"><span data-stu-id="ebf84-120">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Dependent")</span></span>
</dt> </dl>

<span data-ttu-id="ebf84-121">Connexion à la machine virtuelle.</span><span class="sxs-lookup"><span data-stu-id="ebf84-121">The connection to the virtual machine.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="ebf84-122">Notes</span><span class="sxs-lookup"><span data-stu-id="ebf84-122">Remarks</span></span>

<span data-ttu-id="ebf84-123">L’accès à la classe **MSVM \_ SystemTerminalConnection** peut être limité par le filtrage UAC.</span><span class="sxs-lookup"><span data-stu-id="ebf84-123">Access to the **Msvm\_SystemTerminalConnection** class might be restricted by UAC Filtering.</span></span> <span data-ttu-id="ebf84-124">Pour plus d’informations, consultez [contrôle de compte d’utilisateur et WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span><span class="sxs-lookup"><span data-stu-id="ebf84-124">For more information, see [User Account Control and WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span></span>

## <a name="requirements"></a><span data-ttu-id="ebf84-125">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="ebf84-125">Requirements</span></span>



| <span data-ttu-id="ebf84-126">Condition requise</span><span class="sxs-lookup"><span data-stu-id="ebf84-126">Requirement</span></span> | <span data-ttu-id="ebf84-127">Valeur</span><span class="sxs-lookup"><span data-stu-id="ebf84-127">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ebf84-128">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="ebf84-128">Minimum supported client</span></span><br/> | <span data-ttu-id="ebf84-129">Applications de \[ Bureau Windows 8 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="ebf84-129">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="ebf84-130">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="ebf84-130">Minimum supported server</span></span><br/> | <span data-ttu-id="ebf84-131">Applications de bureau Windows Server 2012 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="ebf84-131">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="ebf84-132">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="ebf84-132">Namespace</span></span><br/>                | <span data-ttu-id="ebf84-133">\\Virtualisation racine \\ v2</span><span class="sxs-lookup"><span data-stu-id="ebf84-133">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="ebf84-134">MOF</span><span class="sxs-lookup"><span data-stu-id="ebf84-134">MOF</span></span><br/>                      | <dl> <span data-ttu-id="ebf84-135"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="ebf84-135"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="ebf84-136">DLL</span><span class="sxs-lookup"><span data-stu-id="ebf84-136">DLL</span></span><br/>                      | <dl> <span data-ttu-id="ebf84-137"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="ebf84-137"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="ebf84-138">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="ebf84-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ebf84-139">**\_HOSTEDDEPENDENCY CIM**</span><span class="sxs-lookup"><span data-stu-id="ebf84-139">**CIM\_HostedDependency**</span></span>](cim-hosteddependency.md)
</dt> <dt>

<span data-ttu-id="ebf84-140">[**\_HOSTEDDEPENDENCY CIM**](/previous-versions//cc136861(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="ebf84-140">[**CIM\_HostedDependency**](/previous-versions//cc136861(v=vs.85))</span></span>
</dt> <dt>

[<span data-ttu-id="ebf84-141">Classes vidéo</span><span class="sxs-lookup"><span data-stu-id="ebf84-141">Video Classes</span></span>](video-classes.md)
</dt> </dl>

 

