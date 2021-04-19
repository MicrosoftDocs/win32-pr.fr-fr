---
title: IWMPClosedCaption2 propriété SAMILangCount
description: La propriété SAMILangCount obtient le nombre de langues prises en charge par le fichier SAMI actuel.
ms.assetid: e3c7203d-66cb-49e2-9204-795c0f27248f
keywords:
- Propriété SAMILangCount lecteur Windows Media
- Propriété SAMILangCount lecteur Windows Media, interface IWMPClosedCaption2
- Interface IWMPClosedCaption2 lecteur Windows Media, propriété SAMILangCount
topic_type:
- apiref
api_name:
- IWMPClosedCaption2.SAMILangCount
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ea01357de508dea319389cd14ab85ebafe0329e6
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106543919"
---
# <a name="iwmpclosedcaption2samilangcount-property"></a><span data-ttu-id="cf8d6-106">IWMPClosedCaption2 :: SAMILangCount, propriété</span><span class="sxs-lookup"><span data-stu-id="cf8d6-106">IWMPClosedCaption2::SAMILangCount property</span></span>

<span data-ttu-id="cf8d6-107">La propriété **SAMILangCount** obtient le nombre de langues prises en charge par le fichier sami actuel.</span><span class="sxs-lookup"><span data-stu-id="cf8d6-107">The **SAMILangCount** property gets the number of languages supported by the current SAMI file.</span></span>

## <a name="syntax"></a><span data-ttu-id="cf8d6-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="cf8d6-108">Syntax</span></span>


```CSharp
public System.Int32 SAMILangCount {get; set;}
```


```VB

Public ReadOnly Property SAMILangCount As System.Int32
```





## <a name="property-value"></a><span data-ttu-id="cf8d6-109">Valeur de la propriété</span><span class="sxs-lookup"><span data-stu-id="cf8d6-109">Property value</span></span>

<span data-ttu-id="cf8d6-110">**System. Int32** qui correspond au nombre de langues prises en charge.</span><span class="sxs-lookup"><span data-stu-id="cf8d6-110">A **System.Int32** that is the number of languages supported.</span></span>

## <a name="remarks"></a><span data-ttu-id="cf8d6-111">Notes</span><span class="sxs-lookup"><span data-stu-id="cf8d6-111">Remarks</span></span>

<span data-ttu-id="cf8d6-112">Cette propriété retourne la valeur 0, sauf si un fichier multimédia numérique est ouvert (AxWindowsMediaPlayer. openState est égal à 13).</span><span class="sxs-lookup"><span data-stu-id="cf8d6-112">This property returns 0 unless a digital media file is open (AxWindowsMediaPlayer.openState is equal to 13).</span></span>

## <a name="requirements"></a><span data-ttu-id="cf8d6-113">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="cf8d6-113">Requirements</span></span>



| <span data-ttu-id="cf8d6-114">Condition requise</span><span class="sxs-lookup"><span data-stu-id="cf8d6-114">Requirement</span></span> | <span data-ttu-id="cf8d6-115">Valeur</span><span class="sxs-lookup"><span data-stu-id="cf8d6-115">Value</span></span> |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="cf8d6-116">Version</span><span class="sxs-lookup"><span data-stu-id="cf8d6-116">Version</span></span><br/>   | <span data-ttu-id="cf8d6-117">Lecteur Windows Media série 9 ou version ultérieure</span><span class="sxs-lookup"><span data-stu-id="cf8d6-117">Windows Media Player 9 Series or later</span></span><br/>                                                                      |
| <span data-ttu-id="cf8d6-118">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="cf8d6-118">Namespace</span></span><br/> | <span data-ttu-id="cf8d6-119">**WMPLib**</span><span class="sxs-lookup"><span data-stu-id="cf8d6-119">**WMPLib**</span></span><br/>                                                                                                  |
| <span data-ttu-id="cf8d6-120">Assembly</span><span class="sxs-lookup"><span data-stu-id="cf8d6-120">Assembly</span></span><br/>  | <dl> <span data-ttu-id="cf8d6-121"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span><span class="sxs-lookup"><span data-stu-id="cf8d6-121"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="cf8d6-122">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="cf8d6-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cf8d6-123">**Ajout de sous-titres à des médias numériques**</span><span class="sxs-lookup"><span data-stu-id="cf8d6-123">**Adding Closed Captions to Digital Media**</span></span>](adding-closed-captions-to-digital-media.md)
</dt> <dt>

[<span data-ttu-id="cf8d6-124">**Interface IWMPClosedCaption (VB et C#)**</span><span class="sxs-lookup"><span data-stu-id="cf8d6-124">**IWMPClosedCaption Interface (VB and C#)**</span></span>](iwmpclosedcaption--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="cf8d6-125">**IWMPClosedCaption. SAMILang (VB et C#)**</span><span class="sxs-lookup"><span data-stu-id="cf8d6-125">**IWMPClosedCaption.SAMILang (VB and C#)**</span></span>](wmplibiwmpclosedcaption-iwmpclosedcaption-samilang--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="cf8d6-126">**Interface IWMPClosedCaption2 (VB et C#)**</span><span class="sxs-lookup"><span data-stu-id="cf8d6-126">**IWMPClosedCaption2 Interface (VB and C#)**</span></span>](iwmpclosedcaption2--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="cf8d6-127">**IWMPClosedCaption2. getSAMILangName (VB et C#)**</span><span class="sxs-lookup"><span data-stu-id="cf8d6-127">**IWMPClosedCaption2.getSAMILangName (VB and C#)**</span></span>](wmplibiwmpclosedcaption2-iwmpclosedcaption2-getsamilangname--vb-and-c.md)
</dt> </dl>

 

 





