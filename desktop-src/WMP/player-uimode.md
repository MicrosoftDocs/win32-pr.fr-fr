---
title: Player. uiMode
description: La propriété uiMode spécifie ou récupère une valeur indiquant les contrôles qui sont affichés dans l’interface utilisateur.
ms.assetid: 6297d22b-e8ed-4f28-83f6-b74d3265c520
keywords:
- Lecteur Windows Media Player. uiMode
topic_type:
- apiref
api_name:
- Player.uiMode
api_location:
- wmp.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2b1fd2e8e3a2ac6314255cd6ebc350b2ace8cb63
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106541079"
---
# <a name="playeruimode"></a><span data-ttu-id="ec739-104">Player. uiMode</span><span class="sxs-lookup"><span data-stu-id="ec739-104">Player.uiMode</span></span>

<span data-ttu-id="ec739-105">La propriété **UIMODE** spécifie ou récupère une valeur indiquant les contrôles qui sont affichés dans l’interface utilisateur.</span><span class="sxs-lookup"><span data-stu-id="ec739-105">The **uiMode** property specifies or retrieves a value indicating which controls are shown in the user interface.</span></span>

## <a name="syntax"></a><span data-ttu-id="ec739-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="ec739-106">Syntax</span></span>

<span data-ttu-id="ec739-107">*lecteur* . **UIMODE**</span><span class="sxs-lookup"><span data-stu-id="ec739-107">*player* .**uiMode**</span></span>

## <a name="possible-values"></a><span data-ttu-id="ec739-108">Valeurs possibles</span><span class="sxs-lookup"><span data-stu-id="ec739-108">Possible Values</span></span>

<span data-ttu-id="ec739-109">Cette propriété est une **chaîne** en lecture/écriture.</span><span class="sxs-lookup"><span data-stu-id="ec739-109">This property is a read/write **String**.</span></span>



| <span data-ttu-id="ec739-110">Valeur</span><span class="sxs-lookup"><span data-stu-id="ec739-110">Value</span></span>     | <span data-ttu-id="ec739-111">Description</span><span class="sxs-lookup"><span data-stu-id="ec739-111">Description</span></span>                                                                                                                                                                                                           | <span data-ttu-id="ec739-112">Exemple audio</span><span class="sxs-lookup"><span data-stu-id="ec739-112">Audio Example</span></span>                                          | <span data-ttu-id="ec739-113">Exemple de vidéo</span><span class="sxs-lookup"><span data-stu-id="ec739-113">Video Example</span></span>                                          |
|-----------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------|--------------------------------------------------------|
| <span data-ttu-id="ec739-114">invisibles</span><span class="sxs-lookup"><span data-stu-id="ec739-114">invisible</span></span> | <span data-ttu-id="ec739-115">Le lecteur Windows Media est incorporé sans aucune interface utilisateur visible (fenêtre contrôles, vidéo ou visualisation).</span><span class="sxs-lookup"><span data-stu-id="ec739-115">Windows Media Player is embedded without any visible user interface (controls, video or visualization window).</span></span>                                                                                                        | <span data-ttu-id="ec739-116">(Rien ne s’affiche.)</span><span class="sxs-lookup"><span data-stu-id="ec739-116">(Nothing is displayed.)</span></span>                                | <span data-ttu-id="ec739-117">(Rien ne s’affiche.)</span><span class="sxs-lookup"><span data-stu-id="ec739-117">(Nothing is displayed.)</span></span>                                |
| <span data-ttu-id="ec739-118">aucun</span><span class="sxs-lookup"><span data-stu-id="ec739-118">none</span></span>      | <span data-ttu-id="ec739-119">Le lecteur Windows Media est incorporé sans contrôles, et seule la fenêtre vidéo ou visualisation s’affiche.</span><span class="sxs-lookup"><span data-stu-id="ec739-119">Windows Media Player is embedded without controls, and with only the video or visualization window displayed.</span></span>                                                                                                         | ![« aucune » avec l’audio](images/uimode-none-audio-v11.png) | ![« aucune » avec vidéo](images/uimode-none-video-v11.png) |
| <span data-ttu-id="ec739-122">minimales</span><span class="sxs-lookup"><span data-stu-id="ec739-122">mini</span></span>      | <span data-ttu-id="ec739-123">Le lecteur Windows Media est incorporé avec la fenêtre d’État, les commandes lecture/pause, arrêter, muet et volume affichées en plus de la fenêtre vidéo ou visualisation.</span><span class="sxs-lookup"><span data-stu-id="ec739-123">Windows Media Player is embedded with the status window, play/pause, stop, mute, and volume controls shown in addition to the video or visualization window.</span></span>                                                          | ![« mini » avec l’audio](images/uimode-mini-audio-v11.png) | ![« mini » avec vidéo](images/uimode-mini-video-v11.png) |
| <span data-ttu-id="ec739-126">complet</span><span class="sxs-lookup"><span data-stu-id="ec739-126">full</span></span>      | <span data-ttu-id="ec739-127">Par défaut.</span><span class="sxs-lookup"><span data-stu-id="ec739-127">Default.</span></span> <span data-ttu-id="ec739-128">Le lecteur Windows Media est intégré à la fenêtre d’État, à la barre de recherche, aux commandes lecture/pause, arrêter, muet, suivant, précédent, avance rapide, inversée rapide et volume, en plus de la fenêtre vidéo ou de visualisation.</span><span class="sxs-lookup"><span data-stu-id="ec739-128">Windows Media Player is embedded with the status window, seek bar, play/pause, stop, mute, next, previous, fast forward, fast reverse, and volume controls in addition to the video or visualization window.</span></span> | ![« Full » avec l’audio](images/uimode-full-audio-v11.png) | ![« Full » avec vidéo](images/uimode-full-video-v11.png) |
| <span data-ttu-id="ec739-131">custom</span><span class="sxs-lookup"><span data-stu-id="ec739-131">custom</span></span>    | <span data-ttu-id="ec739-132">Le lecteur Windows Media est incorporé avec une interface utilisateur personnalisée.</span><span class="sxs-lookup"><span data-stu-id="ec739-132">Windows Media Player is embedded with a custom user interface.</span></span> <span data-ttu-id="ec739-133">Ne peut être utilisé que dans les programmes C++.</span><span class="sxs-lookup"><span data-stu-id="ec739-133">Can only be used in C++ programs.</span></span>                                                                                                                      | <span data-ttu-id="ec739-134">(L’interface utilisateur personnalisée s’affiche.)</span><span class="sxs-lookup"><span data-stu-id="ec739-134">(Custom user interface is displayed.)</span></span>                  | <span data-ttu-id="ec739-135">(L’interface utilisateur personnalisée s’affiche.)</span><span class="sxs-lookup"><span data-stu-id="ec739-135">(Custom user interface is displayed.)</span></span>                  |



 

## <a name="remarks"></a><span data-ttu-id="ec739-136">Notes</span><span class="sxs-lookup"><span data-stu-id="ec739-136">Remarks</span></span>

<span data-ttu-id="ec739-137">Cette propriété spécifie l’apparence du lecteur Windows Media incorporé.</span><span class="sxs-lookup"><span data-stu-id="ec739-137">This property specifies the appearance of the embedded Windows Media Player.</span></span> <span data-ttu-id="ec739-138">Lorsque **UIMODE** a la valeur « None », « mini » ou « Full », une fenêtre est présente pour l’affichage des clips vidéo et des visualisations audio.</span><span class="sxs-lookup"><span data-stu-id="ec739-138">When **uiMode** is set to "none", "mini", or "full", a window is present for the display of video clips and audio visualizations.</span></span> <span data-ttu-id="ec739-139">Cette fenêtre peut être masquée en mode mini ou en mode complet en affectant à l’attribut **Height** de la balise **OBJECT** la valeur 40, qui est mesurée à partir du bas et laisse la partie Controls de l’interface utilisateur visible.</span><span class="sxs-lookup"><span data-stu-id="ec739-139">This window can be hidden in mini or full mode by setting the **height** attribute of the **OBJECT** tag to 40, which is measured from the bottom, and leaves the controls portion of the user interface visible.</span></span> <span data-ttu-id="ec739-140">Si aucune interface incorporée n’est souhaitée, affectez la valeur zéro aux attributs **Width** et **Height** .</span><span class="sxs-lookup"><span data-stu-id="ec739-140">If no embedded interface is desired, set both the **width** and **height** attributes to zero.</span></span>

<span data-ttu-id="ec739-141">Si **UIMODE** est défini sur « invisible », aucune interface utilisateur n’est affichée, mais l’espace est toujours réservé sur la page, comme indiqué par **Width** et **Height**.</span><span class="sxs-lookup"><span data-stu-id="ec739-141">If **uiMode** is set to "invisible", no user interface is displayed, but space is still reserved on the page as specified by **width** and **height**.</span></span> <span data-ttu-id="ec739-142">Cela est utile pour conserver la mise en page quand **UIMODE** peut changer.</span><span class="sxs-lookup"><span data-stu-id="ec739-142">This is useful for retaining page layout when **uiMode** can change.</span></span> <span data-ttu-id="ec739-143">En outre, l’espace réservé est transparent, de sorte que tous les éléments superposés derrière le contrôle sont visibles.</span><span class="sxs-lookup"><span data-stu-id="ec739-143">Additionally, the reserved space is transparent, so any elements layered behind the control will be visible.</span></span>

<span data-ttu-id="ec739-144">Si **UIMODE** a la valeur « Full » ou « mini », le lecteur Windows Media affiche les contrôles de transport en mode plein écran.</span><span class="sxs-lookup"><span data-stu-id="ec739-144">If **uiMode** is set to "full" or "mini", Windows Media Player displays transport controls in full-screen mode.</span></span> <span data-ttu-id="ec739-145">Si **UIMODE** a la valeur « None », aucun contrôle n’est affiché en mode plein écran.</span><span class="sxs-lookup"><span data-stu-id="ec739-145">If **uiMode** is set to "none", no controls are displayed in full-screen mode.</span></span>

<span data-ttu-id="ec739-146">Si la fenêtre est visible et que le contenu audio est lu, la visualisation affichée sera celle qui est la plus récemment utilisée dans le lecteur Windows Media.</span><span class="sxs-lookup"><span data-stu-id="ec739-146">If the window is visible and audio content is being played, the visualization displayed will be the one most recently used in Windows Media Player.</span></span>

<span data-ttu-id="ec739-147">Si **UIMODE** a la valeur « Custom » dans un programme C++ qui implémente **IWMPRemoteMediaServices**, le fichier d’apparence indiqué par **IWMPRemoteMediaServices :: GetCustomUIMode** s’affiche.</span><span class="sxs-lookup"><span data-stu-id="ec739-147">If **uiMode** is set to "custom" in a C++ program that implements **IWMPRemoteMediaServices**, the skin file indicated by **IWMPRemoteMediaServices::GetCustomUIMode** is displayed.</span></span>

<span data-ttu-id="ec739-148">Pendant la lecture en plein écran, le lecteur Windows Media masque le curseur de la souris quand **enableContextMenu** est égal à false et **UIMODE** est égal à « None ».</span><span class="sxs-lookup"><span data-stu-id="ec739-148">During full-screen playback, Windows Media Player hides the mouse cursor when **enableContextMenu** equals false and **uiMode** equals "none".</span></span>

## <a name="examples"></a><span data-ttu-id="ec739-149">Exemples</span><span class="sxs-lookup"><span data-stu-id="ec739-149">Examples</span></span>

<span data-ttu-id="ec739-150">L’exemple suivant crée un élément SELECT HTML qui permet à l’utilisateur de modifier l’interface utilisateur d’un objet **lecteur** incorporé.</span><span class="sxs-lookup"><span data-stu-id="ec739-150">The following example creates an HTML SELECT element that allows the user to change the user interface for an embedded **Player** object.</span></span> <span data-ttu-id="ec739-151">L’objet **Player** a été créé avec ID = "Player".</span><span class="sxs-lookup"><span data-stu-id="ec739-151">The **Player** object was created with ID = "Player".</span></span>


```
<!-- Create an HTML SELECT element. -->
<SELECT  ID = UI  LANGUAGE="JScript"

         /* Specify the UI mode the user selects. */
         onChange = "Player.uiMode = UI.value">

/* These are the four UI mode options. */
<OPTION VALUE="invisible">Invisible
<OPTION VALUE="none">No Controls
<OPTION VALUE="mini">Mini Player
<OPTION VALUE="full">Full Player
</SELECT>

```



<span data-ttu-id="ec739-152">Windows Media Player 10 Mobile : cette propriété accepte ou retourne uniquement les valeurs « None » ou « Full ».</span><span class="sxs-lookup"><span data-stu-id="ec739-152">Windows Media Player 10 Mobile: This property only accepts or returns values of "none" or "full".</span></span> <span data-ttu-id="ec739-153">Sur les périphériques Smartphone, seul l’état de lecture et un compteur s’affichent lorsque *UIMODE* est défini sur « Full ».</span><span class="sxs-lookup"><span data-stu-id="ec739-153">On Smartphone devices, only playback status and a counter are displayed when *uiMode* is set to "full".</span></span>

## <a name="requirements"></a><span data-ttu-id="ec739-154">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="ec739-154">Requirements</span></span>



| <span data-ttu-id="ec739-155">Condition requise</span><span class="sxs-lookup"><span data-stu-id="ec739-155">Requirement</span></span> | <span data-ttu-id="ec739-156">Valeur</span><span class="sxs-lookup"><span data-stu-id="ec739-156">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ec739-157">Version</span><span class="sxs-lookup"><span data-stu-id="ec739-157">Version</span></span><br/> | <span data-ttu-id="ec739-158">Lecteur Windows Media version 7,0 ou ultérieure.</span><span class="sxs-lookup"><span data-stu-id="ec739-158">Windows Media Player version 7.0 or later.</span></span> <span data-ttu-id="ec739-159">Lecteur Windows Media série 9 ou version ultérieure pour « invisible » ou « personnalisé ».</span><span class="sxs-lookup"><span data-stu-id="ec739-159">Windows Media Player 9 Series or later for "invisible" or "custom".</span></span><br/> |
| <span data-ttu-id="ec739-160">DLL</span><span class="sxs-lookup"><span data-stu-id="ec739-160">DLL</span></span><br/>     | <dl> <span data-ttu-id="ec739-161"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="ec739-161"><dt>Wmp.dll</dt></span></span> </dl>                                        |



## <a name="see-also"></a><span data-ttu-id="ec739-162">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="ec739-162">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ec739-163">**Interface IWMPRemoteMediaServices**</span><span class="sxs-lookup"><span data-stu-id="ec739-163">**IWMPRemoteMediaServices Interface**</span></span>](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpremotemediaservices)
</dt> <dt>

[<span data-ttu-id="ec739-164">**IWMPRemoteMediaServices::GetCustomUIMode**</span><span class="sxs-lookup"><span data-stu-id="ec739-164">**IWMPRemoteMediaServices::GetCustomUIMode**</span></span>](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpremotemediaservices-getcustomuimode)
</dt> <dt>

[<span data-ttu-id="ec739-165">**Objet Player**</span><span class="sxs-lookup"><span data-stu-id="ec739-165">**Player Object**</span></span>](player-object.md)
</dt> </dl>

 

 





