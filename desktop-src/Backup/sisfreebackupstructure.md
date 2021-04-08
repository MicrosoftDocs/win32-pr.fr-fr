---
title: SisFreeBackupStructure, fonction (sisbkup. h)
description: Libère la structure de sauvegarde SIS spécifiée.
ms.assetid: 34d5e919-e4bf-4105-ac15-a2ff5adfbdee
keywords:
- Sauvegarde de la fonction SisFreeBackupStructure
topic_type:
- apiref
api_name:
- SisFreeBackupStructure
api_location:
- Sisbkup.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d3a135c4787ff116ec10efd61fa1492033393c88
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103740693"
---
# <a name="sisfreebackupstructure-function"></a><span data-ttu-id="f320b-104">SisFreeBackupStructure fonction)</span><span class="sxs-lookup"><span data-stu-id="f320b-104">SisFreeBackupStructure function</span></span>

<span data-ttu-id="f320b-105">La fonction **SisFreeBackupStructure** libère la structure de sauvegarde SIS spécifiée.</span><span class="sxs-lookup"><span data-stu-id="f320b-105">The **SisFreeBackupStructure** function frees the specified SIS backup structure.</span></span>

## <a name="syntax"></a><span data-ttu-id="f320b-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="f320b-106">Syntax</span></span>


```C++
BOOL SisFreeBackupStructure(
  _In_ PVOID sisBackupStructure
);
```



## <a name="parameters"></a><span data-ttu-id="f320b-107">Paramètres</span><span class="sxs-lookup"><span data-stu-id="f320b-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f320b-108">*sisBackupStructure* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="f320b-108">*sisBackupStructure* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f320b-109">Pointeur vers la structure de sauvegarde SIS retournée par [**SisCreateBackupStructure**](siscreatebackupstructure.md).</span><span class="sxs-lookup"><span data-stu-id="f320b-109">Pointer to the SIS backup structure returned from [**SisCreateBackupStructure**](siscreatebackupstructure.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f320b-110">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="f320b-110">Return value</span></span>

<span data-ttu-id="f320b-111">Cette fonction retourne la **valeur true** si elle se termine avec succès et la **valeur false** dans le cas contraire.</span><span class="sxs-lookup"><span data-stu-id="f320b-111">This function returns **TRUE** if it completes successfully and **FALSE** otherwise.</span></span> <span data-ttu-id="f320b-112">Appelez [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) pour obtenir plus d’informations sur la raison de l’échec de l’appel.</span><span class="sxs-lookup"><span data-stu-id="f320b-112">Call [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) to get more information about the reason the call failed.</span></span>

## <a name="remarks"></a><span data-ttu-id="f320b-113">Notes</span><span class="sxs-lookup"><span data-stu-id="f320b-113">Remarks</span></span>

<span data-ttu-id="f320b-114">Cette fonction doit être appelée une fois que l’opération de sauvegarde est terminée pour le volume identifié par la valeur du paramètre *sisBackupStructure* .</span><span class="sxs-lookup"><span data-stu-id="f320b-114">This function should be called after the backup operation is completed for the volume identified by the value of the *sisBackupStructure* parameter.</span></span>

<span data-ttu-id="f320b-115">Notez qu’il n’est pas possible de supposer que cela libère uniquement de la mémoire.</span><span class="sxs-lookup"><span data-stu-id="f320b-115">Note that it is not safe to assume that this only deallocates memory.</span></span> <span data-ttu-id="f320b-116">Par exemple, cette fonction peut également effectuer des opérations administratives supplémentaires pour l’architecture SIS.</span><span class="sxs-lookup"><span data-stu-id="f320b-116">For example, this function may also perform additional administrative operations for the SIS architecture.</span></span> <span data-ttu-id="f320b-117">Par conséquent, appelez cette fonction même si votre opération de sauvegarde se termine immédiatement après.</span><span class="sxs-lookup"><span data-stu-id="f320b-117">Therefore, call this function even if your backup operation will exit immediately afterward.</span></span>

## <a name="requirements"></a><span data-ttu-id="f320b-118">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="f320b-118">Requirements</span></span>



| <span data-ttu-id="f320b-119">Condition requise</span><span class="sxs-lookup"><span data-stu-id="f320b-119">Requirement</span></span> | <span data-ttu-id="f320b-120">Valeur</span><span class="sxs-lookup"><span data-stu-id="f320b-120">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="f320b-121">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="f320b-121">Minimum supported client</span></span><br/> | <span data-ttu-id="f320b-122">Applications de \[ Bureau Windows XP uniquement\]</span><span class="sxs-lookup"><span data-stu-id="f320b-122">Windows XP \[desktop apps only\]</span></span><br/>                                            |
| <span data-ttu-id="f320b-123">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="f320b-123">Minimum supported server</span></span><br/> | <span data-ttu-id="f320b-124">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="f320b-124">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="f320b-125">En-tête</span><span class="sxs-lookup"><span data-stu-id="f320b-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="f320b-126"><dt>Sisbkup. h</dt></span><span class="sxs-lookup"><span data-stu-id="f320b-126"><dt>Sisbkup.h</dt></span></span> </dl>   |
| <span data-ttu-id="f320b-127">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="f320b-127">Library</span></span><br/>                  | <dl> <span data-ttu-id="f320b-128"><dt>Sisbkup. lib</dt></span><span class="sxs-lookup"><span data-stu-id="f320b-128"><dt>Sisbkup.lib</dt></span></span> </dl> |
| <span data-ttu-id="f320b-129">DLL</span><span class="sxs-lookup"><span data-stu-id="f320b-129">DLL</span></span><br/>                      | <dl> <span data-ttu-id="f320b-130"><dt>Sisbkup.dll</dt></span><span class="sxs-lookup"><span data-stu-id="f320b-130"><dt>Sisbkup.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f320b-131">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="f320b-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f320b-132">**SisCreateBackupStructure**</span><span class="sxs-lookup"><span data-stu-id="f320b-132">**SisCreateBackupStructure**</span></span>](siscreatebackupstructure.md)
</dt> </dl>

 

