---
description: La propriété CurrentSubpictureStream définit ou récupère le flux de sous-image en cours.
ms.assetid: 66473c87-ddfe-4555-89ad-90e210a75694
title: Propriété CurrentSubpictureStream
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8c954ad7cfb7aba6dd9bc800ac983d86b6325843
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/06/2021
ms.locfileid: "104522567"
---
# <a name="currentsubpicturestream-property"></a><span data-ttu-id="dcd12-103">Propriété CurrentSubpictureStream</span><span class="sxs-lookup"><span data-stu-id="dcd12-103">CurrentSubpictureStream Property</span></span>

> [!Note]  
> <span data-ttu-id="dcd12-104">Ce composant peut être utilisé dans les systèmes d’exploitation Microsoft Windows 2000, Windows XP et Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="dcd12-104">This component is available for use in the Microsoft Windows 2000, Windows XP, and Windows Server 2003 operating systems.</span></span> <span data-ttu-id="dcd12-105">Il sera peut-être modifié ou indisponible dans les versions ultérieures.</span><span class="sxs-lookup"><span data-stu-id="dcd12-105">It may be altered or unavailable in subsequent versions.</span></span>

 

<span data-ttu-id="dcd12-106">La `CurrentSubpictureStream` propriété définit ou récupère le flux de sous-image en cours.</span><span class="sxs-lookup"><span data-stu-id="dcd12-106">The `CurrentSubpictureStream` property sets or retrieves the current subpicture stream.</span></span>

``` syntax
[ iSPStream = ] MSWebDVD.CurrentSubpictureStream
```

## <a name="return-value"></a><span data-ttu-id="dcd12-107">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="dcd12-107">Return Value</span></span>

<span data-ttu-id="dcd12-108">Retourne une valeur entière représentant le flux.</span><span class="sxs-lookup"><span data-stu-id="dcd12-108">Returns an integer value representing the stream.</span></span>

## <a name="remarks"></a><span data-ttu-id="dcd12-109">Notes</span><span class="sxs-lookup"><span data-stu-id="dcd12-109">Remarks</span></span>

<span data-ttu-id="dcd12-110">Les valeurs possibles de cette propriété sont les suivantes :</span><span class="sxs-lookup"><span data-stu-id="dcd12-110">The possible values of this property are:</span></span>



| <span data-ttu-id="dcd12-111">Valeur</span><span class="sxs-lookup"><span data-stu-id="dcd12-111">Value</span></span>   | <span data-ttu-id="dcd12-112">Description</span><span class="sxs-lookup"><span data-stu-id="dcd12-112">Description</span></span>              |
|---------|--------------------------|
| <span data-ttu-id="dcd12-113">de 0 à 31</span><span class="sxs-lookup"><span data-stu-id="dcd12-113">0 to 31</span></span> | <span data-ttu-id="dcd12-114">Flux de sous-image</span><span class="sxs-lookup"><span data-stu-id="dcd12-114">The subpicture stream</span></span>    |
| <span data-ttu-id="dcd12-115">63</span><span class="sxs-lookup"><span data-stu-id="dcd12-115">63</span></span>      | <span data-ttu-id="dcd12-116">Flux muet faible-débit</span><span class="sxs-lookup"><span data-stu-id="dcd12-116">Muted low-bitrate stream</span></span> |



 

<span data-ttu-id="dcd12-117">Cette propriété est en lecture/écriture sans valeur par défaut.</span><span class="sxs-lookup"><span data-stu-id="dcd12-117">This property is read/write with no default value.</span></span> <span data-ttu-id="dcd12-118">Avant de définir un nouveau flux de sous-image, appelez [**IsSubpictureStreamEnabled**](issubpicturestreamenabled-method.md) pour vérifier que le flux est disponible.</span><span class="sxs-lookup"><span data-stu-id="dcd12-118">Before setting a new subpicture stream, call [**IsSubpictureStreamEnabled**](issubpicturestreamenabled-method.md) to verify that the stream is available.</span></span>

<span data-ttu-id="dcd12-119">La définition de cette propriété entraîne le basculement de la propriété [**SubpictureOn**](subpictureon-property.md) sur **true**.</span><span class="sxs-lookup"><span data-stu-id="dcd12-119">Setting this property causes the [**SubpictureOn**](subpictureon-property.md) property to toggle to **True**.</span></span>

## <a name="see-also"></a><span data-ttu-id="dcd12-120">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="dcd12-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="dcd12-121">**SubpictureOn**</span><span class="sxs-lookup"><span data-stu-id="dcd12-121">**SubpictureOn**</span></span>](subpictureon-property.md)
</dt> <dt>

[<span data-ttu-id="dcd12-122">**SubpictureStreamsAvailable**</span><span class="sxs-lookup"><span data-stu-id="dcd12-122">**SubpictureStreamsAvailable**</span></span>](subpicturestreamsavailable-property.md)
</dt> </dl>

 

 



