---
title: LISTBOX. findItem
description: La méthode findItem recherche une chaîne donnée en commençant par l’élément qui suit l’index d’élément spécifié.
ms.assetid: 8d112d99-1866-45e5-b0ef-5d4a3c8b388d
keywords:
- LISTBOX. findItem Windows Media Player
topic_type:
- apiref
api_name:
- LISTBOX.findItem
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 161f4dd8b93fe4fed6a794dffde3e58e840c74e5
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106530307"
---
# <a name="listboxfinditem"></a><span data-ttu-id="84b21-104">LISTBOX. findItem</span><span class="sxs-lookup"><span data-stu-id="84b21-104">LISTBOX.findItem</span></span>

<span data-ttu-id="84b21-105">La méthode **FindItem** recherche une chaîne donnée en commençant par l’élément qui suit l’index d’élément spécifié.</span><span class="sxs-lookup"><span data-stu-id="84b21-105">The **findItem** method searches for a given string starting with the item following the specified item index.</span></span>

``` syntax
        elementID.findItem(startIndex, searchString)
```

## <a name="parameters"></a><span data-ttu-id="84b21-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="84b21-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="84b21-107"><span id="startIndex"></span><span id="startindex"></span><span id="STARTINDEX"></span>*startIndex*</span><span class="sxs-lookup"><span data-stu-id="84b21-107"><span id="startIndex"></span><span id="startindex"></span><span id="STARTINDEX"></span>*startIndex*</span></span>
</dt> <dd>

<span data-ttu-id="84b21-108">**Nombre** (**long**) contenant l’index de l’élément à partir duquel commencer la recherche.</span><span class="sxs-lookup"><span data-stu-id="84b21-108">**Number** (**long**) containing the index of the item at which to start the search.</span></span>

</dd> <dt>

<span data-ttu-id="84b21-109"><span id="searchString"></span><span id="searchstring"></span><span id="SEARCHSTRING"></span>*searchString*</span><span class="sxs-lookup"><span data-stu-id="84b21-109"><span id="searchString"></span><span id="searchstring"></span><span id="SEARCHSTRING"></span>*searchString*</span></span>
</dt> <dd>

<span data-ttu-id="84b21-110">**Chaîne** contenant le texte à rechercher.</span><span class="sxs-lookup"><span data-stu-id="84b21-110">**String** containing the text to search for.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="84b21-111">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="84b21-111">Return Value</span></span>

<span data-ttu-id="84b21-112">Cette méthode retourne un **nombre** (**long**) contenant l’index de l’élément qui contient la chaîne.</span><span class="sxs-lookup"><span data-stu-id="84b21-112">This method returns a **Number** (**long**) containing the index of the item that contains the string.</span></span>

## <a name="remarks"></a><span data-ttu-id="84b21-113">Notes</span><span class="sxs-lookup"><span data-stu-id="84b21-113">Remarks</span></span>

<span data-ttu-id="84b21-114">Pour démarrer la recherche à la première ligne du contrôle de zone de liste, utilisez 1 comme *startIndex*.</span><span class="sxs-lookup"><span data-stu-id="84b21-114">To start the search at the first line of the list box control, use  1 as the *startIndex*.</span></span> <span data-ttu-id="84b21-115">Pour continuer à rechercher du texte après la détection de la première ligne, utilisez l’index de ligne retourné comme *startIndex*, et la recherche commence à la ligne suivante.</span><span class="sxs-lookup"><span data-stu-id="84b21-115">To continue to search for text after the first line is found, use the returned line index as the *startIndex*, and the search will start at the next line.</span></span> <span data-ttu-id="84b21-116">Cette méthode recherche des sous-chaînes et ne respecte pas la casse.</span><span class="sxs-lookup"><span data-stu-id="84b21-116">This method will search for substrings and is not case-sensitive.</span></span>

## <a name="requirements"></a><span data-ttu-id="84b21-117">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="84b21-117">Requirements</span></span>



| <span data-ttu-id="84b21-118">Condition requise</span><span class="sxs-lookup"><span data-stu-id="84b21-118">Requirement</span></span> | <span data-ttu-id="84b21-119">Valeur</span><span class="sxs-lookup"><span data-stu-id="84b21-119">Value</span></span> |
|--------------------|---------------------------------------------------------|
| <span data-ttu-id="84b21-120">Version</span><span class="sxs-lookup"><span data-stu-id="84b21-120">Version</span></span><br/> | <span data-ttu-id="84b21-121">Lecteur Windows Media pour Windows XP ou version ultérieure</span><span class="sxs-lookup"><span data-stu-id="84b21-121">Windows Media Player for Windows XP or later</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="84b21-122">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="84b21-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="84b21-123">**Élément LISTBOX**</span><span class="sxs-lookup"><span data-stu-id="84b21-123">**LISTBOX Element**</span></span>](listbox-element.md)
</dt> </dl>

 

 





