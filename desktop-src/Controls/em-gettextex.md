---
title: Message EM_GETTEXTEX (RichEdit. h)
description: Obtient le texte à partir d’un contrôle RichEdit.
ms.assetid: 46431563-fde1-4407-ab7a-b2248c0e12b8
keywords:
- EM_GETTEXTEX les contrôles de message Windows
topic_type:
- apiref
api_name:
- EM_GETTEXTEX
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 357cfe37d3432b396183b500c945ad89397c0294
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104465150"
---
# <a name="em_gettextex-message"></a><span data-ttu-id="31fa0-104">\_Message GETTEXTEX em</span><span class="sxs-lookup"><span data-stu-id="31fa0-104">EM\_GETTEXTEX message</span></span>

<span data-ttu-id="31fa0-105">Obtient le texte à partir d’un contrôle RichEdit.</span><span class="sxs-lookup"><span data-stu-id="31fa0-105">Gets the text from a rich edit control.</span></span>

## <a name="parameters"></a><span data-ttu-id="31fa0-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="31fa0-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="31fa0-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="31fa0-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="31fa0-108">Pointeur vers une structure [**GETTEXTEX**](/windows/desktop/api/Richedit/ns-richedit-gettextex) , qui indique comment traduire le texte avant de le placer dans la mémoire tampon de sortie.</span><span class="sxs-lookup"><span data-stu-id="31fa0-108">Pointer to a [**GETTEXTEX**](/windows/desktop/api/Richedit/ns-richedit-gettextex) structure, which indicates how to translate the text before putting it into the output buffer.</span></span>

</dd> <dt>

<span data-ttu-id="31fa0-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="31fa0-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="31fa0-110">Pointeur vers la mémoire tampon pour recevoir le texte.</span><span class="sxs-lookup"><span data-stu-id="31fa0-110">Pointer to the buffer to receive the text.</span></span> <span data-ttu-id="31fa0-111">La taille de cette mémoire tampon, en octets, est spécifiée par le membre **CB** de la structure [**GETTEXTEX**](/windows/desktop/api/Richedit/ns-richedit-gettextex) .</span><span class="sxs-lookup"><span data-stu-id="31fa0-111">The size of this buffer, in bytes, is specified by the **cb** member of the [**GETTEXTEX**](/windows/desktop/api/Richedit/ns-richedit-gettextex) structure.</span></span> <span data-ttu-id="31fa0-112">Utilisez le message [**em \_ GETTEXTLENGTHEX**](em-gettextlengthex.md) pour connaître la taille requise pour la mémoire tampon.</span><span class="sxs-lookup"><span data-stu-id="31fa0-112">Use the [**EM\_GETTEXTLENGTHEX**](em-gettextlengthex.md) message to get the required size of the buffer.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="31fa0-113">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="31fa0-113">Return value</span></span>

<span data-ttu-id="31fa0-114">La valeur de retour est le nombre de **TCHAR** s copié dans la mémoire tampon de sortie, y compris la marque de fin null.</span><span class="sxs-lookup"><span data-stu-id="31fa0-114">The return value is the number of **TCHAR** s copied into the output buffer, including the null terminator.</span></span>

## <a name="remarks"></a><span data-ttu-id="31fa0-115">Notes</span><span class="sxs-lookup"><span data-stu-id="31fa0-115">Remarks</span></span>

<span data-ttu-id="31fa0-116">Si la taille de la mémoire tampon de sortie est inférieure à la taille du texte dans le contrôle, le contrôle d’édition copie le texte à partir de son début et le place dans la mémoire tampon jusqu’à ce que la mémoire tampon soit pleine.</span><span class="sxs-lookup"><span data-stu-id="31fa0-116">If the size of the output buffer is less than the size of the text in the control, the edit control will copy text from its beginning and place it in the buffer until the buffer is full.</span></span> <span data-ttu-id="31fa0-117">Un caractère null de fin sera toujours placé à la fin de la mémoire tampon.</span><span class="sxs-lookup"><span data-stu-id="31fa0-117">A terminating null character will still be placed at the end of the buffer.</span></span>

<span data-ttu-id="31fa0-118">Si du texte ANSI est demandé, **em \_ GETTEXTEX** utilise la fonction [**WideCharToMultiByte**](/windows/desktop/api/stringapiset/nf-stringapiset-widechartomultibyte) pour convertir les caractères Unicode en ANSI.</span><span class="sxs-lookup"><span data-stu-id="31fa0-118">If ANSI text is requested, **EM\_GETTEXTEX** uses the [**WideCharToMultiByte**](/windows/desktop/api/stringapiset/nf-stringapiset-widechartomultibyte) function to translate the Unicode characters to ANSI.</span></span> <span data-ttu-id="31fa0-119">Elle vous permet de passer d’Unicode à ANSI à l’aide d’une page de codes particulière.</span><span class="sxs-lookup"><span data-stu-id="31fa0-119">It allows you to go from Unicode to ANSI using a particular code page.</span></span> <span data-ttu-id="31fa0-120">La structure [**GETTEXTEX**](/windows/desktop/api/Richedit/ns-richedit-gettextex) contient des membres (**lpDefaultChar** et **lpUsedDefChar**) qui sont utilisés dans la traduction Unicode en ANSI.</span><span class="sxs-lookup"><span data-stu-id="31fa0-120">The [**GETTEXTEX**](/windows/desktop/api/Richedit/ns-richedit-gettextex) structure contains members (**lpDefaultChar** and **lpUsedDefChar**) that are used in the translation from Unicode to ANSI.</span></span>

## <a name="requirements"></a><span data-ttu-id="31fa0-121">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="31fa0-121">Requirements</span></span>



| <span data-ttu-id="31fa0-122">Condition requise</span><span class="sxs-lookup"><span data-stu-id="31fa0-122">Requirement</span></span> | <span data-ttu-id="31fa0-123">Valeur</span><span class="sxs-lookup"><span data-stu-id="31fa0-123">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="31fa0-124">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="31fa0-124">Minimum supported client</span></span><br/> | <span data-ttu-id="31fa0-125">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="31fa0-125">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="31fa0-126">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="31fa0-126">Minimum supported server</span></span><br/> | <span data-ttu-id="31fa0-127">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="31fa0-127">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="31fa0-128">En-tête</span><span class="sxs-lookup"><span data-stu-id="31fa0-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="31fa0-129"><dt>RichEdit. h</dt></span><span class="sxs-lookup"><span data-stu-id="31fa0-129"><dt>Richedit.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="31fa0-130">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="31fa0-130">See also</span></span>

<dl> <dt>

<span data-ttu-id="31fa0-131">**Référence**</span><span class="sxs-lookup"><span data-stu-id="31fa0-131">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="31fa0-132">**\_SETTEXTEX em**</span><span class="sxs-lookup"><span data-stu-id="31fa0-132">**EM\_SETTEXTEX**</span></span>](em-settextex.md)
</dt> <dt>

[<span data-ttu-id="31fa0-133">**GETTEXTEX**</span><span class="sxs-lookup"><span data-stu-id="31fa0-133">**GETTEXTEX**</span></span>](/windows/desktop/api/Richedit/ns-richedit-gettextex)
</dt> <dt>

<span data-ttu-id="31fa0-134">**Autres ressources**</span><span class="sxs-lookup"><span data-stu-id="31fa0-134">**Other Resources**</span></span>
</dt> <dt>

[<span data-ttu-id="31fa0-135">**WideCharToMultiByte**</span><span class="sxs-lookup"><span data-stu-id="31fa0-135">**WideCharToMultiByte**</span></span>](/windows/desktop/api/stringapiset/nf-stringapiset-widechartomultibyte)
</dt> <dt>

[<span data-ttu-id="31fa0-136">**WM, \_ SETTEXT**</span><span class="sxs-lookup"><span data-stu-id="31fa0-136">**WM\_SETTEXT**</span></span>](/windows/desktop/winmsg/wm-settext)
</dt> </dl>

 

