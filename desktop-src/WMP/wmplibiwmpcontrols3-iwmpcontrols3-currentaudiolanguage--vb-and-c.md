---
title: IWMPControls3 propriété currentAudioLanguage
description: La propriété currentAudioLanguage obtient ou définit l’identificateur de paramètres régionaux (LCID) de la langue audio pour la lecture.
ms.assetid: 4adf26c7-077a-483e-8a76-accf871eca4c
keywords:
- propriété currentAudioLanguage lecteur Windows Media
- propriété currentAudioLanguage lecteur Windows Media, interface IWMPControls3
- Interface IWMPControls3 lecteur Windows Media, propriété currentAudioLanguage
topic_type:
- apiref
api_name:
- IWMPControls3.currentAudioLanguage
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7c4621b5eace56cb883a6c8b14c3b1f082b12d3a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106537656"
---
# <a name="iwmpcontrols3currentaudiolanguage-property"></a><span data-ttu-id="fbac8-106">IWMPControls3 :: currentAudioLanguage, propriété</span><span class="sxs-lookup"><span data-stu-id="fbac8-106">IWMPControls3::currentAudioLanguage property</span></span>

<span data-ttu-id="fbac8-107">La propriété **currentAudioLanguage** obtient ou définit l’identificateur de paramètres régionaux (LCID) de la langue audio pour la lecture.</span><span class="sxs-lookup"><span data-stu-id="fbac8-107">The **currentAudioLanguage** property gets or sets the locale identifier (LCID) of the audio language for playback.</span></span>

## <a name="syntax"></a><span data-ttu-id="fbac8-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="fbac8-108">Syntax</span></span>


```CSharp
public System.Int32 currentAudioLanguage {get; set;}
```


```VB

Public Property currentAudioLanguage As System.Int32
```





## <a name="property-value"></a><span data-ttu-id="fbac8-109">Valeur de la propriété</span><span class="sxs-lookup"><span data-stu-id="fbac8-109">Property value</span></span>

<span data-ttu-id="fbac8-110">**System. Int32** qui est le LCID de la langue audio.</span><span class="sxs-lookup"><span data-stu-id="fbac8-110">A **System.Int32** that is the LCID of the audio language.</span></span>

## <a name="remarks"></a><span data-ttu-id="fbac8-111">Notes</span><span class="sxs-lookup"><span data-stu-id="fbac8-111">Remarks</span></span>

<span data-ttu-id="fbac8-112">Un LCID identifie de façon unique un dialecte de langage particulier, appelé paramètres régionaux.</span><span class="sxs-lookup"><span data-stu-id="fbac8-112">An LCID uniquely identifies a particular language dialect, called a locale.</span></span>

<span data-ttu-id="fbac8-113">Pour le contenu Windows Media, les propriétés et les méthodes liées à la sélection de la langue ne prennent en charge qu’une seule sortie.</span><span class="sxs-lookup"><span data-stu-id="fbac8-113">For Windows Media-based content, properties and methods related to language selection support only a single output.</span></span>

<span data-ttu-id="fbac8-114">Lors de l’utilisation d’un contenu DVD, la spécification d’un LCID entraîne la sélection de la première piste audio disponible avec l’ID de langue spécifié.</span><span class="sxs-lookup"><span data-stu-id="fbac8-114">When working with DVD content, specifying an LCID will cause the first available audio track having the specified language ID to be selected.</span></span>

## <a name="requirements"></a><span data-ttu-id="fbac8-115">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="fbac8-115">Requirements</span></span>



| <span data-ttu-id="fbac8-116">Condition requise</span><span class="sxs-lookup"><span data-stu-id="fbac8-116">Requirement</span></span> | <span data-ttu-id="fbac8-117">Valeur</span><span class="sxs-lookup"><span data-stu-id="fbac8-117">Value</span></span> |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="fbac8-118">Version</span><span class="sxs-lookup"><span data-stu-id="fbac8-118">Version</span></span><br/>   | <span data-ttu-id="fbac8-119">Lecteur Windows Media série 9 ou version ultérieure</span><span class="sxs-lookup"><span data-stu-id="fbac8-119">Windows Media Player 9 Series or later</span></span><br/>                                                                      |
| <span data-ttu-id="fbac8-120">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="fbac8-120">Namespace</span></span><br/> | <span data-ttu-id="fbac8-121">**WMPLib**</span><span class="sxs-lookup"><span data-stu-id="fbac8-121">**WMPLib**</span></span><br/>                                                                                                  |
| <span data-ttu-id="fbac8-122">Assembly</span><span class="sxs-lookup"><span data-stu-id="fbac8-122">Assembly</span></span><br/>  | <dl> <span data-ttu-id="fbac8-123"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span><span class="sxs-lookup"><span data-stu-id="fbac8-123"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="fbac8-124">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="fbac8-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fbac8-125">**Interface IWMPControls3 (VB et C#)**</span><span class="sxs-lookup"><span data-stu-id="fbac8-125">**IWMPControls3 Interface (VB and C#)**</span></span>](iwmpcontrols3--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="fbac8-126">**IWMPControls3. audioLanguageCount (VB et C#)**</span><span class="sxs-lookup"><span data-stu-id="fbac8-126">**IWMPControls3.audioLanguageCount (VB and C#)**</span></span>](wmplibiwmpcontrols3-iwmpcontrols3-audiolanguagecount--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="fbac8-127">**IWMPControls3. currentAudioLanguageIndex (VB et C#)**</span><span class="sxs-lookup"><span data-stu-id="fbac8-127">**IWMPControls3.currentAudioLanguageIndex (VB and C#)**</span></span>](wmplibiwmpcontrols3-iwmpcontrols3-currentaudiolanguageindex--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="fbac8-128">**IWMPControls3. getAudioLanguageDescription (VB et C#)**</span><span class="sxs-lookup"><span data-stu-id="fbac8-128">**IWMPControls3.getAudioLanguageDescription (VB and C#)**</span></span>](wmplibiwmpcontrols3-iwmpcontrols3-getaudiolanguagedescription--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="fbac8-129">**IWMPControls3. getAudioLanguageID (VB et C#)**</span><span class="sxs-lookup"><span data-stu-id="fbac8-129">**IWMPControls3.getAudioLanguageID (VB and C#)**</span></span>](wmplibiwmpcontrols3-iwmpcontrols3-getaudiolanguageid--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="fbac8-130">**IWMPControls3. getLanguageName (VB et C#)**</span><span class="sxs-lookup"><span data-stu-id="fbac8-130">**IWMPControls3.getLanguageName (VB and C#)**</span></span>](wmplibiwmpcontrols3-iwmpcontrols3-getlanguagename--vb-and-c.md)
</dt> </dl>

 

 





