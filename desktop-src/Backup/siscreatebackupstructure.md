---
title: SisCreateBackupStructure, fonction (sisbkup. h)
description: Crée une structure de sauvegarde SIS basée sur les informations fournies.
ms.assetid: a8c48961-fa24-4eb6-92cd-1b9bc83cec41
keywords:
- Sauvegarde de la fonction SisCreateBackupStructure
topic_type:
- apiref
api_name:
- SisCreateBackupStructure
api_location:
- Sisbkup.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ad432095f9d264e124df1d84070056fc827c625e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104464782"
---
# <a name="siscreatebackupstructure-function"></a><span data-ttu-id="e05d4-104">SisCreateBackupStructure fonction)</span><span class="sxs-lookup"><span data-stu-id="e05d4-104">SisCreateBackupStructure function</span></span>

<span data-ttu-id="e05d4-105">La fonction **SisCreateBackupStructure** crée une structure de sauvegarde SIS basée sur les informations fournies.</span><span class="sxs-lookup"><span data-stu-id="e05d4-105">The **SisCreateBackupStructure** function creates a SIS backup structure based on the supplied information.</span></span>

## <a name="syntax"></a><span data-ttu-id="e05d4-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="e05d4-106">Syntax</span></span>


```C++
BOOL SisCreateBackupStructure(
  _In_  PWCHAR volumeRoot,
  _Out_ PVOID  *sisBackupStructure,
  _Out_ PWCHAR *commonStoreRootPathname,
  _Out_ PULONG countOfCommonStoreFilesToBackUp,
  _Out_ PWCHAR **commonStoreFilesToBackUp
);
```



## <a name="parameters"></a><span data-ttu-id="e05d4-107">Paramètres</span><span class="sxs-lookup"><span data-stu-id="e05d4-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e05d4-108">*volumeRoot* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="e05d4-108">*volumeRoot* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e05d4-109">Nom de fichier de la racine du volume, sans la barre oblique inverse de fin, du volume à sauvegarder.</span><span class="sxs-lookup"><span data-stu-id="e05d4-109">File name of the volume root, without the trailing backslash, of the volume to be backed up.</span></span> <span data-ttu-id="e05d4-110">Par exemple, spécifiez « C : » et non pas « C : \\ ».</span><span class="sxs-lookup"><span data-stu-id="e05d4-110">For example, specify "C:" and not "C:\\".</span></span>

</dd> <dt>

<span data-ttu-id="e05d4-111">*sisBackupStructure* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="e05d4-111">*sisBackupStructure* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="e05d4-112">Structure de sauvegarde SIS retournée.</span><span class="sxs-lookup"><span data-stu-id="e05d4-112">Returned SIS backup structure.</span></span>

</dd> <dt>

<span data-ttu-id="e05d4-113">*commonStoreRootPathname* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="e05d4-113">*commonStoreRootPathname* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="e05d4-114">Nom de chemin d’accès complet du magasin commun du volume spécifié.</span><span class="sxs-lookup"><span data-stu-id="e05d4-114">Fully qualified path name of the specified volume's common store.</span></span> <span data-ttu-id="e05d4-115">Par exemple, « c : \\ SIS Common Store ».</span><span class="sxs-lookup"><span data-stu-id="e05d4-115">For example, "c:\\SIS Common Store".</span></span>

</dd> <dt>

<span data-ttu-id="e05d4-116">*countOfCommonStoreFilesToBackUp* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="e05d4-116">*countOfCommonStoreFilesToBackUp* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="e05d4-117">Nombre de fichiers listés dans le paramètre *commonStoreFilesToBackUp* .</span><span class="sxs-lookup"><span data-stu-id="e05d4-117">Number of files listed in the *commonStoreFilesToBackUp* parameter.</span></span>

</dd> <dt>

<span data-ttu-id="e05d4-118">*commonStoreFilesToBackUp* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="e05d4-118">*commonStoreFilesToBackUp* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="e05d4-119">Pointeur vers un tableau de noms de fichiers qui spécifie une liste de fichiers internes utilisés par SIS pour gérer le volume spécifié.</span><span class="sxs-lookup"><span data-stu-id="e05d4-119">Pointer to an array of file names that specifies a list of internal files used by SIS to manage the specified volume.</span></span> <span data-ttu-id="e05d4-120">Ces fichiers doivent être sauvegardés en même temps et de la même façon que les fichiers du magasin commun demandés par [ **SisCSFilesToBackupForLink**](siscsfilestobackupforlink.md)</span><span class="sxs-lookup"><span data-stu-id="e05d4-120">These files should be backed up at the same time and in the same manner as the common-store files requested by [**SisCSFilesToBackupForLink**](siscsfilestobackupforlink.md)</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e05d4-121">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="e05d4-121">Return value</span></span>

<span data-ttu-id="e05d4-122">Cette fonction retourne la **valeur true** si elle se termine avec succès et la **valeur false** dans le cas contraire.</span><span class="sxs-lookup"><span data-stu-id="e05d4-122">This function returns **TRUE** if it completes successfully and **FALSE** otherwise.</span></span> <span data-ttu-id="e05d4-123">Appelez [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) pour obtenir plus d’informations sur la raison de l’échec de l’appel.</span><span class="sxs-lookup"><span data-stu-id="e05d4-123">Call [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) to get more information about the reason the call failed.</span></span>

## <a name="remarks"></a><span data-ttu-id="e05d4-124">Notes</span><span class="sxs-lookup"><span data-stu-id="e05d4-124">Remarks</span></span>

<span data-ttu-id="e05d4-125">Cette fonction crée une structure de sauvegarde SIS, qui est utilisée par l’API de sauvegarde SIS pour créer et tenir à jour une liste des liens de fichiers sur le volume et les fichiers d’origine vers lesquels pointent les liens.</span><span class="sxs-lookup"><span data-stu-id="e05d4-125">This function creates a SIS backup structure, which is used by the SIS backup API to create and maintain a list of the file links on the volume and the original files the links point to.</span></span> <span data-ttu-id="e05d4-126">Cette fonction ne doit être appelée qu’une seule fois pour chaque volume compatible SIS en cours de sauvegarde.</span><span class="sxs-lookup"><span data-stu-id="e05d4-126">This function should be called only once for each SIS-enabled volume being backed up.</span></span> <span data-ttu-id="e05d4-127">Tous les fichiers du volume spécifié doivent être traités comme des fichiers de stockage commun et sauvegardés uniquement si SIS indique qu’ils le doivent.</span><span class="sxs-lookup"><span data-stu-id="e05d4-127">All files within the specified volume should be treated as common-store files and backed up only if SIS indicates that they should.</span></span>

<span data-ttu-id="e05d4-128">Les paramètres *countOfCommonStoreFilesToBackUp* et *commonStoreFilesToBackUp* retournent ensemble une liste des fichiers qui doivent être sauvegardés, quels que soient les liens sauvegardés.</span><span class="sxs-lookup"><span data-stu-id="e05d4-128">The *countOfCommonStoreFilesToBackUp* and *commonStoreFilesToBackUp* parameters together return a list of files that must be backed up regardless of which links are backed up.</span></span>

<span data-ttu-id="e05d4-129">Si *countOfCommonStoreFilesToBackUp* a la valeur 0, *commonStoreFilesToBackUp* peut être un pointeur **null** .</span><span class="sxs-lookup"><span data-stu-id="e05d4-129">If *countOfCommonStoreFilesToBackUp* is 0, *commonStoreFilesToBackUp* may be a **NULL** pointer.</span></span> <span data-ttu-id="e05d4-130">La valeur du paramètre *commonStoreFilesToBackUp* doit être ignorée.</span><span class="sxs-lookup"><span data-stu-id="e05d4-130">The value of the *commonStoreFilesToBackUp* parameter should be ignored.</span></span>

<span data-ttu-id="e05d4-131">Une fois l’opération de sauvegarde terminée, Désallouez la mémoire utilisée par le tableau de chaînes *commonStoreFilesToBackUp* en appelant [**SisFreeAllocatedMemory**](sisfreeallocatedmemory.md).</span><span class="sxs-lookup"><span data-stu-id="e05d4-131">After the backup operation is complete, deallocate the memory used by the *commonStoreFilesToBackUp* array of strings by calling [**SisFreeAllocatedMemory**](sisfreeallocatedmemory.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="e05d4-132">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="e05d4-132">Requirements</span></span>



| <span data-ttu-id="e05d4-133">Condition requise</span><span class="sxs-lookup"><span data-stu-id="e05d4-133">Requirement</span></span> | <span data-ttu-id="e05d4-134">Valeur</span><span class="sxs-lookup"><span data-stu-id="e05d4-134">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="e05d4-135">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="e05d4-135">Minimum supported client</span></span><br/> | <span data-ttu-id="e05d4-136">Applications de \[ Bureau Windows XP uniquement\]</span><span class="sxs-lookup"><span data-stu-id="e05d4-136">Windows XP \[desktop apps only\]</span></span><br/>                                            |
| <span data-ttu-id="e05d4-137">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="e05d4-137">Minimum supported server</span></span><br/> | <span data-ttu-id="e05d4-138">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="e05d4-138">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="e05d4-139">En-tête</span><span class="sxs-lookup"><span data-stu-id="e05d4-139">Header</span></span><br/>                   | <dl> <span data-ttu-id="e05d4-140"><dt>Sisbkup. h</dt></span><span class="sxs-lookup"><span data-stu-id="e05d4-140"><dt>Sisbkup.h</dt></span></span> </dl>   |
| <span data-ttu-id="e05d4-141">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="e05d4-141">Library</span></span><br/>                  | <dl> <span data-ttu-id="e05d4-142"><dt>Sisbkup. lib</dt></span><span class="sxs-lookup"><span data-stu-id="e05d4-142"><dt>Sisbkup.lib</dt></span></span> </dl> |
| <span data-ttu-id="e05d4-143">DLL</span><span class="sxs-lookup"><span data-stu-id="e05d4-143">DLL</span></span><br/>                      | <dl> <span data-ttu-id="e05d4-144"><dt>Sisbkup.dll</dt></span><span class="sxs-lookup"><span data-stu-id="e05d4-144"><dt>Sisbkup.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e05d4-145">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="e05d4-145">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e05d4-146">**SisCreateRestoreStructure**</span><span class="sxs-lookup"><span data-stu-id="e05d4-146">**SisCreateRestoreStructure**</span></span>](siscreaterestorestructure.md)
</dt> <dt>

[<span data-ttu-id="e05d4-147">**SisCSFilesToBackupForLink**</span><span class="sxs-lookup"><span data-stu-id="e05d4-147">**SisCSFilesToBackupForLink**</span></span>](siscsfilestobackupforlink.md)
</dt> <dt>

[<span data-ttu-id="e05d4-148">**SisFreeAllocatedMemory**</span><span class="sxs-lookup"><span data-stu-id="e05d4-148">**SisFreeAllocatedMemory**</span></span>](sisfreeallocatedmemory.md)
</dt> </dl>

 

