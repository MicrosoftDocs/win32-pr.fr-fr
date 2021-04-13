---
title: Message CB_SETLOCALE (winuser. h)
description: Une application envoie un \_ message CB SETLOCALE pour définir les paramètres régionaux actuels de la zone de liste déroulante. Si la zone de liste déroulante a le \_ style de tri CBS et que des chaînes sont ajoutées à l’aide \_ de CB ADDSTRING, les paramètres régionaux d’une zone de liste déroulante affectent le mode de tri des éléments de liste.
ms.assetid: 06f9c69d-1220-490f-bc67-6e125f696e87
keywords:
- CB_SETLOCALE les contrôles de message Windows
topic_type:
- apiref
api_name:
- CB_SETLOCALE
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 025f33dc8ba236965a98ca984446b04846ecd2ba
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104465930"
---
# <a name="cb_setlocale-message"></a><span data-ttu-id="f50f3-105">\_Message CB SETLOCALE</span><span class="sxs-lookup"><span data-stu-id="f50f3-105">CB\_SETLOCALE message</span></span>

<span data-ttu-id="f50f3-106">Une application envoie un message **CB \_ SETLOCALE** pour définir les paramètres régionaux actuels de la zone de liste déroulante.</span><span class="sxs-lookup"><span data-stu-id="f50f3-106">An application sends a **CB\_SETLOCALE** message to set the current locale of the combo box.</span></span> <span data-ttu-id="f50f3-107">Si la zone de liste déroulante a le style de [**\_ Tri CBS**](combo-box-styles.md) et que des chaînes sont ajoutées à l’aide de [**CB \_ ADDSTRING**](cb-addstring.md), les paramètres régionaux d’une zone de liste déroulante affectent le mode de tri des éléments de liste.</span><span class="sxs-lookup"><span data-stu-id="f50f3-107">If the combo box has the [**CBS\_SORT**](combo-box-styles.md) style and strings are added using [**CB\_ADDSTRING**](cb-addstring.md), the locale of a combo box affects how list items are sorted.</span></span>

## <a name="parameters"></a><span data-ttu-id="f50f3-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="f50f3-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f50f3-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="f50f3-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="f50f3-110">Spécifie l’identificateur de paramètres régionaux pour la zone de liste déroulante à utiliser pour le tri lors de l’ajout de texte.</span><span class="sxs-lookup"><span data-stu-id="f50f3-110">Specifies the locale identifier for the combo box to use for sorting when adding text.</span></span>

</dd> <dt>

<span data-ttu-id="f50f3-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="f50f3-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="f50f3-112">Ce paramètre n'est pas utilisé.</span><span class="sxs-lookup"><span data-stu-id="f50f3-112">This parameter is not used.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f50f3-113">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="f50f3-113">Return value</span></span>

<span data-ttu-id="f50f3-114">La valeur de retour est l’identificateur de paramètres régionaux précédent.</span><span class="sxs-lookup"><span data-stu-id="f50f3-114">The return value is the previous locale identifier.</span></span> <span data-ttu-id="f50f3-115">Si *wParam* spécifie des paramètres régionaux qui ne sont pas installés sur le système, la valeur de retour est CB \_ Err et les paramètres régionaux actuels de la zone de liste déroulante ne sont pas modifiés.</span><span class="sxs-lookup"><span data-stu-id="f50f3-115">If *wParam* specifies a locale not installed on the system, the return value is CB\_ERR and the current combo box locale is not changed.</span></span>

## <a name="remarks"></a><span data-ttu-id="f50f3-116">Notes</span><span class="sxs-lookup"><span data-stu-id="f50f3-116">Remarks</span></span>

<span data-ttu-id="f50f3-117">Utilisez la macro [**MAKELCID**](/windows/desktop/api/winnt/nf-winnt-makelcid) pour construire un identificateur de paramètres régionaux et la macro [**MAKELANGID**](/windows/desktop/api/winnt/nf-winnt-makelangid) pour construire un identificateur de langue.</span><span class="sxs-lookup"><span data-stu-id="f50f3-117">Use the [**MAKELCID**](/windows/desktop/api/winnt/nf-winnt-makelcid) macro to construct a locale identifier and the [**MAKELANGID**](/windows/desktop/api/winnt/nf-winnt-makelangid) macro to construct a language identifier.</span></span> <span data-ttu-id="f50f3-118">L’identificateur de langue est constitué d’un identificateur de langue primaire et d’un identificateur de sous-langue.</span><span class="sxs-lookup"><span data-stu-id="f50f3-118">The language identifier is made up of a primary language identifier and a sublanguage identifier.</span></span>

## <a name="requirements"></a><span data-ttu-id="f50f3-119">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="f50f3-119">Requirements</span></span>



| <span data-ttu-id="f50f3-120">Condition requise</span><span class="sxs-lookup"><span data-stu-id="f50f3-120">Requirement</span></span> | <span data-ttu-id="f50f3-121">Valeur</span><span class="sxs-lookup"><span data-stu-id="f50f3-121">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f50f3-122">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="f50f3-122">Minimum supported client</span></span><br/> | <span data-ttu-id="f50f3-123">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="f50f3-123">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="f50f3-124">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="f50f3-124">Minimum supported server</span></span><br/> | <span data-ttu-id="f50f3-125">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="f50f3-125">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="f50f3-126">En-tête</span><span class="sxs-lookup"><span data-stu-id="f50f3-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="f50f3-127"><dt>Winuser. h (inclure Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="f50f3-127"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f50f3-128">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="f50f3-128">See also</span></span>

<dl> <dt>

<span data-ttu-id="f50f3-129">**Référence**</span><span class="sxs-lookup"><span data-stu-id="f50f3-129">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="f50f3-130">**$ \_ ADDSTRING**</span><span class="sxs-lookup"><span data-stu-id="f50f3-130">**CB\_ADDSTRING**</span></span>](cb-addstring.md)
</dt> <dt>

[<span data-ttu-id="f50f3-131">**\_GETLOCALE CB**</span><span class="sxs-lookup"><span data-stu-id="f50f3-131">**CB\_GETLOCALE**</span></span>](cb-getlocale.md)
</dt> <dt>

<span data-ttu-id="f50f3-132">**Autres ressources**</span><span class="sxs-lookup"><span data-stu-id="f50f3-132">**Other Resources**</span></span>
</dt> <dt>

[<span data-ttu-id="f50f3-133">**MAKELANGID**</span><span class="sxs-lookup"><span data-stu-id="f50f3-133">**MAKELANGID**</span></span>](/windows/desktop/api/winnt/nf-winnt-makelangid)
</dt> <dt>

[<span data-ttu-id="f50f3-134">**MAKELCID**</span><span class="sxs-lookup"><span data-stu-id="f50f3-134">**MAKELCID**</span></span>](/windows/desktop/api/winnt/nf-winnt-makelcid)
</dt> </dl>

 

