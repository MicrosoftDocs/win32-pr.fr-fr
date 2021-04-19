---
description: La \_ classe WMI de l’Association LogicalProgramGroupDirectory Win32 associe les groupes de programmes logiques (regroupements dans le menu Démarrer) et les répertoires de fichiers dans lesquels elles sont stockées.
ms.assetid: 31a8b56a-d4fd-4cc5-9997-ec6211fe9425
ms.tgt_platform: multiple
title: Classe Win32_LogicalProgramGroupDirectory
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_LogicalProgramGroupDirectory
- Win32_LogicalProgramGroupDirectory.Antecedent
- Win32_LogicalProgramGroupDirectory.Dependent
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: d6ebaddd4455ba1b62832f940d78534c90cefeeb
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106515343"
---
# <a name="win32_logicalprogramgroupdirectory-class"></a><span data-ttu-id="9a769-103">\_Classe LogicalProgramGroupDirectory Win32</span><span class="sxs-lookup"><span data-stu-id="9a769-103">Win32\_LogicalProgramGroupDirectory class</span></span>

<span data-ttu-id="9a769-104">La [classe WMI](/windows/desktop/WmiSdk/retrieving-a-class) de l’Association **\_ LogicalProgramGroupDirectory Win32** associe les groupes de programmes logiques (regroupements dans le menu **Démarrer** ) et les répertoires de fichiers dans lesquels elles sont stockées.</span><span class="sxs-lookup"><span data-stu-id="9a769-104">The **Win32\_LogicalProgramGroupDirectory** association [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) relates logical program groups (groupings in the **Start** menu) and the file directories in which they are stored.</span></span>

<span data-ttu-id="9a769-105">La syntaxe suivante est simplifiée par rapport au code MOF (Managed Object Format) et inclut toutes les propriétés héritées.</span><span class="sxs-lookup"><span data-stu-id="9a769-105">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span> <span data-ttu-id="9a769-106">Les propriétés et les méthodes sont classées par ordre alphabétique, et non par ordre MOF.</span><span class="sxs-lookup"><span data-stu-id="9a769-106">Properties and methods are in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="9a769-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="9a769-107">Syntax</span></span>

``` syntax
[Dynamic, Provider("CIMWin32"), Privileges("SeRestorePrivilege"), UUID("{F25FE467-783E-11d2-90BF-0060081A46FD}"), AMENDMENT]
class Win32_LogicalProgramGroupDirectory : CIM_Dependency
{
  Win32_LogicalProgramGroup REF Antecedent;
  Win32_Directory           REF Dependent;
};
```

## <a name="members"></a><span data-ttu-id="9a769-108">Membres</span><span class="sxs-lookup"><span data-stu-id="9a769-108">Members</span></span>

<span data-ttu-id="9a769-109">La classe **Win32 \_ LogicalProgramGroupDirectory** possède les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="9a769-109">The **Win32\_LogicalProgramGroupDirectory** class has these types of members:</span></span>

-   [<span data-ttu-id="9a769-110">Propriétés</span><span class="sxs-lookup"><span data-stu-id="9a769-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="9a769-111">Propriétés</span><span class="sxs-lookup"><span data-stu-id="9a769-111">Properties</span></span>

<span data-ttu-id="9a769-112">La classe **Win32 \_ LogicalProgramGroupDirectory** a ces propriétés.</span><span class="sxs-lookup"><span data-stu-id="9a769-112">The **Win32\_LogicalProgramGroupDirectory** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="9a769-113">**Antécédent**</span><span class="sxs-lookup"><span data-stu-id="9a769-113">**Antecedent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9a769-114">Type de données : **Win32 \_ LogicalProgramGroup**</span><span class="sxs-lookup"><span data-stu-id="9a769-114">Data type: **Win32\_LogicalProgramGroup**</span></span>
</dt> <dt>

<span data-ttu-id="9a769-115">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="9a769-115">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="9a769-116">Qualificateurs : [**clé**](/windows/desktop/WmiSdk/key-qualifier), [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Antecedent"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("WMI \| Win32 \_ LogicalProgramGroup")</span><span class="sxs-lookup"><span data-stu-id="9a769-116">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Antecedent"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("WMI\|Win32\_LogicalProgramGroup")</span></span>
</dt> </dl>

<span data-ttu-id="9a769-117">Référence à l’instance de qui représente le groupe de programmes logique.</span><span class="sxs-lookup"><span data-stu-id="9a769-117">Reference to the instance representing the logical program group.</span></span>

</dd> <dt>

<span data-ttu-id="9a769-118">**Charge**</span><span class="sxs-lookup"><span data-stu-id="9a769-118">**Dependent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9a769-119">Type de données **: \_ répertoire win32**</span><span class="sxs-lookup"><span data-stu-id="9a769-119">Data type: **Win32\_Directory**</span></span>
</dt> <dt>

<span data-ttu-id="9a769-120">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="9a769-120">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="9a769-121">Qualificateurs : [**clé**](/windows/desktop/WmiSdk/key-qualifier), [**remplacement**](/windows/desktop/WmiSdk/standard-qualifiers) (« dépendant »), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) (« \| répertoire win32 Win32 \_ »)</span><span class="sxs-lookup"><span data-stu-id="9a769-121">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Dependent"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("WMI\|Win32\_Directory")</span></span>
</dt> </dl>

<span data-ttu-id="9a769-122">Référence à l’instance représentant le répertoire de fichiers pour le groupe de programmes logique.</span><span class="sxs-lookup"><span data-stu-id="9a769-122">Reference to the instance representing the file directory for the logical program group.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="9a769-123">Notes</span><span class="sxs-lookup"><span data-stu-id="9a769-123">Remarks</span></span>

<span data-ttu-id="9a769-124">La classe **Win32 \_ LogicalProgramGroupDirectory** est dérivée de la [**\_ dépendance CIM**](cim-dependency.md).</span><span class="sxs-lookup"><span data-stu-id="9a769-124">The **Win32\_LogicalProgramGroupDirectory** class is derived from [**CIM\_Dependency**](cim-dependency.md).</span></span>

<span data-ttu-id="9a769-125">Le processus appelant qui utilise cette classe doit avoir le privilège **se \_ Restore \_ Name** sur l’ordinateur où se trouve le registre.</span><span class="sxs-lookup"><span data-stu-id="9a769-125">The calling process that uses this class must have the **SE\_RESTORE\_NAME** privilege on the computer in which the registry resides.</span></span> <span data-ttu-id="9a769-126">Par exemple, si vous énumérez cette classe sur l’ordinateur local, le compte sous lequel votre application s’exécute doit disposer de ce privilège.</span><span class="sxs-lookup"><span data-stu-id="9a769-126">For example, if you enumerate this class on the local computer, the account under which your application runs must have this privilege.</span></span> <span data-ttu-id="9a769-127">Pour plus d’informations, consultez [exécution d’opérations privilégiées](/windows/desktop/WmiSdk/executing-privileged-operations).</span><span class="sxs-lookup"><span data-stu-id="9a769-127">For more information, see [Executing Privileged Operations](/windows/desktop/WmiSdk/executing-privileged-operations).</span></span>

## <a name="requirements"></a><span data-ttu-id="9a769-128">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="9a769-128">Requirements</span></span>



| <span data-ttu-id="9a769-129">Condition requise</span><span class="sxs-lookup"><span data-stu-id="9a769-129">Requirement</span></span> | <span data-ttu-id="9a769-130">Valeur</span><span class="sxs-lookup"><span data-stu-id="9a769-130">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="9a769-131">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="9a769-131">Minimum supported client</span></span><br/> | <span data-ttu-id="9a769-132">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="9a769-132">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="9a769-133">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="9a769-133">Minimum supported server</span></span><br/> | <span data-ttu-id="9a769-134">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="9a769-134">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="9a769-135">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="9a769-135">Namespace</span></span><br/>                | <span data-ttu-id="9a769-136">\\Cimv2 racine</span><span class="sxs-lookup"><span data-stu-id="9a769-136">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="9a769-137">MOF</span><span class="sxs-lookup"><span data-stu-id="9a769-137">MOF</span></span><br/>                      | <dl> <span data-ttu-id="9a769-138"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="9a769-138"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="9a769-139">DLL</span><span class="sxs-lookup"><span data-stu-id="9a769-139">DLL</span></span><br/>                      | <dl> <span data-ttu-id="9a769-140"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="9a769-140"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9a769-141">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="9a769-141">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9a769-142">**\_Dépendance CIM**</span><span class="sxs-lookup"><span data-stu-id="9a769-142">**CIM\_Dependency**</span></span>](cim-dependency.md)
</dt> <dt>

<span data-ttu-id="9a769-143">[Classes du système d’exploitation](/previous-versions//aa392727(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="9a769-143">[Operating System Classes](/previous-versions//aa392727(v=vs.85))</span></span>
</dt> </dl>

 

