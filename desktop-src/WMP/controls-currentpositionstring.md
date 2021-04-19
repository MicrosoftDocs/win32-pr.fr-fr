---
title: Controls. currentPositionString
description: La propriété currentPositionString récupère la position actuelle dans l’élément multimédia sous la forme d’une chaîne au format HH MM SS (heures, minutes et secondes).
ms.assetid: 2b360cdb-3cf8-4d3c-82c2-7eb621f82f4c
keywords:
- Controls. currentPositionString Windows Media Player
topic_type:
- apiref
api_name:
- Controls.currentPositionString
api_location:
- wmp.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cbf3472d71afc543c596485d10f0d7e59dde90a0
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106542714"
---
# <a name="controlscurrentpositionstring"></a><span data-ttu-id="2e9b5-104">Controls. currentPositionString</span><span class="sxs-lookup"><span data-stu-id="2e9b5-104">Controls.currentPositionString</span></span>

<span data-ttu-id="2e9b5-105">La propriété **currentPositionString** récupère la position actuelle dans l’élément multimédia sous la forme d’une **chaîne** au format hh : mm : SS (heures, minutes et secondes).</span><span class="sxs-lookup"><span data-stu-id="2e9b5-105">The **currentPositionString** property retrieves the current position in the media item as a **String** formatted as HH:MM:SS (hours, minutes, and seconds).</span></span>

``` syntax
player.controls.currentPositionString
      
```

## <a name="possible-values"></a><span data-ttu-id="2e9b5-106">Valeurs possibles</span><span class="sxs-lookup"><span data-stu-id="2e9b5-106">Possible Values</span></span>

<span data-ttu-id="2e9b5-107">Cette propriété est une **chaîne** en lecture seule.</span><span class="sxs-lookup"><span data-stu-id="2e9b5-107">This property is a read-only **String**.</span></span>

## <a name="remarks"></a><span data-ttu-id="2e9b5-108">Notes</span><span class="sxs-lookup"><span data-stu-id="2e9b5-108">Remarks</span></span>

<span data-ttu-id="2e9b5-109">Si l’élément multimédia a une valeur inférieure à une heure, la partie HH : n’est pas incluse.</span><span class="sxs-lookup"><span data-stu-id="2e9b5-109">If the media item is less than an hour long, the HH: portion is not included.</span></span>

> [!Note]  
> <span data-ttu-id="2e9b5-110">Vous devez inclure du code pour arrêter la minuterie lorsque l’élément multimédia est arrêté ou suspendu.</span><span class="sxs-lookup"><span data-stu-id="2e9b5-110">You should include code to stop the timer when the media item is stopped or paused.</span></span>

 

## <a name="examples"></a><span data-ttu-id="2e9b5-111">Exemples</span><span class="sxs-lookup"><span data-stu-id="2e9b5-111">Examples</span></span>

<span data-ttu-id="2e9b5-112">L’exemple JScript suivant démarre une minuterie HTML qui affiche la position actuelle du fichier multimédia à intervalles d’une seconde.</span><span class="sxs-lookup"><span data-stu-id="2e9b5-112">The following JScript example starts an HTML timer that displays the current position of the media file at one-second intervals.</span></span> <span data-ttu-id="2e9b5-113">Un élément de texte HTML nommé MyText a été créé pour afficher la position actuelle.</span><span class="sxs-lookup"><span data-stu-id="2e9b5-113">An HTML TEXT element named MyText was created to display the current position.</span></span> <span data-ttu-id="2e9b5-114">L’objet **Player** a été créé avec ID = "Player".</span><span class="sxs-lookup"><span data-stu-id="2e9b5-114">The **Player** object was created with ID = "Player".</span></span>


```JScript
var timer = window.setInterval("MyText.value = Player.controls.currentPositionString",1000);
```



## <a name="requirements"></a><span data-ttu-id="2e9b5-115">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="2e9b5-115">Requirements</span></span>



| <span data-ttu-id="2e9b5-116">Condition requise</span><span class="sxs-lookup"><span data-stu-id="2e9b5-116">Requirement</span></span> | <span data-ttu-id="2e9b5-117">Valeur</span><span class="sxs-lookup"><span data-stu-id="2e9b5-117">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="2e9b5-118">Version</span><span class="sxs-lookup"><span data-stu-id="2e9b5-118">Version</span></span><br/> | <span data-ttu-id="2e9b5-119">Lecteur Windows Media version 7,0 ou ultérieure.</span><span class="sxs-lookup"><span data-stu-id="2e9b5-119">Windows Media Player version 7.0 or later.</span></span><br/>                              |
| <span data-ttu-id="2e9b5-120">DLL</span><span class="sxs-lookup"><span data-stu-id="2e9b5-120">DLL</span></span><br/>     | <dl> <span data-ttu-id="2e9b5-121"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="2e9b5-121"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2e9b5-122">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="2e9b5-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2e9b5-123">**Controls (objet)**</span><span class="sxs-lookup"><span data-stu-id="2e9b5-123">**Controls Object**</span></span>](controls-object.md)
</dt> </dl>

 

 





