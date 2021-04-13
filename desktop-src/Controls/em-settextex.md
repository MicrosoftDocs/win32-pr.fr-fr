---
title: Message EM_SETTEXTEX (RichEdit. h)
description: Combine les fonctionnalités des messages WM \_ SETTEXT et em \_ REPLACESEL et ajoute la possibilité de définir du texte à l’aide d’une page de codes et d’utiliser du texte enrichi ou du texte brut.
ms.assetid: 1ba9e4c0-7870-4057-8a8b-d0e6577349ac
keywords:
- EM_SETTEXTEX les contrôles de message Windows
topic_type:
- apiref
api_name:
- EM_SETTEXTEX
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cfdd7dece965f70fe41d40edf44d365795d44fc4
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104465703"
---
# <a name="em_settextex-message"></a><span data-ttu-id="956dd-104">\_Message SETTEXTEX em</span><span class="sxs-lookup"><span data-stu-id="956dd-104">EM\_SETTEXTEX message</span></span>

<span data-ttu-id="956dd-105">Combine les fonctionnalités des messages [**WM \_ SETTEXT**](/windows/desktop/winmsg/wm-settext) et [**em \_ REPLACESEL**](em-replacesel.md) et ajoute la possibilité de définir du texte à l’aide d’une page de codes et d’utiliser du texte enrichi ou du texte brut.</span><span class="sxs-lookup"><span data-stu-id="956dd-105">Combines the functionality of the [**WM\_SETTEXT**](/windows/desktop/winmsg/wm-settext) and [**EM\_REPLACESEL**](em-replacesel.md) messages, and adds the ability to set text using a code page and to use either rich text or plain text.</span></span>

## <a name="parameters"></a><span data-ttu-id="956dd-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="956dd-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="956dd-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="956dd-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="956dd-108">Pointeur vers une structure [**SETTEXTEX**](/windows/desktop/api/Richedit/ns-richedit-settextex) qui spécifie des indicateurs et une page de codes facultative à utiliser lors de la conversion en Unicode.</span><span class="sxs-lookup"><span data-stu-id="956dd-108">Pointer to a [**SETTEXTEX**](/windows/desktop/api/Richedit/ns-richedit-settextex) structure that specifies flags and an optional code page to use in translating to Unicode.</span></span>

</dd> <dt>

<span data-ttu-id="956dd-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="956dd-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="956dd-110">Pointeur vers le texte se terminant par null à insérer.</span><span class="sxs-lookup"><span data-stu-id="956dd-110">Pointer to the null-terminated text to insert.</span></span> <span data-ttu-id="956dd-111">Ce texte est une chaîne ANSI, sauf si la page de codes est 1200 (Unicode).</span><span class="sxs-lookup"><span data-stu-id="956dd-111">This text is an ANSI string, unless the code page is 1200 (Unicode).</span></span> <span data-ttu-id="956dd-112">Si *lParam* commence par une séquence ASCII RTF valide, par exemple « { \\ RTF » ou « {urtf », le texte est lu à l’aide du lecteur RTF.</span><span class="sxs-lookup"><span data-stu-id="956dd-112">If *lParam* starts with a valid RTF ASCII sequence for example, "{\\rtf" or "{urtf" the text is read in using the RTF reader.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="956dd-113">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="956dd-113">Return value</span></span>

<span data-ttu-id="956dd-114">Si l’opération définit tout le texte et s’effectue correctement, la valeur de retour est 1.</span><span class="sxs-lookup"><span data-stu-id="956dd-114">If the operation is setting all of the text and succeeds, the return value is 1.</span></span>

<span data-ttu-id="956dd-115">Si l’opération définit la sélection et s’effectue correctement, la valeur de retour est le nombre d’octets ou de caractères copiés.</span><span class="sxs-lookup"><span data-stu-id="956dd-115">If the operation is setting the selection and succeeds, the return value is the number of bytes or characters copied.</span></span>

<span data-ttu-id="956dd-116">Si l’opération échoue, la valeur de retour est zéro.</span><span class="sxs-lookup"><span data-stu-id="956dd-116">If the operation fails, the return value is zero.</span></span>

## <a name="requirements"></a><span data-ttu-id="956dd-117">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="956dd-117">Requirements</span></span>



| <span data-ttu-id="956dd-118">Condition requise</span><span class="sxs-lookup"><span data-stu-id="956dd-118">Requirement</span></span> | <span data-ttu-id="956dd-119">Valeur</span><span class="sxs-lookup"><span data-stu-id="956dd-119">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="956dd-120">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="956dd-120">Minimum supported client</span></span><br/> | <span data-ttu-id="956dd-121">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="956dd-121">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="956dd-122">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="956dd-122">Minimum supported server</span></span><br/> | <span data-ttu-id="956dd-123">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="956dd-123">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="956dd-124">Composant redistribuable</span><span class="sxs-lookup"><span data-stu-id="956dd-124">Redistributable</span></span><br/>          | <span data-ttu-id="956dd-125">Édition enrichie 3,0</span><span class="sxs-lookup"><span data-stu-id="956dd-125">Rich Edit 3.0</span></span><br/>                                                              |
| <span data-ttu-id="956dd-126">En-tête</span><span class="sxs-lookup"><span data-stu-id="956dd-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="956dd-127"><dt>RichEdit. h</dt></span><span class="sxs-lookup"><span data-stu-id="956dd-127"><dt>Richedit.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="956dd-128">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="956dd-128">See also</span></span>

<dl> <dt>

<span data-ttu-id="956dd-129">**Référence**</span><span class="sxs-lookup"><span data-stu-id="956dd-129">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="956dd-130">**\_GETTEXTEX em**</span><span class="sxs-lookup"><span data-stu-id="956dd-130">**EM\_GETTEXTEX**</span></span>](em-gettextex.md)
</dt> <dt>

[<span data-ttu-id="956dd-131">**SETTEXTEX**</span><span class="sxs-lookup"><span data-stu-id="956dd-131">**SETTEXTEX**</span></span>](/windows/desktop/api/Richedit/ns-richedit-settextex)
</dt> </dl>

 

