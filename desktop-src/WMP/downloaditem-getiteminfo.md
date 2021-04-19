---
title: Méthode DownloadItem. getItemInfo
description: Remarque Cette section décrit les fonctionnalités conçues pour être utilisées par les magasins en ligne. L’utilisation de cette fonctionnalité en dehors du contexte d’un magasin en ligne n’est pas prise en charge. La méthode getItemInfo récupère la valeur d’un attribut pour l’élément de téléchargement.
ms.assetid: da885611-b4a0-4264-8b32-13cc6f87d6e9
keywords:
- méthode getItemInfo lecteur Windows Media
- méthode getItemInfo lecteur Windows Media, classe DownloadItem
- Classe DownloadItem lecteur Windows Media, méthode getItemInfo
topic_type:
- apiref
api_name:
- DownloadItem.getItemInfo
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1367e5c7a8990a9172ee758d2b811b9074ed02fc
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106530299"
---
# <a name="downloaditemgetiteminfo-method"></a><span data-ttu-id="77495-108">Méthode DownloadItem. getItemInfo</span><span class="sxs-lookup"><span data-stu-id="77495-108">DownloadItem.getItemInfo method</span></span>

> [!Note]  
> <span data-ttu-id="77495-109">Cette section décrit les fonctionnalités conçues pour être utilisées par les magasins en ligne.</span><span class="sxs-lookup"><span data-stu-id="77495-109">This section describes functionality designed for use by online stores.</span></span> <span data-ttu-id="77495-110">L’utilisation de cette fonctionnalité en dehors du contexte d’un magasin en ligne n’est pas prise en charge.</span><span class="sxs-lookup"><span data-stu-id="77495-110">Use of this functionality outside the context of an online store is not supported.</span></span>

 

<span data-ttu-id="77495-111">La méthode **getItemInfo** récupère la valeur d’un attribut pour l’élément de téléchargement.</span><span class="sxs-lookup"><span data-stu-id="77495-111">The **getItemInfo** method retrieves the value of an attribute for the download item.</span></span>

## <a name="syntax"></a><span data-ttu-id="77495-112">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="77495-112">Syntax</span></span>


```JScript
strRetVal = DownloadItem.getItemInfo(
  itemname
)
```



## <a name="parameters"></a><span data-ttu-id="77495-113">Paramètres</span><span class="sxs-lookup"><span data-stu-id="77495-113">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="77495-114">*ItemName* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="77495-114">*itemname* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="77495-115">**Chaîne** contenant le nom de l’attribut.</span><span class="sxs-lookup"><span data-stu-id="77495-115">**String** containing the attribute name.</span></span> <span data-ttu-id="77495-116">Les valeurs prises en charge sont AlbumArtist, album, Duration, WM/Provider, title, UserRating et WM/TrackNumber.</span><span class="sxs-lookup"><span data-stu-id="77495-116">Supported values are AlbumArtist, Album, Duration, WM/Provider, Title, UserRating, and WM/TrackNumber.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="77495-117">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="77495-117">Return value</span></span>

<span data-ttu-id="77495-118">Cette méthode retourne une **chaîne** contenant la valeur de l’attribut spécifié par *ItemName*.</span><span class="sxs-lookup"><span data-stu-id="77495-118">This method returns a **String** containing the value of the attribute specified by *itemname*.</span></span>

## <a name="remarks"></a><span data-ttu-id="77495-119">Notes</span><span class="sxs-lookup"><span data-stu-id="77495-119">Remarks</span></span>

<span data-ttu-id="77495-120">Cette méthode récupère les attributs spécifiés à l’aide de la chaîne de description BITS.</span><span class="sxs-lookup"><span data-stu-id="77495-120">This method retrieves attributes specified using the BITS description string.</span></span> <span data-ttu-id="77495-121">Consultez la [Convention de travail bits du lecteur Windows Media](windows-media-player-bits-job-convention.md).</span><span class="sxs-lookup"><span data-stu-id="77495-121">See [Windows Media Player BITS Job Convention](windows-media-player-bits-job-convention.md).</span></span>

<span data-ttu-id="77495-122">Cette méthode est prise en charge pour le téléchargement en arrière-plan.</span><span class="sxs-lookup"><span data-stu-id="77495-122">This method is supported for background downloading.</span></span> <span data-ttu-id="77495-123">Votre code ne doit pas appeler cette méthode lors de l’utilisation d’un téléchargement en temps réel.</span><span class="sxs-lookup"><span data-stu-id="77495-123">Your code should not call this method when using real-time downloading.</span></span>

<span data-ttu-id="77495-124">Cette méthode peut récupérer des informations sur les tâches BITS ajoutées au cours de la session du lecteur Windows Media en cours uniquement.</span><span class="sxs-lookup"><span data-stu-id="77495-124">This method can retrieve information for BITS jobs added during the current Windows Media Player session only.</span></span>

## <a name="requirements"></a><span data-ttu-id="77495-125">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="77495-125">Requirements</span></span>



| <span data-ttu-id="77495-126">Condition requise</span><span class="sxs-lookup"><span data-stu-id="77495-126">Requirement</span></span> | <span data-ttu-id="77495-127">Valeur</span><span class="sxs-lookup"><span data-stu-id="77495-127">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="77495-128">Version</span><span class="sxs-lookup"><span data-stu-id="77495-128">Version</span></span><br/> | <span data-ttu-id="77495-129">Lecteur Windows Media 10 ou version ultérieure</span><span class="sxs-lookup"><span data-stu-id="77495-129">Windows Media Player 10 or later</span></span><br/>                                        |
| <span data-ttu-id="77495-130">DLL</span><span class="sxs-lookup"><span data-stu-id="77495-130">DLL</span></span><br/>     | <dl> <span data-ttu-id="77495-131"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="77495-131"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="77495-132">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="77495-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="77495-133">**DownloadItem. type**</span><span class="sxs-lookup"><span data-stu-id="77495-133">**DownloadItem.type**</span></span>](downloaditem-type.md)
</dt> <dt>

[<span data-ttu-id="77495-134">**Objet DownloadItem**</span><span class="sxs-lookup"><span data-stu-id="77495-134">**DownloadItem Object**</span></span>](downloaditem-object.md)
</dt> </dl>

 

 





