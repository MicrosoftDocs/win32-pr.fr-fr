---
title: Attribut WM/conducteur
description: L’attribut WM/conducteur est le nom du conducteur de la musique.
ms.assetid: 31c7d310-da6a-4c30-86b0-15defaee1743
keywords:
- Attribut WM/conducteur lecteur Windows Media
topic_type:
- apiref
api_name:
- WM/Conductor
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3d1ae08dfee807d130f04dd258c6af81a8d68057
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106543603"
---
# <a name="wmconductor-attribute"></a><span data-ttu-id="f3d47-104">Attribut WM/conducteur</span><span class="sxs-lookup"><span data-stu-id="f3d47-104">WM/Conductor Attribute</span></span>

<span data-ttu-id="f3d47-105">L’attribut **WM/conducteur** est le nom du conducteur de la musique.</span><span class="sxs-lookup"><span data-stu-id="f3d47-105">The **WM/Conductor** attribute is the name of the conductor of the music.</span></span>

## <a name="applies-to"></a><span data-ttu-id="f3d47-106">S'applique à</span><span class="sxs-lookup"><span data-stu-id="f3d47-106">Applies To</span></span>

-   [<span data-ttu-id="f3d47-107">Éléments audio</span><span class="sxs-lookup"><span data-stu-id="f3d47-107">Audio Items</span></span>](audio-item-attributes.md)
-   [<span data-ttu-id="f3d47-108">Pistes de CD</span><span class="sxs-lookup"><span data-stu-id="f3d47-108">CD Tracks</span></span>](cd-track-attributes.md)
-   [<span data-ttu-id="f3d47-109">Attributs de fichiers Windows Media couramment utilisés</span><span class="sxs-lookup"><span data-stu-id="f3d47-109">Commonly Used Windows Media File Attributes</span></span>](commonly-used-windows-media-file-attributes.md)

## <a name="remarks"></a><span data-ttu-id="f3d47-110">Notes</span><span class="sxs-lookup"><span data-stu-id="f3d47-110">Remarks</span></span>

<span data-ttu-id="f3d47-111">Cet attribut est stocké à la fois dans la bibliothèque (ou le cache) et dans le fichier multimédia numérique.</span><span class="sxs-lookup"><span data-stu-id="f3d47-111">This attribute is stored in both the library (or cache) and the digital media file.</span></span>

<span data-ttu-id="f3d47-112">Cet attribut peut avoir plusieurs valeurs.</span><span class="sxs-lookup"><span data-stu-id="f3d47-112">This attribute may have multiple values.</span></span> <span data-ttu-id="f3d47-113">Pour récupérer toutes les valeurs d’un attribut à valeurs multiples, vous devez utiliser la méthode **Media. getItemInfoByType** , et non la méthode **Media. getItemInfo** .</span><span class="sxs-lookup"><span data-stu-id="f3d47-113">To retrieve all of the values for a multi-valued attribute, you must use the **Media.getItemInfoByType** method, not the **Media.getItemInfo** method.</span></span>

<span data-ttu-id="f3d47-114">Le **conducteur** est un alias de cet attribut.</span><span class="sxs-lookup"><span data-stu-id="f3d47-114">**Conductor** is an alias for this attribute.</span></span>

<span data-ttu-id="f3d47-115">La constante du kit de développement logiciel (SDK) du format Windows Media pour cet attribut est g \_ wszWMConductor.</span><span class="sxs-lookup"><span data-stu-id="f3d47-115">The Windows Media Format SDK constant for this attribute is g\_wszWMConductor.</span></span>

<span data-ttu-id="f3d47-116">Pour déterminer si vous pouvez modifier la valeur de cet attribut, utilisez la méthode [Media. isReadOnlyItem](media-isreadonlyitem.md) .</span><span class="sxs-lookup"><span data-stu-id="f3d47-116">To determine whether you can change the value of this attribute, use the [Media.isReadOnlyItem](media-isreadonlyitem.md) method.</span></span>

## <a name="requirements"></a><span data-ttu-id="f3d47-117">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="f3d47-117">Requirements</span></span>



| <span data-ttu-id="f3d47-118">Condition requise</span><span class="sxs-lookup"><span data-stu-id="f3d47-118">Requirement</span></span> | <span data-ttu-id="f3d47-119">Valeur</span><span class="sxs-lookup"><span data-stu-id="f3d47-119">Value</span></span> |
|--------------------|---------------------------------------------------|
| <span data-ttu-id="f3d47-120">Version</span><span class="sxs-lookup"><span data-stu-id="f3d47-120">Version</span></span><br/> | <span data-ttu-id="f3d47-121">Lecteur Windows Media série 9 ou version ultérieure</span><span class="sxs-lookup"><span data-stu-id="f3d47-121">Windows Media Player 9 Series or later</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="f3d47-122">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="f3d47-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f3d47-123">**Référence d’attribut**</span><span class="sxs-lookup"><span data-stu-id="f3d47-123">**Attribute Reference**</span></span>](attribute-reference.md)
</dt> <dt>

[<span data-ttu-id="f3d47-124">**Media. getItemInfoByType**</span><span class="sxs-lookup"><span data-stu-id="f3d47-124">**Media.getItemInfoByType**</span></span>](media-getiteminfobytype.md)
</dt> </dl>

 

 





