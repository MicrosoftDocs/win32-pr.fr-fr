---
title: Controls. getAudioLanguageDescription, méthode
description: La méthode getAudioLanguageDescription récupère la description de la langue audio correspondant à l’index de base 1 spécifié.
ms.assetid: 995a2568-f15f-4b92-9782-92ba5273f444
keywords:
- méthode getAudioLanguageDescription lecteur Windows Media
- méthode getAudioLanguageDescription lecteur Windows Media, classe de contrôles
- Classe Controls lecteur Windows Media, méthode getAudioLanguageDescription
topic_type:
- apiref
api_name:
- Controls.getAudioLanguageDescription
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1d28e82648a1047252402694f4948d2a2734f344
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106542520"
---
# <a name="controlsgetaudiolanguagedescription-method"></a><span data-ttu-id="e1bf4-106">Controls. getAudioLanguageDescription, méthode</span><span class="sxs-lookup"><span data-stu-id="e1bf4-106">Controls.getAudioLanguageDescription method</span></span>

<span data-ttu-id="e1bf4-107">La méthode **getAudioLanguageDescription** récupère la description de la langue audio correspondant à l’index de base 1 spécifié.</span><span class="sxs-lookup"><span data-stu-id="e1bf4-107">The **getAudioLanguageDescription** method retrieves the description for the audio language corresponding to the specified one-based index.</span></span>

## <a name="syntax"></a><span data-ttu-id="e1bf4-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="e1bf4-108">Syntax</span></span>


```JScript
strRetVal = Controls.getAudioLanguageDescription(
  index
)
```



## <a name="parameters"></a><span data-ttu-id="e1bf4-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="e1bf4-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e1bf4-110">*index* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="e1bf4-110">*index* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e1bf4-111">**Nombre** (**long**) spécifiant l’index de langue audio basé sur un.</span><span class="sxs-lookup"><span data-stu-id="e1bf4-111">**Number** (**long**) specifying the one-based audio language index.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e1bf4-112">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="e1bf4-112">Return value</span></span>

<span data-ttu-id="e1bf4-113">Cette méthode retourne une valeur de **chaîne** .</span><span class="sxs-lookup"><span data-stu-id="e1bf4-113">This method returns a **String** value.</span></span>

## <a name="remarks"></a><span data-ttu-id="e1bf4-114">Notes</span><span class="sxs-lookup"><span data-stu-id="e1bf4-114">Remarks</span></span>

<span data-ttu-id="e1bf4-115">Pour le contenu Windows Media, les propriétés et les méthodes liées à la sélection de la langue ne prennent en charge qu’une seule sortie.</span><span class="sxs-lookup"><span data-stu-id="e1bf4-115">For Windows Media-based content, properties and methods related to language selection only support a single output.</span></span>

<span data-ttu-id="e1bf4-116">Utilisez la propriété **audioLanguageCount** pour obtenir le nombre de langues audio prises en charge, puis accédez à une langue audio individuellement à l’aide d’un index de base un.</span><span class="sxs-lookup"><span data-stu-id="e1bf4-116">Use the **audioLanguageCount** property to get the number of supported audio languages, and then access an audio language individually by using a one-based index.</span></span>

<span data-ttu-id="e1bf4-117">**Lecteur Windows Media 10 Mobile :** Cette méthode n’est pas prise en charge.</span><span class="sxs-lookup"><span data-stu-id="e1bf4-117">**Windows Media Player 10 Mobile:** This method is not supported.</span></span>

## <a name="requirements"></a><span data-ttu-id="e1bf4-118">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="e1bf4-118">Requirements</span></span>



| <span data-ttu-id="e1bf4-119">Condition requise</span><span class="sxs-lookup"><span data-stu-id="e1bf4-119">Requirement</span></span> | <span data-ttu-id="e1bf4-120">Valeur</span><span class="sxs-lookup"><span data-stu-id="e1bf4-120">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="e1bf4-121">Version</span><span class="sxs-lookup"><span data-stu-id="e1bf4-121">Version</span></span><br/> | <span data-ttu-id="e1bf4-122">Lecteur Windows Media série 9 ou version ultérieure.</span><span class="sxs-lookup"><span data-stu-id="e1bf4-122">Windows Media Player 9 Series or later.</span></span><br/>                                 |
| <span data-ttu-id="e1bf4-123">DLL</span><span class="sxs-lookup"><span data-stu-id="e1bf4-123">DLL</span></span><br/>     | <dl> <span data-ttu-id="e1bf4-124"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="e1bf4-124"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e1bf4-125">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="e1bf4-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e1bf4-126">**Controls (objet)**</span><span class="sxs-lookup"><span data-stu-id="e1bf4-126">**Controls Object**</span></span>](controls-object.md)
</dt> <dt>

[<span data-ttu-id="e1bf4-127">**Controls. audioLanguageCount**</span><span class="sxs-lookup"><span data-stu-id="e1bf4-127">**Controls.audioLanguageCount**</span></span>](controls-audiolanguagecount.md)
</dt> <dt>

[<span data-ttu-id="e1bf4-128">**Controls. currentAudioLanguage**</span><span class="sxs-lookup"><span data-stu-id="e1bf4-128">**Controls.currentAudioLanguage**</span></span>](controls-currentaudiolanguage.md)
</dt> <dt>

[<span data-ttu-id="e1bf4-129">**Controls. currentAudioLanguageIndex**</span><span class="sxs-lookup"><span data-stu-id="e1bf4-129">**Controls.currentAudioLanguageIndex**</span></span>](controls-currentaudiolanguageindex.md)
</dt> <dt>

[<span data-ttu-id="e1bf4-130">**Controls. getAudioLanguageID**</span><span class="sxs-lookup"><span data-stu-id="e1bf4-130">**Controls.getAudioLanguageID**</span></span>](controls-getaudiolanguageid.md)
</dt> <dt>

[<span data-ttu-id="e1bf4-131">**Controls. getLanguageName**</span><span class="sxs-lookup"><span data-stu-id="e1bf4-131">**Controls.getLanguageName**</span></span>](controls-getlanguagename.md)
</dt> </dl>

 

 





