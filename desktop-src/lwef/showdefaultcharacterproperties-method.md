---
title: Méthode ShowDefaultCharacterProperties
description: Méthode ShowDefaultCharacterProperties
ms.assetid: a3b109c0-5701-4a72-baae-bcbb97b025a3
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2f055b2ca0f00e0a13c24ec95dc82509ae9c45b7
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103672809"
---
# <a name="showdefaultcharacterproperties-method"></a><span data-ttu-id="a34e7-103">Méthode ShowDefaultCharacterProperties</span><span class="sxs-lookup"><span data-stu-id="a34e7-103">ShowDefaultCharacterProperties Method</span></span>

<span data-ttu-id="a34e7-104">\[Microsoft Agent est déconseillé à partir de Windows 7 et peut ne pas être disponible dans les versions ultérieures de Windows.\]</span><span class="sxs-lookup"><span data-stu-id="a34e7-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

<dl> <dt>

<span data-ttu-id="a34e7-105"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Descriptive**</span><span class="sxs-lookup"><span data-stu-id="a34e7-105"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Description**</span></span>
</dt> <dd>

<span data-ttu-id="a34e7-106">Affiche les propriétés du caractère par défaut.</span><span class="sxs-lookup"><span data-stu-id="a34e7-106">Displays the default character's properties.</span></span>

</dd> <dt>

<span data-ttu-id="a34e7-107"><span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Stockéesyntaxe**</span><span class="sxs-lookup"><span data-stu-id="a34e7-107"><span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Syntax**</span></span>
</dt> <dd>

<span data-ttu-id="a34e7-108">\*agent \* \* *. ShowDefaultCharacterProperties* \*  \[ *X* , *Y*\]</span><span class="sxs-lookup"><span data-stu-id="a34e7-108">*agent\*\*\*.ShowDefaultCharacterProperties*\* \[ *X* , *Y* \]</span></span>



| <span data-ttu-id="a34e7-109">Partie</span><span class="sxs-lookup"><span data-stu-id="a34e7-109">Part</span></span> | <span data-ttu-id="a34e7-110">Description</span><span class="sxs-lookup"><span data-stu-id="a34e7-110">Description</span></span>                                                                                                                                                |
|------|------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a34e7-111">*X*</span><span class="sxs-lookup"><span data-stu-id="a34e7-111">*X*</span></span>  | <span data-ttu-id="a34e7-112">Optionnel.</span><span class="sxs-lookup"><span data-stu-id="a34e7-112">Optional.</span></span> <span data-ttu-id="a34e7-113">Valeur entière de type short qui indique la coordonnée d’écran horizontale (*X* ) pour afficher la fenêtre.</span><span class="sxs-lookup"><span data-stu-id="a34e7-113">A short integer value that indicates the horizontal (*X* ) screen coordinate to display the window.</span></span> <span data-ttu-id="a34e7-114">Cette coordonnée doit être spécifiée en pixels.</span><span class="sxs-lookup"><span data-stu-id="a34e7-114">This coordinate must be specified in pixels.</span></span> |
| <span data-ttu-id="a34e7-115">*O*</span><span class="sxs-lookup"><span data-stu-id="a34e7-115">*Y*</span></span>  | <span data-ttu-id="a34e7-116">Optionnel.</span><span class="sxs-lookup"><span data-stu-id="a34e7-116">Optional.</span></span> <span data-ttu-id="a34e7-117">Valeur entière de type short qui indique la coordonnée d’écran verticale (*Y*) pour afficher la fenêtre.</span><span class="sxs-lookup"><span data-stu-id="a34e7-117">A short integer value that indicates the vertical (*Y*) screen coordinate to display the window.</span></span> <span data-ttu-id="a34e7-118">Cette coordonnée doit être spécifiée en pixels.</span><span class="sxs-lookup"><span data-stu-id="a34e7-118">This coordinate must be specified in pixels.</span></span>    |



 

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="a34e7-119">Notes</span><span class="sxs-lookup"><span data-stu-id="a34e7-119">Remarks</span></span>

<span data-ttu-id="a34e7-120">L’appel de cette méthode affiche la fenêtre de propriétés de caractères par défaut (et non la feuille de propriétés de l’agent Microsoft).</span><span class="sxs-lookup"><span data-stu-id="a34e7-120">Calling this method displays the default character properties window (not the Microsoft Agent property sheet).</span></span> <span data-ttu-id="a34e7-121">Si vous ne spécifiez pas les coordonnées X et Y, la fenêtre s’affiche au dernier emplacement affiché.</span><span class="sxs-lookup"><span data-stu-id="a34e7-121">If you do not specify the X and Y coordinates, the window appears at the last location it was displayed.</span></span>

## <a name="see-also"></a><span data-ttu-id="a34e7-122">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="a34e7-122">See Also</span></span>

[<span data-ttu-id="a34e7-123">**Événement DefaultCharacterChange**</span><span class="sxs-lookup"><span data-stu-id="a34e7-123">**DefaultCharacterChange event**</span></span>](defaultcharacterchange-event.md)


 

 




