---
title: Attribut Is_Protected
description: L' \_ attribut is protected indique si le contenu est protégé à l’aide de la gestion des droits numériques (DRM).
ms.assetid: 049d4116-7ba6-49f5-ad54-82a98b79d6bc
keywords:
- Is_Protected attribut lecteur Windows Media
topic_type:
- apiref
api_name:
- Is_Protected
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2ba626e72e139a5373973edea581f0f8462eee32
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106537921"
---
# <a name="is_protected-attribute"></a><span data-ttu-id="cf480-104">\_Attribut protégé</span><span class="sxs-lookup"><span data-stu-id="cf480-104">Is\_Protected Attribute</span></span>

<span data-ttu-id="cf480-105">L’attribut **is \_ protected** indique si le contenu est protégé à l’aide de la gestion des droits numériques (DRM).</span><span class="sxs-lookup"><span data-stu-id="cf480-105">The **Is\_Protected** attribute indicates whether the content is protected using digital rights management (DRM).</span></span>

## <a name="applies-to"></a><span data-ttu-id="cf480-106">S'applique à</span><span class="sxs-lookup"><span data-stu-id="cf480-106">Applies To</span></span>

-   [<span data-ttu-id="cf480-107">Éléments audio</span><span class="sxs-lookup"><span data-stu-id="cf480-107">Audio Items</span></span>](audio-item-attributes.md)
-   [<span data-ttu-id="cf480-108">Fichiers Windows Media couramment utilisés</span><span class="sxs-lookup"><span data-stu-id="cf480-108">Commonly Used Windows Media Files</span></span>](commonly-used-windows-media-file-attributes.md)
-   [<span data-ttu-id="cf480-109">Éléments vidéo</span><span class="sxs-lookup"><span data-stu-id="cf480-109">Video Items</span></span>](video-item-attributes.md)

## <a name="remarks"></a><span data-ttu-id="cf480-110">Notes</span><span class="sxs-lookup"><span data-stu-id="cf480-110">Remarks</span></span>

<span data-ttu-id="cf480-111">Cet attribut est stocké à la fois dans la bibliothèque et dans le fichier multimédia numérique.</span><span class="sxs-lookup"><span data-stu-id="cf480-111">This attribute is stored in both the library and the digital media file.</span></span>

<span data-ttu-id="cf480-112">**DigitallySecure** est un alias pour cet attribut.</span><span class="sxs-lookup"><span data-stu-id="cf480-112">**DigitallySecure** is an alias for this attribute.</span></span>

<span data-ttu-id="cf480-113">La constante du kit de développement logiciel (SDK) du format Windows Media pour cet attribut est g \_ wszWMProtected.</span><span class="sxs-lookup"><span data-stu-id="cf480-113">The Windows Media Format SDK constant for this attribute is g\_wszWMProtected.</span></span>

<span data-ttu-id="cf480-114">Pour déterminer si vous pouvez modifier la valeur de cet attribut, utilisez la méthode [Media. isReadOnlyItem](media-isreadonlyitem.md) .</span><span class="sxs-lookup"><span data-stu-id="cf480-114">To determine whether you can change the value of this attribute, use the [Media.isReadOnlyItem](media-isreadonlyitem.md) method.</span></span>

## <a name="requirements"></a><span data-ttu-id="cf480-115">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="cf480-115">Requirements</span></span>



| <span data-ttu-id="cf480-116">Condition requise</span><span class="sxs-lookup"><span data-stu-id="cf480-116">Requirement</span></span> | <span data-ttu-id="cf480-117">Valeur</span><span class="sxs-lookup"><span data-stu-id="cf480-117">Value</span></span> |
|--------------------|---------------------------------------------------|
| <span data-ttu-id="cf480-118">Version</span><span class="sxs-lookup"><span data-stu-id="cf480-118">Version</span></span><br/> | <span data-ttu-id="cf480-119">Lecteur Windows Media série 9 ou version ultérieure</span><span class="sxs-lookup"><span data-stu-id="cf480-119">Windows Media Player 9 Series or later</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="cf480-120">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="cf480-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cf480-121">**Référence d’attribut**</span><span class="sxs-lookup"><span data-stu-id="cf480-121">**Attribute Reference**</span></span>](attribute-reference.md)
</dt> </dl>

 

 





