---
title: DsBackupRead, fonction (ntdsbcli. h)
description: Lit un bloc de données à partir du fichier actuellement ouvert dans une mémoire tampon.
ms.assetid: 01576d41-3cd6-4540-966b-7d98561f7b8c
ms.tgt_platform: multiple
keywords:
- Active Directory de la fonction DsBackupRead
topic_type:
- apiref
api_name:
- DsBackupRead
api_location:
- Ntdsbcli.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 409c2a7d93503aad4edff88070c0458efc961d23
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103942033"
---
# <a name="dsbackupread-function"></a><span data-ttu-id="b8508-104">DsBackupRead fonction)</span><span class="sxs-lookup"><span data-stu-id="b8508-104">DsBackupRead function</span></span>

<span data-ttu-id="b8508-105">\[Cette fonction peut être utilisée dans les systèmes d’exploitation spécifiés dans la section Configuration requise.</span><span class="sxs-lookup"><span data-stu-id="b8508-105">\[This function is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="b8508-106">Il sera peut-être modifié ou indisponible dans les versions ultérieures.</span><span class="sxs-lookup"><span data-stu-id="b8508-106">It may be altered or unavailable in subsequent versions.</span></span> <span data-ttu-id="b8508-107">À partir de Windows Vista, utilisez [service VSS (VSS)](../vss/volume-shadow-copy-service-overview.md) à la place.\]</span><span class="sxs-lookup"><span data-stu-id="b8508-107">Beginning with Windows Vista, use [Volume Shadow Copy Service (VSS)](../vss/volume-shadow-copy-service-overview.md) instead.\]</span></span>

<span data-ttu-id="b8508-108">La fonction **DsBackupRead** lit un bloc de données à partir du fichier ouvert actuel, dans une mémoire tampon.</span><span class="sxs-lookup"><span data-stu-id="b8508-108">The **DsBackupRead** function reads a block of data from the current open file, into a buffer.</span></span> <span data-ttu-id="b8508-109">L’application cliente est censée appeler cette fonction à plusieurs reprises jusqu’à ce que l’intégralité du fichier de sauvegarde soit reçue.</span><span class="sxs-lookup"><span data-stu-id="b8508-109">The client application is expected to call this function repeatedly until the entire backup file has been received.</span></span> <span data-ttu-id="b8508-110">La fonction [**DsBackupOpenFile**](dsbackupopenfile.md) fournit la taille totale du fichier de sauvegarde.</span><span class="sxs-lookup"><span data-stu-id="b8508-110">The [**DsBackupOpenFile**](dsbackupopenfile.md) function provides the entire size of the backup file.</span></span>

## <a name="syntax"></a><span data-ttu-id="b8508-111">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="b8508-111">Syntax</span></span>


```C++
HRESULT DsBackupRead(
  _In_  HBC    hbc,
  _In_  PVOID  pvBuffer,
  _In_  DWORD  cbBuffer,
  _Out_ PDWORD pcbRead
);
```



## <a name="parameters"></a><span data-ttu-id="b8508-112">Paramètres</span><span class="sxs-lookup"><span data-stu-id="b8508-112">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b8508-113">*Hbc* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="b8508-113">*hbc* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b8508-114">Contient le descripteur de contexte de sauvegarde obtenu avec la fonction [**DsBackupPrepare**](dsbackupprepare.md) .</span><span class="sxs-lookup"><span data-stu-id="b8508-114">Contains the backup context handle obtained with the [**DsBackupPrepare**](dsbackupprepare.md) function.</span></span>

</dd> <dt>

<span data-ttu-id="b8508-115">*pvBuffer* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="b8508-115">*pvBuffer* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b8508-116">Pointeur vers une mémoire tampon qui reçoit les données.</span><span class="sxs-lookup"><span data-stu-id="b8508-116">Pointer to a buffer that receives the data.</span></span> <span data-ttu-id="b8508-117">La taille de cette mémoire tampon doit être d’au moins *cbBuffer* octets.</span><span class="sxs-lookup"><span data-stu-id="b8508-117">This buffer must be at least *cbBuffer* bytes in size.</span></span>

</dd> <dt>

<span data-ttu-id="b8508-118">*cbBuffer* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="b8508-118">*cbBuffer* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b8508-119">Contient la taille, en octets, de la mémoire tampon à *pvBuffer*.</span><span class="sxs-lookup"><span data-stu-id="b8508-119">Contains the size, in bytes, of the buffer at *pvBuffer*.</span></span> <span data-ttu-id="b8508-120">Cette valeur doit être un multiple de 8192 et doit être supérieur ou égal à 24576.</span><span class="sxs-lookup"><span data-stu-id="b8508-120">This value must be a multiple of 8192 and must be greater than or equal to 24576.</span></span>

</dd> <dt>

<span data-ttu-id="b8508-121">*pcbRead* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="b8508-121">*pcbRead* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="b8508-122">Pointeur vers une valeur **DWORD** qui reçoit le nombre réel d’octets lus.</span><span class="sxs-lookup"><span data-stu-id="b8508-122">Pointer to a **DWORD** value that receives the actual number of bytes read.</span></span> <span data-ttu-id="b8508-123">Ce nombre peut être inférieur au nombre d’octets demandés, car certains transports fragmentent la mémoire tampon en cours de transmission au lieu de remplir l’intégralité de la mémoire tampon avec des données.</span><span class="sxs-lookup"><span data-stu-id="b8508-123">This may be less than the number of bytes requested because some transports fragment the buffer being transmitted instead of filling the entire buffer with data.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b8508-124">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="b8508-124">Return value</span></span>

<span data-ttu-id="b8508-125">Retourne **S \_ OK** si la fonction réussit ou un code d’erreur Win32 ou RPC dans le cas contraire.</span><span class="sxs-lookup"><span data-stu-id="b8508-125">Returns **S\_OK** if the function is successful or a Win32 or RPC error code otherwise.</span></span> <span data-ttu-id="b8508-126">Les codes d’erreur possibles sont les suivants :</span><span class="sxs-lookup"><span data-stu-id="b8508-126">Possible error codes include the following.</span></span>

<dl> <dt>

<span data-ttu-id="b8508-127">**paramètre d’erreur \_ non valide \_**</span><span class="sxs-lookup"><span data-stu-id="b8508-127">**ERROR\_INVALID\_PARAMETER**</span></span>
</dt> <dd>

<span data-ttu-id="b8508-128">Un ou plusieurs paramètres ne sont pas valides.</span><span class="sxs-lookup"><span data-stu-id="b8508-128">One or more parameters are not valid.</span></span>

</dd> <dt>

<span data-ttu-id="b8508-129">**\_EOF de handle d’erreur \_**</span><span class="sxs-lookup"><span data-stu-id="b8508-129">**ERROR\_HANDLE\_EOF**</span></span>
</dt> <dd>

<span data-ttu-id="b8508-130">La fin du fichier de sauvegarde a été atteinte.</span><span class="sxs-lookup"><span data-stu-id="b8508-130">The end of the backup file was reached.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="b8508-131">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="b8508-131">Requirements</span></span>



| <span data-ttu-id="b8508-132">Condition requise</span><span class="sxs-lookup"><span data-stu-id="b8508-132">Requirement</span></span> | <span data-ttu-id="b8508-133">Valeur</span><span class="sxs-lookup"><span data-stu-id="b8508-133">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="b8508-134">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="b8508-134">Minimum supported client</span></span><br/> | <span data-ttu-id="b8508-135">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="b8508-135">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="b8508-136">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="b8508-136">Minimum supported server</span></span><br/> | <span data-ttu-id="b8508-137">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="b8508-137">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="b8508-138">En-tête</span><span class="sxs-lookup"><span data-stu-id="b8508-138">Header</span></span><br/>                   | <dl> <span data-ttu-id="b8508-139"><dt>Ntdsbcli. h</dt></span><span class="sxs-lookup"><span data-stu-id="b8508-139"><dt>Ntdsbcli.h</dt></span></span> </dl>   |
| <span data-ttu-id="b8508-140">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="b8508-140">Library</span></span><br/>                  | <dl> <span data-ttu-id="b8508-141"><dt>Ntdsbcli. lib</dt></span><span class="sxs-lookup"><span data-stu-id="b8508-141"><dt>Ntdsbcli.lib</dt></span></span> </dl> |
| <span data-ttu-id="b8508-142">DLL</span><span class="sxs-lookup"><span data-stu-id="b8508-142">DLL</span></span><br/>                      | <dl> <span data-ttu-id="b8508-143"><dt>Ntdsbcli.dll</dt></span><span class="sxs-lookup"><span data-stu-id="b8508-143"><dt>Ntdsbcli.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b8508-144">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="b8508-144">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b8508-145">**DsBackupOpenFile**</span><span class="sxs-lookup"><span data-stu-id="b8508-145">**DsBackupOpenFile**</span></span>](dsbackupopenfile.md)
</dt> <dt>

[<span data-ttu-id="b8508-146">**DsBackupPrepare**</span><span class="sxs-lookup"><span data-stu-id="b8508-146">**DsBackupPrepare**</span></span>](dsbackupprepare.md)
</dt> <dt>

[<span data-ttu-id="b8508-147">**DsBackupFree**</span><span class="sxs-lookup"><span data-stu-id="b8508-147">**DsBackupFree**</span></span>](dsbackupfree.md)
</dt> <dt>

[<span data-ttu-id="b8508-148">Sauvegarde d’un serveur de Active Directory</span><span class="sxs-lookup"><span data-stu-id="b8508-148">Backing Up an Active Directory Server</span></span>](backing-up-an-active-directory-server.md)
</dt> <dt>

[<span data-ttu-id="b8508-149">Fonctions de sauvegarde d’annuaire</span><span class="sxs-lookup"><span data-stu-id="b8508-149">Directory Backup Functions</span></span>](directory-backup-functions.md)
</dt> </dl>

 

