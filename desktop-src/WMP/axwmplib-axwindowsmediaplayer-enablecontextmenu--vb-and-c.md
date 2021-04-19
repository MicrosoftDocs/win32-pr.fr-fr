---
title: AxWindowsMediaPlayer. enableContextMenu, propriété
description: La propriété enableContextMenu obtient ou définit une valeur indiquant s’il faut activer le menu contextuel qui apparaît lorsque l’utilisateur clique sur le bouton droit de la souris.
ms.assetid: 6096cab7-c1fa-4b71-804b-e84facab2229
keywords:
- propriété enableContextMenu lecteur Windows Media
- propriété enableContextMenu lecteur Windows Media, classe AxWindowsMediaPlayer
- Classe AxWindowsMediaPlayer lecteur Windows Media, propriété enableContextMenu
topic_type:
- apiref
api_name:
- AxWindowsMediaPlayer.enableContextMenu
api_location:
- AxInterop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 09c705fd45b9b994863ab4f93df1c3ae10858930
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106530282"
---
# <a name="axwindowsmediaplayerenablecontextmenu-property"></a><span data-ttu-id="1e252-106">AxWindowsMediaPlayer. enableContextMenu, propriété</span><span class="sxs-lookup"><span data-stu-id="1e252-106">AxWindowsMediaPlayer.enableContextMenu property</span></span>

<span data-ttu-id="1e252-107">La propriété enableContextMenu obtient ou définit une valeur indiquant s’il faut activer le menu contextuel qui apparaît lorsque l’utilisateur clique sur le bouton droit de la souris.</span><span class="sxs-lookup"><span data-stu-id="1e252-107">The enableContextMenu property gets or sets a value indicating whether to enable the context menu, which appears when the right mouse button is clicked.</span></span>

## <a name="syntax"></a><span data-ttu-id="1e252-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="1e252-108">Syntax</span></span>


```CSharp
public System.Boolean enableContextMenu {get; set;}
```


```VB

Public Property enableContextMenu As System.Boolean
```





## <a name="property-value"></a><span data-ttu-id="1e252-109">Valeur de la propriété</span><span class="sxs-lookup"><span data-stu-id="1e252-109">Property value</span></span>

<span data-ttu-id="1e252-110">Valeur System. Boolean qui indique s’il faut activer le menu contextuel.</span><span class="sxs-lookup"><span data-stu-id="1e252-110">A System.Boolean value that indicates whether to enable the context menu.</span></span> <span data-ttu-id="1e252-111">La valeur par défaut est true.</span><span class="sxs-lookup"><span data-stu-id="1e252-111">The default value is true.</span></span>

## <a name="remarks"></a><span data-ttu-id="1e252-112">Notes</span><span class="sxs-lookup"><span data-stu-id="1e252-112">Remarks</span></span>

<span data-ttu-id="1e252-113">Pendant la lecture en plein écran, le lecteur Windows Media masque le curseur de la souris quand **enableContextMenu** est égal à false et **UIMODE** est égal à « None ».</span><span class="sxs-lookup"><span data-stu-id="1e252-113">During full-screen playback, Windows Media Player hides the mouse cursor when **enableContextMenu** equals false and **uiMode** equals "none".</span></span>

## <a name="requirements"></a><span data-ttu-id="1e252-114">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="1e252-114">Requirements</span></span>



| <span data-ttu-id="1e252-115">Condition requise</span><span class="sxs-lookup"><span data-stu-id="1e252-115">Requirement</span></span> | <span data-ttu-id="1e252-116">Valeur</span><span class="sxs-lookup"><span data-stu-id="1e252-116">Value</span></span> |
|----------------------|----------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="1e252-117">Version</span><span class="sxs-lookup"><span data-stu-id="1e252-117">Version</span></span><br/>   | <span data-ttu-id="1e252-118">Lecteur Windows Media série 9 ou version ultérieure</span><span class="sxs-lookup"><span data-stu-id="1e252-118">Windows Media Player 9 Series or later</span></span><br/>                                                                          |
| <span data-ttu-id="1e252-119">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="1e252-119">Namespace</span></span><br/> | <span data-ttu-id="1e252-120">**AxWMPLib**</span><span class="sxs-lookup"><span data-stu-id="1e252-120">**AxWMPLib**</span></span><br/>                                                                                                    |
| <span data-ttu-id="1e252-121">Assembly</span><span class="sxs-lookup"><span data-stu-id="1e252-121">Assembly</span></span><br/>  | <dl> <span data-ttu-id="1e252-122"><dt>AxInterop.WMPLib.dll (AxInterop.WMPLib.dll.dll)</dt></span><span class="sxs-lookup"><span data-stu-id="1e252-122"><dt>AxInterop.WMPLib.dll (AxInterop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1e252-123">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="1e252-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1e252-124">**Objet AxWindowsMediaPlayer (VB et C#)**</span><span class="sxs-lookup"><span data-stu-id="1e252-124">**AxWindowsMediaPlayer Object (VB and C#)**</span></span>](axwindowsmediaplayer-object--vb-and-c.md)
</dt> </dl>

 

 





