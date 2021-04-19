---
title: AxWindowsMediaPlayer. stretchToFit, propriété
description: La propriété stretchToFit obtient ou définit une valeur qui indique si la vidéo affichée par le contrôle du lecteur Windows Media se redimensionne automatiquement pour s’adapter à la fenêtre vidéo, lorsque la fenêtre vidéo est plus grande que les dimensions de l’image vidéo.
ms.assetid: 02e2bcba-4975-4ddd-996b-9bd40774ebc1
keywords:
- propriété stretchToFit lecteur Windows Media
- propriété stretchToFit lecteur Windows Media, classe AxWindowsMediaPlayer
- Classe AxWindowsMediaPlayer lecteur Windows Media, propriété stretchToFit
topic_type:
- apiref
api_name:
- AxWindowsMediaPlayer.stretchToFit
api_location:
- AxInterop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2dd6937ffa556817a80f0b21dfaed6d270c2e351
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106545569"
---
# <a name="axwindowsmediaplayerstretchtofit-property"></a><span data-ttu-id="39069-106">AxWindowsMediaPlayer. stretchToFit, propriété</span><span class="sxs-lookup"><span data-stu-id="39069-106">AxWindowsMediaPlayer.stretchToFit property</span></span>

<span data-ttu-id="39069-107">La propriété stretchToFit obtient ou définit une valeur qui indique si la vidéo affichée par le contrôle du lecteur Windows Media se redimensionne automatiquement pour s’adapter à la fenêtre vidéo, lorsque la fenêtre vidéo est plus grande que les dimensions de l’image vidéo.</span><span class="sxs-lookup"><span data-stu-id="39069-107">The stretchToFit property gets or sets a value indicating whether video displayed by the Windows Media Player control automatically sizes to fit the video window, when the video window is larger than the dimensions of the video image.</span></span>

## <a name="syntax"></a><span data-ttu-id="39069-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="39069-108">Syntax</span></span>


```CSharp
public System.Boolean stretchToFit {get; set;}
```


```VB

Public Property stretchToFit As System.Boolean
```





## <a name="property-value"></a><span data-ttu-id="39069-109">Valeur de la propriété</span><span class="sxs-lookup"><span data-stu-id="39069-109">Property value</span></span>

<span data-ttu-id="39069-110">Valeur System. Boolean qui indique si la vidéo sera étirée pour s’ajuster à la fenêtre.</span><span class="sxs-lookup"><span data-stu-id="39069-110">The System.Boolean value that indicates whether the video will stretch to fit the window.</span></span> <span data-ttu-id="39069-111">La valeur par défaut est false.</span><span class="sxs-lookup"><span data-stu-id="39069-111">The default value is false.</span></span>

## <a name="remarks"></a><span data-ttu-id="39069-112">Notes</span><span class="sxs-lookup"><span data-stu-id="39069-112">Remarks</span></span>

<span data-ttu-id="39069-113">Quand **stretchToFit** a la valeur true, le contrôle du lecteur Windows Media conserve les proportions d’origine de la vidéo.</span><span class="sxs-lookup"><span data-stu-id="39069-113">When **stretchToFit** is set to true, the Windows Media Player control maintains the original aspect ratio of the video.</span></span> <span data-ttu-id="39069-114">Si les proportions de la vidéo ne correspondent pas aux proportions de la fenêtre vidéo, les zones de masque noires peuvent apparaître en haut et en bas, ou à gauche et à droite de l’image vidéo.</span><span class="sxs-lookup"><span data-stu-id="39069-114">If the aspect ratio of the video does not match the aspect ratio of the video window, black mask areas may appear on either the top and the bottom, or left and right, of the video image.</span></span>

<span data-ttu-id="39069-115">Cette propriété s’applique au contrôle du lecteur Windows Media uniquement lorsqu’il est incorporé dans une page Web.</span><span class="sxs-lookup"><span data-stu-id="39069-115">This property applies to the Windows Media Player control only when it is embedded in a webpage.</span></span>

## <a name="requirements"></a><span data-ttu-id="39069-116">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="39069-116">Requirements</span></span>



| <span data-ttu-id="39069-117">Condition requise</span><span class="sxs-lookup"><span data-stu-id="39069-117">Requirement</span></span> | <span data-ttu-id="39069-118">Valeur</span><span class="sxs-lookup"><span data-stu-id="39069-118">Value</span></span> |
|----------------------|----------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="39069-119">Version</span><span class="sxs-lookup"><span data-stu-id="39069-119">Version</span></span><br/>   | <span data-ttu-id="39069-120">Lecteur Windows Media série 9 ou version ultérieure</span><span class="sxs-lookup"><span data-stu-id="39069-120">Windows Media Player 9 Series or later</span></span><br/>                                                                          |
| <span data-ttu-id="39069-121">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="39069-121">Namespace</span></span><br/> | <span data-ttu-id="39069-122">**AxWMPLib**</span><span class="sxs-lookup"><span data-stu-id="39069-122">**AxWMPLib**</span></span><br/>                                                                                                    |
| <span data-ttu-id="39069-123">Assembly</span><span class="sxs-lookup"><span data-stu-id="39069-123">Assembly</span></span><br/>  | <dl> <span data-ttu-id="39069-124"><dt>AxInterop.WMPLib.dll (AxInterop.WMPLib.dll.dll)</dt></span><span class="sxs-lookup"><span data-stu-id="39069-124"><dt>AxInterop.WMPLib.dll (AxInterop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="39069-125">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="39069-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="39069-126">**Objet AxWindowsMediaPlayer (VB et C#)**</span><span class="sxs-lookup"><span data-stu-id="39069-126">**AxWindowsMediaPlayer Object (VB and C#)**</span></span>](axwindowsmediaplayer-object--vb-and-c.md)
</dt> </dl>

 

 





