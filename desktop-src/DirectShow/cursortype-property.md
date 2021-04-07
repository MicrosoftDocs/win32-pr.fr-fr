---
description: La propriété CursorType définit ou récupère le type de curseur actuel.
ms.assetid: f362e790-a7c7-4fb6-86f3-7cd25f78fe0e
title: CursorType, propriété
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1c17ae74c471bebe6da2bcef4d22d7c247f4eda1
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/06/2021
ms.locfileid: "103846357"
---
# <a name="cursortype-property"></a><span data-ttu-id="632d1-103">CursorType, propriété</span><span class="sxs-lookup"><span data-stu-id="632d1-103">CursorType Property</span></span>

> [!Note]  
> <span data-ttu-id="632d1-104">Ce composant peut être utilisé dans les systèmes d’exploitation Microsoft Windows 2000, Windows XP et Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="632d1-104">This component is available for use in the Microsoft Windows 2000, Windows XP, and Windows Server 2003 operating systems.</span></span> <span data-ttu-id="632d1-105">Il sera peut-être modifié ou indisponible dans les versions ultérieures.</span><span class="sxs-lookup"><span data-stu-id="632d1-105">It may be altered or unavailable in subsequent versions.</span></span>

 

<span data-ttu-id="632d1-106">La `CursorType` propriété définit ou récupère le type de curseur actuel.</span><span class="sxs-lookup"><span data-stu-id="632d1-106">The `CursorType` property sets or retrieves the current cursor type.</span></span>

``` syntax
[ iCursorType = ] MSWebDVD.CursorType
```

## <a name="return-value"></a><span data-ttu-id="632d1-107">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="632d1-107">Return Value</span></span>

<span data-ttu-id="632d1-108">Retourne une valeur entière représentant le type de curseur.</span><span class="sxs-lookup"><span data-stu-id="632d1-108">Returns an integer value representing the cursor type.</span></span>

## <a name="remarks"></a><span data-ttu-id="632d1-109">Notes</span><span class="sxs-lookup"><span data-stu-id="632d1-109">Remarks</span></span>

<span data-ttu-id="632d1-110">Les valeurs possibles pour cette propriété sont :</span><span class="sxs-lookup"><span data-stu-id="632d1-110">The possible values for this property are:</span></span>



| <span data-ttu-id="632d1-111">Valeur</span><span class="sxs-lookup"><span data-stu-id="632d1-111">Value</span></span> | <span data-ttu-id="632d1-112">Description</span><span class="sxs-lookup"><span data-stu-id="632d1-112">Description</span></span> |
|-------|-------------|
| <span data-ttu-id="632d1-113">0</span><span class="sxs-lookup"><span data-stu-id="632d1-113">0</span></span>     | <span data-ttu-id="632d1-114">Flèche</span><span class="sxs-lookup"><span data-stu-id="632d1-114">Arrow</span></span>       |
| <span data-ttu-id="632d1-115">1</span><span class="sxs-lookup"><span data-stu-id="632d1-115">1</span></span>     | <span data-ttu-id="632d1-116">Zoom avant</span><span class="sxs-lookup"><span data-stu-id="632d1-116">Zoom In</span></span>     |
| <span data-ttu-id="632d1-117">2</span><span class="sxs-lookup"><span data-stu-id="632d1-117">2</span></span>     | <span data-ttu-id="632d1-118">Zoom arrière</span><span class="sxs-lookup"><span data-stu-id="632d1-118">Zoom Out</span></span>    |
| <span data-ttu-id="632d1-119">3</span><span class="sxs-lookup"><span data-stu-id="632d1-119">3</span></span>     | <span data-ttu-id="632d1-120">Toutefois</span><span class="sxs-lookup"><span data-stu-id="632d1-120">Hand</span></span>        |
| <span data-ttu-id="632d1-121">-1</span><span class="sxs-lookup"><span data-stu-id="632d1-121">-1</span></span>    | <span data-ttu-id="632d1-122">Aucun</span><span class="sxs-lookup"><span data-stu-id="632d1-122">None</span></span>        |



 

<span data-ttu-id="632d1-123">Cette propriété est en lecture/écriture avec une valeur par défaut de zéro.</span><span class="sxs-lookup"><span data-stu-id="632d1-123">This property is read/write with a default value of zero.</span></span> <span data-ttu-id="632d1-124">Lorsque l’image est zoomée, le paramètre `CursorType` à la **main** (0x3) met l’application en mode glisser-déplacer, ce qui permet à l’utilisateur de déplacer l’image à l’intérieur de la zone d’affichage vidéo.</span><span class="sxs-lookup"><span data-stu-id="632d1-124">When the picture is zoomed in, setting `CursorType` to **Hand** (0x3) puts the application into drag mode, enabling the user to move the image inside the video display area.</span></span>

 

 



