---
title: Structure WM_BACKUP_RESTORE_STATUS (wmdrmsdk. h)
description: La \_ structure d’état de la restauration de la sauvegarde WM contient des \_ \_ informations sur une opération de sauvegarde ou de restauration de licence en attente.
ms.assetid: 74e94bc6-376b-4848-a9f9-11c9cb4005f2
keywords:
- Structure WM_BACKUP_RESTORE_STATUS format Windows Media
- structure Windows Media format
topic_type:
- apiref
api_name:
- WM_BACKUP_RESTORE_STATUS
api_location:
- Wmdrmsdk.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 476cd4ddab42ec9f8f44ff51b492bd3913824cf7
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106526812"
---
# <a name="wm_backup_restore_status-structure"></a><span data-ttu-id="4a21f-105">\_Structure d' \_ État de restauration de la sauvegarde WM \_</span><span class="sxs-lookup"><span data-stu-id="4a21f-105">WM\_BACKUP\_RESTORE\_STATUS structure</span></span>

<span data-ttu-id="4a21f-106">La structure d’état de la restauration de la **\_ sauvegarde \_ \_ WM** contient des informations sur une opération de sauvegarde ou de restauration de licence en attente.</span><span class="sxs-lookup"><span data-stu-id="4a21f-106">The **WM\_BACKUP\_RESTORE\_STATUS** structure holds information about a pending license backup or restore operation.</span></span>

## <a name="syntax"></a><span data-ttu-id="4a21f-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="4a21f-107">Syntax</span></span>


```C++
typedef struct WM_BACKUP_RESTORE_STATUS {
  MSDRM_STATUS eStatus;
  BSTR         bstrError;
} ;
```



## <a name="members"></a><span data-ttu-id="4a21f-108">Membres</span><span class="sxs-lookup"><span data-stu-id="4a21f-108">Members</span></span>

<dl> <dt>

<span data-ttu-id="4a21f-109">**eStatus**</span><span class="sxs-lookup"><span data-stu-id="4a21f-109">**eStatus**</span></span>
</dt> <dd>

<span data-ttu-id="4a21f-110">Membre de l’énumération d' [**\_ État msdrm**](msdrm-status.md) spécifiant l’État.</span><span class="sxs-lookup"><span data-stu-id="4a21f-110">Member of the [**MSDRM\_STATUS**](msdrm-status.md) enumeration specifying the status.</span></span>

</dd> <dt>

<span data-ttu-id="4a21f-111">**bstrError**</span><span class="sxs-lookup"><span data-stu-id="4a21f-111">**bstrError**</span></span>
</dt> <dd>

<span data-ttu-id="4a21f-112">Chaîne contenant l’erreur.</span><span class="sxs-lookup"><span data-stu-id="4a21f-112">String containing the error.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="4a21f-113">Notes</span><span class="sxs-lookup"><span data-stu-id="4a21f-113">Remarks</span></span>

<span data-ttu-id="4a21f-114">Cette structure est reçue lorsque vous appelez la méthode [**IWMDRMLicenseBackupRestoreStatus :: GetStatus**](iwmdrmlicensebackuprestorestatus-getstatus.md) .</span><span class="sxs-lookup"><span data-stu-id="4a21f-114">This structure is received when you call the [**IWMDRMLicenseBackupRestoreStatus::GetStatus**](iwmdrmlicensebackuprestorestatus-getstatus.md) method.</span></span> <span data-ttu-id="4a21f-115">Elle contient l’état de l’opération de sauvegarde ou de restauration en attente au moment de l’appel.</span><span class="sxs-lookup"><span data-stu-id="4a21f-115">It contains the status of the pending backup or restore operation at the time of the call.</span></span>

## <a name="requirements"></a><span data-ttu-id="4a21f-116">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="4a21f-116">Requirements</span></span>



| <span data-ttu-id="4a21f-117">Condition requise</span><span class="sxs-lookup"><span data-stu-id="4a21f-117">Requirement</span></span> | <span data-ttu-id="4a21f-118">Valeur</span><span class="sxs-lookup"><span data-stu-id="4a21f-118">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="4a21f-119">En-tête</span><span class="sxs-lookup"><span data-stu-id="4a21f-119">Header</span></span><br/> | <dl> <span data-ttu-id="4a21f-120"><dt>Wmdrmsdk. h</dt></span><span class="sxs-lookup"><span data-stu-id="4a21f-120"><dt>Wmdrmsdk.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4a21f-121">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="4a21f-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4a21f-122">**Structures**</span><span class="sxs-lookup"><span data-stu-id="4a21f-122">**Structures**</span></span>](drm-structures.md)
</dt> </dl>

 

 





