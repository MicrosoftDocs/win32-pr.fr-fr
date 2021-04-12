---
title: Message COLOROKSTRING (COMMDLG. h)
description: Une boîte de dialogue de couleur envoie le message COLOROKSTRING Registered à votre procédure de Hook, CCHookProc, lorsque l’utilisateur sélectionne une couleur et clique sur le bouton OK.
ms.assetid: 18b28558-1262-4c88-becf-76ce799b7542
keywords:
- Boîtes de dialogue de message COLOROKSTRING
topic_type:
- apiref
api_name:
- COLOROKSTRING
- COLOROKSTRINGA
- COLOROKSTRINGW
api_location:
- Commdlg.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 86229c71f1234efb4b561ac73bc8aa20f6258cdc
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104103648"
---
# <a name="colorokstring-message"></a><span data-ttu-id="84af8-104">Message COLOROKSTRING</span><span class="sxs-lookup"><span data-stu-id="84af8-104">COLOROKSTRING message</span></span>

<span data-ttu-id="84af8-105">Une boîte de dialogue de **couleur** envoie le message **COLOROKSTRING** Registered à votre procédure de Hook, [*CCHookProc*](/windows/win32/api/commdlg/nc-commdlg-lpcchookproc), lorsque l’utilisateur sélectionne une couleur et clique sur le bouton **OK** .</span><span class="sxs-lookup"><span data-stu-id="84af8-105">A **Color** dialog box sends the **COLOROKSTRING** registered message to your hook procedure, [*CCHookProc*](/windows/win32/api/commdlg/nc-commdlg-lpcchookproc), when the user selects a color and clicks the **OK** button.</span></span> <span data-ttu-id="84af8-106">La procédure de raccordement peut accepter la couleur et autoriser la fermeture de la boîte de dialogue, ou refuser la couleur et forcer la boîte de dialogue à rester ouverte.</span><span class="sxs-lookup"><span data-stu-id="84af8-106">The hook procedure can accept the color and allow the dialog box to close, or reject the color and force the dialog box to remain open.</span></span>


```C++
#define COLOROKSTRING TEXT("commdlg_ColorOK")
```



## <a name="parameters"></a><span data-ttu-id="84af8-107">Paramètres</span><span class="sxs-lookup"><span data-stu-id="84af8-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="84af8-108">*wParam*</span><span class="sxs-lookup"><span data-stu-id="84af8-108">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="84af8-109">Ce paramètre n'est pas utilisé.</span><span class="sxs-lookup"><span data-stu-id="84af8-109">This parameter is not used.</span></span>

</dd> <dt>

<span data-ttu-id="84af8-110">*lParam*</span><span class="sxs-lookup"><span data-stu-id="84af8-110">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="84af8-111">Pointeur vers une structure [**les ChooseColor.**](/windows/win32/api/commdlg/ns-commdlg-choosecolora-r1) .</span><span class="sxs-lookup"><span data-stu-id="84af8-111">A pointer to a [**CHOOSECOLOR**](/windows/win32/api/commdlg/ns-commdlg-choosecolora-r1) structure.</span></span> <span data-ttu-id="84af8-112">Le membre **rgbResult** de cette structure contient la valeur de couleur RVB de la couleur sélectionnée.</span><span class="sxs-lookup"><span data-stu-id="84af8-112">The **rgbResult** member of this structure contains the RGB color value of the selected color.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="84af8-113">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="84af8-113">Return value</span></span>

<span data-ttu-id="84af8-114">Si la procédure de raccordement retourne la valeur zéro, la boîte de dialogue **couleur** accepte la couleur sélectionnée et se ferme.</span><span class="sxs-lookup"><span data-stu-id="84af8-114">If the hook procedure returns zero, the **Color** dialog box accepts the selected color and closes.</span></span>

<span data-ttu-id="84af8-115">Si la procédure de raccordement retourne une valeur différente de zéro, la boîte de dialogue **couleur** rejette la couleur sélectionnée et reste ouverte.</span><span class="sxs-lookup"><span data-stu-id="84af8-115">If the hook procedure returns a nonzero value, the **Color** dialog box rejects the selected color and remains open.</span></span>

## <a name="remarks"></a><span data-ttu-id="84af8-116">Notes</span><span class="sxs-lookup"><span data-stu-id="84af8-116">Remarks</span></span>

<span data-ttu-id="84af8-117">La procédure de hook doit spécifier la constante **COLOROKSTRING** dans un appel à la fonction [**RegisterWindowMessage**](/windows/desktop/api/winuser/nf-winuser-registerwindowmessagea) pour obtenir l’identificateur du message envoyé par la boîte de dialogue.</span><span class="sxs-lookup"><span data-stu-id="84af8-117">The hook procedure must specify the **COLOROKSTRING** constant in a call to the [**RegisterWindowMessage**](/windows/desktop/api/winuser/nf-winuser-registerwindowmessagea) function to get the identifier of the message sent by the dialog box.</span></span>

## <a name="requirements"></a><span data-ttu-id="84af8-118">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="84af8-118">Requirements</span></span>



| <span data-ttu-id="84af8-119">Condition requise</span><span class="sxs-lookup"><span data-stu-id="84af8-119">Requirement</span></span> | <span data-ttu-id="84af8-120">Valeur</span><span class="sxs-lookup"><span data-stu-id="84af8-120">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="84af8-121">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="84af8-121">Minimum supported client</span></span><br/> | <span data-ttu-id="84af8-122">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="84af8-122">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="84af8-123">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="84af8-123">Minimum supported server</span></span><br/> | <span data-ttu-id="84af8-124">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="84af8-124">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="84af8-125">En-tête</span><span class="sxs-lookup"><span data-stu-id="84af8-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="84af8-126"><dt>Commdlg. h (inclure Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="84af8-126"><dt>Commdlg.h (include Windows.h)</dt></span></span> </dl> |
| <span data-ttu-id="84af8-127">Noms Unicode et ANSI</span><span class="sxs-lookup"><span data-stu-id="84af8-127">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="84af8-128">**COLOROKSTRINGW** (Unicode) et **COLOROKSTRINGA** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="84af8-128">**COLOROKSTRINGW** (Unicode) and **COLOROKSTRINGA** (ANSI)</span></span><br/>                                    |



## <a name="see-also"></a><span data-ttu-id="84af8-129">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="84af8-129">See also</span></span>

<dl> <dt>

<span data-ttu-id="84af8-130">**Référence**</span><span class="sxs-lookup"><span data-stu-id="84af8-130">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="84af8-131">**LES ChooseColor.**</span><span class="sxs-lookup"><span data-stu-id="84af8-131">**CHOOSECOLOR**</span></span>](/windows/win32/api/commdlg/ns-commdlg-choosecolora-r1)
</dt> <dt>

[<span data-ttu-id="84af8-132">**RegisterWindowMessage**</span><span class="sxs-lookup"><span data-stu-id="84af8-132">**RegisterWindowMessage**</span></span>](/windows/desktop/api/winuser/nf-winuser-registerwindowmessagea)
</dt> <dt>

<span data-ttu-id="84af8-133">**Méthodologique**</span><span class="sxs-lookup"><span data-stu-id="84af8-133">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="84af8-134">Bibliothèque de boîtes de dialogue communes</span><span class="sxs-lookup"><span data-stu-id="84af8-134">Common Dialog Box Library</span></span>](common-dialog-box-library.md)
</dt> </dl>

 

