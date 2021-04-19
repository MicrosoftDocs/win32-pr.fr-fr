---
title: Controls. getAudioLanguageID, méthode
description: La méthode getAudioLanguageID récupère l’identificateur de paramètres régionaux (LCID) pour un index de langue audio spécifié.
ms.assetid: 8134a7ce-bdc7-46b2-b10e-2bf1215b0de1
keywords:
- méthode getAudioLanguageID lecteur Windows Media
- méthode getAudioLanguageID lecteur Windows Media, classe de contrôles
- Classe Controls lecteur Windows Media, méthode getAudioLanguageID
topic_type:
- apiref
api_name:
- Controls.getAudioLanguageID
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9ab27e95edfc74fa7a9f57d2010bf86299c55dd4
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106525415"
---
# <a name="controlsgetaudiolanguageid-method"></a><span data-ttu-id="ac9e5-106">Controls. getAudioLanguageID, méthode</span><span class="sxs-lookup"><span data-stu-id="ac9e5-106">Controls.getAudioLanguageID method</span></span>

<span data-ttu-id="ac9e5-107">La méthode **getAudioLanguageID** récupère l’identificateur de paramètres régionaux (LCID) pour un index de langue audio spécifié.</span><span class="sxs-lookup"><span data-stu-id="ac9e5-107">The **getAudioLanguageID** method retrieves the locale identifier (LCID) for a specified audio language index.</span></span>

## <a name="syntax"></a><span data-ttu-id="ac9e5-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="ac9e5-108">Syntax</span></span>


```JScript
retVal = Controls.getAudioLanguageID(
  index
)
```



## <a name="parameters"></a><span data-ttu-id="ac9e5-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="ac9e5-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ac9e5-110">*index* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="ac9e5-110">*index* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ac9e5-111">**Nombre** (**long**) spécifiant l’index de langue audio.</span><span class="sxs-lookup"><span data-stu-id="ac9e5-111">**Number** (**long**) specifying the audio language index.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ac9e5-112">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="ac9e5-112">Return value</span></span>

<span data-ttu-id="ac9e5-113">Cette méthode retourne un **nombre** (**long**).</span><span class="sxs-lookup"><span data-stu-id="ac9e5-113">This method returns a **Number** (**long**).</span></span>

## <a name="remarks"></a><span data-ttu-id="ac9e5-114">Notes</span><span class="sxs-lookup"><span data-stu-id="ac9e5-114">Remarks</span></span>

<span data-ttu-id="ac9e5-115">Un LCID identifie de façon unique un dialecte de langage particulier, appelé paramètres régionaux.</span><span class="sxs-lookup"><span data-stu-id="ac9e5-115">An LCID uniquely identifies a particular language dialect, called a locale.</span></span>

<span data-ttu-id="ac9e5-116">Pour le contenu Windows Media, les propriétés et les méthodes liées à la sélection de la langue ne prennent en charge qu’une seule sortie.</span><span class="sxs-lookup"><span data-stu-id="ac9e5-116">For Windows Media-based content, properties and methods related to language selection only support a single output.</span></span>

<span data-ttu-id="ac9e5-117">**Lecteur Windows Media 10 Mobile :** Cette propriété retourne toujours le LCID de langue neutre (0).</span><span class="sxs-lookup"><span data-stu-id="ac9e5-117">**Windows Media Player 10 Mobile:** This property always returns the language-neutral LCID (0).</span></span>

## <a name="requirements"></a><span data-ttu-id="ac9e5-118">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="ac9e5-118">Requirements</span></span>



| <span data-ttu-id="ac9e5-119">Condition requise</span><span class="sxs-lookup"><span data-stu-id="ac9e5-119">Requirement</span></span> | <span data-ttu-id="ac9e5-120">Valeur</span><span class="sxs-lookup"><span data-stu-id="ac9e5-120">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="ac9e5-121">Version</span><span class="sxs-lookup"><span data-stu-id="ac9e5-121">Version</span></span><br/> | <span data-ttu-id="ac9e5-122">Lecteur Windows Media série 9 ou version ultérieure.</span><span class="sxs-lookup"><span data-stu-id="ac9e5-122">Windows Media Player 9 Series or later.</span></span><br/>                                 |
| <span data-ttu-id="ac9e5-123">DLL</span><span class="sxs-lookup"><span data-stu-id="ac9e5-123">DLL</span></span><br/>     | <dl> <span data-ttu-id="ac9e5-124"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="ac9e5-124"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ac9e5-125">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="ac9e5-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ac9e5-126">**Controls (objet)**</span><span class="sxs-lookup"><span data-stu-id="ac9e5-126">**Controls Object**</span></span>](controls-object.md)
</dt> <dt>

[<span data-ttu-id="ac9e5-127">**Controls. audioLanguageCount**</span><span class="sxs-lookup"><span data-stu-id="ac9e5-127">**Controls.audioLanguageCount**</span></span>](controls-audiolanguagecount.md)
</dt> <dt>

[<span data-ttu-id="ac9e5-128">**Controls. currentAudioLanguage**</span><span class="sxs-lookup"><span data-stu-id="ac9e5-128">**Controls.currentAudioLanguage**</span></span>](controls-currentaudiolanguage.md)
</dt> <dt>

[<span data-ttu-id="ac9e5-129">**Controls. currentAudioLanguageIndex**</span><span class="sxs-lookup"><span data-stu-id="ac9e5-129">**Controls.currentAudioLanguageIndex**</span></span>](controls-currentaudiolanguageindex.md)
</dt> <dt>

[<span data-ttu-id="ac9e5-130">**Controls. getAudioLanguageDescription**</span><span class="sxs-lookup"><span data-stu-id="ac9e5-130">**Controls.getAudioLanguageDescription**</span></span>](controls-getaudiolanguagedescription.md)
</dt> <dt>

[<span data-ttu-id="ac9e5-131">**Controls. getLanguageName**</span><span class="sxs-lookup"><span data-stu-id="ac9e5-131">**Controls.getLanguageName**</span></span>](controls-getlanguagename.md)
</dt> </dl>

 

 





