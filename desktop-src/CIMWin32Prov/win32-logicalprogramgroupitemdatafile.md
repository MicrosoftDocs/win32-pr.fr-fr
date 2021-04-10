---
description: La \_ classe WMI d’association LogicalProgramGroupItemDataFile Win32 associe les éléments de groupe de programmes du menu Démarrer et les fichiers dans lesquels elles sont stockées.
ms.assetid: 9327c205-d0ad-4f2b-a65e-2a648e7c13e0
ms.tgt_platform: multiple
title: Classe Win32_LogicalProgramGroupItemDataFile
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_LogicalProgramGroupItemDataFile
- Win32_LogicalProgramGroupItemDataFile.Antecedent
- Win32_LogicalProgramGroupItemDataFile.Dependent
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: beec7074104482e4c6bc91ba7efeaea89104a011
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104111602"
---
# <a name="win32_logicalprogramgroupitemdatafile-class"></a><span data-ttu-id="17413-103">\_Classe LogicalProgramGroupItemDataFile Win32</span><span class="sxs-lookup"><span data-stu-id="17413-103">Win32\_LogicalProgramGroupItemDataFile class</span></span>

<span data-ttu-id="17413-104">La [classe WMI](/windows/desktop/WmiSdk/retrieving-a-class) d’association **\_ LogicalProgramGroupItemDataFile Win32** associe les éléments de groupe de programmes du menu **Démarrer** et les fichiers dans lesquels elles sont stockées.</span><span class="sxs-lookup"><span data-stu-id="17413-104">The **Win32\_LogicalProgramGroupItemDataFile** association [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) relates the program group items of the **Start** menu and the files in which they are stored.</span></span>

<span data-ttu-id="17413-105">La syntaxe suivante est simplifiée par rapport au code MOF (Managed Object Format) et inclut toutes les propriétés héritées.</span><span class="sxs-lookup"><span data-stu-id="17413-105">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span> <span data-ttu-id="17413-106">Les propriétés et les méthodes sont classées par ordre alphabétique, et non par ordre MOF.</span><span class="sxs-lookup"><span data-stu-id="17413-106">Properties and methods are in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="17413-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="17413-107">Syntax</span></span>

``` syntax
[Dynamic, Provider("CIMWin32"), Privileges("SeRestorePrivilege"), UUID("{08FFAD62-8050-11d2-90CE-0060081A46FD}"), AMENDMENT]
class Win32_LogicalProgramGroupItemDataFile : CIM_Dependency
{
  Win32_LogicalProgramGroupItem REF Antecedent;
  CIM_DataFile                  REF Dependent;
};
```

## <a name="members"></a><span data-ttu-id="17413-108">Membres</span><span class="sxs-lookup"><span data-stu-id="17413-108">Members</span></span>

<span data-ttu-id="17413-109">La classe **Win32 \_ LogicalProgramGroupItemDataFile** possède les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="17413-109">The **Win32\_LogicalProgramGroupItemDataFile** class has these types of members:</span></span>

-   [<span data-ttu-id="17413-110">Propriétés</span><span class="sxs-lookup"><span data-stu-id="17413-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="17413-111">Propriétés</span><span class="sxs-lookup"><span data-stu-id="17413-111">Properties</span></span>

<span data-ttu-id="17413-112">La classe **Win32 \_ LogicalProgramGroupItemDataFile** a ces propriétés.</span><span class="sxs-lookup"><span data-stu-id="17413-112">The **Win32\_LogicalProgramGroupItemDataFile** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="17413-113">**Antécédent**</span><span class="sxs-lookup"><span data-stu-id="17413-113">**Antecedent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="17413-114">Type de données : **Win32 \_ LogicalProgramGroupItem**</span><span class="sxs-lookup"><span data-stu-id="17413-114">Data type: **Win32\_LogicalProgramGroupItem**</span></span>
</dt> <dt>

<span data-ttu-id="17413-115">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="17413-115">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="17413-116">Qualificateurs : [**clé**](/windows/desktop/WmiSdk/key-qualifier), [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Antecedent"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("WMI \| Win32 \_ LogicalProgramGroupItem")</span><span class="sxs-lookup"><span data-stu-id="17413-116">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Antecedent"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("WMI\|Win32\_LogicalProgramGroupItem")</span></span>
</dt> </dl>

<span data-ttu-id="17413-117">Référence à l’instance représentant les regroupements de programmes dans le menu **Démarrer** .</span><span class="sxs-lookup"><span data-stu-id="17413-117">Reference to the instance representing the program groupings in the **Start** menu.</span></span>

</dd> <dt>

<span data-ttu-id="17413-118">**Charge**</span><span class="sxs-lookup"><span data-stu-id="17413-118">**Dependent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="17413-119">Type de données **: \_ fichier** de données CIM</span><span class="sxs-lookup"><span data-stu-id="17413-119">Data type: **CIM\_DataFile**</span></span>
</dt> <dt>

<span data-ttu-id="17413-120">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="17413-120">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="17413-121">Qualificateurs : [**clé**](/windows/desktop/WmiSdk/key-qualifier), [**remplacement**](/windows/desktop/WmiSdk/standard-qualifiers) (« dépendant »), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) (« fichier de \| fichier CIM CIM \_ »)</span><span class="sxs-lookup"><span data-stu-id="17413-121">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Dependent"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("CIM\|CIM\_DataFile")</span></span>
</dt> </dl>

<span data-ttu-id="17413-122">Référence à l’instance représentant la classe associée au groupe de programmes.</span><span class="sxs-lookup"><span data-stu-id="17413-122">Reference to the instance representing the class associated with the program group.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="17413-123">Notes</span><span class="sxs-lookup"><span data-stu-id="17413-123">Remarks</span></span>

<span data-ttu-id="17413-124">La classe **Win32 \_ LogicalProgramGroupItemDataFile** est dérivée de la [**\_ dépendance CIM**](cim-dependency.md).</span><span class="sxs-lookup"><span data-stu-id="17413-124">The **Win32\_LogicalProgramGroupItemDataFile** class is derived from [**CIM\_Dependency**](cim-dependency.md).</span></span>

<span data-ttu-id="17413-125">Le processus appelant qui utilise cette classe doit avoir le privilège **se \_ Restore \_ Name** sur l’ordinateur où se trouve le registre.</span><span class="sxs-lookup"><span data-stu-id="17413-125">The calling process that uses this class must have the **SE\_RESTORE\_NAME** privilege on the computer in which the registry resides.</span></span> <span data-ttu-id="17413-126">Par exemple, si vous énumérez cette classe sur l’ordinateur local, le compte sous lequel votre application s’exécute doit disposer de ce privilège.</span><span class="sxs-lookup"><span data-stu-id="17413-126">For example, if you enumerate this class on the local computer, the account under which your application runs must have this privilege.</span></span> <span data-ttu-id="17413-127">Pour plus d’informations, consultez [exécution d’opérations privilégiées](/windows/desktop/WmiSdk/executing-privileged-operations).</span><span class="sxs-lookup"><span data-stu-id="17413-127">For more information, see [Executing Privileged Operations](/windows/desktop/WmiSdk/executing-privileged-operations).</span></span>

## <a name="requirements"></a><span data-ttu-id="17413-128">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="17413-128">Requirements</span></span>



| <span data-ttu-id="17413-129">Condition requise</span><span class="sxs-lookup"><span data-stu-id="17413-129">Requirement</span></span> | <span data-ttu-id="17413-130">Valeur</span><span class="sxs-lookup"><span data-stu-id="17413-130">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="17413-131">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="17413-131">Minimum supported client</span></span><br/> | <span data-ttu-id="17413-132">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="17413-132">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="17413-133">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="17413-133">Minimum supported server</span></span><br/> | <span data-ttu-id="17413-134">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="17413-134">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="17413-135">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="17413-135">Namespace</span></span><br/>                | <span data-ttu-id="17413-136">\\Cimv2 racine</span><span class="sxs-lookup"><span data-stu-id="17413-136">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="17413-137">MOF</span><span class="sxs-lookup"><span data-stu-id="17413-137">MOF</span></span><br/>                      | <dl> <span data-ttu-id="17413-138"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="17413-138"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="17413-139">DLL</span><span class="sxs-lookup"><span data-stu-id="17413-139">DLL</span></span><br/>                      | <dl> <span data-ttu-id="17413-140"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="17413-140"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="17413-141">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="17413-141">See also</span></span>

<dl> <dt>

[<span data-ttu-id="17413-142">**\_Dépendance CIM**</span><span class="sxs-lookup"><span data-stu-id="17413-142">**CIM\_Dependency**</span></span>](cim-dependency.md)
</dt> <dt>

<span data-ttu-id="17413-143">[Classes du système d’exploitation](/previous-versions//aa392727(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="17413-143">[Operating System Classes](/previous-versions//aa392727(v=vs.85))</span></span>
</dt> </dl>

 

