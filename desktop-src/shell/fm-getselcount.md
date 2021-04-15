---
description: Envoyé par une extension du gestionnaire de fichiers pour récupérer le nombre de fichiers sélectionnés dans la fenêtre du gestionnaire de fichiers active (la fenêtre répertoire ou la fenêtre résultats de la recherche).
title: Message FM_GETSELCOUNT (Wfext. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- FM_GETSELCOUNT
api_type:
- HeaderDef
api_location:
- Wfext.h
ms.assetid: 0d43bf37-863c-45cc-94ea-5b2aedba5353
ms.openlocfilehash: aac7d08de3785bb02c31dabc1ef7a25fea0d5b73
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104991073"
---
# <a name="fm_getselcount-message"></a><span data-ttu-id="bf0a8-103">\_Message FM GETSELCOUNT</span><span class="sxs-lookup"><span data-stu-id="bf0a8-103">FM\_GETSELCOUNT message</span></span>

<span data-ttu-id="bf0a8-104">Envoyé par une extension du gestionnaire de fichiers pour récupérer le nombre de fichiers sélectionnés dans la fenêtre du gestionnaire de fichiers active (la fenêtre répertoire ou la fenêtre résultats de la recherche).</span><span class="sxs-lookup"><span data-stu-id="bf0a8-104">Sent by a File Manager extension to retrieve a count of the selected files in the active File Manager window (either the directory window or the Search Results window).</span></span>

## <a name="parameters"></a><span data-ttu-id="bf0a8-105">Paramètres</span><span class="sxs-lookup"><span data-stu-id="bf0a8-105">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="bf0a8-106">*wParam*</span><span class="sxs-lookup"><span data-stu-id="bf0a8-106">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="bf0a8-107">Doit être zéro.</span><span class="sxs-lookup"><span data-stu-id="bf0a8-107">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="bf0a8-108">*lParam*</span><span class="sxs-lookup"><span data-stu-id="bf0a8-108">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="bf0a8-109">Doit être zéro.</span><span class="sxs-lookup"><span data-stu-id="bf0a8-109">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="bf0a8-110">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="bf0a8-110">Return value</span></span>

<span data-ttu-id="bf0a8-111">Retourne le nombre de fichiers sélectionnés.</span><span class="sxs-lookup"><span data-stu-id="bf0a8-111">Returns the number of selected files.</span></span>

## <a name="requirements"></a><span data-ttu-id="bf0a8-112">Spécifications</span><span class="sxs-lookup"><span data-stu-id="bf0a8-112">Requirements</span></span>



| <span data-ttu-id="bf0a8-113">Condition requise</span><span class="sxs-lookup"><span data-stu-id="bf0a8-113">Requirement</span></span> | <span data-ttu-id="bf0a8-114">Valeur</span><span class="sxs-lookup"><span data-stu-id="bf0a8-114">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="bf0a8-115">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="bf0a8-115">Minimum supported client</span></span><br/> | <span data-ttu-id="bf0a8-116">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="bf0a8-116">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                         |
| <span data-ttu-id="bf0a8-117">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="bf0a8-117">Minimum supported server</span></span><br/> | <span data-ttu-id="bf0a8-118">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="bf0a8-118">Windows 2000 Server \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="bf0a8-119">En-tête</span><span class="sxs-lookup"><span data-stu-id="bf0a8-119">Header</span></span><br/>                   | <dl> <span data-ttu-id="bf0a8-120"><dt>Wfext. h</dt></span><span class="sxs-lookup"><span data-stu-id="bf0a8-120"><dt>Wfext.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="bf0a8-121">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="bf0a8-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bf0a8-122">**\_GETFILESEL FM**</span><span class="sxs-lookup"><span data-stu-id="bf0a8-122">**FM\_GETFILESEL**</span></span>](fm-getfilesel.md)
</dt> <dt>

[<span data-ttu-id="bf0a8-123">**\_GETFILESELLFN FM**</span><span class="sxs-lookup"><span data-stu-id="bf0a8-123">**FM\_GETFILESELLFN**</span></span>](fm-getfilesellfn.md)
</dt> <dt>

[<span data-ttu-id="bf0a8-124">**\_GETSELCOUNTLFN FM**</span><span class="sxs-lookup"><span data-stu-id="bf0a8-124">**FM\_GETSELCOUNTLFN**</span></span>](fm-getselcountlfn.md)
</dt> </dl>

 

 




