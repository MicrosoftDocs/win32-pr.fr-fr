---
title: Controls. currentAudioLanguageIndex
description: La propriété currentAudioLanguageIndex spécifie ou récupère l’index de base un qui correspond au langage audio pour la lecture.
ms.assetid: 9a1ae887-4e64-4758-a8a2-bf2e10a7a5c7
keywords:
- Controls. currentAudioLanguageIndex Windows Media Player
topic_type:
- apiref
api_name:
- Controls.currentAudioLanguageIndex
api_location:
- wmp.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cf1eb87873170c486782368f431f4fa8e3597b20
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106534781"
---
# <a name="controlscurrentaudiolanguageindex"></a><span data-ttu-id="16d25-104">Controls. currentAudioLanguageIndex</span><span class="sxs-lookup"><span data-stu-id="16d25-104">Controls.currentAudioLanguageIndex</span></span>

<span data-ttu-id="16d25-105">La propriété **currentAudioLanguageIndex** spécifie ou récupère l’index de base un qui correspond au langage audio pour la lecture.</span><span class="sxs-lookup"><span data-stu-id="16d25-105">The **currentAudioLanguageIndex** property specifies or retrieves the one-based index that corresponds to the audio language for playback.</span></span>

``` syntax
player.controls.currentAudioLanguageIndex
      
```

## <a name="possible-values"></a><span data-ttu-id="16d25-106">Valeurs possibles</span><span class="sxs-lookup"><span data-stu-id="16d25-106">Possible Values</span></span>

<span data-ttu-id="16d25-107">Cette propriété est un **nombre** en lecture/écriture (**long**).</span><span class="sxs-lookup"><span data-stu-id="16d25-107">This property is a read/write **Number** (**long**).</span></span>

## <a name="remarks"></a><span data-ttu-id="16d25-108">Notes</span><span class="sxs-lookup"><span data-stu-id="16d25-108">Remarks</span></span>

<span data-ttu-id="16d25-109">Pour le contenu Windows Media, les propriétés et les méthodes liées à la sélection de la langue ne prennent en charge qu’une seule sortie.</span><span class="sxs-lookup"><span data-stu-id="16d25-109">For Windows Media-based content, properties and methods related to language selection only support a single output.</span></span>

<span data-ttu-id="16d25-110">Utilisez la propriété **audioLanguageCount** pour connaître le nombre de langues audio prises en charge.</span><span class="sxs-lookup"><span data-stu-id="16d25-110">Use the **audioLanguageCount** property to get the number of supported audio languages.</span></span>

<span data-ttu-id="16d25-111">**Lecteur Windows Media 10 Mobile :** Cette propriété accepte ou retourne uniquement la valeur 0.</span><span class="sxs-lookup"><span data-stu-id="16d25-111">**Windows Media Player 10 Mobile:** This property only accepts or returns 0.</span></span>

## <a name="requirements"></a><span data-ttu-id="16d25-112">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="16d25-112">Requirements</span></span>



| <span data-ttu-id="16d25-113">Condition requise</span><span class="sxs-lookup"><span data-stu-id="16d25-113">Requirement</span></span> | <span data-ttu-id="16d25-114">Valeur</span><span class="sxs-lookup"><span data-stu-id="16d25-114">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="16d25-115">Version</span><span class="sxs-lookup"><span data-stu-id="16d25-115">Version</span></span><br/> | <span data-ttu-id="16d25-116">Lecteur Windows Media série 9 ou version ultérieure.</span><span class="sxs-lookup"><span data-stu-id="16d25-116">Windows Media Player 9 Series or later.</span></span><br/>                                 |
| <span data-ttu-id="16d25-117">DLL</span><span class="sxs-lookup"><span data-stu-id="16d25-117">DLL</span></span><br/>     | <dl> <span data-ttu-id="16d25-118"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="16d25-118"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="16d25-119">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="16d25-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="16d25-120">**Controls (objet)**</span><span class="sxs-lookup"><span data-stu-id="16d25-120">**Controls Object**</span></span>](controls-object.md)
</dt> <dt>

[<span data-ttu-id="16d25-121">**Controls. audioLanguageCount**</span><span class="sxs-lookup"><span data-stu-id="16d25-121">**Controls.audioLanguageCount**</span></span>](controls-audiolanguagecount.md)
</dt> <dt>

[<span data-ttu-id="16d25-122">**Controls. currentAudioLanguage**</span><span class="sxs-lookup"><span data-stu-id="16d25-122">**Controls.currentAudioLanguage**</span></span>](controls-currentaudiolanguage.md)
</dt> <dt>

[<span data-ttu-id="16d25-123">**Controls. getAudioLanguageDescription**</span><span class="sxs-lookup"><span data-stu-id="16d25-123">**Controls.getAudioLanguageDescription**</span></span>](controls-getaudiolanguagedescription.md)
</dt> <dt>

[<span data-ttu-id="16d25-124">**Controls. getAudioLanguageID**</span><span class="sxs-lookup"><span data-stu-id="16d25-124">**Controls.getAudioLanguageID**</span></span>](controls-getaudiolanguageid.md)
</dt> <dt>

[<span data-ttu-id="16d25-125">**Controls. getLanguageName**</span><span class="sxs-lookup"><span data-stu-id="16d25-125">**Controls.getLanguageName**</span></span>](controls-getlanguagename.md)
</dt> </dl>

 

 





