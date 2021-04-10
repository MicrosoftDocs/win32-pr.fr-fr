---
description: Renomme le fichier de codec spécifié dans le chemin d’accès de l’objet.
ms.assetid: fd6ce02c-d513-4643-ac27-313c32732f1e
ms.tgt_platform: multiple
title: Renommer la méthode de la classe Win32_CodecFile
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_CodecFile.Rename
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: a4eb931a0155518ad9644ebb1cce0b604be80602
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103950772"
---
# <a name="rename-method-of-the-win32_codecfile-class"></a><span data-ttu-id="13dc2-103">Renommer la méthode de la \_ classe CodecFile Win32</span><span class="sxs-lookup"><span data-stu-id="13dc2-103">Rename method of the Win32\_CodecFile class</span></span>

<span data-ttu-id="13dc2-104">La méthode de la classe **Renommer** [WMI](/windows/desktop/WmiSdk/retrieving-a-class) renomme le fichier de codec spécifié dans le chemin d’accès de l’objet.</span><span class="sxs-lookup"><span data-stu-id="13dc2-104">The **Rename** [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) method renames the codec file specified in the object path.</span></span> <span data-ttu-id="13dc2-105">Un changement de nom n’est pas pris en charge si la destination se trouve sur un autre lecteur ou si le remplacement d’un fichier logique existant est nécessaire.</span><span class="sxs-lookup"><span data-stu-id="13dc2-105">A rename is not supported if the destination is on another drive or if overwriting an existing logical file is required.</span></span>

<span data-ttu-id="13dc2-106">Cette rubrique utilise la syntaxe format MOF (MOF).</span><span class="sxs-lookup"><span data-stu-id="13dc2-106">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="13dc2-107">Pour plus d’informations sur l’utilisation de cette méthode, consultez [appel d’une méthode](/windows/desktop/WmiSdk/calling-a-method).</span><span class="sxs-lookup"><span data-stu-id="13dc2-107">For more information about using this method see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="13dc2-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="13dc2-108">Syntax</span></span>


```mof
uint32 Rename(
   string FileName
);
```



## <a name="parameters"></a><span data-ttu-id="13dc2-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="13dc2-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="13dc2-110">*FileName*</span><span class="sxs-lookup"><span data-stu-id="13dc2-110">*FileName*</span></span> 
</dt> <dd>

<span data-ttu-id="13dc2-111">Nouveau nom complet du fichier (ou répertoire).</span><span class="sxs-lookup"><span data-stu-id="13dc2-111">Fully qualified new name of the file (or directory).</span></span> <span data-ttu-id="13dc2-112">Exemple : c : \\ temp \\newfile.txt.</span><span class="sxs-lookup"><span data-stu-id="13dc2-112">Example: c:\\temp\\newfile.txt.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="13dc2-113">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="13dc2-113">Return value</span></span>

<span data-ttu-id="13dc2-114">Retourne une valeur entière égale à 0 (zéro) si le fichier a été renommé avec succès, et tout autre nombre pour indiquer une erreur.</span><span class="sxs-lookup"><span data-stu-id="13dc2-114">Returns an integer value of 0 (zero) if the file was successfully renamed, and any other number to indicate an error.</span></span>

<dl> <dt>

<span data-ttu-id="13dc2-115">**0**</span><span class="sxs-lookup"><span data-stu-id="13dc2-115">**0**</span></span>
</dt> <dd>

<span data-ttu-id="13dc2-116">La demande a abouti.</span><span class="sxs-lookup"><span data-stu-id="13dc2-116">The request was successful.</span></span>

</dd> <dt>

<span data-ttu-id="13dc2-117">**2**</span><span class="sxs-lookup"><span data-stu-id="13dc2-117">**2**</span></span>
</dt> <dd>

<span data-ttu-id="13dc2-118">L’accès a été refusé.</span><span class="sxs-lookup"><span data-stu-id="13dc2-118">Access was denied.</span></span>

</dd> <dt>

<span data-ttu-id="13dc2-119">**8**</span><span class="sxs-lookup"><span data-stu-id="13dc2-119">**8**</span></span>
</dt> <dd>

<span data-ttu-id="13dc2-120">Une erreur non spécifiée s’est produite.</span><span class="sxs-lookup"><span data-stu-id="13dc2-120">An unspecified failure occurred.</span></span>

</dd> <dt>

<span data-ttu-id="13dc2-121">**9**</span><span class="sxs-lookup"><span data-stu-id="13dc2-121">**9**</span></span>
</dt> <dd>

<span data-ttu-id="13dc2-122">Le nom spécifié n’est pas valide.</span><span class="sxs-lookup"><span data-stu-id="13dc2-122">The name specified was not valid.</span></span>

</dd> <dt>

<span data-ttu-id="13dc2-123">**10**</span><span class="sxs-lookup"><span data-stu-id="13dc2-123">**10**</span></span>
</dt> <dd>

<span data-ttu-id="13dc2-124">L’objet spécifié existe déjà.</span><span class="sxs-lookup"><span data-stu-id="13dc2-124">The object specified already exists.</span></span>

</dd> <dt>

<span data-ttu-id="13dc2-125">**11**</span><span class="sxs-lookup"><span data-stu-id="13dc2-125">**11**</span></span>
</dt> <dd>

<span data-ttu-id="13dc2-126">Le système de fichiers n’est pas NTFS.</span><span class="sxs-lookup"><span data-stu-id="13dc2-126">The file system is not NTFS.</span></span>

</dd> <dt>

<span data-ttu-id="13dc2-127">**12**</span><span class="sxs-lookup"><span data-stu-id="13dc2-127">**12**</span></span>
</dt> <dd>

<span data-ttu-id="13dc2-128">La plateforme n’est pas Windows.</span><span class="sxs-lookup"><span data-stu-id="13dc2-128">The platform is not Windows.</span></span>

</dd> <dt>

<span data-ttu-id="13dc2-129">**13**</span><span class="sxs-lookup"><span data-stu-id="13dc2-129">**13**</span></span>
</dt> <dd>

<span data-ttu-id="13dc2-130">Le lecteur n’est pas le même.</span><span class="sxs-lookup"><span data-stu-id="13dc2-130">The drive is not the same.</span></span>

</dd> <dt>

<span data-ttu-id="13dc2-131">**14**</span><span class="sxs-lookup"><span data-stu-id="13dc2-131">**14**</span></span>
</dt> <dd>

<span data-ttu-id="13dc2-132">Le répertoire n'est pas vide.</span><span class="sxs-lookup"><span data-stu-id="13dc2-132">The directory is not empty.</span></span>

</dd> <dt>

<span data-ttu-id="13dc2-133">**15**</span><span class="sxs-lookup"><span data-stu-id="13dc2-133">**15**</span></span>
</dt> <dd>

<span data-ttu-id="13dc2-134">Une violation de partage s’est produite.</span><span class="sxs-lookup"><span data-stu-id="13dc2-134">There has been a sharing violation.</span></span>

</dd> <dt>

<span data-ttu-id="13dc2-135">**16**</span><span class="sxs-lookup"><span data-stu-id="13dc2-135">**16**</span></span>
</dt> <dd>

<span data-ttu-id="13dc2-136">Le fichier de démarrage spécifié n’est pas valide.</span><span class="sxs-lookup"><span data-stu-id="13dc2-136">The start file specified was not valid.</span></span>

</dd> <dt>

<span data-ttu-id="13dc2-137">**17**</span><span class="sxs-lookup"><span data-stu-id="13dc2-137">**17**</span></span>
</dt> <dd>

<span data-ttu-id="13dc2-138">Un privilège requis pour l’opération n’est pas conservé.</span><span class="sxs-lookup"><span data-stu-id="13dc2-138">A privilege required for the operation is not held.</span></span>

</dd> <dt>

<span data-ttu-id="13dc2-139">**21**</span><span class="sxs-lookup"><span data-stu-id="13dc2-139">**21**</span></span>
</dt> <dd>

<span data-ttu-id="13dc2-140">Un paramètre spécifié n’est pas valide.</span><span class="sxs-lookup"><span data-stu-id="13dc2-140">A parameter specified is not valid.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="13dc2-141">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="13dc2-141">Requirements</span></span>



| <span data-ttu-id="13dc2-142">Condition requise</span><span class="sxs-lookup"><span data-stu-id="13dc2-142">Requirement</span></span> | <span data-ttu-id="13dc2-143">Valeur</span><span class="sxs-lookup"><span data-stu-id="13dc2-143">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="13dc2-144">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="13dc2-144">Minimum supported client</span></span><br/> | <span data-ttu-id="13dc2-145">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="13dc2-145">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="13dc2-146">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="13dc2-146">Minimum supported server</span></span><br/> | <span data-ttu-id="13dc2-147">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="13dc2-147">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="13dc2-148">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="13dc2-148">Namespace</span></span><br/>                | <span data-ttu-id="13dc2-149">\\Cimv2 racine</span><span class="sxs-lookup"><span data-stu-id="13dc2-149">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="13dc2-150">MOF</span><span class="sxs-lookup"><span data-stu-id="13dc2-150">MOF</span></span><br/>                      | <dl> <span data-ttu-id="13dc2-151"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="13dc2-151"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="13dc2-152">DLL</span><span class="sxs-lookup"><span data-stu-id="13dc2-152">DLL</span></span><br/>                      | <dl> <span data-ttu-id="13dc2-153"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="13dc2-153"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="13dc2-154">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="13dc2-154">See also</span></span>

<dl> <dt>

<span data-ttu-id="13dc2-155">[Classes du système d’exploitation](/previous-versions//aa392727(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="13dc2-155">[Operating System Classes](/previous-versions//aa392727(v=vs.85))</span></span>
</dt> <dt>

[<span data-ttu-id="13dc2-156">**\_CodecFile Win32**</span><span class="sxs-lookup"><span data-stu-id="13dc2-156">**Win32\_CodecFile**</span></span>](win32-codecfile.md)
</dt> </dl>

 

