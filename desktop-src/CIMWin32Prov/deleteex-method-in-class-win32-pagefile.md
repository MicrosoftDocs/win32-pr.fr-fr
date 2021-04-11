---
description: Supprime le fichier d’échange logique (ou le répertoire) spécifié dans le chemin d’accès de l’objet.
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
ms.openlocfilehash: 2f62875313f6be432ab191fc91bbac381627de3c
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104110518"
---
# <a name="deleteex-method-of-the-win32_pagefile-class"></a><span data-ttu-id="f338c-103">Méthode DeleteEx de la \_ classe du fichier d’échange Win32</span><span class="sxs-lookup"><span data-stu-id="f338c-103">DeleteEx method of the Win32\_PageFile class</span></span>

<span data-ttu-id="f338c-104">La méthode de [classe WMI](/windows/desktop/WmiSdk/retrieving-a-class) **DeleteEx** supprime le fichier d’échange logique (ou le répertoire) spécifié dans le chemin d’accès de l’objet.</span><span class="sxs-lookup"><span data-stu-id="f338c-104">The **DeleteEx** [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) method deletes the logical paging file (or directory) specified in the object path.</span></span> <span data-ttu-id="f338c-105">**DeleteEx** est une version étendue de la méthode [**Delete**](delete-method-in-class-win32-directory.md) .</span><span class="sxs-lookup"><span data-stu-id="f338c-105">**DeleteEx** is an extended version of the [**Delete**](delete-method-in-class-win32-directory.md) method.</span></span>

<span data-ttu-id="f338c-106">Cette rubrique utilise la syntaxe format MOF (MOF).</span><span class="sxs-lookup"><span data-stu-id="f338c-106">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="f338c-107">Pour plus d’informations sur l’utilisation de cette méthode, consultez [appel d’une méthode](/windows/desktop/WmiSdk/calling-a-method).</span><span class="sxs-lookup"><span data-stu-id="f338c-107">For more information about using this method, see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="f338c-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="f338c-108">Syntax</span></span>


```mof
uint32 DeleteEx(
  [out]          string StopFileName,
  [in, optional] string StartFileName
);
```



## <a name="parameters"></a><span data-ttu-id="f338c-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="f338c-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f338c-110">*StopFileName* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="f338c-110">*StopFileName* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="f338c-111">Nom du fichier ou du répertoire dans lequel la méthode **DeleteEx** a échoué.</span><span class="sxs-lookup"><span data-stu-id="f338c-111">Name of the file or directory where the **DeleteEx** method failed.</span></span> <span data-ttu-id="f338c-112">Ce paramètre a la **valeur null** si la méthode est réussie.</span><span class="sxs-lookup"><span data-stu-id="f338c-112">This parameter is **null** if the method succeeds.</span></span>

</dd> <dt>

<span data-ttu-id="f338c-113">*StartFileName* \[ dans, facultatif\]</span><span class="sxs-lookup"><span data-stu-id="f338c-113">*StartFileName* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="f338c-114">Nomme le fichier ou le répertoire enfant à utiliser comme point de départ pour **DeleteEx**.</span><span class="sxs-lookup"><span data-stu-id="f338c-114">Names the child file or directory to use as a starting point for **DeleteEx**.</span></span> <span data-ttu-id="f338c-115">Le paramètre *StartFileName* est généralement le paramètre *StopFileName* qui spécifie le fichier ou le répertoire dans lequel une erreur s’est produite à partir de l’appel de méthode précédent.</span><span class="sxs-lookup"><span data-stu-id="f338c-115">The *StartFileName* parameter is typically the *StopFileName* parameter that specifies the file or directory at which an error occurred from the previous method call.</span></span> <span data-ttu-id="f338c-116">Si ce paramètre a la **valeur null**, l’opération est effectuée sur le fichier ou le répertoire spécifié dans l’appel de ExecMethod.</span><span class="sxs-lookup"><span data-stu-id="f338c-116">If this parameter is **NULL**, the operation is performed on the file or directory specified in the ExecMethod call.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f338c-117">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="f338c-117">Return value</span></span>

<span data-ttu-id="f338c-118">Retourne la valeur 0 (zéro) si le fichier a été supprimé avec succès, et tout autre nombre pour indiquer une erreur.</span><span class="sxs-lookup"><span data-stu-id="f338c-118">Returns a value of 0 (zero) if the file was successfully deleted, and any other number to indicate an error.</span></span>

<dl> <dt>

<span data-ttu-id="f338c-119">**0**</span><span class="sxs-lookup"><span data-stu-id="f338c-119">**0**</span></span>
</dt> <dd>

<span data-ttu-id="f338c-120">La demande a abouti.</span><span class="sxs-lookup"><span data-stu-id="f338c-120">The request was successful.</span></span>

</dd> <dt>

<span data-ttu-id="f338c-121">**2**</span><span class="sxs-lookup"><span data-stu-id="f338c-121">**2**</span></span>
</dt> <dd>

<span data-ttu-id="f338c-122">L’accès a été refusé.</span><span class="sxs-lookup"><span data-stu-id="f338c-122">Access was denied.</span></span>

</dd> <dt>

<span data-ttu-id="f338c-123">**8**</span><span class="sxs-lookup"><span data-stu-id="f338c-123">**8**</span></span>
</dt> <dd>

<span data-ttu-id="f338c-124">Une erreur non spécifiée s’est produite.</span><span class="sxs-lookup"><span data-stu-id="f338c-124">An unspecified failure occurred.</span></span>

</dd> <dt>

<span data-ttu-id="f338c-125">**9**</span><span class="sxs-lookup"><span data-stu-id="f338c-125">**9**</span></span>
</dt> <dd>

<span data-ttu-id="f338c-126">Le nom spécifié n’est pas valide.</span><span class="sxs-lookup"><span data-stu-id="f338c-126">The name specified was not valid.</span></span>

</dd> <dt>

<span data-ttu-id="f338c-127">**10**</span><span class="sxs-lookup"><span data-stu-id="f338c-127">**10**</span></span>
</dt> <dd>

<span data-ttu-id="f338c-128">L’objet spécifié existe déjà.</span><span class="sxs-lookup"><span data-stu-id="f338c-128">The object specified already exists.</span></span>

</dd> <dt>

<span data-ttu-id="f338c-129">**11**</span><span class="sxs-lookup"><span data-stu-id="f338c-129">**11**</span></span>
</dt> <dd>

<span data-ttu-id="f338c-130">Le système de fichiers n’est pas NTFS.</span><span class="sxs-lookup"><span data-stu-id="f338c-130">The file system is not NTFS.</span></span>

</dd> <dt>

<span data-ttu-id="f338c-131">**12**</span><span class="sxs-lookup"><span data-stu-id="f338c-131">**12**</span></span>
</dt> <dd>

<span data-ttu-id="f338c-132">La plateforme n’est pas Windows.</span><span class="sxs-lookup"><span data-stu-id="f338c-132">The platform is not Windows.</span></span>

</dd> <dt>

<span data-ttu-id="f338c-133">**13**</span><span class="sxs-lookup"><span data-stu-id="f338c-133">**13**</span></span>
</dt> <dd>

<span data-ttu-id="f338c-134">Le lecteur n’est pas le même.</span><span class="sxs-lookup"><span data-stu-id="f338c-134">The drive is not the same.</span></span>

</dd> <dt>

<span data-ttu-id="f338c-135">**14**</span><span class="sxs-lookup"><span data-stu-id="f338c-135">**14**</span></span>
</dt> <dd>

<span data-ttu-id="f338c-136">Le répertoire n'est pas vide.</span><span class="sxs-lookup"><span data-stu-id="f338c-136">The directory is not empty.</span></span>

</dd> <dt>

<span data-ttu-id="f338c-137">**15**</span><span class="sxs-lookup"><span data-stu-id="f338c-137">**15**</span></span>
</dt> <dd>

<span data-ttu-id="f338c-138">Une violation de partage s’est produite.</span><span class="sxs-lookup"><span data-stu-id="f338c-138">There has been a sharing violation.</span></span>

</dd> <dt>

<span data-ttu-id="f338c-139">**16**</span><span class="sxs-lookup"><span data-stu-id="f338c-139">**16**</span></span>
</dt> <dd>

<span data-ttu-id="f338c-140">Le fichier de démarrage spécifié n’est pas valide.</span><span class="sxs-lookup"><span data-stu-id="f338c-140">The start file specified was not valid.</span></span>

</dd> <dt>

<span data-ttu-id="f338c-141">**17**</span><span class="sxs-lookup"><span data-stu-id="f338c-141">**17**</span></span>
</dt> <dd>

<span data-ttu-id="f338c-142">Un privilège requis pour l’opération n’est pas conservé.</span><span class="sxs-lookup"><span data-stu-id="f338c-142">A privilege required for the operation is not held.</span></span>

</dd> <dt>

<span data-ttu-id="f338c-143">**21**</span><span class="sxs-lookup"><span data-stu-id="f338c-143">**21**</span></span>
</dt> <dd>

<span data-ttu-id="f338c-144">Un paramètre spécifié n’est pas valide.</span><span class="sxs-lookup"><span data-stu-id="f338c-144">A parameter specified is not valid.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="f338c-145">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="f338c-145">Requirements</span></span>



| <span data-ttu-id="f338c-146">Condition requise</span><span class="sxs-lookup"><span data-stu-id="f338c-146">Requirement</span></span> | <span data-ttu-id="f338c-147">Valeur</span><span class="sxs-lookup"><span data-stu-id="f338c-147">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="f338c-148">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="f338c-148">Minimum supported client</span></span><br/> | <span data-ttu-id="f338c-149">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="f338c-149">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="f338c-150">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="f338c-150">Minimum supported server</span></span><br/> | <span data-ttu-id="f338c-151">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="f338c-151">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="f338c-152">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="f338c-152">Namespace</span></span><br/>                | <span data-ttu-id="f338c-153">\\Cimv2 racine</span><span class="sxs-lookup"><span data-stu-id="f338c-153">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="f338c-154">MOF</span><span class="sxs-lookup"><span data-stu-id="f338c-154">MOF</span></span><br/>                      | <dl> <span data-ttu-id="f338c-155"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="f338c-155"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="f338c-156">DLL</span><span class="sxs-lookup"><span data-stu-id="f338c-156">DLL</span></span><br/>                      | <dl> <span data-ttu-id="f338c-157"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="f338c-157"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f338c-158">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="f338c-158">See also</span></span>

<dl> <dt>

<span data-ttu-id="f338c-159">[Classes du système d’exploitation](/previous-versions//aa392727(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="f338c-159">[Operating System Classes](/previous-versions//aa392727(v=vs.85))</span></span>
</dt> <dt>

[<span data-ttu-id="f338c-160">**\_Fichier d’échange Win32**</span><span class="sxs-lookup"><span data-stu-id="f338c-160">**Win32\_PageFile**</span></span>](win32-pagefile.md)
</dt> </dl>

 

