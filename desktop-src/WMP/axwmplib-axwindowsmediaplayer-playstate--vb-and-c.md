---
title: AxWindowsMediaPlayer. lecture, propriété
description: La propriété lecture obtient une valeur d’énumération indiquant l’état de l’opération du lecteur Windows Media.
ms.assetid: ab9f1547-5c28-4289-beaf-9262f7f59b07
keywords:
- propriété lecture lecteur Windows Media
- propriété lecture lecteur Windows Media, classe AxWindowsMediaPlayer
- Classe AxWindowsMediaPlayer lecteur Windows Media, propriété lecture
topic_type:
- apiref
api_name:
- AxWindowsMediaPlayer.playState
api_location:
- AxInterop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d397c65c1cfd7f4adb040cc94e208a66c6c42d1b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106529990"
---
# <a name="axwindowsmediaplayerplaystate-property"></a><span data-ttu-id="09c43-106">AxWindowsMediaPlayer. lecture, propriété</span><span class="sxs-lookup"><span data-stu-id="09c43-106">AxWindowsMediaPlayer.playState property</span></span>

<span data-ttu-id="09c43-107">La propriété lecture obtient une valeur d’énumération indiquant l’état de l’opération du lecteur Windows Media.</span><span class="sxs-lookup"><span data-stu-id="09c43-107">The playState property gets an enumeration value indicating the state of the Windows Media Player operation.</span></span>

<span data-ttu-id="09c43-108">Cette propriété est en lecture seule.</span><span class="sxs-lookup"><span data-stu-id="09c43-108">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="09c43-109">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="09c43-109">Syntax</span></span>


```CSharp
public WMPPlayState playState {get;}
```


```VB

Public ReadOnly Property playState As WMPPlayState
```





## <a name="property-value"></a><span data-ttu-id="09c43-110">Valeur de la propriété</span><span class="sxs-lookup"><span data-stu-id="09c43-110">Property value</span></span>

<span data-ttu-id="09c43-111">Valeur d’énumération WMPLib. WMPPlayState.</span><span class="sxs-lookup"><span data-stu-id="09c43-111">The WMPLib.WMPPlayState enumeration value.</span></span>

## <a name="remarks"></a><span data-ttu-id="09c43-112">Notes</span><span class="sxs-lookup"><span data-stu-id="09c43-112">Remarks</span></span>

<span data-ttu-id="09c43-113">Il n’est pas garanti que les États du lecteur Windows Media se produisent dans un ordre particulier.</span><span class="sxs-lookup"><span data-stu-id="09c43-113">Windows Media Player states are not guaranteed to occur in any particular order.</span></span> <span data-ttu-id="09c43-114">En outre, tous les États ne se produisent pas nécessairement au cours d’une séquence d’événements.</span><span class="sxs-lookup"><span data-stu-id="09c43-114">Furthermore, not every state necessarily occurs during a sequence of events.</span></span> <span data-ttu-id="09c43-115">Vous ne devez pas écrire du code qui s’appuie sur l’ordre de l’État.</span><span class="sxs-lookup"><span data-stu-id="09c43-115">You should not write code that relies upon state order.</span></span>

## <a name="examples"></a><span data-ttu-id="09c43-116">Exemples</span><span class="sxs-lookup"><span data-stu-id="09c43-116">Examples</span></span>

<span data-ttu-id="09c43-117">L’exemple suivant utilise la propriété lecture pour afficher l’état de lecture actuel du joueur dans une étiquette.</span><span class="sxs-lookup"><span data-stu-id="09c43-117">The following example uses the playState property to display the current playing status of the player in a label.</span></span> <span data-ttu-id="09c43-118">L’objet AxWMPLib. AxWindowsMediaPlayer est représenté par la variable Player.</span><span class="sxs-lookup"><span data-stu-id="09c43-118">The AxWMPLib.AxWindowsMediaPlayer object is represented by the variable named player.</span></span>


```CSharp
// Test whether Windows Media Player is in the playing state. 
if (player.playState == WMPLib.WMPPlayState.wmppsPlaying)
{
    playStateLabel.Text = "Windows Media Player is playing!";
}
else
{
    playStateLabel.Text = "Windows Media Player is NOT playing!";
}
```


```VB

' Test whether Windows Media Player is in the playing state. 
If (player.playState = WMPLib.WMPPlayState.wmppsPlaying) Then

    playStateLabel.Text = &quot;Windows Media Player is playing!&quot;

Else

    playStateLabel.Text = &quot;Windows Media Player is NOT playing!&quot;

End If
```





## <a name="requirements"></a><span data-ttu-id="09c43-119">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="09c43-119">Requirements</span></span>



| <span data-ttu-id="09c43-120">Condition requise</span><span class="sxs-lookup"><span data-stu-id="09c43-120">Requirement</span></span> | <span data-ttu-id="09c43-121">Valeur</span><span class="sxs-lookup"><span data-stu-id="09c43-121">Value</span></span> |
|----------------------|----------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="09c43-122">Version</span><span class="sxs-lookup"><span data-stu-id="09c43-122">Version</span></span><br/>   | <span data-ttu-id="09c43-123">Lecteur Windows Media série 9 ou version ultérieure</span><span class="sxs-lookup"><span data-stu-id="09c43-123">Windows Media Player 9 Series or later</span></span><br/>                                                                          |
| <span data-ttu-id="09c43-124">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="09c43-124">Namespace</span></span><br/> | <span data-ttu-id="09c43-125">**AxWMPLib**</span><span class="sxs-lookup"><span data-stu-id="09c43-125">**AxWMPLib**</span></span><br/>                                                                                                    |
| <span data-ttu-id="09c43-126">Assembly</span><span class="sxs-lookup"><span data-stu-id="09c43-126">Assembly</span></span><br/>  | <dl> <span data-ttu-id="09c43-127"><dt>AxInterop.WMPLib.dll (AxInterop.WMPLib.dll.dll)</dt></span><span class="sxs-lookup"><span data-stu-id="09c43-127"><dt>AxInterop.WMPLib.dll (AxInterop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="09c43-128">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="09c43-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="09c43-129">**Objet AxWindowsMediaPlayer (VB et C#)**</span><span class="sxs-lookup"><span data-stu-id="09c43-129">**AxWindowsMediaPlayer Object (VB and C#)**</span></span>](axwindowsmediaplayer-object--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="09c43-130">**Événement AxWindowsMediaPlayer. PlayStateChange (VB et C#)**</span><span class="sxs-lookup"><span data-stu-id="09c43-130">**AxWindowsMediaPlayer.PlayStateChange Event (VB and C#)**</span></span>](axwmplib-axwindowsmediaplayer-playstatechange.md)
</dt> <dt>

[<span data-ttu-id="09c43-131">**WMPPlayState**</span><span class="sxs-lookup"><span data-stu-id="09c43-131">**WMPPlayState**</span></span>](/previous-versions/windows/desktop/api/wmp/ne-wmp-wmpplaystate)
</dt> </dl>

 

 





