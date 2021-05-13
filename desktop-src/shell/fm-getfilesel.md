---
description: Envoyé par une extension du gestionnaire de fichiers pour récupérer des informations sur un fichier sélectionné à partir de la fenêtre du gestionnaire de fichiers active (la fenêtre répertoire ou la fenêtre résultats de la recherche).
title: Message FM_GETFILESEL (Wfext. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- FM_GETFILESEL
api_type:
- HeaderDef
api_location:
- Wfext.h
ms.assetid: c2b4aac6-165b-4eba-b012-ee7a20481cd3
ms.openlocfilehash: 2da95a39f8e84215640e926ae21a043865223665
ms.sourcegitcommit: 3caaa3c92dcb1ef12f84464d14ce6262e65e988e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/12/2021
ms.locfileid: "109841420"
---
# <a name="fm_getfilesel-message"></a><span data-ttu-id="41642-103">\_Message FM GETFILESEL</span><span class="sxs-lookup"><span data-stu-id="41642-103">FM\_GETFILESEL message</span></span>

<span data-ttu-id="41642-104">Envoyé par une extension du gestionnaire de fichiers pour récupérer des informations sur un fichier sélectionné à partir de la fenêtre du gestionnaire de fichiers active (la fenêtre répertoire ou la fenêtre résultats de la recherche).</span><span class="sxs-lookup"><span data-stu-id="41642-104">Sent by a File Manager extension to retrieve information about a selected file from the active File Manager window (either the directory window or the Search Results window).</span></span>

## <a name="parameters"></a><span data-ttu-id="41642-105">Paramètres</span><span class="sxs-lookup"><span data-stu-id="41642-105">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="41642-106">*index*</span><span class="sxs-lookup"><span data-stu-id="41642-106">*index*</span></span> 
</dt> <dd>

<span data-ttu-id="41642-107">Index de base zéro du fichier sélectionné à récupérer.</span><span class="sxs-lookup"><span data-stu-id="41642-107">The zero-based index of the selected file to retrieve.</span></span>

</dd> <dt>

<span data-ttu-id="41642-108">*lpfmsgfs*</span><span class="sxs-lookup"><span data-stu-id="41642-108">*lpfmsgfs*</span></span> 
</dt> <dd>

<span data-ttu-id="41642-109">Adresse d’une structure [**\_ GETFILESEL FMS**](fms-getfilesel.md) qui reçoit des informations sur la sélection.</span><span class="sxs-lookup"><span data-stu-id="41642-109">The address of an [**FMS\_GETFILESEL**](fms-getfilesel.md) structure that receives information about the selection.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="41642-110">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="41642-110">Return value</span></span>

<span data-ttu-id="41642-111">Retourne l’index de base zéro du fichier sélectionné qui a été récupéré.</span><span class="sxs-lookup"><span data-stu-id="41642-111">Returns the zero-based index of the selected file that was retrieved.</span></span>

## <a name="remarks"></a><span data-ttu-id="41642-112">Notes</span><span class="sxs-lookup"><span data-stu-id="41642-112">Remarks</span></span>

<span data-ttu-id="41642-113">Une extension peut utiliser le message [**FM \_ GETSELCOUNT**](fm-getselcount.md) pour récupérer le nombre de fichiers sélectionnés.</span><span class="sxs-lookup"><span data-stu-id="41642-113">An extension can use the [**FM\_GETSELCOUNT**](fm-getselcount.md) message to retrieve the count of selected files.</span></span>

## <a name="requirements"></a><span data-ttu-id="41642-114">Spécifications</span><span class="sxs-lookup"><span data-stu-id="41642-114">Requirements</span></span>



| <span data-ttu-id="41642-115">Condition requise</span><span class="sxs-lookup"><span data-stu-id="41642-115">Requirement</span></span> | <span data-ttu-id="41642-116">Valeur</span><span class="sxs-lookup"><span data-stu-id="41642-116">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="41642-117">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="41642-117">Minimum supported client</span></span><br/> | <span data-ttu-id="41642-118">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="41642-118">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                         |
| <span data-ttu-id="41642-119">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="41642-119">Minimum supported server</span></span><br/> | <span data-ttu-id="41642-120">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="41642-120">Windows 2000 Server \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="41642-121">En-tête</span><span class="sxs-lookup"><span data-stu-id="41642-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="41642-122"><dt>Wfext. h</dt></span><span class="sxs-lookup"><span data-stu-id="41642-122"><dt>Wfext.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="41642-123">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="41642-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="41642-124">**FMExtensionProc**</span><span class="sxs-lookup"><span data-stu-id="41642-124">**FMExtensionProc**</span></span>](fmextensionproc.md)
</dt> <dt>

[<span data-ttu-id="41642-125">**\_GETFILESELLFN FM**</span><span class="sxs-lookup"><span data-stu-id="41642-125">**FM\_GETFILESELLFN**</span></span>](fm-getfilesellfn.md)
</dt> <dt>

[<span data-ttu-id="41642-126">**\_GETSELCOUNTLFN FM**</span><span class="sxs-lookup"><span data-stu-id="41642-126">**FM\_GETSELCOUNTLFN**</span></span>](fm-getselcountlfn.md)
</dt> </dl>

 

 




