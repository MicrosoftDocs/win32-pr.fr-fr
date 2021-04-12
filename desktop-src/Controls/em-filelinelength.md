---
title: Message EM_FILELINELENGTH (CommCtrl. h)
description: Récupère la longueur, en caractères, d’une ligne dans un contrôle d’édition, indépendamment de la façon dont les lignes sont affichées à l’écran.
ms.assetid: cfb0632c-9ba9-4864-939a-dbbaed6c177e
keywords:
- EM_FILELINELENGTH les contrôles de message Windows
topic_type:
- apiref
api_name:
- EM_FILELINELENGTH
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4aa50f4d9b49253a558095be78e0e781d7d4c7f8
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104508713"
---
# <a name="em_filelinelength-message"></a><span data-ttu-id="2c757-104">\_Message FILELINELENGTH em</span><span class="sxs-lookup"><span data-stu-id="2c757-104">EM\_FILELINELENGTH message</span></span>

<span data-ttu-id="2c757-105">Récupère la longueur, en caractères, d’une ligne dans un contrôle d’édition, indépendamment de la façon dont les lignes sont affichées à l’écran.</span><span class="sxs-lookup"><span data-stu-id="2c757-105">Retrieves the length, in characters, of a line in an edit control, independently of how lines are displayed on the screen.</span></span>

## <a name="parameters"></a><span data-ttu-id="2c757-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="2c757-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2c757-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="2c757-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="2c757-108">Index de caractère d’un caractère de la ligne dont la longueur doit être récupérée.</span><span class="sxs-lookup"><span data-stu-id="2c757-108">The character index of a character in the line whose length is to be retrieved.</span></span> <span data-ttu-id="2c757-109">Si ce paramètre est supérieur au nombre de caractères dans le contrôle, la valeur de retour est zéro.</span><span class="sxs-lookup"><span data-stu-id="2c757-109">If this parameter is greater than the number of characters in the control, the return value is zero.</span></span>

<span data-ttu-id="2c757-110">Ce paramètre peut être-1.</span><span class="sxs-lookup"><span data-stu-id="2c757-110">This parameter can be -1.</span></span> <span data-ttu-id="2c757-111">Dans ce cas, le message retourne le nombre de caractères non sélectionnés sur les lignes contenant les caractères sélectionnés.</span><span class="sxs-lookup"><span data-stu-id="2c757-111">In this case, the message returns the number of unselected characters on lines containing selected characters.</span></span> <span data-ttu-id="2c757-112">Par exemple, si la sélection est étendue à partir du quatrième caractère d’une ligne jusqu’au huitième caractère à partir de la fin de la ligne suivante, la valeur de retour est 10 (trois caractères sur la première ligne et sept sur la suivante).</span><span class="sxs-lookup"><span data-stu-id="2c757-112">For example, if the selection extended from the fourth character of one line through the eighth character from the end of the next line, the return value would be 10 (three characters on the first line and seven on the next).</span></span>

</dd> <dt>

<span data-ttu-id="2c757-113">*lParam*</span><span class="sxs-lookup"><span data-stu-id="2c757-113">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="2c757-114">Ce paramètre n'est pas utilisé.</span><span class="sxs-lookup"><span data-stu-id="2c757-114">This parameter is not used.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2c757-115">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="2c757-115">Return value</span></span>

<span data-ttu-id="2c757-116">Pour les contrôles d’édition multiligne, la valeur de retour est la longueur, dans **TCHAR** s, de la ligne spécifiée par le paramètre *wParam* , indépendamment de la façon dont les lignes sont affichées à l’écran.</span><span class="sxs-lookup"><span data-stu-id="2c757-116">For multiline edit controls, the return value is the length, in **TCHAR** s, of the line specified by the *wParam* parameter, independently of how lines are displayed on the screen.</span></span> <span data-ttu-id="2c757-117">Elle n’inclut pas le caractère de retour chariot ou de saut de ligne à la fin de la ligne.</span><span class="sxs-lookup"><span data-stu-id="2c757-117">It does not include the carriage-return or linefeed character at the end of the line.</span></span>

<span data-ttu-id="2c757-118">Pour les contrôles d’édition sur une seule ligne, la valeur de retour est la longueur, dans **TCHAR** s, du texte dans le contrôle d’édition.</span><span class="sxs-lookup"><span data-stu-id="2c757-118">For single-line edit controls, the return value is the length, in **TCHAR** s, of the text in the edit control.</span></span>

<span data-ttu-id="2c757-119">Si *wParam* est supérieur au nombre de caractères dans le contrôle, la valeur de retour est zéro.</span><span class="sxs-lookup"><span data-stu-id="2c757-119">If *wParam* is greater than the number of characters in the control, the return value is zero.</span></span>

## <a name="remarks"></a><span data-ttu-id="2c757-120">Notes</span><span class="sxs-lookup"><span data-stu-id="2c757-120">Remarks</span></span>

<span data-ttu-id="2c757-121">Utilisez le message [**em \_ FILELINEINDEX**](em-lineindex.md) pour récupérer un index de caractère pour un numéro de ligne donné au sein d’un contrôle d’édition multiligne, indépendamment de la façon dont les lignes sont affichées à l’écran.</span><span class="sxs-lookup"><span data-stu-id="2c757-121">Use the [**EM\_FILELINEINDEX**](em-lineindex.md) message to retrieve a character index for a given line number within a multiline edit control, independently of how lines are displayed on the screen.</span></span>

## <a name="requirements"></a><span data-ttu-id="2c757-122">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="2c757-122">Requirements</span></span>



| <span data-ttu-id="2c757-123">Condition requise</span><span class="sxs-lookup"><span data-stu-id="2c757-123">Requirement</span></span> | <span data-ttu-id="2c757-124">Valeur</span><span class="sxs-lookup"><span data-stu-id="2c757-124">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2c757-125">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="2c757-125">Minimum supported client</span></span><br/> | <span data-ttu-id="2c757-126">Applications de bureau Windows 10, 1809 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="2c757-126">Windows 10, 1809 \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="2c757-127">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="2c757-127">Minimum supported server</span></span><br/> | <span data-ttu-id="2c757-128">Applications de bureau Windows Server 2019 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="2c757-128">Windows Server 2019 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="2c757-129">En-tête</span><span class="sxs-lookup"><span data-stu-id="2c757-129">Header</span></span><br/>                   | <dl> <span data-ttu-id="2c757-130"><dt>CommCtrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="2c757-130"><dt>CommCtrl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2c757-131">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="2c757-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2c757-132">**\_FILELINEINDEX em**</span><span class="sxs-lookup"><span data-stu-id="2c757-132">**EM\_FILELINEINDEX**</span></span>](em-filelineindex.md)
</dt> </dl>

 

 





