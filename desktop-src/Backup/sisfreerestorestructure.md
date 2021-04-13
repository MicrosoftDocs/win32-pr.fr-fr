---
title: SisFreeRestoreStructure, fonction (sisbkup. h)
description: Libère la mémoire allouée pour la structure de restauration SIS spécifiée et effectue des tâches qui préparent le filtre SIS à configurer correctement les liens créés lors de l’opération de restauration.
ms.assetid: dbdccb53-b38e-465d-a6d0-ee86923a5879
keywords:
- Sauvegarde de la fonction SisFreeRestoreStructure
topic_type:
- apiref
api_name:
- SisFreeRestoreStructure
api_location:
- Sisbkup.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7293514d798fe65c82863a83549039b05ec8eb3e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104466650"
---
# <a name="sisfreerestorestructure-function"></a><span data-ttu-id="0d97e-104">SisFreeRestoreStructure fonction)</span><span class="sxs-lookup"><span data-stu-id="0d97e-104">SisFreeRestoreStructure function</span></span>

<span data-ttu-id="0d97e-105">La fonction **SisFreeRestoreStructure** libère la mémoire allouée pour la structure de restauration SIS spécifiée et effectue des tâches qui préparent le filtre sis à configurer correctement les liens créés lors de l’opération de restauration.</span><span class="sxs-lookup"><span data-stu-id="0d97e-105">The **SisFreeRestoreStructure** function frees the memory allocated for the specified SIS restore structure, and performs tasks that prepare the SIS filter to properly set up the links created during the restore operation.</span></span>

## <a name="syntax"></a><span data-ttu-id="0d97e-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="0d97e-106">Syntax</span></span>


```C++
BOOL SisFreeRestoreStructure(
  _In_ PVOID sisRestoreStructure
);
```



## <a name="parameters"></a><span data-ttu-id="0d97e-107">Paramètres</span><span class="sxs-lookup"><span data-stu-id="0d97e-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0d97e-108">*sisRestoreStructure* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="0d97e-108">*sisRestoreStructure* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0d97e-109">Pointeur vers une structure de restauration SIS retournée à partir de [**SisCreateRestoreStructure**](siscreaterestorestructure.md).</span><span class="sxs-lookup"><span data-stu-id="0d97e-109">Pointer to a SIS restore structure returned from [**SisCreateRestoreStructure**](siscreaterestorestructure.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0d97e-110">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="0d97e-110">Return value</span></span>

<span data-ttu-id="0d97e-111">Cette fonction retourne la **valeur true** si elle se termine avec succès et la **valeur false** dans le cas contraire.</span><span class="sxs-lookup"><span data-stu-id="0d97e-111">This function returns **TRUE** if it completes successfully and **FALSE** otherwise.</span></span> <span data-ttu-id="0d97e-112">Appelez [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) pour obtenir plus d’informations sur la raison de l’échec de l’appel.</span><span class="sxs-lookup"><span data-stu-id="0d97e-112">Call [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) to get more information about the reason the call failed.</span></span>

## <a name="remarks"></a><span data-ttu-id="0d97e-113">Notes</span><span class="sxs-lookup"><span data-stu-id="0d97e-113">Remarks</span></span>

<span data-ttu-id="0d97e-114">L’accès aux liens SIS avant l’exécution de l’appel à cette fonction peut entraîner une vérification du volume ou une lecture partielle du contenu du lien.</span><span class="sxs-lookup"><span data-stu-id="0d97e-114">Accessing the SIS links before the call to this function completes can result in a volume check or a partial read of the link's contents.</span></span>

<span data-ttu-id="0d97e-115">Notez qu’il n’est pas possible de supposer que cela libère uniquement de la mémoire.</span><span class="sxs-lookup"><span data-stu-id="0d97e-115">Note that it is not safe to assume that this only deallocates memory.</span></span> <span data-ttu-id="0d97e-116">Par exemple, cette fonction peut également effectuer des opérations administratives supplémentaires pour l’architecture SIS.</span><span class="sxs-lookup"><span data-stu-id="0d97e-116">For example, this function may also perform additional administrative operations for the SIS architecture.</span></span> <span data-ttu-id="0d97e-117">Par conséquent, appelez cette fonction même si votre opération de restauration se termine immédiatement après.</span><span class="sxs-lookup"><span data-stu-id="0d97e-117">Therefore, call this function even if your restore operation will exit immediately afterward.</span></span>

## <a name="requirements"></a><span data-ttu-id="0d97e-118">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="0d97e-118">Requirements</span></span>



| <span data-ttu-id="0d97e-119">Condition requise</span><span class="sxs-lookup"><span data-stu-id="0d97e-119">Requirement</span></span> | <span data-ttu-id="0d97e-120">Valeur</span><span class="sxs-lookup"><span data-stu-id="0d97e-120">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="0d97e-121">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="0d97e-121">Minimum supported client</span></span><br/> | <span data-ttu-id="0d97e-122">Applications de \[ Bureau Windows XP uniquement\]</span><span class="sxs-lookup"><span data-stu-id="0d97e-122">Windows XP \[desktop apps only\]</span></span><br/>                                            |
| <span data-ttu-id="0d97e-123">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="0d97e-123">Minimum supported server</span></span><br/> | <span data-ttu-id="0d97e-124">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="0d97e-124">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="0d97e-125">En-tête</span><span class="sxs-lookup"><span data-stu-id="0d97e-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="0d97e-126"><dt>Sisbkup. h</dt></span><span class="sxs-lookup"><span data-stu-id="0d97e-126"><dt>Sisbkup.h</dt></span></span> </dl>   |
| <span data-ttu-id="0d97e-127">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="0d97e-127">Library</span></span><br/>                  | <dl> <span data-ttu-id="0d97e-128"><dt>Sisbkup. lib</dt></span><span class="sxs-lookup"><span data-stu-id="0d97e-128"><dt>Sisbkup.lib</dt></span></span> </dl> |
| <span data-ttu-id="0d97e-129">DLL</span><span class="sxs-lookup"><span data-stu-id="0d97e-129">DLL</span></span><br/>                      | <dl> <span data-ttu-id="0d97e-130"><dt>Sisbkup.dll</dt></span><span class="sxs-lookup"><span data-stu-id="0d97e-130"><dt>Sisbkup.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0d97e-131">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="0d97e-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0d97e-132">**SisCreateRestoreStructure**</span><span class="sxs-lookup"><span data-stu-id="0d97e-132">**SisCreateRestoreStructure**</span></span>](siscreaterestorestructure.md)
</dt> </dl>

 

