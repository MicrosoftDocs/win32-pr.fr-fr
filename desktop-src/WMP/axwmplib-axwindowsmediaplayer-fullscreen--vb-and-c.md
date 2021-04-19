---
title: AxWindowsMediaPlayer. fullScreen, propriété
description: La propriété fullScreen obtient ou définit une valeur indiquant si le contenu vidéo est lu en mode plein écran.
ms.assetid: 6c48a54a-e0f1-4bf5-8a53-7ccc78fc76ad
keywords:
- propriété fullScreen lecteur Windows Media
- propriété fullScreen lecteur Windows Media, classe AxWindowsMediaPlayer
- Classe AxWindowsMediaPlayer lecteur Windows Media, propriété fullScreen
topic_type:
- apiref
api_name:
- AxWindowsMediaPlayer.fullScreen
api_location:
- AxInterop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 23bfb1a2c67ecfa3ba7cced6f0ccb564bb387b52
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106537358"
---
# <a name="axwindowsmediaplayerfullscreen-property"></a><span data-ttu-id="3a8c6-106">AxWindowsMediaPlayer. fullScreen, propriété</span><span class="sxs-lookup"><span data-stu-id="3a8c6-106">AxWindowsMediaPlayer.fullScreen property</span></span>

<span data-ttu-id="3a8c6-107">La propriété fullScreen obtient ou définit une valeur indiquant si le contenu vidéo est lu en mode plein écran.</span><span class="sxs-lookup"><span data-stu-id="3a8c6-107">The fullScreen property gets or sets a value indicating whether video content is played in full-screen mode.</span></span>

## <a name="syntax"></a><span data-ttu-id="3a8c6-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="3a8c6-108">Syntax</span></span>


```CSharp
public System.Boolean fullScreen {get; set;}
```


```VB

Public Property fullScreen As System.Boolean
```





## <a name="property-value"></a><span data-ttu-id="3a8c6-109">Valeur de la propriété</span><span class="sxs-lookup"><span data-stu-id="3a8c6-109">Property value</span></span>

<span data-ttu-id="3a8c6-110">Valeur System. Boolean qui indique si le contenu est lu en mode plein écran.</span><span class="sxs-lookup"><span data-stu-id="3a8c6-110">A System.Boolean value that indicates whether content is played in full-screen mode.</span></span> <span data-ttu-id="3a8c6-111">La valeur par défaut est false.</span><span class="sxs-lookup"><span data-stu-id="3a8c6-111">The default value is false.</span></span>

## <a name="remarks"></a><span data-ttu-id="3a8c6-112">Notes</span><span class="sxs-lookup"><span data-stu-id="3a8c6-112">Remarks</span></span>

<span data-ttu-id="3a8c6-113">Pour que le mode plein écran fonctionne correctement quand vous incorporez le contrôle du lecteur Windows Media, la zone d’affichage de la vidéo doit avoir une hauteur et une largeur d’au moins un pixel.</span><span class="sxs-lookup"><span data-stu-id="3a8c6-113">For full-screen mode to work properly when embedding the Windows Media Player control, the video display area must have a height and width of at least one pixel.</span></span> <span data-ttu-id="3a8c6-114">Si **UIMODE** a la valeur « mini » ou « Full », la hauteur du contrôle lui-même doit être supérieure ou égale à 65 pour s’adapter à la zone d’affichage vidéo en plus de l’interface utilisateur.</span><span class="sxs-lookup"><span data-stu-id="3a8c6-114">If **uiMode** is set to "mini" or "full", the height of the control itself must be 65 or greater to accommodate the video display area in addition to the user interface.</span></span>

<span data-ttu-id="3a8c6-115">Si **UIMODE** a la valeur « invisible », l’affectation de la valeur true à cette propriété génère une erreur et n’affecte pas le comportement du contrôle.</span><span class="sxs-lookup"><span data-stu-id="3a8c6-115">If **uiMode** is set to "invisible", then setting this property to true raises an error and does not affect the behavior of the control.</span></span>

<span data-ttu-id="3a8c6-116">Pendant la lecture en plein écran, le lecteur Windows Media masque le curseur de la souris quand [enableContextMenu](axwmplib-axwindowsmediaplayer-enablecontextmenu--vb-and-c.md) est égal à false et **UIMODE** est égal à « None ».</span><span class="sxs-lookup"><span data-stu-id="3a8c6-116">During full-screen playback, Windows Media Player hides the mouse cursor when [enableContextMenu](axwmplib-axwindowsmediaplayer-enablecontextmenu--vb-and-c.md) equals false and **uiMode** equals "none".</span></span>

<span data-ttu-id="3a8c6-117">Si **UIMODE** a la valeur « Full » ou « mini », le lecteur Windows Media affiche les contrôles de transport en mode plein écran lorsque le curseur de la souris se déplace.</span><span class="sxs-lookup"><span data-stu-id="3a8c6-117">If **uiMode** is set to "full" or "mini", Windows Media Player displays transport controls in full-screen mode when the mouse cursor moves.</span></span> <span data-ttu-id="3a8c6-118">Après un bref intervalle d’absence de mouvement de la souris, les contrôles de transport sont masqués.</span><span class="sxs-lookup"><span data-stu-id="3a8c6-118">After a brief interval of no mouse movement, the transport controls are hidden.</span></span> <span data-ttu-id="3a8c6-119">Si **UIMODE** a la valeur « None », aucun contrôle n’est affiché en mode plein écran.</span><span class="sxs-lookup"><span data-stu-id="3a8c6-119">If **uiMode** is set to "none", no controls are displayed in full-screen mode.</span></span>

> [!Note]  
> <span data-ttu-id="3a8c6-120">L’affichage des contrôles de transport en mode plein écran nécessite le système d’exploitation Windows XP.</span><span class="sxs-lookup"><span data-stu-id="3a8c6-120">Displaying transport controls in full-screen mode requires the Windows XP operating system.</span></span>

 

<span data-ttu-id="3a8c6-121">Si les contrôles de transport ne s’affichent pas en mode plein écran, le lecteur Windows Media quitte automatiquement le mode plein écran lorsque la lecture s’arrête.</span><span class="sxs-lookup"><span data-stu-id="3a8c6-121">If transport controls are not displayed in full-screen mode, then Windows Media Player automatically exits full-screen mode when playback stops.</span></span>

## <a name="examples"></a><span data-ttu-id="3a8c6-122">Exemples</span><span class="sxs-lookup"><span data-stu-id="3a8c6-122">Examples</span></span>

<span data-ttu-id="3a8c6-123">L’exemple suivant crée un bouton qui utilise la propriété fullScreen pour faire basculer un objet lecteur incorporé en mode plein écran.</span><span class="sxs-lookup"><span data-stu-id="3a8c6-123">The following example creates a button that uses the fullScreen property to switch an embedded player object to full-screen mode.</span></span> <span data-ttu-id="3a8c6-124">L’objet AxWMPLib. AxWindowsMediaPlayer est représenté par la variable Player.</span><span class="sxs-lookup"><span data-stu-id="3a8c6-124">The AxWMPLib.AxWindowsMediaPlayer object is represented by the variable named player.</span></span>


```CSharp
private void fullScreen_Click(object sender, System.EventArgs e)
{
    // If the player is playing, switch to full screen. 
    if (player.playState == WMPLib.WMPPlayState.wmppsPlaying)
    {
        player.fullScreen = true;
    }
}
```


```VB

Public Sub fullScreen_Click(ByVal sender As Object, ByVal e As System.EventArgs) Handles fullScreen.Click

    &#39; If the player is playing, switch to full screen. 
    If (player.playState = WMPLib.WMPPlayState.wmppsPlaying) Then

        player.fullScreen = True

    End If

End Sub
```





## <a name="requirements"></a><span data-ttu-id="3a8c6-125">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="3a8c6-125">Requirements</span></span>



| <span data-ttu-id="3a8c6-126">Condition requise</span><span class="sxs-lookup"><span data-stu-id="3a8c6-126">Requirement</span></span> | <span data-ttu-id="3a8c6-127">Valeur</span><span class="sxs-lookup"><span data-stu-id="3a8c6-127">Value</span></span> |
|----------------------|--------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3a8c6-128">Version</span><span class="sxs-lookup"><span data-stu-id="3a8c6-128">Version</span></span><br/>   | <span data-ttu-id="3a8c6-129">Lecteur Windows Media série 9 ou version ultérieure</span><span class="sxs-lookup"><span data-stu-id="3a8c6-129">Windows Media Player 9 Series or later</span></span><br/>                                                                  |
| <span data-ttu-id="3a8c6-130">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="3a8c6-130">Namespace</span></span><br/> | <span data-ttu-id="3a8c6-131">**AxWMPLib**</span><span class="sxs-lookup"><span data-stu-id="3a8c6-131">**AxWMPLib**</span></span><br/>                                                                                            |
| <span data-ttu-id="3a8c6-132">Assembly</span><span class="sxs-lookup"><span data-stu-id="3a8c6-132">Assembly</span></span><br/>  | <dl> <span data-ttu-id="3a8c6-133"><dt>AxInterop. WMPLib (AxInterop.WMPLib.dll)</dt></span><span class="sxs-lookup"><span data-stu-id="3a8c6-133"><dt>AxInterop.WMPLib (AxInterop.WMPLib.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3a8c6-134">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="3a8c6-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3a8c6-135">**Objet AxWindowsMediaPlayer (VB et C#)**</span><span class="sxs-lookup"><span data-stu-id="3a8c6-135">**AxWindowsMediaPlayer Object (VB and C#)**</span></span>](axwindowsmediaplayer-object--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="3a8c6-136">**AxWindowsMediaPlayer. uiMode (VB et C#)**</span><span class="sxs-lookup"><span data-stu-id="3a8c6-136">**AxWindowsMediaPlayer.uiMode (VB and C#)**</span></span>](axwmplib-axwindowsmediaplayer-uimode--vb-and-c.md)
</dt> </dl>

 

 





