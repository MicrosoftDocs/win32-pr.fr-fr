---
title: Controls. getLanguageName, méthode
description: La méthode getLanguageName récupère le nom de la langue audio avec l’identificateur de paramètres régionaux (LCID) spécifié.
ms.assetid: 9e142c89-92bf-476f-bae7-b94f5b5ebe01
keywords:
- méthode getLanguageName lecteur Windows Media
- méthode getLanguageName lecteur Windows Media, classe de contrôles
- Classe Controls lecteur Windows Media, méthode getLanguageName
topic_type:
- apiref
api_name:
- Controls.getLanguageName
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 798a6b22f344953df716e4df4ed8a9a0daff2a7b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106525589"
---
# <a name="controlsgetlanguagename-method"></a><span data-ttu-id="2f7f7-106">Controls. getLanguageName, méthode</span><span class="sxs-lookup"><span data-stu-id="2f7f7-106">Controls.getLanguageName method</span></span>

<span data-ttu-id="2f7f7-107">La méthode **getLanguageName** récupère le nom de la langue audio avec l’identificateur de paramètres régionaux (LCID) spécifié.</span><span class="sxs-lookup"><span data-stu-id="2f7f7-107">The **getLanguageName** method retrieves the name of the audio language with the specified locale identifier (LCID).</span></span>

## <a name="syntax"></a><span data-ttu-id="2f7f7-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="2f7f7-108">Syntax</span></span>


```JScript
strRetVal = Controls.getLanguageName(
  LCID
)
```



## <a name="parameters"></a><span data-ttu-id="2f7f7-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="2f7f7-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2f7f7-110">*LCID* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="2f7f7-110">*LCID* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2f7f7-111">**Nombre** (**long**) spécifiant le LCID.</span><span class="sxs-lookup"><span data-stu-id="2f7f7-111">**Number** (**long**) specifying the LCID.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2f7f7-112">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="2f7f7-112">Return value</span></span>

<span data-ttu-id="2f7f7-113">Cette méthode retourne une **chaîne**.</span><span class="sxs-lookup"><span data-stu-id="2f7f7-113">This method returns a **String**.</span></span>

## <a name="remarks"></a><span data-ttu-id="2f7f7-114">Notes</span><span class="sxs-lookup"><span data-stu-id="2f7f7-114">Remarks</span></span>

<span data-ttu-id="2f7f7-115">Un LCID identifie de façon unique un dialecte de langage particulier, appelé paramètres régionaux.</span><span class="sxs-lookup"><span data-stu-id="2f7f7-115">An LCID uniquely identifies a particular language dialect, called a locale.</span></span>

<span data-ttu-id="2f7f7-116">Pour le contenu Windows Media, les propriétés et les méthodes liées à la sélection de la langue ne prennent en charge qu’une seule sortie.</span><span class="sxs-lookup"><span data-stu-id="2f7f7-116">For Windows Media-based content, properties and methods related to language selection only support a single output.</span></span>

## <a name="requirements"></a><span data-ttu-id="2f7f7-117">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="2f7f7-117">Requirements</span></span>



| <span data-ttu-id="2f7f7-118">Condition requise</span><span class="sxs-lookup"><span data-stu-id="2f7f7-118">Requirement</span></span> | <span data-ttu-id="2f7f7-119">Valeur</span><span class="sxs-lookup"><span data-stu-id="2f7f7-119">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="2f7f7-120">Version</span><span class="sxs-lookup"><span data-stu-id="2f7f7-120">Version</span></span><br/> | <span data-ttu-id="2f7f7-121">Lecteur Windows Media série 9 ou version ultérieure.</span><span class="sxs-lookup"><span data-stu-id="2f7f7-121">Windows Media Player 9 Series or later.</span></span><br/>                                 |
| <span data-ttu-id="2f7f7-122">DLL</span><span class="sxs-lookup"><span data-stu-id="2f7f7-122">DLL</span></span><br/>     | <dl> <span data-ttu-id="2f7f7-123"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="2f7f7-123"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2f7f7-124">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="2f7f7-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2f7f7-125">**Controls (objet)**</span><span class="sxs-lookup"><span data-stu-id="2f7f7-125">**Controls Object**</span></span>](controls-object.md)
</dt> <dt>

[<span data-ttu-id="2f7f7-126">**Controls. audioLanguageCount**</span><span class="sxs-lookup"><span data-stu-id="2f7f7-126">**Controls.audioLanguageCount**</span></span>](controls-audiolanguagecount.md)
</dt> <dt>

[<span data-ttu-id="2f7f7-127">**Controls. currentAudioLanguage**</span><span class="sxs-lookup"><span data-stu-id="2f7f7-127">**Controls.currentAudioLanguage**</span></span>](controls-currentaudiolanguage.md)
</dt> <dt>

[<span data-ttu-id="2f7f7-128">**Controls. currentAudioLanguageIndex**</span><span class="sxs-lookup"><span data-stu-id="2f7f7-128">**Controls.currentAudioLanguageIndex**</span></span>](controls-currentaudiolanguageindex.md)
</dt> <dt>

[<span data-ttu-id="2f7f7-129">**Controls. getAudioLanguageDescription**</span><span class="sxs-lookup"><span data-stu-id="2f7f7-129">**Controls.getAudioLanguageDescription**</span></span>](controls-getaudiolanguagedescription.md)
</dt> <dt>

[<span data-ttu-id="2f7f7-130">**Controls. getAudioLanguageID**</span><span class="sxs-lookup"><span data-stu-id="2f7f7-130">**Controls.getAudioLanguageID**</span></span>](controls-getaudiolanguageid.md)
</dt> </dl>

 

 





