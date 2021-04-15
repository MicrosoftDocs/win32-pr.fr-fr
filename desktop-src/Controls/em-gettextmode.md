---
title: Message EM_GETTEXTMODE (RichEdit. h)
description: Obtient le mode texte actuel et le niveau d’annulation d’un contrôle RichEdit.
ms.assetid: 5c976a82-9c51-4700-9db4-a6b0ed7bb852
keywords:
- EM_GETTEXTMODE les contrôles de message Windows
topic_type:
- apiref
api_name:
- EM_GETTEXTMODE
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 012a12aec573518c859ec7f2a0319036dcd1ef87
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104466239"
---
# <a name="em_gettextmode-message"></a><span data-ttu-id="e03e9-104">\_Message GETTEXTMODE em</span><span class="sxs-lookup"><span data-stu-id="e03e9-104">EM\_GETTEXTMODE message</span></span>

<span data-ttu-id="e03e9-105">Obtient le mode texte actuel et le niveau d’annulation d’un contrôle RichEdit.</span><span class="sxs-lookup"><span data-stu-id="e03e9-105">Gets the current text mode and undo level of a rich edit control.</span></span>

## <a name="parameters"></a><span data-ttu-id="e03e9-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="e03e9-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e03e9-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="e03e9-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="e03e9-108">Non utilisé ; doit être égal à zéro.</span><span class="sxs-lookup"><span data-stu-id="e03e9-108">Not used; must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="e03e9-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="e03e9-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="e03e9-110">Non utilisé ; doit être égal à zéro.</span><span class="sxs-lookup"><span data-stu-id="e03e9-110">Not used; must be zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e03e9-111">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="e03e9-111">Return value</span></span>

<span data-ttu-id="e03e9-112">La valeur de retour est une ou plusieurs valeurs du type d’énumération [**TextMode**](/windows/win32/api/richedit/ne-richedit-textmode) .</span><span class="sxs-lookup"><span data-stu-id="e03e9-112">The return value is one or more values from the [**TEXTMODE**](/windows/win32/api/richedit/ne-richedit-textmode) enumeration type.</span></span> <span data-ttu-id="e03e9-113">Les valeurs indiquent le mode texte actuel et le niveau d’annulation du contrôle.</span><span class="sxs-lookup"><span data-stu-id="e03e9-113">The values indicate the current text mode and undo level of the control.</span></span>

## <a name="requirements"></a><span data-ttu-id="e03e9-114">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="e03e9-114">Requirements</span></span>



| <span data-ttu-id="e03e9-115">Condition requise</span><span class="sxs-lookup"><span data-stu-id="e03e9-115">Requirement</span></span> | <span data-ttu-id="e03e9-116">Valeur</span><span class="sxs-lookup"><span data-stu-id="e03e9-116">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="e03e9-117">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="e03e9-117">Minimum supported client</span></span><br/> | <span data-ttu-id="e03e9-118">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="e03e9-118">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="e03e9-119">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="e03e9-119">Minimum supported server</span></span><br/> | <span data-ttu-id="e03e9-120">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="e03e9-120">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="e03e9-121">En-tête</span><span class="sxs-lookup"><span data-stu-id="e03e9-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="e03e9-122"><dt>RichEdit. h</dt></span><span class="sxs-lookup"><span data-stu-id="e03e9-122"><dt>Richedit.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e03e9-123">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="e03e9-123">See also</span></span>

<dl> <dt>

<span data-ttu-id="e03e9-124">**Référence**</span><span class="sxs-lookup"><span data-stu-id="e03e9-124">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="e03e9-125">**\_SETTEXTMODE em**</span><span class="sxs-lookup"><span data-stu-id="e03e9-125">**EM\_SETTEXTMODE**</span></span>](em-settextmode.md)
</dt> <dt>

[<span data-ttu-id="e03e9-126">**TEXTMODE**</span><span class="sxs-lookup"><span data-stu-id="e03e9-126">**TEXTMODE**</span></span>](/windows/win32/api/richedit/ne-richedit-textmode)
</dt> </dl>

 

 





