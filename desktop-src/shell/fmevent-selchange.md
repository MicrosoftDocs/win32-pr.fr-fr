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
ms.openlocfilehash: e9aa647434aab5a483626757179a7b23b3372a02
ms.sourcegitcommit: 3caaa3c92dcb1ef12f84464d14ce6262e65e988e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/12/2021
ms.locfileid: "109842260"
---
# <a name="fmevent_selchange-message"></a><span data-ttu-id="65278-103">\_Message FMEVENT selChange</span><span class="sxs-lookup"><span data-stu-id="65278-103">FMEVENT\_SELCHANGE message</span></span>

<span data-ttu-id="65278-104">Envoyé à une DLL d’extension lorsque l’utilisateur sélectionne un nom de fichier dans la fenêtre répertoire du gestionnaire de fichiers ou dans la fenêtre des résultats de la recherche.</span><span class="sxs-lookup"><span data-stu-id="65278-104">Sent to an extension DLL when the user selects a file name in the File Manager directory window or Search Results window.</span></span>

## <a name="parameters"></a><span data-ttu-id="65278-105">Paramètres</span><span class="sxs-lookup"><span data-stu-id="65278-105">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="65278-106">*wParam*</span><span class="sxs-lookup"><span data-stu-id="65278-106">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="65278-107">Doit être zéro.</span><span class="sxs-lookup"><span data-stu-id="65278-107">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="65278-108">*lParam*</span><span class="sxs-lookup"><span data-stu-id="65278-108">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="65278-109">Doit être zéro.</span><span class="sxs-lookup"><span data-stu-id="65278-109">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="65278-110">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="65278-110">Return value</span></span>

<span data-ttu-id="65278-111">Une DLL d’extension doit retourner zéro si elle traite ce message.</span><span class="sxs-lookup"><span data-stu-id="65278-111">An extension DLL should return zero if it processes this message.</span></span>

## <a name="remarks"></a><span data-ttu-id="65278-112">Notes</span><span class="sxs-lookup"><span data-stu-id="65278-112">Remarks</span></span>

<span data-ttu-id="65278-113">Les modifications apportées à la partie de l’arborescence de la fenêtre de répertoire ne génèrent pas ce message.</span><span class="sxs-lookup"><span data-stu-id="65278-113">Changes in the tree portion of the directory window do not produce this message.</span></span>

<span data-ttu-id="65278-114">Étant donné que l’utilisateur peut modifier la sélection plusieurs fois, la DLL d’extension doit retourner promptement après le traitement de ce message pour éviter de ralentir le processus de sélection de l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="65278-114">Because the user can change the selection many times, the extension DLL must return promptly after processing this message to avoid slowing the selection process for the user.</span></span>

## <a name="requirements"></a><span data-ttu-id="65278-115">Spécifications</span><span class="sxs-lookup"><span data-stu-id="65278-115">Requirements</span></span>



| <span data-ttu-id="65278-116">Condition requise</span><span class="sxs-lookup"><span data-stu-id="65278-116">Requirement</span></span> | <span data-ttu-id="65278-117">Valeur</span><span class="sxs-lookup"><span data-stu-id="65278-117">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="65278-118">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="65278-118">Minimum supported client</span></span><br/> | <span data-ttu-id="65278-119">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="65278-119">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                         |
| <span data-ttu-id="65278-120">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="65278-120">Minimum supported server</span></span><br/> | <span data-ttu-id="65278-121">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="65278-121">Windows 2000 Server \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="65278-122">En-tête</span><span class="sxs-lookup"><span data-stu-id="65278-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="65278-123"><dt>Wfext. h</dt></span><span class="sxs-lookup"><span data-stu-id="65278-123"><dt>Wfext.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="65278-124">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="65278-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="65278-125">**FMExtensionProc**</span><span class="sxs-lookup"><span data-stu-id="65278-125">**FMExtensionProc**</span></span>](fmextensionproc.md)
</dt> </dl>

 

 




