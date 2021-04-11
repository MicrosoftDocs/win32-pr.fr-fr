---
description: La \_ classe WMI de l’Association SystemNetworkConnections Win32 associe une connexion réseau et le système informatique sur lequel elle réside.
ms.assetid: 7c47f653-74a9-4729-a72c-94930181f8c9
ms.tgt_platform: multiple
title: Classe Win32_SystemNetworkConnections
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_SystemNetworkConnections
- Win32_SystemNetworkConnections.GroupComponent
- Win32_SystemNetworkConnections.PartComponent
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: e90562dd4f98a00cf848fb83a9e3051b387241e4
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104111495"
---
# <a name="win32_systemnetworkconnections-class"></a><span data-ttu-id="3caf3-103">\_Classe SystemNetworkConnections Win32</span><span class="sxs-lookup"><span data-stu-id="3caf3-103">Win32\_SystemNetworkConnections class</span></span>

<span data-ttu-id="3caf3-104">La [classe WMI](../wmisdk/retrieving-a-class.md) de l’Association **\_ SystemNetworkConnections Win32** associe une connexion réseau et le système informatique sur lequel elle réside.</span><span class="sxs-lookup"><span data-stu-id="3caf3-104">The **Win32\_SystemNetworkConnections** association [WMI class](../wmisdk/retrieving-a-class.md) relates a network connection and the computer system on which it resides.</span></span>

<span data-ttu-id="3caf3-105">La syntaxe suivante est simplifiée par rapport au code MOF (Managed Object Format) et inclut toutes les propriétés héritées.</span><span class="sxs-lookup"><span data-stu-id="3caf3-105">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span> <span data-ttu-id="3caf3-106">Les propriétés et les méthodes sont classées par ordre alphabétique, et non par ordre MOF.</span><span class="sxs-lookup"><span data-stu-id="3caf3-106">Properties and methods are in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="3caf3-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="3caf3-107">Syntax</span></span>

``` syntax
[Dynamic, Provider("CIMWin32"), UUID("{8502C4F7-5FBB-11D2-AAC1-006008C78BC7}"), AMENDMENT]
class Win32_SystemNetworkConnections : CIM_SystemComponent
{
  Win32_ComputerSystem    REF GroupComponent;
  Win32_NetworkConnection REF PartComponent;
};
```

## <a name="members"></a><span data-ttu-id="3caf3-108">Membres</span><span class="sxs-lookup"><span data-stu-id="3caf3-108">Members</span></span>

<span data-ttu-id="3caf3-109">La classe **Win32 \_ SystemNetworkConnections** possède les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="3caf3-109">The **Win32\_SystemNetworkConnections** class has these types of members:</span></span>

-   [<span data-ttu-id="3caf3-110">Propriétés</span><span class="sxs-lookup"><span data-stu-id="3caf3-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="3caf3-111">Propriétés</span><span class="sxs-lookup"><span data-stu-id="3caf3-111">Properties</span></span>

<span data-ttu-id="3caf3-112">La classe **Win32 \_ SystemNetworkConnections** a ces propriétés.</span><span class="sxs-lookup"><span data-stu-id="3caf3-112">The **Win32\_SystemNetworkConnections** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="3caf3-113">**GroupComponent**</span><span class="sxs-lookup"><span data-stu-id="3caf3-113">**GroupComponent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3caf3-114">Type de données : **Win32 \_ ComputerSystem**</span><span class="sxs-lookup"><span data-stu-id="3caf3-114">Data type: **Win32\_ComputerSystem**</span></span>
</dt> <dt>

<span data-ttu-id="3caf3-115">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="3caf3-115">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="3caf3-116">Qualificateurs : [**clé**](../wmisdk/key-qualifier.md), [**substitution**](../wmisdk/standard-qualifiers.md) (« GroupComponent »), [**MappingStrings**](../wmisdk/standard-qualifiers.md) (« WMI \| Win32 \_ ComputerSystem »)</span><span class="sxs-lookup"><span data-stu-id="3caf3-116">Qualifiers: [**key**](../wmisdk/key-qualifier.md), [**Override**](../wmisdk/standard-qualifiers.md) ("GroupComponent"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("WMI\|Win32\_ComputerSystem")</span></span>
</dt> </dl>

<span data-ttu-id="3caf3-117">Référence à l’instance de qui représente le système informatique connecté au réseau.</span><span class="sxs-lookup"><span data-stu-id="3caf3-117">Reference to the instance representing the computer system connected to the network.</span></span>

</dd> <dt>

<span data-ttu-id="3caf3-118">**PartComponent**</span><span class="sxs-lookup"><span data-stu-id="3caf3-118">**PartComponent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3caf3-119">Type de données : **Win32 \_ NetworkConnection**</span><span class="sxs-lookup"><span data-stu-id="3caf3-119">Data type: **Win32\_NetworkConnection**</span></span>
</dt> <dt>

<span data-ttu-id="3caf3-120">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="3caf3-120">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="3caf3-121">Qualificateurs : [**clé**](../wmisdk/key-qualifier.md), [**remplacement**](../wmisdk/standard-qualifiers.md) ("PartComponent"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("WMI \| Win32 \_ NetworkConnection")</span><span class="sxs-lookup"><span data-stu-id="3caf3-121">Qualifiers: [**key**](../wmisdk/key-qualifier.md), [**Override**](../wmisdk/standard-qualifiers.md) ("PartComponent"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("WMI\|Win32\_NetworkConnection")</span></span>
</dt> </dl>

<span data-ttu-id="3caf3-122">Référence à l’instance représentant la connexion réseau à ce système informatique.</span><span class="sxs-lookup"><span data-stu-id="3caf3-122">Reference to the instance representing the network connection to this computer system.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="3caf3-123">Notes</span><span class="sxs-lookup"><span data-stu-id="3caf3-123">Remarks</span></span>

<span data-ttu-id="3caf3-124">La classe **Win32 \_ SystemNetworkConnections** est dérivée de [**CIM \_ SystemComponent**](cim-systemcomponent.md).</span><span class="sxs-lookup"><span data-stu-id="3caf3-124">The **Win32\_SystemNetworkConnections** class is derived from [**CIM\_SystemComponent**](cim-systemcomponent.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="3caf3-125">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="3caf3-125">Requirements</span></span>



| <span data-ttu-id="3caf3-126">Condition requise</span><span class="sxs-lookup"><span data-stu-id="3caf3-126">Requirement</span></span> | <span data-ttu-id="3caf3-127">Valeur</span><span class="sxs-lookup"><span data-stu-id="3caf3-127">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="3caf3-128">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="3caf3-128">Minimum supported client</span></span><br/> | <span data-ttu-id="3caf3-129">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="3caf3-129">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="3caf3-130">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="3caf3-130">Minimum supported server</span></span><br/> | <span data-ttu-id="3caf3-131">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="3caf3-131">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="3caf3-132">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="3caf3-132">Namespace</span></span><br/>                | <span data-ttu-id="3caf3-133">\\Cimv2 racine</span><span class="sxs-lookup"><span data-stu-id="3caf3-133">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="3caf3-134">MOF</span><span class="sxs-lookup"><span data-stu-id="3caf3-134">MOF</span></span><br/>                      | <dl> <span data-ttu-id="3caf3-135"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="3caf3-135"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="3caf3-136">DLL</span><span class="sxs-lookup"><span data-stu-id="3caf3-136">DLL</span></span><br/>                      | <dl> <span data-ttu-id="3caf3-137"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="3caf3-137"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3caf3-138">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="3caf3-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3caf3-139">**\_SYSTEMCOMPONENT CIM**</span><span class="sxs-lookup"><span data-stu-id="3caf3-139">**CIM\_SystemComponent**</span></span>](cim-systemcomponent.md)
</dt> <dt>

[<span data-ttu-id="3caf3-140">Classes du système d’exploitation</span><span class="sxs-lookup"><span data-stu-id="3caf3-140">Operating System Classes</span></span>](./operating-system-classes.md)
</dt> </dl>

 

 
