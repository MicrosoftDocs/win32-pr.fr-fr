---
title: Message TB_SETMAXTEXTROWS (commctrl. h)
description: Définit le nombre maximal de lignes de texte affichées sur un bouton de barre d’outils.
ms.assetid: a14d74e8-cc21-482d-9bca-38dc7c0528ec
keywords:
- TB_SETMAXTEXTROWS les contrôles de message Windows
topic_type:
- apiref
api_name:
- TB_SETMAXTEXTROWS
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d0984c0b73280ec90c4e659d3bb3b4cc89cdcf4c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103941846"
---
# <a name="tb_setmaxtextrows-message"></a><span data-ttu-id="95e9c-104">TO \_ SETMAXTEXTROWS message</span><span class="sxs-lookup"><span data-stu-id="95e9c-104">TB\_SETMAXTEXTROWS message</span></span>

<span data-ttu-id="95e9c-105">Définit le nombre maximal de lignes de texte affichées sur un bouton de barre d’outils.</span><span class="sxs-lookup"><span data-stu-id="95e9c-105">Sets the maximum number of text rows displayed on a toolbar button.</span></span>

## <a name="parameters"></a><span data-ttu-id="95e9c-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="95e9c-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="95e9c-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="95e9c-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="95e9c-108">Nombre maximal de lignes de texte qui peuvent être affichées.</span><span class="sxs-lookup"><span data-stu-id="95e9c-108">Maximum number of rows of text that can be displayed.</span></span>

</dd> <dt>

<span data-ttu-id="95e9c-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="95e9c-109">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="95e9c-110">Doit être zéro.</span><span class="sxs-lookup"><span data-stu-id="95e9c-110">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="95e9c-111">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="95e9c-111">Return value</span></span>

<span data-ttu-id="95e9c-112">Retourne une valeur différente de zéro en cas de réussite, ou zéro dans le cas contraire.</span><span class="sxs-lookup"><span data-stu-id="95e9c-112">Returns nonzero if successful, or zero otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="95e9c-113">Notes</span><span class="sxs-lookup"><span data-stu-id="95e9c-113">Remarks</span></span>

<span data-ttu-id="95e9c-114">Pour que le texte soit renvoyé à la ligne, vous devez définir la largeur de bouton maximale en envoyant un message [**\_ SETBUTTONWIDTH to**](tb-setbuttonwidth.md) .</span><span class="sxs-lookup"><span data-stu-id="95e9c-114">To cause text to wrap, you must set the maximum button width by sending a [**TB\_SETBUTTONWIDTH**](tb-setbuttonwidth.md) message.</span></span> <span data-ttu-id="95e9c-115">Le texte est renvoyé à la ligne au niveau d’un saut de mot ; les sauts de ligne (« \\ n ») dans le texte sont ignorés.</span><span class="sxs-lookup"><span data-stu-id="95e9c-115">The text wraps at a word break; line breaks ("\\n") in the text are ignored.</span></span> <span data-ttu-id="95e9c-116">Le texte dans les \_ barres d’outils de liste TBSTYLE est toujours affiché sur une seule ligne.</span><span class="sxs-lookup"><span data-stu-id="95e9c-116">Text in TBSTYLE\_LIST toolbars is always shown on a single line.</span></span>

## <a name="requirements"></a><span data-ttu-id="95e9c-117">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="95e9c-117">Requirements</span></span>



| <span data-ttu-id="95e9c-118">Condition requise</span><span class="sxs-lookup"><span data-stu-id="95e9c-118">Requirement</span></span> | <span data-ttu-id="95e9c-119">Valeur</span><span class="sxs-lookup"><span data-stu-id="95e9c-119">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="95e9c-120">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="95e9c-120">Minimum supported client</span></span><br/> | <span data-ttu-id="95e9c-121">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="95e9c-121">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="95e9c-122">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="95e9c-122">Minimum supported server</span></span><br/> | <span data-ttu-id="95e9c-123">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="95e9c-123">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="95e9c-124">En-tête</span><span class="sxs-lookup"><span data-stu-id="95e9c-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="95e9c-125"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="95e9c-125"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





