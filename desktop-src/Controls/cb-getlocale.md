---
title: Message CB_GETLOCALE (winuser. h)
description: Obtient les paramètres régionaux actuels de la zone de liste déroulante. Les paramètres régionaux sont utilisés pour déterminer l’ordre de tri correct du texte affiché pour les zones de liste déroulante avec le \_ style de tri CBS et le texte ajouté à l’aide du \_ message CB ADDSTRING.
ms.assetid: 57c77ce2-bad0-43f3-8325-f2a7227994ec
keywords:
- CB_GETLOCALE les contrôles de message Windows
topic_type:
- apiref
api_name:
- CB_GETLOCALE
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 847d9f73e8bf0b1d533d0b79ba86d939bee0e9b4
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104032851"
---
# <a name="cb_getlocale-message"></a><span data-ttu-id="a547e-105">\_Message GETLOCALE CB</span><span class="sxs-lookup"><span data-stu-id="a547e-105">CB\_GETLOCALE message</span></span>

<span data-ttu-id="a547e-106">Obtient les paramètres régionaux actuels de la zone de liste déroulante.</span><span class="sxs-lookup"><span data-stu-id="a547e-106">Gets the current locale of the combo box.</span></span> <span data-ttu-id="a547e-107">Les paramètres régionaux sont utilisés pour déterminer l’ordre de tri correct du texte affiché pour les zones de liste déroulante avec le style de [**\_ Tri CBS**](combo-box-styles.md) et le texte ajouté à l’aide du message [**CB \_ ADDSTRING**](cb-addstring.md) .</span><span class="sxs-lookup"><span data-stu-id="a547e-107">The locale is used to determine the correct sorting order of displayed text for combo boxes with the [**CBS\_SORT**](combo-box-styles.md) style and text added by using the [**CB\_ADDSTRING**](cb-addstring.md) message.</span></span>

## <a name="parameters"></a><span data-ttu-id="a547e-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="a547e-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a547e-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="a547e-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="a547e-110">Non utilisé ; doit être égal à zéro.</span><span class="sxs-lookup"><span data-stu-id="a547e-110">Not used; must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="a547e-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="a547e-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="a547e-112">Non utilisé ; doit être égal à zéro.</span><span class="sxs-lookup"><span data-stu-id="a547e-112">Not used; must be zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a547e-113">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="a547e-113">Return value</span></span>

<span data-ttu-id="a547e-114">La valeur de retour spécifie les paramètres régionaux actuels de la zone de liste déroulante.</span><span class="sxs-lookup"><span data-stu-id="a547e-114">The return value specifies the current locale of the combo box.</span></span> <span data-ttu-id="a547e-115">Le [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) contient le code de pays/région et le [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) contient l’identificateur de langue.</span><span class="sxs-lookup"><span data-stu-id="a547e-115">The [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) contains the country/region code and the [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) contains the language identifier.</span></span>

## <a name="remarks"></a><span data-ttu-id="a547e-116">Notes</span><span class="sxs-lookup"><span data-stu-id="a547e-116">Remarks</span></span>

<span data-ttu-id="a547e-117">L’identificateur de langue est constitué d’un identificateur de sous-langue et d’un identificateur de langue primaire.</span><span class="sxs-lookup"><span data-stu-id="a547e-117">The language identifier is made up of a sublanguage identifier and a primary language identifier.</span></span> <span data-ttu-id="a547e-118">La macro [**PRIMARYLANGID**](/windows/desktop/api/winnt/nf-winnt-primarylangid) obtient l’identificateur de langue principal et la macro [**SUBLANGID**](/windows/desktop/api/winnt/nf-winnt-sublangid) obtient l’identificateur de sous-langue.</span><span class="sxs-lookup"><span data-stu-id="a547e-118">The [**PRIMARYLANGID**](/windows/desktop/api/winnt/nf-winnt-primarylangid) macro obtains the primary language identifier and the [**SUBLANGID**](/windows/desktop/api/winnt/nf-winnt-sublangid) macro obtains the sublanguage identifier.</span></span>

## <a name="requirements"></a><span data-ttu-id="a547e-119">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="a547e-119">Requirements</span></span>



| <span data-ttu-id="a547e-120">Condition requise</span><span class="sxs-lookup"><span data-stu-id="a547e-120">Requirement</span></span> | <span data-ttu-id="a547e-121">Valeur</span><span class="sxs-lookup"><span data-stu-id="a547e-121">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a547e-122">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="a547e-122">Minimum supported client</span></span><br/> | <span data-ttu-id="a547e-123">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="a547e-123">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="a547e-124">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="a547e-124">Minimum supported server</span></span><br/> | <span data-ttu-id="a547e-125">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="a547e-125">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="a547e-126">En-tête</span><span class="sxs-lookup"><span data-stu-id="a547e-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="a547e-127"><dt>Winuser. h (inclure Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="a547e-127"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a547e-128">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="a547e-128">See also</span></span>

<dl> <dt>

<span data-ttu-id="a547e-129">**Référence**</span><span class="sxs-lookup"><span data-stu-id="a547e-129">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="a547e-130">**$ \_ ADDSTRING**</span><span class="sxs-lookup"><span data-stu-id="a547e-130">**CB\_ADDSTRING**</span></span>](cb-addstring.md)
</dt> <dt>

[<span data-ttu-id="a547e-131">**CB \_ SETLOCALE**</span><span class="sxs-lookup"><span data-stu-id="a547e-131">**CB\_SETLOCALE**</span></span>](cb-setlocale.md)
</dt> <dt>

<span data-ttu-id="a547e-132">**Autres ressources**</span><span class="sxs-lookup"><span data-stu-id="a547e-132">**Other Resources**</span></span>
</dt> <dt>

<span data-ttu-id="a547e-133">[**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="a547e-133">[**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85))</span></span>
</dt> <dt>

<span data-ttu-id="a547e-134">[**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="a547e-134">[**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85))</span></span>
</dt> <dt>

[<span data-ttu-id="a547e-135">**PRIMARYLANGID**</span><span class="sxs-lookup"><span data-stu-id="a547e-135">**PRIMARYLANGID**</span></span>](/windows/desktop/api/winnt/nf-winnt-primarylangid)
</dt> <dt>

[<span data-ttu-id="a547e-136">**SUBLANGID**</span><span class="sxs-lookup"><span data-stu-id="a547e-136">**SUBLANGID**</span></span>](/windows/desktop/api/winnt/nf-winnt-sublangid)
</dt> </dl>

 

