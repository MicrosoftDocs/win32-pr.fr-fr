---
title: IWMPNetwork propriété sourceProtocol
description: La propriété sourceProtocol obtient le protocole source utilisé pour recevoir des données.
ms.assetid: db1d7651-3f25-4ac9-a3e1-dc3a8ddf8c40
keywords:
- propriété sourceProtocol lecteur Windows Media
- propriété sourceProtocol lecteur Windows Media, interface IWMPNetwork
- Interface IWMPNetwork lecteur Windows Media, propriété sourceProtocol
topic_type:
- apiref
api_name:
- IWMPNetwork.sourceProtocol
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a5017e1a053c124a1f7f50668c6f392eb541d57f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106543344"
---
# <a name="iwmpnetworksourceprotocol-property"></a><span data-ttu-id="89425-106">IWMPNetwork :: sourceProtocol, propriété</span><span class="sxs-lookup"><span data-stu-id="89425-106">IWMPNetwork::sourceProtocol property</span></span>

<span data-ttu-id="89425-107">La propriété **sourceProtocol** obtient le protocole source utilisé pour recevoir des données.</span><span class="sxs-lookup"><span data-stu-id="89425-107">The **sourceProtocol** property gets the source protocol used to receive data.</span></span>

## <a name="syntax"></a><span data-ttu-id="89425-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="89425-108">Syntax</span></span>


```CSharp
public System.String sourceProtocol {get; set;}
```


```VB

Public ReadOnly Property sourceProtocol As System.String
```





## <a name="property-value"></a><span data-ttu-id="89425-109">Valeur de la propriété</span><span class="sxs-lookup"><span data-stu-id="89425-109">Property value</span></span>

<span data-ttu-id="89425-110">**System. String** qui est le nom du protocole source.</span><span class="sxs-lookup"><span data-stu-id="89425-110">A **System.String** that is the name of the source protocol.</span></span>

## <a name="remarks"></a><span data-ttu-id="89425-111">Notes</span><span class="sxs-lookup"><span data-stu-id="89425-111">Remarks</span></span>

<span data-ttu-id="89425-112">Cette propriété obtient une chaîne de longueur nulle ("") lors de la diffusion d’un CD ou d’un DVD.</span><span class="sxs-lookup"><span data-stu-id="89425-112">This property gets a zero-length string ("") when playing a CD or DVD.</span></span>

## <a name="examples"></a><span data-ttu-id="89425-113">Exemples</span><span class="sxs-lookup"><span data-stu-id="89425-113">Examples</span></span>

<span data-ttu-id="89425-114">L’exemple de code suivant utilise **sourceProtocol** pour afficher le protocole source utilisé pour recevoir des données.</span><span class="sxs-lookup"><span data-stu-id="89425-114">The following code example uses **sourceProtocol** to display the source protocol used to receive data.</span></span> <span data-ttu-id="89425-115">Les informations s’affichent dans une étiquette, en réponse à l’événement **PlayStateChange** .</span><span class="sxs-lookup"><span data-stu-id="89425-115">The information is displayed in a label, in response to the **PlayStateChange** Event.</span></span> <span data-ttu-id="89425-116">L’objet **AxWMPLib. AxWindowsMediaPlayer** est représenté par la variable Player.</span><span class="sxs-lookup"><span data-stu-id="89425-116">The **AxWMPLib.AxWindowsMediaPlayer** object is represented by the variable named player.</span></span>


```CSharp
// Add a delegate for the PlayStateChange event.
player.PlayStateChange += new AxWMPLib._WMPOCXEvents_PlayStateChangeEventHandler(player_PlayStateChange);

// Create an event handler for the PlayStateChange event.
private void player_PlayStateChange(object sender, AxWMPLib._WMPOCXEvents_PlayStateChangeEvent e)
{
    // Display the network source protocol when the player is playing by testing for a 
    // play state enum value of WMPLib.WMPPlayState.wmppsPlaying which equals 3. 
    if (e.newState == 3) 
    {
        sourceProtocolLabel.Text = ("Source protocol: " + player.network.sourceProtocol);
    } 
}
```


```VB

' Create an event handler for the PlayStateChange event.
Public Sub player_PlayStateChange(ByVal sender As Object, ByVal e As AxWMPLib._WMPOCXEvents_PlayStateChangeEvent) Handles player.PlayStateChange

    &#39; Display the network source protocol when the player is playing by testing for a 
    &#39; play state enum value of WMPLib.WMPPlayState.wmppsPlaying which equals 3.
    If (e.newState = 3) Then

        sourceProtocolLabel.Text = (&quot;Source protocol: &quot; + player.network.sourceProtocol)

    End If

End Sub
```





## <a name="requirements"></a><span data-ttu-id="89425-117">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="89425-117">Requirements</span></span>



| <span data-ttu-id="89425-118">Condition requise</span><span class="sxs-lookup"><span data-stu-id="89425-118">Requirement</span></span> | <span data-ttu-id="89425-119">Valeur</span><span class="sxs-lookup"><span data-stu-id="89425-119">Value</span></span> |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="89425-120">Version</span><span class="sxs-lookup"><span data-stu-id="89425-120">Version</span></span><br/>   | <span data-ttu-id="89425-121">Lecteur Windows Media série 9 ou version ultérieure</span><span class="sxs-lookup"><span data-stu-id="89425-121">Windows Media Player 9 Series or later</span></span><br/>                                                                      |
| <span data-ttu-id="89425-122">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="89425-122">Namespace</span></span><br/> | <span data-ttu-id="89425-123">**WMPLib**</span><span class="sxs-lookup"><span data-stu-id="89425-123">**WMPLib**</span></span><br/>                                                                                                  |
| <span data-ttu-id="89425-124">Assembly</span><span class="sxs-lookup"><span data-stu-id="89425-124">Assembly</span></span><br/>  | <dl> <span data-ttu-id="89425-125"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span><span class="sxs-lookup"><span data-stu-id="89425-125"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="89425-126">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="89425-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="89425-127">**Interface IWMPNetwork (VB et C#)**</span><span class="sxs-lookup"><span data-stu-id="89425-127">**IWMPNetwork Interface (VB and C#)**</span></span>](iwmpnetwork--vb-and-c.md)
</dt> </dl>

 

 





