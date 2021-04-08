---
title: SisRestoredLink, fonction (sisbkup. h)
description: Retourne les noms du ou des fichiers du magasin commun vers lesquels pointe le lien SIS restauré spécifié.
ms.assetid: 4eefd975-6055-44c0-93ab-900638948f3e
keywords:
- Sauvegarde de la fonction SisRestoredLink
topic_type:
- apiref
api_name:
- SisRestoredLink
api_location:
- Sisbkup.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fd539d1ad6c203441b2bcd469a7d8f2fe8bdfc7c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103941855"
---
# <a name="sisrestoredlink-function"></a><span data-ttu-id="7a1a7-104">SisRestoredLink fonction)</span><span class="sxs-lookup"><span data-stu-id="7a1a7-104">SisRestoredLink function</span></span>

<span data-ttu-id="7a1a7-105">La fonction **SisRestoredLink** retourne le nom du ou des fichiers du magasin commun vers lequel pointe le lien SIS restauré spécifié.</span><span class="sxs-lookup"><span data-stu-id="7a1a7-105">The **SisRestoredLink** function returns the names of the common-store file or files pointed to by the specified restored SIS link.</span></span>

## <a name="syntax"></a><span data-ttu-id="7a1a7-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="7a1a7-106">Syntax</span></span>


```C++
BOOL SisRestoredLink(
  _In_  PVOID  sisRestoreStructure,
  _In_  PWCHAR restoredFileName,
  _In_  PVOID  reparseData,
  _In_  ULONG  reparseDataSize,
  _Out_ PULONG countOfCommonStoreFilesToRestore,
  _Out_ PWCHAR **commonStoreFilesToRestore
);
```



## <a name="parameters"></a><span data-ttu-id="7a1a7-107">Paramètres</span><span class="sxs-lookup"><span data-stu-id="7a1a7-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7a1a7-108">*sisRestoreStructure* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="7a1a7-108">*sisRestoreStructure* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7a1a7-109">Pointeur vers une structure de restauration SIS retournée à partir de [**SisCreateRestoreStructure**](siscreaterestorestructure.md).</span><span class="sxs-lookup"><span data-stu-id="7a1a7-109">Pointer to a SIS restore structure returned from [**SisCreateRestoreStructure**](siscreaterestorestructure.md).</span></span>

</dd> <dt>

<span data-ttu-id="7a1a7-110">*restoredFileName* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="7a1a7-110">*restoredFileName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7a1a7-111">Nom de fichier complet du fichier de liaison SIS restauré.</span><span class="sxs-lookup"><span data-stu-id="7a1a7-111">Fully qualified file name of the restored SIS link file.</span></span>

</dd> <dt>

<span data-ttu-id="7a1a7-112">*reparseData* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="7a1a7-112">*reparseData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7a1a7-113">Pointeur vers le contenu du point d’analyse SIS.</span><span class="sxs-lookup"><span data-stu-id="7a1a7-113">Pointer to the contents of the SIS reparse point.</span></span> <span data-ttu-id="7a1a7-114">Ce point d’analyse contient des données décrivant le lien SIS restauré.</span><span class="sxs-lookup"><span data-stu-id="7a1a7-114">This reparse point contains data describing the restored SIS link.</span></span> <span data-ttu-id="7a1a7-115">Pour récupérer les données du point d’analyse d’un fichier, utilisez le code de contrôle [**FSCTL \_ obtenir le \_ \_ point d’analyse**](/windows/desktop/api/winioctl/ni-winioctl-fsctl_get_reparse_point) .</span><span class="sxs-lookup"><span data-stu-id="7a1a7-115">To retrieve the reparse point data for a file, use the [**FSCTL\_GET\_REPARSE\_POINT**](/windows/desktop/api/winioctl/ni-winioctl-fsctl_get_reparse_point) control code.</span></span>

</dd> <dt>

<span data-ttu-id="7a1a7-116">*reparseDataSize* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="7a1a7-116">*reparseDataSize* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7a1a7-117">Taille du contenu du point d’analyse SIS pointé par *reparseData*, en octets.</span><span class="sxs-lookup"><span data-stu-id="7a1a7-117">Size of the contents of the SIS reparse point pointed to by *reparseData*, in bytes.</span></span>

</dd> <dt>

<span data-ttu-id="7a1a7-118">*countOfCommonStoreFilesToRestore* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="7a1a7-118">*countOfCommonStoreFilesToRestore* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="7a1a7-119">Nombre de fichiers listés dans le paramètre *commonStoreFilesToRestore* .</span><span class="sxs-lookup"><span data-stu-id="7a1a7-119">Number of files listed in the *commonStoreFilesToRestore* parameter.</span></span>

</dd> <dt>

<span data-ttu-id="7a1a7-120">*commonStoreFilesToRestore* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="7a1a7-120">*commonStoreFilesToRestore* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="7a1a7-121">Pointeur vers un tableau de noms de fichiers Common-Store.</span><span class="sxs-lookup"><span data-stu-id="7a1a7-121">Pointer to an array of common-store file names.</span></span> <span data-ttu-id="7a1a7-122">Ces fichiers doivent être restaurés en même temps et de la même façon que les fichiers du magasin commun demandés par [**SisCSFilesToBackupForLink**](siscsfilestobackupforlink.md).</span><span class="sxs-lookup"><span data-stu-id="7a1a7-122">These files should be restored at the same time and in the same manner as the common-store files requested by [**SisCSFilesToBackupForLink**](siscsfilestobackupforlink.md).</span></span>

<span data-ttu-id="7a1a7-123">Si la valeur du paramètre *countOfCommonStoreFilesToRestore* n’est pas 0, la valeur du paramètre *commonStoreFilesToRestore* contient les noms des fichiers du magasin commun à restaurer suite à la restauration du lien SIS.</span><span class="sxs-lookup"><span data-stu-id="7a1a7-123">If the value of the *countOfCommonStoreFilesToRestore* parameter is not 0, the value of the *commonStoreFilesToRestore* parameter will contain the names of the common-store files to be restored as a result of restoring the SIS link.</span></span> <span data-ttu-id="7a1a7-124">Si la valeur est 0, cela signifie que les fichiers du magasin commun ont été retournés une fois ou qu’ils sont déjà présents sur le volume.</span><span class="sxs-lookup"><span data-stu-id="7a1a7-124">If the value is 0, then either the common-store files have been returned once, or they are already present on the volume.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7a1a7-125">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="7a1a7-125">Return value</span></span>

<span data-ttu-id="7a1a7-126">Cette fonction retourne la **valeur true** si elle se termine avec succès et la **valeur false** dans le cas contraire.</span><span class="sxs-lookup"><span data-stu-id="7a1a7-126">This function returns **TRUE** if it completes successfully and **FALSE** otherwise.</span></span> <span data-ttu-id="7a1a7-127">Appelez [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) pour obtenir plus d’informations sur la raison de l’échec de l’appel.</span><span class="sxs-lookup"><span data-stu-id="7a1a7-127">Call [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) to get more information about the reason the call failed.</span></span>

## <a name="remarks"></a><span data-ttu-id="7a1a7-128">Notes</span><span class="sxs-lookup"><span data-stu-id="7a1a7-128">Remarks</span></span>

<span data-ttu-id="7a1a7-129">Vous devez appeler cette fonction pour chaque lien SIS qui a été restauré.</span><span class="sxs-lookup"><span data-stu-id="7a1a7-129">You should call this function for each SIS link that has been restored.</span></span>

<span data-ttu-id="7a1a7-130">Cette fonction renverra chaque fichier de magasin commun au plus une fois pour chaque opération de restauration. toute tentative de restauration de liens SIS supplémentaires qui affichent le même fichier de magasin commun n’entraîne pas le renvoi du nom de fichier du magasin commun.</span><span class="sxs-lookup"><span data-stu-id="7a1a7-130">This function will return each common-store file at most once for each restore operation; any attempt to restore additional SIS links that see the same common-store file will not result in that common-store file name being returned.</span></span>

<span data-ttu-id="7a1a7-131">Cette fonction ne retourne pas de fichier de magasin commun qui n’a pas également été retourné dans un appel à [**SisCSFilesToBackupForLink**](siscsfilestobackupforlink.md) pendant l’opération de sauvegarde, en supposant que les données de réanalyse SIS stockées sur le média n’ont pas été endommagées.</span><span class="sxs-lookup"><span data-stu-id="7a1a7-131">This function will not return a common-store file that was not also returned in a call to [**SisCSFilesToBackupForLink**](siscsfilestobackupforlink.md) during the backup operation, assuming that the SIS reparse data stored on the media has not been corrupted.</span></span>

<span data-ttu-id="7a1a7-132">Lors de la restauration d’un lien SIS, votre opération de restauration doit créer uniquement le fichier partiellement alloué approprié, initialiser toutes les plages allouées, puis écrire les données de nouvelle analyse SIS exactement telles qu’elles ont été lues pendant l’opération de sauvegarde.</span><span class="sxs-lookup"><span data-stu-id="7a1a7-132">When restoring a SIS link, your restore operation should create only the appropriate sparse file, initialize any allocated ranges, and then write the SIS reparse data exactly as it was read during the backup operation.</span></span> <span data-ttu-id="7a1a7-133">Il est essentiel que votre opération de restauration crée des fichiers partiellement alloués avec des plages non allouées, plutôt que des fichiers partiellement alloués (ou des fichiers non distants) initialisés avec des zéros.</span><span class="sxs-lookup"><span data-stu-id="7a1a7-133">It is crucial that your restore operation create sparse files with unallocated ranges rather than sparse files (or nonsparse files) initialized with zeroes.</span></span>

<span data-ttu-id="7a1a7-134">Notez que cette fonction n’identifie pas nécessairement le ou les fichiers du magasin commun qui correspondent à un ensemble de liens SIS sur le support de sauvegarde si ces fichiers ou fichiers du magasin commun existent toujours sur le disque.</span><span class="sxs-lookup"><span data-stu-id="7a1a7-134">Note that this function will not necessarily identify the common-store file or files corresponding to a set of SIS links on the backup media if those common-store file or files still exist on disk.</span></span> <span data-ttu-id="7a1a7-135">Le contenu du flux de données d’un fichier du magasin commun n’est jamais modifié une fois qu’il a été créé. par conséquent, si le fichier existe déjà sur le disque, il n’est pas nécessaire de le restaurer.</span><span class="sxs-lookup"><span data-stu-id="7a1a7-135">The contents of a common-store file's data stream never changes once it is created, so if the file already exists on the disk there is no need to restore it.</span></span>

<span data-ttu-id="7a1a7-136">Les noms de fichiers Common-Store sont globalement uniques pour garantir l’intégrité de l’opération de restauration, même si elle ne se produit pas sur le même volume SIS que l’opération de sauvegarde a accédé.</span><span class="sxs-lookup"><span data-stu-id="7a1a7-136">Common-store file names are globally unique to ensure the integrity of the restore operation even if it does not occur on the same SIS-enabled volume that the backup operation has accessed.</span></span>

## <a name="requirements"></a><span data-ttu-id="7a1a7-137">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="7a1a7-137">Requirements</span></span>



| <span data-ttu-id="7a1a7-138">Condition requise</span><span class="sxs-lookup"><span data-stu-id="7a1a7-138">Requirement</span></span> | <span data-ttu-id="7a1a7-139">Valeur</span><span class="sxs-lookup"><span data-stu-id="7a1a7-139">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="7a1a7-140">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="7a1a7-140">Minimum supported client</span></span><br/> | <span data-ttu-id="7a1a7-141">Applications de \[ Bureau Windows XP uniquement\]</span><span class="sxs-lookup"><span data-stu-id="7a1a7-141">Windows XP \[desktop apps only\]</span></span><br/>                                            |
| <span data-ttu-id="7a1a7-142">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="7a1a7-142">Minimum supported server</span></span><br/> | <span data-ttu-id="7a1a7-143">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="7a1a7-143">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="7a1a7-144">En-tête</span><span class="sxs-lookup"><span data-stu-id="7a1a7-144">Header</span></span><br/>                   | <dl> <span data-ttu-id="7a1a7-145"><dt>Sisbkup. h</dt></span><span class="sxs-lookup"><span data-stu-id="7a1a7-145"><dt>Sisbkup.h</dt></span></span> </dl>   |
| <span data-ttu-id="7a1a7-146">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="7a1a7-146">Library</span></span><br/>                  | <dl> <span data-ttu-id="7a1a7-147"><dt>Sisbkup. lib</dt></span><span class="sxs-lookup"><span data-stu-id="7a1a7-147"><dt>Sisbkup.lib</dt></span></span> </dl> |
| <span data-ttu-id="7a1a7-148">DLL</span><span class="sxs-lookup"><span data-stu-id="7a1a7-148">DLL</span></span><br/>                      | <dl> <span data-ttu-id="7a1a7-149"><dt>Sisbkup.dll</dt></span><span class="sxs-lookup"><span data-stu-id="7a1a7-149"><dt>Sisbkup.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7a1a7-150">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="7a1a7-150">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7a1a7-151">**SisCreateRestoreStructure**</span><span class="sxs-lookup"><span data-stu-id="7a1a7-151">**SisCreateRestoreStructure**</span></span>](siscreaterestorestructure.md)
</dt> <dt>

[<span data-ttu-id="7a1a7-152">**SisCSFilesToBackupForLink**</span><span class="sxs-lookup"><span data-stu-id="7a1a7-152">**SisCSFilesToBackupForLink**</span></span>](siscsfilestobackupforlink.md)
</dt> </dl>

 

