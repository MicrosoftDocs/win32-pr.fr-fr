---
title: PLAYLIST. copier
description: La méthode de copie commence une opération de copie à partir du CD.
ms.assetid: 7d919ae5-456b-4cb9-ad52-9396f5c867d6
keywords:
- SÉLECTION. copier le lecteur Windows Media
topic_type:
- apiref
api_name:
- PLAYLIST.copy
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: f1c24de6af571eec948a92f666a76df6b65187c6
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106539272"
---
# <a name="playlistcopy"></a><span data-ttu-id="51a02-104">PLAYLIST. copier</span><span class="sxs-lookup"><span data-stu-id="51a02-104">PLAYLIST.copy</span></span>

<span data-ttu-id="51a02-105">La méthode de **copie** commence une opération de copie à partir du CD.</span><span class="sxs-lookup"><span data-stu-id="51a02-105">The **copy** method begins a copy operation from the CD.</span></span>

``` syntax
        elementID.copy()
```

## <a name="parameters"></a><span data-ttu-id="51a02-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="51a02-106">Parameters</span></span>

<span data-ttu-id="51a02-107">Cette méthode n’a aucun paramètre.</span><span class="sxs-lookup"><span data-stu-id="51a02-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="51a02-108">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="51a02-108">Return Value</span></span>

<span data-ttu-id="51a02-109">Cette méthode ne retourne pas de valeur.</span><span class="sxs-lookup"><span data-stu-id="51a02-109">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="51a02-110">Notes</span><span class="sxs-lookup"><span data-stu-id="51a02-110">Remarks</span></span>

<span data-ttu-id="51a02-111">Cette méthode copie uniquement les éléments cochés dans la sélection et fonctionne de la même façon que dans le volet **copier à partir du CD-ROM** en mode complet du lecteur Windows Media.</span><span class="sxs-lookup"><span data-stu-id="51a02-111">This method copies only the checked items in the playlist, and works the same way as in the **Copy from CD** pane in the full mode of Windows Media Player.</span></span> <span data-ttu-id="51a02-112">Pour que cette méthode fonctionne, un CD doit se trouver dans le lecteur de CD.</span><span class="sxs-lookup"><span data-stu-id="51a02-112">For this method to work, a CD must be in the CD drive.</span></span> <span data-ttu-id="51a02-113">Affectez la valeur true à l’attribut **checkboxesVisible** pour permettre aux utilisateurs de sélectionner des éléments individuels sur un CD avant la copie.</span><span class="sxs-lookup"><span data-stu-id="51a02-113">Set the **checkboxesVisible** attribute to true to allow users to select individual items on a CD before copying.</span></span>

## <a name="requirements"></a><span data-ttu-id="51a02-114">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="51a02-114">Requirements</span></span>



| <span data-ttu-id="51a02-115">Condition requise</span><span class="sxs-lookup"><span data-stu-id="51a02-115">Requirement</span></span> | <span data-ttu-id="51a02-116">Valeur</span><span class="sxs-lookup"><span data-stu-id="51a02-116">Value</span></span> |
|--------------------|------------------------------------------------------|
| <span data-ttu-id="51a02-117">Version</span><span class="sxs-lookup"><span data-stu-id="51a02-117">Version</span></span><br/> | <span data-ttu-id="51a02-118">Lecteur Windows Media version 7,0 ou ultérieure</span><span class="sxs-lookup"><span data-stu-id="51a02-118">Windows Media Player version 7.0 or later</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="51a02-119">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="51a02-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="51a02-120">**Élément PLAYLIST**</span><span class="sxs-lookup"><span data-stu-id="51a02-120">**PLAYLIST Element**</span></span>](playlist-element.md)
</dt> <dt>

[<span data-ttu-id="51a02-121">**PLAYLIST. abortCopy**</span><span class="sxs-lookup"><span data-stu-id="51a02-121">**PLAYLIST.abortCopy**</span></span>](playlist-abortcopy.md)
</dt> <dt>

[<span data-ttu-id="51a02-122">**PLAYLIST. copie**</span><span class="sxs-lookup"><span data-stu-id="51a02-122">**PLAYLIST.copying**</span></span>](playlist-copying.md)
</dt> </dl>

 

 





