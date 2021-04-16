---
description: Décompresse le fichier de codec logique (ou le répertoire) spécifié dans le chemin d’accès de l’objet. Cette méthode est une version étendue de la méthode decompress.
ms.assetid: 257c69fa-c4f7-48be-8317-55db4b01601b
ms.tgt_platform: multiple
title: Méthode UncompressEx de la classe Win32_CodecFile
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_CodecFile.UncompressEx
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: 547062a85336681b78a6081646801e78e4713e3c
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104524119"
---
# <a name="uncompressex-method-of-the-win32_codecfile-class"></a><span data-ttu-id="812ca-104">Méthode UncompressEx de la \_ classe Win32 CodecFile</span><span class="sxs-lookup"><span data-stu-id="812ca-104">UncompressEx method of the Win32\_CodecFile class</span></span>

<span data-ttu-id="812ca-105">La méthode de [classe WMI](/windows/desktop/WmiSdk/retrieving-a-class) **UncompressEx** décompresse le fichier de codec logique (ou le répertoire) spécifié dans le chemin d’accès de l’objet.</span><span class="sxs-lookup"><span data-stu-id="812ca-105">The **UncompressEx** [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) method uncompresses the logical codec file (or directory) specified in the object path.</span></span> <span data-ttu-id="812ca-106">Cette méthode est une version étendue de la méthode [**decompress**](uncompress-method-in-class-win32-directory.md) .</span><span class="sxs-lookup"><span data-stu-id="812ca-106">This method is an extended version of the [**Uncompress**](uncompress-method-in-class-win32-directory.md) method.</span></span>

<span data-ttu-id="812ca-107">Cette rubrique utilise la syntaxe format MOF (MOF).</span><span class="sxs-lookup"><span data-stu-id="812ca-107">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="812ca-108">Pour plus d’informations sur l’utilisation de cette méthode, consultez [appel d’une méthode](/windows/desktop/WmiSdk/calling-a-method).</span><span class="sxs-lookup"><span data-stu-id="812ca-108">For more information about using this method, see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="812ca-109">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="812ca-109">Syntax</span></span>


```mof
uint32 UncompressEx(
  [out]          string  StopFileName,
  [in, optional] string  StartFileName,
  [in, optional] boolean Recursive
);
```



## <a name="parameters"></a><span data-ttu-id="812ca-110">Paramètres</span><span class="sxs-lookup"><span data-stu-id="812ca-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="812ca-111">*StopFileName* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="812ca-111">*StopFileName* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="812ca-112">Nom du fichier ou du répertoire dans lequel la méthode **UncompressEx** a échoué.</span><span class="sxs-lookup"><span data-stu-id="812ca-112">Name of the file or directory where the **UncompressEx** method failed.</span></span> <span data-ttu-id="812ca-113">Ce paramètre a la **valeur null** si la méthode est réussie.</span><span class="sxs-lookup"><span data-stu-id="812ca-113">This parameter will be **null** if the method succeeds.</span></span>

</dd> <dt>

<span data-ttu-id="812ca-114">*StartFileName* \[ dans, facultatif\]</span><span class="sxs-lookup"><span data-stu-id="812ca-114">*StartFileName* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="812ca-115">Nomme le fichier ou le répertoire enfant à utiliser comme point de départ pour **UncompressEx**. Le paramètre *StartFileName* est généralement le paramètre *StopFileName* spécifiant le fichier ou le répertoire dans lequel une erreur s’est produite à partir de l’appel de méthode précédent.</span><span class="sxs-lookup"><span data-stu-id="812ca-115">Names the child file or directory to use as a starting point for **UncompressEx**.The *StartFileName* parameter is typically the *StopFileName* parameter specifying the file or directory at which an error occurred from the previous method call.</span></span> <span data-ttu-id="812ca-116">Si ce paramètre a la **valeur null**, l’opération est effectuée sur le fichier ou le répertoire spécifié dans l’appel de **ExecMethod** .</span><span class="sxs-lookup"><span data-stu-id="812ca-116">If this parameter is **NULL**, the operation is performed on the file or directory specified in the **ExecMethod** call.</span></span>

</dd> <dt>

<span data-ttu-id="812ca-117">*Récursif* \[ dans, facultatif\]</span><span class="sxs-lookup"><span data-stu-id="812ca-117">*Recursive* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="812ca-118">Si la **valeur est true**, la modification de la propriété sera appliquée de manière récursive aux fichiers et aux répertoires dans le répertoire spécifié par l’instance [**CIM \_ LogicalFile**](cim-logicalfile.md) .</span><span class="sxs-lookup"><span data-stu-id="812ca-118">If **true**, the change of ownership will be applied recursively to files and directories within the directory specified by the [**CIM\_LogicalFile**](cim-logicalfile.md) instance.</span></span> <span data-ttu-id="812ca-119">Remarque : pour les instances de fichier, le paramètre d’entrée *récursive* est ignoré.</span><span class="sxs-lookup"><span data-stu-id="812ca-119">Note: for file instances, the *Recursive* input parameter is ignored.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="812ca-120">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="812ca-120">Return value</span></span>

<span data-ttu-id="812ca-121">Retourne une valeur entière égale à 0 (zéro) si le fichier a été décompressé avec succès, et tout autre nombre pour indiquer une erreur.</span><span class="sxs-lookup"><span data-stu-id="812ca-121">Returns an integer value of 0 (zero) if the file was successfully decompressed, and any other number to indicate an error.</span></span>

<dl> <dt>

<span data-ttu-id="812ca-122">**0**</span><span class="sxs-lookup"><span data-stu-id="812ca-122">**0**</span></span>
</dt> <dd>

<span data-ttu-id="812ca-123">La demande a abouti.</span><span class="sxs-lookup"><span data-stu-id="812ca-123">The request was successful.</span></span>

</dd> <dt>

<span data-ttu-id="812ca-124">**2**</span><span class="sxs-lookup"><span data-stu-id="812ca-124">**2**</span></span>
</dt> <dd>

<span data-ttu-id="812ca-125">L’accès a été refusé.</span><span class="sxs-lookup"><span data-stu-id="812ca-125">Access was denied.</span></span>

</dd> <dt>

<span data-ttu-id="812ca-126">**8**</span><span class="sxs-lookup"><span data-stu-id="812ca-126">**8**</span></span>
</dt> <dd>

<span data-ttu-id="812ca-127">Une erreur non spécifiée s’est produite.</span><span class="sxs-lookup"><span data-stu-id="812ca-127">An unspecified failure occurred.</span></span>

</dd> <dt>

<span data-ttu-id="812ca-128">**9**</span><span class="sxs-lookup"><span data-stu-id="812ca-128">**9**</span></span>
</dt> <dd>

<span data-ttu-id="812ca-129">Le nom spécifié n’est pas valide.</span><span class="sxs-lookup"><span data-stu-id="812ca-129">The name specified was not valid.</span></span>

</dd> <dt>

<span data-ttu-id="812ca-130">**10**</span><span class="sxs-lookup"><span data-stu-id="812ca-130">**10**</span></span>
</dt> <dd>

<span data-ttu-id="812ca-131">L’objet spécifié existe déjà.</span><span class="sxs-lookup"><span data-stu-id="812ca-131">The object specified already exists.</span></span>

</dd> <dt>

<span data-ttu-id="812ca-132">**11**</span><span class="sxs-lookup"><span data-stu-id="812ca-132">**11**</span></span>
</dt> <dd>

<span data-ttu-id="812ca-133">Le système de fichiers n’est pas NTFS.</span><span class="sxs-lookup"><span data-stu-id="812ca-133">The file system is not NTFS.</span></span>

</dd> <dt>

<span data-ttu-id="812ca-134">**12**</span><span class="sxs-lookup"><span data-stu-id="812ca-134">**12**</span></span>
</dt> <dd>

<span data-ttu-id="812ca-135">La plateforme n’est pas Windows.</span><span class="sxs-lookup"><span data-stu-id="812ca-135">The platform is not Windows.</span></span>

</dd> <dt>

<span data-ttu-id="812ca-136">**13**</span><span class="sxs-lookup"><span data-stu-id="812ca-136">**13**</span></span>
</dt> <dd>

<span data-ttu-id="812ca-137">Le lecteur n’est pas le même.</span><span class="sxs-lookup"><span data-stu-id="812ca-137">The drive is not the same.</span></span>

</dd> <dt>

<span data-ttu-id="812ca-138">**14**</span><span class="sxs-lookup"><span data-stu-id="812ca-138">**14**</span></span>
</dt> <dd>

<span data-ttu-id="812ca-139">Le répertoire n'est pas vide.</span><span class="sxs-lookup"><span data-stu-id="812ca-139">The directory is not empty.</span></span>

</dd> <dt>

<span data-ttu-id="812ca-140">**15**</span><span class="sxs-lookup"><span data-stu-id="812ca-140">**15**</span></span>
</dt> <dd>

<span data-ttu-id="812ca-141">Une violation de partage s’est produite.</span><span class="sxs-lookup"><span data-stu-id="812ca-141">There has been a sharing violation.</span></span>

</dd> <dt>

<span data-ttu-id="812ca-142">**16**</span><span class="sxs-lookup"><span data-stu-id="812ca-142">**16**</span></span>
</dt> <dd>

<span data-ttu-id="812ca-143">Le fichier de démarrage spécifié n’est pas valide.</span><span class="sxs-lookup"><span data-stu-id="812ca-143">The start file specified was not valid.</span></span>

</dd> <dt>

<span data-ttu-id="812ca-144">**17**</span><span class="sxs-lookup"><span data-stu-id="812ca-144">**17**</span></span>
</dt> <dd>

<span data-ttu-id="812ca-145">Un privilège requis pour l’opération n’est pas conservé.</span><span class="sxs-lookup"><span data-stu-id="812ca-145">A privilege required for the operation is not held.</span></span>

</dd> <dt>

<span data-ttu-id="812ca-146">**21**</span><span class="sxs-lookup"><span data-stu-id="812ca-146">**21**</span></span>
</dt> <dd>

<span data-ttu-id="812ca-147">Un paramètre spécifié n’est pas valide.</span><span class="sxs-lookup"><span data-stu-id="812ca-147">A parameter specified is not valid.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="812ca-148">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="812ca-148">Requirements</span></span>



| <span data-ttu-id="812ca-149">Condition requise</span><span class="sxs-lookup"><span data-stu-id="812ca-149">Requirement</span></span> | <span data-ttu-id="812ca-150">Valeur</span><span class="sxs-lookup"><span data-stu-id="812ca-150">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="812ca-151">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="812ca-151">Minimum supported client</span></span><br/> | <span data-ttu-id="812ca-152">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="812ca-152">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="812ca-153">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="812ca-153">Minimum supported server</span></span><br/> | <span data-ttu-id="812ca-154">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="812ca-154">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="812ca-155">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="812ca-155">Namespace</span></span><br/>                | <span data-ttu-id="812ca-156">\\Cimv2 racine</span><span class="sxs-lookup"><span data-stu-id="812ca-156">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="812ca-157">MOF</span><span class="sxs-lookup"><span data-stu-id="812ca-157">MOF</span></span><br/>                      | <dl> <span data-ttu-id="812ca-158"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="812ca-158"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="812ca-159">DLL</span><span class="sxs-lookup"><span data-stu-id="812ca-159">DLL</span></span><br/>                      | <dl> <span data-ttu-id="812ca-160"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="812ca-160"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="812ca-161">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="812ca-161">See also</span></span>

<dl> <dt>

<span data-ttu-id="812ca-162">[Classes du système d’exploitation](/previous-versions//aa392727(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="812ca-162">[Operating System Classes](/previous-versions//aa392727(v=vs.85))</span></span>
</dt> <dt>

[<span data-ttu-id="812ca-163">**\_CodecFile Win32**</span><span class="sxs-lookup"><span data-stu-id="812ca-163">**Win32\_CodecFile**</span></span>](win32-codecfile.md)
</dt> </dl>

 

