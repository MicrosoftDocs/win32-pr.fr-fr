---
description: Supprimez le fichier de codec audio ou vidéo logique (ou le répertoire) spécifié dans le chemin d’accès de l’objet.
ms.assetid: df85c8a4-3be3-4bde-b36e-6bc8af6495a9
ms.tgt_platform: multiple
title: Méthode DeleteEx de la classe Win32_CodecFile
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_CodecFile.DeleteEx
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: df5527be497176f167ac368b872253fa3254a404
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103860965"
---
# <a name="deleteex-method-of-the-win32_codecfile-class"></a><span data-ttu-id="0b569-103">Méthode DeleteEx de la \_ classe Win32 CodecFile</span><span class="sxs-lookup"><span data-stu-id="0b569-103">DeleteEx method of the Win32\_CodecFile class</span></span>

<span data-ttu-id="0b569-104">La méthode de [classe WMI](/windows/desktop/WmiSdk/retrieving-a-class) **DeleteEx** supprime le fichier de codec audio ou vidéo logique (ou le répertoire) spécifié dans le chemin d’accès de l’objet.</span><span class="sxs-lookup"><span data-stu-id="0b569-104">The **DeleteEx** [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) method will delete the logical audio or video codec file (or directory) specified in the object path.</span></span> <span data-ttu-id="0b569-105">**DeleteEx** est une version étendue de la méthode [**Delete**](delete-method-in-class-win32-directory.md) .</span><span class="sxs-lookup"><span data-stu-id="0b569-105">**DeleteEx** is an extended version of the [**Delete**](delete-method-in-class-win32-directory.md) method.</span></span>

<span data-ttu-id="0b569-106">Cette rubrique utilise la syntaxe format MOF (MOF).</span><span class="sxs-lookup"><span data-stu-id="0b569-106">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="0b569-107">Pour plus d’informations sur l’utilisation de cette méthode, consultez [appel d’une méthode](/windows/desktop/WmiSdk/calling-a-method).</span><span class="sxs-lookup"><span data-stu-id="0b569-107">For more information about using this method, see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="0b569-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="0b569-108">Syntax</span></span>


```mof
uint32 DeleteEx(
  [out] string StopFileName,
  [in]  String StartFileName
);
```



## <a name="parameters"></a><span data-ttu-id="0b569-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="0b569-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0b569-110">*StopFileName* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="0b569-110">*StopFileName* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="0b569-111">Nom du fichier ou du répertoire dans lequel la méthode **DeleteEx** a échoué.</span><span class="sxs-lookup"><span data-stu-id="0b569-111">Name of the file or directory where the **DeleteEx** method failed.</span></span> <span data-ttu-id="0b569-112">Ce paramètre a la **valeur null** si la méthode est réussie.</span><span class="sxs-lookup"><span data-stu-id="0b569-112">This parameter will be **null** if the method succeeds.</span></span>

</dd> <dt>

<span data-ttu-id="0b569-113">*StartFileName* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="0b569-113">*StartFileName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0b569-114">Nomme le fichier ou le répertoire enfant à utiliser comme point de départ pour **DeleteEx**.</span><span class="sxs-lookup"><span data-stu-id="0b569-114">Names the child file or directory to use as a starting point for **DeleteEx**.</span></span> <span data-ttu-id="0b569-115">Le paramètre *StartFileName* est généralement le paramètre *StopFileName* spécifiant le fichier ou le répertoire dans lequel une erreur s’est produite à partir de l’appel de méthode précédent.</span><span class="sxs-lookup"><span data-stu-id="0b569-115">The *StartFileName* parameter is typically the *StopFileName* parameter specifying the file or directory at which an error occurred from the previous method call.</span></span> <span data-ttu-id="0b569-116">Si ce paramètre a la **valeur null**, l’opération est effectuée sur le fichier ou le répertoire spécifié dans l’appel de **ExecMethod** .</span><span class="sxs-lookup"><span data-stu-id="0b569-116">If this parameter is **NULL**, the operation is performed on the file or directory specified in the **ExecMethod** call.</span></span> <span data-ttu-id="0b569-117">Ce paramètre est facultatif.</span><span class="sxs-lookup"><span data-stu-id="0b569-117">This parameter is optional.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0b569-118">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="0b569-118">Return value</span></span>

<span data-ttu-id="0b569-119">Retourne une valeur entière égale à 0 (zéro) si le fichier a été supprimé avec succès, et tout autre nombre pour indiquer une erreur.</span><span class="sxs-lookup"><span data-stu-id="0b569-119">Returns an integer value of 0 (zero) if the file was successfully deleted, and any other number to indicate an error.</span></span>

<dl> <dt>

<span data-ttu-id="0b569-120">**0**</span><span class="sxs-lookup"><span data-stu-id="0b569-120">**0**</span></span>
</dt> <dd>

<span data-ttu-id="0b569-121">La demande a abouti.</span><span class="sxs-lookup"><span data-stu-id="0b569-121">The request was successful.</span></span>

</dd> <dt>

<span data-ttu-id="0b569-122">**2**</span><span class="sxs-lookup"><span data-stu-id="0b569-122">**2**</span></span>
</dt> <dd>

<span data-ttu-id="0b569-123">L’accès a été refusé.</span><span class="sxs-lookup"><span data-stu-id="0b569-123">Access was denied.</span></span>

</dd> <dt>

<span data-ttu-id="0b569-124">**8**</span><span class="sxs-lookup"><span data-stu-id="0b569-124">**8**</span></span>
</dt> <dd>

<span data-ttu-id="0b569-125">Une erreur non spécifiée s’est produite.</span><span class="sxs-lookup"><span data-stu-id="0b569-125">An unspecified failure occurred.</span></span>

</dd> <dt>

<span data-ttu-id="0b569-126">**9**</span><span class="sxs-lookup"><span data-stu-id="0b569-126">**9**</span></span>
</dt> <dd>

<span data-ttu-id="0b569-127">Le nom spécifié n’est pas valide.</span><span class="sxs-lookup"><span data-stu-id="0b569-127">The name specified was not valid.</span></span>

</dd> <dt>

<span data-ttu-id="0b569-128">**10**</span><span class="sxs-lookup"><span data-stu-id="0b569-128">**10**</span></span>
</dt> <dd>

<span data-ttu-id="0b569-129">L’objet spécifié existe déjà.</span><span class="sxs-lookup"><span data-stu-id="0b569-129">The object specified already exists.</span></span>

</dd> <dt>

<span data-ttu-id="0b569-130">**11**</span><span class="sxs-lookup"><span data-stu-id="0b569-130">**11**</span></span>
</dt> <dd>

<span data-ttu-id="0b569-131">Le système de fichiers n’est pas NTFS.</span><span class="sxs-lookup"><span data-stu-id="0b569-131">The file system is not NTFS.</span></span>

</dd> <dt>

<span data-ttu-id="0b569-132">**12**</span><span class="sxs-lookup"><span data-stu-id="0b569-132">**12**</span></span>
</dt> <dd>

<span data-ttu-id="0b569-133">La plateforme n’est pas Windows.</span><span class="sxs-lookup"><span data-stu-id="0b569-133">The platform is not Windows.</span></span>

</dd> <dt>

<span data-ttu-id="0b569-134">**13**</span><span class="sxs-lookup"><span data-stu-id="0b569-134">**13**</span></span>
</dt> <dd>

<span data-ttu-id="0b569-135">Le lecteur n’est pas le même.</span><span class="sxs-lookup"><span data-stu-id="0b569-135">The drive is not the same.</span></span>

</dd> <dt>

<span data-ttu-id="0b569-136">**14**</span><span class="sxs-lookup"><span data-stu-id="0b569-136">**14**</span></span>
</dt> <dd>

<span data-ttu-id="0b569-137">Le répertoire n'est pas vide.</span><span class="sxs-lookup"><span data-stu-id="0b569-137">The directory is not empty.</span></span>

</dd> <dt>

<span data-ttu-id="0b569-138">**15**</span><span class="sxs-lookup"><span data-stu-id="0b569-138">**15**</span></span>
</dt> <dd>

<span data-ttu-id="0b569-139">Une violation de partage s’est produite.</span><span class="sxs-lookup"><span data-stu-id="0b569-139">There has been a sharing violation.</span></span>

</dd> <dt>

<span data-ttu-id="0b569-140">**16**</span><span class="sxs-lookup"><span data-stu-id="0b569-140">**16**</span></span>
</dt> <dd>

<span data-ttu-id="0b569-141">Le fichier de démarrage spécifié n’est pas valide.</span><span class="sxs-lookup"><span data-stu-id="0b569-141">The start file specified was not valid.</span></span>

</dd> <dt>

<span data-ttu-id="0b569-142">**17**</span><span class="sxs-lookup"><span data-stu-id="0b569-142">**17**</span></span>
</dt> <dd>

<span data-ttu-id="0b569-143">Un privilège requis pour l’opération n’est pas conservé.</span><span class="sxs-lookup"><span data-stu-id="0b569-143">A privilege required for the operation is not held.</span></span>

</dd> <dt>

<span data-ttu-id="0b569-144">**21**</span><span class="sxs-lookup"><span data-stu-id="0b569-144">**21**</span></span>
</dt> <dd>

<span data-ttu-id="0b569-145">Un paramètre spécifié n’est pas valide.</span><span class="sxs-lookup"><span data-stu-id="0b569-145">A parameter specified is not valid.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="0b569-146">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="0b569-146">Requirements</span></span>



| <span data-ttu-id="0b569-147">Condition requise</span><span class="sxs-lookup"><span data-stu-id="0b569-147">Requirement</span></span> | <span data-ttu-id="0b569-148">Valeur</span><span class="sxs-lookup"><span data-stu-id="0b569-148">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="0b569-149">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="0b569-149">Minimum supported client</span></span><br/> | <span data-ttu-id="0b569-150">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="0b569-150">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="0b569-151">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="0b569-151">Minimum supported server</span></span><br/> | <span data-ttu-id="0b569-152">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="0b569-152">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="0b569-153">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="0b569-153">Namespace</span></span><br/>                | <span data-ttu-id="0b569-154">\\Cimv2 racine</span><span class="sxs-lookup"><span data-stu-id="0b569-154">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="0b569-155">MOF</span><span class="sxs-lookup"><span data-stu-id="0b569-155">MOF</span></span><br/>                      | <dl> <span data-ttu-id="0b569-156"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="0b569-156"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="0b569-157">DLL</span><span class="sxs-lookup"><span data-stu-id="0b569-157">DLL</span></span><br/>                      | <dl> <span data-ttu-id="0b569-158"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="0b569-158"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0b569-159">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="0b569-159">See also</span></span>

<dl> <dt>

<span data-ttu-id="0b569-160">[Classes du système d’exploitation](/previous-versions//aa392727(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="0b569-160">[Operating System Classes](/previous-versions//aa392727(v=vs.85))</span></span>
</dt> <dt>

[<span data-ttu-id="0b569-161">**\_CodecFile Win32**</span><span class="sxs-lookup"><span data-stu-id="0b569-161">**Win32\_CodecFile**</span></span>](win32-codecfile.md)
</dt> </dl>

 

