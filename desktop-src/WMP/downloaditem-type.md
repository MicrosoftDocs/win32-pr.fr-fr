---
title: DownloadItem. type
description: Remarque Cette section décrit les fonctionnalités conçues pour être utilisées par les magasins en ligne. L’utilisation de cette fonctionnalité en dehors du contexte d’un magasin en ligne n’est pas prise en charge. La propriété type récupère le type du téléchargement.
ms.assetid: 58ffb8a3-5410-492b-bb0f-9130ed209b78
keywords:
- DownloadItem. type lecteur Windows Media
topic_type:
- apiref
api_name:
- DownloadItem.type
api_location:
- wmp.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4cdcf21ce7443d7730d4a75518fb4749af0b9e52
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106526011"
---
# <a name="downloaditemtype"></a><span data-ttu-id="d6b4c-106">DownloadItem. type</span><span class="sxs-lookup"><span data-stu-id="d6b4c-106">DownloadItem.type</span></span>

> [!Note]  
> <span data-ttu-id="d6b4c-107">Cette section décrit les fonctionnalités conçues pour être utilisées par les magasins en ligne.</span><span class="sxs-lookup"><span data-stu-id="d6b4c-107">This section describes functionality designed for use by online stores.</span></span> <span data-ttu-id="d6b4c-108">L’utilisation de cette fonctionnalité en dehors du contexte d’un magasin en ligne n’est pas prise en charge.</span><span class="sxs-lookup"><span data-stu-id="d6b4c-108">Use of this functionality outside the context of an online store is not supported.</span></span>

 

<span data-ttu-id="d6b4c-109">La propriété **type** récupère le type du téléchargement.</span><span class="sxs-lookup"><span data-stu-id="d6b4c-109">The **type** property retrieves the type of the download.</span></span>

## <a name="syntax"></a><span data-ttu-id="d6b4c-110">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="d6b4c-110">Syntax</span></span>

``` syntax
DownloadManager.getDownloadCollection(
        collectionId
        ).item(
        itemId
        ).type
      
```

## <a name="possible-values"></a><span data-ttu-id="d6b4c-111">Valeurs possibles</span><span class="sxs-lookup"><span data-stu-id="d6b4c-111">Possible Values</span></span>

<span data-ttu-id="d6b4c-112">Cette propriété est une **chaîne** en lecture seule qui contient l’une des valeurs suivantes.</span><span class="sxs-lookup"><span data-stu-id="d6b4c-112">This property is a read-only **String** containing one of the following values.</span></span>



| <span data-ttu-id="d6b4c-113">Valeur</span><span class="sxs-lookup"><span data-stu-id="d6b4c-113">Value</span></span>      | <span data-ttu-id="d6b4c-114">Description</span><span class="sxs-lookup"><span data-stu-id="d6b4c-114">Description</span></span>                                                                                                                                                                            |
|------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d6b4c-115">background</span><span class="sxs-lookup"><span data-stu-id="d6b4c-115">background</span></span> | <span data-ttu-id="d6b4c-116">(Windows XP uniquement.) Le téléchargement se produit en tant que processus en arrière-plan, car le temps processeur devient disponible.</span><span class="sxs-lookup"><span data-stu-id="d6b4c-116">(Windows XP only.) The download occurs as a background process as processor time becomes available.</span></span> <span data-ttu-id="d6b4c-117">Les États de téléchargement persistent même lorsque Windows Media Player ou Windows XP est arrêté.</span><span class="sxs-lookup"><span data-stu-id="d6b4c-117">Download states persist even when Windows Media Player or Windows XP is shut down.</span></span> |
| <span data-ttu-id="d6b4c-118">temps réel</span><span class="sxs-lookup"><span data-stu-id="d6b4c-118">real time</span></span>  | <span data-ttu-id="d6b4c-119">(Tous les systèmes d’exploitation pris en charge.) Le téléchargement a lieu en même temps.</span><span class="sxs-lookup"><span data-stu-id="d6b4c-119">(All supported operating systems.) The download occurs all at once.</span></span> <span data-ttu-id="d6b4c-120">Aucun État de téléchargement n’est conservé entre les sessions.</span><span class="sxs-lookup"><span data-stu-id="d6b4c-120">No download states persist between sessions.</span></span>                                                                       |



 

## <a name="remarks"></a><span data-ttu-id="d6b4c-121">Notes</span><span class="sxs-lookup"><span data-stu-id="d6b4c-121">Remarks</span></span>

<span data-ttu-id="d6b4c-122">Chaque type de téléchargement présente des avantages et des inconvénients.</span><span class="sxs-lookup"><span data-stu-id="d6b4c-122">Each type of download has advantages and disadvantages.</span></span> <span data-ttu-id="d6b4c-123">Le téléchargement en arrière-plan permet à l’utilisateur de passer à d’autres tâches et même de redémarrer Windows sans annuler le téléchargement, mais prend plus de temps pour effectuer le téléchargement et n’est pris en charge que pour Windows XP.</span><span class="sxs-lookup"><span data-stu-id="d6b4c-123">Background downloading allows the user to proceed to other tasks and even restart Windows without cancelling the download, but takes more time overall to complete the download and is only supported for Windows XP.</span></span> <span data-ttu-id="d6b4c-124">Le téléchargement en temps réel prend moins de temps, mais exige que l’utilisateur termine tout téléchargement avant de fermer le lecteur Windows Media.</span><span class="sxs-lookup"><span data-stu-id="d6b4c-124">Real-time downloading takes less time to complete, but requires the user to finish all downloading before closing Windows Media Player.</span></span>

## <a name="requirements"></a><span data-ttu-id="d6b4c-125">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="d6b4c-125">Requirements</span></span>



| <span data-ttu-id="d6b4c-126">Condition requise</span><span class="sxs-lookup"><span data-stu-id="d6b4c-126">Requirement</span></span> | <span data-ttu-id="d6b4c-127">Valeur</span><span class="sxs-lookup"><span data-stu-id="d6b4c-127">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="d6b4c-128">Version</span><span class="sxs-lookup"><span data-stu-id="d6b4c-128">Version</span></span><br/> | <span data-ttu-id="d6b4c-129">Lecteur Windows Media série 9 ou version ultérieure</span><span class="sxs-lookup"><span data-stu-id="d6b4c-129">Windows Media Player 9 Series or later</span></span><br/>                                  |
| <span data-ttu-id="d6b4c-130">DLL</span><span class="sxs-lookup"><span data-stu-id="d6b4c-130">DLL</span></span><br/>     | <dl> <span data-ttu-id="d6b4c-131"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="d6b4c-131"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d6b4c-132">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="d6b4c-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d6b4c-133">**Objet DownloadItem**</span><span class="sxs-lookup"><span data-stu-id="d6b4c-133">**DownloadItem Object**</span></span>](downloaditem-object.md)
</dt> </dl>

 

 





