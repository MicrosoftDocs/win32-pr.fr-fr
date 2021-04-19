---
title: Méthode IWMPControls fastReverse
description: La méthode fastReverse démarre la lecture rapide de l’élément multimédia dans le sens inverse.
ms.assetid: 5c872e8d-2ffc-425f-a4dd-938ddd1426e0
keywords:
- méthode fastReverse lecteur Windows Media
- méthode fastReverse lecteur Windows Media, interface IWMPControls
- Interface IWMPControls lecteur Windows Media, méthode fastReverse
topic_type:
- apiref
api_name:
- IWMPControls.fastReverse
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7061481aea13b0ed83c3a3d0eb47ca24b940358b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106541486"
---
# <a name="iwmpcontrolsfastreverse-method"></a><span data-ttu-id="5d8c8-106">IWMPControls :: fastReverse, méthode</span><span class="sxs-lookup"><span data-stu-id="5d8c8-106">IWMPControls::fastReverse method</span></span>

<span data-ttu-id="5d8c8-107">La méthode **fastReverse** démarre la lecture rapide de l’élément multimédia dans le sens inverse.</span><span class="sxs-lookup"><span data-stu-id="5d8c8-107">The **fastReverse** method starts fast play of the media item in the reverse direction.</span></span>

## <a name="syntax"></a><span data-ttu-id="5d8c8-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="5d8c8-108">Syntax</span></span>


```CSharp
public void fastReverse();
```


```VB

Public Sub fastReverse()
Implements IWMPControls.fastReverse
```





## <a name="parameters"></a><span data-ttu-id="5d8c8-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="5d8c8-109">Parameters</span></span>

<span data-ttu-id="5d8c8-110">Cette méthode n’a aucun paramètre.</span><span class="sxs-lookup"><span data-stu-id="5d8c8-110">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="5d8c8-111">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="5d8c8-111">Return value</span></span>

<span data-ttu-id="5d8c8-112">Cette méthode ne retourne pas de valeur.</span><span class="sxs-lookup"><span data-stu-id="5d8c8-112">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="5d8c8-113">Notes</span><span class="sxs-lookup"><span data-stu-id="5d8c8-113">Remarks</span></span>

<span data-ttu-id="5d8c8-114">La méthode **fastReverse** analyse le clip en sens inverse à cinq fois la vitesse normale, en affichant uniquement les images clés s’il s’agit d’un fichier vidéo.</span><span class="sxs-lookup"><span data-stu-id="5d8c8-114">The **fastReverse** method scans the clip in reverse at five times the normal speed, displaying only the key frames if it is a video file.</span></span> <span data-ttu-id="5d8c8-115">L’appel de **fastReverse** équivaut à spécifier-5,0 pour le taux en définissant la propriété **IWMPSettings. rate** .</span><span class="sxs-lookup"><span data-stu-id="5d8c8-115">Calling **fastReverse** is equivalent to specifying -5.0 for the rate by setting the **IWMPSettings.rate** property.</span></span> <span data-ttu-id="5d8c8-116">Si la fréquence est modifiée par la suite, ou si **IWMPControls. Play** ou **IWMPControls. Stop** est appelé, le lecteur Windows Media arrête rapidement l’opération inverse.</span><span class="sxs-lookup"><span data-stu-id="5d8c8-116">If the rate is subsequently changed, or if **IWMPControls.play** or **IWMPControls.stop** is called, Windows Media Player will cease fast reverse.</span></span>

<span data-ttu-id="5d8c8-117">Si l’élément fait partie d’une sélection, **fastReverse** s’arrête au début de la piste actuelle. Par exemple, si Track 3 se trouve dans **fastReverse**, lorsque le début de la piste 3 est atteint, le lecteur Windows Media ne passe pas à Track 2.</span><span class="sxs-lookup"><span data-stu-id="5d8c8-117">If the item is part of a playlist, **fastReverse** stops at the beginning of the current track. For instance, if track 3 is in **fastReverse**, when the beginning of track 3 is reached, Windows Media Player will not go to track 2.</span></span> <span data-ttu-id="5d8c8-118">Le nombre de lecture n’est pas incrémenté lors de l’appel de **fastReverse**.</span><span class="sxs-lookup"><span data-stu-id="5d8c8-118">The play count is not incremented when calling **fastReverse**.</span></span>

<span data-ttu-id="5d8c8-119">Si vous appelez **IWMPControls. fastForward** alors que **fastReverse** est en cours d’exécution, **fastReverse** sera arrêté et **IWMPControls. fastForward** démarrera.</span><span class="sxs-lookup"><span data-stu-id="5d8c8-119">If you call **IWMPControls.fastForward** while **fastReverse** is running, **fastReverse** will be stopped and **IWMPControls.fastForward** will begin.</span></span>

<span data-ttu-id="5d8c8-120">Cette méthode ne fonctionne pas pour les diffusions en direct et certains types de médias numériques.</span><span class="sxs-lookup"><span data-stu-id="5d8c8-120">This method does not work for live broadcasts and certain digital media types.</span></span> <span data-ttu-id="5d8c8-121">Pour déterminer si vous pouvez utiliser l’inverse rapide dans un clip, transmettez la valeur **System. String** « FastReverse » à la propriété **IWMPControls. IsAvailable** (méthode **IWMPControls. obtenir \_ isAvailable** en C#).</span><span class="sxs-lookup"><span data-stu-id="5d8c8-121">To determine whether you can use fast reverse in a clip, pass the **System.String** value "FastReverse" to the **IWMPControls.isAvailable** property (the **IWMPControls.get\_isAvailable** method in C#).</span></span>

## <a name="examples"></a><span data-ttu-id="5d8c8-122">Exemples</span><span class="sxs-lookup"><span data-stu-id="5d8c8-122">Examples</span></span>

<span data-ttu-id="5d8c8-123">L’exemple suivant utilise **fastReverse** pour inverser l’élément multimédia en cours en réponse à l’événement Click d’un bouton.</span><span class="sxs-lookup"><span data-stu-id="5d8c8-123">The following example uses **fastReverse** to reverse the current media item in response to the Click event of a button.</span></span> <span data-ttu-id="5d8c8-124">L’objet **AxWMPLib. AxWindowsMediaPlayer** est représenté par la variable Player.</span><span class="sxs-lookup"><span data-stu-id="5d8c8-124">The **AxWMPLib.AxWindowsMediaPlayer** object is represented by the variable named player.</span></span>


```CSharp
private void fastReverseButton_Click(object o, System.EventArgs args)
{
    // To get all of the available functionality of the player controls, cast the
    // value returned by player.Ctlcontrols to a WMPLib.IWMPControls3 interface. 
    WMPLib.IWMPControls3 controls = (WMPLib.IWMPControls3)player.Ctlcontrols;

    // Check first to be sure the operation is valid.
    if (controls.get_isAvailable("fastReverse"))
    {
        controls.fastReverse();
    }
}
```


```VB

Public Sub fastReverseButton_Click(ByVal sender As Object, ByVal e As System.EventArgs) Handles fastReverseButton.Click

    &#39; To get all of the available functionality of the player controls, Dim the
    &#39; value returned by player.Ctlcontrols as a WMPLib.IWMPControls3 interface.
    Dim controls As WMPLib.IWMPControls3 = player.Ctlcontrols

    &#39; Check first to be sure the operation is valid.
    If (controls.isAvailable(&quot;fastReverse&quot;)) Then

        controls.fastReverse()

    End If

End Sub
```





## <a name="requirements"></a><span data-ttu-id="5d8c8-125">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="5d8c8-125">Requirements</span></span>



| <span data-ttu-id="5d8c8-126">Condition requise</span><span class="sxs-lookup"><span data-stu-id="5d8c8-126">Requirement</span></span> | <span data-ttu-id="5d8c8-127">Valeur</span><span class="sxs-lookup"><span data-stu-id="5d8c8-127">Value</span></span> |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5d8c8-128">Version</span><span class="sxs-lookup"><span data-stu-id="5d8c8-128">Version</span></span><br/>   | <span data-ttu-id="5d8c8-129">Lecteur Windows Media série 9 ou version ultérieure</span><span class="sxs-lookup"><span data-stu-id="5d8c8-129">Windows Media Player 9 Series or later</span></span><br/>                                                                      |
| <span data-ttu-id="5d8c8-130">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="5d8c8-130">Namespace</span></span><br/> | <span data-ttu-id="5d8c8-131">**WMPLib**</span><span class="sxs-lookup"><span data-stu-id="5d8c8-131">**WMPLib**</span></span><br/>                                                                                                  |
| <span data-ttu-id="5d8c8-132">Assembly</span><span class="sxs-lookup"><span data-stu-id="5d8c8-132">Assembly</span></span><br/>  | <dl> <span data-ttu-id="5d8c8-133"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span><span class="sxs-lookup"><span data-stu-id="5d8c8-133"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5d8c8-134">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="5d8c8-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5d8c8-135">**Interface IWMPControls (VB et C#)**</span><span class="sxs-lookup"><span data-stu-id="5d8c8-135">**IWMPControls Interface (VB and C#)**</span></span>](iwmpcontrols--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="5d8c8-136">**IWMPControls. fastForward (VB et C#)**</span><span class="sxs-lookup"><span data-stu-id="5d8c8-136">**IWMPControls.fastForward (VB and C#)**</span></span>](wmplibiwmpcontrols-iwmpcontrols-fastforward--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="5d8c8-137">**IWMPControls. isAvailable (VB et C#)**</span><span class="sxs-lookup"><span data-stu-id="5d8c8-137">**IWMPControls.isAvailable (VB and C#)**</span></span>](iwmpcontrols-isavailable--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="5d8c8-138">**IWMPControls. Play (VB et C#)**</span><span class="sxs-lookup"><span data-stu-id="5d8c8-138">**IWMPControls.play (VB and C#)**</span></span>](wmplibiwmpcontrols-iwmpcontrols-play--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="5d8c8-139">**IWMPControls. Stop (VB et C#)**</span><span class="sxs-lookup"><span data-stu-id="5d8c8-139">**IWMPControls.stop (VB and C#)**</span></span>](wmplibiwmpcontrols-iwmpcontrols-stop--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="5d8c8-140">**IWMPSettings. rate (VB et C#)**</span><span class="sxs-lookup"><span data-stu-id="5d8c8-140">**IWMPSettings.rate (VB and C#)**</span></span>](wmplibiwmpsettings-iwmpsettings-rate--vb-and-c.md)
</dt> </dl>

 

 





