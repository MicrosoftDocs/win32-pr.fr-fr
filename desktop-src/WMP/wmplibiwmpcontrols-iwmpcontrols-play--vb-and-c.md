---
title: IWMPControls Play, méthode
description: La méthode Play commence la lecture de l’élément multimédia en cours ou reprend la lecture d’un élément suspendu.
ms.assetid: 02e00df6-4dc1-44bb-9826-e69e8298ccaa
keywords:
- Play, méthode lecteur Windows Media
- Play, méthode lecteur Windows Media, interface IWMPControls
- Interface IWMPControls lecteur Windows Media, méthode Play
topic_type:
- apiref
api_name:
- IWMPControls.play
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0fd87a2e2ba3d53b119df328fa68668c91c78d6d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106533215"
---
# <a name="iwmpcontrolsplay-method"></a><span data-ttu-id="9e6c5-106">IWMPControls ::p, méthode</span><span class="sxs-lookup"><span data-stu-id="9e6c5-106">IWMPControls::play method</span></span>

<span data-ttu-id="9e6c5-107">La méthode **Play** commence la lecture de l’élément multimédia en cours ou reprend la lecture d’un élément suspendu.</span><span class="sxs-lookup"><span data-stu-id="9e6c5-107">The **play** method begins playback of the current media item, or resumes playback of a paused item.</span></span>

## <a name="syntax"></a><span data-ttu-id="9e6c5-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="9e6c5-108">Syntax</span></span>


```CSharp
public void play();
```


```VB

Public Sub play()
Implements IWMPControls.play
```





## <a name="parameters"></a><span data-ttu-id="9e6c5-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="9e6c5-109">Parameters</span></span>

<span data-ttu-id="9e6c5-110">Cette méthode n’a aucun paramètre.</span><span class="sxs-lookup"><span data-stu-id="9e6c5-110">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="9e6c5-111">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="9e6c5-111">Return value</span></span>

<span data-ttu-id="9e6c5-112">Cette méthode ne retourne pas de valeur.</span><span class="sxs-lookup"><span data-stu-id="9e6c5-112">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="9e6c5-113">Notes</span><span class="sxs-lookup"><span data-stu-id="9e6c5-113">Remarks</span></span>

<span data-ttu-id="9e6c5-114">Si cette méthode est appelée pendant le transfert rapide ou le rembobinage, la vitesse de lecture (la valeur de **IWMPSettings. rate**) est définie sur 1,0.</span><span class="sxs-lookup"><span data-stu-id="9e6c5-114">If this method is called while fast-forwarding or rewinding, the rate of playback (the value of **IWMPSettings.rate**) is set to 1.0.</span></span>

## <a name="examples"></a><span data-ttu-id="9e6c5-115">Exemples</span><span class="sxs-lookup"><span data-stu-id="9e6c5-115">Examples</span></span>

<span data-ttu-id="9e6c5-116">L’exemple suivant utilise **Play** pour lire l’élément multimédia en cours en réponse à l’événement Click d’un bouton.</span><span class="sxs-lookup"><span data-stu-id="9e6c5-116">The following example uses **play** to play the current media item in response to the Click event of a button.</span></span> <span data-ttu-id="9e6c5-117">L’objet **AxWMPLib. AxWindowsMediaPlayer** est représenté par la variable Player.</span><span class="sxs-lookup"><span data-stu-id="9e6c5-117">The **AxWMPLib.AxWindowsMediaPlayer** object is represented by the variable named player.</span></span>


```CSharp
private void playButton_Click(object o, System.EventArgs args)
{
    // To get all of the available functionality of the player controls, cast the
    // value returned by player.Ctlcontrols to a WMPLib.IWMPControls3 interface. 
    WMPLib.IWMPControls3 controls = (WMPLib.IWMPControls3)player.Ctlcontrols;

    // Check first to be sure the operation is valid. 
    if (controls.get_isAvailable("play"))
    {
        controls.play();
    }
}
```


```VB

Public Sub playButton_Click(ByVal sender As Object, ByVal e As System.EventArgs) Handles playButton.Click

    &#39; To get all of the available functionality of the player controls, Dim the
    &#39; value returned by player.Ctlcontrols as a WMPLib.IWMPControls3 interface.
    Dim controls As WMPLib.IWMPControls3 = player.Ctlcontrols

    &#39; Check first to be sure the operation is valid. 
    If (controls.isAvailable(&quot;play&quot;)) Then

        controls.play()

    End If

End Sub
```





## <a name="requirements"></a><span data-ttu-id="9e6c5-118">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="9e6c5-118">Requirements</span></span>



| <span data-ttu-id="9e6c5-119">Condition requise</span><span class="sxs-lookup"><span data-stu-id="9e6c5-119">Requirement</span></span> | <span data-ttu-id="9e6c5-120">Valeur</span><span class="sxs-lookup"><span data-stu-id="9e6c5-120">Value</span></span> |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9e6c5-121">Version</span><span class="sxs-lookup"><span data-stu-id="9e6c5-121">Version</span></span><br/>   | <span data-ttu-id="9e6c5-122">Lecteur Windows Media série 9 ou version ultérieure</span><span class="sxs-lookup"><span data-stu-id="9e6c5-122">Windows Media Player 9 Series or later</span></span><br/>                                                                      |
| <span data-ttu-id="9e6c5-123">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="9e6c5-123">Namespace</span></span><br/> | <span data-ttu-id="9e6c5-124">**WMPLib**</span><span class="sxs-lookup"><span data-stu-id="9e6c5-124">**WMPLib**</span></span><br/>                                                                                                  |
| <span data-ttu-id="9e6c5-125">Assembly</span><span class="sxs-lookup"><span data-stu-id="9e6c5-125">Assembly</span></span><br/>  | <dl> <span data-ttu-id="9e6c5-126"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span><span class="sxs-lookup"><span data-stu-id="9e6c5-126"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9e6c5-127">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="9e6c5-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9e6c5-128">**Interface IWMPControls (VB et C#)**</span><span class="sxs-lookup"><span data-stu-id="9e6c5-128">**IWMPControls Interface (VB and C#)**</span></span>](iwmpcontrols--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="9e6c5-129">**IWMPControls. playItem (VB et C#)**</span><span class="sxs-lookup"><span data-stu-id="9e6c5-129">**IWMPControls.playItem (VB and C#)**</span></span>](wmplibiwmpcontrols-iwmpcontrols-playitem--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="9e6c5-130">**IWMPSettings. rate (VB et C#)**</span><span class="sxs-lookup"><span data-stu-id="9e6c5-130">**IWMPSettings.rate (VB and C#)**</span></span>](wmplibiwmpsettings-iwmpsettings-rate--vb-and-c.md)
</dt> </dl>

 

 





