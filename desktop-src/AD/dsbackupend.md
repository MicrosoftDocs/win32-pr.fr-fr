---
title: DsBackupEnd, fonction (ntdsbcli. h)
description: Appelé pour terminer une opération de sauvegarde.
ms.assetid: 872645bc-3dbe-4b12-af4f-778d54feb18f
ms.tgt_platform: multiple
keywords:
- Active Directory de la fonction DsBackupEnd
topic_type:
- apiref
api_name:
- DsBackupEnd
api_location:
- Ntdsbcli.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9663eedec7bc298ef594990baababcf2083546e9
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103843450"
---
# <a name="dsbackupend-function"></a><span data-ttu-id="a2ef7-104">DsBackupEnd fonction)</span><span class="sxs-lookup"><span data-stu-id="a2ef7-104">DsBackupEnd function</span></span>

<span data-ttu-id="a2ef7-105">\[Cette fonction peut être utilisée dans les systèmes d’exploitation spécifiés dans la section Configuration requise.</span><span class="sxs-lookup"><span data-stu-id="a2ef7-105">\[This function is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="a2ef7-106">Il sera peut-être modifié ou indisponible dans les versions ultérieures.</span><span class="sxs-lookup"><span data-stu-id="a2ef7-106">It may be altered or unavailable in subsequent versions.</span></span> <span data-ttu-id="a2ef7-107">À partir de Windows Vista, utilisez [service VSS (VSS)](../vss/volume-shadow-copy-service-overview.md) à la place.\]</span><span class="sxs-lookup"><span data-stu-id="a2ef7-107">Beginning with Windows Vista, use [Volume Shadow Copy Service (VSS)](../vss/volume-shadow-copy-service-overview.md) instead.\]</span></span>

<span data-ttu-id="a2ef7-108">La fonction **DsBackupEnd** est appelée pour terminer une opération de sauvegarde.</span><span class="sxs-lookup"><span data-stu-id="a2ef7-108">The **DsBackupEnd** function is called to terminate a backup operation.</span></span>

## <a name="syntax"></a><span data-ttu-id="a2ef7-109">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="a2ef7-109">Syntax</span></span>


```C++
HRESULT DsBackupEnd(
  _In_ HBC hbc
);
```



## <a name="parameters"></a><span data-ttu-id="a2ef7-110">Paramètres</span><span class="sxs-lookup"><span data-stu-id="a2ef7-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a2ef7-111">*Hbc* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="a2ef7-111">*hbc* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a2ef7-112">Contient le descripteur de contexte de sauvegarde obtenu avec la fonction [**DsBackupPrepare**](dsbackupprepare.md) .</span><span class="sxs-lookup"><span data-stu-id="a2ef7-112">Contains the backup context handle obtained with the [**DsBackupPrepare**](dsbackupprepare.md) function.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a2ef7-113">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="a2ef7-113">Return value</span></span>

<span data-ttu-id="a2ef7-114">Retourne **S \_ OK** si la fonction réussit ou un code d’erreur Win32 ou RPC dans le cas contraire.</span><span class="sxs-lookup"><span data-stu-id="a2ef7-114">Returns **S\_OK** if the function is successful or a Win32 or RPC error code otherwise.</span></span> <span data-ttu-id="a2ef7-115">La liste suivante répertorie les autres codes d’erreur possibles.</span><span class="sxs-lookup"><span data-stu-id="a2ef7-115">The following list lists other possible error codes.</span></span>

<dl> <dt>

<span data-ttu-id="a2ef7-116">**paramètre d’erreur \_ non valide \_**</span><span class="sxs-lookup"><span data-stu-id="a2ef7-116">**ERROR\_INVALID\_PARAMETER**</span></span>
</dt> <dd>

<span data-ttu-id="a2ef7-117">*Hbc* n’est pas valide.</span><span class="sxs-lookup"><span data-stu-id="a2ef7-117">*hbc* is not valid.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="a2ef7-118">Notes</span><span class="sxs-lookup"><span data-stu-id="a2ef7-118">Remarks</span></span>

<span data-ttu-id="a2ef7-119">La fonction **DsBackupEnd** ferme les handles de liaison en attente et effectue un nettoyage après une tentative de sauvegarde réussie ou ayant échoué.</span><span class="sxs-lookup"><span data-stu-id="a2ef7-119">The **DsBackupEnd** function closes outstanding binding handles and performs a cleanup after a successful or unsuccessful backup attempt.</span></span>

## <a name="requirements"></a><span data-ttu-id="a2ef7-120">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="a2ef7-120">Requirements</span></span>



| <span data-ttu-id="a2ef7-121">Condition requise</span><span class="sxs-lookup"><span data-stu-id="a2ef7-121">Requirement</span></span> | <span data-ttu-id="a2ef7-122">Valeur</span><span class="sxs-lookup"><span data-stu-id="a2ef7-122">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="a2ef7-123">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="a2ef7-123">Minimum supported client</span></span><br/> | <span data-ttu-id="a2ef7-124">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="a2ef7-124">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="a2ef7-125">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="a2ef7-125">Minimum supported server</span></span><br/> | <span data-ttu-id="a2ef7-126">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="a2ef7-126">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="a2ef7-127">En-tête</span><span class="sxs-lookup"><span data-stu-id="a2ef7-127">Header</span></span><br/>                   | <dl> <span data-ttu-id="a2ef7-128"><dt>Ntdsbcli. h</dt></span><span class="sxs-lookup"><span data-stu-id="a2ef7-128"><dt>Ntdsbcli.h</dt></span></span> </dl>   |
| <span data-ttu-id="a2ef7-129">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="a2ef7-129">Library</span></span><br/>                  | <dl> <span data-ttu-id="a2ef7-130"><dt>Ntdsbcli. lib</dt></span><span class="sxs-lookup"><span data-stu-id="a2ef7-130"><dt>Ntdsbcli.lib</dt></span></span> </dl> |
| <span data-ttu-id="a2ef7-131">DLL</span><span class="sxs-lookup"><span data-stu-id="a2ef7-131">DLL</span></span><br/>                      | <dl> <span data-ttu-id="a2ef7-132"><dt>Ntdsbcli.dll</dt></span><span class="sxs-lookup"><span data-stu-id="a2ef7-132"><dt>Ntdsbcli.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a2ef7-133">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="a2ef7-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a2ef7-134">**DsSetAuthIdentity**</span><span class="sxs-lookup"><span data-stu-id="a2ef7-134">**DsSetAuthIdentity**</span></span>](dssetauthidentity.md)
</dt> <dt>

[<span data-ttu-id="a2ef7-135">Sauvegarde d’un serveur de Active Directory</span><span class="sxs-lookup"><span data-stu-id="a2ef7-135">Backing Up an Active Directory Server</span></span>](backing-up-an-active-directory-server.md)
</dt> <dt>

[<span data-ttu-id="a2ef7-136">Fonctions de sauvegarde d’annuaire</span><span class="sxs-lookup"><span data-stu-id="a2ef7-136">Directory Backup Functions</span></span>](directory-backup-functions.md)
</dt> </dl>

 

