---
title: Propriété de la fréquence IWMPSettings
description: La propriété rate obtient ou définit la vitesse de lecture actuelle pour la vidéo.
ms.assetid: 7baa667b-52e5-4419-8e12-c3627a417b20
keywords:
- propriété rate Windows Media Player
- propriété rate lecteur Windows Media, interface IWMPSettings
- Interface IWMPSettings lecteur Windows Media, propriété rate
topic_type:
- apiref
api_name:
- IWMPSettings.rate
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f502bebdbd22523858637f8abccbe203db104cbe
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106523523"
---
# <a name="iwmpsettingsrate-property"></a><span data-ttu-id="fec97-106">IWMPSettings :: rate, propriété</span><span class="sxs-lookup"><span data-stu-id="fec97-106">IWMPSettings::rate property</span></span>

<span data-ttu-id="fec97-107">La propriété **rate** obtient ou définit la vitesse de lecture actuelle pour la vidéo.</span><span class="sxs-lookup"><span data-stu-id="fec97-107">The **rate** property gets or sets the current playback rate for video.</span></span>

## <a name="syntax"></a><span data-ttu-id="fec97-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="fec97-108">Syntax</span></span>


```CSharp
public System.Double rate {get; set;}
```


```VB

Public Property rate As System.Double
```





## <a name="property-value"></a><span data-ttu-id="fec97-109">Valeur de la propriété</span><span class="sxs-lookup"><span data-stu-id="fec97-109">Property value</span></span>

<span data-ttu-id="fec97-110">**System. double** qui est la vitesse de lecture, avec une valeur par défaut de 1,0.</span><span class="sxs-lookup"><span data-stu-id="fec97-110">A **System.Double** that is the playback rate, with a default value of 1.0.</span></span>

## <a name="remarks"></a><span data-ttu-id="fec97-111">Notes</span><span class="sxs-lookup"><span data-stu-id="fec97-111">Remarks</span></span>

<span data-ttu-id="fec97-112">La valeur récupérée par cette propriété agit comme une valeur de multiplicateur qui vous permet de lire un élément multimédia à un débit plus rapide ou plus lent.</span><span class="sxs-lookup"><span data-stu-id="fec97-112">The value retrieved by this property acts as a multiplier value that enables you to play a media item at a faster or slower rate.</span></span> <span data-ttu-id="fec97-113">La valeur par défaut 1,0 indique la vitesse créée.</span><span class="sxs-lookup"><span data-stu-id="fec97-113">The default value of 1.0 indicates the authored speed.</span></span>

<span data-ttu-id="fec97-114">Notez qu’une piste audio devient difficile à comprendre à des vitesses inférieures à 0,5 ou supérieures à 1,5.</span><span class="sxs-lookup"><span data-stu-id="fec97-114">Note that an audio track becomes difficult to understand at rates lower than 0.5 or higher than 1.5.</span></span> <span data-ttu-id="fec97-115">Un taux de lecture de 2 indique deux fois la vitesse de lecture normale.</span><span class="sxs-lookup"><span data-stu-id="fec97-115">A playback rate of 2 indicates twice the normal playback speed.</span></span>

<span data-ttu-id="fec97-116">Le lecteur Windows Media tentera d’utiliser le plus efficace des quatre modes de lecture suivants</span><span class="sxs-lookup"><span data-stu-id="fec97-116">Windows Media Player will attempt to use the most effective of the following four different playback modes</span></span>

-   <span data-ttu-id="fec97-117">Lecture vidéo lissée avec maintien de la tonalité audio</span><span class="sxs-lookup"><span data-stu-id="fec97-117">Smooth video playback with audio pitch maintained</span></span>
-   <span data-ttu-id="fec97-118">Lecture vidéo lisse avec la tonalité audio non gérée</span><span class="sxs-lookup"><span data-stu-id="fec97-118">Smooth video playback with audio pitch not maintained</span></span>
-   <span data-ttu-id="fec97-119">Lecture vidéo lissée sans audio</span><span class="sxs-lookup"><span data-stu-id="fec97-119">Smooth video playback with no audio</span></span>
-   <span data-ttu-id="fec97-120">Lecture vidéo de l’image clé sans audio</span><span class="sxs-lookup"><span data-stu-id="fec97-120">Keyframe video playback with no audio</span></span>

<span data-ttu-id="fec97-121">Le mode choisi par le lecteur Windows Media dépend de nombreux facteurs, notamment le type de fichier et l’emplacement, le système d’exploitation, le réseau et le serveur.</span><span class="sxs-lookup"><span data-stu-id="fec97-121">The mode chosen by Windows Media Player depends on numerous factors including file type and location, operating system, network, and server.</span></span>

<span data-ttu-id="fec97-122">D’autres considérations s’appliquent également, en fonction du format de média numérique utilisé pour créer le contenu :</span><span class="sxs-lookup"><span data-stu-id="fec97-122">Other considerations apply as well, depending on the digital media format used to create the content:</span></span>

-   <span data-ttu-id="fec97-123">**Windows Media Video (WMV) et ASF.**</span><span class="sxs-lookup"><span data-stu-id="fec97-123">**Windows Media Video (WMV) and ASF.**</span></span> <span data-ttu-id="fec97-124">Les valeurs optimales pour la propriété **rate** sont comprises entre 1 et 10, ou entre 1 et 10 pour la lecture inversée.</span><span class="sxs-lookup"><span data-stu-id="fec97-124">Optimal values for the **rate** property are from 1 to 10, or from  1 to  10 for reverse play.</span></span> <span data-ttu-id="fec97-125">Les valeurs comprises entre 0,5 et 1,0 ou de-0,5 à-1,0 peuvent également fonctionner correctement dans les cas où la tonalité audio peut être conservée, par exemple lors de la lecture de fichiers situés sur l’ordinateur local.</span><span class="sxs-lookup"><span data-stu-id="fec97-125">Values from 0.5 to 1.0 or from -0.5 to -1.0 may also work well in cases where audio pitch can be maintained, such as when playing files located on the local computer.</span></span> <span data-ttu-id="fec97-126">Les valeurs avec une magnitude absolue supérieure à 10 sont autorisées, mais elles ne sont pas très explicites.</span><span class="sxs-lookup"><span data-stu-id="fec97-126">Values with an absolute magnitude greater than 10 are allowed, but are not very meaningful.</span></span>
-   <span data-ttu-id="fec97-127">**Autres formats vidéo.**</span><span class="sxs-lookup"><span data-stu-id="fec97-127">**Other video formats.**</span></span> <span data-ttu-id="fec97-128">La propriété **rate** peut être comprise entre 0 et 9.</span><span class="sxs-lookup"><span data-stu-id="fec97-128">The **rate** property can range from 0 to 9.</span></span> <span data-ttu-id="fec97-129">Les valeurs négatives ne sont pas autorisées.</span><span class="sxs-lookup"><span data-stu-id="fec97-129">Negative values are not allowed.</span></span> <span data-ttu-id="fec97-130">Les valeurs inférieures à 1 représentent un mouvement lent.</span><span class="sxs-lookup"><span data-stu-id="fec97-130">Values less than 1 represent slow motion.</span></span> <span data-ttu-id="fec97-131">Les valeurs supérieures à 9 sont autorisées, mais elles ne sont pas très explicites.</span><span class="sxs-lookup"><span data-stu-id="fec97-131">Values above 9 are allowed, but are not very meaningful.</span></span>

<span data-ttu-id="fec97-132">La méthode **IWMPControls. fastForward** remplace la valeur de **rate** par 5,0, tandis que la méthode **IWMPControls. fastReverse** change la valeur de **rate** en 5,0.</span><span class="sxs-lookup"><span data-stu-id="fec97-132">The **IWMPControls.fastForward** method changes the value of **rate** to 5.0, while the **IWMPControls.fastReverse** method changes the value of **rate** to  5.0.</span></span>

<span data-ttu-id="fec97-133">La vitesse de lecture de certains formats multimédias numériques ne peut pas être modifiée.</span><span class="sxs-lookup"><span data-stu-id="fec97-133">The playback rate of some digital media formats cannot be altered.</span></span> <span data-ttu-id="fec97-134">Utilisez la propriété **IWMPSettings. isAvailable** (en C#, la méthode **IWMPSettings. obtenir \_ isAvailable** ) pour déterminer si cette propriété peut être spécifiée pour un élément multimédia particulier.</span><span class="sxs-lookup"><span data-stu-id="fec97-134">Use the **IWMPSettings.isAvailable** property (In C# the **IWMPSettings.get\_isAvailable** method) to discover whether this property can be specified for a particular media item.</span></span>

## <a name="examples"></a><span data-ttu-id="fec97-135">Exemples</span><span class="sxs-lookup"><span data-stu-id="fec97-135">Examples</span></span>

<span data-ttu-id="fec97-136">L’exemple suivant utilise un contrôle de type UpDown numérique qui permet à l’utilisateur de modifier la vitesse de lecture du média actuel.</span><span class="sxs-lookup"><span data-stu-id="fec97-136">The following example uses a numeric updown control that allows the user to change the playback speed of the current media.</span></span> <span data-ttu-id="fec97-137">Quand l’utilisateur clique sur les flèches haut ou bas du contrôle, la propriété **rate** est définie sur la nouvelle valeur.</span><span class="sxs-lookup"><span data-stu-id="fec97-137">When the user clicks the up or down arrows of the control, the **rate** property is set to the new value.</span></span> <span data-ttu-id="fec97-138">La plage de valeurs possible dans le contrôle est 0,5 (demi-vitesse) à 2,0 (double vitesse).</span><span class="sxs-lookup"><span data-stu-id="fec97-138">The possible range of values in the control are 0.5 (half-speed) to 2.0 (double-speed).</span></span> <span data-ttu-id="fec97-139">L’objet **AxWMPLib. AxWindowsMediaPlayer** est représenté par la variable Player.</span><span class="sxs-lookup"><span data-stu-id="fec97-139">The **AxWMPLib.AxWindowsMediaPlayer** object is represented by the variable named player.</span></span>


```CSharp
private void playbackRate_Click(object sender, System.EventArgs e)
{
    // Get the new value of the control, and cast it from decimal to double.
    double newRate = (double)((System.Windows.Forms.NumericUpDown)sender).Value;

    // Test whether playback rate can be set. 
    if( player.settings.get_isAvailable("Rate") )
    {
        // Set the playback rate to the new value.
        player.settings.rate = newRate;
    }
}
```


```VB

Public Sub playbackRate_Click(ByVal sender As Object, ByVal e As System.EventArgs) Handles playbackRate.Click

    &#39;  Get the new value of the control as a double.
    Dim nUpDown As System.Windows.Forms.NumericUpDown = sender
    Dim newRate As Double = nUpDown.Value

    &#39;  Test whether playback rate can be set. 
    If (player.settings.isAvailable(&quot;Rate&quot;)) Then

        &#39;  Set the playback rate to the new value.
        player.settings.rate = newRate

    End If

End Sub
```





## <a name="requirements"></a><span data-ttu-id="fec97-140">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="fec97-140">Requirements</span></span>



| <span data-ttu-id="fec97-141">Condition requise</span><span class="sxs-lookup"><span data-stu-id="fec97-141">Requirement</span></span> | <span data-ttu-id="fec97-142">Valeur</span><span class="sxs-lookup"><span data-stu-id="fec97-142">Value</span></span> |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="fec97-143">Version</span><span class="sxs-lookup"><span data-stu-id="fec97-143">Version</span></span><br/>   | <span data-ttu-id="fec97-144">Lecteur Windows Media série 9 ou version ultérieure</span><span class="sxs-lookup"><span data-stu-id="fec97-144">Windows Media Player 9 Series or later</span></span><br/>                                                                      |
| <span data-ttu-id="fec97-145">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="fec97-145">Namespace</span></span><br/> | <span data-ttu-id="fec97-146">**WMPLib**</span><span class="sxs-lookup"><span data-stu-id="fec97-146">**WMPLib**</span></span><br/>                                                                                                  |
| <span data-ttu-id="fec97-147">Assembly</span><span class="sxs-lookup"><span data-stu-id="fec97-147">Assembly</span></span><br/>  | <dl> <span data-ttu-id="fec97-148"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span><span class="sxs-lookup"><span data-stu-id="fec97-148"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="fec97-149">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="fec97-149">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fec97-150">**IWMPControls. fastForward (VB et C#)**</span><span class="sxs-lookup"><span data-stu-id="fec97-150">**IWMPControls.fastForward (VB and C#)**</span></span>](wmplibiwmpcontrols-iwmpcontrols-fastforward--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="fec97-151">**IWMPControls. fastReverse (VB et C#)**</span><span class="sxs-lookup"><span data-stu-id="fec97-151">**IWMPControls.fastReverse (VB and C#)**</span></span>](wmplibiwmpcontrols-iwmpcontrols-fastreverse--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="fec97-152">**Interface IWMPSettings (VB et C#)**</span><span class="sxs-lookup"><span data-stu-id="fec97-152">**IWMPSettings Interface (VB and C#)**</span></span>](iwmpsettings--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="fec97-153">**IWMPSettings. isAvailable (VB et C#)**</span><span class="sxs-lookup"><span data-stu-id="fec97-153">**IWMPSettings.isAvailable (VB and C#)**</span></span>](iwmpsettings-isavailable--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="fec97-154">**IWMPSettings. MUTE (VB et C#)**</span><span class="sxs-lookup"><span data-stu-id="fec97-154">**IWMPSettings.mute (VB and C#)**</span></span>](wmplibiwmpsettings-iwmpsettings-mute--vb-and-c.md)
</dt> </dl>

 

 





