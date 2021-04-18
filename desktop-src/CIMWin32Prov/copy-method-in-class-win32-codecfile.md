---
description: Copie le fichier ou le répertoire du codec logique spécifié dans le chemin de l’objet vers l’emplacement spécifié par le paramètre d’entrée.
ms.assetid: 77e67b01-561b-4233-899d-fa4bbf75ecf8
ms.tgt_platform: multiple
title: Méthode Copy de la classe Win32_CodecFile
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_CodecFile.Copy
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: e3bd6621c065192eb45176444257f1c29c897201
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106519217"
---
# <a name="copy-method-of-the-win32_codecfile-class"></a><span data-ttu-id="17597-103">Méthode Copy de la \_ classe CodecFile Win32</span><span class="sxs-lookup"><span data-stu-id="17597-103">Copy method of the Win32\_CodecFile class</span></span>

<span data-ttu-id="17597-104">La méthode **Copy** [WMI Class](/windows/desktop/WmiSdk/retrieving-a-class) copie le fichier de codec logique ou le répertoire spécifié dans le chemin d’accès de l’objet vers l’emplacement spécifié par le paramètre d’entrée.</span><span class="sxs-lookup"><span data-stu-id="17597-104">The **Copy** [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) method copies the logical codec file or directory specified in the object path to the location specified by the input parameter.</span></span> <span data-ttu-id="17597-105">Une copie n’est pas prise en charge si le remplacement d’un fichier logique existant est nécessaire.</span><span class="sxs-lookup"><span data-stu-id="17597-105">A copy is not supported if overwriting an existing logical file is required.</span></span>

<span data-ttu-id="17597-106">Cette rubrique utilise la syntaxe format MOF (MOF).</span><span class="sxs-lookup"><span data-stu-id="17597-106">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="17597-107">Pour plus d’informations sur l’utilisation de cette méthode, consultez [appel d’une méthode](/windows/desktop/WmiSdk/calling-a-method).</span><span class="sxs-lookup"><span data-stu-id="17597-107">For more information about using this method, see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="17597-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="17597-108">Syntax</span></span>


```mof
uint32 Copy(
   string FileName
);
```



## <a name="parameters"></a><span data-ttu-id="17597-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="17597-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="17597-110">*FileName*</span><span class="sxs-lookup"><span data-stu-id="17597-110">*FileName*</span></span> 
</dt> <dd>

<span data-ttu-id="17597-111">Nom complet de la copie du fichier (ou du répertoire).</span><span class="sxs-lookup"><span data-stu-id="17597-111">Fully qualified name of the copy of the file (or directory).</span></span> <span data-ttu-id="17597-112">Exemple : c : \\ temp \\ newDirectory.</span><span class="sxs-lookup"><span data-stu-id="17597-112">Example: c:\\temp\\newdirectory.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="17597-113">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="17597-113">Return value</span></span>

<span data-ttu-id="17597-114">Retourne la valeur 0 (zéro) si le fichier a été copié avec succès, et tout autre nombre pour indiquer une erreur.</span><span class="sxs-lookup"><span data-stu-id="17597-114">Returns an value of 0 (zero) if the file was successfully copied, and any other number to indicate an error.</span></span>

<dl> <dt>

<span data-ttu-id="17597-115">**0**</span><span class="sxs-lookup"><span data-stu-id="17597-115">**0**</span></span>
</dt> <dd>

<span data-ttu-id="17597-116">La demande a abouti.</span><span class="sxs-lookup"><span data-stu-id="17597-116">The request was successful.</span></span>

</dd> <dt>

<span data-ttu-id="17597-117">**2**</span><span class="sxs-lookup"><span data-stu-id="17597-117">**2**</span></span>
</dt> <dd>

<span data-ttu-id="17597-118">L’accès a été refusé.</span><span class="sxs-lookup"><span data-stu-id="17597-118">Access was denied.</span></span>

</dd> <dt>

<span data-ttu-id="17597-119">**8**</span><span class="sxs-lookup"><span data-stu-id="17597-119">**8**</span></span>
</dt> <dd>

<span data-ttu-id="17597-120">Une erreur non spécifiée s’est produite.</span><span class="sxs-lookup"><span data-stu-id="17597-120">An unspecified failure occurred.</span></span>

</dd> <dt>

<span data-ttu-id="17597-121">**9**</span><span class="sxs-lookup"><span data-stu-id="17597-121">**9**</span></span>
</dt> <dd>

<span data-ttu-id="17597-122">Le nom spécifié n’est pas valide.</span><span class="sxs-lookup"><span data-stu-id="17597-122">The name specified was not valid.</span></span>

</dd> <dt>

<span data-ttu-id="17597-123">**10**</span><span class="sxs-lookup"><span data-stu-id="17597-123">**10**</span></span>
</dt> <dd>

<span data-ttu-id="17597-124">L’objet spécifié existe déjà.</span><span class="sxs-lookup"><span data-stu-id="17597-124">The object specified already exists.</span></span>

</dd> <dt>

<span data-ttu-id="17597-125">**11**</span><span class="sxs-lookup"><span data-stu-id="17597-125">**11**</span></span>
</dt> <dd>

<span data-ttu-id="17597-126">Le système de fichiers n’est pas NTFS.</span><span class="sxs-lookup"><span data-stu-id="17597-126">The file system is not NTFS.</span></span>

</dd> <dt>

<span data-ttu-id="17597-127">**12**</span><span class="sxs-lookup"><span data-stu-id="17597-127">**12**</span></span>
</dt> <dd>

<span data-ttu-id="17597-128">La plateforme n’est pas Windows.</span><span class="sxs-lookup"><span data-stu-id="17597-128">The platform is not Windows.</span></span>

</dd> <dt>

<span data-ttu-id="17597-129">**13**</span><span class="sxs-lookup"><span data-stu-id="17597-129">**13**</span></span>
</dt> <dd>

<span data-ttu-id="17597-130">Le lecteur n’est pas le même.</span><span class="sxs-lookup"><span data-stu-id="17597-130">The drive is not the same.</span></span>

</dd> <dt>

<span data-ttu-id="17597-131">**14**</span><span class="sxs-lookup"><span data-stu-id="17597-131">**14**</span></span>
</dt> <dd>

<span data-ttu-id="17597-132">Le répertoire n'est pas vide.</span><span class="sxs-lookup"><span data-stu-id="17597-132">The directory is not empty.</span></span>

</dd> <dt>

<span data-ttu-id="17597-133">**15**</span><span class="sxs-lookup"><span data-stu-id="17597-133">**15**</span></span>
</dt> <dd>

<span data-ttu-id="17597-134">Une violation de partage s’est produite.</span><span class="sxs-lookup"><span data-stu-id="17597-134">There has been a sharing violation.</span></span>

</dd> <dt>

<span data-ttu-id="17597-135">**16**</span><span class="sxs-lookup"><span data-stu-id="17597-135">**16**</span></span>
</dt> <dd>

<span data-ttu-id="17597-136">Le fichier de démarrage spécifié n’est pas valide.</span><span class="sxs-lookup"><span data-stu-id="17597-136">The start file specified was not valid.</span></span>

</dd> <dt>

<span data-ttu-id="17597-137">**17**</span><span class="sxs-lookup"><span data-stu-id="17597-137">**17**</span></span>
</dt> <dd>

<span data-ttu-id="17597-138">Un privilège requis pour l’opération n’est pas conservé.</span><span class="sxs-lookup"><span data-stu-id="17597-138">A privilege required for the operation is not held.</span></span>

</dd> <dt>

<span data-ttu-id="17597-139">**21**</span><span class="sxs-lookup"><span data-stu-id="17597-139">**21**</span></span>
</dt> <dd>

<span data-ttu-id="17597-140">Un paramètre spécifié n’est pas valide.</span><span class="sxs-lookup"><span data-stu-id="17597-140">A parameter specified is not valid.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="17597-141">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="17597-141">Requirements</span></span>



| <span data-ttu-id="17597-142">Condition requise</span><span class="sxs-lookup"><span data-stu-id="17597-142">Requirement</span></span> | <span data-ttu-id="17597-143">Valeur</span><span class="sxs-lookup"><span data-stu-id="17597-143">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="17597-144">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="17597-144">Minimum supported client</span></span><br/> | <span data-ttu-id="17597-145">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="17597-145">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="17597-146">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="17597-146">Minimum supported server</span></span><br/> | <span data-ttu-id="17597-147">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="17597-147">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="17597-148">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="17597-148">Namespace</span></span><br/>                | <span data-ttu-id="17597-149">\\Cimv2 racine</span><span class="sxs-lookup"><span data-stu-id="17597-149">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="17597-150">MOF</span><span class="sxs-lookup"><span data-stu-id="17597-150">MOF</span></span><br/>                      | <dl> <span data-ttu-id="17597-151"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="17597-151"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="17597-152">DLL</span><span class="sxs-lookup"><span data-stu-id="17597-152">DLL</span></span><br/>                      | <dl> <span data-ttu-id="17597-153"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="17597-153"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="17597-154">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="17597-154">See also</span></span>

<dl> <dt>

<span data-ttu-id="17597-155">[Classes du système d’exploitation](/previous-versions//aa392727(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="17597-155">[Operating System Classes](/previous-versions//aa392727(v=vs.85))</span></span>
</dt> <dt>

[<span data-ttu-id="17597-156">**\_CodecFile Win32**</span><span class="sxs-lookup"><span data-stu-id="17597-156">**Win32\_CodecFile**</span></span>](win32-codecfile.md)
</dt> </dl>

 

