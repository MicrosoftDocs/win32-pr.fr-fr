---
description: TakeOwnerShip&\# 8194 ; La méthode de classe WMI obtient la propriété du fichier logique spécifié dans le chemin d’accès de l’objet.
ms.assetid: 1a8ff156-50b2-4550-abcc-7a6ae0e4630f
ms.tgt_platform: multiple
title: Méthode TakeOwnerShip de la classe Win32_ShortcutFile
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_ShortcutFile.TakeOwnerShip
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: 5da7a237ae1943e65bc1cc757d5c4a16c6df8900
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103950453"
---
# <a name="takeownership-method-of-the-win32_shortcutfile-class"></a><span data-ttu-id="2005a-103">Méthode TakeOwnerShip de la \_ classe Win32 ShortcutFile</span><span class="sxs-lookup"><span data-stu-id="2005a-103">TakeOwnerShip method of the Win32\_ShortcutFile class</span></span>

<span data-ttu-id="2005a-104">La méthode de [classe WMI](/windows/desktop/WmiSdk/retrieving-a-class) **TakeOwnership** obtient la propriété du fichier logique spécifié dans le chemin d’accès de l’objet.</span><span class="sxs-lookup"><span data-stu-id="2005a-104">The **TakeOwnerShip** [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) method obtains ownership of the logical file specified in the object path.</span></span> <span data-ttu-id="2005a-105">Si le fichier logique est effectivement un répertoire, **TakeOwnership** agit de manière récursive, en prenant possession de tous les fichiers et sous-répertoires contenus dans le répertoire.</span><span class="sxs-lookup"><span data-stu-id="2005a-105">If the logical file is actually a directory, then **TakeOwnerShip** acts recursively, taking ownership of all the files and subdirectories the directory contains.</span></span>

<span data-ttu-id="2005a-106">Cette rubrique utilise la syntaxe format MOF (MOF).</span><span class="sxs-lookup"><span data-stu-id="2005a-106">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="2005a-107">Pour plus d’informations sur l’utilisation de cette méthode, consultez [appel d’une méthode](/windows/desktop/WmiSdk/calling-a-method).</span><span class="sxs-lookup"><span data-stu-id="2005a-107">For more information about using this method, see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="2005a-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="2005a-108">Syntax</span></span>


```mof
uint32 TakeOwnerShip();
```



## <a name="parameters"></a><span data-ttu-id="2005a-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="2005a-109">Parameters</span></span>

<span data-ttu-id="2005a-110">Cette méthode n’a aucun paramètre.</span><span class="sxs-lookup"><span data-stu-id="2005a-110">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="2005a-111">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="2005a-111">Return value</span></span>

<span data-ttu-id="2005a-112">Retourne l’une des valeurs entières suivantes.</span><span class="sxs-lookup"><span data-stu-id="2005a-112">Returns one of the following integer values.</span></span>

<dl> <dt>

<span data-ttu-id="2005a-113">**0**</span><span class="sxs-lookup"><span data-stu-id="2005a-113">**0**</span></span>
</dt> <dd>

<span data-ttu-id="2005a-114">La demande a abouti.</span><span class="sxs-lookup"><span data-stu-id="2005a-114">The request was successful.</span></span>

</dd> <dt>

<span data-ttu-id="2005a-115">**2**</span><span class="sxs-lookup"><span data-stu-id="2005a-115">**2**</span></span>
</dt> <dd>

<span data-ttu-id="2005a-116">L’accès a été refusé.</span><span class="sxs-lookup"><span data-stu-id="2005a-116">Access was denied.</span></span>

</dd> <dt>

<span data-ttu-id="2005a-117">**8**</span><span class="sxs-lookup"><span data-stu-id="2005a-117">**8**</span></span>
</dt> <dd>

<span data-ttu-id="2005a-118">Une erreur non spécifiée s’est produite.</span><span class="sxs-lookup"><span data-stu-id="2005a-118">An unspecified failure occurred.</span></span>

</dd> <dt>

<span data-ttu-id="2005a-119">**9**</span><span class="sxs-lookup"><span data-stu-id="2005a-119">**9**</span></span>
</dt> <dd>

<span data-ttu-id="2005a-120">Le nom spécifié n’est pas valide.</span><span class="sxs-lookup"><span data-stu-id="2005a-120">The name specified was not valid.</span></span>

</dd> <dt>

<span data-ttu-id="2005a-121">**10**</span><span class="sxs-lookup"><span data-stu-id="2005a-121">**10**</span></span>
</dt> <dd>

<span data-ttu-id="2005a-122">L’objet spécifié existe déjà.</span><span class="sxs-lookup"><span data-stu-id="2005a-122">The object specified already exists.</span></span>

</dd> <dt>

<span data-ttu-id="2005a-123">**11**</span><span class="sxs-lookup"><span data-stu-id="2005a-123">**11**</span></span>
</dt> <dd>

<span data-ttu-id="2005a-124">Le système de fichiers n’est pas NTFS.</span><span class="sxs-lookup"><span data-stu-id="2005a-124">The file system is not NTFS.</span></span>

</dd> <dt>

<span data-ttu-id="2005a-125">**12**</span><span class="sxs-lookup"><span data-stu-id="2005a-125">**12**</span></span>
</dt> <dd>

<span data-ttu-id="2005a-126">La plateforme n’est pas Windows.</span><span class="sxs-lookup"><span data-stu-id="2005a-126">The platform is not Windows.</span></span>

</dd> <dt>

<span data-ttu-id="2005a-127">**13**</span><span class="sxs-lookup"><span data-stu-id="2005a-127">**13**</span></span>
</dt> <dd>

<span data-ttu-id="2005a-128">Le lecteur n’est pas le même.</span><span class="sxs-lookup"><span data-stu-id="2005a-128">The drive is not the same.</span></span>

</dd> <dt>

<span data-ttu-id="2005a-129">**14**</span><span class="sxs-lookup"><span data-stu-id="2005a-129">**14**</span></span>
</dt> <dd>

<span data-ttu-id="2005a-130">Le répertoire n'est pas vide.</span><span class="sxs-lookup"><span data-stu-id="2005a-130">The directory is not empty.</span></span>

</dd> <dt>

<span data-ttu-id="2005a-131">**15**</span><span class="sxs-lookup"><span data-stu-id="2005a-131">**15**</span></span>
</dt> <dd>

<span data-ttu-id="2005a-132">Une violation de partage s’est produite.</span><span class="sxs-lookup"><span data-stu-id="2005a-132">There has been a sharing violation.</span></span>

</dd> <dt>

<span data-ttu-id="2005a-133">**16**</span><span class="sxs-lookup"><span data-stu-id="2005a-133">**16**</span></span>
</dt> <dd>

<span data-ttu-id="2005a-134">Le fichier de démarrage spécifié n’est pas valide.</span><span class="sxs-lookup"><span data-stu-id="2005a-134">The start file specified was not valid.</span></span>

</dd> <dt>

<span data-ttu-id="2005a-135">**17**</span><span class="sxs-lookup"><span data-stu-id="2005a-135">**17**</span></span>
</dt> <dd>

<span data-ttu-id="2005a-136">Un privilège requis pour l’opération n’est pas conservé.</span><span class="sxs-lookup"><span data-stu-id="2005a-136">A privilege required for the operation is not held.</span></span>

</dd> <dt>

<span data-ttu-id="2005a-137">**21**</span><span class="sxs-lookup"><span data-stu-id="2005a-137">**21**</span></span>
</dt> <dd>

<span data-ttu-id="2005a-138">Un paramètre spécifié n’est pas valide.</span><span class="sxs-lookup"><span data-stu-id="2005a-138">A parameter specified is not valid.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="2005a-139">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="2005a-139">Requirements</span></span>



| <span data-ttu-id="2005a-140">Condition requise</span><span class="sxs-lookup"><span data-stu-id="2005a-140">Requirement</span></span> | <span data-ttu-id="2005a-141">Valeur</span><span class="sxs-lookup"><span data-stu-id="2005a-141">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="2005a-142">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="2005a-142">Minimum supported client</span></span><br/> | <span data-ttu-id="2005a-143">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="2005a-143">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="2005a-144">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="2005a-144">Minimum supported server</span></span><br/> | <span data-ttu-id="2005a-145">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="2005a-145">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="2005a-146">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="2005a-146">Namespace</span></span><br/>                | <span data-ttu-id="2005a-147">\\Cimv2 racine</span><span class="sxs-lookup"><span data-stu-id="2005a-147">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="2005a-148">MOF</span><span class="sxs-lookup"><span data-stu-id="2005a-148">MOF</span></span><br/>                      | <dl> <span data-ttu-id="2005a-149"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="2005a-149"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="2005a-150">DLL</span><span class="sxs-lookup"><span data-stu-id="2005a-150">DLL</span></span><br/>                      | <dl> <span data-ttu-id="2005a-151"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="2005a-151"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2005a-152">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="2005a-152">See also</span></span>

<dl> <dt>

<span data-ttu-id="2005a-153">[Classes du système d’exploitation](/previous-versions//aa392727(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="2005a-153">[Operating System Classes](/previous-versions//aa392727(v=vs.85))</span></span>
</dt> <dt>

[<span data-ttu-id="2005a-154">**\_ShortcutFile Win32**</span><span class="sxs-lookup"><span data-stu-id="2005a-154">**Win32\_ShortcutFile**</span></span>](win32-shortcutfile.md)
</dt> </dl>

 

