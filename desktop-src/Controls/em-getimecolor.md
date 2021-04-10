---
title: Message EM_GETIMECOLOR (RichEdit. h)
description: Récupère la couleur de composition de l’éditeur de méthode d’entrée (IME).
ms.assetid: 788ac56c-f2d8-4e9a-8829-b92dcd76e6de
keywords:
- EM_GETIMECOLOR les contrôles de message Windows
topic_type:
- apiref
api_name:
- EM_GETIMECOLOR
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b8a19061651787ff94575f8bc64a69f06d445a7f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103942486"
---
# <a name="em_getimecolor-message"></a><span data-ttu-id="61307-104">\_Message GETIMECOLOR em</span><span class="sxs-lookup"><span data-stu-id="61307-104">EM\_GETIMECOLOR message</span></span>

<span data-ttu-id="61307-105">Récupère la couleur de composition de l’éditeur de méthode d’entrée (IME).</span><span class="sxs-lookup"><span data-stu-id="61307-105">Retrieves the Input Method Editor (IME) composition color.</span></span>

> [!Note]  
> <span data-ttu-id="61307-106">Ce message est pris en charge uniquement dans les versions asiatiques de Microsoft Rich Edit 1,0.</span><span class="sxs-lookup"><span data-stu-id="61307-106">This message is supported only in Asian-language versions of Microsoft Rich Edit 1.0.</span></span> <span data-ttu-id="61307-107">Elle n’est pas prise en charge dans les versions ultérieures de la modification enrichie.</span><span class="sxs-lookup"><span data-stu-id="61307-107">It is not supported in any later versions of Rich Edit.</span></span>

 

## <a name="parameters"></a><span data-ttu-id="61307-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="61307-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="61307-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="61307-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="61307-110">Ce paramètre n’est pas utilisé ; elle doit être égale à zéro.</span><span class="sxs-lookup"><span data-stu-id="61307-110">This parameter is not used; it must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="61307-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="61307-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="61307-112">Tableau de quatre éléments de structures [**COMPCOLOR**](/windows/desktop/api/Richedit/ns-richedit-compcolor) qui reçoit la couleur de composition.</span><span class="sxs-lookup"><span data-stu-id="61307-112">A four-element array of [**COMPCOLOR**](/windows/desktop/api/Richedit/ns-richedit-compcolor) structures that receives the composition color.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="61307-113">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="61307-113">Return value</span></span>

<span data-ttu-id="61307-114">Si l’opération a échoué, la valeur de retour est une valeur différente de zéro.</span><span class="sxs-lookup"><span data-stu-id="61307-114">If the operation succeeds, the return value is a nonzero value.</span></span>

<span data-ttu-id="61307-115">Si l’opération échoue, la valeur de retour est zéro.</span><span class="sxs-lookup"><span data-stu-id="61307-115">If the operation fails, the return value is zero.</span></span>

## <a name="requirements"></a><span data-ttu-id="61307-116">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="61307-116">Requirements</span></span>



| <span data-ttu-id="61307-117">Condition requise</span><span class="sxs-lookup"><span data-stu-id="61307-117">Requirement</span></span> | <span data-ttu-id="61307-118">Valeur</span><span class="sxs-lookup"><span data-stu-id="61307-118">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="61307-119">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="61307-119">Minimum supported client</span></span><br/> | <span data-ttu-id="61307-120">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="61307-120">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="61307-121">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="61307-121">Minimum supported server</span></span><br/> | <span data-ttu-id="61307-122">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="61307-122">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="61307-123">En-tête</span><span class="sxs-lookup"><span data-stu-id="61307-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="61307-124"><dt>RichEdit. h</dt></span><span class="sxs-lookup"><span data-stu-id="61307-124"><dt>Richedit.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="61307-125">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="61307-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="61307-126">**COMPCOLOR**</span><span class="sxs-lookup"><span data-stu-id="61307-126">**COMPCOLOR**</span></span>](/windows/desktop/api/Richedit/ns-richedit-compcolor)
</dt> </dl>

 

 





