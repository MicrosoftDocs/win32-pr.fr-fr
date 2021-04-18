---
title: IWMPControls3 propriété currentAudioLanguageIndex
description: La propriété currentAudioLanguageIndex obtient ou définit l’index de base un qui correspond au langage audio pour la lecture.
ms.assetid: 3ed60827-c4e9-4455-b95e-b6eebf7a9a08
keywords:
- propriété currentAudioLanguageIndex lecteur Windows Media
- propriété currentAudioLanguageIndex lecteur Windows Media, interface IWMPControls3
- Interface IWMPControls3 lecteur Windows Media, propriété currentAudioLanguageIndex
topic_type:
- apiref
api_name:
- IWMPControls3.currentAudioLanguageIndex
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f4fb36eea4038322cacd7f233892151ab77e5eea
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106526852"
---
# <a name="iwmpcontrols3currentaudiolanguageindex-property"></a><span data-ttu-id="5808e-106">IWMPControls3 :: currentAudioLanguageIndex, propriété</span><span class="sxs-lookup"><span data-stu-id="5808e-106">IWMPControls3::currentAudioLanguageIndex property</span></span>

<span data-ttu-id="5808e-107">La propriété **currentAudioLanguageIndex** obtient ou définit l’index de base un qui correspond au langage audio pour la lecture.</span><span class="sxs-lookup"><span data-stu-id="5808e-107">The **currentAudioLanguageIndex** property gets or sets the one-based index that corresponds to the audio language for playback.</span></span>

## <a name="syntax"></a><span data-ttu-id="5808e-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="5808e-108">Syntax</span></span>


```CSharp
public System.Int32 currentAudioLanguageIndex {get; set;}
```


```VB

Public Property currentAudioLanguageIndex As System.Int32
```





## <a name="property-value"></a><span data-ttu-id="5808e-109">Valeur de la propriété</span><span class="sxs-lookup"><span data-stu-id="5808e-109">Property value</span></span>

<span data-ttu-id="5808e-110">**System. Int32** qui est l’index de base un de la langue.</span><span class="sxs-lookup"><span data-stu-id="5808e-110">A **System.Int32** that is the one-based index of the language.</span></span>

## <a name="remarks"></a><span data-ttu-id="5808e-111">Notes</span><span class="sxs-lookup"><span data-stu-id="5808e-111">Remarks</span></span>

<span data-ttu-id="5808e-112">Pour le contenu Windows Media, les propriétés et les méthodes liées à la sélection de la langue ne prennent en charge qu’une seule sortie.</span><span class="sxs-lookup"><span data-stu-id="5808e-112">For Windows Media based content, properties and methods related to language selection support only a single output.</span></span>

<span data-ttu-id="5808e-113">Utilisez la propriété **audioLanguageCount** pour connaître le nombre de langues audio prises en charge.</span><span class="sxs-lookup"><span data-stu-id="5808e-113">Use the **audioLanguageCount** property to get the number of supported audio languages.</span></span>

## <a name="requirements"></a><span data-ttu-id="5808e-114">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="5808e-114">Requirements</span></span>



| <span data-ttu-id="5808e-115">Condition requise</span><span class="sxs-lookup"><span data-stu-id="5808e-115">Requirement</span></span> | <span data-ttu-id="5808e-116">Valeur</span><span class="sxs-lookup"><span data-stu-id="5808e-116">Value</span></span> |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5808e-117">Version</span><span class="sxs-lookup"><span data-stu-id="5808e-117">Version</span></span><br/>   | <span data-ttu-id="5808e-118">Lecteur Windows Media série 9 ou version ultérieure</span><span class="sxs-lookup"><span data-stu-id="5808e-118">Windows Media Player 9 Series or later</span></span><br/>                                                                      |
| <span data-ttu-id="5808e-119">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="5808e-119">Namespace</span></span><br/> | <span data-ttu-id="5808e-120">**WMPLib**</span><span class="sxs-lookup"><span data-stu-id="5808e-120">**WMPLib**</span></span><br/>                                                                                                  |
| <span data-ttu-id="5808e-121">Assembly</span><span class="sxs-lookup"><span data-stu-id="5808e-121">Assembly</span></span><br/>  | <dl> <span data-ttu-id="5808e-122"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span><span class="sxs-lookup"><span data-stu-id="5808e-122"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5808e-123">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="5808e-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5808e-124">**Interface IWMPControls3 (VB et C#)**</span><span class="sxs-lookup"><span data-stu-id="5808e-124">**IWMPControls3 Interface (VB and C#)**</span></span>](iwmpcontrols3--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="5808e-125">**IWMPControls3. audioLanguageCount (VB et C#)**</span><span class="sxs-lookup"><span data-stu-id="5808e-125">**IWMPControls3.audioLanguageCount (VB and C#)**</span></span>](wmplibiwmpcontrols3-iwmpcontrols3-audiolanguagecount--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="5808e-126">**IWMPControls3. currentAudioLanguage (VB et C#)**</span><span class="sxs-lookup"><span data-stu-id="5808e-126">**IWMPControls3.currentAudioLanguage (VB and C#)**</span></span>](wmplibiwmpcontrols3-iwmpcontrols3-currentaudiolanguage--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="5808e-127">**IWMPControls3. getAudioLanguageDescription (VB et C#)**</span><span class="sxs-lookup"><span data-stu-id="5808e-127">**IWMPControls3.getAudioLanguageDescription (VB and C#)**</span></span>](wmplibiwmpcontrols3-iwmpcontrols3-getaudiolanguagedescription--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="5808e-128">**IWMPControls3. getAudioLanguageID (VB et C#)**</span><span class="sxs-lookup"><span data-stu-id="5808e-128">**IWMPControls3.getAudioLanguageID (VB and C#)**</span></span>](wmplibiwmpcontrols3-iwmpcontrols3-getaudiolanguageid--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="5808e-129">**IWMPControls3. getLanguageName (VB et C#)**</span><span class="sxs-lookup"><span data-stu-id="5808e-129">**IWMPControls3.getLanguageName (VB and C#)**</span></span>](wmplibiwmpcontrols3-iwmpcontrols3-getlanguagename--vb-and-c.md)
</dt> </dl>

 

 





