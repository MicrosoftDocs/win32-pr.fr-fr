---
description: Envoyé par une extension du gestionnaire de fichiers pour récupérer les informations de lecteur dans la fenêtre du gestionnaire de fichiers active.
title: Message FM_GETDRIVEINFO (Wfext. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- FM_GETDRIVEINFO
api_type:
- HeaderDef
api_location:
- Wfext.h
ms.assetid: 142fff71-3a1b-4197-8c06-2e981cce4e4f
ms.openlocfilehash: 7accd78b36e82abbf56b02b133c79e92dd40d37c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104991076"
---
# <a name="fm_getdriveinfo-message"></a><span data-ttu-id="5dfd8-103">\_Message FM GETDRIVEINFO</span><span class="sxs-lookup"><span data-stu-id="5dfd8-103">FM\_GETDRIVEINFO message</span></span>

<span data-ttu-id="5dfd8-104">Envoyé par une extension du gestionnaire de fichiers pour récupérer les informations de lecteur dans la fenêtre du gestionnaire de fichiers active.</span><span class="sxs-lookup"><span data-stu-id="5dfd8-104">Sent by a File Manager extension to retrieve drive information from the active File Manager window.</span></span>

## <a name="parameters"></a><span data-ttu-id="5dfd8-105">Paramètres</span><span class="sxs-lookup"><span data-stu-id="5dfd8-105">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5dfd8-106">*wParam*</span><span class="sxs-lookup"><span data-stu-id="5dfd8-106">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="5dfd8-107">Doit être zéro.</span><span class="sxs-lookup"><span data-stu-id="5dfd8-107">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="5dfd8-108">*lpfmsgdi*</span><span class="sxs-lookup"><span data-stu-id="5dfd8-108">*lpfmsgdi*</span></span> 
</dt> <dd>

<span data-ttu-id="5dfd8-109">Adresse d’une structure [**\_ GETDRIVEINFO FMS**](fms-getdriveinfo.md) qui reçoit des informations sur le lecteur.</span><span class="sxs-lookup"><span data-stu-id="5dfd8-109">The address of an [**FMS\_GETDRIVEINFO**](fms-getdriveinfo.md) structure that receives drive information.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5dfd8-110">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="5dfd8-110">Return value</span></span>

<span data-ttu-id="5dfd8-111">Retourne une valeur différente de zéro.</span><span class="sxs-lookup"><span data-stu-id="5dfd8-111">Returns nonzero.</span></span>

## <a name="remarks"></a><span data-ttu-id="5dfd8-112">Notes</span><span class="sxs-lookup"><span data-stu-id="5dfd8-112">Remarks</span></span>

<span data-ttu-id="5dfd8-113">Si 0xFFFFFFFF est retourné dans le membre **dwTotalSpace** ou **dwFreeSpace** de la structure [**FMS \_ GETDRIVEINFO**](fms-getdriveinfo.md) , la bibliothèque d’extensions doit calculer la ou les valeurs.</span><span class="sxs-lookup"><span data-stu-id="5dfd8-113">If 0xFFFFFFFF is returned in the **dwTotalSpace** or **dwFreeSpace** member of the [**FMS\_GETDRIVEINFO**](fms-getdriveinfo.md) structure, the extension library must compute the value or values.</span></span>

## <a name="requirements"></a><span data-ttu-id="5dfd8-114">Spécifications</span><span class="sxs-lookup"><span data-stu-id="5dfd8-114">Requirements</span></span>



| <span data-ttu-id="5dfd8-115">Condition requise</span><span class="sxs-lookup"><span data-stu-id="5dfd8-115">Requirement</span></span> | <span data-ttu-id="5dfd8-116">Valeur</span><span class="sxs-lookup"><span data-stu-id="5dfd8-116">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="5dfd8-117">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="5dfd8-117">Minimum supported client</span></span><br/> | <span data-ttu-id="5dfd8-118">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="5dfd8-118">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                         |
| <span data-ttu-id="5dfd8-119">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="5dfd8-119">Minimum supported server</span></span><br/> | <span data-ttu-id="5dfd8-120">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="5dfd8-120">Windows 2000 Server \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="5dfd8-121">En-tête</span><span class="sxs-lookup"><span data-stu-id="5dfd8-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="5dfd8-122"><dt>Wfext. h</dt></span><span class="sxs-lookup"><span data-stu-id="5dfd8-122"><dt>Wfext.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5dfd8-123">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="5dfd8-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5dfd8-124">**FMExtensionProc**</span><span class="sxs-lookup"><span data-stu-id="5dfd8-124">**FMExtensionProc**</span></span>](fmextensionproc.md)
</dt> </dl>

 

 




