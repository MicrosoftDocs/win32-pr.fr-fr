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
ms.openlocfilehash: 727e098a98ecfe4a4349ebcf9c6f931a8579b70d
ms.sourcegitcommit: 3caaa3c92dcb1ef12f84464d14ce6262e65e988e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/12/2021
ms.locfileid: "109842370"
---
# <a name="fm_getselcount-message"></a><span data-ttu-id="9ed14-103">\_Message FM GETSELCOUNT</span><span class="sxs-lookup"><span data-stu-id="9ed14-103">FM\_GETSELCOUNT message</span></span>

<span data-ttu-id="9ed14-104">Envoyé par une extension du gestionnaire de fichiers pour récupérer le nombre de fichiers sélectionnés dans la fenêtre du gestionnaire de fichiers active (la fenêtre répertoire ou la fenêtre résultats de la recherche).</span><span class="sxs-lookup"><span data-stu-id="9ed14-104">Sent by a File Manager extension to retrieve a count of the selected files in the active File Manager window (either the directory window or the Search Results window).</span></span>

## <a name="parameters"></a><span data-ttu-id="9ed14-105">Paramètres</span><span class="sxs-lookup"><span data-stu-id="9ed14-105">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9ed14-106">*wParam*</span><span class="sxs-lookup"><span data-stu-id="9ed14-106">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="9ed14-107">Doit être zéro.</span><span class="sxs-lookup"><span data-stu-id="9ed14-107">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="9ed14-108">*lParam*</span><span class="sxs-lookup"><span data-stu-id="9ed14-108">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="9ed14-109">Doit être zéro.</span><span class="sxs-lookup"><span data-stu-id="9ed14-109">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9ed14-110">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="9ed14-110">Return value</span></span>

<span data-ttu-id="9ed14-111">Retourne le nombre de fichiers sélectionnés.</span><span class="sxs-lookup"><span data-stu-id="9ed14-111">Returns the number of selected files.</span></span>

## <a name="requirements"></a><span data-ttu-id="9ed14-112">Spécifications</span><span class="sxs-lookup"><span data-stu-id="9ed14-112">Requirements</span></span>



| <span data-ttu-id="9ed14-113">Condition requise</span><span class="sxs-lookup"><span data-stu-id="9ed14-113">Requirement</span></span> | <span data-ttu-id="9ed14-114">Valeur</span><span class="sxs-lookup"><span data-stu-id="9ed14-114">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="9ed14-115">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="9ed14-115">Minimum supported client</span></span><br/> | <span data-ttu-id="9ed14-116">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="9ed14-116">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                         |
| <span data-ttu-id="9ed14-117">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="9ed14-117">Minimum supported server</span></span><br/> | <span data-ttu-id="9ed14-118">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="9ed14-118">Windows 2000 Server \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="9ed14-119">En-tête</span><span class="sxs-lookup"><span data-stu-id="9ed14-119">Header</span></span><br/>                   | <dl> <span data-ttu-id="9ed14-120"><dt>Wfext. h</dt></span><span class="sxs-lookup"><span data-stu-id="9ed14-120"><dt>Wfext.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9ed14-121">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="9ed14-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9ed14-122">**\_GETFILESEL FM**</span><span class="sxs-lookup"><span data-stu-id="9ed14-122">**FM\_GETFILESEL**</span></span>](fm-getfilesel.md)
</dt> <dt>

[<span data-ttu-id="9ed14-123">**\_GETFILESELLFN FM**</span><span class="sxs-lookup"><span data-stu-id="9ed14-123">**FM\_GETFILESELLFN**</span></span>](fm-getfilesellfn.md)
</dt> <dt>

[<span data-ttu-id="9ed14-124">**\_GETSELCOUNTLFN FM**</span><span class="sxs-lookup"><span data-stu-id="9ed14-124">**FM\_GETSELCOUNTLFN**</span></span>](fm-getselcountlfn.md)
</dt> </dl>

 

 




