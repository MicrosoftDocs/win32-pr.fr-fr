---
description: Un descripteur HRECOWORDLIST est utilisé pour gérer une liste de mots que vous attachez à un contexte de module de reconnaissance. Vous utilisez une liste de mots pour améliorer les résultats de la reconnaissance.
ms.assetid: 7333307b-1857-48a7-bb9f-bdbd8530f093
title: Handle HRECOWORDLIST (Récapitulatifis. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f5e5d33862cacb7040a26edc23d7db04c57206c7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104526572"
---
# <a name="hrecowordlist-handle"></a><span data-ttu-id="262fb-104">Handle HRECOWORDLIST</span><span class="sxs-lookup"><span data-stu-id="262fb-104">HRECOWORDLIST Handle</span></span>

<span data-ttu-id="262fb-105">Un descripteur **HRECOWORDLIST** est utilisé pour gérer une liste de mots que vous attachez à un contexte de module de reconnaissance.</span><span class="sxs-lookup"><span data-stu-id="262fb-105">An **HRECOWORDLIST** handle is used to manage a word list you attach to a recognizer context.</span></span> <span data-ttu-id="262fb-106">Vous utilisez une liste de mots pour améliorer les résultats de la reconnaissance.</span><span class="sxs-lookup"><span data-stu-id="262fb-106">You use a word list to improve recognition results.</span></span>


```C++
typedef HANDLE HRECOWORDLIST;
```



## <a name="remarks"></a><span data-ttu-id="262fb-107">Notes</span><span class="sxs-lookup"><span data-stu-id="262fb-107">Remarks</span></span>

<span data-ttu-id="262fb-108">La fonction suivante utilise un **HRECOWORDLIST**.</span><span class="sxs-lookup"><span data-stu-id="262fb-108">The following function use an **HRECOWORDLIST**.</span></span>



| <span data-ttu-id="262fb-109">Fonction</span><span class="sxs-lookup"><span data-stu-id="262fb-109">Function</span></span>                                         | <span data-ttu-id="262fb-110">Description</span><span class="sxs-lookup"><span data-stu-id="262fb-110">Description</span></span>                                         |
|--------------------------------------------------|-----------------------------------------------------|
| [<span data-ttu-id="262fb-111">**AddWordsToWordList**</span><span class="sxs-lookup"><span data-stu-id="262fb-111">**AddWordsToWordList**</span></span>](/windows/desktop/api/recapis/nf-recapis-addwordstowordlist) | <span data-ttu-id="262fb-112">Ajoute un ou plusieurs mots à la liste de mots.</span><span class="sxs-lookup"><span data-stu-id="262fb-112">Adds one or more words to the word list.</span></span><br/> |
| [<span data-ttu-id="262fb-113">**DestroyWordList**</span><span class="sxs-lookup"><span data-stu-id="262fb-113">**DestroyWordList**</span></span>](/windows/desktop/api/recapis/nf-recapis-destroywordlist)       | <span data-ttu-id="262fb-114">Détruit la liste de mots active.</span><span class="sxs-lookup"><span data-stu-id="262fb-114">Destroys the current word list.</span></span><br/>          |
| [<span data-ttu-id="262fb-115">**MakeWordList**</span><span class="sxs-lookup"><span data-stu-id="262fb-115">**MakeWordList**</span></span>](/windows/desktop/api/recapis/nf-recapis-makewordlist)             | <span data-ttu-id="262fb-116">Crée une liste de mots.</span><span class="sxs-lookup"><span data-stu-id="262fb-116">Creates a word list.</span></span><br/>                     |



 

## <a name="requirements"></a><span data-ttu-id="262fb-117">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="262fb-117">Requirements</span></span>



| <span data-ttu-id="262fb-118">Condition requise</span><span class="sxs-lookup"><span data-stu-id="262fb-118">Requirement</span></span> | <span data-ttu-id="262fb-119">Valeur</span><span class="sxs-lookup"><span data-stu-id="262fb-119">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="262fb-120">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="262fb-120">Minimum supported client</span></span><br/> | <span data-ttu-id="262fb-121">Applications de bureau Windows XP Édition Tablet PC \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="262fb-121">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                        |
| <span data-ttu-id="262fb-122">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="262fb-122">Minimum supported server</span></span><br/> | <span data-ttu-id="262fb-123">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="262fb-123">None supported</span></span><br/>                                                            |
| <span data-ttu-id="262fb-124">En-tête</span><span class="sxs-lookup"><span data-stu-id="262fb-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="262fb-125"><dt>Récapitulatif</dt></span><span class="sxs-lookup"><span data-stu-id="262fb-125"><dt>Recapis.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="262fb-126">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="262fb-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="262fb-127">**SetWordList fonction)**</span><span class="sxs-lookup"><span data-stu-id="262fb-127">**SetWordList Function**</span></span>](/windows/desktop/api/recapis/nf-recapis-setwordlist)
</dt> </dl>

 

 




