---
description: 'Méthode Delete de la classe Win32_PageFile : supprime le fichier d’échange logique (ou le répertoire) spécifié dans le chemin d’accès de l’objet.'
ms.assetid: cc36d621-597e-4343-8bf6-bfca7fa29276
ms.tgt_platform: multiple
title: Méthode Delete de la classe Win32_PageFile
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_PageFile.Delete
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: 8b35751633387f3db1d7dccbf13694f56717a1d3
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108089587"
---
# <a name="delete-method-of-the-win32_pagefile-class"></a><span data-ttu-id="f3c33-103">Méthode Delete de la \_ classe pagefile Win32</span><span class="sxs-lookup"><span data-stu-id="f3c33-103">Delete method of the Win32\_PageFile class</span></span>

<span data-ttu-id="f3c33-104">La méthode **Delete** [WMI Class](/windows/desktop/WmiSdk/retrieving-a-class) supprime le fichier d’échange logique (ou le répertoire) spécifié dans le chemin d’accès de l’objet.</span><span class="sxs-lookup"><span data-stu-id="f3c33-104">The **Delete** [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) method deletes the logical paging file (or directory) specified in the object path.</span></span>

<span data-ttu-id="f3c33-105">Cette rubrique utilise la syntaxe format MOF (MOF).</span><span class="sxs-lookup"><span data-stu-id="f3c33-105">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="f3c33-106">Pour plus d’informations sur l’utilisation de cette méthode, consultez [appel d’une méthode](/windows/desktop/WmiSdk/calling-a-method).</span><span class="sxs-lookup"><span data-stu-id="f3c33-106">For more information about using this method, see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="f3c33-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="f3c33-107">Syntax</span></span>


```mof
uint32 Delete();
```



## <a name="parameters"></a><span data-ttu-id="f3c33-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="f3c33-108">Parameters</span></span>

<span data-ttu-id="f3c33-109">Cette méthode n’a aucun paramètre.</span><span class="sxs-lookup"><span data-stu-id="f3c33-109">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="f3c33-110">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="f3c33-110">Return value</span></span>

<span data-ttu-id="f3c33-111">Retourne la valeur 0 (zéro) si le fichier a été supprimé avec succès, et tout autre nombre pour indiquer une erreur.</span><span class="sxs-lookup"><span data-stu-id="f3c33-111">Returns a value of 0 (zero) if the file was successfully deleted, and any other number to indicate an error.</span></span>

<dl> <dt>

<span data-ttu-id="f3c33-112">**0**</span><span class="sxs-lookup"><span data-stu-id="f3c33-112">**0**</span></span>
</dt> <dd>

<span data-ttu-id="f3c33-113">La demande a abouti.</span><span class="sxs-lookup"><span data-stu-id="f3c33-113">The request was successful.</span></span>

</dd> <dt>

<span data-ttu-id="f3c33-114">**2**</span><span class="sxs-lookup"><span data-stu-id="f3c33-114">**2**</span></span>
</dt> <dd>

<span data-ttu-id="f3c33-115">L’accès a été refusé.</span><span class="sxs-lookup"><span data-stu-id="f3c33-115">Access was denied.</span></span>

</dd> <dt>

<span data-ttu-id="f3c33-116">**8**</span><span class="sxs-lookup"><span data-stu-id="f3c33-116">**8**</span></span>
</dt> <dd>

<span data-ttu-id="f3c33-117">Une erreur non spécifiée s’est produite.</span><span class="sxs-lookup"><span data-stu-id="f3c33-117">An unspecified failure occurred.</span></span>

</dd> <dt>

<span data-ttu-id="f3c33-118">**9**</span><span class="sxs-lookup"><span data-stu-id="f3c33-118">**9**</span></span>
</dt> <dd>

<span data-ttu-id="f3c33-119">Le nom spécifié n’est pas valide.</span><span class="sxs-lookup"><span data-stu-id="f3c33-119">The name specified was not valid.</span></span>

</dd> <dt>

<span data-ttu-id="f3c33-120">**10**</span><span class="sxs-lookup"><span data-stu-id="f3c33-120">**10**</span></span>
</dt> <dd>

<span data-ttu-id="f3c33-121">L’objet spécifié existe déjà.</span><span class="sxs-lookup"><span data-stu-id="f3c33-121">The object specified already exists.</span></span>

</dd> <dt>

<span data-ttu-id="f3c33-122">**11**</span><span class="sxs-lookup"><span data-stu-id="f3c33-122">**11**</span></span>
</dt> <dd>

<span data-ttu-id="f3c33-123">Le système de fichiers n’est pas NTFS.</span><span class="sxs-lookup"><span data-stu-id="f3c33-123">The file system is not NTFS.</span></span>

</dd> <dt>

<span data-ttu-id="f3c33-124">**12**</span><span class="sxs-lookup"><span data-stu-id="f3c33-124">**12**</span></span>
</dt> <dd>

<span data-ttu-id="f3c33-125">La plateforme n’est pas Windows.</span><span class="sxs-lookup"><span data-stu-id="f3c33-125">The platform is not Windows.</span></span>

</dd> <dt>

<span data-ttu-id="f3c33-126">**13**</span><span class="sxs-lookup"><span data-stu-id="f3c33-126">**13**</span></span>
</dt> <dd>

<span data-ttu-id="f3c33-127">Le lecteur n’est pas le même.</span><span class="sxs-lookup"><span data-stu-id="f3c33-127">The drive is not the same.</span></span>

</dd> <dt>

<span data-ttu-id="f3c33-128">**14**</span><span class="sxs-lookup"><span data-stu-id="f3c33-128">**14**</span></span>
</dt> <dd>

<span data-ttu-id="f3c33-129">Le répertoire n'est pas vide.</span><span class="sxs-lookup"><span data-stu-id="f3c33-129">The directory is not empty.</span></span>

</dd> <dt>

<span data-ttu-id="f3c33-130">**15**</span><span class="sxs-lookup"><span data-stu-id="f3c33-130">**15**</span></span>
</dt> <dd>

<span data-ttu-id="f3c33-131">Une violation de partage s’est produite.</span><span class="sxs-lookup"><span data-stu-id="f3c33-131">There has been a sharing violation.</span></span>

</dd> <dt>

<span data-ttu-id="f3c33-132">**16**</span><span class="sxs-lookup"><span data-stu-id="f3c33-132">**16**</span></span>
</dt> <dd>

<span data-ttu-id="f3c33-133">Le fichier de démarrage spécifié n’est pas valide.</span><span class="sxs-lookup"><span data-stu-id="f3c33-133">The start file specified was not valid.</span></span>

</dd> <dt>

<span data-ttu-id="f3c33-134">**17**</span><span class="sxs-lookup"><span data-stu-id="f3c33-134">**17**</span></span>
</dt> <dd>

<span data-ttu-id="f3c33-135">Un privilège requis pour l’opération n’est pas conservé.</span><span class="sxs-lookup"><span data-stu-id="f3c33-135">A privilege required for the operation is not held.</span></span>

</dd> <dt>

<span data-ttu-id="f3c33-136">**21**</span><span class="sxs-lookup"><span data-stu-id="f3c33-136">**21**</span></span>
</dt> <dd>

<span data-ttu-id="f3c33-137">Un paramètre spécifié n’est pas valide.</span><span class="sxs-lookup"><span data-stu-id="f3c33-137">A parameter specified is not valid.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="f3c33-138">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="f3c33-138">Requirements</span></span>



| <span data-ttu-id="f3c33-139">Condition requise</span><span class="sxs-lookup"><span data-stu-id="f3c33-139">Requirement</span></span> | <span data-ttu-id="f3c33-140">Valeur</span><span class="sxs-lookup"><span data-stu-id="f3c33-140">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="f3c33-141">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="f3c33-141">Minimum supported client</span></span><br/> | <span data-ttu-id="f3c33-142">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="f3c33-142">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="f3c33-143">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="f3c33-143">Minimum supported server</span></span><br/> | <span data-ttu-id="f3c33-144">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="f3c33-144">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="f3c33-145">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="f3c33-145">Namespace</span></span><br/>                | <span data-ttu-id="f3c33-146">\\Cimv2 racine</span><span class="sxs-lookup"><span data-stu-id="f3c33-146">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="f3c33-147">MOF</span><span class="sxs-lookup"><span data-stu-id="f3c33-147">MOF</span></span><br/>                      | <dl> <span data-ttu-id="f3c33-148"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="f3c33-148"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="f3c33-149">DLL</span><span class="sxs-lookup"><span data-stu-id="f3c33-149">DLL</span></span><br/>                      | <dl> <span data-ttu-id="f3c33-150"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="f3c33-150"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f3c33-151">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="f3c33-151">See also</span></span>

<dl> <dt>

<span data-ttu-id="f3c33-152">[Classes du système d’exploitation](/previous-versions//aa392727(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="f3c33-152">[Operating System Classes](/previous-versions//aa392727(v=vs.85))</span></span>
</dt> <dt>

[<span data-ttu-id="f3c33-153">**\_Fichier d’échange Win32**</span><span class="sxs-lookup"><span data-stu-id="f3c33-153">**Win32\_PageFile**</span></span>](win32-pagefile.md)
</dt> </dl>

 

