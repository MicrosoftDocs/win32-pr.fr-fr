---
description: Méthode TakeOwnerShip de la classe Win32_Directory-la méthode de classe WMI TakeOwnerShip obtient la propriété du fichier logique spécifié dans le chemin d’accès de l’objet.
ms.assetid: 1112823b-0bb6-4dc0-a5c4-8d3839a47a3a
ms.tgt_platform: multiple
title: Méthode TakeOwnerShip de la classe Win32_Directory
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_Directory.TakeOwnerShip
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: 178f1bf523d939883a7fc18b5bdbd7142cc4f824
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108086027"
---
# <a name="takeownership-method-of-the-win32_directory-class"></a><span data-ttu-id="c73ec-103">Méthode TakeOwnerShip de la \_ classe Directory Win32</span><span class="sxs-lookup"><span data-stu-id="c73ec-103">TakeOwnerShip method of the Win32\_Directory class</span></span>

<span data-ttu-id="c73ec-104">La méthode de [classe WMI](/windows/desktop/WmiSdk/retrieving-a-class) **TakeOwnership** obtient la propriété du fichier logique spécifié dans le chemin d’accès de l’objet.</span><span class="sxs-lookup"><span data-stu-id="c73ec-104">The **TakeOwnerShip** [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) method obtains ownership of the logical file specified in the object path.</span></span> <span data-ttu-id="c73ec-105">Si le fichier logique est effectivement un répertoire, **TakeOwnership** agit de manière récursive, en prenant possession de tous les fichiers et sous-répertoires contenus dans le répertoire.</span><span class="sxs-lookup"><span data-stu-id="c73ec-105">If the logical file is actually a directory, then **TakeOwnerShip** acts recursively, taking ownership of all of the files and subdirectories the directory contains.</span></span>

<span data-ttu-id="c73ec-106">Cette rubrique utilise la syntaxe format MOF (MOF).</span><span class="sxs-lookup"><span data-stu-id="c73ec-106">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="c73ec-107">Pour plus d’informations sur l’utilisation de cette méthode, consultez [appel d’une méthode](/windows/desktop/WmiSdk/calling-a-method).</span><span class="sxs-lookup"><span data-stu-id="c73ec-107">For more information about using this method see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="c73ec-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="c73ec-108">Syntax</span></span>


```mof
uint32 TakeOwnerShip();
```



## <a name="parameters"></a><span data-ttu-id="c73ec-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="c73ec-109">Parameters</span></span>

<span data-ttu-id="c73ec-110">Cette méthode n’a aucun paramètre.</span><span class="sxs-lookup"><span data-stu-id="c73ec-110">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="c73ec-111">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="c73ec-111">Return value</span></span>

<span data-ttu-id="c73ec-112">Retourne l’une des valeurs suivantes.</span><span class="sxs-lookup"><span data-stu-id="c73ec-112">Returns one of the following values.</span></span>

<dl> <dt>

<span data-ttu-id="c73ec-113">**0**</span><span class="sxs-lookup"><span data-stu-id="c73ec-113">**0**</span></span>
</dt> <dd>

<span data-ttu-id="c73ec-114">La demande a abouti.</span><span class="sxs-lookup"><span data-stu-id="c73ec-114">The request was successful.</span></span>

</dd> <dt>

<span data-ttu-id="c73ec-115">**2**</span><span class="sxs-lookup"><span data-stu-id="c73ec-115">**2**</span></span>
</dt> <dd>

<span data-ttu-id="c73ec-116">L’accès a été refusé.</span><span class="sxs-lookup"><span data-stu-id="c73ec-116">Access was denied.</span></span>

</dd> <dt>

<span data-ttu-id="c73ec-117">**8**</span><span class="sxs-lookup"><span data-stu-id="c73ec-117">**8**</span></span>
</dt> <dd>

<span data-ttu-id="c73ec-118">Une erreur non spécifiée s’est produite.</span><span class="sxs-lookup"><span data-stu-id="c73ec-118">An unspecified failure occurred.</span></span>

</dd> <dt>

<span data-ttu-id="c73ec-119">**9**</span><span class="sxs-lookup"><span data-stu-id="c73ec-119">**9**</span></span>
</dt> <dd>

<span data-ttu-id="c73ec-120">Le nom spécifié n’est pas valide.</span><span class="sxs-lookup"><span data-stu-id="c73ec-120">The name specified was not valid.</span></span>

</dd> <dt>

<span data-ttu-id="c73ec-121">**10**</span><span class="sxs-lookup"><span data-stu-id="c73ec-121">**10**</span></span>
</dt> <dd>

<span data-ttu-id="c73ec-122">L’objet spécifié existe déjà.</span><span class="sxs-lookup"><span data-stu-id="c73ec-122">The object specified already exists.</span></span>

</dd> <dt>

<span data-ttu-id="c73ec-123">**11**</span><span class="sxs-lookup"><span data-stu-id="c73ec-123">**11**</span></span>
</dt> <dd>

<span data-ttu-id="c73ec-124">Le système de fichiers n’est pas NTFS.</span><span class="sxs-lookup"><span data-stu-id="c73ec-124">The file system is not NTFS.</span></span>

</dd> <dt>

<span data-ttu-id="c73ec-125">**12**</span><span class="sxs-lookup"><span data-stu-id="c73ec-125">**12**</span></span>
</dt> <dd>

<span data-ttu-id="c73ec-126">La plateforme n’est pas Windows.</span><span class="sxs-lookup"><span data-stu-id="c73ec-126">The platform is not Windows.</span></span>

</dd> <dt>

<span data-ttu-id="c73ec-127">**13**</span><span class="sxs-lookup"><span data-stu-id="c73ec-127">**13**</span></span>
</dt> <dd>

<span data-ttu-id="c73ec-128">Le lecteur n’est pas le même.</span><span class="sxs-lookup"><span data-stu-id="c73ec-128">The drive is not the same.</span></span>

</dd> <dt>

<span data-ttu-id="c73ec-129">**14**</span><span class="sxs-lookup"><span data-stu-id="c73ec-129">**14**</span></span>
</dt> <dd>

<span data-ttu-id="c73ec-130">Le répertoire n'est pas vide.</span><span class="sxs-lookup"><span data-stu-id="c73ec-130">The directory is not empty.</span></span>

</dd> <dt>

<span data-ttu-id="c73ec-131">**15**</span><span class="sxs-lookup"><span data-stu-id="c73ec-131">**15**</span></span>
</dt> <dd>

<span data-ttu-id="c73ec-132">Une violation de partage s’est produite.</span><span class="sxs-lookup"><span data-stu-id="c73ec-132">There has been a sharing violation.</span></span>

</dd> <dt>

<span data-ttu-id="c73ec-133">**16**</span><span class="sxs-lookup"><span data-stu-id="c73ec-133">**16**</span></span>
</dt> <dd>

<span data-ttu-id="c73ec-134">Le fichier de démarrage spécifié n’est pas valide.</span><span class="sxs-lookup"><span data-stu-id="c73ec-134">The start file specified was not valid.</span></span>

</dd> <dt>

<span data-ttu-id="c73ec-135">**17**</span><span class="sxs-lookup"><span data-stu-id="c73ec-135">**17**</span></span>
</dt> <dd>

<span data-ttu-id="c73ec-136">Un privilège requis pour l’opération n’est pas conservé.</span><span class="sxs-lookup"><span data-stu-id="c73ec-136">A privilege required for the operation is not held.</span></span>

</dd> <dt>

<span data-ttu-id="c73ec-137">**21**</span><span class="sxs-lookup"><span data-stu-id="c73ec-137">**21**</span></span>
</dt> <dd>

<span data-ttu-id="c73ec-138">Un paramètre spécifié n’est pas valide.</span><span class="sxs-lookup"><span data-stu-id="c73ec-138">A parameter specified is not valid.</span></span>

</dd> </dl>

## <a name="examples"></a><span data-ttu-id="c73ec-139">Exemples</span><span class="sxs-lookup"><span data-stu-id="c73ec-139">Examples</span></span>

<span data-ttu-id="c73ec-140">L’Visual Basic Code de script suivant appelle la méthode [**TakeOwnership**](takeownership-method-in-class-cim-directory.md) pour prendre possession du dossier C : \\ temp.</span><span class="sxs-lookup"><span data-stu-id="c73ec-140">The following Visual Basic Script code calls the [**TakeOwnerShip**](takeownership-method-in-class-cim-directory.md) method to take ownership of the C:\\temp folder.</span></span>


```VB
strComputer = "." 

Set objWMIService = _
    GetObject("winmgmts:\\" & strComputer & "\root\CIMV2") 

' Obtain the definition of the class.
Set objShare = objWMIService.Get("Win32_Directory")

' Execute the method and obtain the return status.
' The OutParameters object in objOutParams
' is created by the provider.
Set objOutParams = objWMIService.ExecMethod( _
    "Win32_Directory.Name='C:\\temp'", "TakeOwnerShip")

wscript.echo objOutParams.ReturnValue
```



## <a name="requirements"></a><span data-ttu-id="c73ec-141">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="c73ec-141">Requirements</span></span>



| <span data-ttu-id="c73ec-142">Condition requise</span><span class="sxs-lookup"><span data-stu-id="c73ec-142">Requirement</span></span> | <span data-ttu-id="c73ec-143">Valeur</span><span class="sxs-lookup"><span data-stu-id="c73ec-143">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="c73ec-144">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="c73ec-144">Minimum supported client</span></span><br/> | <span data-ttu-id="c73ec-145">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="c73ec-145">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="c73ec-146">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="c73ec-146">Minimum supported server</span></span><br/> | <span data-ttu-id="c73ec-147">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="c73ec-147">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="c73ec-148">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="c73ec-148">Namespace</span></span><br/>                | <span data-ttu-id="c73ec-149">\\Cimv2 racine</span><span class="sxs-lookup"><span data-stu-id="c73ec-149">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="c73ec-150">MOF</span><span class="sxs-lookup"><span data-stu-id="c73ec-150">MOF</span></span><br/>                      | <dl> <span data-ttu-id="c73ec-151"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="c73ec-151"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="c73ec-152">DLL</span><span class="sxs-lookup"><span data-stu-id="c73ec-152">DLL</span></span><br/>                      | <dl> <span data-ttu-id="c73ec-153"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="c73ec-153"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c73ec-154">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="c73ec-154">See also</span></span>

<dl> <dt>

<span data-ttu-id="c73ec-155">[Classes du système d’exploitation](/previous-versions//aa392727(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="c73ec-155">[Operating System Classes](/previous-versions//aa392727(v=vs.85))</span></span>
</dt> <dt>

[<span data-ttu-id="c73ec-156">**\_Répertoire Win32**</span><span class="sxs-lookup"><span data-stu-id="c73ec-156">**Win32\_Directory**</span></span>](win32-directory.md)
</dt> </dl>

 

