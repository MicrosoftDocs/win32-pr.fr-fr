---
title: Message EM_SETENDOFLINE (CommCtrl. h)
description: Définit le caractère de fin de ligne utilisé lors de l’insertion d’un LineBreak.
ms.assetid: a10b3f57-0e67-4a0f-89f3-9c8ebd1514f8
keywords:
- EM_SETENDOFLINE les contrôles de message Windows
topic_type:
- apiref
api_name:
- EM_SETENDOFLINE
api_location:
- CommCtrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 10/19/2018
ms.openlocfilehash: 5ee7c500ba3818cad0f5ee74e9994ed8af049ea0
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104466543"
---
# <a name="em_setendofline-message"></a><span data-ttu-id="8c2db-104">\_Message SETENDOFLINE em</span><span class="sxs-lookup"><span data-stu-id="8c2db-104">EM\_SETENDOFLINE message</span></span>

<span data-ttu-id="8c2db-105">Définit le caractère de fin de ligne utilisé lors de l’insertion d’un LineBreak.</span><span class="sxs-lookup"><span data-stu-id="8c2db-105">Sets the end-of-line character used when a linebreak is inserted.</span></span>

## <a name="parameters"></a><span data-ttu-id="8c2db-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="8c2db-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8c2db-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="8c2db-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="8c2db-108">Spécifie le caractère de fin de ligne utilisé lors de l’insertion d’un LineBreak.</span><span class="sxs-lookup"><span data-stu-id="8c2db-108">Specifies the end-of-line character used when a linebreak is inserted.</span></span> <span data-ttu-id="8c2db-109">Il peut s’agir de l’une des valeurs suivantes.</span><span class="sxs-lookup"><span data-stu-id="8c2db-109">This can be one of the following values.</span></span>


| <span data-ttu-id="8c2db-110">Valeur</span><span class="sxs-lookup"><span data-stu-id="8c2db-110">Value</span></span>                                                                                                                                                   | <span data-ttu-id="8c2db-111">Signification</span><span class="sxs-lookup"><span data-stu-id="8c2db-111">Meaning</span></span>                                                                                        |
|---------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------|
| <span id="EC_ENDOFLINE_DETECTFROMCONTENT"></span><span id="ec_endofline_detectfromcontent"></span><dl> <span data-ttu-id="8c2db-112"><dt>**\_ENDOFLINE EC \_ DETECTFROMCONTENT**</dt></span><span class="sxs-lookup"><span data-stu-id="8c2db-112"><dt>**EC\_ENDOFLINE\_DETECTFROMCONTENT**</dt></span></span> </dl> | <span data-ttu-id="8c2db-113">Définit le caractère de fin de ligne utilisé pour le nouveau sauts sur le caractère utilisé par le document actif.</span><span class="sxs-lookup"><span data-stu-id="8c2db-113">Sets the end-of-line character used for new linebreaks to the character used by the current document.</span></span><br/>  |
| <span id="EC_ENDOFLINE_CRLF"></span><span id="ec_endofline_crlf"></span><dl> <span data-ttu-id="8c2db-114"><dt>**\_ENDOFLINE ce \_ CRLF**</dt></span><span class="sxs-lookup"><span data-stu-id="8c2db-114"><dt>**EC\_ENDOFLINE\_CRLF**</dt></span></span> </dl>                                        | <span data-ttu-id="8c2db-115">Définit le caractère de fin de ligne utilisé pour le nouveau sauts sur le retour chariot suivi du saut de ligne (CRLF).</span><span class="sxs-lookup"><span data-stu-id="8c2db-115">Sets the end-of-line character used for new linebreaks to carriage return followed by linefeed (CRLF).</span></span><br/> |
| <span id="EC_ENDOFLINE_CR"></span><span id="ec_endofline_cr"></span><dl> <span data-ttu-id="8c2db-116"><dt>**\_ENDOFLINE ce \_ CR**</dt></span><span class="sxs-lookup"><span data-stu-id="8c2db-116"><dt>**EC\_ENDOFLINE\_CR**</dt></span></span> </dl>                                              | <span data-ttu-id="8c2db-117">Définit le caractère de fin de ligne utilisé pour le nouveau sauts sur le retour chariot (CR).</span><span class="sxs-lookup"><span data-stu-id="8c2db-117">Sets the end-of-line character used for new linebreaks to carriage return (CR).</span></span><br/>                        |
| <span id="EC_ENDOFLINE_LF"></span><span id="ec_endofline_lf"></span><dl> <span data-ttu-id="8c2db-118"><dt>**EC \_ ENDOFLINE \_ LF**</dt></span><span class="sxs-lookup"><span data-stu-id="8c2db-118"><dt>**EC\_ENDOFLINE\_LF**</dt></span></span> </dl>                                              | <span data-ttu-id="8c2db-119">Définit le caractère de fin de ligne utilisé pour le nouveau sauts de saut de ligne (LF).</span><span class="sxs-lookup"><span data-stu-id="8c2db-119">Sets the end-of-line character used for new linebreaks to linefeed (LF).</span></span><br/>                               |

</dd> <dt>

<span data-ttu-id="8c2db-120">*lParam*</span><span class="sxs-lookup"><span data-stu-id="8c2db-120">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="8c2db-121">Ce paramètre n'est pas utilisé.</span><span class="sxs-lookup"><span data-stu-id="8c2db-121">This parameter is not used.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8c2db-122">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="8c2db-122">Return value</span></span>

<span data-ttu-id="8c2db-123">Si l’opération a échoué, la valeur de retour est différente de zéro.</span><span class="sxs-lookup"><span data-stu-id="8c2db-123">If the operation succeeds, the return value is nonzero.</span></span>

<span data-ttu-id="8c2db-124">Si l’opération échoue, la valeur de retour est zéro.</span><span class="sxs-lookup"><span data-stu-id="8c2db-124">If the operation fails, the return value is zero.</span></span>

## <a name="remarks"></a><span data-ttu-id="8c2db-125">Notes</span><span class="sxs-lookup"><span data-stu-id="8c2db-125">Remarks</span></span>

<span data-ttu-id="8c2db-126">Lorsque le jeu de caractères de fin de ligne est **EC \_ ENDOFLINE \_ DETECTFROMCONTENT**, le contrôle d’édition détecte uniquement les caractères de fin de ligne pris en charge en fonction de son style de fenêtre étendu. consultez [modifier les styles étendus de contrôle](edit-control-window-extended-styles.md).</span><span class="sxs-lookup"><span data-stu-id="8c2db-126">When the end-of-line character set is **EC\_ENDOFLINE\_DETECTFROMCONTENT**, the edit control will only detect end-of-line characters supported according to its extended window style, see [Edit Control Extended Styles](edit-control-window-extended-styles.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="8c2db-127">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="8c2db-127">Requirements</span></span>



| <span data-ttu-id="8c2db-128">Condition requise</span><span class="sxs-lookup"><span data-stu-id="8c2db-128">Requirement</span></span> | <span data-ttu-id="8c2db-129">Valeur</span><span class="sxs-lookup"><span data-stu-id="8c2db-129">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8c2db-130">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="8c2db-130">Minimum supported client</span></span><br/> | <span data-ttu-id="8c2db-131">Applications de bureau Windows 10, 1809 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="8c2db-131">Windows 10, 1809 \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="8c2db-132">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="8c2db-132">Minimum supported server</span></span><br/> | <span data-ttu-id="8c2db-133">Applications de bureau Windows Server 2019 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="8c2db-133">Windows Server 2019 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="8c2db-134">En-tête</span><span class="sxs-lookup"><span data-stu-id="8c2db-134">Header</span></span><br/>                   | <dl> <span data-ttu-id="8c2db-135"><dt>CommCtrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="8c2db-135"><dt>CommCtrl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8c2db-136">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="8c2db-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8c2db-137">\**\_GETENDOFLINE em*</span><span class="sxs-lookup"><span data-stu-id="8c2db-137">\**EM\_GETENDOFLINE*</span></span>](em-getendofline.md)
</dt> </dl>

 

 





