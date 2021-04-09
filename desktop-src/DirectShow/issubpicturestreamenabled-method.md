---
description: La méthode IsSubpictureStreamEnabled récupère une valeur indiquant si le flux de sous-image spécifié est activé dans le titre actuel.
ms.assetid: c6436f77-ca94-464f-9336-f485f5d5d199
title: Méthode IsSubpictureStreamEnabled
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 818b4ff18dac87ea3346a1a503764b2e5e9cd02a
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/06/2021
ms.locfileid: "103846641"
---
# <a name="issubpicturestreamenabled-method"></a><span data-ttu-id="3f6ac-103">Méthode IsSubpictureStreamEnabled</span><span class="sxs-lookup"><span data-stu-id="3f6ac-103">IsSubpictureStreamEnabled Method</span></span>

> [!Note]  
> <span data-ttu-id="3f6ac-104">Ce composant peut être utilisé dans les systèmes d’exploitation Microsoft Windows 2000, Windows XP et Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="3f6ac-104">This component is available for use in the Microsoft Windows 2000, Windows XP, and Windows Server 2003 operating systems.</span></span> <span data-ttu-id="3f6ac-105">Il sera peut-être modifié ou indisponible dans les versions ultérieures.</span><span class="sxs-lookup"><span data-stu-id="3f6ac-105">It may be altered or unavailable in subsequent versions.</span></span>

 

<span data-ttu-id="3f6ac-106">La `IsSubpictureStreamEnabled` méthode récupère une valeur indiquant si le flux de sous-image spécifié est activé dans le titre actuel.</span><span class="sxs-lookup"><span data-stu-id="3f6ac-106">The `IsSubpictureStreamEnabled` method retrieves a value indicating whether the specified subpicture stream is enabled in the current title.</span></span>

``` syntax
[ bEnabled = ] MSWebDVD.IsSubpictureStreamEnabled(iStream)
```

## <a name="parameters"></a><span data-ttu-id="3f6ac-107">Paramètres</span><span class="sxs-lookup"><span data-stu-id="3f6ac-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3f6ac-108"><span id="iStream"></span><span id="istream"></span><span id="ISTREAM"></span>*iStream*</span><span class="sxs-lookup"><span data-stu-id="3f6ac-108"><span id="iStream"></span><span id="istream"></span><span id="ISTREAM"></span>*iStream*</span></span>
</dt> <dd>

<span data-ttu-id="3f6ac-109">Spécifie le flux de sous-image sous la forme d’un entier.</span><span class="sxs-lookup"><span data-stu-id="3f6ac-109">Specifies the subpicture stream as an Integer.</span></span>



| <span data-ttu-id="3f6ac-110">Valeur</span><span class="sxs-lookup"><span data-stu-id="3f6ac-110">Value</span></span>   | <span data-ttu-id="3f6ac-111">Description</span><span class="sxs-lookup"><span data-stu-id="3f6ac-111">Description</span></span>              |
|---------|--------------------------|
| <span data-ttu-id="3f6ac-112">de 0 à 31</span><span class="sxs-lookup"><span data-stu-id="3f6ac-112">0 to 31</span></span> | <span data-ttu-id="3f6ac-113">flux de sous-image</span><span class="sxs-lookup"><span data-stu-id="3f6ac-113">subpicture stream</span></span>        |
| <span data-ttu-id="3f6ac-114">63</span><span class="sxs-lookup"><span data-stu-id="3f6ac-114">63</span></span>      | <span data-ttu-id="3f6ac-115">flux muet faible-débit</span><span class="sxs-lookup"><span data-stu-id="3f6ac-115">muted low-bitrate stream</span></span> |



 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3f6ac-116">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="3f6ac-116">Return Value</span></span>

<span data-ttu-id="3f6ac-117">Retourne une valeur booléenne indiquant si le flux audio spécifié est disponible dans le titre actuel.</span><span class="sxs-lookup"><span data-stu-id="3f6ac-117">Returns a Boolean value indicating whether the specified audio stream is available in the current title.</span></span> <span data-ttu-id="3f6ac-118">True signifie qu’il est disponible.</span><span class="sxs-lookup"><span data-stu-id="3f6ac-118">True means it is available.</span></span>

## <a name="remarks"></a><span data-ttu-id="3f6ac-119">Notes</span><span class="sxs-lookup"><span data-stu-id="3f6ac-119">Remarks</span></span>

<span data-ttu-id="3f6ac-120">Bien qu’un disque puisse contenir jusqu’à 32 flux de sous-image, chaque flux n’est pas nécessairement disponible pour chaque titre.</span><span class="sxs-lookup"><span data-stu-id="3f6ac-120">Although a disc can contain up to 32 subpicture streams, each stream is not necessarily available for each title.</span></span> <span data-ttu-id="3f6ac-121">Vérifiez toujours qu’un flux est disponible pour un titre avant de définir la propriété [**CurrentSubpictureStream**](currentsubpicturestream-property.md) .</span><span class="sxs-lookup"><span data-stu-id="3f6ac-121">Always verify that a stream is available for a title before setting the [**CurrentSubpictureStream**](currentsubpicturestream-property.md) property.</span></span>

 

 



