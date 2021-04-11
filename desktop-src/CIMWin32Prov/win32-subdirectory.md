---
description: La \_ classe WMI d’association de sous-répertoires Win32 lie un répertoire (dossier) et l’un de ses sous-répertoires (sous-dossiers).
ms.assetid: f0565b7b-d593-468b-96b1-3922428c61e1
ms.tgt_platform: multiple
title: Classe Win32_SubDirectory
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_SubDirectory
- Win32_SubDirectory.GroupComponent
- Win32_SubDirectory.PartComponent
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 046de6ad1e09874351b37d58f7277126e39e990a
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104111199"
---
# <a name="win32_subdirectory-class"></a><span data-ttu-id="59bf2-103">\_Classe de sous-répertoire Win32</span><span class="sxs-lookup"><span data-stu-id="59bf2-103">Win32\_SubDirectory class</span></span>

<span data-ttu-id="59bf2-104">La [classe WMI](../wmisdk/retrieving-a-class.md) d’association de **\_ sous-répertoires Win32** lie un répertoire (dossier) et l’un de ses sous-répertoires (sous-dossiers).</span><span class="sxs-lookup"><span data-stu-id="59bf2-104">The **Win32\_SubDirectory** association [WMI class](../wmisdk/retrieving-a-class.md) relates a directory (folder) and one of its subdirectories (subfolders).</span></span>

<span data-ttu-id="59bf2-105">La syntaxe suivante est simplifiée par rapport au code MOF (Managed Object Format) et inclut toutes les propriétés héritées.</span><span class="sxs-lookup"><span data-stu-id="59bf2-105">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span> <span data-ttu-id="59bf2-106">Les propriétés et les méthodes sont classées par ordre alphabétique, et non par ordre MOF.</span><span class="sxs-lookup"><span data-stu-id="59bf2-106">Properties and methods are in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="59bf2-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="59bf2-107">Syntax</span></span>

``` syntax
[Dynamic, Provider("CIMWin32"), UUID("{F25FE469-783E-11d2-90BF-0060081A46FD}"), AMENDMENT]
class Win32_SubDirectory : CIM_Component
{
  Win32_Directory REF GroupComponent;
  Win32_Directory REF PartComponent;
};
```

## <a name="members"></a><span data-ttu-id="59bf2-108">Membres</span><span class="sxs-lookup"><span data-stu-id="59bf2-108">Members</span></span>

<span data-ttu-id="59bf2-109">La classe de **\_ sous-répertoire win32** possède les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="59bf2-109">The **Win32\_SubDirectory** class has these types of members:</span></span>

-   [<span data-ttu-id="59bf2-110">Propriétés</span><span class="sxs-lookup"><span data-stu-id="59bf2-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="59bf2-111">Propriétés</span><span class="sxs-lookup"><span data-stu-id="59bf2-111">Properties</span></span>

<span data-ttu-id="59bf2-112">La classe de **\_ sous-répertoire win32** possède ces propriétés.</span><span class="sxs-lookup"><span data-stu-id="59bf2-112">The **Win32\_SubDirectory** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="59bf2-113">**GroupComponent**</span><span class="sxs-lookup"><span data-stu-id="59bf2-113">**GroupComponent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="59bf2-114">Type de données **: \_ répertoire win32**</span><span class="sxs-lookup"><span data-stu-id="59bf2-114">Data type: **Win32\_Directory**</span></span>
</dt> <dt>

<span data-ttu-id="59bf2-115">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="59bf2-115">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="59bf2-116">Qualificateurs : [**clé**](../wmisdk/key-qualifier.md), [**remplacement**](../wmisdk/standard-qualifiers.md) ("GroupComponent"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) (" \| répertoire Win32 WMI \_ ")</span><span class="sxs-lookup"><span data-stu-id="59bf2-116">Qualifiers: [**Key**](../wmisdk/key-qualifier.md), [**Override**](../wmisdk/standard-qualifiers.md) ("GroupComponent"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("WMI\|Win32\_Directory")</span></span>
</dt> </dl>

<span data-ttu-id="59bf2-117">Référence à l’instance représentant les propriétés du répertoire parent (dossier) dans cette association.</span><span class="sxs-lookup"><span data-stu-id="59bf2-117">Reference to the instance representing the properties of the parent directory (folder) in this association.</span></span>

</dd> <dt>

<span data-ttu-id="59bf2-118">**PartComponent**</span><span class="sxs-lookup"><span data-stu-id="59bf2-118">**PartComponent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="59bf2-119">Type de données **: \_ répertoire win32**</span><span class="sxs-lookup"><span data-stu-id="59bf2-119">Data type: **Win32\_Directory**</span></span>
</dt> <dt>

<span data-ttu-id="59bf2-120">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="59bf2-120">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="59bf2-121">Qualificateurs : [**clé**](../wmisdk/key-qualifier.md), [**remplacement**](../wmisdk/standard-qualifiers.md) (« PartComponent »), [**MappingStrings**](../wmisdk/standard-qualifiers.md) (« \| répertoire win32 Win32 \_ »)</span><span class="sxs-lookup"><span data-stu-id="59bf2-121">Qualifiers: [**Key**](../wmisdk/key-qualifier.md), [**Override**](../wmisdk/standard-qualifiers.md) ("PartComponent"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("WMI\|Win32\_Directory")</span></span>
</dt> </dl>

<span data-ttu-id="59bf2-122">Référence à l’instance représentant le sous-répertoire (sous-dossier) qui fait partie de l’Association.</span><span class="sxs-lookup"><span data-stu-id="59bf2-122">Reference to the instance representing the subdirectory (subfolder) part of the association.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="59bf2-123">Notes</span><span class="sxs-lookup"><span data-stu-id="59bf2-123">Remarks</span></span>

<span data-ttu-id="59bf2-124">La classe de **\_ sous-répertoire win32** est dérivée du [**\_ composant CIM**](cim-component.md).</span><span class="sxs-lookup"><span data-stu-id="59bf2-124">The **Win32\_SubDirectory** class is derived from [**CIM\_Component**](cim-component.md).</span></span>

<span data-ttu-id="59bf2-125">Pour retourner une collection de sous-dossiers d’un dossier, créez une requête d’association qui définit *ResultRole* sur *PartComponent*.</span><span class="sxs-lookup"><span data-stu-id="59bf2-125">To return a collection of subfolders for a folder, create an association query that sets the *ResultRole* to *PartComponent*.</span></span> <span data-ttu-id="59bf2-126">Cela indique que tous les éléments de la collection retournée doivent jouer le rôle d’un PartComponent, ou sous-dossier, de l’objet Folder.</span><span class="sxs-lookup"><span data-stu-id="59bf2-126">This indicates that all the items in the returned collection must play the role of a PartComponent, or subfolder, of the folder object.</span></span> <span data-ttu-id="59bf2-127">Pour retourner le dossier parent d’un dossier, affectez à *ResultRole* la valeur *GroupComponent*.</span><span class="sxs-lookup"><span data-stu-id="59bf2-127">To return the parent folder for a folder, set the *ResultRole* to *GroupComponent*.</span></span>

<span data-ttu-id="59bf2-128">La classe de **\_ sous-répertoire win32** fonctionne uniquement au niveau du système de fichiers juste au-dessus ou immédiatement au-dessous du dossier spécifié.</span><span class="sxs-lookup"><span data-stu-id="59bf2-128">The **Win32\_SubDirectory** class works only on the file system level immediately above or immediately below the specified folder.</span></span>

## <a name="examples"></a><span data-ttu-id="59bf2-129">Exemples</span><span class="sxs-lookup"><span data-stu-id="59bf2-129">Examples</span></span>

<span data-ttu-id="59bf2-130">L’exemple VBScript suivant retourne une liste de tous les sous-dossiers dans le dossier C : \\ scripts.</span><span class="sxs-lookup"><span data-stu-id="59bf2-130">The following VBScript sample returns a list of all subfolders within the folder C:\\Scripts.</span></span>


```VB
strComputer = "."
Set objWMIService = GetObject("winmgmts:" _
 & "{impersonationLevel=impersonate}!\\" & strComputer & "\root\cimv2")
Set colSubfolders = objWMIService.ExecQuery _
 ("ASSOCIATORS OF {Win32_Directory.Name='c:\scripts'} " _
 & "WHERE AssocClass = Win32_Subdirectory " _
 & "ResultRole = PartComponent")
For Each objFolder in colSubfolders
 Wscript.Echo objFolder.Name
Next
```



## <a name="requirements"></a><span data-ttu-id="59bf2-131">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="59bf2-131">Requirements</span></span>



| <span data-ttu-id="59bf2-132">Condition requise</span><span class="sxs-lookup"><span data-stu-id="59bf2-132">Requirement</span></span> | <span data-ttu-id="59bf2-133">Valeur</span><span class="sxs-lookup"><span data-stu-id="59bf2-133">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="59bf2-134">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="59bf2-134">Minimum supported client</span></span><br/> | <span data-ttu-id="59bf2-135">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="59bf2-135">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="59bf2-136">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="59bf2-136">Minimum supported server</span></span><br/> | <span data-ttu-id="59bf2-137">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="59bf2-137">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="59bf2-138">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="59bf2-138">Namespace</span></span><br/>                | <span data-ttu-id="59bf2-139">\\Cimv2 racine</span><span class="sxs-lookup"><span data-stu-id="59bf2-139">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="59bf2-140">MOF</span><span class="sxs-lookup"><span data-stu-id="59bf2-140">MOF</span></span><br/>                      | <dl> <span data-ttu-id="59bf2-141"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="59bf2-141"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="59bf2-142">DLL</span><span class="sxs-lookup"><span data-stu-id="59bf2-142">DLL</span></span><br/>                      | <dl> <span data-ttu-id="59bf2-143"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="59bf2-143"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="59bf2-144">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="59bf2-144">See also</span></span>

<dl> <dt>

[<span data-ttu-id="59bf2-145">**\_Composant CIM**</span><span class="sxs-lookup"><span data-stu-id="59bf2-145">**CIM\_Component**</span></span>](cim-component.md)
</dt> <dt>

[<span data-ttu-id="59bf2-146">Classes du système d’exploitation</span><span class="sxs-lookup"><span data-stu-id="59bf2-146">Operating System Classes</span></span>](./operating-system-classes.md)
</dt> </dl>

 

 
