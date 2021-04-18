---
title: AxWindowsMediaPlayer. windowlessVideo, propriété
description: La propriété windowlessVideo obtient ou définit une valeur indiquant si le contrôle du lecteur Windows Media affiche la vidéo en mode sans fenêtre.
ms.assetid: 70386aae-cd30-405d-90dd-9b3fa63dad17
keywords:
- propriété windowlessVideo lecteur Windows Media
- propriété windowlessVideo lecteur Windows Media, classe AxWindowsMediaPlayer
- Classe AxWindowsMediaPlayer lecteur Windows Media, propriété windowlessVideo
topic_type:
- apiref
api_name:
- AxWindowsMediaPlayer.windowlessVideo
api_location:
- AxInterop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d22ecc0f39b03201809877fe8ebc667d62e16d0b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106526491"
---
# <a name="axwindowsmediaplayerwindowlessvideo-property"></a><span data-ttu-id="cbd2b-106">AxWindowsMediaPlayer. windowlessVideo, propriété</span><span class="sxs-lookup"><span data-stu-id="cbd2b-106">AxWindowsMediaPlayer.windowlessVideo property</span></span>

<span data-ttu-id="cbd2b-107">La propriété windowlessVideo obtient ou définit une valeur indiquant si le contrôle du lecteur Windows Media affiche la vidéo en mode sans fenêtre.</span><span class="sxs-lookup"><span data-stu-id="cbd2b-107">The windowlessVideo property gets or sets a value indicating whether the Windows Media Player control renders video in windowless mode.</span></span>

## <a name="syntax"></a><span data-ttu-id="cbd2b-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="cbd2b-108">Syntax</span></span>


```CSharp
public System.Boolean windowlessVideo {get; set;}
```


```VB

Public Property windowlessVideo As System.Boolean
```





## <a name="property-value"></a><span data-ttu-id="cbd2b-109">Valeur de la propriété</span><span class="sxs-lookup"><span data-stu-id="cbd2b-109">Property value</span></span>

<span data-ttu-id="cbd2b-110">Valeur System. Boolean indiquant si le contrôle du lecteur Windows Media affiche la vidéo en mode sans fenêtre.</span><span class="sxs-lookup"><span data-stu-id="cbd2b-110">A System.Boolean value indicating whether the Windows Media Player control renders video in windowless mode.</span></span> <span data-ttu-id="cbd2b-111">La valeur par défaut est false.</span><span class="sxs-lookup"><span data-stu-id="cbd2b-111">The default value is false.</span></span>

## <a name="remarks"></a><span data-ttu-id="cbd2b-112">Notes</span><span class="sxs-lookup"><span data-stu-id="cbd2b-112">Remarks</span></span>

<span data-ttu-id="cbd2b-113">Par défaut, un contrôle du lecteur Windows Media incorporé affiche la vidéo dans sa propre fenêtre au sein de la zone cliente.</span><span class="sxs-lookup"><span data-stu-id="cbd2b-113">By default, an embedded Windows Media Player control renders video in its own window within the client area.</span></span> <span data-ttu-id="cbd2b-114">Quand **windowlessVideo** a la valeur true, l’objet lecteur Windows Media affiche la vidéo directement dans la zone cliente, ce qui vous permet d’appliquer des effets spéciaux ou de coucher la vidéo avec du texte.</span><span class="sxs-lookup"><span data-stu-id="cbd2b-114">When **windowlessVideo** is set to true, the Windows Media Player object renders video directly in the client area, so you can apply special effects or layer the video with text.</span></span>

<span data-ttu-id="cbd2b-115">Dans Windows Vista, le rendu de la vidéo en mode sans fenêtre peut dégrader les performances.</span><span class="sxs-lookup"><span data-stu-id="cbd2b-115">In Windows Vista, rendering video in windowless mode can degrade performance.</span></span>

<span data-ttu-id="cbd2b-116">L’obtention d’une valeur pour cette propriété n’est pas prise en charge pour Netscape Navigator.</span><span class="sxs-lookup"><span data-stu-id="cbd2b-116">Getting a value for this property is not supported for Netscape Navigator.</span></span> <span data-ttu-id="cbd2b-117">La définition d’une valeur pour cette propriété dans Netscape Navigator peut donner des résultats inattendus.</span><span class="sxs-lookup"><span data-stu-id="cbd2b-117">Setting a value for this property in Netscape Navigator may yield unexpected results.</span></span>

## <a name="requirements"></a><span data-ttu-id="cbd2b-118">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="cbd2b-118">Requirements</span></span>



| <span data-ttu-id="cbd2b-119">Condition requise</span><span class="sxs-lookup"><span data-stu-id="cbd2b-119">Requirement</span></span> | <span data-ttu-id="cbd2b-120">Valeur</span><span class="sxs-lookup"><span data-stu-id="cbd2b-120">Value</span></span> |
|----------------------|----------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="cbd2b-121">Version</span><span class="sxs-lookup"><span data-stu-id="cbd2b-121">Version</span></span><br/>   | <span data-ttu-id="cbd2b-122">Lecteur Windows Media série 9 ou version ultérieure</span><span class="sxs-lookup"><span data-stu-id="cbd2b-122">Windows Media Player 9 Series or later</span></span><br/>                                                                          |
| <span data-ttu-id="cbd2b-123">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="cbd2b-123">Namespace</span></span><br/> | <span data-ttu-id="cbd2b-124">**AxWMPLib**</span><span class="sxs-lookup"><span data-stu-id="cbd2b-124">**AxWMPLib**</span></span><br/>                                                                                                    |
| <span data-ttu-id="cbd2b-125">Assembly</span><span class="sxs-lookup"><span data-stu-id="cbd2b-125">Assembly</span></span><br/>  | <dl> <span data-ttu-id="cbd2b-126"><dt>AxInterop.WMPLib.dll (AxInterop.WMPLib.dll.dll)</dt></span><span class="sxs-lookup"><span data-stu-id="cbd2b-126"><dt>AxInterop.WMPLib.dll (AxInterop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="cbd2b-127">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="cbd2b-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cbd2b-128">**Objet AxWindowsMediaPlayer (VB et C#)**</span><span class="sxs-lookup"><span data-stu-id="cbd2b-128">**AxWindowsMediaPlayer Object (VB and C#)**</span></span>](axwindowsmediaplayer-object--vb-and-c.md)
</dt> </dl>

 

 





