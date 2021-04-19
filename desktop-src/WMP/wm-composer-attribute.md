---
title: Attribut WM/composer
description: L’attribut WM/composer est le nom du compositeur de la musique.
ms.assetid: 48459027-ed80-46a2-ad5c-ace602144150
keywords:
- Attribut WM/composer lecteur Windows Media
topic_type:
- apiref
api_name:
- WM/Composer
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a2f206b1a23126612f3f7c875b9a9b4badca8339
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106530488"
---
# <a name="wmcomposer-attribute"></a><span data-ttu-id="090dc-104">Attribut WM/composer</span><span class="sxs-lookup"><span data-stu-id="090dc-104">WM/Composer Attribute</span></span>

<span data-ttu-id="090dc-105">L’attribut **WM/composer** est le nom du compositeur de la musique.</span><span class="sxs-lookup"><span data-stu-id="090dc-105">The **WM/Composer** attribute is the name of the composer of the music.</span></span>

## <a name="applies-to"></a><span data-ttu-id="090dc-106">S'applique à</span><span class="sxs-lookup"><span data-stu-id="090dc-106">Applies To</span></span>

-   [<span data-ttu-id="090dc-107">Éléments audio</span><span class="sxs-lookup"><span data-stu-id="090dc-107">Audio Items</span></span>](audio-item-attributes.md)
-   [<span data-ttu-id="090dc-108">Sélections de CD</span><span class="sxs-lookup"><span data-stu-id="090dc-108">CD Playlists</span></span>](cd-playlist-attributes.md)
-   [<span data-ttu-id="090dc-109">Pistes de CD</span><span class="sxs-lookup"><span data-stu-id="090dc-109">CD Tracks</span></span>](cd-track-attributes.md)
-   [<span data-ttu-id="090dc-110">Attributs de fichiers Windows Media couramment utilisés</span><span class="sxs-lookup"><span data-stu-id="090dc-110">Commonly Used Windows Media File Attributes</span></span>](commonly-used-windows-media-file-attributes.md)

## <a name="remarks"></a><span data-ttu-id="090dc-111">Notes</span><span class="sxs-lookup"><span data-stu-id="090dc-111">Remarks</span></span>

<span data-ttu-id="090dc-112">Cet attribut est stocké à la fois dans la bibliothèque (ou le cache) et dans le fichier multimédia numérique.</span><span class="sxs-lookup"><span data-stu-id="090dc-112">This attribute is stored in both the library (or cache) and the digital media file.</span></span>

<span data-ttu-id="090dc-113">Cet attribut peut avoir plusieurs valeurs.</span><span class="sxs-lookup"><span data-stu-id="090dc-113">This attribute may have multiple values.</span></span> <span data-ttu-id="090dc-114">Pour récupérer toutes les valeurs d’un attribut à valeurs multiples, vous devez utiliser la méthode **Media. getItemInfoByType** , et non la méthode **Media. getItemInfo** .</span><span class="sxs-lookup"><span data-stu-id="090dc-114">To retrieve all of the values for a multi-valued attribute, you must use the **Media.getItemInfoByType** method, not the **Media.getItemInfo** method.</span></span>

<span data-ttu-id="090dc-115">**Compositeur** est un alias pour cet attribut.</span><span class="sxs-lookup"><span data-stu-id="090dc-115">**Composer** is an alias for this attribute.</span></span>

<span data-ttu-id="090dc-116">La constante du kit de développement logiciel (SDK) du format Windows Media pour cet attribut est g \_ wszWMComposer.</span><span class="sxs-lookup"><span data-stu-id="090dc-116">The Windows Media Format SDK constant for this attribute is g\_wszWMComposer.</span></span>

<span data-ttu-id="090dc-117">Pour déterminer si vous pouvez modifier la valeur de cet attribut, utilisez la méthode [Media. isReadOnlyItem](media-isreadonlyitem.md) .</span><span class="sxs-lookup"><span data-stu-id="090dc-117">To determine whether you can change the value of this attribute, use the [Media.isReadOnlyItem](media-isreadonlyitem.md) method.</span></span>

## <a name="requirements"></a><span data-ttu-id="090dc-118">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="090dc-118">Requirements</span></span>



| <span data-ttu-id="090dc-119">Condition requise</span><span class="sxs-lookup"><span data-stu-id="090dc-119">Requirement</span></span> | <span data-ttu-id="090dc-120">Valeur</span><span class="sxs-lookup"><span data-stu-id="090dc-120">Value</span></span> |
|--------------------|---------------------------------------------------|
| <span data-ttu-id="090dc-121">Version</span><span class="sxs-lookup"><span data-stu-id="090dc-121">Version</span></span><br/> | <span data-ttu-id="090dc-122">Lecteur Windows Media série 9 ou version ultérieure</span><span class="sxs-lookup"><span data-stu-id="090dc-122">Windows Media Player 9 Series or later</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="090dc-123">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="090dc-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="090dc-124">**Référence d’attribut**</span><span class="sxs-lookup"><span data-stu-id="090dc-124">**Attribute Reference**</span></span>](attribute-reference.md)
</dt> <dt>

[<span data-ttu-id="090dc-125">**Media. getItemInfoByType**</span><span class="sxs-lookup"><span data-stu-id="090dc-125">**Media.getItemInfoByType**</span></span>](media-getiteminfobytype.md)
</dt> </dl>

 

 





