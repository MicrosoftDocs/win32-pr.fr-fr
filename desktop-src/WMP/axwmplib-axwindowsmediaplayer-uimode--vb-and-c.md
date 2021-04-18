---
title: AxWindowsMediaPlayer. uiMode, propriété
description: La propriété uiMode obtient ou définit une valeur indiquant les contrôles qui sont affichés dans l’interface utilisateur.
ms.assetid: 01034418-be70-44f3-8812-e529c747c9e4
keywords:
- propriété uiMode lecteur Windows Media
- propriété uiMode lecteur Windows Media, classe AxWindowsMediaPlayer
- Classe AxWindowsMediaPlayer lecteur Windows Media, propriété uiMode
topic_type:
- apiref
api_name:
- AxWindowsMediaPlayer.uiMode
api_location:
- AxInterop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 33edcf6bdff9e1587269df9eb49c3729099d091e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106528930"
---
# <a name="axwindowsmediaplayeruimode-property"></a><span data-ttu-id="f25f3-106">AxWindowsMediaPlayer. uiMode, propriété</span><span class="sxs-lookup"><span data-stu-id="f25f3-106">AxWindowsMediaPlayer.uiMode property</span></span>

<span data-ttu-id="f25f3-107">La propriété uiMode obtient ou définit une valeur indiquant les contrôles qui sont affichés dans l’interface utilisateur.</span><span class="sxs-lookup"><span data-stu-id="f25f3-107">The uiMode property gets or sets a value indicating which controls are shown in the user interface.</span></span>

## <a name="syntax"></a><span data-ttu-id="f25f3-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="f25f3-108">Syntax</span></span>


```CSharp
public System.String uiMode {get; set;}
```


```VB

Public Property uiMode As System.String
```





## <a name="property-value"></a><span data-ttu-id="f25f3-109">Valeur de la propriété</span><span class="sxs-lookup"><span data-stu-id="f25f3-109">Property value</span></span>

<span data-ttu-id="f25f3-110">System. String qui est l’une des valeurs suivantes.</span><span class="sxs-lookup"><span data-stu-id="f25f3-110">A System.String that is one of the following values.</span></span>



| <span data-ttu-id="f25f3-111">Valeur</span><span class="sxs-lookup"><span data-stu-id="f25f3-111">Value</span></span>     | <span data-ttu-id="f25f3-112">Description</span><span class="sxs-lookup"><span data-stu-id="f25f3-112">Description</span></span>                                                                                                                                                                                                     | <span data-ttu-id="f25f3-113">Exemple audio</span><span class="sxs-lookup"><span data-stu-id="f25f3-113">Audio example</span></span>                                                   | <span data-ttu-id="f25f3-114">Exemple de vidéo</span><span class="sxs-lookup"><span data-stu-id="f25f3-114">Video example</span></span>                                                   |
|-----------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------|-----------------------------------------------------------------|
| <span data-ttu-id="f25f3-115">invisibles</span><span class="sxs-lookup"><span data-stu-id="f25f3-115">invisible</span></span> | <span data-ttu-id="f25f3-116">Le lecteur Windows Media est incorporé sans aucune interface utilisateur visible (fenêtre contrôles, vidéo ou visualisation).</span><span class="sxs-lookup"><span data-stu-id="f25f3-116">Windows Media Player is embedded without any visible user interface (controls, video or visualization window).</span></span>                                                                                                  | <span data-ttu-id="f25f3-117">(Rien ne s’affiche.)</span><span class="sxs-lookup"><span data-stu-id="f25f3-117">(Nothing is displayed.)</span></span>                                         | <span data-ttu-id="f25f3-118">(Rien ne s’affiche.)</span><span class="sxs-lookup"><span data-stu-id="f25f3-118">(Nothing is displayed.)</span></span>                                         |
| <span data-ttu-id="f25f3-119">aucun</span><span class="sxs-lookup"><span data-stu-id="f25f3-119">none</span></span>      | <span data-ttu-id="f25f3-120">Le lecteur Windows Media est incorporé sans contrôles, et seule la fenêtre vidéo ou visualisation s’affiche.</span><span class="sxs-lookup"><span data-stu-id="f25f3-120">Windows Media Player is embedded without controls, and with only the video or visualization window displayed.</span></span>                                                                                                   | ![UIMODE = 'none’avec l’audio](images/uimode-none-audio-v11.png) | ![UIMODE = 'none’avec vidéo](images/uimode-none-video-v11.png) |
| <span data-ttu-id="f25f3-123">minimales</span><span class="sxs-lookup"><span data-stu-id="f25f3-123">mini</span></span>      | <span data-ttu-id="f25f3-124">Le lecteur Windows Media est incorporé avec la fenêtre d’État, les commandes lecture/pause, arrêter, muet et volume affichées en plus de la fenêtre vidéo ou visualisation.</span><span class="sxs-lookup"><span data-stu-id="f25f3-124">Windows Media Player is embedded with the status window, play/pause, stop, mute, and volume controls shown in addition to the video or visualization window.</span></span>                                                    | ![UIMODE = 'mini’avec l’audio](images/uimode-mini-audio-v11.png) | ![UIMODE = 'mini’avec vidéo](images/uimode-mini-video-v11.png) |
| <span data-ttu-id="f25f3-127">complet</span><span class="sxs-lookup"><span data-stu-id="f25f3-127">full</span></span>      | <span data-ttu-id="f25f3-128">Par défaut.</span><span class="sxs-lookup"><span data-stu-id="f25f3-128">Default.</span></span> <span data-ttu-id="f25f3-129">Le lecteur Windows Media est intégré à la fenêtre d’État, à la barre de recherche, aux commandes lecture/pause, arrêter, muet, suivant, précédent, avance rapide, rembobiner et volume, en plus de la fenêtre vidéo ou visualisation.</span><span class="sxs-lookup"><span data-stu-id="f25f3-129">Windows Media Player is embedded with the status window, seek bar, play/pause, stop, mute, next, previous, fast forward, rewind, and volume controls in addition to the video or visualization window.</span></span> | ![UIMODE = 'Full’avec l’audio](images/uimode-full-audio-v11.png) | ![UIMODE = 'Full’avec vidéo](images/uimode-full-video-v11.png) |
| <span data-ttu-id="f25f3-132">custom</span><span class="sxs-lookup"><span data-stu-id="f25f3-132">custom</span></span>    | <span data-ttu-id="f25f3-133">Le lecteur Windows Media est incorporé avec une interface utilisateur personnalisée.</span><span class="sxs-lookup"><span data-stu-id="f25f3-133">Windows Media Player is embedded with a custom user interface.</span></span> <span data-ttu-id="f25f3-134">Ne peut être utilisé que dans les programmes C++.</span><span class="sxs-lookup"><span data-stu-id="f25f3-134">Can only be used in C++ programs.</span></span>                                                                                                                | <span data-ttu-id="f25f3-135">(L’interface utilisateur personnalisée s’affiche.)</span><span class="sxs-lookup"><span data-stu-id="f25f3-135">(Custom user interface is displayed.)</span></span>                           | <span data-ttu-id="f25f3-136">(L’interface utilisateur personnalisée s’affiche.)</span><span class="sxs-lookup"><span data-stu-id="f25f3-136">(Custom user interface is displayed.)</span></span>                           |



 

## <a name="remarks"></a><span data-ttu-id="f25f3-137">Notes</span><span class="sxs-lookup"><span data-stu-id="f25f3-137">Remarks</span></span>

<span data-ttu-id="f25f3-138">Cette propriété spécifie l’apparence du lecteur Windows Media incorporé.</span><span class="sxs-lookup"><span data-stu-id="f25f3-138">This property specifies the appearance of the embedded Windows Media Player.</span></span> <span data-ttu-id="f25f3-139">Lorsque **UIMODE** a la valeur « None », « mini » ou « Full », une fenêtre est présente pour l’affichage des clips vidéo et des visualisations audio.</span><span class="sxs-lookup"><span data-stu-id="f25f3-139">When **uiMode** is set to "none", "mini", or "full", a window is present for the display of video clips and audio visualizations.</span></span> <span data-ttu-id="f25f3-140">Cette fenêtre peut être masquée en mode mini ou en mode complet en affectant à l’attribut **Height** de la balise **OBJECT** la valeur 40, qui est mesurée à partir du bas et laisse la partie Controls de l’interface utilisateur visible.</span><span class="sxs-lookup"><span data-stu-id="f25f3-140">This window can be hidden in mini or full mode by setting the **height** attribute of the **OBJECT** tag to 40, which is measured from the bottom, and leaves the controls portion of the user interface visible.</span></span> <span data-ttu-id="f25f3-141">Si aucune interface incorporée n’est souhaitée, affectez la valeur zéro aux attributs **Width** et **Height** .</span><span class="sxs-lookup"><span data-stu-id="f25f3-141">If no embedded interface is desired, set both the **width** and **height** attributes to zero.</span></span>

<span data-ttu-id="f25f3-142">Si **UIMODE** est défini sur « invisible », aucune interface utilisateur n’est affichée, mais l’espace est toujours réservé sur la page, comme indiqué par **Width** et **Height**.</span><span class="sxs-lookup"><span data-stu-id="f25f3-142">If **uiMode** is set to "invisible", no user interface is displayed, but space is still reserved on the page as specified by **width** and **height**.</span></span> <span data-ttu-id="f25f3-143">Cela est utile pour conserver la mise en page quand **UIMODE** peut changer.</span><span class="sxs-lookup"><span data-stu-id="f25f3-143">This is useful for retaining page layout when **uiMode** can change.</span></span> <span data-ttu-id="f25f3-144">En outre, l’espace réservé est transparent, de sorte que tous les éléments superposés derrière le contrôle sont visibles.</span><span class="sxs-lookup"><span data-stu-id="f25f3-144">Additionally, the reserved space is transparent, so any elements layered behind the control will be visible.</span></span>

<span data-ttu-id="f25f3-145">Si **UIMODE** a la valeur « Full » ou « mini », le lecteur Windows Media affiche les contrôles de transport en mode plein écran.</span><span class="sxs-lookup"><span data-stu-id="f25f3-145">If **uiMode** is set to "full" or "mini", Windows Media Player displays transport controls in full-screen mode.</span></span> <span data-ttu-id="f25f3-146">Si **UIMODE** a la valeur « None », aucun contrôle n’est affiché en mode plein écran.</span><span class="sxs-lookup"><span data-stu-id="f25f3-146">If **uiMode** is set to "none", no controls are displayed in full-screen mode.</span></span>

<span data-ttu-id="f25f3-147">Si la fenêtre est visible et que le contenu audio est lu, la visualisation affichée sera celle qui est la plus récemment utilisée dans le lecteur Windows Media.</span><span class="sxs-lookup"><span data-stu-id="f25f3-147">If the window is visible and audio content is being played, the visualization displayed will be the one most recently used in Windows Media Player.</span></span>

<span data-ttu-id="f25f3-148">Si **UIMODE** a la valeur « Custom » dans un programme C++ qui implémente **IWMPRemoteMediaServices**, le fichier d’apparence indiqué par **IWMPRemoteMediaServices. GetCustomUIMode** s’affiche.</span><span class="sxs-lookup"><span data-stu-id="f25f3-148">If **uiMode** is set to "custom" in a C++ program that implements **IWMPRemoteMediaServices**, the skin file indicated by **IWMPRemoteMediaServices.GetCustomUIMode** is displayed.</span></span>

<span data-ttu-id="f25f3-149">Pendant la lecture en plein écran, le lecteur Windows Media masque le curseur de la souris quand **enableContextMenu** est égal à false et **UIMODE** est égal à « None ».</span><span class="sxs-lookup"><span data-stu-id="f25f3-149">During full-screen playback, Windows Media Player hides the mouse cursor when **enableContextMenu** equals false and **uiMode** equals "none".</span></span>

## <a name="examples"></a><span data-ttu-id="f25f3-150">Exemples</span><span class="sxs-lookup"><span data-stu-id="f25f3-150">Examples</span></span>

<span data-ttu-id="f25f3-151">L’exemple suivant crée une zone de liste qui permet à l’utilisateur de modifier le mode d’interface utilisateur d’un objet lecteur Windows Media incorporé.</span><span class="sxs-lookup"><span data-stu-id="f25f3-151">The following example creates a list box that allows the user to change the user interface mode for an embedded Windows Media Player object.</span></span> <span data-ttu-id="f25f3-152">L’objet AxWMPLib. AxWindowsMediaPlayer est représenté par la variable Player.</span><span class="sxs-lookup"><span data-stu-id="f25f3-152">The AxWMPLib.AxWindowsMediaPlayer object is represented by the variable named player.</span></span>


```CSharp
// Load the list box with the four UI mode options.
uiModeOptions.Items.Add("invisible");
uiModeOptions.Items.Add("none");
uiModeOptions.Items.Add("mini");
uiModeOptions.Items.Add("full");


private void uiModeOptions_OnSelectedIndexChanged(object sender, System.EventArgs e)
{
    // Get the selected UI mode in the list box as a string.
    string newMode = (string)(((System.Windows.Forms.ListBox)sender).SelectedItem);
     
    // Set the UI mode that the user selected.
    player.uiMode = newMode;            
}
```


```VB

' Load the list box with the four UI mode options.
uiModeOptions.Items.Add(&quot;invisible&quot;)
uiModeOptions.Items.Add(&quot;none&quot;)
uiModeOptions.Items.Add(&quot;mini&quot;)
uiModeOptions.Items.Add(&quot;full&quot;)


Public Sub uiModeOptions_OnSelectedIndexChanged(ByVal sender As Object, ByVal e As System.EventArgs) Handles uiModeOptions.SelectedIndexChanged

    &#39; Get the selected UI mode in the list box as a string.
    Dim lb As System.Windows.Forms.ListBox = sender
    Dim newMode As String = lb.SelectedItem

    &#39; Set the UI mode that the user selected.
    player.uiMode = newMode

End Sub
```





## <a name="requirements"></a><span data-ttu-id="f25f3-153">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="f25f3-153">Requirements</span></span>



| <span data-ttu-id="f25f3-154">Condition requise</span><span class="sxs-lookup"><span data-stu-id="f25f3-154">Requirement</span></span> | <span data-ttu-id="f25f3-155">Valeur</span><span class="sxs-lookup"><span data-stu-id="f25f3-155">Value</span></span> |
|----------------------|----------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f25f3-156">Version</span><span class="sxs-lookup"><span data-stu-id="f25f3-156">Version</span></span><br/>   | <span data-ttu-id="f25f3-157">Lecteur Windows Media version 7,0 ou ultérieure.</span><span class="sxs-lookup"><span data-stu-id="f25f3-157">Windows Media Player version 7.0 or later.</span></span> <span data-ttu-id="f25f3-158">Lecteur Windows Media série 9 ou version ultérieure pour « invisible » ou « personnalisé »</span><span class="sxs-lookup"><span data-stu-id="f25f3-158">Windows Media Player 9 Series or later for "invisible" or "custom"</span></span><br/>   |
| <span data-ttu-id="f25f3-159">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="f25f3-159">Namespace</span></span><br/> | <span data-ttu-id="f25f3-160">**AxWMPLib**</span><span class="sxs-lookup"><span data-stu-id="f25f3-160">**AxWMPLib**</span></span><br/>                                                                                                    |
| <span data-ttu-id="f25f3-161">Assembly</span><span class="sxs-lookup"><span data-stu-id="f25f3-161">Assembly</span></span><br/>  | <dl> <span data-ttu-id="f25f3-162"><dt>AxInterop.WMPLib.dll (AxInterop.WMPLib.dll.dll)</dt></span><span class="sxs-lookup"><span data-stu-id="f25f3-162"><dt>AxInterop.WMPLib.dll (AxInterop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f25f3-163">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="f25f3-163">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f25f3-164">**Objet AxWindowsMediaPlayer (VB et C#)**</span><span class="sxs-lookup"><span data-stu-id="f25f3-164">**AxWindowsMediaPlayer Object (VB and C#)**</span></span>](axwindowsmediaplayer-object--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="f25f3-165">**AxWindowsMediaPlayer. enableContextMenu (VB et C#)**</span><span class="sxs-lookup"><span data-stu-id="f25f3-165">**AxWindowsMediaPlayer.enableContextMenu (VB and C#)**</span></span>](axwmplib-axwindowsmediaplayer-enablecontextmenu--vb-and-c.md)
</dt> </dl>

 

 





