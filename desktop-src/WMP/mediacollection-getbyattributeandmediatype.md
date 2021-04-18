---
title: Méthode MediaCollection. getByAttributeAndMediaType
description: La méthode getByAttributeAndMediaType récupère un objet de sélection contenant des objets multimédias avec l’attribut et le type de média spécifiés.
ms.assetid: 75241b38-ae0e-4216-b405-af9a9c71f5ec
keywords:
- méthode getByAttributeAndMediaType lecteur Windows Media
- méthode getByAttributeAndMediaType lecteur Windows Media, classe MediaCollection
- Classe MediaCollection lecteur Windows Media, méthode getByAttributeAndMediaType
topic_type:
- apiref
api_name:
- MediaCollection.getByAttributeAndMediaType
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7e26abbf2f19d50ec6a10ebbafe12afae8576f34
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106528906"
---
# <a name="mediacollectiongetbyattributeandmediatype-method"></a><span data-ttu-id="601a4-106">Méthode MediaCollection. getByAttributeAndMediaType</span><span class="sxs-lookup"><span data-stu-id="601a4-106">MediaCollection.getByAttributeAndMediaType method</span></span>

<span data-ttu-id="601a4-107">La méthode **getByAttributeAndMediaType** récupère un objet de **sélection** contenant des objets **multimédias** avec l’attribut et le type de média spécifiés.</span><span class="sxs-lookup"><span data-stu-id="601a4-107">The **getByAttributeAndMediaType** method retrieves a **Playlist** object containing **Media** objects having the specified attribute and media type.</span></span>

## <a name="syntax"></a><span data-ttu-id="601a4-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="601a4-108">Syntax</span></span>


```JScript
retVal = MediaCollection.getByAttributeAndMediaType(
  attribute,
  value,
  mediaType
)
```



## <a name="parameters"></a><span data-ttu-id="601a4-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="601a4-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="601a4-110">*attribut* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="601a4-110">*attribute* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="601a4-111">**Chaîne** contenant l’attribut.</span><span class="sxs-lookup"><span data-stu-id="601a4-111">**String** containing the attribute.</span></span>

</dd> <dt>

<span data-ttu-id="601a4-112">*valeur* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="601a4-112">*value* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="601a4-113">**Chaîne** contenant la valeur.</span><span class="sxs-lookup"><span data-stu-id="601a4-113">**String** containing the value.</span></span>

</dd> <dt>

<span data-ttu-id="601a4-114">*MediaType* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="601a4-114">*mediaType* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="601a4-115">**Chaîne** contenant le type de média.</span><span class="sxs-lookup"><span data-stu-id="601a4-115">**String** containing the media type.</span></span> <span data-ttu-id="601a4-116">Doit contenir l’une des valeurs suivantes : « audio », « Video », « photo », « playlist » ou « other ».</span><span class="sxs-lookup"><span data-stu-id="601a4-116">Must contain one of the following values: "audio", "video", "photo", "playlist", or "other".</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="601a4-117">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="601a4-117">Return value</span></span>

<span data-ttu-id="601a4-118">Cette méthode retourne un objet **playlist**</span><span class="sxs-lookup"><span data-stu-id="601a4-118">This method returns a **Playlist** object</span></span>

## <a name="requirements"></a><span data-ttu-id="601a4-119">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="601a4-119">Requirements</span></span>



| <span data-ttu-id="601a4-120">Condition requise</span><span class="sxs-lookup"><span data-stu-id="601a4-120">Requirement</span></span> | <span data-ttu-id="601a4-121">Valeur</span><span class="sxs-lookup"><span data-stu-id="601a4-121">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="601a4-122">Version</span><span class="sxs-lookup"><span data-stu-id="601a4-122">Version</span></span><br/> | <span data-ttu-id="601a4-123">Lecteur Windows Media 11.</span><span class="sxs-lookup"><span data-stu-id="601a4-123">Windows Media Player 11.</span></span><br/>                                                |
| <span data-ttu-id="601a4-124">DLL</span><span class="sxs-lookup"><span data-stu-id="601a4-124">DLL</span></span><br/>     | <dl> <span data-ttu-id="601a4-125"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="601a4-125"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="601a4-126">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="601a4-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="601a4-127">**Référence d’attribut**</span><span class="sxs-lookup"><span data-stu-id="601a4-127">**Attribute Reference**</span></span>](attribute-reference.md)
</dt> <dt>

[<span data-ttu-id="601a4-128">**Objet MediaCollection**</span><span class="sxs-lookup"><span data-stu-id="601a4-128">**MediaCollection Object**</span></span>](mediacollection-object.md)
</dt> <dt>

[<span data-ttu-id="601a4-129">**Objet playlist**</span><span class="sxs-lookup"><span data-stu-id="601a4-129">**Playlist Object**</span></span>](playlist-object.md)
</dt> </dl>

 

 





