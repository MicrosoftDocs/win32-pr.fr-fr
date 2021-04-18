---
title: IWMPControls pause, méthode
description: La méthode pause interrompt la lecture de l’élément multimédia. | IWMPControls pause, méthode
ms.assetid: 1d9ebaf3-84b4-458d-a393-2b685cd0dbfb
keywords:
- méthode pause lecteur Windows Media
- méthode pause lecteur Windows Media, interface IWMPControls
- Interface IWMPControls lecteur Windows Media, pause, méthode
topic_type:
- apiref
api_name:
- IWMPControls.pause
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5cf89cfef66c84be76a529d9c0cef6ec3ae6ac40
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106526651"
---
# <a name="iwmpcontrolspause-method"></a><span data-ttu-id="87c7a-107">IWMPControls ::p méthode ause</span><span class="sxs-lookup"><span data-stu-id="87c7a-107">IWMPControls::pause method</span></span>

<span data-ttu-id="87c7a-108">La méthode **Pause** interrompt la lecture de l’élément multimédia.</span><span class="sxs-lookup"><span data-stu-id="87c7a-108">The **pause** method pauses playback of the media item.</span></span>

## <a name="syntax"></a><span data-ttu-id="87c7a-109">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="87c7a-109">Syntax</span></span>


```CSharp
public void pause();
```


```VB

Public Sub pause()
Implements IWMPControls.pause
```





## <a name="parameters"></a><span data-ttu-id="87c7a-110">Paramètres</span><span class="sxs-lookup"><span data-stu-id="87c7a-110">Parameters</span></span>

<span data-ttu-id="87c7a-111">Cette méthode n’a aucun paramètre.</span><span class="sxs-lookup"><span data-stu-id="87c7a-111">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="87c7a-112">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="87c7a-112">Return value</span></span>

<span data-ttu-id="87c7a-113">Cette méthode ne retourne pas de valeur.</span><span class="sxs-lookup"><span data-stu-id="87c7a-113">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="87c7a-114">Notes</span><span class="sxs-lookup"><span data-stu-id="87c7a-114">Remarks</span></span>

<span data-ttu-id="87c7a-115">Lorsqu’un fichier est en pause, le lecteur Windows Media n’accorde aucune ressource système, telle que le périphérique audio.</span><span class="sxs-lookup"><span data-stu-id="87c7a-115">When a file is paused, Windows Media Player does not give up any system resources, such as the audio device.</span></span>

<span data-ttu-id="87c7a-116">Pour déterminer si un type de média particulier peut être suspendu, transmettez la valeur **System. String** « pause » à la propriété **IWMPControls. IsAvailable** (méthode **IWMPControls. obtenir \_ isAvailable** en C#).</span><span class="sxs-lookup"><span data-stu-id="87c7a-116">To determine whether a particular media type can be paused, pass the **System.String** value "pause" to the **IWMPControls.isAvailable** property (the **IWMPControls.get\_isAvailable** method in C#).</span></span>

## <a name="examples"></a><span data-ttu-id="87c7a-117">Exemples</span><span class="sxs-lookup"><span data-stu-id="87c7a-117">Examples</span></span>

<span data-ttu-id="87c7a-118">L’exemple suivant utilise la fonction **Pause** pour suspendre la lecture de l’élément multimédia en cours en réponse à l’événement Click d’un bouton.</span><span class="sxs-lookup"><span data-stu-id="87c7a-118">The following example uses **pause** to pause playback of the current media item in response to the Click event of a button.</span></span> <span data-ttu-id="87c7a-119">L’objet **AxWMPLib. AxWindowsMediaPlayer** est représenté par la variable Player.</span><span class="sxs-lookup"><span data-stu-id="87c7a-119">The **AxWMPLib.AxWindowsMediaPlayer** object is represented by the variable named player.</span></span>


```CSharp
private void pauseButton_Click(object o, System.EventArgs args)
{
    // To get all of the available functionality of the player controls, cast the
    // value returned by player.Ctlcontrols to a WMPLib.IWMPControls3 interface. 
    WMPLib.IWMPControls3 controls = (WMPLib.IWMPControls3)player.Ctlcontrols;

    // Check first to be sure the operation is valid. 
    if (controls.get_isAvailable("pause"))
    {
        controls.pause();
    }
}
```


```VB

Public Sub pauseButton_Click(ByVal sender As Object, ByVal e As System.EventArgs) Handles pauseButton.Click

    &#39; To get all of the available functionality of the player controls, Dim the
    &#39; value returned by player.Ctlcontrols as a WMPLib.IWMPControls3 interface.
    Dim controls As WMPLib.IWMPControls3 = player.Ctlcontrols

    &#39; Check first to be sure the operation is valid. 
    If (controls.isAvailable(&quot;pause&quot;)) Then

        controls.pause()

    End If

End Sub
```





## <a name="requirements"></a><span data-ttu-id="87c7a-120">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="87c7a-120">Requirements</span></span>



| <span data-ttu-id="87c7a-121">Condition requise</span><span class="sxs-lookup"><span data-stu-id="87c7a-121">Requirement</span></span> | <span data-ttu-id="87c7a-122">Valeur</span><span class="sxs-lookup"><span data-stu-id="87c7a-122">Value</span></span> |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="87c7a-123">Version</span><span class="sxs-lookup"><span data-stu-id="87c7a-123">Version</span></span><br/>   | <span data-ttu-id="87c7a-124">Lecteur Windows Media série 9 ou version ultérieure</span><span class="sxs-lookup"><span data-stu-id="87c7a-124">Windows Media Player 9 Series or later</span></span><br/>                                                                      |
| <span data-ttu-id="87c7a-125">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="87c7a-125">Namespace</span></span><br/> | <span data-ttu-id="87c7a-126">**WMPLib**</span><span class="sxs-lookup"><span data-stu-id="87c7a-126">**WMPLib**</span></span><br/>                                                                                                  |
| <span data-ttu-id="87c7a-127">Assembly</span><span class="sxs-lookup"><span data-stu-id="87c7a-127">Assembly</span></span><br/>  | <dl> <span data-ttu-id="87c7a-128"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span><span class="sxs-lookup"><span data-stu-id="87c7a-128"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="87c7a-129">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="87c7a-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="87c7a-130">**Interface IWMPControls (VB et C#)**</span><span class="sxs-lookup"><span data-stu-id="87c7a-130">**IWMPControls Interface (VB and C#)**</span></span>](iwmpcontrols--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="87c7a-131">**IWMPControls. isAvailable (VB et C#)**</span><span class="sxs-lookup"><span data-stu-id="87c7a-131">**IWMPControls.isAvailable (VB and C#)**</span></span>](iwmpcontrols-isavailable--vb-and-c.md)
</dt> </dl>

 

 





