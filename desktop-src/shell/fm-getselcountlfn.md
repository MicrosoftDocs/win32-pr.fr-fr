---
description: Envoyé par une extension du gestionnaire de fichiers pour récupérer le nombre de fichiers sélectionnés dans la fenêtre du gestionnaire de fichiers active (la fenêtre répertoire ou la fenêtre résultats de la recherche). Le nombre comprend les fichiers qui ont des noms de fichiers longs.
title: Message FM_GETSELCOUNTLFN (Wfext. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- FM_GETSELCOUNTLFN
api_type:
- HeaderDef
api_location:
- Wfext.h
ms.assetid: d0815afc-5356-48a7-a90d-5f48dae6bee5
ms.openlocfilehash: 0a09ca8315405f06db091b27b9d326090796504c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104991601"
---
# <a name="fm_getselcountlfn-message"></a><span data-ttu-id="5e827-104">\_Message FM GETSELCOUNTLFN</span><span class="sxs-lookup"><span data-stu-id="5e827-104">FM\_GETSELCOUNTLFN message</span></span>

<span data-ttu-id="5e827-105">Envoyé par une extension du gestionnaire de fichiers pour récupérer le nombre de fichiers sélectionnés dans la fenêtre du gestionnaire de fichiers active (la fenêtre répertoire ou la fenêtre résultats de la recherche).</span><span class="sxs-lookup"><span data-stu-id="5e827-105">Sent by a File Manager extension to retrieve the number of selected files in the active File Manager window (either the directory window or the Search Results window).</span></span> <span data-ttu-id="5e827-106">Le nombre comprend les fichiers qui ont des noms de fichiers longs.</span><span class="sxs-lookup"><span data-stu-id="5e827-106">The count includes files that have long file names.</span></span>

## <a name="parameters"></a><span data-ttu-id="5e827-107">Paramètres</span><span class="sxs-lookup"><span data-stu-id="5e827-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5e827-108">*wParam*</span><span class="sxs-lookup"><span data-stu-id="5e827-108">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="5e827-109">Doit être zéro.</span><span class="sxs-lookup"><span data-stu-id="5e827-109">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="5e827-110">*lParam*</span><span class="sxs-lookup"><span data-stu-id="5e827-110">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="5e827-111">Doit être zéro.</span><span class="sxs-lookup"><span data-stu-id="5e827-111">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5e827-112">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="5e827-112">Return value</span></span>

<span data-ttu-id="5e827-113">Retourne le nombre de fichiers sélectionnés.</span><span class="sxs-lookup"><span data-stu-id="5e827-113">Returns the number of selected files.</span></span>

## <a name="remarks"></a><span data-ttu-id="5e827-114">Notes</span><span class="sxs-lookup"><span data-stu-id="5e827-114">Remarks</span></span>

<span data-ttu-id="5e827-115">Seules les extensions qui prennent en charge les noms de fichiers longs (par exemple, les extensions prenant en charge le réseau) doivent utiliser ce message.</span><span class="sxs-lookup"><span data-stu-id="5e827-115">Only extensions that support long file names (for example, network-aware extensions) should use this message.</span></span>

## <a name="requirements"></a><span data-ttu-id="5e827-116">Spécifications</span><span class="sxs-lookup"><span data-stu-id="5e827-116">Requirements</span></span>



| <span data-ttu-id="5e827-117">Condition requise</span><span class="sxs-lookup"><span data-stu-id="5e827-117">Requirement</span></span> | <span data-ttu-id="5e827-118">Valeur</span><span class="sxs-lookup"><span data-stu-id="5e827-118">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="5e827-119">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="5e827-119">Minimum supported client</span></span><br/> | <span data-ttu-id="5e827-120">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="5e827-120">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                         |
| <span data-ttu-id="5e827-121">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="5e827-121">Minimum supported server</span></span><br/> | <span data-ttu-id="5e827-122">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="5e827-122">Windows 2000 Server \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="5e827-123">En-tête</span><span class="sxs-lookup"><span data-stu-id="5e827-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="5e827-124"><dt>Wfext. h</dt></span><span class="sxs-lookup"><span data-stu-id="5e827-124"><dt>Wfext.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5e827-125">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="5e827-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5e827-126">**\_GETFILESEL FM**</span><span class="sxs-lookup"><span data-stu-id="5e827-126">**FM\_GETFILESEL**</span></span>](fm-getfilesel.md)
</dt> <dt>

[<span data-ttu-id="5e827-127">**\_GETFILESELLFN FM**</span><span class="sxs-lookup"><span data-stu-id="5e827-127">**FM\_GETFILESELLFN**</span></span>](fm-getfilesellfn.md)
</dt> <dt>

[<span data-ttu-id="5e827-128">**\_GETSELCOUNT FM**</span><span class="sxs-lookup"><span data-stu-id="5e827-128">**FM\_GETSELCOUNT**</span></span>](fm-getselcount.md)
</dt> </dl>

 

 




