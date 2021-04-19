---
title: Méthode IWMPControls fastForward
description: La méthode fastForward démarre la lecture rapide de l’élément multimédia dans le sens avant. | Méthode IWMPControls fastForward
ms.assetid: 44609d63-1d1a-489c-ac17-60b6d3ddc588
keywords:
- méthode fastForward lecteur Windows Media
- méthode fastForward lecteur Windows Media, interface IWMPControls
- Interface IWMPControls lecteur Windows Media, méthode fastForward
topic_type:
- apiref
api_name:
- IWMPControls.fastForward
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a1d99307a7b188b238157af62833273b8c724eab
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106542745"
---
# <a name="iwmpcontrolsfastforward-method"></a><span data-ttu-id="2af32-107">IWMPControls :: fastForward, méthode</span><span class="sxs-lookup"><span data-stu-id="2af32-107">IWMPControls::fastForward method</span></span>

<span data-ttu-id="2af32-108">La méthode **fastForward** démarre la lecture rapide de l’élément multimédia dans le sens avant.</span><span class="sxs-lookup"><span data-stu-id="2af32-108">The **fastForward** method starts fast play of the media item in the forward direction.</span></span>

## <a name="syntax"></a><span data-ttu-id="2af32-109">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="2af32-109">Syntax</span></span>


```CSharp
public void fastForward();
```


```VB

Public Sub fastForward()
Implements IWMPControls.fastForward
```





## <a name="parameters"></a><span data-ttu-id="2af32-110">Paramètres</span><span class="sxs-lookup"><span data-stu-id="2af32-110">Parameters</span></span>

<span data-ttu-id="2af32-111">Cette méthode n’a aucun paramètre.</span><span class="sxs-lookup"><span data-stu-id="2af32-111">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="2af32-112">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="2af32-112">Return value</span></span>

<span data-ttu-id="2af32-113">Cette méthode ne retourne pas de valeur.</span><span class="sxs-lookup"><span data-stu-id="2af32-113">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="2af32-114">Notes</span><span class="sxs-lookup"><span data-stu-id="2af32-114">Remarks</span></span>

<span data-ttu-id="2af32-115">La méthode **fastForward** lit le clip à cinq fois la vitesse normale.</span><span class="sxs-lookup"><span data-stu-id="2af32-115">The **fastForward** method plays the clip at five times the normal speed.</span></span> <span data-ttu-id="2af32-116">L’appel de **fastForward** équivaut à spécifier 5,0 pour le taux en définissant la propriété **IWMPSettings. rate** .</span><span class="sxs-lookup"><span data-stu-id="2af32-116">Calling **fastForward** is equivalent to specifying 5.0 for the rate by setting the **IWMPSettings.rate** property.</span></span> <span data-ttu-id="2af32-117">Si la fréquence est modifiée par la suite ou si **IWMPControls. Play** ou **IWMPControls. Stop** est appelé, le lecteur Windows Media arrête le transfert rapide.</span><span class="sxs-lookup"><span data-stu-id="2af32-117">If the rate is subsequently changed, or if **IWMPControls.play** or **IWMPControls.stop** is called, Windows Media Player will cease fast forwarding.</span></span>

<span data-ttu-id="2af32-118">La méthode **fastForward** ne fonctionne pas pour les diffusions en direct et certains types de média.</span><span class="sxs-lookup"><span data-stu-id="2af32-118">The **fastForward** method does not work for live broadcasts and certain media types.</span></span> <span data-ttu-id="2af32-119">Pour déterminer si vous pouvez avancer rapidement dans un clip, transmettez la valeur **System. String** « Fastforward » à la propriété **IWMPControls. IsAvailable** (méthode **IWMPControls. obtenir \_ isAvailable** en C#).</span><span class="sxs-lookup"><span data-stu-id="2af32-119">To determine whether you can fast forward in a clip, pass the **System.String** value "FastForward" to the **IWMPControls.isAvailable** property (the **IWMPControls.get\_isAvailable** method in C#).</span></span>

## <a name="examples"></a><span data-ttu-id="2af32-120">Exemples</span><span class="sxs-lookup"><span data-stu-id="2af32-120">Examples</span></span>

<span data-ttu-id="2af32-121">L’exemple suivant utilise **fastForward** pour avancer rapidement l’élément multimédia actuel en réponse à l’événement Click d’un bouton.</span><span class="sxs-lookup"><span data-stu-id="2af32-121">The following example uses **fastForward** to fast-forward the current media item in response to the Click event of a button.</span></span> <span data-ttu-id="2af32-122">L’objet **AxWMPLib. AxWindowsMediaPlayer** est représenté par la variable Player.</span><span class="sxs-lookup"><span data-stu-id="2af32-122">The **AxWMPLib.AxWindowsMediaPlayer** object is represented by the variable named player.</span></span>


```CSharp
private void fastForwardButton_Click(object o, System.EventArgs args)
{
    // To get all of the available functionality of the player controls, cast the
    // value returned by player.Ctlcontrols to a WMPLib.IWMPControls3 interface. 
    WMPLib.IWMPControls3 controls = (WMPLib.IWMPControls3)player.Ctlcontrols;

    // Check first to be sure the operation is valid.
    if (controls.get_isAvailable("fastForward"))
    {
        controls.fastForward();
    }
}
```


```VB

Public Sub fastForwardButton_Click(ByVal sender As Object, ByVal e As System.EventArgs) Handles fastForwardButton.Click

    &#39; To get all of the available functionality of the player controls, Dim the
    &#39; value returned by player.Ctlcontrols as a WMPLib.IWMPControls3 interface. 
    Dim controls As WMPLib.IWMPControls3 = player.Ctlcontrols

    &#39; Check first to be sure the operation is valid.
    If (controls.isAvailable(&quot;fastForward&quot;)) Then

        controls.fastForward()

    End If

End Sub
```





## <a name="requirements"></a><span data-ttu-id="2af32-123">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="2af32-123">Requirements</span></span>



| <span data-ttu-id="2af32-124">Condition requise</span><span class="sxs-lookup"><span data-stu-id="2af32-124">Requirement</span></span> | <span data-ttu-id="2af32-125">Valeur</span><span class="sxs-lookup"><span data-stu-id="2af32-125">Value</span></span> |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2af32-126">Version</span><span class="sxs-lookup"><span data-stu-id="2af32-126">Version</span></span><br/>   | <span data-ttu-id="2af32-127">Lecteur Windows Media série 9 ou version ultérieure</span><span class="sxs-lookup"><span data-stu-id="2af32-127">Windows Media Player 9 Series or later</span></span><br/>                                                                      |
| <span data-ttu-id="2af32-128">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="2af32-128">Namespace</span></span><br/> | <span data-ttu-id="2af32-129">**WMPLib**</span><span class="sxs-lookup"><span data-stu-id="2af32-129">**WMPLib**</span></span><br/>                                                                                                  |
| <span data-ttu-id="2af32-130">Assembly</span><span class="sxs-lookup"><span data-stu-id="2af32-130">Assembly</span></span><br/>  | <dl> <span data-ttu-id="2af32-131"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span><span class="sxs-lookup"><span data-stu-id="2af32-131"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2af32-132">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="2af32-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2af32-133">**Interface IWMPControls (VB et C#)**</span><span class="sxs-lookup"><span data-stu-id="2af32-133">**IWMPControls Interface (VB and C#)**</span></span>](iwmpcontrols--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="2af32-134">**IWMPControls. isAvailable (VB et C#)**</span><span class="sxs-lookup"><span data-stu-id="2af32-134">**IWMPControls.isAvailable (VB and C#)**</span></span>](iwmpcontrols-isavailable--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="2af32-135">**IWMPControls. Play (VB et C#)**</span><span class="sxs-lookup"><span data-stu-id="2af32-135">**IWMPControls.play (VB and C#)**</span></span>](wmplibiwmpcontrols-iwmpcontrols-play--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="2af32-136">**IWMPControls. Stop (VB et C#)**</span><span class="sxs-lookup"><span data-stu-id="2af32-136">**IWMPControls.stop (VB and C#)**</span></span>](wmplibiwmpcontrols-iwmpcontrols-stop--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="2af32-137">**IWMPSettings. rate (VB et C#)**</span><span class="sxs-lookup"><span data-stu-id="2af32-137">**IWMPSettings.rate (VB and C#)**</span></span>](wmplibiwmpsettings-iwmpsettings-rate--vb-and-c.md)
</dt> </dl>

 

 





