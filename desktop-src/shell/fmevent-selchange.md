---
description: Envoyé à une DLL d’extension lorsque l’utilisateur sélectionne un nom de fichier dans la fenêtre répertoire du gestionnaire de fichiers ou dans la fenêtre des résultats de la recherche.
title: Message FMEVENT_SELCHANGE (Wfext. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- FMEVENT_SELCHANGE
api_type:
- HeaderDef
api_location:
- Wfext.h
ms.assetid: 0773aa74-adf2-4e90-aead-2a9a981be3cb
ms.openlocfilehash: 4b05bca54f75bd48b5e710e31c31e5f0f56a2597
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104524503"
---
# <a name="fmevent_selchange-message"></a><span data-ttu-id="17184-103">\_Message FMEVENT selChange</span><span class="sxs-lookup"><span data-stu-id="17184-103">FMEVENT\_SELCHANGE message</span></span>

<span data-ttu-id="17184-104">Envoyé à une DLL d’extension lorsque l’utilisateur sélectionne un nom de fichier dans la fenêtre répertoire du gestionnaire de fichiers ou dans la fenêtre des résultats de la recherche.</span><span class="sxs-lookup"><span data-stu-id="17184-104">Sent to an extension DLL when the user selects a file name in the File Manager directory window or Search Results window.</span></span>

## <a name="parameters"></a><span data-ttu-id="17184-105">Paramètres</span><span class="sxs-lookup"><span data-stu-id="17184-105">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="17184-106">*wParam*</span><span class="sxs-lookup"><span data-stu-id="17184-106">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="17184-107">Doit être zéro.</span><span class="sxs-lookup"><span data-stu-id="17184-107">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="17184-108">*lParam*</span><span class="sxs-lookup"><span data-stu-id="17184-108">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="17184-109">Doit être zéro.</span><span class="sxs-lookup"><span data-stu-id="17184-109">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="17184-110">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="17184-110">Return value</span></span>

<span data-ttu-id="17184-111">Une DLL d’extension doit retourner zéro si elle traite ce message.</span><span class="sxs-lookup"><span data-stu-id="17184-111">An extension DLL should return zero if it processes this message.</span></span>

## <a name="remarks"></a><span data-ttu-id="17184-112">Notes</span><span class="sxs-lookup"><span data-stu-id="17184-112">Remarks</span></span>

<span data-ttu-id="17184-113">Les modifications apportées à la partie de l’arborescence de la fenêtre de répertoire ne génèrent pas ce message.</span><span class="sxs-lookup"><span data-stu-id="17184-113">Changes in the tree portion of the directory window do not produce this message.</span></span>

<span data-ttu-id="17184-114">Étant donné que l’utilisateur peut modifier la sélection plusieurs fois, la DLL d’extension doit retourner promptement après le traitement de ce message pour éviter de ralentir le processus de sélection de l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="17184-114">Because the user can change the selection many times, the extension DLL must return promptly after processing this message to avoid slowing the selection process for the user.</span></span>

## <a name="requirements"></a><span data-ttu-id="17184-115">Spécifications</span><span class="sxs-lookup"><span data-stu-id="17184-115">Requirements</span></span>



| <span data-ttu-id="17184-116">Condition requise</span><span class="sxs-lookup"><span data-stu-id="17184-116">Requirement</span></span> | <span data-ttu-id="17184-117">Valeur</span><span class="sxs-lookup"><span data-stu-id="17184-117">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="17184-118">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="17184-118">Minimum supported client</span></span><br/> | <span data-ttu-id="17184-119">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="17184-119">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                         |
| <span data-ttu-id="17184-120">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="17184-120">Minimum supported server</span></span><br/> | <span data-ttu-id="17184-121">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="17184-121">Windows 2000 Server \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="17184-122">En-tête</span><span class="sxs-lookup"><span data-stu-id="17184-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="17184-123"><dt>Wfext. h</dt></span><span class="sxs-lookup"><span data-stu-id="17184-123"><dt>Wfext.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="17184-124">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="17184-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="17184-125">**FMExtensionProc**</span><span class="sxs-lookup"><span data-stu-id="17184-125">**FMExtensionProc**</span></span>](fmextensionproc.md)
</dt> </dl>

 

 




