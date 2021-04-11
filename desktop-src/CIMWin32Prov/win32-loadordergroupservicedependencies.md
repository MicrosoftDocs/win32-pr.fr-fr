---
description: La \_ classe WMI de l’Association LoadOrderGroupServiceDependencies Win32 associe un service de base et un groupe d’ordre de chargement dont dépend le service pour démarrer l’exécution.
ms.assetid: 56739b80-9028-4a2e-85ed-973a078860c1
ms.tgt_platform: multiple
title: Classe Win32_LoadOrderGroupServiceDependencies
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_LoadOrderGroupServiceDependencies
- Win32_LoadOrderGroupServiceDependencies.Antecedent
- Win32_LoadOrderGroupServiceDependencies.Dependent
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: b95d1aa01def951802434e787931ce348d04ccb6
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104111366"
---
# <a name="win32_loadordergroupservicedependencies-class"></a><span data-ttu-id="e712a-103">\_Classe LoadOrderGroupServiceDependencies Win32</span><span class="sxs-lookup"><span data-stu-id="e712a-103">Win32\_LoadOrderGroupServiceDependencies class</span></span>

<span data-ttu-id="e712a-104">La [classe WMI](/windows/desktop/WmiSdk/retrieving-a-class) de l’Association **\_ LoadOrderGroupServiceDependencies Win32** associe un service de base et un groupe d’ordre de chargement dont dépend le service pour démarrer l’exécution.</span><span class="sxs-lookup"><span data-stu-id="e712a-104">The **Win32\_LoadOrderGroupServiceDependencies** association [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) relates a base service and a load order group that the service depends on to start running.</span></span>

<span data-ttu-id="e712a-105">La syntaxe suivante est simplifiée par rapport au code MOF (Managed Object Format) et inclut toutes les propriétés héritées.</span><span class="sxs-lookup"><span data-stu-id="e712a-105">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span> <span data-ttu-id="e712a-106">Les propriétés sont répertoriées par ordre alphabétique, et non par ordre MOF.</span><span class="sxs-lookup"><span data-stu-id="e712a-106">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="e712a-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="e712a-107">Syntax</span></span>

``` syntax
[Dynamic, Provider("CIMWin32"), UUID("{8502C4FC-5FBB-11D2-AAC1-006008C78BC7}"), AMENDMENT]
class Win32_LoadOrderGroupServiceDependencies : CIM_Dependency
{
  Win32_LoadOrderGroup REF Antecedent;
  Win32_BaseService    REF Dependent;
};
```

## <a name="members"></a><span data-ttu-id="e712a-108">Membres</span><span class="sxs-lookup"><span data-stu-id="e712a-108">Members</span></span>

<span data-ttu-id="e712a-109">La classe **Win32 \_ LoadOrderGroupServiceDependencies** possède les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="e712a-109">The **Win32\_LoadOrderGroupServiceDependencies** class has these types of members:</span></span>

-   [<span data-ttu-id="e712a-110">Propriétés</span><span class="sxs-lookup"><span data-stu-id="e712a-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="e712a-111">Propriétés</span><span class="sxs-lookup"><span data-stu-id="e712a-111">Properties</span></span>

<span data-ttu-id="e712a-112">La classe **Win32 \_ LoadOrderGroupServiceDependencies** a ces propriétés.</span><span class="sxs-lookup"><span data-stu-id="e712a-112">The **Win32\_LoadOrderGroupServiceDependencies** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="e712a-113">**Antécédent**</span><span class="sxs-lookup"><span data-stu-id="e712a-113">**Antecedent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e712a-114">Type de données : **Win32 \_ LoadOrderGroup**</span><span class="sxs-lookup"><span data-stu-id="e712a-114">Data type: **Win32\_LoadOrderGroup**</span></span>
</dt> <dt>

<span data-ttu-id="e712a-115">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="e712a-115">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e712a-116">Qualificateurs : [**clé**](/windows/desktop/WmiSdk/key-qualifier), [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Antecedent"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("WMI \| Win32 \_ LoadOrderGroup")</span><span class="sxs-lookup"><span data-stu-id="e712a-116">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier), [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Antecedent"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("WMI\|Win32\_LoadOrderGroup")</span></span>
</dt> </dl>

<span data-ttu-id="e712a-117">Référence à l’instance de qui représente les propriétés du groupe d’ordre de chargement qui doit démarrer avant que le service de base dépendant de cette classe puisse démarrer.</span><span class="sxs-lookup"><span data-stu-id="e712a-117">Reference to the instance representing the properties of the load order group that must start before the dependent base service of this class can start.</span></span>

</dd> <dt>

<span data-ttu-id="e712a-118">**Charge**</span><span class="sxs-lookup"><span data-stu-id="e712a-118">**Dependent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e712a-119">Type de données : **Win32 \_ BaseService**</span><span class="sxs-lookup"><span data-stu-id="e712a-119">Data type: **Win32\_BaseService**</span></span>
</dt> <dt>

<span data-ttu-id="e712a-120">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="e712a-120">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e712a-121">Qualificateurs : [**clé**](/windows/desktop/WmiSdk/key-qualifier), [**remplacement**](/windows/desktop/WmiSdk/standard-qualifiers) (« dépendant »), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) (« WMI \| Win32 \_ BaseService »)</span><span class="sxs-lookup"><span data-stu-id="e712a-121">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier), [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Dependent"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("WMI\|Win32\_BaseService")</span></span>
</dt> </dl>

<span data-ttu-id="e712a-122">Référence à l’instance de qui représente les propriétés du service de base qui dépend du groupe d’ordre de chargement pour démarrer l’exécution.</span><span class="sxs-lookup"><span data-stu-id="e712a-122">Reference to the instance representing the properties of the base service that is dependent upon the load order group to start running.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="e712a-123">Notes</span><span class="sxs-lookup"><span data-stu-id="e712a-123">Remarks</span></span>

<span data-ttu-id="e712a-124">La classe **Win32 \_ LoadOrderGroupServiceDependencies** est dérivée de la [**\_ dépendance CIM**](cim-dependency.md).</span><span class="sxs-lookup"><span data-stu-id="e712a-124">The **Win32\_LoadOrderGroupServiceDependencies** class is derived from [**CIM\_Dependency**](cim-dependency.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="e712a-125">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="e712a-125">Requirements</span></span>



| <span data-ttu-id="e712a-126">Condition requise</span><span class="sxs-lookup"><span data-stu-id="e712a-126">Requirement</span></span> | <span data-ttu-id="e712a-127">Valeur</span><span class="sxs-lookup"><span data-stu-id="e712a-127">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="e712a-128">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="e712a-128">Minimum supported client</span></span><br/> | <span data-ttu-id="e712a-129">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="e712a-129">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="e712a-130">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="e712a-130">Minimum supported server</span></span><br/> | <span data-ttu-id="e712a-131">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="e712a-131">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="e712a-132">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="e712a-132">Namespace</span></span><br/>                | <span data-ttu-id="e712a-133">\\Cimv2 racine</span><span class="sxs-lookup"><span data-stu-id="e712a-133">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="e712a-134">MOF</span><span class="sxs-lookup"><span data-stu-id="e712a-134">MOF</span></span><br/>                      | <dl> <span data-ttu-id="e712a-135"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="e712a-135"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="e712a-136">DLL</span><span class="sxs-lookup"><span data-stu-id="e712a-136">DLL</span></span><br/>                      | <dl> <span data-ttu-id="e712a-137"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="e712a-137"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e712a-138">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="e712a-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e712a-139">**\_Dépendance CIM**</span><span class="sxs-lookup"><span data-stu-id="e712a-139">**CIM\_Dependency**</span></span>](cim-dependency.md)
</dt> <dt>

<span data-ttu-id="e712a-140">[Classes du système d’exploitation](/previous-versions//aa392727(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="e712a-140">[Operating System Classes](/previous-versions//aa392727(v=vs.85))</span></span>
</dt> </dl>

 

