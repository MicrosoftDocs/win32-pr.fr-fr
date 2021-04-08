---
title: DsBackupFree, fonction (ntdsbcli. h)
description: Libère la mémoire allouée par les fonctions de sauvegarde et de restauration Active Directory Domain Services.
ms.assetid: cde2a530-60e6-440c-9d4e-a90d55846973
ms.tgt_platform: multiple
keywords:
- Active Directory de la fonction DsBackupFree
topic_type:
- apiref
api_name:
- DsBackupFree
api_location:
- Ntdsbcli.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 27855eeb3417eede371357528457248857c3e626
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103843449"
---
# <a name="dsbackupfree-function"></a><span data-ttu-id="65920-104">DsBackupFree fonction)</span><span class="sxs-lookup"><span data-stu-id="65920-104">DsBackupFree function</span></span>

<span data-ttu-id="65920-105">\[Cette fonction peut être utilisée dans les systèmes d’exploitation spécifiés dans la section Configuration requise.</span><span class="sxs-lookup"><span data-stu-id="65920-105">\[This function is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="65920-106">Il sera peut-être modifié ou indisponible dans les versions ultérieures.</span><span class="sxs-lookup"><span data-stu-id="65920-106">It may be altered or unavailable in subsequent versions.</span></span> <span data-ttu-id="65920-107">À partir de Windows Vista, utilisez [service VSS (VSS)](../vss/volume-shadow-copy-service-overview.md) à la place.\]</span><span class="sxs-lookup"><span data-stu-id="65920-107">Beginning with Windows Vista, use [Volume Shadow Copy Service (VSS)](../vss/volume-shadow-copy-service-overview.md) instead.\]</span></span>

<span data-ttu-id="65920-108">La fonction **DsBackupFree** libère la mémoire allouée par les fonctions de sauvegarde et de restauration Active Directory Domain Services.</span><span class="sxs-lookup"><span data-stu-id="65920-108">The **DsBackupFree** function releases memory allocated by the Active Directory Domain Services backup and restore functions.</span></span> <span data-ttu-id="65920-109">Les fonctions suivantes allouent de la mémoire qui doit être libérée avec la fonction **DsBackupFree** .</span><span class="sxs-lookup"><span data-stu-id="65920-109">The following functions allocate memory that must be released with the **DsBackupFree** function.</span></span>

-   [<span data-ttu-id="65920-110">**DsBackupGetBackupLogs**</span><span class="sxs-lookup"><span data-stu-id="65920-110">**DsBackupGetBackupLogs**</span></span>](dsbackupgetbackuplogs.md)
-   [<span data-ttu-id="65920-111">**DsBackupGetDatabaseNames**</span><span class="sxs-lookup"><span data-stu-id="65920-111">**DsBackupGetDatabaseNames**</span></span>](dsbackupgetdatabasenames.md)
-   [<span data-ttu-id="65920-112">**DsBackupPrepare**</span><span class="sxs-lookup"><span data-stu-id="65920-112">**DsBackupPrepare**</span></span>](dsbackupprepare.md)
-   [<span data-ttu-id="65920-113">**DsRestoreGetDatabaseLocations**</span><span class="sxs-lookup"><span data-stu-id="65920-113">**DsRestoreGetDatabaseLocations**</span></span>](dsrestoregetdatabaselocations.md)

## <a name="syntax"></a><span data-ttu-id="65920-114">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="65920-114">Syntax</span></span>


```C++
VOID NTDSBCLI_API DsBackupFree(
  _In_ PVOID pvBuffer
);
```



## <a name="parameters"></a><span data-ttu-id="65920-115">Paramètres</span><span class="sxs-lookup"><span data-stu-id="65920-115">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="65920-116">*pvBuffer* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="65920-116">*pvBuffer* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="65920-117">Pointeur vers la mémoire tampon à libérer.</span><span class="sxs-lookup"><span data-stu-id="65920-117">Pointer to the memory buffer to be freed.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="65920-118">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="65920-118">Return value</span></span>

<span data-ttu-id="65920-119">Cette fonction ne retourne pas de valeur.</span><span class="sxs-lookup"><span data-stu-id="65920-119">This function does not return a value.</span></span>

## <a name="requirements"></a><span data-ttu-id="65920-120">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="65920-120">Requirements</span></span>



| <span data-ttu-id="65920-121">Condition requise</span><span class="sxs-lookup"><span data-stu-id="65920-121">Requirement</span></span> | <span data-ttu-id="65920-122">Valeur</span><span class="sxs-lookup"><span data-stu-id="65920-122">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="65920-123">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="65920-123">Minimum supported client</span></span><br/> | <span data-ttu-id="65920-124">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="65920-124">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="65920-125">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="65920-125">Minimum supported server</span></span><br/> | <span data-ttu-id="65920-126">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="65920-126">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="65920-127">En-tête</span><span class="sxs-lookup"><span data-stu-id="65920-127">Header</span></span><br/>                   | <dl> <span data-ttu-id="65920-128"><dt>Ntdsbcli. h</dt></span><span class="sxs-lookup"><span data-stu-id="65920-128"><dt>Ntdsbcli.h</dt></span></span> </dl>   |
| <span data-ttu-id="65920-129">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="65920-129">Library</span></span><br/>                  | <dl> <span data-ttu-id="65920-130"><dt>Ntdsbcli. lib</dt></span><span class="sxs-lookup"><span data-stu-id="65920-130"><dt>Ntdsbcli.lib</dt></span></span> </dl> |
| <span data-ttu-id="65920-131">DLL</span><span class="sxs-lookup"><span data-stu-id="65920-131">DLL</span></span><br/>                      | <dl> <span data-ttu-id="65920-132"><dt>Ntdsbcli.dll</dt></span><span class="sxs-lookup"><span data-stu-id="65920-132"><dt>Ntdsbcli.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="65920-133">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="65920-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="65920-134">**DsBackupGetBackupLogs**</span><span class="sxs-lookup"><span data-stu-id="65920-134">**DsBackupGetBackupLogs**</span></span>](dsbackupgetbackuplogs.md)
</dt> <dt>

[<span data-ttu-id="65920-135">**DsBackupGetDatabaseNames**</span><span class="sxs-lookup"><span data-stu-id="65920-135">**DsBackupGetDatabaseNames**</span></span>](dsbackupgetdatabasenames.md)
</dt> <dt>

[<span data-ttu-id="65920-136">**DsBackupPrepare**</span><span class="sxs-lookup"><span data-stu-id="65920-136">**DsBackupPrepare**</span></span>](dsbackupprepare.md)
</dt> <dt>

[<span data-ttu-id="65920-137">**DsRestoreGetDatabaseLocations**</span><span class="sxs-lookup"><span data-stu-id="65920-137">**DsRestoreGetDatabaseLocations**</span></span>](dsrestoregetdatabaselocations.md)
</dt> <dt>

[<span data-ttu-id="65920-138">Sauvegarde d’un serveur de Active Directory</span><span class="sxs-lookup"><span data-stu-id="65920-138">Backing Up an Active Directory Server</span></span>](backing-up-an-active-directory-server.md)
</dt> <dt>

[<span data-ttu-id="65920-139">Fonctions de sauvegarde d’annuaire</span><span class="sxs-lookup"><span data-stu-id="65920-139">Directory Backup Functions</span></span>](directory-backup-functions.md)
</dt> </dl>

 

