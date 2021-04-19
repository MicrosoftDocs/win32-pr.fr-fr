---
title: Méthode DownloadManager. getDownloadCollection
description: Remarque Cette section décrit les fonctionnalités conçues pour être utilisées par les magasins en ligne. L’utilisation de cette fonctionnalité en dehors du contexte d’un magasin en ligne n’est pas prise en charge. La méthode getDownloadCollection récupère la collection de téléchargements spécifiée.
ms.assetid: 743d6bcf-2d5b-4a30-a4ef-4538cf7c901e
keywords:
- méthode getDownloadCollection lecteur Windows Media
- méthode getDownloadCollection lecteur Windows Media, classe DownloadManager
- Classe DownloadManager lecteur Windows Media, méthode getDownloadCollection
topic_type:
- apiref
api_name:
- DownloadManager.getDownloadCollection
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2e879d82c3f49db08d75b8aec37271e8d966019e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106535903"
---
# <a name="downloadmanagergetdownloadcollection-method"></a><span data-ttu-id="7b783-108">Méthode DownloadManager. getDownloadCollection</span><span class="sxs-lookup"><span data-stu-id="7b783-108">DownloadManager.getDownloadCollection method</span></span>

> [!Note]  
> <span data-ttu-id="7b783-109">Cette section décrit les fonctionnalités conçues pour être utilisées par les magasins en ligne.</span><span class="sxs-lookup"><span data-stu-id="7b783-109">This section describes functionality designed for use by online stores.</span></span> <span data-ttu-id="7b783-110">L’utilisation de cette fonctionnalité en dehors du contexte d’un magasin en ligne n’est pas prise en charge.</span><span class="sxs-lookup"><span data-stu-id="7b783-110">Use of this functionality outside the context of an online store is not supported.</span></span>

 

<span data-ttu-id="7b783-111">La méthode **getDownloadCollection** récupère la collection de téléchargements spécifiée.</span><span class="sxs-lookup"><span data-stu-id="7b783-111">The **getDownloadCollection** method retrieves the specified download collection.</span></span>

## <a name="syntax"></a><span data-ttu-id="7b783-112">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="7b783-112">Syntax</span></span>


```JScript
retVal = DownloadManager.getDownloadCollection(
  collectionId
)
```



## <a name="parameters"></a><span data-ttu-id="7b783-113">Paramètres</span><span class="sxs-lookup"><span data-stu-id="7b783-113">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7b783-114">L’un des  \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="7b783-114">*collectionId* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7b783-115">**Nombre** (**long**) spécifiant l’ID de la collection de téléchargements à récupérer.</span><span class="sxs-lookup"><span data-stu-id="7b783-115">**Number** (**long**) specifying the ID of the download collection to retrieve.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7b783-116">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="7b783-116">Return value</span></span>

<span data-ttu-id="7b783-117">Cette méthode retourne un objet **DownloadCollection** .</span><span class="sxs-lookup"><span data-stu-id="7b783-117">This method returns a **DownloadCollection** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="7b783-118">Notes</span><span class="sxs-lookup"><span data-stu-id="7b783-118">Remarks</span></span>

<span data-ttu-id="7b783-119">Vous devez d’abord appeler *downloadmanager*. **createDownloadCollection** pour créer une nouvelle collection et récupérer sa valeur d’ID.</span><span class="sxs-lookup"><span data-stu-id="7b783-119">You must first call *DownloadManager*.**createDownloadCollection** to create a new collection and retrieve its ID value.</span></span>

<span data-ttu-id="7b783-120">Une collection de téléchargements existante peut contenir des éléments qui ont été marqués comme étant annulés.</span><span class="sxs-lookup"><span data-stu-id="7b783-120">An existing download collection may contain items that have been marked as cancelled.</span></span>

<span data-ttu-id="7b783-121">Les éléments de téléchargement en temps réel qui ne sont pas terminés dans une session antérieure ne sont pas récupérés dans le cadre de la collection.</span><span class="sxs-lookup"><span data-stu-id="7b783-121">Real-time download items not completed in a prior session are not retrieved as part of the collection.</span></span> <span data-ttu-id="7b783-122">Les téléchargements en arrière-plan qui ont été effectués avant la session active restent dans la collection de téléchargements jusqu’à ce qu’ils soient supprimés.</span><span class="sxs-lookup"><span data-stu-id="7b783-122">Background downloads that were completed prior to the current session remain in the download collection until removed.</span></span>

## <a name="requirements"></a><span data-ttu-id="7b783-123">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="7b783-123">Requirements</span></span>



| <span data-ttu-id="7b783-124">Condition requise</span><span class="sxs-lookup"><span data-stu-id="7b783-124">Requirement</span></span> | <span data-ttu-id="7b783-125">Valeur</span><span class="sxs-lookup"><span data-stu-id="7b783-125">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="7b783-126">Version</span><span class="sxs-lookup"><span data-stu-id="7b783-126">Version</span></span><br/> | <span data-ttu-id="7b783-127">Lecteur Windows Media série 9 ou version ultérieure</span><span class="sxs-lookup"><span data-stu-id="7b783-127">Windows Media Player 9 Series or later</span></span><br/>                                  |
| <span data-ttu-id="7b783-128">DLL</span><span class="sxs-lookup"><span data-stu-id="7b783-128">DLL</span></span><br/>     | <dl> <span data-ttu-id="7b783-129"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="7b783-129"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7b783-130">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="7b783-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7b783-131">**Objet DownloadManager**</span><span class="sxs-lookup"><span data-stu-id="7b783-131">**DownloadManager Object**</span></span>](downloadmanager-object.md)
</dt> <dt>

[<span data-ttu-id="7b783-132">**DownloadManager. createDownloadCollection**</span><span class="sxs-lookup"><span data-stu-id="7b783-132">**DownloadManager. createDownloadCollection**</span></span>](downloadmanager-createdownloadcollection.md)
</dt> <dt>

[<span data-ttu-id="7b783-133">**Objet DownloadCollection**</span><span class="sxs-lookup"><span data-stu-id="7b783-133">**DownloadCollection Object**</span></span>](downloadcollection-object.md)
</dt> </dl>

 

 





