---
description: Décompresse le fichier de codec logique (ou le répertoire) spécifié dans le chemin d’accès de l’objet.
ms.assetid: abe74267-1274-4b20-82ac-51ca94d7af33
ms.tgt_platform: multiple
title: Méthode decompress de la classe Win32_CodecFile
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_CodecFile.Uncompress
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: 7d1ffcf99877781c7070b42dac5ffe9ef83af2d5
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103860830"
---
# <a name="uncompress-method-of-the-win32_codecfile-class"></a><span data-ttu-id="0c67d-103">Méthode decompress de la \_ classe CodecFile Win32</span><span class="sxs-lookup"><span data-stu-id="0c67d-103">Uncompress method of the Win32\_CodecFile class</span></span>

<span data-ttu-id="0c67d-104">La méthode de [classe WMI](/windows/desktop/WmiSdk/retrieving-a-class) de **décompression** décompresse le fichier de codec logique (ou le répertoire) spécifié dans le chemin d’accès de l’objet.</span><span class="sxs-lookup"><span data-stu-id="0c67d-104">The **Uncompress** [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) method uncompresses the logical codec file (or directory) specified in the object path.</span></span>

<span data-ttu-id="0c67d-105">Cette rubrique utilise la syntaxe format MOF (MOF).</span><span class="sxs-lookup"><span data-stu-id="0c67d-105">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="0c67d-106">Pour plus d’informations sur l’utilisation de cette méthode, consultez [appel d’une méthode](/windows/desktop/WmiSdk/calling-a-method).</span><span class="sxs-lookup"><span data-stu-id="0c67d-106">For more information about using this method, see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="0c67d-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="0c67d-107">Syntax</span></span>


```mof
uint32 Uncompress();
```



## <a name="parameters"></a><span data-ttu-id="0c67d-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="0c67d-108">Parameters</span></span>

<span data-ttu-id="0c67d-109">Cette méthode n’a aucun paramètre.</span><span class="sxs-lookup"><span data-stu-id="0c67d-109">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="0c67d-110">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="0c67d-110">Return value</span></span>

<span data-ttu-id="0c67d-111">Retourne une valeur entière égale à 0 (zéro) si le fichier a été décompressé avec succès, et tout autre nombre pour indiquer une erreur.</span><span class="sxs-lookup"><span data-stu-id="0c67d-111">Returns an integer value of 0 (zero) if the file was successfully decompressed, and any other number to indicate an error.</span></span>

<dl> <dt>

<span data-ttu-id="0c67d-112">**0**</span><span class="sxs-lookup"><span data-stu-id="0c67d-112">**0**</span></span>
</dt> <dd>

<span data-ttu-id="0c67d-113">La demande a abouti.</span><span class="sxs-lookup"><span data-stu-id="0c67d-113">The request was successful.</span></span>

</dd> <dt>

<span data-ttu-id="0c67d-114">**2**</span><span class="sxs-lookup"><span data-stu-id="0c67d-114">**2**</span></span>
</dt> <dd>

<span data-ttu-id="0c67d-115">L’accès a été refusé.</span><span class="sxs-lookup"><span data-stu-id="0c67d-115">Access was denied.</span></span>

</dd> <dt>

<span data-ttu-id="0c67d-116">**8**</span><span class="sxs-lookup"><span data-stu-id="0c67d-116">**8**</span></span>
</dt> <dd>

<span data-ttu-id="0c67d-117">Une erreur non spécifiée s’est produite.</span><span class="sxs-lookup"><span data-stu-id="0c67d-117">An unspecified failure occurred.</span></span>

</dd> <dt>

<span data-ttu-id="0c67d-118">**9**</span><span class="sxs-lookup"><span data-stu-id="0c67d-118">**9**</span></span>
</dt> <dd>

<span data-ttu-id="0c67d-119">Le nom spécifié n’est pas valide.</span><span class="sxs-lookup"><span data-stu-id="0c67d-119">The name specified was not valid.</span></span>

</dd> <dt>

<span data-ttu-id="0c67d-120">**10**</span><span class="sxs-lookup"><span data-stu-id="0c67d-120">**10**</span></span>
</dt> <dd>

<span data-ttu-id="0c67d-121">L’objet spécifié existe déjà.</span><span class="sxs-lookup"><span data-stu-id="0c67d-121">The object specified already exists.</span></span>

</dd> <dt>

<span data-ttu-id="0c67d-122">**11**</span><span class="sxs-lookup"><span data-stu-id="0c67d-122">**11**</span></span>
</dt> <dd>

<span data-ttu-id="0c67d-123">Le système de fichiers n’est pas NTFS.</span><span class="sxs-lookup"><span data-stu-id="0c67d-123">The file system is not NTFS.</span></span>

</dd> <dt>

<span data-ttu-id="0c67d-124">**12**</span><span class="sxs-lookup"><span data-stu-id="0c67d-124">**12**</span></span>
</dt> <dd>

<span data-ttu-id="0c67d-125">La plateforme n’est pas Windows.</span><span class="sxs-lookup"><span data-stu-id="0c67d-125">The platform is not Windows.</span></span>

</dd> <dt>

<span data-ttu-id="0c67d-126">**13**</span><span class="sxs-lookup"><span data-stu-id="0c67d-126">**13**</span></span>
</dt> <dd>

<span data-ttu-id="0c67d-127">Le lecteur n’est pas le même.</span><span class="sxs-lookup"><span data-stu-id="0c67d-127">The drive is not the same.</span></span>

</dd> <dt>

<span data-ttu-id="0c67d-128">**14**</span><span class="sxs-lookup"><span data-stu-id="0c67d-128">**14**</span></span>
</dt> <dd>

<span data-ttu-id="0c67d-129">Le répertoire n'est pas vide.</span><span class="sxs-lookup"><span data-stu-id="0c67d-129">The directory is not empty.</span></span>

</dd> <dt>

<span data-ttu-id="0c67d-130">**15**</span><span class="sxs-lookup"><span data-stu-id="0c67d-130">**15**</span></span>
</dt> <dd>

<span data-ttu-id="0c67d-131">Une violation de partage s’est produite.</span><span class="sxs-lookup"><span data-stu-id="0c67d-131">There has been a sharing violation.</span></span>

</dd> <dt>

<span data-ttu-id="0c67d-132">**16**</span><span class="sxs-lookup"><span data-stu-id="0c67d-132">**16**</span></span>
</dt> <dd>

<span data-ttu-id="0c67d-133">Le fichier de démarrage spécifié n’est pas valide.</span><span class="sxs-lookup"><span data-stu-id="0c67d-133">The start file specified was not valid.</span></span>

</dd> <dt>

<span data-ttu-id="0c67d-134">**17**</span><span class="sxs-lookup"><span data-stu-id="0c67d-134">**17**</span></span>
</dt> <dd>

<span data-ttu-id="0c67d-135">Un privilège requis pour l’opération n’est pas conservé.</span><span class="sxs-lookup"><span data-stu-id="0c67d-135">A privilege required for the operation is not held.</span></span>

</dd> <dt>

<span data-ttu-id="0c67d-136">**21**</span><span class="sxs-lookup"><span data-stu-id="0c67d-136">**21**</span></span>
</dt> <dd>

<span data-ttu-id="0c67d-137">Un paramètre spécifié n’est pas valide.</span><span class="sxs-lookup"><span data-stu-id="0c67d-137">A parameter specified is not valid.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="0c67d-138">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="0c67d-138">Requirements</span></span>



| <span data-ttu-id="0c67d-139">Condition requise</span><span class="sxs-lookup"><span data-stu-id="0c67d-139">Requirement</span></span> | <span data-ttu-id="0c67d-140">Valeur</span><span class="sxs-lookup"><span data-stu-id="0c67d-140">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="0c67d-141">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="0c67d-141">Minimum supported client</span></span><br/> | <span data-ttu-id="0c67d-142">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="0c67d-142">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="0c67d-143">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="0c67d-143">Minimum supported server</span></span><br/> | <span data-ttu-id="0c67d-144">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="0c67d-144">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="0c67d-145">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="0c67d-145">Namespace</span></span><br/>                | <span data-ttu-id="0c67d-146">\\Cimv2 racine</span><span class="sxs-lookup"><span data-stu-id="0c67d-146">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="0c67d-147">MOF</span><span class="sxs-lookup"><span data-stu-id="0c67d-147">MOF</span></span><br/>                      | <dl> <span data-ttu-id="0c67d-148"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="0c67d-148"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="0c67d-149">DLL</span><span class="sxs-lookup"><span data-stu-id="0c67d-149">DLL</span></span><br/>                      | <dl> <span data-ttu-id="0c67d-150"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="0c67d-150"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0c67d-151">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="0c67d-151">See also</span></span>

<dl> <dt>

<span data-ttu-id="0c67d-152">[Classes du système d’exploitation](/previous-versions//aa392727(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="0c67d-152">[Operating System Classes](/previous-versions//aa392727(v=vs.85))</span></span>
</dt> <dt>

[<span data-ttu-id="0c67d-153">**\_CodecFile Win32**</span><span class="sxs-lookup"><span data-stu-id="0c67d-153">**Win32\_CodecFile**</span></span>](win32-codecfile.md)
</dt> </dl>

 

