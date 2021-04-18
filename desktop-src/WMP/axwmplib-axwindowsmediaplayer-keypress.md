---
title: Événement KeyPress de l’objet AxWindowsMediaPlayer
description: L’événement KeyPress se produit lorsqu’une touche est enfoncée et libérée. | Événement KeyPress de l’objet AxWindowsMediaPlayer
ms.assetid: 73ecd6f9-1b58-4e28-ad1b-2d930a235e1d
keywords:
- Événement KeyPress de l’objet AxWindowsMediaPlayer lecteur Windows Media
topic_type:
- apiref
api_name:
- KeyPress Event of the AxWindowsMediaPlayer Object
api_location:
- AxInterop.WMPLib.dll
api_type:
- Assembly
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c4a01e84b8f765d024c753d08211f3bb84e7f011
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106526832"
---
# <a name="keypress-event-of-the-axwindowsmediaplayer-object"></a><span data-ttu-id="53e30-105">Événement KeyPress de l’objet AxWindowsMediaPlayer</span><span class="sxs-lookup"><span data-stu-id="53e30-105">KeyPress Event of the AxWindowsMediaPlayer Object</span></span>

<span data-ttu-id="53e30-106">L’événement KeyPress se produit lorsqu’une touche est enfoncée et libérée.</span><span class="sxs-lookup"><span data-stu-id="53e30-106">The KeyPress event occurs when a key is pressed and released.</span></span>

``` syntax
[C#]
private void player_KeyPressEvent(
  object sender,
  _WMPOCXEvents_KeyPressEvent e
)

[Visual Basic]
Private Sub player_KeyPressEvent(  
  sender As Object,  
  e As _WMPOCXEvents_KeyPressEvent
) Handles player.KeyPressEvent
```

## <a name="event-data"></a><span data-ttu-id="53e30-107">Données d'événements</span><span class="sxs-lookup"><span data-stu-id="53e30-107">Event Data</span></span>

<span data-ttu-id="53e30-108">Le gestionnaire associé à cet événement est de type **AxWMPLib. \_ WMPOCXEvents \_ KeyPressEventHandler**.</span><span class="sxs-lookup"><span data-stu-id="53e30-108">The handler associated with this event is of type **AxWMPLib.\_WMPOCXEvents\_KeyPressEventHandler**.</span></span> <span data-ttu-id="53e30-109">Ce gestionnaire reçoit un argument de type **AxWMPLib. \_ WMPOCXEvents \_ KeyPressEvent**, qui contient la propriété suivante associée à cet événement.</span><span class="sxs-lookup"><span data-stu-id="53e30-109">This handler receives an argument of type **AxWMPLib.\_WMPOCXEvents\_KeyPressEvent**, which contains the following property related to this event.</span></span>



| <span data-ttu-id="53e30-110">Propriété</span><span class="sxs-lookup"><span data-stu-id="53e30-110">Property</span></span>      | <span data-ttu-id="53e30-111">Description</span><span class="sxs-lookup"><span data-stu-id="53e30-111">Description</span></span>                                                                        |
|---------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="53e30-112">**nKeyAscii**</span><span class="sxs-lookup"><span data-stu-id="53e30-112">**nKeyAscii**</span></span> | <span data-ttu-id="53e30-113">System. Int16Specifies Code ANSI numérique standard pour le caractère.</span><span class="sxs-lookup"><span data-stu-id="53e30-113">System.Int16Specifies the standard numeric ANSI code for the character.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="53e30-114">Notes</span><span class="sxs-lookup"><span data-stu-id="53e30-114">Remarks</span></span>

<span data-ttu-id="53e30-115">Cet événement se produit lorsque la séquence de touches génère un caractère imprimable du clavier, la touche CTRL combinée à un caractère de l’alphabet standard ou l’un des quelques caractères spéciaux, et la touche entrée ou retour arrière.</span><span class="sxs-lookup"><span data-stu-id="53e30-115">This event occurs when the keystroke results in any printable keyboard character, the CTRL key combined with a character from the standard alphabet or one of a few special characters, and the ENTER or BACKSPACE key.</span></span>

## <a name="requirements"></a><span data-ttu-id="53e30-116">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="53e30-116">Requirements</span></span>



| <span data-ttu-id="53e30-117">Condition requise</span><span class="sxs-lookup"><span data-stu-id="53e30-117">Requirement</span></span> | <span data-ttu-id="53e30-118">Valeur</span><span class="sxs-lookup"><span data-stu-id="53e30-118">Value</span></span> |
|----------------------|----------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="53e30-119">Version</span><span class="sxs-lookup"><span data-stu-id="53e30-119">Version</span></span><br/>   | <span data-ttu-id="53e30-120">Lecteur Windows Media série 9 ou version ultérieure</span><span class="sxs-lookup"><span data-stu-id="53e30-120">Windows Media Player 9 Series or later</span></span><br/>                                                                          |
| <span data-ttu-id="53e30-121">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="53e30-121">Namespace</span></span><br/> | <span data-ttu-id="53e30-122">**AxWMPLib**</span><span class="sxs-lookup"><span data-stu-id="53e30-122">**AxWMPLib**</span></span><br/>                                                                                                    |
| <span data-ttu-id="53e30-123">Assembly</span><span class="sxs-lookup"><span data-stu-id="53e30-123">Assembly</span></span><br/>  | <dl> <span data-ttu-id="53e30-124"><dt>AxInterop.WMPLib.dll (AxInterop.WMPLib.dll.dll)</dt></span><span class="sxs-lookup"><span data-stu-id="53e30-124"><dt>AxInterop.WMPLib.dll (AxInterop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="53e30-125">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="53e30-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="53e30-126">**Objet AxWindowsMediaPlayer (VB et C#)**</span><span class="sxs-lookup"><span data-stu-id="53e30-126">**AxWindowsMediaPlayer Object (VB and C#)**</span></span>](axwindowsmediaplayer-object--vb-and-c.md)
</dt> </dl>

 

 





