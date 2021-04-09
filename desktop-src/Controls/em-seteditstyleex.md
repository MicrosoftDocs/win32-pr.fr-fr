---
title: Message EM_SETEDITSTYLEEX (RichEdit. h)
description: Définit les indicateurs de style de modification étendu actuels.
ms.assetid: C5CECC7C-6418-4A72-9F0B-6F55BE89E302
keywords:
- EM_SETEDITSTYLEEX les contrôles de message Windows
topic_type:
- apiref
api_name:
- EM_SETEDITSTYLEEX
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 72fe7a1ff420048f620d69196360678e9718a510
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103942663"
---
# <a name="em_seteditstyleex-message"></a><span data-ttu-id="1a19a-104">\_Message SETEDITSTYLEEX em</span><span class="sxs-lookup"><span data-stu-id="1a19a-104">EM\_SETEDITSTYLEEX message</span></span>

<span data-ttu-id="1a19a-105">Définit les indicateurs de style de modification étendu actuels.</span><span class="sxs-lookup"><span data-stu-id="1a19a-105">Sets the current extended edit style flags.</span></span>


```C++
#define EM_SETEDITSTYLEEX       (WM_USER + 275)
```



## <a name="parameters"></a><span data-ttu-id="1a19a-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="1a19a-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1a19a-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="1a19a-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="1a19a-108">Spécifie un ou plusieurs indicateurs de style de modification étendus.</span><span class="sxs-lookup"><span data-stu-id="1a19a-108">Specifies one or more extended edit style flags.</span></span> <span data-ttu-id="1a19a-109">Pour obtenir la liste des valeurs possibles, consultez [**em \_ GETEDITSTYLEEX**](/windows/desktop/Controls/em-geteditstyleex).</span><span class="sxs-lookup"><span data-stu-id="1a19a-109">For a list of possible values, see [**EM\_GETEDITSTYLEEX**](/windows/desktop/Controls/em-geteditstyleex).</span></span>

</dd> <dt>

<span data-ttu-id="1a19a-110">*lParam*</span><span class="sxs-lookup"><span data-stu-id="1a19a-110">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="1a19a-111">Masque composé d’une ou plusieurs des valeurs *wParam* .</span><span class="sxs-lookup"><span data-stu-id="1a19a-111">A mask consisting of one or more of the *wParam* values.</span></span> <span data-ttu-id="1a19a-112">Seules les valeurs spécifiées dans ce masque seront définies ou désactivées.</span><span class="sxs-lookup"><span data-stu-id="1a19a-112">Only the values specified in this mask will be set or cleared.</span></span> <span data-ttu-id="1a19a-113">Cela permet de définir ou d’effacer un seul indicateur sans lire les États de l’indicateur actuel.</span><span class="sxs-lookup"><span data-stu-id="1a19a-113">This allows a single flag to be set or cleared without reading the current flag states.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1a19a-114">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="1a19a-114">Return value</span></span>

<span data-ttu-id="1a19a-115">La valeur de retour est l’état des indicateurs de style de modification étendus après que la modification enrichie a tenté d’implémenter vos modifications de style de modification.</span><span class="sxs-lookup"><span data-stu-id="1a19a-115">The return value is the state of the extended edit style flags after rich edit has attempted to implement your edit style changes.</span></span> <span data-ttu-id="1a19a-116">Les indicateurs de style de modification sont un ensemble d’indicateurs qui indiquent le style d’édition actuel.</span><span class="sxs-lookup"><span data-stu-id="1a19a-116">The edit style flags are a set of flags that indicate the current edit style.</span></span>

## <a name="requirements"></a><span data-ttu-id="1a19a-117">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="1a19a-117">Requirements</span></span>



| <span data-ttu-id="1a19a-118">Condition requise</span><span class="sxs-lookup"><span data-stu-id="1a19a-118">Requirement</span></span> | <span data-ttu-id="1a19a-119">Valeur</span><span class="sxs-lookup"><span data-stu-id="1a19a-119">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="1a19a-120">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="1a19a-120">Minimum supported client</span></span><br/> | <span data-ttu-id="1a19a-121">Applications de \[ Bureau Windows 8 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="1a19a-121">Windows 8 \[desktop apps only\]</span></span><br/>                                            |
| <span data-ttu-id="1a19a-122">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="1a19a-122">Minimum supported server</span></span><br/> | <span data-ttu-id="1a19a-123">Applications de bureau Windows Server 2012 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="1a19a-123">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="1a19a-124">En-tête</span><span class="sxs-lookup"><span data-stu-id="1a19a-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="1a19a-125"><dt>RichEdit. h</dt></span><span class="sxs-lookup"><span data-stu-id="1a19a-125"><dt>Richedit.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1a19a-126">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="1a19a-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1a19a-127">**\_GETEDITSTYLEEX em**</span><span class="sxs-lookup"><span data-stu-id="1a19a-127">**EM\_GETEDITSTYLEEX**</span></span>](em-geteditstyleex.md)
</dt> </dl>

 

