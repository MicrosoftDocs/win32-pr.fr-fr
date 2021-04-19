---
title: Attribut SyncOnly
description: L’attribut SyncOnly est une représentation sous forme de chaîne d’une valeur booléenne utilisée par le lecteur Windows Media pour déterminer si une sélection est disponible uniquement pour la synchronisation.
ms.assetid: 36149bb9-3a0b-4f6d-8be3-97d2a87faa83
keywords:
- Attribut SyncOnly lecteur Windows Media
topic_type:
- apiref
api_name:
- SyncOnly
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b0245ffac2c4c64717adf669fcc6ff8fd0768382
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106541026"
---
# <a name="synconly-attribute"></a><span data-ttu-id="c7bfc-104">Attribut SyncOnly</span><span class="sxs-lookup"><span data-stu-id="c7bfc-104">SyncOnly Attribute</span></span>

<span data-ttu-id="c7bfc-105">L’attribut **SyncOnly** est une représentation sous forme de chaîne d’une valeur **booléenne** utilisée par le lecteur Windows Media pour déterminer si une sélection est disponible uniquement pour la synchronisation.</span><span class="sxs-lookup"><span data-stu-id="c7bfc-105">The **SyncOnly** attribute is a string representation of a **Boolean** value that Windows Media Player uses to determine whether a playlist is available only for synchronization.</span></span>

## <a name="applies-to"></a><span data-ttu-id="c7bfc-106">S'applique à</span><span class="sxs-lookup"><span data-stu-id="c7bfc-106">Applies To</span></span>

-   [<span data-ttu-id="c7bfc-107">Sélections</span><span class="sxs-lookup"><span data-stu-id="c7bfc-107">Playlists</span></span>](playlist-attributes-ref.md)

## <a name="remarks"></a><span data-ttu-id="c7bfc-108">Notes</span><span class="sxs-lookup"><span data-stu-id="c7bfc-108">Remarks</span></span>

<span data-ttu-id="c7bfc-109">La valeur 1 indique que la sélection est disponible uniquement pour la synchronisation et ne peut pas apparaître dans le nœud **sélection automatique** .</span><span class="sxs-lookup"><span data-stu-id="c7bfc-109">A value of 1 indicates that the playlist is available only for synchronization and cannot appear in the **Auto Playlist** node.</span></span> <span data-ttu-id="c7bfc-110">La valeur zéro indique que la sélection peut apparaître dans le nœud **sélection automatique** .</span><span class="sxs-lookup"><span data-stu-id="c7bfc-110">A value of zero indicates that the playlist can appear in the **Auto Playlist** node.</span></span>

<span data-ttu-id="c7bfc-111">Pour déterminer si vous pouvez modifier la valeur de cet attribut, utilisez la méthode [Media. isReadOnlyItem](media-isreadonlyitem.md) .</span><span class="sxs-lookup"><span data-stu-id="c7bfc-111">To determine whether you can change the value of this attribute, use the [Media.isReadOnlyItem](media-isreadonlyitem.md) method.</span></span>

## <a name="requirements"></a><span data-ttu-id="c7bfc-112">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="c7bfc-112">Requirements</span></span>



| <span data-ttu-id="c7bfc-113">Condition requise</span><span class="sxs-lookup"><span data-stu-id="c7bfc-113">Requirement</span></span> | <span data-ttu-id="c7bfc-114">Valeur</span><span class="sxs-lookup"><span data-stu-id="c7bfc-114">Value</span></span> |
|--------------------|---------------------------------------------|
| <span data-ttu-id="c7bfc-115">Version</span><span class="sxs-lookup"><span data-stu-id="c7bfc-115">Version</span></span><br/> | <span data-ttu-id="c7bfc-116">Lecteur Windows Media 10 ou version ultérieure</span><span class="sxs-lookup"><span data-stu-id="c7bfc-116">Windows Media Player 10 or later</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="c7bfc-117">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="c7bfc-117">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c7bfc-118">**Référence d’attribut**</span><span class="sxs-lookup"><span data-stu-id="c7bfc-118">**Attribute Reference**</span></span>](attribute-reference.md)
</dt> </dl>

 

 





