---
title: DsBackupClose, fonction (ntdsbcli. h)
description: Ferme un fichier de sauvegarde ouvert avec la fonction DsBackupOpenFile.
ms.assetid: 5452a222-abe8-4d2d-84ff-6f577073b220
ms.tgt_platform: multiple
keywords:
- Active Directory de la fonction DsBackupClose
topic_type:
- apiref
api_name:
- DsBackupClose
api_location:
- Ntdsbcli.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c5d03c9cd7f125d223d264236a52120714d5198c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104465070"
---
# <a name="dsbackupclose-function"></a><span data-ttu-id="5d7cb-104">DsBackupClose fonction)</span><span class="sxs-lookup"><span data-stu-id="5d7cb-104">DsBackupClose function</span></span>

<span data-ttu-id="5d7cb-105">\[Cette fonction peut être utilisée dans les systèmes d’exploitation spécifiés dans la section Configuration requise.</span><span class="sxs-lookup"><span data-stu-id="5d7cb-105">\[This function is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="5d7cb-106">Il sera peut-être modifié ou indisponible dans les versions ultérieures.</span><span class="sxs-lookup"><span data-stu-id="5d7cb-106">It may be altered or unavailable in subsequent versions.</span></span> <span data-ttu-id="5d7cb-107">À partir de Windows Vista, utilisez [service VSS (VSS)](../vss/volume-shadow-copy-service-overview.md) à la place.\]</span><span class="sxs-lookup"><span data-stu-id="5d7cb-107">Beginning with Windows Vista, use [Volume Shadow Copy Service (VSS)](../vss/volume-shadow-copy-service-overview.md) instead.\]</span></span>

<span data-ttu-id="5d7cb-108">La fonction **DsBackupClose** ferme un fichier de sauvegarde ouvert avec la fonction [**DsBackupOpenFile**](dsbackupopenfile.md) .</span><span class="sxs-lookup"><span data-stu-id="5d7cb-108">The **DsBackupClose** function closes a backup file opened with the [**DsBackupOpenFile**](dsbackupopenfile.md) function.</span></span> <span data-ttu-id="5d7cb-109">Pour chaque descripteur de sauvegarde, un seul fichier peut être ouvert à la fois. cette fonction ferme donc le fichier actuellement ouvert.</span><span class="sxs-lookup"><span data-stu-id="5d7cb-109">For each backup handle, only one file can be opened at a time, so this function closes the currently open file.</span></span>

## <a name="syntax"></a><span data-ttu-id="5d7cb-110">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="5d7cb-110">Syntax</span></span>


```C++
HRESULT DsBackupClose(
  _In_ HBC hbc
);
```



## <a name="parameters"></a><span data-ttu-id="5d7cb-111">Paramètres</span><span class="sxs-lookup"><span data-stu-id="5d7cb-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5d7cb-112">*Hbc* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="5d7cb-112">*hbc* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5d7cb-113">Contient le descripteur de contexte de sauvegarde obtenu avec la fonction [**DsBackupPrepare**](dsbackupprepare.md) .</span><span class="sxs-lookup"><span data-stu-id="5d7cb-113">Contains the backup context handle obtained with the [**DsBackupPrepare**](dsbackupprepare.md) function.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5d7cb-114">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="5d7cb-114">Return value</span></span>

<span data-ttu-id="5d7cb-115">Retourne **S \_ OK** si la fonction réussit ou un code d’erreur Win32 ou RPC dans le cas contraire.</span><span class="sxs-lookup"><span data-stu-id="5d7cb-115">Returns **S\_OK** if the function is successful or a Win32 or RPC error code otherwise.</span></span> <span data-ttu-id="5d7cb-116">La liste suivante répertorie les autres codes d’erreur possibles.</span><span class="sxs-lookup"><span data-stu-id="5d7cb-116">The following list lists other possible error codes.</span></span>

<dl> <dt>

<span data-ttu-id="5d7cb-117">**paramètre d’erreur \_ non valide \_**</span><span class="sxs-lookup"><span data-stu-id="5d7cb-117">**ERROR\_INVALID\_PARAMETER**</span></span>
</dt> <dd>

<span data-ttu-id="5d7cb-118">*Hbc* n’est pas valide.</span><span class="sxs-lookup"><span data-stu-id="5d7cb-118">*hbc* is not valid.</span></span>

</dd> <dt>

<span data-ttu-id="5d7cb-119">**hrInvalidHandle**</span><span class="sxs-lookup"><span data-stu-id="5d7cb-119">**hrInvalidHandle**</span></span>
</dt> <dd>

<span data-ttu-id="5d7cb-120">Aucun fichier n’est actuellement ouvert.</span><span class="sxs-lookup"><span data-stu-id="5d7cb-120">No file is currently open.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="5d7cb-121">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="5d7cb-121">Requirements</span></span>



| <span data-ttu-id="5d7cb-122">Condition requise</span><span class="sxs-lookup"><span data-stu-id="5d7cb-122">Requirement</span></span> | <span data-ttu-id="5d7cb-123">Valeur</span><span class="sxs-lookup"><span data-stu-id="5d7cb-123">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="5d7cb-124">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="5d7cb-124">Minimum supported client</span></span><br/> | <span data-ttu-id="5d7cb-125">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="5d7cb-125">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="5d7cb-126">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="5d7cb-126">Minimum supported server</span></span><br/> | <span data-ttu-id="5d7cb-127">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="5d7cb-127">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="5d7cb-128">En-tête</span><span class="sxs-lookup"><span data-stu-id="5d7cb-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="5d7cb-129"><dt>Ntdsbcli. h</dt></span><span class="sxs-lookup"><span data-stu-id="5d7cb-129"><dt>Ntdsbcli.h</dt></span></span> </dl>   |
| <span data-ttu-id="5d7cb-130">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="5d7cb-130">Library</span></span><br/>                  | <dl> <span data-ttu-id="5d7cb-131"><dt>Ntdsbcli. lib</dt></span><span class="sxs-lookup"><span data-stu-id="5d7cb-131"><dt>Ntdsbcli.lib</dt></span></span> </dl> |
| <span data-ttu-id="5d7cb-132">DLL</span><span class="sxs-lookup"><span data-stu-id="5d7cb-132">DLL</span></span><br/>                      | <dl> <span data-ttu-id="5d7cb-133"><dt>Ntdsbcli.dll</dt></span><span class="sxs-lookup"><span data-stu-id="5d7cb-133"><dt>Ntdsbcli.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5d7cb-134">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="5d7cb-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5d7cb-135">**DsBackupOpenFile**</span><span class="sxs-lookup"><span data-stu-id="5d7cb-135">**DsBackupOpenFile**</span></span>](dsbackupopenfile.md)
</dt> <dt>

[<span data-ttu-id="5d7cb-136">**DsBackupPrepare**</span><span class="sxs-lookup"><span data-stu-id="5d7cb-136">**DsBackupPrepare**</span></span>](dsbackupprepare.md)
</dt> <dt>

[<span data-ttu-id="5d7cb-137">Sauvegarde d’un serveur de Active Directory</span><span class="sxs-lookup"><span data-stu-id="5d7cb-137">Backing Up an Active Directory Server</span></span>](backing-up-an-active-directory-server.md)
</dt> <dt>

[<span data-ttu-id="5d7cb-138">Fonctions de sauvegarde d’annuaire</span><span class="sxs-lookup"><span data-stu-id="5d7cb-138">Directory Backup Functions</span></span>](directory-backup-functions.md)
</dt> </dl>

 

