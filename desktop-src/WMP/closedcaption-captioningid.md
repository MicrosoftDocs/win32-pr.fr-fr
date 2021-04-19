---
title: ClosedCaption.captioningID
description: La propriété captioningID spécifie ou récupère le nom de l’élément affichant le sous-titrage.
ms.assetid: 99d4aae3-485f-4c86-9130-101b1ca968e9
keywords:
- Lecteur Windows Media ClosedCaption. captioningID
topic_type:
- apiref
api_name:
- ClosedCaption.captioningID
api_location:
- wmp.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: faadae626dd5ac0314c4140e3f9d82ab645ef9b2
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106522407"
---
# <a name="closedcaptioncaptioningid"></a><span data-ttu-id="a2f36-104">ClosedCaption.captioningID</span><span class="sxs-lookup"><span data-stu-id="a2f36-104">ClosedCaption.captioningID</span></span>

<span data-ttu-id="a2f36-105">La propriété **captioningID** spécifie ou récupère le nom de l’élément affichant le sous-titrage.</span><span class="sxs-lookup"><span data-stu-id="a2f36-105">The **captioningID** property specifies or retrieves the name of the element displaying the captioning.</span></span>

``` syntax
player.closedCaption.captioningID
```

## <a name="possible-values"></a><span data-ttu-id="a2f36-106">Valeurs possibles</span><span class="sxs-lookup"><span data-stu-id="a2f36-106">Possible Values</span></span>

<span data-ttu-id="a2f36-107">Cette propriété est une **chaîne** en lecture/écriture.</span><span class="sxs-lookup"><span data-stu-id="a2f36-107">This property is a read/write **String**.</span></span>

## <a name="remarks"></a><span data-ttu-id="a2f36-108">Notes</span><span class="sxs-lookup"><span data-stu-id="a2f36-108">Remarks</span></span>

<span data-ttu-id="a2f36-109">Le nom d’élément spécifié peut être n’importe quel élément HTML dans la page Web, à condition qu’il prenne en charge l’attribut innerHTML.</span><span class="sxs-lookup"><span data-stu-id="a2f36-109">The element name specified can be any HTML element in the webpage as long as it supports the innerHTML attribute.</span></span> <span data-ttu-id="a2f36-110">Si la page Web contient plusieurs frames, le nom de l’élément ne peut faire référence qu’à un élément du même frame que le contrôle du lecteur.</span><span class="sxs-lookup"><span data-stu-id="a2f36-110">If the webpage contains multiple frames, the element name can only refer to an element in the same frame as the Player control.</span></span>

<span data-ttu-id="a2f36-111">**Lecteur Windows Media 10 Mobile :** Cette propriété est en lecture seule et retourne toujours une chaîne vide.</span><span class="sxs-lookup"><span data-stu-id="a2f36-111">**Windows Media Player 10 Mobile:** This property is read only, and always returns an empty string.</span></span>

## <a name="examples"></a><span data-ttu-id="a2f36-112">Exemples</span><span class="sxs-lookup"><span data-stu-id="a2f36-112">Examples</span></span>

<span data-ttu-id="a2f36-113">L’exemple Microsoft JScript suivant utilise *ClosedCaption*. **captioningID** pour choisir la zone d’une page Web utilisée pour afficher les sous-titres.</span><span class="sxs-lookup"><span data-stu-id="a2f36-113">The following Microsoft JScript example uses *ClosedCaption*.**captioningID** to choose the area of a webpage used to display captions.</span></span> <span data-ttu-id="a2f36-114">Deux éléments HTML DIV ont été créés, respectivement avec ID = CC1 et ID = CC2.</span><span class="sxs-lookup"><span data-stu-id="a2f36-114">Two HTML DIV elements were created, with ID = CC1 and ID = CC2, respectively.</span></span> <span data-ttu-id="a2f36-115">L’objet **Player** a été créé avec ID = "Player".</span><span class="sxs-lookup"><span data-stu-id="a2f36-115">The **Player** object was created with ID = "Player".</span></span>


```JScript
<!-- Create two HTML BUTTON elements to allow the user to choose a display region. -->
<INPUT TYPE = "BUTTON"  NAME = "SET1"  VALUE = "Move Caption to CC1"
       OnClick = "
           /* Clear the caption text from the other DIV */
           CC2.innerHTML = 'This is the CC2 DIV';

           /* Show the captions in the DIV named CC1. */ 
           Player.ClosedCaption.captioningID = 'CC1';
          ">

<INPUT TYPE = "BUTTON" NAME = "SET2" VALUE = "Move Caption to CC2"
       OnClick = "
           /* Clear the caption text from the other DIV */
           CC1.innerHTML = 'This is the CC1 DIV';

           /* Show the captions in the DIV named CC2. */
           Player.ClosedCaption.captioningID = 'CC2';
          ">

```



## <a name="requirements"></a><span data-ttu-id="a2f36-116">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="a2f36-116">Requirements</span></span>



| <span data-ttu-id="a2f36-117">Condition requise</span><span class="sxs-lookup"><span data-stu-id="a2f36-117">Requirement</span></span> | <span data-ttu-id="a2f36-118">Valeur</span><span class="sxs-lookup"><span data-stu-id="a2f36-118">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="a2f36-119">Version</span><span class="sxs-lookup"><span data-stu-id="a2f36-119">Version</span></span><br/> | <span data-ttu-id="a2f36-120">Lecteur Windows Media version 7,0 ou ultérieure.</span><span class="sxs-lookup"><span data-stu-id="a2f36-120">Windows Media Player version 7.0 or later.</span></span><br/>                              |
| <span data-ttu-id="a2f36-121">DLL</span><span class="sxs-lookup"><span data-stu-id="a2f36-121">DLL</span></span><br/>     | <dl> <span data-ttu-id="a2f36-122"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="a2f36-122"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a2f36-123">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="a2f36-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a2f36-124">**Ajout de sous-titres à des médias numériques**</span><span class="sxs-lookup"><span data-stu-id="a2f36-124">**Adding Closed Captions to Digital Media**</span></span>](adding-closed-captions-to-digital-media.md)
</dt> <dt>

[<span data-ttu-id="a2f36-125">**Objet ClosedCaption**</span><span class="sxs-lookup"><span data-stu-id="a2f36-125">**ClosedCaption Object**</span></span>](closedcaption-object.md)
</dt> </dl>

 

 





