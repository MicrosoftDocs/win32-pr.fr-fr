---
description: Récupère la police avec laquelle le contrôle dessine actuellement son texte.
ms.assetid: a6d05ef5-9933-4d03-a677-a8328bf1cb7d
title: Message WM_GETFONT (winuser. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5254b701630f09cc7980470a9f5be68ad377bc03
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106519412"
---
# <a name="wm_getfont-message"></a><span data-ttu-id="1dfe8-103">\_Message WM GETFONT</span><span class="sxs-lookup"><span data-stu-id="1dfe8-103">WM\_GETFONT message</span></span>

<span data-ttu-id="1dfe8-104">Récupère la police avec laquelle le contrôle dessine actuellement son texte.</span><span class="sxs-lookup"><span data-stu-id="1dfe8-104">Retrieves the font with which the control is currently drawing its text.</span></span>


```C++
#define WM_GETFONT                      0x0031
```



## <a name="parameters"></a><span data-ttu-id="1dfe8-105">Paramètres</span><span class="sxs-lookup"><span data-stu-id="1dfe8-105">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1dfe8-106">*wParam*</span><span class="sxs-lookup"><span data-stu-id="1dfe8-106">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="1dfe8-107">Ce paramètre n’est pas utilisé et doit être égal à zéro.</span><span class="sxs-lookup"><span data-stu-id="1dfe8-107">This parameter is not used and must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="1dfe8-108">*lParam*</span><span class="sxs-lookup"><span data-stu-id="1dfe8-108">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="1dfe8-109">Ce paramètre n’est pas utilisé et doit être égal à zéro.</span><span class="sxs-lookup"><span data-stu-id="1dfe8-109">This parameter is not used and must be zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1dfe8-110">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="1dfe8-110">Return value</span></span>

<span data-ttu-id="1dfe8-111">Tapez : **Hfont**</span><span class="sxs-lookup"><span data-stu-id="1dfe8-111">Type: **HFONT**</span></span>

<span data-ttu-id="1dfe8-112">La valeur de retour est un handle de la police utilisée par le contrôle, ou **null** si le contrôle utilise la police système.</span><span class="sxs-lookup"><span data-stu-id="1dfe8-112">The return value is a handle to the font used by the control, or **NULL** if the control is using the system font.</span></span>

## <a name="requirements"></a><span data-ttu-id="1dfe8-113">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="1dfe8-113">Requirements</span></span>



| <span data-ttu-id="1dfe8-114">Condition requise</span><span class="sxs-lookup"><span data-stu-id="1dfe8-114">Requirement</span></span> | <span data-ttu-id="1dfe8-115">Valeur</span><span class="sxs-lookup"><span data-stu-id="1dfe8-115">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="1dfe8-116">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="1dfe8-116">Minimum supported client</span></span><br/> | <span data-ttu-id="1dfe8-117">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="1dfe8-117">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="1dfe8-118">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="1dfe8-118">Minimum supported server</span></span><br/> | <span data-ttu-id="1dfe8-119">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="1dfe8-119">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="1dfe8-120">En-tête</span><span class="sxs-lookup"><span data-stu-id="1dfe8-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="1dfe8-121"><dt>Winuser. h (inclure Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="1dfe8-121"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1dfe8-122">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="1dfe8-122">See also</span></span>

<dl> <dt>

<span data-ttu-id="1dfe8-123">**Référence**</span><span class="sxs-lookup"><span data-stu-id="1dfe8-123">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="1dfe8-124">**\_SetFont WM**</span><span class="sxs-lookup"><span data-stu-id="1dfe8-124">**WM\_SETFONT**</span></span>](wm-setfont.md)
</dt> <dt>

<span data-ttu-id="1dfe8-125">**Méthodologique**</span><span class="sxs-lookup"><span data-stu-id="1dfe8-125">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="1dfe8-126">Windows</span><span class="sxs-lookup"><span data-stu-id="1dfe8-126">Windows</span></span>](windows.md)
</dt> </dl>

 

 




