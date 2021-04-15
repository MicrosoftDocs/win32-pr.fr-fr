---
title: Message EM_GETFILELINE (CommCtrl. h)
description: Copie une ligne de texte à partir d’un contrôle d’édition, indépendamment de la façon dont les lignes sont affichées à l’écran, et les place dans une mémoire tampon spécifiée.
ms.assetid: ff56d2c6-5013-46c6-90d8-ee2bdc9074b1
keywords:
- EM_GETFILELINE les contrôles de message Windows
topic_type:
- apiref
api_name:
- EM_GETLINE
api_location:
- CommCtrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 10/19/2018
ms.openlocfilehash: 6b3be3ea4ae883fc808f7ddc8fb60f0d93bcd6ed
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104466110"
---
# <a name="em_getfileline-message-commctrlh"></a><span data-ttu-id="583f0-104">Message EM_GETFILELINE (CommCtrl. h)</span><span class="sxs-lookup"><span data-stu-id="583f0-104">EM_GETFILELINE message (CommCtrl.h)</span></span>

<span data-ttu-id="583f0-105">Copie une ligne de texte à partir d’un contrôle d’édition, indépendamment de la façon dont les lignes sont affichées à l’écran, et les place dans une mémoire tampon spécifiée.</span><span class="sxs-lookup"><span data-stu-id="583f0-105">Copies a line of text from an edit control, independently of how lines are displayed on the screen, and places it in a specified buffer.</span></span>

## <a name="parameters"></a><span data-ttu-id="583f0-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="583f0-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="583f0-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="583f0-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="583f0-108">Index de base zéro de la ligne à récupérer à partir d’un contrôle d’édition multiligne.</span><span class="sxs-lookup"><span data-stu-id="583f0-108">The zero-based index of the line to retrieve from a multiline edit control.</span></span> <span data-ttu-id="583f0-109">La valeur zéro spécifie la ligne la plus grande.</span><span class="sxs-lookup"><span data-stu-id="583f0-109">A value of zero specifies the topmost line.</span></span> <span data-ttu-id="583f0-110">Ce paramètre est ignoré par un contrôle d’édition sur une seule ligne.</span><span class="sxs-lookup"><span data-stu-id="583f0-110">This parameter is ignored by a single-line edit control.</span></span>

</dd> <dt>

<span data-ttu-id="583f0-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="583f0-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="583f0-112">Pointeur vers la mémoire tampon qui reçoit une copie de la ligne.</span><span class="sxs-lookup"><span data-stu-id="583f0-112">A pointer to the buffer that receives a copy of the line.</span></span> <span data-ttu-id="583f0-113">Avant d’envoyer le message, définissez le premier mot de cette mémoire tampon sur la taille, dans **TCHAR** s, de la mémoire tampon.</span><span class="sxs-lookup"><span data-stu-id="583f0-113">Before sending the message, set the first word of this buffer to the size, in **TCHAR** s, of the buffer.</span></span> <span data-ttu-id="583f0-114">Pour le texte ANSI, il s’agit du nombre d’octets ; pour le texte Unicode, il s’agit du nombre de caractères.</span><span class="sxs-lookup"><span data-stu-id="583f0-114">For ANSI text, this is the number of bytes; for Unicode text, this is the number of characters.</span></span> <span data-ttu-id="583f0-115">La taille dans le premier mot est remplacée par la ligne copiée.</span><span class="sxs-lookup"><span data-stu-id="583f0-115">The size in the first word is overwritten by the copied line.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="583f0-116">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="583f0-116">Return value</span></span>

<span data-ttu-id="583f0-117">La valeur de retour est le nombre de **TCHAR** s copié.</span><span class="sxs-lookup"><span data-stu-id="583f0-117">The return value is the number of **TCHAR** s copied.</span></span> <span data-ttu-id="583f0-118">La valeur de retour est égale à zéro si le numéro de ligne spécifié par le paramètre *wParam* est supérieur au nombre de lignes dans le contrôle d’édition.</span><span class="sxs-lookup"><span data-stu-id="583f0-118">The return value is zero if the line number specified by the *wParam* parameter is greater than the number of lines in the edit control.</span></span>

## <a name="remarks"></a><span data-ttu-id="583f0-119">Notes</span><span class="sxs-lookup"><span data-stu-id="583f0-119">Remarks</span></span>

<span data-ttu-id="583f0-120">La ligne copiée ne contient pas de caractère null de fin.</span><span class="sxs-lookup"><span data-stu-id="583f0-120">The copied line does not contain a terminating null character.</span></span>

## <a name="requirements"></a><span data-ttu-id="583f0-121">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="583f0-121">Requirements</span></span>



| <span data-ttu-id="583f0-122">Condition requise</span><span class="sxs-lookup"><span data-stu-id="583f0-122">Requirement</span></span> | <span data-ttu-id="583f0-123">Valeur</span><span class="sxs-lookup"><span data-stu-id="583f0-123">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="583f0-124">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="583f0-124">Minimum supported client</span></span><br/> | <span data-ttu-id="583f0-125">Applications de bureau Windows 10, 1809 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="583f0-125">Windows 10, 1809 \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="583f0-126">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="583f0-126">Minimum supported server</span></span><br/> | <span data-ttu-id="583f0-127">Applications de bureau Windows Server 2019 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="583f0-127">Windows Server 2019 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="583f0-128">En-tête</span><span class="sxs-lookup"><span data-stu-id="583f0-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="583f0-129"><dt>CommCtrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="583f0-129"><dt>CommCtrl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="583f0-130">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="583f0-130">See also</span></span>

<dl> <dt>

<span data-ttu-id="583f0-131">**Référence**</span><span class="sxs-lookup"><span data-stu-id="583f0-131">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="583f0-132">**\_FILELINELENGTH em**</span><span class="sxs-lookup"><span data-stu-id="583f0-132">**EM\_FILELINELENGTH**</span></span>](em-filelinelength.md)
</dt> <dt>

[<span data-ttu-id="583f0-133">**Modifier \_ GetFileLine**</span><span class="sxs-lookup"><span data-stu-id="583f0-133">**Edit\_GetFileLine**</span></span>](/windows/win32/api/commctrl/nf-commctrl-edit_getfileline)
</dt> <dt>

<span data-ttu-id="583f0-134">**Autres ressources**</span><span class="sxs-lookup"><span data-stu-id="583f0-134">**Other Resources**</span></span>
</dt> <dt>

[<span data-ttu-id="583f0-135">**WM \_ GETTEXT**</span><span class="sxs-lookup"><span data-stu-id="583f0-135">**WM\_GETTEXT**</span></span>](/windows/desktop/winmsg/wm-gettext)
</dt> </dl>

 

