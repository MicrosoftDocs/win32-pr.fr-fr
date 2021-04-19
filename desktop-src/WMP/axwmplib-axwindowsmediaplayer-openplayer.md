---
title: Méthode AxWindowsMediaPlayer. openPlayer
description: La méthode openPlayer ouvre le lecteur Windows Media à l’aide de l’URL spécifiée. | Méthode AxWindowsMediaPlayer. openPlayer
ms.assetid: 9a9d8200-f427-42ff-b49f-d973cf86014f
keywords:
- méthode openPlayer lecteur Windows Media
- méthode openPlayer lecteur Windows Media, classe AxWindowsMediaPlayer
- Classe AxWindowsMediaPlayer lecteur Windows Media, méthode openPlayer
topic_type:
- apiref
api_name:
- AxWindowsMediaPlayer.openPlayer
api_location:
- AxInterop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 58416a1f20969b0bd223f653f44b5633f19cb096
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106535899"
---
# <a name="axwindowsmediaplayeropenplayer-method"></a><span data-ttu-id="30a37-107">Méthode AxWindowsMediaPlayer. openPlayer</span><span class="sxs-lookup"><span data-stu-id="30a37-107">AxWindowsMediaPlayer.openPlayer method</span></span>

<span data-ttu-id="30a37-108">La méthode **openPlayer** ouvre le lecteur Windows Media à l’aide de l’URL spécifiée.</span><span class="sxs-lookup"><span data-stu-id="30a37-108">The **openPlayer** method opens Windows Media Player using the specified URL.</span></span>

## <a name="syntax"></a><span data-ttu-id="30a37-109">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="30a37-109">Syntax</span></span>


```CSharp
public void openPlayer(
  System.String bstrURL
);
```


```VB

Public Sub openPlayer( _
  ByVal bstrURL As System.String _
)
```





## <a name="parameters"></a><span data-ttu-id="30a37-110">Paramètres</span><span class="sxs-lookup"><span data-stu-id="30a37-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="30a37-111">*bstrURL*</span><span class="sxs-lookup"><span data-stu-id="30a37-111">*bstrURL*</span></span> 
</dt> <dd>

<span data-ttu-id="30a37-112">**System. String** qui est l’URL de l’élément multimédia à lire.</span><span class="sxs-lookup"><span data-stu-id="30a37-112">The **System.String** that is the URL of the media item to play.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="30a37-113">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="30a37-113">Return value</span></span>

<span data-ttu-id="30a37-114">Cette méthode ne retourne pas de valeur.</span><span class="sxs-lookup"><span data-stu-id="30a37-114">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="30a37-115">Notes</span><span class="sxs-lookup"><span data-stu-id="30a37-115">Remarks</span></span>

<span data-ttu-id="30a37-116">Cette méthode lance le lecteur Windows Media avec l’URL spécifiée définie en tant qu’élément multimédia actuel.</span><span class="sxs-lookup"><span data-stu-id="30a37-116">This method launches Windows Media Player with the specified URL set as the current media item.</span></span> <span data-ttu-id="30a37-117">Si le joueur a été précédemment fermé en mode apparence, il s’ouvre en utilisant la dernière apparence choisie par l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="30a37-117">If the Player was previously closed in skin mode it will open using the skin last chosen by the user.</span></span> <span data-ttu-id="30a37-118">Dans le cas contraire, le joueur s’ouvre en mode complet.</span><span class="sxs-lookup"><span data-stu-id="30a37-118">Otherwise, the Player opens in full mode.</span></span>

## <a name="requirements"></a><span data-ttu-id="30a37-119">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="30a37-119">Requirements</span></span>



| <span data-ttu-id="30a37-120">Condition requise</span><span class="sxs-lookup"><span data-stu-id="30a37-120">Requirement</span></span> | <span data-ttu-id="30a37-121">Valeur</span><span class="sxs-lookup"><span data-stu-id="30a37-121">Value</span></span> |
|----------------------|----------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="30a37-122">Version</span><span class="sxs-lookup"><span data-stu-id="30a37-122">Version</span></span><br/>   | <span data-ttu-id="30a37-123">Lecteur Windows Media série 9 ou version ultérieure</span><span class="sxs-lookup"><span data-stu-id="30a37-123">Windows Media Player 9 Series or later</span></span><br/>                                                                          |
| <span data-ttu-id="30a37-124">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="30a37-124">Namespace</span></span><br/> | <span data-ttu-id="30a37-125">**AxWMPLib**</span><span class="sxs-lookup"><span data-stu-id="30a37-125">**AxWMPLib**</span></span><br/>                                                                                                    |
| <span data-ttu-id="30a37-126">Assembly</span><span class="sxs-lookup"><span data-stu-id="30a37-126">Assembly</span></span><br/>  | <dl> <span data-ttu-id="30a37-127"><dt>AxInterop.WMPLib.dll (AxInterop.WMPLib.dll.dll)</dt></span><span class="sxs-lookup"><span data-stu-id="30a37-127"><dt>AxInterop.WMPLib.dll (AxInterop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="30a37-128">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="30a37-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="30a37-129">**Objet AxWindowsMediaPlayer (VB et C#)**</span><span class="sxs-lookup"><span data-stu-id="30a37-129">**AxWindowsMediaPlayer Object (VB and C#)**</span></span>](axwindowsmediaplayer-object--vb-and-c.md)
</dt> </dl>

 

 





