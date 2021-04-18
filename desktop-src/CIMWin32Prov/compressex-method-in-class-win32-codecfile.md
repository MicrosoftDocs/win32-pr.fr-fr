---
description: Compresse le fichier de codec logique (ou le répertoire) spécifié dans le chemin d’accès de l’objet (cette méthode est une version étendue de la méthode Compress).
ms.assetid: e1ecf0de-3b81-443e-9936-326d7d2d9210
ms.tgt_platform: multiple
title: Méthode CompressEx de la classe Win32_CodecFile
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_CodecFile.CompressEx
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: 4ab2915a4f550c799fed8a58e5573e8264b92f1e
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104482928"
---
# <a name="compressex-method-of-the-win32_codecfile-class"></a><span data-ttu-id="499d1-103">Méthode CompressEx de la \_ classe Win32 CodecFile</span><span class="sxs-lookup"><span data-stu-id="499d1-103">CompressEx method of the Win32\_CodecFile class</span></span>

<span data-ttu-id="499d1-104">La méthode de [classe WMI](/windows/desktop/WmiSdk/retrieving-a-class) **CompressEx** compresse le fichier de codec logique (ou le répertoire) spécifié dans le chemin d’accès de l’objet (cette méthode est une version étendue de la méthode [**Compress**](compress-method-in-class-win32-directory.md) ).</span><span class="sxs-lookup"><span data-stu-id="499d1-104">The **CompressEx** [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) method compresses the logical codec file (or directory) specified in the object path (this method is an extended version of the [**Compress**](compress-method-in-class-win32-directory.md) method).</span></span>

<span data-ttu-id="499d1-105">Cette rubrique utilise la syntaxe format MOF (MOF).</span><span class="sxs-lookup"><span data-stu-id="499d1-105">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="499d1-106">Pour plus d’informations sur l’utilisation de cette méthode, consultez [appel d’une méthode](/windows/desktop/WmiSdk/calling-a-method).</span><span class="sxs-lookup"><span data-stu-id="499d1-106">For more information about using this method, see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="499d1-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="499d1-107">Syntax</span></span>


```mof
uint32 CompressEx(
  [out]          string  StopFileName,
  [in, optional] string  StartFileName,
  [in, optional] boolean Recursive
);
```



## <a name="parameters"></a><span data-ttu-id="499d1-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="499d1-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="499d1-109">*StopFileName* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="499d1-109">*StopFileName* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="499d1-110">Nom du fichier ou du répertoire dans lequel la méthode **CompressEx** a échoué.</span><span class="sxs-lookup"><span data-stu-id="499d1-110">Name of the file or directory where the **CompressEx** method failed.</span></span> <span data-ttu-id="499d1-111">Ce paramètre a la **valeur null** si la méthode est réussie.</span><span class="sxs-lookup"><span data-stu-id="499d1-111">This parameter will be **null** if the method succeeds.</span></span>

</dd> <dt>

<span data-ttu-id="499d1-112">*StartFileName* \[ dans, facultatif\]</span><span class="sxs-lookup"><span data-stu-id="499d1-112">*StartFileName* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="499d1-113">Nomme le fichier ou le répertoire enfant à utiliser comme point de départ pour **CompressEx** . Le paramètre *StartFileName* est généralement le paramètre *StopFileName* spécifiant le fichier ou le répertoire dans lequel une erreur s’est produite à partir de l’appel de méthode précédent.</span><span class="sxs-lookup"><span data-stu-id="499d1-113">Names the child file or directory to use as a starting point for **CompressEx** .The *StartFileName* parameter is typically the *StopFileName* parameter specifying the file or directory at which an error occurred from the previous method call.</span></span> <span data-ttu-id="499d1-114">Si ce paramètre a la **valeur null**, l’opération est effectuée sur le fichier ou le répertoire spécifié dans l’appel de **ExecMethod** .</span><span class="sxs-lookup"><span data-stu-id="499d1-114">If this parameter is **NULL**, the operation is performed on the file or directory specified in the **ExecMethod** call.</span></span>

</dd> <dt>

<span data-ttu-id="499d1-115">*Récursif* \[ dans, facultatif\]</span><span class="sxs-lookup"><span data-stu-id="499d1-115">*Recursive* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="499d1-116">Si la **valeur est true**, la modification de la propriété sera appliquée de manière récursive aux fichiers et aux répertoires dans le répertoire spécifié par l’instance [**CIM \_ LogicalFile**](cim-logicalfile.md) .</span><span class="sxs-lookup"><span data-stu-id="499d1-116">If **true**, the change of ownership will be applied recursively to files and directories within the directory specified by the [**CIM\_LogicalFile**](cim-logicalfile.md) instance.</span></span> <span data-ttu-id="499d1-117">Remarque : pour les instances de fichier, le paramètre d’entrée *récursive* est ignoré.</span><span class="sxs-lookup"><span data-stu-id="499d1-117">Note: for file instances, the *Recursive* input parameter is ignored.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="499d1-118">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="499d1-118">Return value</span></span>

<span data-ttu-id="499d1-119">Retourne la valeur 0 (zéro) si le fichier a été compressé avec succès, et tout autre nombre pour indiquer une erreur.</span><span class="sxs-lookup"><span data-stu-id="499d1-119">Returns an value of 0 (zero) if the file was successfully compressed, and any other number to indicate an error.</span></span>

<dl> <dt>

<span data-ttu-id="499d1-120">**0**</span><span class="sxs-lookup"><span data-stu-id="499d1-120">**0**</span></span>
</dt> <dd>

<span data-ttu-id="499d1-121">La demande a abouti.</span><span class="sxs-lookup"><span data-stu-id="499d1-121">The request was successful.</span></span>

</dd> <dt>

<span data-ttu-id="499d1-122">**2**</span><span class="sxs-lookup"><span data-stu-id="499d1-122">**2**</span></span>
</dt> <dd>

<span data-ttu-id="499d1-123">L’accès a été refusé.</span><span class="sxs-lookup"><span data-stu-id="499d1-123">Access was denied.</span></span>

</dd> <dt>

<span data-ttu-id="499d1-124">**8**</span><span class="sxs-lookup"><span data-stu-id="499d1-124">**8**</span></span>
</dt> <dd>

<span data-ttu-id="499d1-125">Une erreur non spécifiée s’est produite.</span><span class="sxs-lookup"><span data-stu-id="499d1-125">An unspecified failure occurred.</span></span>

</dd> <dt>

<span data-ttu-id="499d1-126">**9**</span><span class="sxs-lookup"><span data-stu-id="499d1-126">**9**</span></span>
</dt> <dd>

<span data-ttu-id="499d1-127">Le nom spécifié n’est pas valide.</span><span class="sxs-lookup"><span data-stu-id="499d1-127">The name specified was not valid.</span></span>

</dd> <dt>

<span data-ttu-id="499d1-128">**10**</span><span class="sxs-lookup"><span data-stu-id="499d1-128">**10**</span></span>
</dt> <dd>

<span data-ttu-id="499d1-129">L’objet spécifié existe déjà.</span><span class="sxs-lookup"><span data-stu-id="499d1-129">The object specified already exists.</span></span>

</dd> <dt>

<span data-ttu-id="499d1-130">**11**</span><span class="sxs-lookup"><span data-stu-id="499d1-130">**11**</span></span>
</dt> <dd>

<span data-ttu-id="499d1-131">Le système de fichiers n’est pas NTFS.</span><span class="sxs-lookup"><span data-stu-id="499d1-131">The file system is not NTFS.</span></span>

</dd> <dt>

<span data-ttu-id="499d1-132">**12**</span><span class="sxs-lookup"><span data-stu-id="499d1-132">**12**</span></span>
</dt> <dd>

<span data-ttu-id="499d1-133">La plateforme n’est pas Windows.</span><span class="sxs-lookup"><span data-stu-id="499d1-133">The platform is not Windows.</span></span>

</dd> <dt>

<span data-ttu-id="499d1-134">**13**</span><span class="sxs-lookup"><span data-stu-id="499d1-134">**13**</span></span>
</dt> <dd>

<span data-ttu-id="499d1-135">Le lecteur n’est pas le même.</span><span class="sxs-lookup"><span data-stu-id="499d1-135">The drive is not the same.</span></span>

</dd> <dt>

<span data-ttu-id="499d1-136">**14**</span><span class="sxs-lookup"><span data-stu-id="499d1-136">**14**</span></span>
</dt> <dd>

<span data-ttu-id="499d1-137">Le répertoire n'est pas vide.</span><span class="sxs-lookup"><span data-stu-id="499d1-137">The directory is not empty.</span></span>

</dd> <dt>

<span data-ttu-id="499d1-138">**15**</span><span class="sxs-lookup"><span data-stu-id="499d1-138">**15**</span></span>
</dt> <dd>

<span data-ttu-id="499d1-139">Une violation de partage s’est produite.</span><span class="sxs-lookup"><span data-stu-id="499d1-139">There has been a sharing violation.</span></span>

</dd> <dt>

<span data-ttu-id="499d1-140">**16**</span><span class="sxs-lookup"><span data-stu-id="499d1-140">**16**</span></span>
</dt> <dd>

<span data-ttu-id="499d1-141">Le fichier de démarrage spécifié n’est pas valide.</span><span class="sxs-lookup"><span data-stu-id="499d1-141">The start file specified was not valid.</span></span>

</dd> <dt>

<span data-ttu-id="499d1-142">**17**</span><span class="sxs-lookup"><span data-stu-id="499d1-142">**17**</span></span>
</dt> <dd>

<span data-ttu-id="499d1-143">Un privilège requis pour l’opération n’est pas conservé.</span><span class="sxs-lookup"><span data-stu-id="499d1-143">A privilege required for the operation is not held.</span></span>

</dd> <dt>

<span data-ttu-id="499d1-144">**21**</span><span class="sxs-lookup"><span data-stu-id="499d1-144">**21**</span></span>
</dt> <dd>

<span data-ttu-id="499d1-145">Un paramètre spécifié n’est pas valide.</span><span class="sxs-lookup"><span data-stu-id="499d1-145">A parameter specified is not valid.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="499d1-146">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="499d1-146">Requirements</span></span>



| <span data-ttu-id="499d1-147">Condition requise</span><span class="sxs-lookup"><span data-stu-id="499d1-147">Requirement</span></span> | <span data-ttu-id="499d1-148">Valeur</span><span class="sxs-lookup"><span data-stu-id="499d1-148">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="499d1-149">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="499d1-149">Minimum supported client</span></span><br/> | <span data-ttu-id="499d1-150">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="499d1-150">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="499d1-151">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="499d1-151">Minimum supported server</span></span><br/> | <span data-ttu-id="499d1-152">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="499d1-152">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="499d1-153">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="499d1-153">Namespace</span></span><br/>                | <span data-ttu-id="499d1-154">\\Cimv2 racine</span><span class="sxs-lookup"><span data-stu-id="499d1-154">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="499d1-155">MOF</span><span class="sxs-lookup"><span data-stu-id="499d1-155">MOF</span></span><br/>                      | <dl> <span data-ttu-id="499d1-156"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="499d1-156"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="499d1-157">DLL</span><span class="sxs-lookup"><span data-stu-id="499d1-157">DLL</span></span><br/>                      | <dl> <span data-ttu-id="499d1-158"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="499d1-158"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="499d1-159">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="499d1-159">See also</span></span>

<dl> <dt>

<span data-ttu-id="499d1-160">[Classes du système d’exploitation](/previous-versions//aa392727(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="499d1-160">[Operating System Classes](/previous-versions//aa392727(v=vs.85))</span></span>
</dt> <dt>

[<span data-ttu-id="499d1-161">**\_CodecFile Win32**</span><span class="sxs-lookup"><span data-stu-id="499d1-161">**Win32\_CodecFile**</span></span>](win32-codecfile.md)
</dt> </dl>

 

