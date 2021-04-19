---
title: Message TB_SETBUTTONSIZE (commctrl. h)
description: Définit la taille des boutons sur une barre d’outils.
ms.assetid: ef6beed7-a3d6-4379-b9c1-c64a5e33ce78
keywords:
- TB_SETBUTTONSIZE les contrôles de message Windows
topic_type:
- apiref
api_name:
- TB_SETBUTTONSIZE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5db17b943c8a7cc8e71735d08718ece02a8c2582
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "106509105"
---
# <a name="tb_setbuttonsize-message"></a><span data-ttu-id="219c8-104">TO \_ SETBUTTONSIZE message</span><span class="sxs-lookup"><span data-stu-id="219c8-104">TB\_SETBUTTONSIZE message</span></span>

<span data-ttu-id="219c8-105">Définit la taille des boutons sur une barre d’outils.</span><span class="sxs-lookup"><span data-stu-id="219c8-105">Sets the size of buttons on a toolbar.</span></span>

## <a name="parameters"></a><span data-ttu-id="219c8-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="219c8-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="219c8-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="219c8-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="219c8-108">Doit être zéro.</span><span class="sxs-lookup"><span data-stu-id="219c8-108">Must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="219c8-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="219c8-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="219c8-110">Le [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) spécifie la largeur, en pixels, des boutons.</span><span class="sxs-lookup"><span data-stu-id="219c8-110">The [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) specifies the width, in pixels, of the buttons.</span></span> <span data-ttu-id="219c8-111">Le [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) spécifie la hauteur, en pixels, des boutons.</span><span class="sxs-lookup"><span data-stu-id="219c8-111">The [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) specifies the height, in pixels, of the buttons.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="219c8-112">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="219c8-112">Return value</span></span>

<span data-ttu-id="219c8-113">Retourne la **valeur true** en cas de réussite, ou **false** dans le cas contraire.</span><span class="sxs-lookup"><span data-stu-id="219c8-113">Returns **TRUE** if successful, or **FALSE** otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="219c8-114">Notes</span><span class="sxs-lookup"><span data-stu-id="219c8-114">Remarks</span></span>

<span data-ttu-id="219c8-115">**To \_ SETBUTTONSIZE** doit généralement être appelé après l’ajout de boutons.</span><span class="sxs-lookup"><span data-stu-id="219c8-115">**TB\_SETBUTTONSIZE** should generally be called after adding buttons.</span></span>

<span data-ttu-id="219c8-116">Utilisez [**to \_ SETBUTTONWIDTH**](tb-setbuttonwidth.md) pour définir les largeurs maximales et minimales autorisées pour les boutons avant leur ajout.</span><span class="sxs-lookup"><span data-stu-id="219c8-116">Use [**TB\_SETBUTTONWIDTH**](tb-setbuttonwidth.md) to set the maximum and minimum allowed widths for buttons before they are added.</span></span> <span data-ttu-id="219c8-117">Utilisez **to \_ SETBUTTONSIZE** pour définir la taille réelle des boutons.</span><span class="sxs-lookup"><span data-stu-id="219c8-117">Use **TB\_SETBUTTONSIZE** to set the actual size of buttons.</span></span>

## <a name="examples"></a><span data-ttu-id="219c8-118">Exemples</span><span class="sxs-lookup"><span data-stu-id="219c8-118">Examples</span></span>

<span data-ttu-id="219c8-119">L’exemple de code suivant définit la largeur des boutons sur 80 pixels et la hauteur sur 30 pixels.</span><span class="sxs-lookup"><span data-stu-id="219c8-119">The following example code sets the width of buttons to 80 pixels and the height to 30 pixels.</span></span>


```C++
// hWndToolbar is a handle to the toolbar window.
SendMessage(hWndToolbar, TB_SETBUTTONSIZE, 0, MAKELPARAM(80, 30);
```



## <a name="requirements"></a><span data-ttu-id="219c8-120">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="219c8-120">Requirements</span></span>



| <span data-ttu-id="219c8-121">Condition requise</span><span class="sxs-lookup"><span data-stu-id="219c8-121">Requirement</span></span> | <span data-ttu-id="219c8-122">Valeur</span><span class="sxs-lookup"><span data-stu-id="219c8-122">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="219c8-123">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="219c8-123">Minimum supported client</span></span><br/> | <span data-ttu-id="219c8-124">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="219c8-124">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="219c8-125">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="219c8-125">Minimum supported server</span></span><br/> | <span data-ttu-id="219c8-126">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="219c8-126">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="219c8-127">En-tête</span><span class="sxs-lookup"><span data-stu-id="219c8-127">Header</span></span><br/>                   | <dl> <span data-ttu-id="219c8-128"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="219c8-128"><dt>Commctrl.h</dt></span></span> </dl> |



 

