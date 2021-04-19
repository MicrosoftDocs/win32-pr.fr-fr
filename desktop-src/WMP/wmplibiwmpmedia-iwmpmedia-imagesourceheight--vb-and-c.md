---
title: IWMPMedia propriété imageSourceHeight
description: La propriété imageSourceHeight obtient la hauteur de l’élément multimédia actuel en pixels.
ms.assetid: d60f1713-7110-4605-9009-45825c380546
keywords:
- propriété imageSourceHeight lecteur Windows Media
- propriété imageSourceHeight lecteur Windows Media, interface IWMPMedia
- Interface IWMPMedia lecteur Windows Media, propriété imageSourceHeight
topic_type:
- apiref
api_name:
- IWMPMedia.imageSourceHeight
- IWMPMedia.get_imageSourceHeight
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4b80a702f119ba72220e5ac3ac86b524ce8c11c6
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106542740"
---
# <a name="iwmpmediaimagesourceheight-property"></a><span data-ttu-id="6bfbf-106">IWMPMedia :: imageSourceHeight, propriété</span><span class="sxs-lookup"><span data-stu-id="6bfbf-106">IWMPMedia::imageSourceHeight property</span></span>

<span data-ttu-id="6bfbf-107">La propriété **imageSourceHeight** obtient la hauteur de l’élément multimédia actuel en pixels.</span><span class="sxs-lookup"><span data-stu-id="6bfbf-107">The **imageSourceHeight** property gets the height of the current media item in pixels.</span></span>

<span data-ttu-id="6bfbf-108">Cette propriété est en lecture seule.</span><span class="sxs-lookup"><span data-stu-id="6bfbf-108">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="6bfbf-109">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="6bfbf-109">Syntax</span></span>


```CSharp
public System.Int32 imageSourceHeight {get;}
```


```VB

Public ReadOnly Property imageSourceHeight As System.Int32
```





## <a name="property-value"></a><span data-ttu-id="6bfbf-110">Valeur de la propriété</span><span class="sxs-lookup"><span data-stu-id="6bfbf-110">Property value</span></span>

<span data-ttu-id="6bfbf-111">**System. Int32** qui correspond à la hauteur de l’élément multimédia.</span><span class="sxs-lookup"><span data-stu-id="6bfbf-111">A **System.Int32** that is the height of the media item.</span></span>

## <a name="remarks"></a><span data-ttu-id="6bfbf-112">Notes</span><span class="sxs-lookup"><span data-stu-id="6bfbf-112">Remarks</span></span>

<span data-ttu-id="6bfbf-113">Si l’élément multimédia n’est pas celui en cours, cette propriété retourne la valeur zéro.</span><span class="sxs-lookup"><span data-stu-id="6bfbf-113">If the media item is not the current one, this property returns zero.</span></span>

<span data-ttu-id="6bfbf-114">Avant d’utiliser cette propriété, vous devez disposer d’un accès en lecture à la bibliothèque.</span><span class="sxs-lookup"><span data-stu-id="6bfbf-114">Before using this property, you must have read access to the library.</span></span> <span data-ttu-id="6bfbf-115">Pour plus d’informations, consultez [accès à la bibliothèque](library-access.md).</span><span class="sxs-lookup"><span data-stu-id="6bfbf-115">For more information, see [Library Access](library-access.md).</span></span>

## <a name="examples"></a><span data-ttu-id="6bfbf-116">Exemples</span><span class="sxs-lookup"><span data-stu-id="6bfbf-116">Examples</span></span>

<span data-ttu-id="6bfbf-117">L’exemple suivant utilise **imageSourceHeight** pour afficher la taille de l’image, en pixels, de l’élément multimédia actuel dans une zone de texte.</span><span class="sxs-lookup"><span data-stu-id="6bfbf-117">The following example uses **imageSourceHeight** to display the image size, in pixels, of the current media item in a text box.</span></span> <span data-ttu-id="6bfbf-118">L’objet **AxWMPLib. AxWindowsMediaPlayer** est représenté par la variable Player.</span><span class="sxs-lookup"><span data-stu-id="6bfbf-118">The **AxWMPLib.AxWindowsMediaPlayer** object is represented by the variable named player.</span></span>


```CSharp
// Create an event handler for the OpenStateChange event.
private void player_OpenStateChange(object sender, AxWMPLib._WMPOCXEvents_OpenStateChangeEvent e)
{
    // Test whether the current media item is open.
    if (e.newState == (int)WMPLib.WMPOpenState.wmposMediaOpen)
    {
         // Store the height and width of the new media item.
         int height = player.currentMedia.imageSourceHeight;
         int width = player.currentMedia.imageSourceWidth;

         // Clear all the information in the text box.
         videoSize.Clear();

         // Test whether an image is visible.
         if (height != 0 && width != 0)
         {
            // Display the image size information.
            videoSize.Text = (width.ToString() + " x " + height.ToString());
         }
    }
}
```


```VB

' Create an event handler for the OpenStateChange event.
Public Sub player_OpenStateChange(ByVal sender As Object, ByVal e As AxWMPLib._WMPOCXEvents_OpenStateChangeEvent) Handles player.OpenStateChange

    &#39; Test whether the current media item is open.
    If (e.newState = WMPLib.WMPOpenState.wmposMediaOpen) Then

        &#39; Store the height and width of the new media item.
        Dim Height As Integer = player.currentMedia.imageSourceHeight
        Dim Width As Integer = player.currentMedia.imageSourceWidth

        &#39; Clear all the information in the text box.
        videoSize.Clear()

        &#39; Test whether an image is visible.
        If (Height <> 0 And Width <> 0) Then

            &#39; Display the image size information.
            videoSize.Text = (Width.ToString() + &quot; x &quot; + Height.ToString())

        End If

    End If

End Sub
```





## <a name="requirements"></a><span data-ttu-id="6bfbf-119">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="6bfbf-119">Requirements</span></span>



| <span data-ttu-id="6bfbf-120">Condition requise</span><span class="sxs-lookup"><span data-stu-id="6bfbf-120">Requirement</span></span> | <span data-ttu-id="6bfbf-121">Valeur</span><span class="sxs-lookup"><span data-stu-id="6bfbf-121">Value</span></span> |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6bfbf-122">Version</span><span class="sxs-lookup"><span data-stu-id="6bfbf-122">Version</span></span><br/>   | <span data-ttu-id="6bfbf-123">Lecteur Windows Media série 9 ou version ultérieure</span><span class="sxs-lookup"><span data-stu-id="6bfbf-123">Windows Media Player 9 Series or later</span></span><br/>                                                                      |
| <span data-ttu-id="6bfbf-124">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="6bfbf-124">Namespace</span></span><br/> | <span data-ttu-id="6bfbf-125">**WMPLib**</span><span class="sxs-lookup"><span data-stu-id="6bfbf-125">**WMPLib**</span></span><br/>                                                                                                  |
| <span data-ttu-id="6bfbf-126">Assembly</span><span class="sxs-lookup"><span data-stu-id="6bfbf-126">Assembly</span></span><br/>  | <dl> <span data-ttu-id="6bfbf-127"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span><span class="sxs-lookup"><span data-stu-id="6bfbf-127"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6bfbf-128">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="6bfbf-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6bfbf-129">**Interface IWMPMedia (VB et C#)**</span><span class="sxs-lookup"><span data-stu-id="6bfbf-129">**IWMPMedia Interface (VB and C#)**</span></span>](iwmpmedia--vb-and-c.md)
</dt> </dl>

 

 





