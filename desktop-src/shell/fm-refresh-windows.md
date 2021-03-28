---
description: Envoyé par une extension du gestionnaire de fichiers pour faire en sorte que le gestionnaire de fichiers redessine la fenêtre active ou l’ensemble de ses fenêtres.
title: Message FM_REFRESH_WINDOWS (Wfext. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- FM_REFRESH_WINDOWS
api_type:
- HeaderDef
api_location:
- Wfext.h
ms.assetid: 210168c6-d83b-4ffd-93d4-d22fa748cef2
ms.openlocfilehash: 386fdee5c7a8b56899fa7e13282445c57eccff08
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104201144"
---
# <a name="fm_refresh_windows-message"></a><span data-ttu-id="abe0b-103">\_Message Windows d’actualisation FM \_</span><span class="sxs-lookup"><span data-stu-id="abe0b-103">FM\_REFRESH\_WINDOWS message</span></span>

<span data-ttu-id="abe0b-104">Envoyé par une extension du gestionnaire de fichiers pour faire en sorte que le gestionnaire de fichiers redessine la fenêtre active ou l’ensemble de ses fenêtres.</span><span class="sxs-lookup"><span data-stu-id="abe0b-104">Sent by a File Manager extension to cause File Manager to repaint either its active window or all of its windows.</span></span>

## <a name="parameters"></a><span data-ttu-id="abe0b-105">Paramètres</span><span class="sxs-lookup"><span data-stu-id="abe0b-105">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="abe0b-106">*fRepaint*</span><span class="sxs-lookup"><span data-stu-id="abe0b-106">*fRepaint*</span></span> 
</dt> <dd>

<span data-ttu-id="abe0b-107">Valeur qui indique si le gestionnaire de fichiers redessine sa fenêtre active ou toutes ses fenêtres.</span><span class="sxs-lookup"><span data-stu-id="abe0b-107">A value that indicates whether File Manager repaints its active window or all of its windows.</span></span> <span data-ttu-id="abe0b-108">Si ce paramètre a la **valeur true**, le gestionnaire de fichiers redessine toutes ses fenêtres.</span><span class="sxs-lookup"><span data-stu-id="abe0b-108">If this parameter is **TRUE**, File Manager repaints all of its windows.</span></span> <span data-ttu-id="abe0b-109">Dans le cas contraire, le gestionnaire de fichiers redessine uniquement sa fenêtre active.</span><span class="sxs-lookup"><span data-stu-id="abe0b-109">Otherwise, File Manager repaints only its active window.</span></span>

</dd> <dt>

<span data-ttu-id="abe0b-110">*wParam*</span><span class="sxs-lookup"><span data-stu-id="abe0b-110">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="abe0b-111">Doit être zéro.</span><span class="sxs-lookup"><span data-stu-id="abe0b-111">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="abe0b-112">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="abe0b-112">Return value</span></span>

<span data-ttu-id="abe0b-113">Pas de valeur de retour.</span><span class="sxs-lookup"><span data-stu-id="abe0b-113">No return value.</span></span>

## <a name="remarks"></a><span data-ttu-id="abe0b-114">Notes</span><span class="sxs-lookup"><span data-stu-id="abe0b-114">Remarks</span></span>

<span data-ttu-id="abe0b-115">Les modifications du système de fichiers provoquées par une extension sont détectées automatiquement par le gestionnaire de fichiers.</span><span class="sxs-lookup"><span data-stu-id="abe0b-115">File system changes caused by an extension are automatically detected by File Manager.</span></span> <span data-ttu-id="abe0b-116">Une extension ne doit utiliser ce message que dans les situations où des connexions de lecteur sont effectuées ou annulées.</span><span class="sxs-lookup"><span data-stu-id="abe0b-116">An extension should use this message only in situations where drive connections are made or canceled.</span></span>

## <a name="requirements"></a><span data-ttu-id="abe0b-117">Spécifications</span><span class="sxs-lookup"><span data-stu-id="abe0b-117">Requirements</span></span>



| <span data-ttu-id="abe0b-118">Condition requise</span><span class="sxs-lookup"><span data-stu-id="abe0b-118">Requirement</span></span> | <span data-ttu-id="abe0b-119">Valeur</span><span class="sxs-lookup"><span data-stu-id="abe0b-119">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="abe0b-120">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="abe0b-120">Minimum supported client</span></span><br/> | <span data-ttu-id="abe0b-121">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="abe0b-121">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                         |
| <span data-ttu-id="abe0b-122">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="abe0b-122">Minimum supported server</span></span><br/> | <span data-ttu-id="abe0b-123">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="abe0b-123">Windows 2000 Server \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="abe0b-124">En-tête</span><span class="sxs-lookup"><span data-stu-id="abe0b-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="abe0b-125"><dt>Wfext. h</dt></span><span class="sxs-lookup"><span data-stu-id="abe0b-125"><dt>Wfext.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="abe0b-126">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="abe0b-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="abe0b-127">**FMExtensionProc**</span><span class="sxs-lookup"><span data-stu-id="abe0b-127">**FMExtensionProc**</span></span>](fmextensionproc.md)
</dt> </dl>

 

 




