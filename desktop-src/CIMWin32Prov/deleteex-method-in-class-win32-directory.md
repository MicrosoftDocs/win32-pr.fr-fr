---
description: La méthode de classe WMI DeleteEx supprime le fichier logique (ou le répertoire) spécifié dans le chemin d’accès de l’objet. DeleteEx est une version étendue de la méthode Delete.
ms.assetid: 6e5447c1-4d71-4a51-a1e0-b5785c13dfd2
ms.tgt_platform: multiple
title: Méthode DeleteEx de la classe Win32_Directory
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_Directory.DeleteEx
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: ac23a4013053d252aec49b8b7be4aae62c41c8e1
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103950564"
---
# <a name="deleteex-method-of-the-win32_directory-class"></a><span data-ttu-id="d2b1c-104">Méthode DeleteEx de la \_ classe Directory Win32</span><span class="sxs-lookup"><span data-stu-id="d2b1c-104">DeleteEx method of the Win32\_Directory class</span></span>

<span data-ttu-id="d2b1c-105">La méthode de [classe WMI](/windows/desktop/WmiSdk/retrieving-a-class) **DeleteEx** supprime le fichier logique (ou le répertoire) spécifié dans le chemin d’accès de l’objet.</span><span class="sxs-lookup"><span data-stu-id="d2b1c-105">The **DeleteEx** [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) method will delete the logical file (or directory) specified in the object path.</span></span> <span data-ttu-id="d2b1c-106">**DeleteEx** est une version étendue de la méthode [**Delete**](delete-method-in-class-win32-directory.md) .</span><span class="sxs-lookup"><span data-stu-id="d2b1c-106">**DeleteEx** is an extended version of the [**Delete**](delete-method-in-class-win32-directory.md) method.</span></span>

<span data-ttu-id="d2b1c-107">Cette rubrique utilise la syntaxe format MOF (MOF).</span><span class="sxs-lookup"><span data-stu-id="d2b1c-107">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="d2b1c-108">Pour plus d’informations sur l’utilisation de cette méthode, consultez [appel d’une méthode](/windows/desktop/WmiSdk/calling-a-method).</span><span class="sxs-lookup"><span data-stu-id="d2b1c-108">For more information about using this method, see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="d2b1c-109">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="d2b1c-109">Syntax</span></span>


```mof
uint32 DeleteEx(
  [out]          string StopFileName,
  [in, optional] string StartFileName
);
```



## <a name="parameters"></a><span data-ttu-id="d2b1c-110">Paramètres</span><span class="sxs-lookup"><span data-stu-id="d2b1c-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d2b1c-111">*StopFileName* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="d2b1c-111">*StopFileName* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="d2b1c-112">Nom du fichier ou du répertoire dans lequel la méthode **DeleteEx** a échoué.</span><span class="sxs-lookup"><span data-stu-id="d2b1c-112">Name of the file or directory where the **DeleteEx** method failed.</span></span> <span data-ttu-id="d2b1c-113">Ce paramètre a la **valeur null** si la méthode est réussie.</span><span class="sxs-lookup"><span data-stu-id="d2b1c-113">This parameter will be **null** if the method succeeds.</span></span>

</dd> <dt>

<span data-ttu-id="d2b1c-114">*StartFileName* \[ dans, facultatif\]</span><span class="sxs-lookup"><span data-stu-id="d2b1c-114">*StartFileName* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="d2b1c-115">Nomme le fichier ou le répertoire enfant à utiliser comme point de départ pour **DeleteEx**.</span><span class="sxs-lookup"><span data-stu-id="d2b1c-115">Names the child file or directory to use as a starting point for **DeleteEx**.</span></span> <span data-ttu-id="d2b1c-116">Le paramètre *StartFileName* est généralement le paramètre *StopFileName* spécifiant le fichier ou le répertoire dans lequel une erreur s’est produite à partir de l’appel de méthode précédent.</span><span class="sxs-lookup"><span data-stu-id="d2b1c-116">The *StartFileName* parameter is typically the *StopFileName* parameter specifying the file or directory at which an error occurred from the previous method call.</span></span> <span data-ttu-id="d2b1c-117">Si ce paramètre a la **valeur null**, l’opération est effectuée sur le fichier ou le répertoire spécifié dans l’appel de ExecMethod.</span><span class="sxs-lookup"><span data-stu-id="d2b1c-117">If this parameter is **NULL**, the operation is performed on the file or directory specified in the ExecMethod call.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d2b1c-118">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="d2b1c-118">Return value</span></span>

<span data-ttu-id="d2b1c-119">Retourne la valeur 0 (zéro) si le fichier a été supprimé avec succès, et tout autre nombre pour indiquer une erreur.</span><span class="sxs-lookup"><span data-stu-id="d2b1c-119">Returns a value of 0 (zero) if the file was successfully deleted, and any other number to indicate an error.</span></span>

<dl> <dt>

<span data-ttu-id="d2b1c-120">**0**</span><span class="sxs-lookup"><span data-stu-id="d2b1c-120">**0**</span></span>
</dt> <dd>

<span data-ttu-id="d2b1c-121">La demande a abouti.</span><span class="sxs-lookup"><span data-stu-id="d2b1c-121">The request was successful.</span></span>

</dd> <dt>

<span data-ttu-id="d2b1c-122">**2**</span><span class="sxs-lookup"><span data-stu-id="d2b1c-122">**2**</span></span>
</dt> <dd>

<span data-ttu-id="d2b1c-123">L’accès a été refusé.</span><span class="sxs-lookup"><span data-stu-id="d2b1c-123">Access was denied.</span></span>

</dd> <dt>

<span data-ttu-id="d2b1c-124">**8**</span><span class="sxs-lookup"><span data-stu-id="d2b1c-124">**8**</span></span>
</dt> <dd>

<span data-ttu-id="d2b1c-125">Une erreur non spécifiée s’est produite.</span><span class="sxs-lookup"><span data-stu-id="d2b1c-125">An unspecified failure occurred.</span></span>

</dd> <dt>

<span data-ttu-id="d2b1c-126">**9**</span><span class="sxs-lookup"><span data-stu-id="d2b1c-126">**9**</span></span>
</dt> <dd>

<span data-ttu-id="d2b1c-127">Le nom spécifié n’est pas valide.</span><span class="sxs-lookup"><span data-stu-id="d2b1c-127">The name specified was not valid.</span></span>

</dd> <dt>

<span data-ttu-id="d2b1c-128">**10**</span><span class="sxs-lookup"><span data-stu-id="d2b1c-128">**10**</span></span>
</dt> <dd>

<span data-ttu-id="d2b1c-129">L’objet spécifié existe déjà.</span><span class="sxs-lookup"><span data-stu-id="d2b1c-129">The object specified already exists.</span></span>

</dd> <dt>

<span data-ttu-id="d2b1c-130">**11**</span><span class="sxs-lookup"><span data-stu-id="d2b1c-130">**11**</span></span>
</dt> <dd>

<span data-ttu-id="d2b1c-131">Le système de fichiers n’est pas NTFS.</span><span class="sxs-lookup"><span data-stu-id="d2b1c-131">The file system is not NTFS.</span></span>

</dd> <dt>

<span data-ttu-id="d2b1c-132">**12**</span><span class="sxs-lookup"><span data-stu-id="d2b1c-132">**12**</span></span>
</dt> <dd>

<span data-ttu-id="d2b1c-133">La plateforme n’est pas Windows.</span><span class="sxs-lookup"><span data-stu-id="d2b1c-133">The platform is not Windows.</span></span>

</dd> <dt>

<span data-ttu-id="d2b1c-134">**13**</span><span class="sxs-lookup"><span data-stu-id="d2b1c-134">**13**</span></span>
</dt> <dd>

<span data-ttu-id="d2b1c-135">Le lecteur n’est pas le même.</span><span class="sxs-lookup"><span data-stu-id="d2b1c-135">The drive is not the same.</span></span>

</dd> <dt>

<span data-ttu-id="d2b1c-136">**14**</span><span class="sxs-lookup"><span data-stu-id="d2b1c-136">**14**</span></span>
</dt> <dd>

<span data-ttu-id="d2b1c-137">Le répertoire n'est pas vide.</span><span class="sxs-lookup"><span data-stu-id="d2b1c-137">The directory is not empty.</span></span>

</dd> <dt>

<span data-ttu-id="d2b1c-138">**15**</span><span class="sxs-lookup"><span data-stu-id="d2b1c-138">**15**</span></span>
</dt> <dd>

<span data-ttu-id="d2b1c-139">Une violation de partage s’est produite.</span><span class="sxs-lookup"><span data-stu-id="d2b1c-139">There has been a sharing violation.</span></span>

</dd> <dt>

<span data-ttu-id="d2b1c-140">**16**</span><span class="sxs-lookup"><span data-stu-id="d2b1c-140">**16**</span></span>
</dt> <dd>

<span data-ttu-id="d2b1c-141">Le fichier de démarrage spécifié n’est pas valide.</span><span class="sxs-lookup"><span data-stu-id="d2b1c-141">The start file specified was not valid.</span></span>

</dd> <dt>

<span data-ttu-id="d2b1c-142">**17**</span><span class="sxs-lookup"><span data-stu-id="d2b1c-142">**17**</span></span>
</dt> <dd>

<span data-ttu-id="d2b1c-143">Un privilège requis pour l’opération n’est pas conservé.</span><span class="sxs-lookup"><span data-stu-id="d2b1c-143">A privilege required for the operation is not held.</span></span>

</dd> <dt>

<span data-ttu-id="d2b1c-144">**21**</span><span class="sxs-lookup"><span data-stu-id="d2b1c-144">**21**</span></span>
</dt> <dd>

<span data-ttu-id="d2b1c-145">Un paramètre spécifié n’est pas valide.</span><span class="sxs-lookup"><span data-stu-id="d2b1c-145">A parameter specified is not valid.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="d2b1c-146">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="d2b1c-146">Requirements</span></span>



| <span data-ttu-id="d2b1c-147">Condition requise</span><span class="sxs-lookup"><span data-stu-id="d2b1c-147">Requirement</span></span> | <span data-ttu-id="d2b1c-148">Valeur</span><span class="sxs-lookup"><span data-stu-id="d2b1c-148">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="d2b1c-149">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="d2b1c-149">Minimum supported client</span></span><br/> | <span data-ttu-id="d2b1c-150">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="d2b1c-150">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="d2b1c-151">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="d2b1c-151">Minimum supported server</span></span><br/> | <span data-ttu-id="d2b1c-152">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="d2b1c-152">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="d2b1c-153">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="d2b1c-153">Namespace</span></span><br/>                | <span data-ttu-id="d2b1c-154">\\Cimv2 racine</span><span class="sxs-lookup"><span data-stu-id="d2b1c-154">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="d2b1c-155">MOF</span><span class="sxs-lookup"><span data-stu-id="d2b1c-155">MOF</span></span><br/>                      | <dl> <span data-ttu-id="d2b1c-156"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="d2b1c-156"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="d2b1c-157">DLL</span><span class="sxs-lookup"><span data-stu-id="d2b1c-157">DLL</span></span><br/>                      | <dl> <span data-ttu-id="d2b1c-158"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="d2b1c-158"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d2b1c-159">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="d2b1c-159">See also</span></span>

<dl> <dt>

<span data-ttu-id="d2b1c-160">[Classes du système d’exploitation](/previous-versions//aa392727(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="d2b1c-160">[Operating System Classes](/previous-versions//aa392727(v=vs.85))</span></span>
</dt> <dt>

[<span data-ttu-id="d2b1c-161">**\_Répertoire Win32**</span><span class="sxs-lookup"><span data-stu-id="d2b1c-161">**Win32\_Directory**</span></span>](win32-directory.md)
</dt> </dl>

 

