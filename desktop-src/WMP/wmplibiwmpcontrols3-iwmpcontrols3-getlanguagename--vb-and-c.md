---
title: Méthode IWMPControls3 getLanguageName
description: La méthode getLanguageName retourne le nom de la langue audio avec l’identificateur de paramètres régionaux (LCID) spécifié.
ms.assetid: a0651e8d-0ba1-4fff-93f0-fe097231723e
keywords:
- méthode getLanguageName lecteur Windows Media
- méthode getLanguageName lecteur Windows Media, interface IWMPControls3
- Interface IWMPControls3 lecteur Windows Media, méthode getLanguageName
topic_type:
- apiref
api_name:
- IWMPControls3.getLanguageName
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d93bf97c7b5213e3d196897de1c3ebcfa6e6d2c5
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106537120"
---
# <a name="iwmpcontrols3getlanguagename-method"></a><span data-ttu-id="533e6-106">IWMPControls3 :: getLanguageName, méthode</span><span class="sxs-lookup"><span data-stu-id="533e6-106">IWMPControls3::getLanguageName method</span></span>

<span data-ttu-id="533e6-107">La méthode **getLanguageName** retourne le nom de la langue audio avec l’identificateur de paramètres régionaux (LCID) spécifié.</span><span class="sxs-lookup"><span data-stu-id="533e6-107">The **getLanguageName** method returns the name of the audio language with the specified locale identifier (LCID).</span></span>

## <a name="syntax"></a><span data-ttu-id="533e6-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="533e6-108">Syntax</span></span>


```CSharp
public System.String getLanguageName(
  System.Int32 lLangID
);
```


```VB

Public Function getLanguageName( _
  ByVal lLangID As System.Int32 _
) As System.String
Implements IWMPControls3.getLanguageName
```





## <a name="parameters"></a><span data-ttu-id="533e6-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="533e6-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="533e6-110">*lLangID* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="533e6-110">*lLangID* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="533e6-111">**System. Int32** qui est le LCID.</span><span class="sxs-lookup"><span data-stu-id="533e6-111">A **System.Int32** that is the LCID.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="533e6-112">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="533e6-112">Return value</span></span>

<span data-ttu-id="533e6-113">**System. String** qui est le nom de la langue audio.</span><span class="sxs-lookup"><span data-stu-id="533e6-113">A **System.String** that is the name of the audio language.</span></span>

## <a name="remarks"></a><span data-ttu-id="533e6-114">Notes</span><span class="sxs-lookup"><span data-stu-id="533e6-114">Remarks</span></span>

<span data-ttu-id="533e6-115">Un LCID identifie de façon unique un dialecte de langage particulier, appelé paramètres régionaux.</span><span class="sxs-lookup"><span data-stu-id="533e6-115">An LCID uniquely identifies a particular language dialect, called a locale.</span></span>

<span data-ttu-id="533e6-116">Pour le contenu Windows Media, les propriétés et les méthodes liées à la sélection de la langue ne prennent en charge qu’une seule sortie.</span><span class="sxs-lookup"><span data-stu-id="533e6-116">For Windows Media-based content, properties and methods related to language selection support only a single output.</span></span>

## <a name="requirements"></a><span data-ttu-id="533e6-117">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="533e6-117">Requirements</span></span>



| <span data-ttu-id="533e6-118">Condition requise</span><span class="sxs-lookup"><span data-stu-id="533e6-118">Requirement</span></span> | <span data-ttu-id="533e6-119">Valeur</span><span class="sxs-lookup"><span data-stu-id="533e6-119">Value</span></span> |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="533e6-120">Version</span><span class="sxs-lookup"><span data-stu-id="533e6-120">Version</span></span><br/>   | <span data-ttu-id="533e6-121">Lecteur Windows Media série 9 ou version ultérieure</span><span class="sxs-lookup"><span data-stu-id="533e6-121">Windows Media Player 9 Series or later</span></span><br/>                                                                      |
| <span data-ttu-id="533e6-122">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="533e6-122">Namespace</span></span><br/> | <span data-ttu-id="533e6-123">**WMPLib**</span><span class="sxs-lookup"><span data-stu-id="533e6-123">**WMPLib**</span></span><br/>                                                                                                  |
| <span data-ttu-id="533e6-124">Assembly</span><span class="sxs-lookup"><span data-stu-id="533e6-124">Assembly</span></span><br/>  | <dl> <span data-ttu-id="533e6-125"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span><span class="sxs-lookup"><span data-stu-id="533e6-125"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="533e6-126">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="533e6-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="533e6-127">**Interface IWMPControls3 (VB et C#)**</span><span class="sxs-lookup"><span data-stu-id="533e6-127">**IWMPControls3 Interface (VB and C#)**</span></span>](iwmpcontrols3--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="533e6-128">**IWMPControls3. audioLanguageCount (VB et C#)**</span><span class="sxs-lookup"><span data-stu-id="533e6-128">**IWMPControls3.audioLanguageCount (VB and C#)**</span></span>](wmplibiwmpcontrols3-iwmpcontrols3-audiolanguagecount--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="533e6-129">**IWMPControls3. currentAudioLanguage (VB et C#)**</span><span class="sxs-lookup"><span data-stu-id="533e6-129">**IWMPControls3.currentAudioLanguage (VB and C#)**</span></span>](wmplibiwmpcontrols3-iwmpcontrols3-currentaudiolanguage--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="533e6-130">**IWMPControls3. currentAudioLanguageIndex (VB et C#)**</span><span class="sxs-lookup"><span data-stu-id="533e6-130">**IWMPControls3.currentAudioLanguageIndex (VB and C#)**</span></span>](wmplibiwmpcontrols3-iwmpcontrols3-currentaudiolanguageindex--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="533e6-131">**IWMPControls3. getAudioLanguageDescription (VB et C#)**</span><span class="sxs-lookup"><span data-stu-id="533e6-131">**IWMPControls3.getAudioLanguageDescription (VB and C#)**</span></span>](wmplibiwmpcontrols3-iwmpcontrols3-getaudiolanguagedescription--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="533e6-132">**IWMPControls3. getAudioLanguageID (VB et C#)**</span><span class="sxs-lookup"><span data-stu-id="533e6-132">**IWMPControls3.getAudioLanguageID (VB and C#)**</span></span>](wmplibiwmpcontrols3-iwmpcontrols3-getaudiolanguageid--vb-and-c.md)
</dt> </dl>

 

 





