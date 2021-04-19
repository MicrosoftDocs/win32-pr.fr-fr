---
title: Controls. currentAudioLanguage
description: La propriété currentAudioLanguage spécifie ou récupère l’identificateur de paramètres régionaux (LCID) de la langue audio pour la lecture.
ms.assetid: 628845df-add3-4068-9c3d-b4a9b818808c
keywords:
- Controls. currentAudioLanguage Windows Media Player
topic_type:
- apiref
api_name:
- Controls.currentAudioLanguage
api_location:
- wmp.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f1bc84c7d4c14bb742a6db37feca59fb9d0db0e1
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106537566"
---
# <a name="controlscurrentaudiolanguage"></a><span data-ttu-id="c55ea-104">Controls. currentAudioLanguage</span><span class="sxs-lookup"><span data-stu-id="c55ea-104">Controls.currentAudioLanguage</span></span>

<span data-ttu-id="c55ea-105">La propriété **currentAudioLanguage** spécifie ou récupère l’identificateur de paramètres régionaux (LCID) de la langue audio pour la lecture.</span><span class="sxs-lookup"><span data-stu-id="c55ea-105">The **currentAudioLanguage** property specifies or retrieves the locale identifier (LCID) of the audio language for playback.</span></span>

``` syntax
player.controls.currentAudioLanguage
      
```

## <a name="possible-values"></a><span data-ttu-id="c55ea-106">Valeurs possibles</span><span class="sxs-lookup"><span data-stu-id="c55ea-106">Possible Values</span></span>

<span data-ttu-id="c55ea-107">Cette propriété est un **nombre** en lecture/écriture (**long**).</span><span class="sxs-lookup"><span data-stu-id="c55ea-107">This property is a read/write **Number** (**long**).</span></span>

## <a name="remarks"></a><span data-ttu-id="c55ea-108">Notes</span><span class="sxs-lookup"><span data-stu-id="c55ea-108">Remarks</span></span>

<span data-ttu-id="c55ea-109">Un LCID identifie de façon unique un dialecte de langage particulier, appelé paramètres régionaux.</span><span class="sxs-lookup"><span data-stu-id="c55ea-109">An LCID uniquely identifies a particular language dialect, called a locale.</span></span>

<span data-ttu-id="c55ea-110">Pour le contenu Windows Media, les propriétés et les méthodes liées à la sélection de la langue ne prennent en charge qu’une seule sortie.</span><span class="sxs-lookup"><span data-stu-id="c55ea-110">For Windows Media-based content, properties and methods related to language selection only support a single output.</span></span>

<span data-ttu-id="c55ea-111">Lors de l’utilisation d’un contenu DVD, la spécification d’un LCID entraîne la sélection de la première piste audio disponible avec l’ID de langue spécifié.</span><span class="sxs-lookup"><span data-stu-id="c55ea-111">When working with DVD content, specifying an LCID will cause the first available audio track having the specified language ID to be selected.</span></span>

<span data-ttu-id="c55ea-112">**Lecteur Windows Media 10 Mobile :** Cette propriété accepte ou retourne uniquement le LCID de langue neutre (0).</span><span class="sxs-lookup"><span data-stu-id="c55ea-112">**Windows Media Player 10 Mobile:** This property only accepts or returns the language-neutral LCID (0).</span></span>

## <a name="requirements"></a><span data-ttu-id="c55ea-113">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="c55ea-113">Requirements</span></span>



| <span data-ttu-id="c55ea-114">Condition requise</span><span class="sxs-lookup"><span data-stu-id="c55ea-114">Requirement</span></span> | <span data-ttu-id="c55ea-115">Valeur</span><span class="sxs-lookup"><span data-stu-id="c55ea-115">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="c55ea-116">Version</span><span class="sxs-lookup"><span data-stu-id="c55ea-116">Version</span></span><br/> | <span data-ttu-id="c55ea-117">Lecteur Windows Media série 9 ou version ultérieure.</span><span class="sxs-lookup"><span data-stu-id="c55ea-117">Windows Media Player 9 Series or later.</span></span><br/>                                 |
| <span data-ttu-id="c55ea-118">DLL</span><span class="sxs-lookup"><span data-stu-id="c55ea-118">DLL</span></span><br/>     | <dl> <span data-ttu-id="c55ea-119"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="c55ea-119"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c55ea-120">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="c55ea-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c55ea-121">**Controls (objet)**</span><span class="sxs-lookup"><span data-stu-id="c55ea-121">**Controls Object**</span></span>](controls-object.md)
</dt> <dt>

[<span data-ttu-id="c55ea-122">**Controls. audioLanguageCount**</span><span class="sxs-lookup"><span data-stu-id="c55ea-122">**Controls.audioLanguageCount**</span></span>](controls-audiolanguagecount.md)
</dt> <dt>

[<span data-ttu-id="c55ea-123">**Controls. currentAudioLanguageIndex**</span><span class="sxs-lookup"><span data-stu-id="c55ea-123">**Controls.currentAudioLanguageIndex**</span></span>](controls-currentaudiolanguageindex.md)
</dt> <dt>

[<span data-ttu-id="c55ea-124">**Controls. getAudioLanguageDescription**</span><span class="sxs-lookup"><span data-stu-id="c55ea-124">**Controls.getAudioLanguageDescription**</span></span>](controls-getaudiolanguagedescription.md)
</dt> <dt>

[<span data-ttu-id="c55ea-125">**Controls. getAudioLanguageID**</span><span class="sxs-lookup"><span data-stu-id="c55ea-125">**Controls.getAudioLanguageID**</span></span>](controls-getaudiolanguageid.md)
</dt> <dt>

[<span data-ttu-id="c55ea-126">**Controls. getLanguageName**</span><span class="sxs-lookup"><span data-stu-id="c55ea-126">**Controls.getLanguageName**</span></span>](controls-getlanguagename.md)
</dt> </dl>

 

 





