---
title: AxWindowsMediaPlayer. openState, propriété
description: La propriété openState obtient une valeur d’énumération indiquant l’état de la source de contenu.
ms.assetid: 7a76814a-649f-4516-a92a-5f536fb1b147
keywords:
- propriété openState lecteur Windows Media
- propriété openState lecteur Windows Media, classe AxWindowsMediaPlayer
- Classe AxWindowsMediaPlayer lecteur Windows Media, propriété openState
topic_type:
- apiref
api_name:
- AxWindowsMediaPlayer.openState
api_location:
- AxInterop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 919bf906ce67793c4cd26f32892eae8acf441295
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106545389"
---
# <a name="axwindowsmediaplayeropenstate-property"></a><span data-ttu-id="f3747-106">AxWindowsMediaPlayer. openState, propriété</span><span class="sxs-lookup"><span data-stu-id="f3747-106">AxWindowsMediaPlayer.openState property</span></span>

<span data-ttu-id="f3747-107">La propriété openState obtient une valeur d’énumération indiquant l’état de la source de contenu.</span><span class="sxs-lookup"><span data-stu-id="f3747-107">The openState property gets an enumeration value indicating the state of the content source.</span></span>

<span data-ttu-id="f3747-108">Cette propriété est en lecture seule.</span><span class="sxs-lookup"><span data-stu-id="f3747-108">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="f3747-109">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="f3747-109">Syntax</span></span>


```CSharp
public WMPOpenState openState {get;}
```


```VB

Public ReadOnly Property openState As WMPOpenState
```





## <a name="property-value"></a><span data-ttu-id="f3747-110">Valeur de la propriété</span><span class="sxs-lookup"><span data-stu-id="f3747-110">Property value</span></span>

<span data-ttu-id="f3747-111">Valeur d’énumération WMPLib. WMPOpenState.</span><span class="sxs-lookup"><span data-stu-id="f3747-111">The WMPLib.WMPOpenState enumeration value.</span></span>

## <a name="remarks"></a><span data-ttu-id="f3747-112">Notes</span><span class="sxs-lookup"><span data-stu-id="f3747-112">Remarks</span></span>

<span data-ttu-id="f3747-113">Il n’est pas garanti que les États du lecteur Windows Media se produisent dans un ordre particulier.</span><span class="sxs-lookup"><span data-stu-id="f3747-113">Windows Media Player states are not guaranteed to occur in any particular order.</span></span> <span data-ttu-id="f3747-114">En outre, tous les États ne se produisent pas nécessairement au cours d’une séquence d’événements.</span><span class="sxs-lookup"><span data-stu-id="f3747-114">Furthermore, not every state necessarily occurs during a sequence of events.</span></span> <span data-ttu-id="f3747-115">Vous ne devez pas écrire du code qui s’appuie sur l’ordre de l’État.</span><span class="sxs-lookup"><span data-stu-id="f3747-115">You should not write code that relies upon state order.</span></span>

## <a name="requirements"></a><span data-ttu-id="f3747-116">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="f3747-116">Requirements</span></span>



| <span data-ttu-id="f3747-117">Condition requise</span><span class="sxs-lookup"><span data-stu-id="f3747-117">Requirement</span></span> | <span data-ttu-id="f3747-118">Valeur</span><span class="sxs-lookup"><span data-stu-id="f3747-118">Value</span></span> |
|----------------------|----------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f3747-119">Version</span><span class="sxs-lookup"><span data-stu-id="f3747-119">Version</span></span><br/>   | <span data-ttu-id="f3747-120">Lecteur Windows Media série 9 ou version ultérieure</span><span class="sxs-lookup"><span data-stu-id="f3747-120">Windows Media Player 9 Series or later</span></span><br/>                                                                          |
| <span data-ttu-id="f3747-121">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="f3747-121">Namespace</span></span><br/> | <span data-ttu-id="f3747-122">**AxWMPLib**</span><span class="sxs-lookup"><span data-stu-id="f3747-122">**AxWMPLib**</span></span><br/>                                                                                                    |
| <span data-ttu-id="f3747-123">Assembly</span><span class="sxs-lookup"><span data-stu-id="f3747-123">Assembly</span></span><br/>  | <dl> <span data-ttu-id="f3747-124"><dt>AxInterop.WMPLib.dll (AxInterop.WMPLib.dll.dll)</dt></span><span class="sxs-lookup"><span data-stu-id="f3747-124"><dt>AxInterop.WMPLib.dll (AxInterop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f3747-125">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="f3747-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f3747-126">**Objet AxWindowsMediaPlayer (VB et C#)**</span><span class="sxs-lookup"><span data-stu-id="f3747-126">**AxWindowsMediaPlayer Object (VB and C#)**</span></span>](axwindowsmediaplayer-object--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="f3747-127">**Événement AxWindowsMediaPlayer. OpenStateChange**</span><span class="sxs-lookup"><span data-stu-id="f3747-127">**AxWindowsMediaPlayer.OpenStateChange Event**</span></span>](axwmplib-axwindowsmediaplayer-openstatechange.md)
</dt> <dt>

[<span data-ttu-id="f3747-128">**WMPLib.WMPOpenState**</span><span class="sxs-lookup"><span data-stu-id="f3747-128">**WMPLib.WMPOpenState**</span></span>](/previous-versions/windows/desktop/api/wmp/ne-wmp-wmpopenstate)
</dt> </dl>

 

 





