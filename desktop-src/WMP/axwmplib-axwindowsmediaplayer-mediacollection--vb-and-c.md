---
title: AxWindowsMediaPlayer. mediaCollection, propriété
description: La propriété mediaCollection obtient une interface IWMPMediaCollection qui fournit un moyen d’organiser une grande collection d’éléments multimédias.
ms.assetid: ec37e1da-a843-4b89-88fc-ec9255baa98a
keywords:
- propriété mediaCollection lecteur Windows Media
- propriété mediaCollection lecteur Windows Media, classe AxWindowsMediaPlayer
- Classe AxWindowsMediaPlayer lecteur Windows Media, propriété mediaCollection
topic_type:
- apiref
api_name:
- AxWindowsMediaPlayer.mediaCollection
api_location:
- AxInterop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f6501dd5dda8e60b8ba1a5f2667f6b581cbdfd90
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106531079"
---
# <a name="axwindowsmediaplayermediacollection-property"></a><span data-ttu-id="646d2-106">AxWindowsMediaPlayer. mediaCollection, propriété</span><span class="sxs-lookup"><span data-stu-id="646d2-106">AxWindowsMediaPlayer.mediaCollection property</span></span>

<span data-ttu-id="646d2-107">La propriété mediaCollection obtient une interface **IWMPMediaCollection** qui fournit un moyen d’organiser une grande collection d’éléments multimédias.</span><span class="sxs-lookup"><span data-stu-id="646d2-107">The mediaCollection property gets an **IWMPMediaCollection** interface that provides a way to organize a large collection of media items.</span></span>

<span data-ttu-id="646d2-108">Cette propriété est en lecture seule.</span><span class="sxs-lookup"><span data-stu-id="646d2-108">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="646d2-109">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="646d2-109">Syntax</span></span>


```CSharp
public IWMPMediaCollection mediaCollection {get;}
```


```VB

Public ReadOnly Property mediaCollection As IWMPMediaCollection
```





## <a name="property-value"></a><span data-ttu-id="646d2-110">Valeur de la propriété</span><span class="sxs-lookup"><span data-stu-id="646d2-110">Property value</span></span>

<span data-ttu-id="646d2-111">L’interface WMPLib. IWMPMediaCollection à une collection d’éléments multimédias.</span><span class="sxs-lookup"><span data-stu-id="646d2-111">The WMPLib.IWMPMediaCollection interface to a collection of media items.</span></span>

## <a name="remarks"></a><span data-ttu-id="646d2-112">Notes</span><span class="sxs-lookup"><span data-stu-id="646d2-112">Remarks</span></span>

<span data-ttu-id="646d2-113">Pour récupérer la valeur de cette propriété, l’accès en lecture à la bibliothèque est requis.</span><span class="sxs-lookup"><span data-stu-id="646d2-113">To retrieve the value of this property, read access to the library is required.</span></span> <span data-ttu-id="646d2-114">Pour plus d’informations, consultez [accès à la bibliothèque](library-access.md).</span><span class="sxs-lookup"><span data-stu-id="646d2-114">For more information, see [Library Access](library-access.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="646d2-115">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="646d2-115">Requirements</span></span>



| <span data-ttu-id="646d2-116">Condition requise</span><span class="sxs-lookup"><span data-stu-id="646d2-116">Requirement</span></span> | <span data-ttu-id="646d2-117">Valeur</span><span class="sxs-lookup"><span data-stu-id="646d2-117">Value</span></span> |
|----------------------|----------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="646d2-118">Version</span><span class="sxs-lookup"><span data-stu-id="646d2-118">Version</span></span><br/>   | <span data-ttu-id="646d2-119">Lecteur Windows Media série 9 ou version ultérieure</span><span class="sxs-lookup"><span data-stu-id="646d2-119">Windows Media Player 9 Series or later</span></span><br/>                                                                          |
| <span data-ttu-id="646d2-120">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="646d2-120">Namespace</span></span><br/> | <span data-ttu-id="646d2-121">**AxWMPLib**</span><span class="sxs-lookup"><span data-stu-id="646d2-121">**AxWMPLib**</span></span><br/>                                                                                                    |
| <span data-ttu-id="646d2-122">Assembly</span><span class="sxs-lookup"><span data-stu-id="646d2-122">Assembly</span></span><br/>  | <dl> <span data-ttu-id="646d2-123"><dt>AxInterop.WMPLib.dll (AxInterop.WMPLib.dll.dll)</dt></span><span class="sxs-lookup"><span data-stu-id="646d2-123"><dt>AxInterop.WMPLib.dll (AxInterop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="646d2-124">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="646d2-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="646d2-125">**Objet AxWindowsMediaPlayer (VB et C#)**</span><span class="sxs-lookup"><span data-stu-id="646d2-125">**AxWindowsMediaPlayer Object (VB and C#)**</span></span>](axwindowsmediaplayer-object--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="646d2-126">**Interface IWMPMediaCollection (VB et C#)**</span><span class="sxs-lookup"><span data-stu-id="646d2-126">**IWMPMediaCollection Interface (VB and C#)**</span></span>](iwmpmediacollection--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="646d2-127">**IWMPSettings2. mediaAccessRights (VB et C#)**</span><span class="sxs-lookup"><span data-stu-id="646d2-127">**IWMPSettings2.mediaAccessRights (VB and C#)**</span></span>](wmplibiwmpsettings2-iwmpsettings2-mediaaccessrights--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="646d2-128">**IWMPSettings2. requestMediaAccessRights (VB et C#)**</span><span class="sxs-lookup"><span data-stu-id="646d2-128">**IWMPSettings2.requestMediaAccessRights (VB and C#)**</span></span>](wmplibiwmpsettings2-iwmpsettings2-requestmediaaccessrights--vb-and-c.md)
</dt> </dl>

 

 





