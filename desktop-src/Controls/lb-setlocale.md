---
title: Message LB_SETLOCALE (winuser. h)
description: Définit les paramètres régionaux actuels de la zone de liste. Vous pouvez utiliser les paramètres régionaux pour déterminer l’ordre de tri correct du texte affiché (pour les zones de liste avec le \_ style de tri lbs) et du texte ajouté par le \_ message lb ADDSTRING.
ms.assetid: e9503124-de9f-4b92-a59e-ec9320864ae7
keywords:
- LB_SETLOCALE les contrôles de message Windows
topic_type:
- apiref
api_name:
- LB_SETLOCALE
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cd8ea7bb7b6d19144a84ab166f56cd2c0ad49e05
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104033144"
---
# <a name="lb_setlocale-message"></a><span data-ttu-id="57b69-105">LB \_ SETLOCALE message</span><span class="sxs-lookup"><span data-stu-id="57b69-105">LB\_SETLOCALE message</span></span>

<span data-ttu-id="57b69-106">Définit les paramètres régionaux actuels de la zone de liste.</span><span class="sxs-lookup"><span data-stu-id="57b69-106">Sets the current locale of the list box.</span></span> <span data-ttu-id="57b69-107">Vous pouvez utiliser les paramètres régionaux pour déterminer l’ordre de tri correct du texte affiché (pour les zones de liste avec le style de [**\_ Tri lbs**](list-box-styles.md) ) et du texte ajouté par le message [**lb \_ ADDSTRING**](lb-addstring.md) .</span><span class="sxs-lookup"><span data-stu-id="57b69-107">You can use the locale to determine the correct sorting order of displayed text (for list boxes with the [**LBS\_SORT**](list-box-styles.md) style) and of text added by the [**LB\_ADDSTRING**](lb-addstring.md) message.</span></span>

## <a name="parameters"></a><span data-ttu-id="57b69-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="57b69-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="57b69-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="57b69-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="57b69-110">Spécifie l’identificateur de paramètres régionaux qui sera utilisé par la zone de liste pour le tri lors de l’ajout de texte.</span><span class="sxs-lookup"><span data-stu-id="57b69-110">Specifies the locale identifier that the list box will use for sorting when adding text.</span></span>

</dd> <dt>

<span data-ttu-id="57b69-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="57b69-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="57b69-112">Ce paramètre n'est pas utilisé.</span><span class="sxs-lookup"><span data-stu-id="57b69-112">This parameter is not used.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="57b69-113">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="57b69-113">Return value</span></span>

<span data-ttu-id="57b69-114">La valeur de retour est l’identificateur de paramètres régionaux précédent.</span><span class="sxs-lookup"><span data-stu-id="57b69-114">The return value is the previous locale identifier.</span></span> <span data-ttu-id="57b69-115">Si le paramètre *wParam* spécifie des paramètres régionaux qui ne sont pas installés sur le système, la valeur de retour est lb \_ Err et les paramètres régionaux de la zone de liste active ne sont pas modifiés.</span><span class="sxs-lookup"><span data-stu-id="57b69-115">If the *wParam* parameter specifies a locale that is not installed on the system, the return value is LB\_ERR and the current list box locale is not changed.</span></span>

## <a name="remarks"></a><span data-ttu-id="57b69-116">Notes</span><span class="sxs-lookup"><span data-stu-id="57b69-116">Remarks</span></span>

<span data-ttu-id="57b69-117">Utilisez la macro [**MAKELCID**](/windows/desktop/api/winnt/nf-winnt-makelcid) pour construire un identificateur de paramètres régionaux.</span><span class="sxs-lookup"><span data-stu-id="57b69-117">Use the [**MAKELCID**](/windows/desktop/api/winnt/nf-winnt-makelcid) macro to construct a locale identifier.</span></span>

## <a name="requirements"></a><span data-ttu-id="57b69-118">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="57b69-118">Requirements</span></span>



| <span data-ttu-id="57b69-119">Condition requise</span><span class="sxs-lookup"><span data-stu-id="57b69-119">Requirement</span></span> | <span data-ttu-id="57b69-120">Valeur</span><span class="sxs-lookup"><span data-stu-id="57b69-120">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="57b69-121">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="57b69-121">Minimum supported client</span></span><br/> | <span data-ttu-id="57b69-122">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="57b69-122">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="57b69-123">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="57b69-123">Minimum supported server</span></span><br/> | <span data-ttu-id="57b69-124">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="57b69-124">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="57b69-125">En-tête</span><span class="sxs-lookup"><span data-stu-id="57b69-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="57b69-126"><dt>Winuser. h (inclure Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="57b69-126"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="57b69-127">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="57b69-127">See also</span></span>

<dl> <dt>

<span data-ttu-id="57b69-128">**Référence**</span><span class="sxs-lookup"><span data-stu-id="57b69-128">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="57b69-129">**LB \_ ADDSTRING**</span><span class="sxs-lookup"><span data-stu-id="57b69-129">**LB\_ADDSTRING**</span></span>](lb-addstring.md)
</dt> <dt>

[<span data-ttu-id="57b69-130">**\_GETLOCALE lb**</span><span class="sxs-lookup"><span data-stu-id="57b69-130">**LB\_GETLOCALE**</span></span>](lb-getlocale.md)
</dt> </dl>

 

