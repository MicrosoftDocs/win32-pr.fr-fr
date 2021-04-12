---
title: Message LB_GETLOCALE (winuser. h)
description: Obtient les paramètres régionaux actuels de la zone de liste. Vous pouvez utiliser les paramètres régionaux pour déterminer l’ordre de tri correct du texte affiché (pour les zones de liste avec le \_ style de tri lbs) et du texte ajouté par le \_ message lb ADDSTRING.
ms.assetid: ec814b03-5ce2-4b81-a36c-ab4c115f88be
keywords:
- LB_GETLOCALE les contrôles de message Windows
topic_type:
- apiref
api_name:
- LB_GETLOCALE
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 57620b62011dba234710caf1b5d1c429da37ace9
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104465690"
---
# <a name="lb_getlocale-message"></a><span data-ttu-id="e9063-105">\_Message GETLOCALE lb</span><span class="sxs-lookup"><span data-stu-id="e9063-105">LB\_GETLOCALE message</span></span>

<span data-ttu-id="e9063-106">Obtient les paramètres régionaux actuels de la zone de liste.</span><span class="sxs-lookup"><span data-stu-id="e9063-106">Gets the current locale of the list box.</span></span> <span data-ttu-id="e9063-107">Vous pouvez utiliser les paramètres régionaux pour déterminer l’ordre de tri correct du texte affiché (pour les zones de liste avec le style de [**\_ Tri lbs**](list-box-styles.md) ) et du texte ajouté par le message [**lb \_ ADDSTRING**](lb-addstring.md) .</span><span class="sxs-lookup"><span data-stu-id="e9063-107">You can use the locale to determine the correct sorting order of displayed text (for list boxes with the [**LBS\_SORT**](list-box-styles.md) style) and of text added by the [**LB\_ADDSTRING**](lb-addstring.md) message.</span></span>

## <a name="parameters"></a><span data-ttu-id="e9063-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="e9063-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e9063-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="e9063-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="e9063-110">Non utilisé ; doit être égal à zéro.</span><span class="sxs-lookup"><span data-stu-id="e9063-110">Not used; must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="e9063-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="e9063-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="e9063-112">Non utilisé ; doit être égal à zéro.</span><span class="sxs-lookup"><span data-stu-id="e9063-112">Not used; must be zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e9063-113">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="e9063-113">Return value</span></span>

<span data-ttu-id="e9063-114">La valeur de retour spécifie les paramètres régionaux actuels de la zone de liste.</span><span class="sxs-lookup"><span data-stu-id="e9063-114">The return value specifies the current locale of the list box.</span></span> <span data-ttu-id="e9063-115">Le [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) contient le code de pays/région et le [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) contient l’identificateur de langue.</span><span class="sxs-lookup"><span data-stu-id="e9063-115">The [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) contains the country/region code and the [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) contains the language identifier.</span></span>

## <a name="remarks"></a><span data-ttu-id="e9063-116">Notes</span><span class="sxs-lookup"><span data-stu-id="e9063-116">Remarks</span></span>

<span data-ttu-id="e9063-117">L’identificateur de langue se compose d’un identificateur de sous-langue et d’un identificateur de langue primaire.</span><span class="sxs-lookup"><span data-stu-id="e9063-117">The language identifier consists of a sublanguage identifier and a primary language identifier.</span></span> <span data-ttu-id="e9063-118">Utilisez la macro [**PRIMARYLANGID**](/windows/desktop/api/winnt/nf-winnt-primarylangid) pour extraire l’identificateur de langue primaire de la [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) de la valeur de retour, et la macro [**SUBLANGID**](/windows/desktop/api/winnt/nf-winnt-sublangid) pour extraire l’identificateur de sous-langue.</span><span class="sxs-lookup"><span data-stu-id="e9063-118">Use the [**PRIMARYLANGID**](/windows/desktop/api/winnt/nf-winnt-primarylangid) macro to extract the primary language identifier from the [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) of the return value, and the [**SUBLANGID**](/windows/desktop/api/winnt/nf-winnt-sublangid) macro to extract the sublanguage identifier.</span></span>

## <a name="requirements"></a><span data-ttu-id="e9063-119">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="e9063-119">Requirements</span></span>



| <span data-ttu-id="e9063-120">Condition requise</span><span class="sxs-lookup"><span data-stu-id="e9063-120">Requirement</span></span> | <span data-ttu-id="e9063-121">Valeur</span><span class="sxs-lookup"><span data-stu-id="e9063-121">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e9063-122">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="e9063-122">Minimum supported client</span></span><br/> | <span data-ttu-id="e9063-123">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="e9063-123">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="e9063-124">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="e9063-124">Minimum supported server</span></span><br/> | <span data-ttu-id="e9063-125">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="e9063-125">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="e9063-126">En-tête</span><span class="sxs-lookup"><span data-stu-id="e9063-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="e9063-127"><dt>Winuser. h (inclure Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="e9063-127"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e9063-128">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="e9063-128">See also</span></span>

<dl> <dt>

<span data-ttu-id="e9063-129">**Référence**</span><span class="sxs-lookup"><span data-stu-id="e9063-129">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="e9063-130">**LB \_ ADDSTRING**</span><span class="sxs-lookup"><span data-stu-id="e9063-130">**LB\_ADDSTRING**</span></span>](lb-addstring.md)
</dt> <dt>

[<span data-ttu-id="e9063-131">**LB \_ SETLOCALE**</span><span class="sxs-lookup"><span data-stu-id="e9063-131">**LB\_SETLOCALE**</span></span>](lb-setlocale.md)
</dt> <dt>

<span data-ttu-id="e9063-132">**Autres ressources**</span><span class="sxs-lookup"><span data-stu-id="e9063-132">**Other Resources**</span></span>
</dt> <dt>

[<span data-ttu-id="e9063-133">**PRIMARYLANGID**</span><span class="sxs-lookup"><span data-stu-id="e9063-133">**PRIMARYLANGID**</span></span>](/windows/desktop/api/winnt/nf-winnt-primarylangid)
</dt> <dt>

[<span data-ttu-id="e9063-134">**SUBLANGID**</span><span class="sxs-lookup"><span data-stu-id="e9063-134">**SUBLANGID**</span></span>](/windows/desktop/api/winnt/nf-winnt-sublangid)
</dt> </dl>

 

