---
title: Player. newMedia, méthode
description: La méthode newMedia crée un nouvel objet multimédia.
ms.assetid: fccf1559-bac3-4edf-bd88-da2c72cdec21
keywords:
- méthode newMedia lecteur Windows Media
- méthode newMedia lecteur Windows Media, classe Player
- Classe player lecteur Windows Media, méthode newMedia
topic_type:
- apiref
api_name:
- Player.newMedia
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: aaafb97f836135aa9dd112372b1931c8561cb40b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106545646"
---
# <a name="playernewmedia-method"></a><span data-ttu-id="e99d8-106">Player. newMedia, méthode</span><span class="sxs-lookup"><span data-stu-id="e99d8-106">Player.newMedia method</span></span>

<span data-ttu-id="e99d8-107">La méthode **newMedia** crée un nouvel objet **multimédia** .</span><span class="sxs-lookup"><span data-stu-id="e99d8-107">The **newMedia** method creates a new **Media** object.</span></span>

## <a name="syntax"></a><span data-ttu-id="e99d8-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="e99d8-108">Syntax</span></span>


```JScript
retVal = Player.newMedia(
  URL
)
```



## <a name="parameters"></a><span data-ttu-id="e99d8-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="e99d8-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e99d8-110">*URL* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="e99d8-110">*URL* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e99d8-111">**Chaîne** contenant l’URL du fichier multimédia numérique avec lequel créer l’objet **multimédia** .</span><span class="sxs-lookup"><span data-stu-id="e99d8-111">**String** containing the URL of the digital media file to create the **Media** object with.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e99d8-112">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="e99d8-112">Return value</span></span>

<span data-ttu-id="e99d8-113">Cette méthode retourne un objet **multimédia** .</span><span class="sxs-lookup"><span data-stu-id="e99d8-113">This method returns a **Media** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="e99d8-114">Notes</span><span class="sxs-lookup"><span data-stu-id="e99d8-114">Remarks</span></span>

<span data-ttu-id="e99d8-115">Le paramètre *URL* ne doit pas être une chaîne vide ou avoir la valeur null.</span><span class="sxs-lookup"><span data-stu-id="e99d8-115">The *URL* parameter must not be an empty string or null.</span></span>

## <a name="requirements"></a><span data-ttu-id="e99d8-116">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="e99d8-116">Requirements</span></span>



| <span data-ttu-id="e99d8-117">Condition requise</span><span class="sxs-lookup"><span data-stu-id="e99d8-117">Requirement</span></span> | <span data-ttu-id="e99d8-118">Valeur</span><span class="sxs-lookup"><span data-stu-id="e99d8-118">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="e99d8-119">Version</span><span class="sxs-lookup"><span data-stu-id="e99d8-119">Version</span></span><br/> | <span data-ttu-id="e99d8-120">Lecteur Windows Media série 9 ou version ultérieure.</span><span class="sxs-lookup"><span data-stu-id="e99d8-120">Windows Media Player 9 Series or later.</span></span><br/>                                 |
| <span data-ttu-id="e99d8-121">DLL</span><span class="sxs-lookup"><span data-stu-id="e99d8-121">DLL</span></span><br/>     | <dl> <span data-ttu-id="e99d8-122"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="e99d8-122"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e99d8-123">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="e99d8-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e99d8-124">**Objet Player**</span><span class="sxs-lookup"><span data-stu-id="e99d8-124">**Player Object**</span></span>](player-object.md)
</dt> </dl>

 

 





