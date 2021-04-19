---
title: IWMPNetwork propriété bufferingCount
description: La propriété bufferingCount obtient le nombre de fois où la mise en mémoire tampon s’est produite pendant la lecture.
ms.assetid: 2e3a2914-fc38-4477-8c4c-15b4a2e424dc
keywords:
- propriété bufferingCount lecteur Windows Media
- propriété bufferingCount lecteur Windows Media, interface IWMPNetwork
- Interface IWMPNetwork lecteur Windows Media, propriété bufferingCount
topic_type:
- apiref
api_name:
- IWMPNetwork.bufferingCount
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f4958892dd9784ee72b51adfedbbcdee81817b52
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106537395"
---
# <a name="iwmpnetworkbufferingcount-property"></a><span data-ttu-id="85a24-106">IWMPNetwork :: bufferingCount, propriété</span><span class="sxs-lookup"><span data-stu-id="85a24-106">IWMPNetwork::bufferingCount property</span></span>

<span data-ttu-id="85a24-107">La propriété **bufferingCount** obtient le nombre de fois où la mise en mémoire tampon s’est produite pendant la lecture.</span><span class="sxs-lookup"><span data-stu-id="85a24-107">The **bufferingCount** property gets the number of times buffering occurred during playback.</span></span>

## <a name="syntax"></a><span data-ttu-id="85a24-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="85a24-108">Syntax</span></span>


```CSharp
public System.Int32 bufferingCount {get; set;}
```


```VB

Public ReadOnly Property bufferingCount As System.Int32
```





## <a name="property-value"></a><span data-ttu-id="85a24-109">Valeur de la propriété</span><span class="sxs-lookup"><span data-stu-id="85a24-109">Property value</span></span>

<span data-ttu-id="85a24-110">**System. Int32** qui est le nombre de mises en mémoire tampon.</span><span class="sxs-lookup"><span data-stu-id="85a24-110">A **System.Int32** that is the buffering count.</span></span>

## <a name="remarks"></a><span data-ttu-id="85a24-111">Notes</span><span class="sxs-lookup"><span data-stu-id="85a24-111">Remarks</span></span>

<span data-ttu-id="85a24-112">Chaque fois que la lecture est arrêtée et redémarrée, cette propriété est réinitialisée à zéro.</span><span class="sxs-lookup"><span data-stu-id="85a24-112">Each time playback is stopped and restarted, this property is reset to zero.</span></span> <span data-ttu-id="85a24-113">Elle n’est pas réinitialisée si la lecture est suspendue.</span><span class="sxs-lookup"><span data-stu-id="85a24-113">It is not reset if playback is paused.</span></span>

<span data-ttu-id="85a24-114">La mise en mémoire tampon s’applique uniquement au contenu de diffusion en continu.</span><span class="sxs-lookup"><span data-stu-id="85a24-114">Buffering applies only to streaming content.</span></span> <span data-ttu-id="85a24-115">Cette propriété obtient des informations valides uniquement au moment de l’exécution lorsque l’URL pour la lecture est définie à l’aide de la propriété **AxWindowsMediaPlayer. URL** .</span><span class="sxs-lookup"><span data-stu-id="85a24-115">This property gets valid information only during run time when the URL for playback is set by using the **AxWindowsMediaPlayer.URL** property.</span></span>

## <a name="examples"></a><span data-ttu-id="85a24-116">Exemples</span><span class="sxs-lookup"><span data-stu-id="85a24-116">Examples</span></span>

<span data-ttu-id="85a24-117">L’exemple suivant utilise *bufferingCount* pour afficher le nombre de fois que la mise en mémoire tampon se produit pendant la lecture.</span><span class="sxs-lookup"><span data-stu-id="85a24-117">The following example uses *bufferingCount* to display the number of times buffering occurs during playback.</span></span> <span data-ttu-id="85a24-118">Les informations s’affichent dans une étiquette en réponse à l’événement de mise en mémoire tampon.</span><span class="sxs-lookup"><span data-stu-id="85a24-118">The information is displayed in a label in response to the Buffering Event.</span></span> <span data-ttu-id="85a24-119">L’objet **AxWMPLib. AxWindowsMediaPlayer** est représenté par la variable Player.</span><span class="sxs-lookup"><span data-stu-id="85a24-119">The **AxWMPLib.AxWindowsMediaPlayer** object is represented by the variable named player.</span></span>


```CSharp
// Add a delegate for the Buffering event.
player.Buffering += new AxWMPLib._WMPOCXEvents_BufferingEventHandler(player_Buffering);

// Create an event handler for the Buffering event.
private void player_Buffering(object sender, AxWMPLib._WMPOCXEvents_BufferingEvent e)
{
    // Display the bufferingCount when buffering has started.
    if (e.start == true)
    {
        bufferingCountLabel.Text = ("Buffering count: " + player.network.bufferingCount);
    }  
}
```


```VB

' Create an event handler for the Buffering event.
Public Sub player_Buffering(ByVal sender As Object, ByVal e As AxWMPLib._WMPOCXEvents_BufferingEvent) Handles player.Buffering

    &#39; Display the bufferingCount when buffering has started.
    If (e.start = True) Then

        bufferingCountLabel.Text = (&quot;Buffering count: &quot; + player.network.bufferingCount)

    End If

End Sub
```





## <a name="requirements"></a><span data-ttu-id="85a24-120">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="85a24-120">Requirements</span></span>



| <span data-ttu-id="85a24-121">Condition requise</span><span class="sxs-lookup"><span data-stu-id="85a24-121">Requirement</span></span> | <span data-ttu-id="85a24-122">Valeur</span><span class="sxs-lookup"><span data-stu-id="85a24-122">Value</span></span> |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="85a24-123">Version</span><span class="sxs-lookup"><span data-stu-id="85a24-123">Version</span></span><br/>   | <span data-ttu-id="85a24-124">Lecteur Windows Media série 9 ou version ultérieure</span><span class="sxs-lookup"><span data-stu-id="85a24-124">Windows Media Player 9 Series or later</span></span><br/>                                                                      |
| <span data-ttu-id="85a24-125">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="85a24-125">Namespace</span></span><br/> | <span data-ttu-id="85a24-126">**WMPLib**</span><span class="sxs-lookup"><span data-stu-id="85a24-126">**WMPLib**</span></span><br/>                                                                                                  |
| <span data-ttu-id="85a24-127">Assembly</span><span class="sxs-lookup"><span data-stu-id="85a24-127">Assembly</span></span><br/>  | <dl> <span data-ttu-id="85a24-128"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span><span class="sxs-lookup"><span data-stu-id="85a24-128"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="85a24-129">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="85a24-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="85a24-130">**AxWindowsMediaPlayer. URL (VB et C#)**</span><span class="sxs-lookup"><span data-stu-id="85a24-130">**AxWindowsMediaPlayer.URL (VB and C#)**</span></span>](axwmplib-axwindowsmediaplayer-url--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="85a24-131">**Interface IWMPNetwork (VB et C#)**</span><span class="sxs-lookup"><span data-stu-id="85a24-131">**IWMPNetwork Interface (VB and C#)**</span></span>](iwmpnetwork--vb-and-c.md)
</dt> </dl>

 

 





