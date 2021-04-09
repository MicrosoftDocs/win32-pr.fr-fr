---
description: Décompresse le fichier d’échange logique (ou le répertoire) spécifié dans le chemin d’accès de l’objet.
ms.assetid: 9bd98ba8-068e-49af-8dd4-e5ee987eb31d
ms.tgt_platform: multiple
title: Méthode decompress de la classe Win32_PageFile
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_PageFile.Uncompress
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: 45a5b48ffa6b2249992b61eadf72f42f6d71969b
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103861606"
---
# <a name="uncompress-method-of-the-win32_pagefile-class"></a><span data-ttu-id="87fa6-103">Méthode decompress de la \_ classe pagefile Win32</span><span class="sxs-lookup"><span data-stu-id="87fa6-103">Uncompress method of the Win32\_PageFile class</span></span>

<span data-ttu-id="87fa6-104">La méthode de [classe WMI](/windows/desktop/WmiSdk/retrieving-a-class) de **décompression** décompresse le fichier d’échange logique (ou le répertoire) spécifié dans le chemin d’accès de l’objet.</span><span class="sxs-lookup"><span data-stu-id="87fa6-104">The **Uncompress** [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) method uncompresses the logical paging file (or directory) specified in the object path.</span></span>

<span data-ttu-id="87fa6-105">Cette rubrique utilise la syntaxe format MOF (MOF).</span><span class="sxs-lookup"><span data-stu-id="87fa6-105">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="87fa6-106">Pour plus d’informations sur l’utilisation de cette méthode, consultez [appel d’une méthode](/windows/desktop/WmiSdk/calling-a-method).</span><span class="sxs-lookup"><span data-stu-id="87fa6-106">For more information about using this method, see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="87fa6-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="87fa6-107">Syntax</span></span>


```mof
uint32 Uncompress();
```



## <a name="parameters"></a><span data-ttu-id="87fa6-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="87fa6-108">Parameters</span></span>

<span data-ttu-id="87fa6-109">Cette méthode n’a aucun paramètre.</span><span class="sxs-lookup"><span data-stu-id="87fa6-109">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="87fa6-110">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="87fa6-110">Return value</span></span>

<span data-ttu-id="87fa6-111">Retourne la valeur 0 (zéro) si le fichier a été décompressé avec succès, et tout autre nombre pour indiquer une erreur.</span><span class="sxs-lookup"><span data-stu-id="87fa6-111">Returns a value of 0 (zero) if the file was successfully decompressed, and any other number to indicate an error.</span></span>

<dl> <dt>

<span data-ttu-id="87fa6-112">**0**</span><span class="sxs-lookup"><span data-stu-id="87fa6-112">**0**</span></span>
</dt> <dd>

<span data-ttu-id="87fa6-113">La demande a abouti.</span><span class="sxs-lookup"><span data-stu-id="87fa6-113">The request was successful.</span></span>

</dd> <dt>

<span data-ttu-id="87fa6-114">**2**</span><span class="sxs-lookup"><span data-stu-id="87fa6-114">**2**</span></span>
</dt> <dd>

<span data-ttu-id="87fa6-115">L’accès a été refusé.</span><span class="sxs-lookup"><span data-stu-id="87fa6-115">Access was denied.</span></span>

</dd> <dt>

<span data-ttu-id="87fa6-116">**8**</span><span class="sxs-lookup"><span data-stu-id="87fa6-116">**8**</span></span>
</dt> <dd>

<span data-ttu-id="87fa6-117">Une erreur non spécifiée s’est produite.</span><span class="sxs-lookup"><span data-stu-id="87fa6-117">An unspecified failure occurred.</span></span>

</dd> <dt>

<span data-ttu-id="87fa6-118">**9**</span><span class="sxs-lookup"><span data-stu-id="87fa6-118">**9**</span></span>
</dt> <dd>

<span data-ttu-id="87fa6-119">Le nom spécifié n’est pas valide.</span><span class="sxs-lookup"><span data-stu-id="87fa6-119">The name specified was not valid.</span></span>

</dd> <dt>

<span data-ttu-id="87fa6-120">**10**</span><span class="sxs-lookup"><span data-stu-id="87fa6-120">**10**</span></span>
</dt> <dd>

<span data-ttu-id="87fa6-121">L’objet spécifié existe déjà.</span><span class="sxs-lookup"><span data-stu-id="87fa6-121">The object specified already exists.</span></span>

</dd> <dt>

<span data-ttu-id="87fa6-122">**11**</span><span class="sxs-lookup"><span data-stu-id="87fa6-122">**11**</span></span>
</dt> <dd>

<span data-ttu-id="87fa6-123">Le système de fichiers n’est pas NTFS.</span><span class="sxs-lookup"><span data-stu-id="87fa6-123">The file system is not NTFS.</span></span>

</dd> <dt>

<span data-ttu-id="87fa6-124">**12**</span><span class="sxs-lookup"><span data-stu-id="87fa6-124">**12**</span></span>
</dt> <dd>

<span data-ttu-id="87fa6-125">La plateforme n’est pas Windows.</span><span class="sxs-lookup"><span data-stu-id="87fa6-125">The platform is not Windows.</span></span>

</dd> <dt>

<span data-ttu-id="87fa6-126">**13**</span><span class="sxs-lookup"><span data-stu-id="87fa6-126">**13**</span></span>
</dt> <dd>

<span data-ttu-id="87fa6-127">Le lecteur n’est pas le même.</span><span class="sxs-lookup"><span data-stu-id="87fa6-127">The drive is not the same.</span></span>

</dd> <dt>

<span data-ttu-id="87fa6-128">**14**</span><span class="sxs-lookup"><span data-stu-id="87fa6-128">**14**</span></span>
</dt> <dd>

<span data-ttu-id="87fa6-129">Le répertoire n'est pas vide.</span><span class="sxs-lookup"><span data-stu-id="87fa6-129">The directory is not empty.</span></span>

</dd> <dt>

<span data-ttu-id="87fa6-130">**15**</span><span class="sxs-lookup"><span data-stu-id="87fa6-130">**15**</span></span>
</dt> <dd>

<span data-ttu-id="87fa6-131">Une violation de partage s’est produite.</span><span class="sxs-lookup"><span data-stu-id="87fa6-131">There has been a sharing violation.</span></span>

</dd> <dt>

<span data-ttu-id="87fa6-132">**16**</span><span class="sxs-lookup"><span data-stu-id="87fa6-132">**16**</span></span>
</dt> <dd>

<span data-ttu-id="87fa6-133">Le fichier de démarrage spécifié n’est pas valide.</span><span class="sxs-lookup"><span data-stu-id="87fa6-133">The start file specified was not valid.</span></span>

</dd> <dt>

<span data-ttu-id="87fa6-134">**17**</span><span class="sxs-lookup"><span data-stu-id="87fa6-134">**17**</span></span>
</dt> <dd>

<span data-ttu-id="87fa6-135">Un privilège requis pour l’opération n’est pas conservé.</span><span class="sxs-lookup"><span data-stu-id="87fa6-135">A privilege required for the operation is not held.</span></span>

</dd> <dt>

<span data-ttu-id="87fa6-136">**21**</span><span class="sxs-lookup"><span data-stu-id="87fa6-136">**21**</span></span>
</dt> <dd>

<span data-ttu-id="87fa6-137">Un paramètre spécifié n’est pas valide.</span><span class="sxs-lookup"><span data-stu-id="87fa6-137">A parameter specified is not valid.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="87fa6-138">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="87fa6-138">Requirements</span></span>



| <span data-ttu-id="87fa6-139">Condition requise</span><span class="sxs-lookup"><span data-stu-id="87fa6-139">Requirement</span></span> | <span data-ttu-id="87fa6-140">Valeur</span><span class="sxs-lookup"><span data-stu-id="87fa6-140">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="87fa6-141">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="87fa6-141">Minimum supported client</span></span><br/> | <span data-ttu-id="87fa6-142">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="87fa6-142">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="87fa6-143">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="87fa6-143">Minimum supported server</span></span><br/> | <span data-ttu-id="87fa6-144">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="87fa6-144">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="87fa6-145">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="87fa6-145">Namespace</span></span><br/>                | <span data-ttu-id="87fa6-146">\\Cimv2 racine</span><span class="sxs-lookup"><span data-stu-id="87fa6-146">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="87fa6-147">MOF</span><span class="sxs-lookup"><span data-stu-id="87fa6-147">MOF</span></span><br/>                      | <dl> <span data-ttu-id="87fa6-148"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="87fa6-148"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="87fa6-149">DLL</span><span class="sxs-lookup"><span data-stu-id="87fa6-149">DLL</span></span><br/>                      | <dl> <span data-ttu-id="87fa6-150"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="87fa6-150"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="87fa6-151">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="87fa6-151">See also</span></span>

<dl> <dt>

<span data-ttu-id="87fa6-152">[Classes du système d’exploitation](/previous-versions//aa392727(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="87fa6-152">[Operating System Classes](/previous-versions//aa392727(v=vs.85))</span></span>
</dt> <dt>

[<span data-ttu-id="87fa6-153">**\_Fichier d’échange Win32**</span><span class="sxs-lookup"><span data-stu-id="87fa6-153">**Win32\_PageFile**</span></span>](win32-pagefile.md)
</dt> </dl>

 

