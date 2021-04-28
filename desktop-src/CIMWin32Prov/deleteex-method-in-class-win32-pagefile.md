---
description: 'Méthode DeleteEx de la classe Win32_PageFile : supprime le fichier d’échange logique (ou le répertoire) spécifié dans le chemin d’accès de l’objet.'
ms.assetid: ea31f92a-94b9-4d4d-abd9-6c304ac5caee
ms.tgt_platform: multiple
title: Méthode DeleteEx de la classe Win32_PageFile
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_PageFile.DeleteEx
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: 34e27e80c3cfaea352ee97ad29aed0b7ca358546
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108097047"
---
# <a name="deleteex-method-of-the-win32_pagefile-class"></a><span data-ttu-id="57a96-103">Méthode DeleteEx de la \_ classe du fichier d’échange Win32</span><span class="sxs-lookup"><span data-stu-id="57a96-103">DeleteEx method of the Win32\_PageFile class</span></span>

<span data-ttu-id="57a96-104">La méthode de [classe WMI](/windows/desktop/WmiSdk/retrieving-a-class) **DeleteEx** supprime le fichier d’échange logique (ou le répertoire) spécifié dans le chemin d’accès de l’objet.</span><span class="sxs-lookup"><span data-stu-id="57a96-104">The **DeleteEx** [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) method deletes the logical paging file (or directory) specified in the object path.</span></span> <span data-ttu-id="57a96-105">**DeleteEx** est une version étendue de la méthode [**Delete**](delete-method-in-class-win32-directory.md) .</span><span class="sxs-lookup"><span data-stu-id="57a96-105">**DeleteEx** is an extended version of the [**Delete**](delete-method-in-class-win32-directory.md) method.</span></span>

<span data-ttu-id="57a96-106">Cette rubrique utilise la syntaxe format MOF (MOF).</span><span class="sxs-lookup"><span data-stu-id="57a96-106">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="57a96-107">Pour plus d’informations sur l’utilisation de cette méthode, consultez [appel d’une méthode](/windows/desktop/WmiSdk/calling-a-method).</span><span class="sxs-lookup"><span data-stu-id="57a96-107">For more information about using this method, see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="57a96-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="57a96-108">Syntax</span></span>


```mof
uint32 DeleteEx(
  [out]          string StopFileName,
  [in, optional] string StartFileName
);
```



## <a name="parameters"></a><span data-ttu-id="57a96-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="57a96-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="57a96-110">*StopFileName* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="57a96-110">*StopFileName* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="57a96-111">Nom du fichier ou du répertoire dans lequel la méthode **DeleteEx** a échoué.</span><span class="sxs-lookup"><span data-stu-id="57a96-111">Name of the file or directory where the **DeleteEx** method failed.</span></span> <span data-ttu-id="57a96-112">Ce paramètre a la **valeur null** si la méthode est réussie.</span><span class="sxs-lookup"><span data-stu-id="57a96-112">This parameter is **null** if the method succeeds.</span></span>

</dd> <dt>

<span data-ttu-id="57a96-113">*StartFileName* \[ dans, facultatif\]</span><span class="sxs-lookup"><span data-stu-id="57a96-113">*StartFileName* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="57a96-114">Nomme le fichier ou le répertoire enfant à utiliser comme point de départ pour **DeleteEx**.</span><span class="sxs-lookup"><span data-stu-id="57a96-114">Names the child file or directory to use as a starting point for **DeleteEx**.</span></span> <span data-ttu-id="57a96-115">Le paramètre *StartFileName* est généralement le paramètre *StopFileName* qui spécifie le fichier ou le répertoire dans lequel une erreur s’est produite à partir de l’appel de méthode précédent.</span><span class="sxs-lookup"><span data-stu-id="57a96-115">The *StartFileName* parameter is typically the *StopFileName* parameter that specifies the file or directory at which an error occurred from the previous method call.</span></span> <span data-ttu-id="57a96-116">Si ce paramètre a la **valeur null**, l’opération est effectuée sur le fichier ou le répertoire spécifié dans l’appel de ExecMethod.</span><span class="sxs-lookup"><span data-stu-id="57a96-116">If this parameter is **NULL**, the operation is performed on the file or directory specified in the ExecMethod call.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="57a96-117">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="57a96-117">Return value</span></span>

<span data-ttu-id="57a96-118">Retourne la valeur 0 (zéro) si le fichier a été supprimé avec succès, et tout autre nombre pour indiquer une erreur.</span><span class="sxs-lookup"><span data-stu-id="57a96-118">Returns a value of 0 (zero) if the file was successfully deleted, and any other number to indicate an error.</span></span>

<dl> <dt>

<span data-ttu-id="57a96-119">**0**</span><span class="sxs-lookup"><span data-stu-id="57a96-119">**0**</span></span>
</dt> <dd>

<span data-ttu-id="57a96-120">La demande a abouti.</span><span class="sxs-lookup"><span data-stu-id="57a96-120">The request was successful.</span></span>

</dd> <dt>

<span data-ttu-id="57a96-121">**2**</span><span class="sxs-lookup"><span data-stu-id="57a96-121">**2**</span></span>
</dt> <dd>

<span data-ttu-id="57a96-122">L’accès a été refusé.</span><span class="sxs-lookup"><span data-stu-id="57a96-122">Access was denied.</span></span>

</dd> <dt>

<span data-ttu-id="57a96-123">**8**</span><span class="sxs-lookup"><span data-stu-id="57a96-123">**8**</span></span>
</dt> <dd>

<span data-ttu-id="57a96-124">Une erreur non spécifiée s’est produite.</span><span class="sxs-lookup"><span data-stu-id="57a96-124">An unspecified failure occurred.</span></span>

</dd> <dt>

<span data-ttu-id="57a96-125">**9**</span><span class="sxs-lookup"><span data-stu-id="57a96-125">**9**</span></span>
</dt> <dd>

<span data-ttu-id="57a96-126">Le nom spécifié n’est pas valide.</span><span class="sxs-lookup"><span data-stu-id="57a96-126">The name specified was not valid.</span></span>

</dd> <dt>

<span data-ttu-id="57a96-127">**10**</span><span class="sxs-lookup"><span data-stu-id="57a96-127">**10**</span></span>
</dt> <dd>

<span data-ttu-id="57a96-128">L’objet spécifié existe déjà.</span><span class="sxs-lookup"><span data-stu-id="57a96-128">The object specified already exists.</span></span>

</dd> <dt>

<span data-ttu-id="57a96-129">**11**</span><span class="sxs-lookup"><span data-stu-id="57a96-129">**11**</span></span>
</dt> <dd>

<span data-ttu-id="57a96-130">Le système de fichiers n’est pas NTFS.</span><span class="sxs-lookup"><span data-stu-id="57a96-130">The file system is not NTFS.</span></span>

</dd> <dt>

<span data-ttu-id="57a96-131">**12**</span><span class="sxs-lookup"><span data-stu-id="57a96-131">**12**</span></span>
</dt> <dd>

<span data-ttu-id="57a96-132">La plateforme n’est pas Windows.</span><span class="sxs-lookup"><span data-stu-id="57a96-132">The platform is not Windows.</span></span>

</dd> <dt>

<span data-ttu-id="57a96-133">**13**</span><span class="sxs-lookup"><span data-stu-id="57a96-133">**13**</span></span>
</dt> <dd>

<span data-ttu-id="57a96-134">Le lecteur n’est pas le même.</span><span class="sxs-lookup"><span data-stu-id="57a96-134">The drive is not the same.</span></span>

</dd> <dt>

<span data-ttu-id="57a96-135">**14**</span><span class="sxs-lookup"><span data-stu-id="57a96-135">**14**</span></span>
</dt> <dd>

<span data-ttu-id="57a96-136">Le répertoire n'est pas vide.</span><span class="sxs-lookup"><span data-stu-id="57a96-136">The directory is not empty.</span></span>

</dd> <dt>

<span data-ttu-id="57a96-137">**15**</span><span class="sxs-lookup"><span data-stu-id="57a96-137">**15**</span></span>
</dt> <dd>

<span data-ttu-id="57a96-138">Une violation de partage s’est produite.</span><span class="sxs-lookup"><span data-stu-id="57a96-138">There has been a sharing violation.</span></span>

</dd> <dt>

<span data-ttu-id="57a96-139">**16**</span><span class="sxs-lookup"><span data-stu-id="57a96-139">**16**</span></span>
</dt> <dd>

<span data-ttu-id="57a96-140">Le fichier de démarrage spécifié n’est pas valide.</span><span class="sxs-lookup"><span data-stu-id="57a96-140">The start file specified was not valid.</span></span>

</dd> <dt>

<span data-ttu-id="57a96-141">**17**</span><span class="sxs-lookup"><span data-stu-id="57a96-141">**17**</span></span>
</dt> <dd>

<span data-ttu-id="57a96-142">Un privilège requis pour l’opération n’est pas conservé.</span><span class="sxs-lookup"><span data-stu-id="57a96-142">A privilege required for the operation is not held.</span></span>

</dd> <dt>

<span data-ttu-id="57a96-143">**21**</span><span class="sxs-lookup"><span data-stu-id="57a96-143">**21**</span></span>
</dt> <dd>

<span data-ttu-id="57a96-144">Un paramètre spécifié n’est pas valide.</span><span class="sxs-lookup"><span data-stu-id="57a96-144">A parameter specified is not valid.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="57a96-145">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="57a96-145">Requirements</span></span>



| <span data-ttu-id="57a96-146">Condition requise</span><span class="sxs-lookup"><span data-stu-id="57a96-146">Requirement</span></span> | <span data-ttu-id="57a96-147">Valeur</span><span class="sxs-lookup"><span data-stu-id="57a96-147">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="57a96-148">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="57a96-148">Minimum supported client</span></span><br/> | <span data-ttu-id="57a96-149">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="57a96-149">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="57a96-150">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="57a96-150">Minimum supported server</span></span><br/> | <span data-ttu-id="57a96-151">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="57a96-151">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="57a96-152">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="57a96-152">Namespace</span></span><br/>                | <span data-ttu-id="57a96-153">\\Cimv2 racine</span><span class="sxs-lookup"><span data-stu-id="57a96-153">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="57a96-154">MOF</span><span class="sxs-lookup"><span data-stu-id="57a96-154">MOF</span></span><br/>                      | <dl> <span data-ttu-id="57a96-155"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="57a96-155"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="57a96-156">DLL</span><span class="sxs-lookup"><span data-stu-id="57a96-156">DLL</span></span><br/>                      | <dl> <span data-ttu-id="57a96-157"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="57a96-157"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="57a96-158">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="57a96-158">See also</span></span>

<dl> <dt>

<span data-ttu-id="57a96-159">[Classes du système d’exploitation](/previous-versions//aa392727(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="57a96-159">[Operating System Classes](/previous-versions//aa392727(v=vs.85))</span></span>
</dt> <dt>

[<span data-ttu-id="57a96-160">**\_Fichier d’échange Win32**</span><span class="sxs-lookup"><span data-stu-id="57a96-160">**Win32\_PageFile**</span></span>](win32-pagefile.md)
</dt> </dl>

 

