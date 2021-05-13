---
description: Envoyé par une extension du gestionnaire de fichiers pour récupérer des informations sur un fichier sélectionné à partir de la fenêtre du gestionnaire de fichiers active (la fenêtre répertoire ou la fenêtre résultats de la recherche). Le fichier sélectionné peut avoir un nom de fichier long.
title: Message FM_GETFILESELLFN (Wfext. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- FM_GETFILESELLFN
api_type:
- HeaderDef
api_location:
- Wfext.h
ms.assetid: 461fd171-d47f-41d6-953e-8e497e023ab1
ms.openlocfilehash: e991d2705f74aa8822dcef89878e9762f22b08dc
ms.sourcegitcommit: 3caaa3c92dcb1ef12f84464d14ce6262e65e988e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/12/2021
ms.locfileid: "109842390"
---
# <a name="fm_getfilesellfn-message"></a><span data-ttu-id="91e40-104">\_Message FM GETFILESELLFN</span><span class="sxs-lookup"><span data-stu-id="91e40-104">FM\_GETFILESELLFN message</span></span>

<span data-ttu-id="91e40-105">Envoyé par une extension du gestionnaire de fichiers pour récupérer des informations sur un fichier sélectionné à partir de la fenêtre du gestionnaire de fichiers active (la fenêtre répertoire ou la fenêtre résultats de la recherche).</span><span class="sxs-lookup"><span data-stu-id="91e40-105">Sent by a File Manager extension to retrieve information about a selected file from the active File Manager window (either the directory window or the Search Results window).</span></span> <span data-ttu-id="91e40-106">Le fichier sélectionné peut avoir un nom de fichier long.</span><span class="sxs-lookup"><span data-stu-id="91e40-106">The selected file can have a long file name.</span></span>

## <a name="parameters"></a><span data-ttu-id="91e40-107">Paramètres</span><span class="sxs-lookup"><span data-stu-id="91e40-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="91e40-108">*index*</span><span class="sxs-lookup"><span data-stu-id="91e40-108">*index*</span></span> 
</dt> <dd>

<span data-ttu-id="91e40-109">Index de base zéro du fichier sélectionné à récupérer.</span><span class="sxs-lookup"><span data-stu-id="91e40-109">The zero-based index of the selected file to retrieve.</span></span>

</dd> <dt>

<span data-ttu-id="91e40-110">*lpfmsgfs*</span><span class="sxs-lookup"><span data-stu-id="91e40-110">*lpfmsgfs*</span></span> 
</dt> <dd>

<span data-ttu-id="91e40-111">Adresse d’une structure [**\_ GETFILESEL FMS**](fms-getfilesel.md) qui reçoit des informations sur la sélection.</span><span class="sxs-lookup"><span data-stu-id="91e40-111">The address of an [**FMS\_GETFILESEL**](fms-getfilesel.md) structure that receives information about the selection.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="91e40-112">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="91e40-112">Return value</span></span>

<span data-ttu-id="91e40-113">Retourne l’index de base zéro du fichier sélectionné qui a été récupéré.</span><span class="sxs-lookup"><span data-stu-id="91e40-113">Returns the zero-based index of the selected file that was retrieved.</span></span>

## <a name="remarks"></a><span data-ttu-id="91e40-114">Notes</span><span class="sxs-lookup"><span data-stu-id="91e40-114">Remarks</span></span>

<span data-ttu-id="91e40-115">Seules les extensions qui prennent en charge les noms de fichiers longs (par exemple, les extensions prenant en charge le réseau) doivent utiliser ce message.</span><span class="sxs-lookup"><span data-stu-id="91e40-115">Only extensions that support long file names (for example, network-aware extensions) should use this message.</span></span>

<span data-ttu-id="91e40-116">Une extension peut utiliser le message [**FM \_ GETSELCOUNTLFN**](fm-getselcountlfn.md) pour récupérer le nombre de fichiers sélectionnés.</span><span class="sxs-lookup"><span data-stu-id="91e40-116">An extension can use the [**FM\_GETSELCOUNTLFN**](fm-getselcountlfn.md) message to retrieve the count of selected files.</span></span>

## <a name="requirements"></a><span data-ttu-id="91e40-117">Spécifications</span><span class="sxs-lookup"><span data-stu-id="91e40-117">Requirements</span></span>



| <span data-ttu-id="91e40-118">Condition requise</span><span class="sxs-lookup"><span data-stu-id="91e40-118">Requirement</span></span> | <span data-ttu-id="91e40-119">Valeur</span><span class="sxs-lookup"><span data-stu-id="91e40-119">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="91e40-120">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="91e40-120">Minimum supported client</span></span><br/> | <span data-ttu-id="91e40-121">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="91e40-121">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                         |
| <span data-ttu-id="91e40-122">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="91e40-122">Minimum supported server</span></span><br/> | <span data-ttu-id="91e40-123">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="91e40-123">Windows 2000 Server \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="91e40-124">En-tête</span><span class="sxs-lookup"><span data-stu-id="91e40-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="91e40-125"><dt>Wfext. h</dt></span><span class="sxs-lookup"><span data-stu-id="91e40-125"><dt>Wfext.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="91e40-126">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="91e40-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="91e40-127">**FMExtensionProc**</span><span class="sxs-lookup"><span data-stu-id="91e40-127">**FMExtensionProc**</span></span>](fmextensionproc.md)
</dt> <dt>

[<span data-ttu-id="91e40-128">**\_GETFILESEL FM**</span><span class="sxs-lookup"><span data-stu-id="91e40-128">**FM\_GETFILESEL**</span></span>](fm-getfilesel.md)
</dt> <dt>

[<span data-ttu-id="91e40-129">**\_GETSELCOUNT FM**</span><span class="sxs-lookup"><span data-stu-id="91e40-129">**FM\_GETSELCOUNT**</span></span>](fm-getselcount.md)
</dt> </dl>

 

 




