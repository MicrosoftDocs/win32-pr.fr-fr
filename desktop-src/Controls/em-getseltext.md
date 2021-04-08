---
title: Message EM_GETSELTEXT (RichEdit. h)
description: Récupère le texte actuellement sélectionné dans un contrôle RichEdit.
ms.assetid: 56af77c3-f2d7-4b5d-895f-a67c141459e3
keywords:
- EM_GETSELTEXT les contrôles de message Windows
topic_type:
- apiref
api_name:
- EM_GETSELTEXT
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: acde2c0677fa04ff6d7991bca56bad0c08a6f5ff
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103843486"
---
# <a name="em_getseltext-message"></a><span data-ttu-id="c7318-104">\_Message GETSELTEXT em</span><span class="sxs-lookup"><span data-stu-id="c7318-104">EM\_GETSELTEXT message</span></span>

<span data-ttu-id="c7318-105">Récupère le texte actuellement sélectionné dans un contrôle RichEdit.</span><span class="sxs-lookup"><span data-stu-id="c7318-105">Retrieves the currently selected text in a rich edit control.</span></span>

## <a name="parameters"></a><span data-ttu-id="c7318-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="c7318-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c7318-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="c7318-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="c7318-108">Ce paramètre n’est pas utilisé ; elle doit être égale à zéro.</span><span class="sxs-lookup"><span data-stu-id="c7318-108">This parameter is not used; it must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="c7318-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="c7318-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="c7318-110">Pointeur vers une mémoire tampon qui reçoit le texte sélectionné.</span><span class="sxs-lookup"><span data-stu-id="c7318-110">Pointer to a buffer that receives the selected text.</span></span> <span data-ttu-id="c7318-111">L’application appelante doit s’assurer que la mémoire tampon est suffisamment grande pour contenir le texte sélectionné.</span><span class="sxs-lookup"><span data-stu-id="c7318-111">The calling application must ensure that the buffer is large enough to hold the selected text.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c7318-112">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="c7318-112">Return value</span></span>

<span data-ttu-id="c7318-113">Ce message retourne le nombre de caractères copiés, à l’exclusion du caractère null de fin.</span><span class="sxs-lookup"><span data-stu-id="c7318-113">This message returns the number of characters copied, not including the terminating null character.</span></span>

## <a name="requirements"></a><span data-ttu-id="c7318-114">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="c7318-114">Requirements</span></span>



| <span data-ttu-id="c7318-115">Condition requise</span><span class="sxs-lookup"><span data-stu-id="c7318-115">Requirement</span></span> | <span data-ttu-id="c7318-116">Valeur</span><span class="sxs-lookup"><span data-stu-id="c7318-116">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="c7318-117">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="c7318-117">Minimum supported client</span></span><br/> | <span data-ttu-id="c7318-118">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="c7318-118">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="c7318-119">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="c7318-119">Minimum supported server</span></span><br/> | <span data-ttu-id="c7318-120">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="c7318-120">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="c7318-121">En-tête</span><span class="sxs-lookup"><span data-stu-id="c7318-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="c7318-122"><dt>RichEdit. h</dt></span><span class="sxs-lookup"><span data-stu-id="c7318-122"><dt>Richedit.h</dt></span></span> </dl> |



 

 





