---
title: SisCreateRestoreStructure, fonction (sisbkup. h)
description: Crée une structure de restauration SIS basée sur les informations fournies.
ms.assetid: acdd4258-813d-42af-a2e1-e59a1426f86c
keywords:
- Sauvegarde de la fonction SisCreateRestoreStructure
topic_type:
- apiref
api_name:
- SisCreateRestoreStructure
api_location:
- Sisbkup.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4b83ebcdd609b00fdec19666a6915926692a2048
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103843306"
---
# <a name="siscreaterestorestructure-function"></a><span data-ttu-id="cd7e0-104">SisCreateRestoreStructure fonction)</span><span class="sxs-lookup"><span data-stu-id="cd7e0-104">SisCreateRestoreStructure function</span></span>

<span data-ttu-id="cd7e0-105">La fonction **SisCreateRestoreStructure** crée une structure de restauration SIS basée sur les informations fournies.</span><span class="sxs-lookup"><span data-stu-id="cd7e0-105">The **SisCreateRestoreStructure** function creates a SIS restore structure based on the supplied information.</span></span>

## <a name="syntax"></a><span data-ttu-id="cd7e0-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="cd7e0-106">Syntax</span></span>


```C++
BOOL SisCreateRestoreStructure(
  _In_  PWCHAR volumeRoot,
  _Out_ PVOID  *sisRestoreStructure,
  _Out_ PWCHAR *commonStoreRootPathname,
  _Out_ PULONG countOfCommonStoreFilesToRestore,
  _Out_ PWCHAR **commonStoreFilesToRestore
);
```



## <a name="parameters"></a><span data-ttu-id="cd7e0-107">Paramètres</span><span class="sxs-lookup"><span data-stu-id="cd7e0-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="cd7e0-108">*volumeRoot* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="cd7e0-108">*volumeRoot* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="cd7e0-109">Nom de fichier de la racine du volume, sans la barre oblique inverse de fin, du volume à sauvegarder.</span><span class="sxs-lookup"><span data-stu-id="cd7e0-109">File name of the volume root, without the trailing backslash, of the volume to be backed up.</span></span> <span data-ttu-id="cd7e0-110">Par exemple, spécifiez « C : » et non pas « C : \\ ».</span><span class="sxs-lookup"><span data-stu-id="cd7e0-110">For example, specify "C:" and not "C:\\".</span></span> <span data-ttu-id="cd7e0-111">Le volume ne peut pas être le volume système ou de démarrage.</span><span class="sxs-lookup"><span data-stu-id="cd7e0-111">The volume cannot be the system or boot volume.</span></span>

</dd> <dt>

<span data-ttu-id="cd7e0-112">*sisRestoreStructure* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="cd7e0-112">*sisRestoreStructure* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="cd7e0-113">Structure de restauration SIS retournée.</span><span class="sxs-lookup"><span data-stu-id="cd7e0-113">Returned SIS restore structure.</span></span> <span data-ttu-id="cd7e0-114">Cette structure doit être traitée comme opaque par l’appelant.</span><span class="sxs-lookup"><span data-stu-id="cd7e0-114">This structure should be treated as opaque by the caller.</span></span>

</dd> <dt>

<span data-ttu-id="cd7e0-115">*commonStoreRootPathname* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="cd7e0-115">*commonStoreRootPathname* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="cd7e0-116">Nom de chemin d’accès complet du magasin commun du volume spécifié.</span><span class="sxs-lookup"><span data-stu-id="cd7e0-116">Fully qualified path name of the specified volume's common store.</span></span> <span data-ttu-id="cd7e0-117">Par exemple, « c : \\ SIS Common Store ».</span><span class="sxs-lookup"><span data-stu-id="cd7e0-117">For example, "c:\\SIS Common Store".</span></span>

</dd> <dt>

<span data-ttu-id="cd7e0-118">*countOfCommonStoreFilesToRestore* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="cd7e0-118">*countOfCommonStoreFilesToRestore* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="cd7e0-119">Nombre de fichiers listés dans le paramètre *commonStoreFilesToRestore* .</span><span class="sxs-lookup"><span data-stu-id="cd7e0-119">Number of files listed in the *commonStoreFilesToRestore* parameter.</span></span>

</dd> <dt>

<span data-ttu-id="cd7e0-120">*commonStoreFilesToRestore* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="cd7e0-120">*commonStoreFilesToRestore* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="cd7e0-121">Pointeur vers un tableau de noms de fichiers qui spécifie la liste des fichiers internes utilisés par SIS pour gérer le volume spécifié.</span><span class="sxs-lookup"><span data-stu-id="cd7e0-121">Pointer to an array of file names that specifies the list of internal files used by SIS to manage the specified volume.</span></span> <span data-ttu-id="cd7e0-122">Ces fichiers doivent être restaurés en même temps et de la même façon que les fichiers du magasin commun demandés par [**SisCSFilesToBackupForLink**](siscsfilestobackupforlink.md).</span><span class="sxs-lookup"><span data-stu-id="cd7e0-122">These files should be restored at the same time and in the same manner as the common-store files requested by [**SisCSFilesToBackupForLink**](siscsfilestobackupforlink.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="cd7e0-123">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="cd7e0-123">Return value</span></span>

<span data-ttu-id="cd7e0-124">Cette fonction retourne la **valeur true** si elle se termine avec succès et la **valeur false** dans le cas contraire.</span><span class="sxs-lookup"><span data-stu-id="cd7e0-124">This function returns **TRUE** if it completes successfully and **FALSE** otherwise.</span></span> <span data-ttu-id="cd7e0-125">Appelez [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) pour obtenir plus d’informations sur la raison de l’échec de l’appel.</span><span class="sxs-lookup"><span data-stu-id="cd7e0-125">Call [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) to get more information about the reason the call failed.</span></span>

## <a name="remarks"></a><span data-ttu-id="cd7e0-126">Notes</span><span class="sxs-lookup"><span data-stu-id="cd7e0-126">Remarks</span></span>

<span data-ttu-id="cd7e0-127">Cette fonction établit l’environnement de restauration sur le volume spécifié, de la façon dont [**SisCreateBackupStructure**](siscreatebackupstructure.md) établit l’environnement de sauvegarde sur le volume spécifié.</span><span class="sxs-lookup"><span data-stu-id="cd7e0-127">This function establishes the restore environment on the specified volume in the way that [**SisCreateBackupStructure**](siscreatebackupstructure.md) establishes the backup environment on the specified volume.</span></span>

<span data-ttu-id="cd7e0-128">Notez que cette fonction n’identifie pas nécessairement le ou les fichiers du magasin commun qui correspondent à un ensemble de liens SIS sur le support de sauvegarde si ces fichiers ou fichiers du magasin commun existent toujours sur le disque.</span><span class="sxs-lookup"><span data-stu-id="cd7e0-128">Note that this function will not necessarily identify the common-store file or files corresponding to a set of SIS links on the backup media if those common store file or files still exist on disk.</span></span> <span data-ttu-id="cd7e0-129">Le contenu du flux de données d’un fichier du magasin commun n’est jamais modifié une fois qu’il a été créé. par conséquent, si le fichier existe déjà sur le disque, il n’est pas nécessaire de le restaurer.</span><span class="sxs-lookup"><span data-stu-id="cd7e0-129">The contents of a common-store file's data stream never change once it is created, so if the file already exists on the disk there is no need to restore it.</span></span>

<span data-ttu-id="cd7e0-130">Les noms de fichiers Common-Store sont globalement uniques pour garantir l’intégrité de l’opération de restauration, même si elle ne se produit pas sur le même volume SIS que l’opération de sauvegarde a accédé.</span><span class="sxs-lookup"><span data-stu-id="cd7e0-130">Common-store file names are globally unique to ensure the integrity of the restore operation even if it does not occur on the same SIS-enabled volume that the backup operation has accessed.</span></span>

<span data-ttu-id="cd7e0-131">Une fois l’opération de restauration terminée, libérez la mémoire utilisée par le tableau de chaînes *commonStoreFilesToRestore* en appelant [**SisFreeAllocatedMemory**](sisfreeallocatedmemory.md).</span><span class="sxs-lookup"><span data-stu-id="cd7e0-131">After the restore operation is complete, deallocate the memory used by the *commonStoreFilesToRestore* array of strings by calling [**SisFreeAllocatedMemory**](sisfreeallocatedmemory.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="cd7e0-132">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="cd7e0-132">Requirements</span></span>



| <span data-ttu-id="cd7e0-133">Condition requise</span><span class="sxs-lookup"><span data-stu-id="cd7e0-133">Requirement</span></span> | <span data-ttu-id="cd7e0-134">Valeur</span><span class="sxs-lookup"><span data-stu-id="cd7e0-134">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="cd7e0-135">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="cd7e0-135">Minimum supported client</span></span><br/> | <span data-ttu-id="cd7e0-136">Applications de \[ Bureau Windows XP uniquement\]</span><span class="sxs-lookup"><span data-stu-id="cd7e0-136">Windows XP \[desktop apps only\]</span></span><br/>                                            |
| <span data-ttu-id="cd7e0-137">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="cd7e0-137">Minimum supported server</span></span><br/> | <span data-ttu-id="cd7e0-138">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="cd7e0-138">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="cd7e0-139">En-tête</span><span class="sxs-lookup"><span data-stu-id="cd7e0-139">Header</span></span><br/>                   | <dl> <span data-ttu-id="cd7e0-140"><dt>Sisbkup. h</dt></span><span class="sxs-lookup"><span data-stu-id="cd7e0-140"><dt>Sisbkup.h</dt></span></span> </dl>   |
| <span data-ttu-id="cd7e0-141">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="cd7e0-141">Library</span></span><br/>                  | <dl> <span data-ttu-id="cd7e0-142"><dt>Sisbkup. lib</dt></span><span class="sxs-lookup"><span data-stu-id="cd7e0-142"><dt>Sisbkup.lib</dt></span></span> </dl> |
| <span data-ttu-id="cd7e0-143">DLL</span><span class="sxs-lookup"><span data-stu-id="cd7e0-143">DLL</span></span><br/>                      | <dl> <span data-ttu-id="cd7e0-144"><dt>Sisbkup.dll</dt></span><span class="sxs-lookup"><span data-stu-id="cd7e0-144"><dt>Sisbkup.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="cd7e0-145">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="cd7e0-145">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cd7e0-146">**SisCreateBackupStructure**</span><span class="sxs-lookup"><span data-stu-id="cd7e0-146">**SisCreateBackupStructure**</span></span>](siscreatebackupstructure.md)
</dt> <dt>

[<span data-ttu-id="cd7e0-147">**SisCSFilesToBackupForLink**</span><span class="sxs-lookup"><span data-stu-id="cd7e0-147">**SisCSFilesToBackupForLink**</span></span>](siscsfilestobackupforlink.md)
</dt> <dt>

[<span data-ttu-id="cd7e0-148">**SisFreeAllocatedMemory**</span><span class="sxs-lookup"><span data-stu-id="cd7e0-148">**SisFreeAllocatedMemory**</span></span>](sisfreeallocatedmemory.md)
</dt> <dt>

[<span data-ttu-id="cd7e0-149">**SisFreeBackupStructure**</span><span class="sxs-lookup"><span data-stu-id="cd7e0-149">**SisFreeBackupStructure**</span></span>](sisfreebackupstructure.md)
</dt> </dl>

 

