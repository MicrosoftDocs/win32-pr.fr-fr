---
description: La méthode SaveBookmark enregistre la position actuelle du disque et l’état de l’objet MSWebDVD afin que l’utilisateur puisse retourner au même endroit ultérieurement.
ms.assetid: 975687c5-f93e-4473-b23b-63e0ae6bbb5d
title: Méthode SaveBookmark (segment. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f2013a56d3f6885f7a4235497ad42bb03f0ebf7a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106525213"
---
# <a name="savebookmark-method"></a><span data-ttu-id="67af2-103">Méthode SaveBookmark</span><span class="sxs-lookup"><span data-stu-id="67af2-103">SaveBookmark Method</span></span>

> [!Note]  
> <span data-ttu-id="67af2-104">Ce composant peut être utilisé dans les systèmes d’exploitation Microsoft Windows 2000, Windows XP et Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="67af2-104">This component is available for use in the Microsoft Windows 2000, Windows XP, and Windows Server 2003 operating systems.</span></span> <span data-ttu-id="67af2-105">Il sera peut-être modifié ou indisponible dans les versions ultérieures.</span><span class="sxs-lookup"><span data-stu-id="67af2-105">It may be altered or unavailable in subsequent versions.</span></span>

 

<span data-ttu-id="67af2-106">La `SaveBookmark` méthode enregistre la position actuelle du disque et l’état de l’objet **mswebdvd** pour permettre à l’utilisateur de revenir ultérieurement au même endroit.</span><span class="sxs-lookup"><span data-stu-id="67af2-106">The `SaveBookmark` method saves the current disc position and state of the **MSWebDVD** object so the user can return to the same place later.</span></span>

``` syntax
MSWebDVD.SaveBookmark()
```

## <a name="return-value"></a><span data-ttu-id="67af2-107">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="67af2-107">Return Value</span></span>

<span data-ttu-id="67af2-108">Pas de valeur de retour.</span><span class="sxs-lookup"><span data-stu-id="67af2-108">No return value.</span></span>

## <a name="remarks"></a><span data-ttu-id="67af2-109">Notes</span><span class="sxs-lookup"><span data-stu-id="67af2-109">Remarks</span></span>

<span data-ttu-id="67af2-110">Un signet est un instantané de l’état actuel du navigateur DVD.</span><span class="sxs-lookup"><span data-stu-id="67af2-110">A bookmark is a snapshot of the DVD Navigator's current state.</span></span> <span data-ttu-id="67af2-111">Cela comprend des informations telles que l’emplacement de lecture sur le disque et les flux audio et sous-images qui sont sélectionnés.</span><span class="sxs-lookup"><span data-stu-id="67af2-111">This includes information such as where it is playing on the disc, and which audio and subpictures streams are selected.</span></span> <span data-ttu-id="67af2-112">En enregistrant un signet, l’utilisateur peut fermer l’application, arrêter l’ordinateur, puis revenir ultérieurement pour continuer à afficher le disque là où il s’était arrêté, avec tous les paramètres comme auparavant.</span><span class="sxs-lookup"><span data-stu-id="67af2-112">By saving a bookmark, the user can close the application, shut down the computer, and come back later to continue viewing the disc right where he or she left off, with all settings just as they were before.</span></span> <span data-ttu-id="67af2-113">Un seul signet peut être enregistré à un moment donné.</span><span class="sxs-lookup"><span data-stu-id="67af2-113">Only one bookmark can be saved at any given time.</span></span> <span data-ttu-id="67af2-114">Lorsque vous appelez `SaveBookmark` , l’ancien signet est remplacé.</span><span class="sxs-lookup"><span data-stu-id="67af2-114">When you call `SaveBookmark`, the old bookmark is overwritten.</span></span>

## <a name="requirements"></a><span data-ttu-id="67af2-115">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="67af2-115">Requirements</span></span>



| <span data-ttu-id="67af2-116">Condition requise</span><span class="sxs-lookup"><span data-stu-id="67af2-116">Requirement</span></span> | <span data-ttu-id="67af2-117">Valeur</span><span class="sxs-lookup"><span data-stu-id="67af2-117">Value</span></span> |
|-------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="67af2-118">En-tête</span><span class="sxs-lookup"><span data-stu-id="67af2-118">Header</span></span><br/> | <dl> <span data-ttu-id="67af2-119"><dt>Segment. h</dt></span><span class="sxs-lookup"><span data-stu-id="67af2-119"><dt>Segment.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="67af2-120">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="67af2-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="67af2-121">**RestoreBookmark**</span><span class="sxs-lookup"><span data-stu-id="67af2-121">**RestoreBookmark**</span></span>](restorebookmark-method.md)
</dt> </dl>

 

 




