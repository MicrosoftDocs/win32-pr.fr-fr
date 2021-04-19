---
title: Méthode IWMPControls3 getAudioLanguageDescription
description: La méthode getAudioLanguageDescription retourne la description de la langue audio correspondant à l’index de base 1 spécifié.
ms.assetid: bf3db27f-ba14-409e-8942-fe863d6f3670
keywords:
- méthode getAudioLanguageDescription lecteur Windows Media
- méthode getAudioLanguageDescription lecteur Windows Media, interface IWMPControls3
- Interface IWMPControls3 lecteur Windows Media, méthode getAudioLanguageDescription
topic_type:
- apiref
api_name:
- IWMPControls3.getAudioLanguageDescription
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bb45ceb166ca9c948823e516029569e457f35e27
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106537655"
---
# <a name="iwmpcontrols3getaudiolanguagedescription-method"></a><span data-ttu-id="f85e3-106">IWMPControls3 :: getAudioLanguageDescription, méthode</span><span class="sxs-lookup"><span data-stu-id="f85e3-106">IWMPControls3::getAudioLanguageDescription method</span></span>

<span data-ttu-id="f85e3-107">La méthode **getAudioLanguageDescription** retourne la description de la langue audio correspondant à l’index de base 1 spécifié.</span><span class="sxs-lookup"><span data-stu-id="f85e3-107">The **getAudioLanguageDescription** method returns the description for the audio language corresponding to the specified one-based index.</span></span>

## <a name="syntax"></a><span data-ttu-id="f85e3-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="f85e3-108">Syntax</span></span>


```CSharp
public System.String getAudioLanguageDescription(
  System.Int32 lIndex
);
```


```VB

Public Function getAudioLanguageDescription( _
  ByVal lIndex As System.Int32 _
) As System.String
Implements IWMPControls3.getAudioLanguageDescription
```





## <a name="parameters"></a><span data-ttu-id="f85e3-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="f85e3-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f85e3-110">*Lindex* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="f85e3-110">*lIndex* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f85e3-111">**System. Int32** qui est l’index de langage audio basé sur un.</span><span class="sxs-lookup"><span data-stu-id="f85e3-111">A **System.Int32** that is the one-based audio language index.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f85e3-112">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="f85e3-112">Return value</span></span>

<span data-ttu-id="f85e3-113">**System. String** qui est la description de la langue audio.</span><span class="sxs-lookup"><span data-stu-id="f85e3-113">A **System.String** that is the description of the audio language.</span></span>

## <a name="remarks"></a><span data-ttu-id="f85e3-114">Notes</span><span class="sxs-lookup"><span data-stu-id="f85e3-114">Remarks</span></span>

<span data-ttu-id="f85e3-115">Pour le contenu Windows Media, les propriétés et les méthodes liées à la sélection de la langue ne prennent en charge qu’une seule sortie.</span><span class="sxs-lookup"><span data-stu-id="f85e3-115">For Windows Media based content, properties and methods related to language selection support only a single output.</span></span>

<span data-ttu-id="f85e3-116">Utilisez la propriété **audioLanguageCount** pour obtenir le nombre de langues audio prises en charge, puis accédez à une langue audio individuellement à l’aide d’un index de base un.</span><span class="sxs-lookup"><span data-stu-id="f85e3-116">Use the **audioLanguageCount** property to get the number of supported audio languages, and then access an audio language individually by using a one-based index.</span></span>

## <a name="requirements"></a><span data-ttu-id="f85e3-117">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="f85e3-117">Requirements</span></span>



| <span data-ttu-id="f85e3-118">Condition requise</span><span class="sxs-lookup"><span data-stu-id="f85e3-118">Requirement</span></span> | <span data-ttu-id="f85e3-119">Valeur</span><span class="sxs-lookup"><span data-stu-id="f85e3-119">Value</span></span> |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f85e3-120">Version</span><span class="sxs-lookup"><span data-stu-id="f85e3-120">Version</span></span><br/>   | <span data-ttu-id="f85e3-121">Lecteur Windows Media série 9 ou version ultérieure</span><span class="sxs-lookup"><span data-stu-id="f85e3-121">Windows Media Player 9 Series or later</span></span><br/>                                                                      |
| <span data-ttu-id="f85e3-122">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="f85e3-122">Namespace</span></span><br/> | <span data-ttu-id="f85e3-123">**WMPLib**</span><span class="sxs-lookup"><span data-stu-id="f85e3-123">**WMPLib**</span></span><br/>                                                                                                  |
| <span data-ttu-id="f85e3-124">Assembly</span><span class="sxs-lookup"><span data-stu-id="f85e3-124">Assembly</span></span><br/>  | <dl> <span data-ttu-id="f85e3-125"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span><span class="sxs-lookup"><span data-stu-id="f85e3-125"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f85e3-126">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="f85e3-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f85e3-127">**Interface IWMPControls3 (VB et C#)**</span><span class="sxs-lookup"><span data-stu-id="f85e3-127">**IWMPControls3 Interface (VB and C#)**</span></span>](iwmpcontrols3--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="f85e3-128">**IWMPControls3. audioLanguageCount (VB et C#)**</span><span class="sxs-lookup"><span data-stu-id="f85e3-128">**IWMPControls3.audioLanguageCount (VB and C#)**</span></span>](wmplibiwmpcontrols3-iwmpcontrols3-audiolanguagecount--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="f85e3-129">**IWMPControls3. currentAudioLanguageIndex (VB et C#)**</span><span class="sxs-lookup"><span data-stu-id="f85e3-129">**IWMPControls3.currentAudioLanguageIndex (VB and C#)**</span></span>](wmplibiwmpcontrols3-iwmpcontrols3-currentaudiolanguageindex--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="f85e3-130">**IWMPControls3. currentAudioLanguage (VB et C#)**</span><span class="sxs-lookup"><span data-stu-id="f85e3-130">**IWMPControls3.currentAudioLanguage (VB and C#)**</span></span>](wmplibiwmpcontrols3-iwmpcontrols3-currentaudiolanguage--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="f85e3-131">**IWMPControls3. getAudioLanguageID (VB et C#)**</span><span class="sxs-lookup"><span data-stu-id="f85e3-131">**IWMPControls3.getAudioLanguageID (VB and C#)**</span></span>](wmplibiwmpcontrols3-iwmpcontrols3-getaudiolanguageid--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="f85e3-132">**IWMPControls3. getLanguageName (VB et C#)**</span><span class="sxs-lookup"><span data-stu-id="f85e3-132">**IWMPControls3.getLanguageName (VB and C#)**</span></span>](wmplibiwmpcontrols3-iwmpcontrols3-getlanguagename--vb-and-c.md)
</dt> </dl>

 

 





