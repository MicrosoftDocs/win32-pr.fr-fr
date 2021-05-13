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
ms.openlocfilehash: 0abac794ed23eca30676a839a6eb5ad7c1079c3c
ms.sourcegitcommit: 3caaa3c92dcb1ef12f84464d14ce6262e65e988e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/12/2021
ms.locfileid: "109842410"
---
# <a name="fm_getdriveinfo-message"></a><span data-ttu-id="eb938-103">\_Message FM GETDRIVEINFO</span><span class="sxs-lookup"><span data-stu-id="eb938-103">FM\_GETDRIVEINFO message</span></span>

<span data-ttu-id="eb938-104">Envoyé par une extension du gestionnaire de fichiers pour récupérer les informations de lecteur dans la fenêtre du gestionnaire de fichiers active.</span><span class="sxs-lookup"><span data-stu-id="eb938-104">Sent by a File Manager extension to retrieve drive information from the active File Manager window.</span></span>

## <a name="parameters"></a><span data-ttu-id="eb938-105">Paramètres</span><span class="sxs-lookup"><span data-stu-id="eb938-105">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="eb938-106">*wParam*</span><span class="sxs-lookup"><span data-stu-id="eb938-106">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="eb938-107">Doit être zéro.</span><span class="sxs-lookup"><span data-stu-id="eb938-107">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="eb938-108">*lpfmsgdi*</span><span class="sxs-lookup"><span data-stu-id="eb938-108">*lpfmsgdi*</span></span> 
</dt> <dd>

<span data-ttu-id="eb938-109">Adresse d’une structure [**\_ GETDRIVEINFO FMS**](fms-getdriveinfo.md) qui reçoit des informations sur le lecteur.</span><span class="sxs-lookup"><span data-stu-id="eb938-109">The address of an [**FMS\_GETDRIVEINFO**](fms-getdriveinfo.md) structure that receives drive information.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="eb938-110">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="eb938-110">Return value</span></span>

<span data-ttu-id="eb938-111">Retourne une valeur différente de zéro.</span><span class="sxs-lookup"><span data-stu-id="eb938-111">Returns nonzero.</span></span>

## <a name="remarks"></a><span data-ttu-id="eb938-112">Notes</span><span class="sxs-lookup"><span data-stu-id="eb938-112">Remarks</span></span>

<span data-ttu-id="eb938-113">Si 0xFFFFFFFF est retourné dans le membre **dwTotalSpace** ou **dwFreeSpace** de la structure [**FMS \_ GETDRIVEINFO**](fms-getdriveinfo.md) , la bibliothèque d’extensions doit calculer la ou les valeurs.</span><span class="sxs-lookup"><span data-stu-id="eb938-113">If 0xFFFFFFFF is returned in the **dwTotalSpace** or **dwFreeSpace** member of the [**FMS\_GETDRIVEINFO**](fms-getdriveinfo.md) structure, the extension library must compute the value or values.</span></span>

## <a name="requirements"></a><span data-ttu-id="eb938-114">Spécifications</span><span class="sxs-lookup"><span data-stu-id="eb938-114">Requirements</span></span>



| <span data-ttu-id="eb938-115">Condition requise</span><span class="sxs-lookup"><span data-stu-id="eb938-115">Requirement</span></span> | <span data-ttu-id="eb938-116">Valeur</span><span class="sxs-lookup"><span data-stu-id="eb938-116">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="eb938-117">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="eb938-117">Minimum supported client</span></span><br/> | <span data-ttu-id="eb938-118">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="eb938-118">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                         |
| <span data-ttu-id="eb938-119">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="eb938-119">Minimum supported server</span></span><br/> | <span data-ttu-id="eb938-120">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="eb938-120">Windows 2000 Server \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="eb938-121">En-tête</span><span class="sxs-lookup"><span data-stu-id="eb938-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="eb938-122"><dt>Wfext. h</dt></span><span class="sxs-lookup"><span data-stu-id="eb938-122"><dt>Wfext.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="eb938-123">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="eb938-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="eb938-124">**FMExtensionProc**</span><span class="sxs-lookup"><span data-stu-id="eb938-124">**FMExtensionProc**</span></span>](fmextensionproc.md)
</dt> </dl>

 

 




