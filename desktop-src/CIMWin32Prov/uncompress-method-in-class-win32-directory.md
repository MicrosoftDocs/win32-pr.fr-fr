---
description: Décompresse le fichier d’entrée de répertoire logique (ou le répertoire) spécifié dans le chemin d’accès de l’objet.
ms.assetid: dd39aae3-7c88-48fc-93ed-5225d2f1491c
ms.tgt_platform: multiple
title: Méthode decompress de la classe Win32_Directory
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_Directory.Uncompress
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: 7c46a6bb90d43c1b793350bb96822a1aaed8dd9a
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104111395"
---
# <a name="uncompress-method-of-the-win32_directory-class"></a><span data-ttu-id="f32f0-103">Méthode decompress de la \_ classe Directory Win32</span><span class="sxs-lookup"><span data-stu-id="f32f0-103">Uncompress method of the Win32\_Directory class</span></span>

<span data-ttu-id="f32f0-104">La méthode de [classe WMI](/windows/desktop/WmiSdk/retrieving-a-class) de **décompression** décompresse le fichier d’entrée de répertoire logique (ou le répertoire) spécifié dans le chemin d’accès de l’objet.</span><span class="sxs-lookup"><span data-stu-id="f32f0-104">The **Uncompress** [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) method uncompresses the logical directory entry file (or directory) specified in the object path.</span></span>

<span data-ttu-id="f32f0-105">Cette rubrique utilise la syntaxe format MOF (MOF).</span><span class="sxs-lookup"><span data-stu-id="f32f0-105">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="f32f0-106">Pour plus d’informations sur l’utilisation de cette méthode, consultez [appel d’une méthode](/windows/desktop/WmiSdk/calling-a-method).</span><span class="sxs-lookup"><span data-stu-id="f32f0-106">For more information about using this method, see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="f32f0-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="f32f0-107">Syntax</span></span>


```mof
uint32 Uncompress();
```



## <a name="parameters"></a><span data-ttu-id="f32f0-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="f32f0-108">Parameters</span></span>

<span data-ttu-id="f32f0-109">Cette méthode n’a aucun paramètre.</span><span class="sxs-lookup"><span data-stu-id="f32f0-109">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="f32f0-110">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="f32f0-110">Return value</span></span>

<span data-ttu-id="f32f0-111">Retourne une valeur entière égale à 0 (zéro) si le fichier a été décompressé avec succès, et tout autre nombre pour indiquer une erreur.</span><span class="sxs-lookup"><span data-stu-id="f32f0-111">Returns an integer value of 0 (zero) if the file was successfully decompressed, and any other number to indicate an error.</span></span>

<dl> <dt>

<span data-ttu-id="f32f0-112">**0**</span><span class="sxs-lookup"><span data-stu-id="f32f0-112">**0**</span></span>
</dt> <dd>

<span data-ttu-id="f32f0-113">La demande a abouti.</span><span class="sxs-lookup"><span data-stu-id="f32f0-113">The request was successful.</span></span>

</dd> <dt>

<span data-ttu-id="f32f0-114">**2**</span><span class="sxs-lookup"><span data-stu-id="f32f0-114">**2**</span></span>
</dt> <dd>

<span data-ttu-id="f32f0-115">L’accès a été refusé.</span><span class="sxs-lookup"><span data-stu-id="f32f0-115">Access was denied.</span></span>

</dd> <dt>

<span data-ttu-id="f32f0-116">**8**</span><span class="sxs-lookup"><span data-stu-id="f32f0-116">**8**</span></span>
</dt> <dd>

<span data-ttu-id="f32f0-117">Une erreur non spécifiée s’est produite.</span><span class="sxs-lookup"><span data-stu-id="f32f0-117">An unspecified failure occurred.</span></span>

</dd> <dt>

<span data-ttu-id="f32f0-118">**9**</span><span class="sxs-lookup"><span data-stu-id="f32f0-118">**9**</span></span>
</dt> <dd>

<span data-ttu-id="f32f0-119">Le nom spécifié n’est pas valide.</span><span class="sxs-lookup"><span data-stu-id="f32f0-119">The name specified was not valid.</span></span>

</dd> <dt>

<span data-ttu-id="f32f0-120">**10**</span><span class="sxs-lookup"><span data-stu-id="f32f0-120">**10**</span></span>
</dt> <dd>

<span data-ttu-id="f32f0-121">L’objet spécifié existe déjà.</span><span class="sxs-lookup"><span data-stu-id="f32f0-121">The object specified already exists.</span></span>

</dd> <dt>

<span data-ttu-id="f32f0-122">**11**</span><span class="sxs-lookup"><span data-stu-id="f32f0-122">**11**</span></span>
</dt> <dd>

<span data-ttu-id="f32f0-123">Le système de fichiers n’est pas NTFS.</span><span class="sxs-lookup"><span data-stu-id="f32f0-123">The file system is not NTFS.</span></span>

</dd> <dt>

<span data-ttu-id="f32f0-124">**12**</span><span class="sxs-lookup"><span data-stu-id="f32f0-124">**12**</span></span>
</dt> <dd>

<span data-ttu-id="f32f0-125">La plateforme n’est pas Windows.</span><span class="sxs-lookup"><span data-stu-id="f32f0-125">The platform is not Windows.</span></span>

</dd> <dt>

<span data-ttu-id="f32f0-126">**13**</span><span class="sxs-lookup"><span data-stu-id="f32f0-126">**13**</span></span>
</dt> <dd>

<span data-ttu-id="f32f0-127">Le lecteur n’est pas le même.</span><span class="sxs-lookup"><span data-stu-id="f32f0-127">The drive is not the same.</span></span>

</dd> <dt>

<span data-ttu-id="f32f0-128">**14**</span><span class="sxs-lookup"><span data-stu-id="f32f0-128">**14**</span></span>
</dt> <dd>

<span data-ttu-id="f32f0-129">Le répertoire n'est pas vide.</span><span class="sxs-lookup"><span data-stu-id="f32f0-129">The directory is not empty.</span></span>

</dd> <dt>

<span data-ttu-id="f32f0-130">**15**</span><span class="sxs-lookup"><span data-stu-id="f32f0-130">**15**</span></span>
</dt> <dd>

<span data-ttu-id="f32f0-131">Une violation de partage s’est produite.</span><span class="sxs-lookup"><span data-stu-id="f32f0-131">There has been a sharing violation.</span></span>

</dd> <dt>

<span data-ttu-id="f32f0-132">**16**</span><span class="sxs-lookup"><span data-stu-id="f32f0-132">**16**</span></span>
</dt> <dd>

<span data-ttu-id="f32f0-133">Le fichier de démarrage spécifié n’est pas valide.</span><span class="sxs-lookup"><span data-stu-id="f32f0-133">The start file specified was not valid.</span></span>

</dd> <dt>

<span data-ttu-id="f32f0-134">**17**</span><span class="sxs-lookup"><span data-stu-id="f32f0-134">**17**</span></span>
</dt> <dd>

<span data-ttu-id="f32f0-135">Un privilège requis pour l’opération n’est pas conservé.</span><span class="sxs-lookup"><span data-stu-id="f32f0-135">A privilege required for the operation is not held.</span></span>

</dd> <dt>

<span data-ttu-id="f32f0-136">**21**</span><span class="sxs-lookup"><span data-stu-id="f32f0-136">**21**</span></span>
</dt> <dd>

<span data-ttu-id="f32f0-137">Un paramètre spécifié n’est pas valide.</span><span class="sxs-lookup"><span data-stu-id="f32f0-137">A parameter specified is not valid.</span></span>

</dd> </dl>

## <a name="examples"></a><span data-ttu-id="f32f0-138">Exemples</span><span class="sxs-lookup"><span data-stu-id="f32f0-138">Examples</span></span>

<span data-ttu-id="f32f0-139">L’exemple VBScript suivant décompresse le dossier c : \\ scripts.</span><span class="sxs-lookup"><span data-stu-id="f32f0-139">The following VBScript sample uncompresses the folder c:\\Scripts.</span></span>


```VB
strComputer = "."
Set objWMIService = GetObject("winmgmts:" _
 & "{impersonationLevel=impersonate}!\\" & strComputer & "\root\cimv2")
Set colFolders = objWMIService.ExecQuery _
 ("SELECT * FROM Win32_Directory WHERE Name = 'c:\\Scripts'")
For Each objFolder in colFolders
 errResults = objFolder.Uncompress
 Wscript.Echo errResults
Next
```



## <a name="requirements"></a><span data-ttu-id="f32f0-140">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="f32f0-140">Requirements</span></span>



| <span data-ttu-id="f32f0-141">Condition requise</span><span class="sxs-lookup"><span data-stu-id="f32f0-141">Requirement</span></span> | <span data-ttu-id="f32f0-142">Valeur</span><span class="sxs-lookup"><span data-stu-id="f32f0-142">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="f32f0-143">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="f32f0-143">Minimum supported client</span></span><br/> | <span data-ttu-id="f32f0-144">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="f32f0-144">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="f32f0-145">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="f32f0-145">Minimum supported server</span></span><br/> | <span data-ttu-id="f32f0-146">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="f32f0-146">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="f32f0-147">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="f32f0-147">Namespace</span></span><br/>                | <span data-ttu-id="f32f0-148">\\Cimv2 racine</span><span class="sxs-lookup"><span data-stu-id="f32f0-148">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="f32f0-149">MOF</span><span class="sxs-lookup"><span data-stu-id="f32f0-149">MOF</span></span><br/>                      | <dl> <span data-ttu-id="f32f0-150"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="f32f0-150"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="f32f0-151">DLL</span><span class="sxs-lookup"><span data-stu-id="f32f0-151">DLL</span></span><br/>                      | <dl> <span data-ttu-id="f32f0-152"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="f32f0-152"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f32f0-153">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="f32f0-153">See also</span></span>

<dl> <dt>

<span data-ttu-id="f32f0-154">[Classes du système d’exploitation](/previous-versions//aa392727(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="f32f0-154">[Operating System Classes](/previous-versions//aa392727(v=vs.85))</span></span>
</dt> <dt>

[<span data-ttu-id="f32f0-155">**\_Répertoire Win32**</span><span class="sxs-lookup"><span data-stu-id="f32f0-155">**Win32\_Directory**</span></span>](win32-directory.md)
</dt> <dt>

[<span data-ttu-id="f32f0-156">**Dens**</span><span class="sxs-lookup"><span data-stu-id="f32f0-156">**Compress**</span></span>](compress-method-in-class-win32-directory.md)
</dt> </dl>

 

