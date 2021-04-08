---
title: SisFreeAllocatedMemory, fonction (sisbkup. h)
description: Libère la mémoire allouée par les fonctions d’API SIS.
ms.assetid: 8fab79c8-593c-46df-a885-09a59620a977
keywords:
- Sauvegarde de la fonction SisFreeAllocatedMemory
topic_type:
- apiref
api_name:
- SisFreeAllocatedMemory
api_location:
- Sisbkup.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 724970817b89f6a9f2490b0776775f6a3a4e69ca
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103843305"
---
# <a name="sisfreeallocatedmemory-function"></a><span data-ttu-id="8d48e-104">SisFreeAllocatedMemory fonction)</span><span class="sxs-lookup"><span data-stu-id="8d48e-104">SisFreeAllocatedMemory function</span></span>

<span data-ttu-id="8d48e-105">La fonction **SisFreeAllocatedMemory** libère de la mémoire allouée par les fonctions d’API SIS.</span><span class="sxs-lookup"><span data-stu-id="8d48e-105">The **SisFreeAllocatedMemory** function frees memory allocated by SIS API functions.</span></span>

## <a name="syntax"></a><span data-ttu-id="8d48e-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="8d48e-106">Syntax</span></span>


```C++
void SisFreeAllocatedMemory(
  _In_ PVOID allocatedSpace
);
```



## <a name="parameters"></a><span data-ttu-id="8d48e-107">Paramètres</span><span class="sxs-lookup"><span data-stu-id="8d48e-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8d48e-108">*allocatedSpace* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="8d48e-108">*allocatedSpace* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8d48e-109">Pointeur vers la mémoire allouée par l’API SIS.</span><span class="sxs-lookup"><span data-stu-id="8d48e-109">Pointer to the memory allocated by the SIS API.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8d48e-110">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="8d48e-110">Return value</span></span>

<span data-ttu-id="8d48e-111">Cette fonction ne retourne pas de valeur.</span><span class="sxs-lookup"><span data-stu-id="8d48e-111">This function does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="8d48e-112">Notes</span><span class="sxs-lookup"><span data-stu-id="8d48e-112">Remarks</span></span>

<span data-ttu-id="8d48e-113">Une fois l’appel à cette fonction terminé, l’appelant ne peut plus accéder à la mémoire libérée.</span><span class="sxs-lookup"><span data-stu-id="8d48e-113">After the call to this function completes, the caller may no longer access the freed memory.</span></span>

<span data-ttu-id="8d48e-114">Cet appel doit être utilisé pour libérer la mémoire allouée pour les chaînes de paramètres *commonStoreRootPathname* retournées à partir de [**SisCreateBackupStructure**](siscreatebackupstructure.md) et [**SisCreateRestoreStructure**](siscreaterestorestructure.md), et le tableau de chaînes contenant des noms de fichiers de magasin commun retournés à partir de **SisCreateBackupStructure**, [**SisCSFilesToBackupForLink**](siscsfilestobackupforlink.md), **SisCreateRestoreStructure** et [**SisRestoredLink**](sisrestoredlink.md).</span><span class="sxs-lookup"><span data-stu-id="8d48e-114">This call should be used to deallocate the memory allocated for the *commonStoreRootPathname* parameter strings returned from [**SisCreateBackupStructure**](siscreatebackupstructure.md) and [**SisCreateRestoreStructure**](siscreaterestorestructure.md), and the array of strings containing common-store file names returned from **SisCreateBackupStructure**, [**SisCSFilesToBackupForLink**](siscsfilestobackupforlink.md), **SisCreateRestoreStructure**, and [**SisRestoredLink**](sisrestoredlink.md).</span></span> <span data-ttu-id="8d48e-115">Dans ce dernier cas, le tableau lui-même doit également être libéré en appelant **SisFreeAllocatedMemory**.</span><span class="sxs-lookup"><span data-stu-id="8d48e-115">In the latter case, the array itself also must be freed by calling **SisFreeAllocatedMemory**.</span></span>

## <a name="requirements"></a><span data-ttu-id="8d48e-116">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="8d48e-116">Requirements</span></span>



| <span data-ttu-id="8d48e-117">Condition requise</span><span class="sxs-lookup"><span data-stu-id="8d48e-117">Requirement</span></span> | <span data-ttu-id="8d48e-118">Valeur</span><span class="sxs-lookup"><span data-stu-id="8d48e-118">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="8d48e-119">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="8d48e-119">Minimum supported client</span></span><br/> | <span data-ttu-id="8d48e-120">Applications de \[ Bureau Windows XP uniquement\]</span><span class="sxs-lookup"><span data-stu-id="8d48e-120">Windows XP \[desktop apps only\]</span></span><br/>                                            |
| <span data-ttu-id="8d48e-121">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="8d48e-121">Minimum supported server</span></span><br/> | <span data-ttu-id="8d48e-122">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="8d48e-122">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="8d48e-123">En-tête</span><span class="sxs-lookup"><span data-stu-id="8d48e-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="8d48e-124"><dt>Sisbkup. h</dt></span><span class="sxs-lookup"><span data-stu-id="8d48e-124"><dt>Sisbkup.h</dt></span></span> </dl>   |
| <span data-ttu-id="8d48e-125">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="8d48e-125">Library</span></span><br/>                  | <dl> <span data-ttu-id="8d48e-126"><dt>Sisbkup. lib</dt></span><span class="sxs-lookup"><span data-stu-id="8d48e-126"><dt>Sisbkup.lib</dt></span></span> </dl> |
| <span data-ttu-id="8d48e-127">DLL</span><span class="sxs-lookup"><span data-stu-id="8d48e-127">DLL</span></span><br/>                      | <dl> <span data-ttu-id="8d48e-128"><dt>Sisbkup.dll</dt></span><span class="sxs-lookup"><span data-stu-id="8d48e-128"><dt>Sisbkup.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8d48e-129">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="8d48e-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8d48e-130">**SisCreateBackupStructure**</span><span class="sxs-lookup"><span data-stu-id="8d48e-130">**SisCreateBackupStructure**</span></span>](siscreatebackupstructure.md)
</dt> <dt>

[<span data-ttu-id="8d48e-131">**SisCreateRestoreStructure**</span><span class="sxs-lookup"><span data-stu-id="8d48e-131">**SisCreateRestoreStructure**</span></span>](siscreaterestorestructure.md)
</dt> <dt>

[<span data-ttu-id="8d48e-132">**SisCSFilesToBackupForLink**</span><span class="sxs-lookup"><span data-stu-id="8d48e-132">**SisCSFilesToBackupForLink**</span></span>](siscsfilestobackupforlink.md)
</dt> <dt>

[<span data-ttu-id="8d48e-133">**SisRestoredLink**</span><span class="sxs-lookup"><span data-stu-id="8d48e-133">**SisRestoredLink**</span></span>](sisrestoredlink.md)
</dt> </dl>

 

 





