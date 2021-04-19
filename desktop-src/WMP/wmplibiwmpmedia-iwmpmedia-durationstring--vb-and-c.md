---
title: IWMPMedia propriété durationString
description: La propriété durationString obtient une chaîne indiquant la durée de l’élément multimédia actuel au format HH MM SS.
ms.assetid: de33c737-d73e-41f0-9c1b-944279194738
keywords:
- propriété durationString lecteur Windows Media
- propriété durationString lecteur Windows Media, interface IWMPMedia
- Interface IWMPMedia lecteur Windows Media, propriété durationString
topic_type:
- apiref
api_name:
- IWMPMedia.durationString
- IWMPMedia.get_durationString
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c9e6bc732388036aa9e79aeedd988de94fa263bf
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106529996"
---
# <a name="iwmpmediadurationstring-property"></a><span data-ttu-id="a2b76-106">IWMPMedia ::d propriété urationString</span><span class="sxs-lookup"><span data-stu-id="a2b76-106">IWMPMedia::durationString property</span></span>

<span data-ttu-id="a2b76-107">La propriété **durationString** obtient une chaîne indiquant la durée de l’élément multimédia actuel au format hh : mm : SS.</span><span class="sxs-lookup"><span data-stu-id="a2b76-107">The **durationString** property gets a string indicating the duration of the current media item in HH:MM:SS format.</span></span>

<span data-ttu-id="a2b76-108">Cette propriété est en lecture seule.</span><span class="sxs-lookup"><span data-stu-id="a2b76-108">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="a2b76-109">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="a2b76-109">Syntax</span></span>


```CSharp
public System.String durationString {get;}
```


```VB

Public ReadOnly Property durationString As System.String
```





## <a name="property-value"></a><span data-ttu-id="a2b76-110">Valeur de la propriété</span><span class="sxs-lookup"><span data-stu-id="a2b76-110">Property value</span></span>

<span data-ttu-id="a2b76-111">**System. String** qui correspond à la durée.</span><span class="sxs-lookup"><span data-stu-id="a2b76-111">A **System.String** that is the duration.</span></span>

## <a name="remarks"></a><span data-ttu-id="a2b76-112">Notes</span><span class="sxs-lookup"><span data-stu-id="a2b76-112">Remarks</span></span>

<span data-ttu-id="a2b76-113">Si cette propriété est utilisée avec un élément multimédia autre que celui spécifié dans AxWindowsMediaPlayer. currentMedia, elle ne peut pas contenir de valeur valide.</span><span class="sxs-lookup"><span data-stu-id="a2b76-113">If this property is used with a media item other than the one specified in AxWindowsMediaPlayer.currentMedia, it may not contain a valid value.</span></span> <span data-ttu-id="a2b76-114">Si l’élément multimédia est inférieur à une heure, la partie heures de la valeur de retour est omise.</span><span class="sxs-lookup"><span data-stu-id="a2b76-114">If the media item is less than an hour long, the hours portion of the return value is omitted.</span></span>

<span data-ttu-id="a2b76-115">Avant d’utiliser cette propriété, vous devez disposer d’un accès en lecture à la bibliothèque.</span><span class="sxs-lookup"><span data-stu-id="a2b76-115">Before using this property, you must have read access to the library.</span></span> <span data-ttu-id="a2b76-116">Pour plus d’informations, consultez [accès à la bibliothèque](library-access.md).</span><span class="sxs-lookup"><span data-stu-id="a2b76-116">For more information, see [Library Access](library-access.md).</span></span>

## <a name="examples"></a><span data-ttu-id="a2b76-117">Exemples</span><span class="sxs-lookup"><span data-stu-id="a2b76-117">Examples</span></span>

<span data-ttu-id="a2b76-118">L’exemple suivant utilise **durationString** pour afficher la durée de l’élément multimédia actuel comme texte mis en forme dans une étiquette.</span><span class="sxs-lookup"><span data-stu-id="a2b76-118">The following example uses **durationString** to display the duration of the current media item as formatted text in a label.</span></span> <span data-ttu-id="a2b76-119">L’objet **AxWMPLib. AxWindowsMediaPlayer** est représenté par la variable Player.</span><span class="sxs-lookup"><span data-stu-id="a2b76-119">The **AxWMPLib.AxWindowsMediaPlayer** object is represented by the variable named player.</span></span>


```CSharp
// Create an event handler for the OpenStateChange event.
private void player_OpenStateChange(object sender, AxWMPLib._WMPOCXEvents_OpenStateChangeEvent e)
{
    // Test whether the current media item is open.
    if (e.newState == (int)WMPLib.WMPOpenState.wmposMediaOpen)
    {
         // Display the formatted duration string in the label.
         mediaDuration.Text = player.currentMedia.durationString;
    }
}
```


```VB

' Create an event handler for the OpenStateChange event.
Public Sub player_OpenStateChange(ByVal sender As Object, ByVal e As AxWMPLib._WMPOCXEvents_OpenStateChangeEvent) Handles player.OpenStateChange

    &#39; Test whether the current media item is open.
    If (e.newState = 13) Then

        &#39; Display the formatted duration string in the label.
        mediaDuration.Text = player.currentMedia.durationString

    End If

End Sub
```





## <a name="requirements"></a><span data-ttu-id="a2b76-120">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="a2b76-120">Requirements</span></span>



| <span data-ttu-id="a2b76-121">Condition requise</span><span class="sxs-lookup"><span data-stu-id="a2b76-121">Requirement</span></span> | <span data-ttu-id="a2b76-122">Valeur</span><span class="sxs-lookup"><span data-stu-id="a2b76-122">Value</span></span> |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a2b76-123">Version</span><span class="sxs-lookup"><span data-stu-id="a2b76-123">Version</span></span><br/>   | <span data-ttu-id="a2b76-124">Lecteur Windows Media série 9 ou version ultérieure</span><span class="sxs-lookup"><span data-stu-id="a2b76-124">Windows Media Player 9 Series or later</span></span><br/>                                                                      |
| <span data-ttu-id="a2b76-125">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="a2b76-125">Namespace</span></span><br/> | <span data-ttu-id="a2b76-126">**WMPLib**</span><span class="sxs-lookup"><span data-stu-id="a2b76-126">**WMPLib**</span></span><br/>                                                                                                  |
| <span data-ttu-id="a2b76-127">Assembly</span><span class="sxs-lookup"><span data-stu-id="a2b76-127">Assembly</span></span><br/>  | <dl> <span data-ttu-id="a2b76-128"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span><span class="sxs-lookup"><span data-stu-id="a2b76-128"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a2b76-129">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="a2b76-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a2b76-130">**AxWindowsMediaPlayer. currentMedia (VB et C#)**</span><span class="sxs-lookup"><span data-stu-id="a2b76-130">**AxWindowsMediaPlayer.currentMedia (VB and C#)**</span></span>](axwmplib-axwindowsmediaplayer-currentmedia--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="a2b76-131">**Interface IWMPMedia (VB et C#)**</span><span class="sxs-lookup"><span data-stu-id="a2b76-131">**IWMPMedia Interface (VB and C#)**</span></span>](iwmpmedia--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="a2b76-132">**IWMPMedia. Duration (VB et C#)**</span><span class="sxs-lookup"><span data-stu-id="a2b76-132">**IWMPMedia.duration (VB and C#)**</span></span>](wmplibiwmpmedia-iwmpmedia-duration--vb-and-c.md)
</dt> </dl>

 

 





