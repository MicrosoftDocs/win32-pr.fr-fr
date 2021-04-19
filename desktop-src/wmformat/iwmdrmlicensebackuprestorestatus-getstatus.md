---
title: IWMDRMLicenseBackupRestoreStatus GetStatus, méthode (wmdrmsdk. h)
description: La méthode GetStatus récupère des informations d’État détaillées sur une opération de sauvegarde ou de restauration de licence.
ms.assetid: 1a695baf-0971-4dbf-90fa-1b10178a3348
keywords:
- Méthode GetStatus Windows Media format
- Méthode GetStatus Windows Media format, interface IWMDRMLicenseBackupRestoreStatus
- Interface IWMDRMLicenseBackupRestoreStatus Windows Media format, GetStatus, méthode
topic_type:
- apiref
api_name:
- IWMDRMLicenseBackupRestoreStatus.GetStatus
api_location:
- Wmdrmsdk.lib
- Wmdrmsdk.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3373e71bcae9dc1054e97e8b758ac72389b9a712
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106539248"
---
# <a name="iwmdrmlicensebackuprestorestatusgetstatus-method"></a><span data-ttu-id="53c27-106">IWMDRMLicenseBackupRestoreStatus :: GetStatus, méthode</span><span class="sxs-lookup"><span data-stu-id="53c27-106">IWMDRMLicenseBackupRestoreStatus::GetStatus method</span></span>

<span data-ttu-id="53c27-107">La méthode **GetStatus** récupère des informations d’État détaillées sur une opération de sauvegarde ou de restauration de licence.</span><span class="sxs-lookup"><span data-stu-id="53c27-107">The **GetStatus** method retrieves detailed status information about a license backup or restore operation.</span></span>

## <a name="syntax"></a><span data-ttu-id="53c27-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="53c27-108">Syntax</span></span>


```C++
HRESULT GetStatus(
  [out] WM_BACKUP_RESTORE_STATUS *pStatus
);
```



## <a name="parameters"></a><span data-ttu-id="53c27-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="53c27-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="53c27-110">*pStatus* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="53c27-110">*pStatus* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="53c27-111">Pointeur vers une structure d' [**\_ État de \_ restauration \_ de sauvegarde WM**](wm-backup-restore-status.md) qui reçoit les informations d’État.</span><span class="sxs-lookup"><span data-stu-id="53c27-111">Pointer to a [**WM\_BACKUP\_RESTORE\_STATUS**](wm-backup-restore-status.md) structure that receives the status information.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="53c27-112">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="53c27-112">Return value</span></span>

<span data-ttu-id="53c27-113">La méthode retourne un **HRESULT**.</span><span class="sxs-lookup"><span data-stu-id="53c27-113">The method returns an **HRESULT**.</span></span> <span data-ttu-id="53c27-114">Les valeurs possibles sont notamment celles figurant dans le tableau suivant.</span><span class="sxs-lookup"><span data-stu-id="53c27-114">Possible values include, but are not limited to, those in the following table.</span></span>



| <span data-ttu-id="53c27-115">Code de retour</span><span class="sxs-lookup"><span data-stu-id="53c27-115">Return code</span></span>                                                                          | <span data-ttu-id="53c27-116">Description</span><span class="sxs-lookup"><span data-stu-id="53c27-116">Description</span></span>                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <span data-ttu-id="53c27-117"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="53c27-117"><dt>**S\_OK**</dt></span></span> </dl> | <span data-ttu-id="53c27-118">S_OK</span><span class="sxs-lookup"><span data-stu-id="53c27-118">The method succeeded.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="53c27-119">Notes</span><span class="sxs-lookup"><span data-stu-id="53c27-119">Remarks</span></span>

<span data-ttu-id="53c27-120">Aucun.</span><span class="sxs-lookup"><span data-stu-id="53c27-120">None.</span></span>

## <a name="requirements"></a><span data-ttu-id="53c27-121">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="53c27-121">Requirements</span></span>



| <span data-ttu-id="53c27-122">Condition requise</span><span class="sxs-lookup"><span data-stu-id="53c27-122">Requirement</span></span> | <span data-ttu-id="53c27-123">Valeur</span><span class="sxs-lookup"><span data-stu-id="53c27-123">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="53c27-124">En-tête</span><span class="sxs-lookup"><span data-stu-id="53c27-124">Header</span></span><br/>  | <dl> <span data-ttu-id="53c27-125"><dt>Wmdrmsdk. h</dt></span><span class="sxs-lookup"><span data-stu-id="53c27-125"><dt>Wmdrmsdk.h</dt></span></span> </dl>   |
| <span data-ttu-id="53c27-126">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="53c27-126">Library</span></span><br/> | <dl> <span data-ttu-id="53c27-127"><dt>Wmdrmsdk. lib</dt></span><span class="sxs-lookup"><span data-stu-id="53c27-127"><dt>Wmdrmsdk.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="53c27-128">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="53c27-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="53c27-129">**Interface IWMDRMLicenseBackupRestoreStatus**</span><span class="sxs-lookup"><span data-stu-id="53c27-129">**IWMDRMLicenseBackupRestoreStatus Interface**</span></span>](iwmdrmlicensebackuprestorestatus.md)
</dt> </dl>

 

 





