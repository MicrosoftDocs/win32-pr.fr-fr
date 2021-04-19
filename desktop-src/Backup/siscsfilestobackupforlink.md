---
title: SisCSFilesToBackupForLink, fonction (sisbkup. h)
description: Retourne des informations décrivant les fichiers du magasin commun vers lesquels pointe le lien SIS spécifié.
ms.assetid: 0580c34e-195a-4a2c-893f-bc339dcc88d7
keywords:
- Sauvegarde de la fonction SisCSFilesToBackupForLink
topic_type:
- apiref
api_name:
- SisCSFilesToBackupForLink
api_location:
- Sisbkup.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 27d4f52728d662f43efed85d662874bd4b008947
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "106513587"
---
# <a name="siscsfilestobackupforlink-function"></a><span data-ttu-id="105c6-104">SisCSFilesToBackupForLink fonction)</span><span class="sxs-lookup"><span data-stu-id="105c6-104">SisCSFilesToBackupForLink function</span></span>

<span data-ttu-id="105c6-105">La fonction **SisCSFilesToBackupForLink** retourne des informations décrivant les fichiers de magasin commun vers lesquels pointe le lien SIS spécifié.</span><span class="sxs-lookup"><span data-stu-id="105c6-105">The **SisCSFilesToBackupForLink** function returns information describing the common-store files the specified SIS link points to.</span></span>

## <a name="syntax"></a><span data-ttu-id="105c6-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="105c6-106">Syntax</span></span>


```C++
BOOL SisCSFilesToBackupForLink(
  _In_  PVOID  sisBackupStructure,
  _In_  PVOID  reparseData,
  _In_  ULONG  reparseDataSize,
  _Out_ PVOID  thisFileContext,
  _Out_ PVOID  *matchingFileContext,
  _Out_ PULONG countOfCommonStoreFilesToBackUp,
  _Out_ PWCHAR **commonStoreFilesToBackUp
);
```



## <a name="parameters"></a><span data-ttu-id="105c6-107">Paramètres</span><span class="sxs-lookup"><span data-stu-id="105c6-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="105c6-108">*sisBackupStructure* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="105c6-108">*sisBackupStructure* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="105c6-109">Pointeur vers la structure de sauvegarde SIS retournée par [**SisCreateBackupStructure**](siscreatebackupstructure.md).</span><span class="sxs-lookup"><span data-stu-id="105c6-109">Pointer to the SIS backup structure returned from [**SisCreateBackupStructure**](siscreatebackupstructure.md).</span></span>

</dd> <dt>

<span data-ttu-id="105c6-110">*reparseData* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="105c6-110">*reparseData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="105c6-111">Pointeur vers le contenu du point d’analyse SIS.</span><span class="sxs-lookup"><span data-stu-id="105c6-111">Pointer to the contents of the SIS reparse point.</span></span> <span data-ttu-id="105c6-112">Ce point d’analyse contient des données décrivant un lien SIS.</span><span class="sxs-lookup"><span data-stu-id="105c6-112">This reparse point contains data describing a SIS link.</span></span> <span data-ttu-id="105c6-113">Pour récupérer les données du point d’analyse d’un fichier, utilisez le code de contrôle [**FSCTL \_ obtenir le \_ \_ point d’analyse**](/windows/desktop/api/winioctl/ni-winioctl-fsctl_get_reparse_point) .</span><span class="sxs-lookup"><span data-stu-id="105c6-113">To retrieve the reparse point data for a file, use the [**FSCTL\_GET\_REPARSE\_POINT**](/windows/desktop/api/winioctl/ni-winioctl-fsctl_get_reparse_point) control code.</span></span>

</dd> <dt>

<span data-ttu-id="105c6-114">*reparseDataSize* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="105c6-114">*reparseDataSize* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="105c6-115">Taille du contenu du point d’analyse SIS pointé par *reparseData*, en octets.</span><span class="sxs-lookup"><span data-stu-id="105c6-115">Size of the contents of the SIS reparse point pointed to by *reparseData*, in bytes.</span></span>

</dd> <dt>

<span data-ttu-id="105c6-116">*thisFileContext* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="105c6-116">*thisFileContext* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="105c6-117">Pointeur vers une chaîne de contexte fournie par l’application de sauvegarde appelant cette fonction.</span><span class="sxs-lookup"><span data-stu-id="105c6-117">Pointer to a context string supplied by the backup application calling this function.</span></span> <span data-ttu-id="105c6-118">Le contenu de cette chaîne de contenu est entièrement déterminé par cette application de sauvegarde et n’est pas interprété par l’API de sauvegarde SIS.</span><span class="sxs-lookup"><span data-stu-id="105c6-118">The contents of this content string are entirely determined by this backup application and is not interpreted by the SIS Backup API.</span></span> <span data-ttu-id="105c6-119">Ce paramètre est facultatif. s’il n’est pas utilisé, affectez la valeur **null** à ce paramètre.</span><span class="sxs-lookup"><span data-stu-id="105c6-119">This parameter is optional; if not used, set the value of this parameter to **NULL**.</span></span> <span data-ttu-id="105c6-120">La valeur de ce paramètre ne sera pas traitée dans ce cas.</span><span class="sxs-lookup"><span data-stu-id="105c6-120">The value of this parameter will not be processed in this case.</span></span>

</dd> <dt>

<span data-ttu-id="105c6-121">*matchingFileContext* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="105c6-121">*matchingFileContext* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="105c6-122">Pointeur doublement indirect vers la chaîne de contexte du lien SIS identifié par les informations passées dans les quatre premiers paramètres de cette fonction.</span><span class="sxs-lookup"><span data-stu-id="105c6-122">Doubly-indirect pointer to the context string of the SIS link identified by the information passed in the first four parameters of this function.</span></span> <span data-ttu-id="105c6-123">Ce paramètre est facultatif. Si une chaîne de contexte n’est pas fournie comme valeur du paramètre *thisFileContext* , affectez la valeur **null** à ce paramètre.</span><span class="sxs-lookup"><span data-stu-id="105c6-123">This parameter is optional; if a context string is not provided as the value of the *thisFileContext* parameter, set the value of this parameter to **NULL**.</span></span> <span data-ttu-id="105c6-124">La valeur de ce paramètre ne sera pas traitée dans ce cas.</span><span class="sxs-lookup"><span data-stu-id="105c6-124">The value of this parameter will not be processed in this case.</span></span>

</dd> <dt>

<span data-ttu-id="105c6-125">*countOfCommonStoreFilesToBackUp* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="105c6-125">*countOfCommonStoreFilesToBackUp* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="105c6-126">Nombre de fichiers listés dans le paramètre *commonStoreFilesToBackUp* .</span><span class="sxs-lookup"><span data-stu-id="105c6-126">Number of files listed in the *commonStoreFilesToBackUp* parameter.</span></span>

</dd> <dt>

<span data-ttu-id="105c6-127">*commonStoreFilesToBackUp* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="105c6-127">*commonStoreFilesToBackUp* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="105c6-128">Pointeur vers un tableau de noms de fichiers.</span><span class="sxs-lookup"><span data-stu-id="105c6-128">Pointer to an array of file names.</span></span> <span data-ttu-id="105c6-129">Ces fichiers doivent être sauvegardés en même temps et de la même façon que les fichiers du magasin commun demandés par [**SisCreateBackupStructure**](siscreatebackupstructure.md).</span><span class="sxs-lookup"><span data-stu-id="105c6-129">These files should be backed up at the same time and in the same manner as the common-store files requested by [**SisCreateBackupStructure**](siscreatebackupstructure.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="105c6-130">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="105c6-130">Return value</span></span>

<span data-ttu-id="105c6-131">Cette fonction retourne la **valeur true** si elle se termine avec succès et la **valeur false** dans le cas contraire.</span><span class="sxs-lookup"><span data-stu-id="105c6-131">This function returns **TRUE** if it completes successfully and **FALSE** otherwise.</span></span> <span data-ttu-id="105c6-132">Appelez [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) pour obtenir plus d’informations sur la raison de l’échec de l’appel.</span><span class="sxs-lookup"><span data-stu-id="105c6-132">Call [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) to get more information about the reason the call failed.</span></span>

## <a name="remarks"></a><span data-ttu-id="105c6-133">Notes</span><span class="sxs-lookup"><span data-stu-id="105c6-133">Remarks</span></span>

<span data-ttu-id="105c6-134">L’application de sauvegarde ne doit appeler cette fonction qu’une seule fois pour chaque fichier de liaison SIS en cours de sauvegarde.</span><span class="sxs-lookup"><span data-stu-id="105c6-134">The backup application should call this function only once for each SIS link file being backed up.</span></span>

<span data-ttu-id="105c6-135">L’application de sauvegarde peut identifier un point d’analyse SIS par sa balise, la balise d’analyse d’e/s de \_ \_ balise \_ SIS.</span><span class="sxs-lookup"><span data-stu-id="105c6-135">The backup application can identify a SIS reparse point by its tag, IO\_REPARSE\_TAG\_SIS.</span></span> <span data-ttu-id="105c6-136">Cette balise est définie dans Winnt. h.</span><span class="sxs-lookup"><span data-stu-id="105c6-136">This tag is defined in Winnt.h.</span></span>

<span data-ttu-id="105c6-137">Si ce point d’analyse identifié par la valeur du paramètre *reparseData* décrit la première instance d’un fichier à sauvegarder, cette fonction retourne **null** comme valeur du paramètre *matchingFileContext* et initialise la valeur du tableau *commonStoreFilesToBackUp* de chaînes avec les noms du ou des fichiers du magasin commun qui doivent être sauvegardés (e).</span><span class="sxs-lookup"><span data-stu-id="105c6-137">If this reparse point identified by the value of the *reparseData* parameter describes the first instance of a file to be backed up, this function will return **NULL** as the value of the *matchingFileContext* parameter, and initialize the value of the *commonStoreFilesToBackUp* array of strings with the names of the common-store file or files to be backed up.</span></span> <span data-ttu-id="105c6-138">Dans le cas contraire, cette fonction définit la valeur du paramètre *matchingFileContext* sur la chaîne de contexte correspondant à la première instance du fichier spécifié et affecte à la valeur du paramètre *countOfCommonStoreFilesToBackUp* la valeur 0.</span><span class="sxs-lookup"><span data-stu-id="105c6-138">Otherwise, this function will set the value of the *matchingFileContext* parameter to the context string corresponding to the first instance of the specified file and set the value of the *countOfCommonStoreFilesToBackUp* parameter to 0.</span></span> <span data-ttu-id="105c6-139">S’il existe plusieurs fichiers de magasin commun correspondant au lien spécifié, la valeur du paramètre *thisFileContext* est la chaîne de contexte correspondant au premier fichier de magasin commun retourné dans le tableau qui est, commonStoreFilesToBackUp \[ 0 \] .</span><span class="sxs-lookup"><span data-stu-id="105c6-139">If there are multiple common-store files corresponding to the specified link, the value of the *thisFileContext* parameter will be the context string corresponding to the first common-store file returned in the array that is, commonStoreFilesToBackUp\[0\].</span></span>

<span data-ttu-id="105c6-140">La version actuelle de cette fonction retournera au plus un fichier de magasin commun, mais il est possible que dans les versions ultérieures, un seul lien puisse être sauvegardé par plusieurs fichiers du magasin commun, par exemple, un pour chaque flux du fichier afin que votre application de sauvegarde prenne en charge plusieurs fichiers dans chaque appel à cette fonction.</span><span class="sxs-lookup"><span data-stu-id="105c6-140">The current version of this function will return at most one common-store file, but it is possible that in future versions a single link may be backed by several common-store files for example, one for each stream in the file so your backup application should support multiple files in each call to this function.</span></span> <span data-ttu-id="105c6-141">Dans tous les cas, chaque fichier de magasin commun est retourné au plus une fois pour chaque passe de sauvegarde.</span><span class="sxs-lookup"><span data-stu-id="105c6-141">In any case, each common-store file will be returned at most once for each backup pass.</span></span>

<span data-ttu-id="105c6-142">Votre application de sauvegarde doit sauvegarder ou restaurer le ou les fichiers du magasin commun identifiés par le nom de fichier ou les noms de fichiers retournés dans le paramètre *commonStoreFilesToBackUp* .</span><span class="sxs-lookup"><span data-stu-id="105c6-142">Your backup application should back up or restore the common-store file or files identified by the file name or file names returned in the *commonStoreFilesToBackUp* parameter.</span></span> <span data-ttu-id="105c6-143">Qu’il y ait ou non un fichier de magasin commun, votre application de sauvegarde doit sauvegarder le fichier de liaison SIS tel qu’il existe sur le disque, par exemple, comme un point d’analyse et un fichier partiellement alloué, et probablement sans aucune plage remplie.</span><span class="sxs-lookup"><span data-stu-id="105c6-143">Regardless of whether there is a corresponding common-store file, your backup application should back up the SIS link file as it exists on the disk for example, as a reparse point and a sparse file, and most likely with no ranges filled in.</span></span> <span data-ttu-id="105c6-144">Votre application de sauvegarde peut sauvegarder ou restaurer le ou les fichiers du magasin commun immédiatement, les différer ou les combiner en fonction des besoins.</span><span class="sxs-lookup"><span data-stu-id="105c6-144">Your backup application may back up or restore the common-store file or files immediately, postpone backing them up, or mix them together as necessary.</span></span>

<span data-ttu-id="105c6-145">Une fois l’opération de sauvegarde terminée, Désallouez la mémoire utilisée par le tableau de chaînes *commonStoreFilesToBackUp* en appelant [**SisFreeAllocatedMemory**](sisfreeallocatedmemory.md).</span><span class="sxs-lookup"><span data-stu-id="105c6-145">After the backup operation is complete, deallocate the memory used by the *commonStoreFilesToBackUp* array of strings by calling [**SisFreeAllocatedMemory**](sisfreeallocatedmemory.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="105c6-146">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="105c6-146">Requirements</span></span>



| <span data-ttu-id="105c6-147">Condition requise</span><span class="sxs-lookup"><span data-stu-id="105c6-147">Requirement</span></span> | <span data-ttu-id="105c6-148">Valeur</span><span class="sxs-lookup"><span data-stu-id="105c6-148">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="105c6-149">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="105c6-149">Minimum supported client</span></span><br/> | <span data-ttu-id="105c6-150">Applications de \[ Bureau Windows XP uniquement\]</span><span class="sxs-lookup"><span data-stu-id="105c6-150">Windows XP \[desktop apps only\]</span></span><br/>                                            |
| <span data-ttu-id="105c6-151">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="105c6-151">Minimum supported server</span></span><br/> | <span data-ttu-id="105c6-152">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="105c6-152">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="105c6-153">En-tête</span><span class="sxs-lookup"><span data-stu-id="105c6-153">Header</span></span><br/>                   | <dl> <span data-ttu-id="105c6-154"><dt>Sisbkup. h</dt></span><span class="sxs-lookup"><span data-stu-id="105c6-154"><dt>Sisbkup.h</dt></span></span> </dl>   |
| <span data-ttu-id="105c6-155">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="105c6-155">Library</span></span><br/>                  | <dl> <span data-ttu-id="105c6-156"><dt>Sisbkup. lib</dt></span><span class="sxs-lookup"><span data-stu-id="105c6-156"><dt>Sisbkup.lib</dt></span></span> </dl> |
| <span data-ttu-id="105c6-157">DLL</span><span class="sxs-lookup"><span data-stu-id="105c6-157">DLL</span></span><br/>                      | <dl> <span data-ttu-id="105c6-158"><dt>Sisbkup.dll</dt></span><span class="sxs-lookup"><span data-stu-id="105c6-158"><dt>Sisbkup.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="105c6-159">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="105c6-159">See also</span></span>

<dl> <dt>

[<span data-ttu-id="105c6-160">**SisFreeAllocatedMemory**</span><span class="sxs-lookup"><span data-stu-id="105c6-160">**SisFreeAllocatedMemory**</span></span>](sisfreeallocatedmemory.md)
</dt> <dt>

[<span data-ttu-id="105c6-161">**SisCreateBackupStructure**</span><span class="sxs-lookup"><span data-stu-id="105c6-161">**SisCreateBackupStructure**</span></span>](siscreatebackupstructure.md)
</dt> </dl>

 

