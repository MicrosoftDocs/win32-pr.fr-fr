---
title: Message EM_SETEDITSTYLE (RichEdit. h)
description: Définit les indicateurs de style de modification actuels pour un contrôle RichEdit.
ms.assetid: e48de6b3-0fd2-4791-9863-a6dcdafa3642
keywords:
- EM_SETEDITSTYLE les contrôles de message Windows
topic_type:
- apiref
api_name:
- EM_SETEDITSTYLE
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 14c7b7e1d3990a00fb6931ed39bbd28aa6f8c2ce
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104509170"
---
# <a name="em_seteditstyle-message"></a><span data-ttu-id="70dcb-104">\_Message SETEDITSTYLE em</span><span class="sxs-lookup"><span data-stu-id="70dcb-104">EM\_SETEDITSTYLE message</span></span>

<span data-ttu-id="70dcb-105">Définit les indicateurs de style de modification actuels pour un contrôle RichEdit.</span><span class="sxs-lookup"><span data-stu-id="70dcb-105">Sets the current edit style flags for a rich edit control.</span></span>

## <a name="parameters"></a><span data-ttu-id="70dcb-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="70dcb-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="70dcb-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="70dcb-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="70dcb-108">Spécifie un ou plusieurs indicateurs de style de modification.</span><span class="sxs-lookup"><span data-stu-id="70dcb-108">Specifies one or more edit style flags.</span></span> <span data-ttu-id="70dcb-109">Pour obtenir la liste des valeurs possibles, consultez [**em \_ GETEDITSTYLE**](em-geteditstyle.md).</span><span class="sxs-lookup"><span data-stu-id="70dcb-109">For a list of possible values, see [**EM\_GETEDITSTYLE**](em-geteditstyle.md).</span></span>

</dd> <dt>

<span data-ttu-id="70dcb-110">*lParam*</span><span class="sxs-lookup"><span data-stu-id="70dcb-110">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="70dcb-111">Masque composé d’une ou plusieurs des valeurs *wParam* .</span><span class="sxs-lookup"><span data-stu-id="70dcb-111">A mask consisting of one or more of the *wParam* values.</span></span> <span data-ttu-id="70dcb-112">Seules les valeurs spécifiées dans ce masque seront définies ou désactivées.</span><span class="sxs-lookup"><span data-stu-id="70dcb-112">Only the values specified in this mask will be set or cleared.</span></span> <span data-ttu-id="70dcb-113">Cela permet de définir ou d’effacer un seul indicateur sans lire les États de l’indicateur actuel.</span><span class="sxs-lookup"><span data-stu-id="70dcb-113">This allows a single flag to be set or cleared without reading the current flag states.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="70dcb-114">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="70dcb-114">Return value</span></span>

<span data-ttu-id="70dcb-115">La valeur de retour est l’état des indicateurs de style de modification après que le contrôle RichEdit a tenté d’implémenter vos modifications de style de modification.</span><span class="sxs-lookup"><span data-stu-id="70dcb-115">The return value is the state of the edit style flags after the rich edit control has attempted to implement your edit style changes.</span></span> <span data-ttu-id="70dcb-116">Les indicateurs de style de modification sont un ensemble d’indicateurs qui indiquent le style d’édition actuel.</span><span class="sxs-lookup"><span data-stu-id="70dcb-116">The edit style flags are a set of flags that indicate the current edit style.</span></span>

## <a name="requirements"></a><span data-ttu-id="70dcb-117">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="70dcb-117">Requirements</span></span>



| <span data-ttu-id="70dcb-118">Condition requise</span><span class="sxs-lookup"><span data-stu-id="70dcb-118">Requirement</span></span> | <span data-ttu-id="70dcb-119">Valeur</span><span class="sxs-lookup"><span data-stu-id="70dcb-119">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="70dcb-120">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="70dcb-120">Minimum supported client</span></span><br/> | <span data-ttu-id="70dcb-121">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="70dcb-121">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="70dcb-122">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="70dcb-122">Minimum supported server</span></span><br/> | <span data-ttu-id="70dcb-123">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="70dcb-123">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="70dcb-124">Composant redistribuable</span><span class="sxs-lookup"><span data-stu-id="70dcb-124">Redistributable</span></span><br/>          | <span data-ttu-id="70dcb-125">Édition enrichie 3,0</span><span class="sxs-lookup"><span data-stu-id="70dcb-125">Rich Edit 3.0</span></span><br/>                                                              |
| <span data-ttu-id="70dcb-126">En-tête</span><span class="sxs-lookup"><span data-stu-id="70dcb-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="70dcb-127"><dt>RichEdit. h</dt></span><span class="sxs-lookup"><span data-stu-id="70dcb-127"><dt>Richedit.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="70dcb-128">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="70dcb-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="70dcb-129">**EM \_ GETEDITSTYLE**</span><span class="sxs-lookup"><span data-stu-id="70dcb-129">**EM\_GETEDITSTYLE**</span></span>](em-geteditstyle.md)
</dt> </dl>

 

 





