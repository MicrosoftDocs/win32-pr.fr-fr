---
description: Se produit lorsque la sélection actuelle de texte dans le contrôle InkEdit a changé ou que le point d’insertion a été déplacé.
ms.assetid: 14ddffe7-bdfe-4a35-82c7-b3401b5b720c
title: Événement InkEdit. SelChange (. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 66b51ef4edbf7d7fb02be17dc416c0a777a9519a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106529270"
---
# <a name="inkeditselchange-event"></a><span data-ttu-id="ddbeb-103">Événement InkEdit. SelChange</span><span class="sxs-lookup"><span data-stu-id="ddbeb-103">InkEdit.SelChange event</span></span>

<span data-ttu-id="ddbeb-104">Se produit lorsque la sélection actuelle de texte dans le contrôle [InkEdit](inkedit-control-reference.md) a changé ou que le point d’insertion a été déplacé.</span><span class="sxs-lookup"><span data-stu-id="ddbeb-104">Occurs when the current selection of text in the [InkEdit](inkedit-control-reference.md) control has changed or the insertion point has moved.</span></span>

## <a name="syntax"></a><span data-ttu-id="ddbeb-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="ddbeb-105">Syntax</span></span>


```C++
void SelChange();
```



## <a name="parameters"></a><span data-ttu-id="ddbeb-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="ddbeb-106">Parameters</span></span>

<span data-ttu-id="ddbeb-107">Cet événement n’a pas de paramètres.</span><span class="sxs-lookup"><span data-stu-id="ddbeb-107">This event has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="ddbeb-108">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="ddbeb-108">Return value</span></span>

<span data-ttu-id="ddbeb-109">Cet événement ne retourne pas de valeur.</span><span class="sxs-lookup"><span data-stu-id="ddbeb-109">This event does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="ddbeb-110">Notes</span><span class="sxs-lookup"><span data-stu-id="ddbeb-110">Remarks</span></span>

<span data-ttu-id="ddbeb-111">Vous pouvez utiliser l’événement **SelChange** pour vérifier les différentes propriétés qui fournissent des informations sur la sélection actuelle (par exemple, [**SelBold**](/windows/desktop/api/inked/nf-inked-iinkedit-get_selbold)) afin de pouvoir mettre à jour les boutons dans une barre d’outils, par exemple.</span><span class="sxs-lookup"><span data-stu-id="ddbeb-111">You can use the **SelChange** event to check the various properties that give information about the current selection (such as [**SelBold**](/windows/desktop/api/inked/nf-inked-iinkedit-get_selbold)) so you can update buttons in a toolbar, for example.</span></span>

## <a name="requirements"></a><span data-ttu-id="ddbeb-112">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="ddbeb-112">Requirements</span></span>



| <span data-ttu-id="ddbeb-113">Condition requise</span><span class="sxs-lookup"><span data-stu-id="ddbeb-113">Requirement</span></span> | <span data-ttu-id="ddbeb-114">Valeur</span><span class="sxs-lookup"><span data-stu-id="ddbeb-114">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ddbeb-115">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="ddbeb-115">Minimum supported client</span></span><br/> | <span data-ttu-id="ddbeb-116">Applications de bureau Windows XP Édition Tablet PC \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="ddbeb-116">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="ddbeb-117">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="ddbeb-117">Minimum supported server</span></span><br/> | <span data-ttu-id="ddbeb-118">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="ddbeb-118">None supported</span></span><br/>                                                                                     |
| <span data-ttu-id="ddbeb-119">En-tête</span><span class="sxs-lookup"><span data-stu-id="ddbeb-119">Header</span></span><br/>                   | <dl> <span data-ttu-id="ddbeb-120"><dt>« Y2. h » (nécessite également l' \_ entrée i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="ddbeb-120"><dt>Inked.h (also requires inked\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="ddbeb-121">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="ddbeb-121">Library</span></span><br/>                  | <dl> <span data-ttu-id="ddbeb-122"><dt>InkEd.dll</dt></span><span class="sxs-lookup"><span data-stu-id="ddbeb-122"><dt>InkEd.dll</dt></span></span> </dl>                          |



## <a name="see-also"></a><span data-ttu-id="ddbeb-123">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="ddbeb-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ddbeb-124">InkEdit</span><span class="sxs-lookup"><span data-stu-id="ddbeb-124">InkEdit</span></span>](inkedit-control-reference.md)
</dt> </dl>

 

 




