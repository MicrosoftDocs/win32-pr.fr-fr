---
title: Message EM_GETTEXTRANGE (RichEdit. h)
description: Récupère une plage de caractères spécifiée à partir d’un contrôle RichEdit.
ms.assetid: 18398963-eb2c-4f64-99f5-9614a5d34b52
keywords:
- EM_GETTEXTRANGE les contrôles de message Windows
topic_type:
- apiref
api_name:
- EM_GETTEXTRANGE
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d68c4089bbe2cc09daa39d69e9094a4abaead787
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103942561"
---
# <a name="em_gettextrange-message"></a><span data-ttu-id="a0279-104">\_Message GETTEXTRANGE em</span><span class="sxs-lookup"><span data-stu-id="a0279-104">EM\_GETTEXTRANGE message</span></span>

<span data-ttu-id="a0279-105">Récupère une plage de caractères spécifiée à partir d’un contrôle RichEdit.</span><span class="sxs-lookup"><span data-stu-id="a0279-105">Retrieves a specified range of characters from a rich edit control.</span></span>

## <a name="parameters"></a><span data-ttu-id="a0279-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="a0279-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a0279-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="a0279-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="a0279-108">Ce paramètre n’est pas utilisé ; elle doit être égale à zéro.</span><span class="sxs-lookup"><span data-stu-id="a0279-108">This parameter is not used; it must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="a0279-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="a0279-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="a0279-110">Pointeur vers une structure [**TEXTRANGE**](/windows/win32/api/richedit/ns-richedit-textrangea) qui spécifie la plage de caractères à récupérer et une mémoire tampon dans laquelle copier les caractères.</span><span class="sxs-lookup"><span data-stu-id="a0279-110">Pointer to a [**TEXTRANGE**](/windows/win32/api/richedit/ns-richedit-textrangea) structure that specifies the range of characters to retrieve and a buffer to copy the characters to.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a0279-111">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="a0279-111">Return value</span></span>

<span data-ttu-id="a0279-112">Le message retourne le nombre de caractères copiés, à l’exclusion du caractère null de fin.</span><span class="sxs-lookup"><span data-stu-id="a0279-112">The message returns the number of characters copied, not including the terminating null character.</span></span>

## <a name="requirements"></a><span data-ttu-id="a0279-113">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="a0279-113">Requirements</span></span>



| <span data-ttu-id="a0279-114">Condition requise</span><span class="sxs-lookup"><span data-stu-id="a0279-114">Requirement</span></span> | <span data-ttu-id="a0279-115">Valeur</span><span class="sxs-lookup"><span data-stu-id="a0279-115">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="a0279-116">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="a0279-116">Minimum supported client</span></span><br/> | <span data-ttu-id="a0279-117">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="a0279-117">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="a0279-118">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="a0279-118">Minimum supported server</span></span><br/> | <span data-ttu-id="a0279-119">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="a0279-119">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="a0279-120">En-tête</span><span class="sxs-lookup"><span data-stu-id="a0279-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="a0279-121"><dt>RichEdit. h</dt></span><span class="sxs-lookup"><span data-stu-id="a0279-121"><dt>Richedit.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a0279-122">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="a0279-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a0279-123">**TEXTRANGE**</span><span class="sxs-lookup"><span data-stu-id="a0279-123">**TEXTRANGE**</span></span>](/windows/win32/api/richedit/ns-richedit-textrangea)
</dt> </dl>

 

 





