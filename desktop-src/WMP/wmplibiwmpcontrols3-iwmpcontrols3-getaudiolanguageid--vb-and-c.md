---
title: Méthode IWMPControls3 getAudioLanguageID
description: La méthode getAudioLanguageID retourne l’identificateur de paramètres régionaux (LCID) pour un index de langue audio spécifié.
ms.assetid: 880bbfca-6f69-41ce-a078-467c1939fae5
keywords:
- méthode getAudioLanguageID lecteur Windows Media
- méthode getAudioLanguageID lecteur Windows Media, interface IWMPControls3
- Interface IWMPControls3 lecteur Windows Media, méthode getAudioLanguageID
topic_type:
- apiref
api_name:
- IWMPControls3.getAudioLanguageID
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fb8112eafec018b12012d20b37bfe30f7b464377
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106530000"
---
# <a name="iwmpcontrols3getaudiolanguageid-method"></a><span data-ttu-id="76d5b-106">IWMPControls3 :: getAudioLanguageID, méthode</span><span class="sxs-lookup"><span data-stu-id="76d5b-106">IWMPControls3::getAudioLanguageID method</span></span>

<span data-ttu-id="76d5b-107">La méthode **getAudioLanguageID** retourne l’identificateur de paramètres régionaux (LCID) pour un index de langue audio spécifié.</span><span class="sxs-lookup"><span data-stu-id="76d5b-107">The **getAudioLanguageID** method returns the locale identifier (LCID) for a specified audio language index.</span></span>

## <a name="syntax"></a><span data-ttu-id="76d5b-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="76d5b-108">Syntax</span></span>


```CSharp
public System.Int32 getAudioLanguageID(
  System.Int32 lIndex
);
```


```VB

Public Function getAudioLanguageID( _
  ByVal lIndex As System.Int32 _
) As System.Int32
Implements IWMPControls3.getAudioLanguageID
```





## <a name="parameters"></a><span data-ttu-id="76d5b-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="76d5b-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="76d5b-110">*Lindex* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="76d5b-110">*lIndex* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="76d5b-111">**System. Int32** qui est l’index de base un de la langue audio.</span><span class="sxs-lookup"><span data-stu-id="76d5b-111">A **System.Int32** that is the one-based index of the audio language.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="76d5b-112">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="76d5b-112">Return value</span></span>

<span data-ttu-id="76d5b-113">**System. Int32** qui est le LCID.</span><span class="sxs-lookup"><span data-stu-id="76d5b-113">A **System.Int32** that is the LCID.</span></span>

## <a name="remarks"></a><span data-ttu-id="76d5b-114">Notes</span><span class="sxs-lookup"><span data-stu-id="76d5b-114">Remarks</span></span>

<span data-ttu-id="76d5b-115">Un LCID identifie de façon unique un dialecte de langage particulier, appelé paramètres régionaux.</span><span class="sxs-lookup"><span data-stu-id="76d5b-115">An LCID uniquely identifies a particular language dialect, called a locale.</span></span>

<span data-ttu-id="76d5b-116">Pour le contenu Windows Media, les propriétés et les méthodes liées à la sélection de la langue ne prennent en charge qu’une seule sortie.</span><span class="sxs-lookup"><span data-stu-id="76d5b-116">For Windows Media based content, properties and methods related to language selection support only a single output.</span></span>

<span data-ttu-id="76d5b-117">Utilisez la propriété **audioLanguageCount** pour obtenir le nombre de langues audio prises en charge, puis accédez à une langue audio individuellement à l’aide d’un index de base un.</span><span class="sxs-lookup"><span data-stu-id="76d5b-117">Use the **audioLanguageCount** property to get the number of supported audio languages, and then access an audio language individually by using a one-based index.</span></span>

## <a name="requirements"></a><span data-ttu-id="76d5b-118">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="76d5b-118">Requirements</span></span>



| <span data-ttu-id="76d5b-119">Condition requise</span><span class="sxs-lookup"><span data-stu-id="76d5b-119">Requirement</span></span> | <span data-ttu-id="76d5b-120">Valeur</span><span class="sxs-lookup"><span data-stu-id="76d5b-120">Value</span></span> |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="76d5b-121">Version</span><span class="sxs-lookup"><span data-stu-id="76d5b-121">Version</span></span><br/>   | <span data-ttu-id="76d5b-122">Lecteur Windows Media série 9 ou version ultérieure</span><span class="sxs-lookup"><span data-stu-id="76d5b-122">Windows Media Player 9 Series or later</span></span><br/>                                                                      |
| <span data-ttu-id="76d5b-123">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="76d5b-123">Namespace</span></span><br/> | <span data-ttu-id="76d5b-124">**WMPLib**</span><span class="sxs-lookup"><span data-stu-id="76d5b-124">**WMPLib**</span></span><br/>                                                                                                  |
| <span data-ttu-id="76d5b-125">Assembly</span><span class="sxs-lookup"><span data-stu-id="76d5b-125">Assembly</span></span><br/>  | <dl> <span data-ttu-id="76d5b-126"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span><span class="sxs-lookup"><span data-stu-id="76d5b-126"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="76d5b-127">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="76d5b-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="76d5b-128">**Interface IWMPControls3 (VB et C#)**</span><span class="sxs-lookup"><span data-stu-id="76d5b-128">**IWMPControls3 Interface (VB and C#)**</span></span>](iwmpcontrols3--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="76d5b-129">**IWMPControls3. audioLanguageCount (VB et C#)**</span><span class="sxs-lookup"><span data-stu-id="76d5b-129">**IWMPControls3.audioLanguageCount (VB and C#)**</span></span>](wmplibiwmpcontrols3-iwmpcontrols3-audiolanguagecount--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="76d5b-130">**IWMPControls3. currentAudioLanguage (VB et C#)**</span><span class="sxs-lookup"><span data-stu-id="76d5b-130">**IWMPControls3.currentAudioLanguage (VB and C#)**</span></span>](wmplibiwmpcontrols3-iwmpcontrols3-currentaudiolanguage--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="76d5b-131">**IWMPControls3. currentAudioLanguageIndex (VB et C#)**</span><span class="sxs-lookup"><span data-stu-id="76d5b-131">**IWMPControls3.currentAudioLanguageIndex (VB and C#)**</span></span>](wmplibiwmpcontrols3-iwmpcontrols3-currentaudiolanguageindex--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="76d5b-132">**IWMPControls3. getAudioLanguageDescription (VB et C#)**</span><span class="sxs-lookup"><span data-stu-id="76d5b-132">**IWMPControls3.getAudioLanguageDescription (VB and C#)**</span></span>](wmplibiwmpcontrols3-iwmpcontrols3-getaudiolanguagedescription--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="76d5b-133">**IWMPControls3. getLanguageName (VB et C#)**</span><span class="sxs-lookup"><span data-stu-id="76d5b-133">**IWMPControls3.getLanguageName (VB and C#)**</span></span>](wmplibiwmpcontrols3-iwmpcontrols3-getlanguagename--vb-and-c.md)
</dt> </dl>

 

 





