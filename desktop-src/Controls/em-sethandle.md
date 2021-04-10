---
title: Message EM_SETHANDLE (winuser. h)
description: Définit le handle de la mémoire qui sera utilisée par un contrôle d’édition multiligne.
ms.assetid: 0eae9365-62af-4040-8a51-273997a00b81
keywords:
- EM_SETHANDLE les contrôles de message Windows
topic_type:
- apiref
api_name:
- EM_SETHANDLE
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ac8f918d056db1000c6018f55d89095a73a15109
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104105574"
---
# <a name="em_sethandle-message"></a><span data-ttu-id="8501d-104">\_Message SETHANDLE em</span><span class="sxs-lookup"><span data-stu-id="8501d-104">EM\_SETHANDLE message</span></span>

<span data-ttu-id="8501d-105">Définit le handle de la mémoire qui sera utilisée par un contrôle d’édition multiligne.</span><span class="sxs-lookup"><span data-stu-id="8501d-105">Sets the handle of the memory that will be used by a multiline edit control.</span></span>

## <a name="parameters"></a><span data-ttu-id="8501d-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="8501d-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8501d-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="8501d-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="8501d-108">Handle vers la mémoire tampon que le contrôle d’édition utilise pour stocker le texte actuellement affiché au lieu d’allouer sa propre mémoire.</span><span class="sxs-lookup"><span data-stu-id="8501d-108">A handle to the memory buffer the edit control uses to store the currently displayed text instead of allocating its own memory.</span></span> <span data-ttu-id="8501d-109">Si nécessaire, le contrôle réalloue cette mémoire.</span><span class="sxs-lookup"><span data-stu-id="8501d-109">If necessary, the control reallocates this memory.</span></span>

</dd> <dt>

<span data-ttu-id="8501d-110">*lParam*</span><span class="sxs-lookup"><span data-stu-id="8501d-110">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="8501d-111">Ce paramètre n'est pas utilisé.</span><span class="sxs-lookup"><span data-stu-id="8501d-111">This parameter is not used.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8501d-112">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="8501d-112">Return value</span></span>

<span data-ttu-id="8501d-113">Ce message ne retourne pas de valeur.</span><span class="sxs-lookup"><span data-stu-id="8501d-113">This message does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="8501d-114">Notes</span><span class="sxs-lookup"><span data-stu-id="8501d-114">Remarks</span></span>

<span data-ttu-id="8501d-115">Avant qu’une application ne définisse un nouveau descripteur de mémoire, elle doit envoyer un message [**em \_ GETHANDLE**](em-gethandle.md) pour récupérer le handle de la mémoire tampon actuelle et libérer cette mémoire.</span><span class="sxs-lookup"><span data-stu-id="8501d-115">Before an application sets a new memory handle, it should send an [**EM\_GETHANDLE**](em-gethandle.md) message to retrieve the handle of the current memory buffer and should free that memory.</span></span>

<span data-ttu-id="8501d-116">Un contrôle d’édition réalloue automatiquement la mémoire tampon donnée à chaque fois qu’elle a besoin d’espace supplémentaire pour le texte, ou elle supprime suffisamment de texte afin que de l’espace supplémentaire ne soit plus nécessaire.</span><span class="sxs-lookup"><span data-stu-id="8501d-116">An edit control automatically reallocates the given buffer whenever it needs additional space for text, or it removes enough text so that additional space is no longer needed.</span></span>

<span data-ttu-id="8501d-117">L’envoi d’un message **em \_ SETHANDLE** efface le tampon d’annulation ([**em \_ CANUNDO**](em-canundo.md) retourne zéro) et l’indicateur de modification interne ([**em \_ GETMODIFY**](em-getmodify.md) retourne zéro).</span><span class="sxs-lookup"><span data-stu-id="8501d-117">Sending an **EM\_SETHANDLE** message clears the undo buffer ([**EM\_CANUNDO**](em-canundo.md) returns zero) and the internal modification flag ([**EM\_GETMODIFY**](em-getmodify.md) returns zero).</span></span> <span data-ttu-id="8501d-118">La fenêtre Modifier le contrôle est redessinée.</span><span class="sxs-lookup"><span data-stu-id="8501d-118">The edit control window is redrawn.</span></span>

<span data-ttu-id="8501d-119">**Modification riche :** Le **message \_ SETHANDLE em** n’est pas pris en charge.</span><span class="sxs-lookup"><span data-stu-id="8501d-119">**Rich Edit:** The **EM\_SETHANDLE** message is not supported.</span></span> <span data-ttu-id="8501d-120">Les contrôles RichEdit ne stockent pas de texte sous la forme d’un simple tableau de caractères.</span><span class="sxs-lookup"><span data-stu-id="8501d-120">Rich edit controls do not store text as a simple array of characters.</span></span>

## <a name="requirements"></a><span data-ttu-id="8501d-121">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="8501d-121">Requirements</span></span>



| <span data-ttu-id="8501d-122">Condition requise</span><span class="sxs-lookup"><span data-stu-id="8501d-122">Requirement</span></span> | <span data-ttu-id="8501d-123">Valeur</span><span class="sxs-lookup"><span data-stu-id="8501d-123">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8501d-124">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="8501d-124">Minimum supported client</span></span><br/> | <span data-ttu-id="8501d-125">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="8501d-125">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="8501d-126">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="8501d-126">Minimum supported server</span></span><br/> | <span data-ttu-id="8501d-127">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="8501d-127">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="8501d-128">En-tête</span><span class="sxs-lookup"><span data-stu-id="8501d-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="8501d-129"><dt>Winuser. h (inclure Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="8501d-129"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8501d-130">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="8501d-130">See also</span></span>

<dl> <dt>

<span data-ttu-id="8501d-131">**Référence**</span><span class="sxs-lookup"><span data-stu-id="8501d-131">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="8501d-132">**EM \_ CANUNDO**</span><span class="sxs-lookup"><span data-stu-id="8501d-132">**EM\_CANUNDO**</span></span>](em-canundo.md)
</dt> <dt>

[<span data-ttu-id="8501d-133">**EM \_ GETHANDLE**</span><span class="sxs-lookup"><span data-stu-id="8501d-133">**EM\_GETHANDLE**</span></span>](em-gethandle.md)
</dt> <dt>

[<span data-ttu-id="8501d-134">**\_GETMODIFY em**</span><span class="sxs-lookup"><span data-stu-id="8501d-134">**EM\_GETMODIFY**</span></span>](em-getmodify.md)
</dt> </dl>

 

 





