---
title: Événement Player. AudioLanguageChange
description: L’événement AudioLanguageChange se produit lorsque le langage audio actuel change. | Événement Player. AudioLanguageChange
ms.assetid: 29006a51-1b72-4fab-9906-8a0af3d92560
keywords:
- Événement AudioLanguageChange lecteur Windows Media
- Événement AudioLanguageChange lecteur Windows Media, classe Player
- Classe de lecteur Windows Media Player, événement AudioLanguageChange
topic_type:
- apiref
api_name:
- Player.AudioLanguageChange
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e84809a966280c379f7051e500b4e385d640f890
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106542317"
---
# <a name="playeraudiolanguagechange-event"></a><span data-ttu-id="1cef6-107">Événement Player. AudioLanguageChange</span><span class="sxs-lookup"><span data-stu-id="1cef6-107">Player.AudioLanguageChange event</span></span>

<span data-ttu-id="1cef6-108">L’événement **AudioLanguageChange** se produit lorsque le langage audio actuel change.</span><span class="sxs-lookup"><span data-stu-id="1cef6-108">The **AudioLanguageChange** event occurs when the current audio language changes.</span></span>

## <a name="syntax"></a><span data-ttu-id="1cef6-109">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="1cef6-109">Syntax</span></span>


```JScript
Player.AudioLanguageChange(
  LangID
)
```



## <a name="parameters"></a><span data-ttu-id="1cef6-110">Paramètres</span><span class="sxs-lookup"><span data-stu-id="1cef6-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1cef6-111">*LangID*</span><span class="sxs-lookup"><span data-stu-id="1cef6-111">*LangID*</span></span> 
</dt> <dd>

<span data-ttu-id="1cef6-112">**Nombre** (**long**) spécifiant le nouvel identificateur de paramètres régionaux (LCID).</span><span class="sxs-lookup"><span data-stu-id="1cef6-112">**Number** (**long**) specifying the new locale identifier (LCID).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1cef6-113">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="1cef6-113">Return value</span></span>

<span data-ttu-id="1cef6-114">Cet événement ne retourne pas de valeur.</span><span class="sxs-lookup"><span data-stu-id="1cef6-114">This event does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="1cef6-115">Notes</span><span class="sxs-lookup"><span data-stu-id="1cef6-115">Remarks</span></span>

<span data-ttu-id="1cef6-116">Un LCID identifie de façon unique un dialecte de langage particulier, appelé paramètres régionaux.</span><span class="sxs-lookup"><span data-stu-id="1cef6-116">An LCID uniquely identifies a particular language dialect, called a locale.</span></span>

<span data-ttu-id="1cef6-117">La valeur des paramètres d’événement est spécifiée par le lecteur Windows Media et est accessible ou transmise à une méthode dans un fichier Microsoft JScript importé en utilisant le nom de paramètre donné.</span><span class="sxs-lookup"><span data-stu-id="1cef6-117">The value of event parameters is specified by Windows Media Player, and can be accessed or passed to a method in an imported Microsoft JScript file by using the parameter name given.</span></span> <span data-ttu-id="1cef6-118">Ce nom de paramètre doit être tapé exactement comme indiqué, y compris la mise en majuscules.</span><span class="sxs-lookup"><span data-stu-id="1cef6-118">This parameter name must be typed exactly as shown, including capitalization.</span></span>

<span data-ttu-id="1cef6-119">**Lecteur Windows Media 10 Mobile :** Cet événement n’est pas pris en charge.</span><span class="sxs-lookup"><span data-stu-id="1cef6-119">**Windows Media Player 10 Mobile:** This event is not supported.</span></span>

## <a name="requirements"></a><span data-ttu-id="1cef6-120">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="1cef6-120">Requirements</span></span>



| <span data-ttu-id="1cef6-121">Condition requise</span><span class="sxs-lookup"><span data-stu-id="1cef6-121">Requirement</span></span> | <span data-ttu-id="1cef6-122">Valeur</span><span class="sxs-lookup"><span data-stu-id="1cef6-122">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="1cef6-123">Version</span><span class="sxs-lookup"><span data-stu-id="1cef6-123">Version</span></span><br/> | <span data-ttu-id="1cef6-124">Lecteur Windows Media série 9 ou version ultérieure.</span><span class="sxs-lookup"><span data-stu-id="1cef6-124">Windows Media Player 9 Series or later.</span></span><br/>                                 |
| <span data-ttu-id="1cef6-125">DLL</span><span class="sxs-lookup"><span data-stu-id="1cef6-125">DLL</span></span><br/>     | <dl> <span data-ttu-id="1cef6-126"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="1cef6-126"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1cef6-127">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="1cef6-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1cef6-128">**Controls. currentAudioLanguage**</span><span class="sxs-lookup"><span data-stu-id="1cef6-128">**Controls.currentAudioLanguage**</span></span>](controls-currentaudiolanguage.md)
</dt> <dt>

[<span data-ttu-id="1cef6-129">**Objet Player**</span><span class="sxs-lookup"><span data-stu-id="1cef6-129">**Player Object**</span></span>](player-object.md)
</dt> </dl>

 

 





