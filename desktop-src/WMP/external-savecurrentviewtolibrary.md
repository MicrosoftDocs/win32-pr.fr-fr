---
title: External. saveCurrentViewToLibrary, méthode
description: La méthode saveCurrentViewToLibrary crée une sélection à partir des éléments multimédias dans l’affichage actuel et enregistre la sélection dans la bibliothèque locale.
ms.assetid: cd87e932-d599-4298-bbee-6755999dda15
keywords:
- méthode saveCurrentViewToLibrary lecteur Windows Media
- méthode saveCurrentViewToLibrary lecteur Windows Media, classe externe
- Classe externe lecteur Windows Media, méthode saveCurrentViewToLibrary
topic_type:
- apiref
api_name:
- External.saveCurrentViewToLibrary
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 212f590f03c32821c0774c4898720c92558ecc73
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106537362"
---
# <a name="externalsavecurrentviewtolibrary-method"></a><span data-ttu-id="1ddca-106">External. saveCurrentViewToLibrary, méthode</span><span class="sxs-lookup"><span data-stu-id="1ddca-106">External.saveCurrentViewToLibrary method</span></span>

<span data-ttu-id="1ddca-107">La méthode **saveCurrentViewToLibrary** crée une sélection à partir des éléments multimédias dans l’affichage actuel et enregistre la sélection dans la bibliothèque locale.</span><span class="sxs-lookup"><span data-stu-id="1ddca-107">The **saveCurrentViewToLibrary** method creates a playlist from the media items in the current view and saves the playlist in the local library.</span></span>

## <a name="syntax"></a><span data-ttu-id="1ddca-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="1ddca-108">Syntax</span></span>


```JScript
External.saveCurrentViewToLibrary(
  FriendlyListName,
  Local
)
```



## <a name="parameters"></a><span data-ttu-id="1ddca-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="1ddca-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1ddca-110">*FriendlyListName* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="1ddca-110">*FriendlyListName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1ddca-111">**Chaîne** qui spécifie un nom convivial pour la sélection.</span><span class="sxs-lookup"><span data-stu-id="1ddca-111">**String** that specifies a friendly name for the playlist.</span></span> <span data-ttu-id="1ddca-112">Le lecteur Windows Media affiche ce nom dans son interface utilisateur.</span><span class="sxs-lookup"><span data-stu-id="1ddca-112">Windows Media Player displays this name in its user interface.</span></span>

</dd> <dt>

<span data-ttu-id="1ddca-113">*Local* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="1ddca-113">*Local* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1ddca-114">**Valeur booléenne** qui spécifie si la sélection est dynamique ou statique.</span><span class="sxs-lookup"><span data-stu-id="1ddca-114">**Boolean** that specifies whether the playlist is dynamic or static.</span></span> <span data-ttu-id="1ddca-115">**True** spécifie Dynamic, et **false** spécifie static.</span><span class="sxs-lookup"><span data-stu-id="1ddca-115">**TRUE** specifies dynamic, and **FALSE** specifies static.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1ddca-116">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="1ddca-116">Return value</span></span>

<span data-ttu-id="1ddca-117">Cette méthode ne retourne pas de valeur.</span><span class="sxs-lookup"><span data-stu-id="1ddca-117">This method does not return a value.</span></span>

## <a name="requirements"></a><span data-ttu-id="1ddca-118">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="1ddca-118">Requirements</span></span>



| <span data-ttu-id="1ddca-119">Condition requise</span><span class="sxs-lookup"><span data-stu-id="1ddca-119">Requirement</span></span> | <span data-ttu-id="1ddca-120">Valeur</span><span class="sxs-lookup"><span data-stu-id="1ddca-120">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="1ddca-121">Version</span><span class="sxs-lookup"><span data-stu-id="1ddca-121">Version</span></span><br/> | <span data-ttu-id="1ddca-122">Lecteur Windows Media 11</span><span class="sxs-lookup"><span data-stu-id="1ddca-122">Windows Media Player 11</span></span><br/>                                                 |
| <span data-ttu-id="1ddca-123">DLL</span><span class="sxs-lookup"><span data-stu-id="1ddca-123">DLL</span></span><br/>     | <dl> <span data-ttu-id="1ddca-124"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="1ddca-124"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1ddca-125">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="1ddca-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1ddca-126">**Objet externe pour les magasins de type 1 en ligne**</span><span class="sxs-lookup"><span data-stu-id="1ddca-126">**External Object for Type 1 Online Stores**</span></span>](external-object-for-type-1-online-stores.md)
</dt> </dl>

 

 





