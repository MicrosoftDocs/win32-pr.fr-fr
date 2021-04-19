---
title: Attribut WM/Writer
description: L’attribut WM/Writer est le nom du writer qui a écrit les mots du contenu.
ms.assetid: e2035cf7-29f4-4642-9388-4cd7cb08149e
keywords:
- Attribut WM/Writer du lecteur Windows Media
topic_type:
- apiref
api_name:
- WM/Writer
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 29aabf353fc742370ac5d01f084544be8143d3ec
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106541346"
---
# <a name="wmwriter-attribute"></a><span data-ttu-id="dad5a-104">Attribut WM/Writer</span><span class="sxs-lookup"><span data-stu-id="dad5a-104">WM/Writer Attribute</span></span>

<span data-ttu-id="dad5a-105">L’attribut **WM/Writer** est le nom du writer qui a écrit les mots du contenu.</span><span class="sxs-lookup"><span data-stu-id="dad5a-105">The **WM/Writer** attribute is the name of the writer who wrote the words of the content.</span></span>

## <a name="applies-to"></a><span data-ttu-id="dad5a-106">S'applique à</span><span class="sxs-lookup"><span data-stu-id="dad5a-106">Applies To</span></span>

-   [<span data-ttu-id="dad5a-107">Éléments audio</span><span class="sxs-lookup"><span data-stu-id="dad5a-107">Audio Items</span></span>](audio-item-attributes.md)
-   [<span data-ttu-id="dad5a-108">Attributs de fichiers Windows Media couramment utilisés</span><span class="sxs-lookup"><span data-stu-id="dad5a-108">Commonly Used Windows Media File Attributes</span></span>](commonly-used-windows-media-file-attributes.md)
-   [<span data-ttu-id="dad5a-109">Éléments vidéo</span><span class="sxs-lookup"><span data-stu-id="dad5a-109">Video Items</span></span>](video-item-attributes.md)

## <a name="remarks"></a><span data-ttu-id="dad5a-110">Notes</span><span class="sxs-lookup"><span data-stu-id="dad5a-110">Remarks</span></span>

<span data-ttu-id="dad5a-111">Cet attribut est stocké à la fois dans la bibliothèque et dans le fichier multimédia numérique.</span><span class="sxs-lookup"><span data-stu-id="dad5a-111">This attribute is stored in both the library and the digital media file.</span></span>

<span data-ttu-id="dad5a-112">Cet attribut peut avoir plusieurs valeurs.</span><span class="sxs-lookup"><span data-stu-id="dad5a-112">This attribute may have multiple values.</span></span> <span data-ttu-id="dad5a-113">Pour récupérer toutes les valeurs d’un attribut à valeurs multiples, vous devez utiliser la méthode **Media. getItemInfoByType** , et non la méthode **Media. getItemInfo** .</span><span class="sxs-lookup"><span data-stu-id="dad5a-113">To retrieve all of the values for a multi-valued attribute, you must use the **Media.getItemInfoByType** method, not the **Media.getItemInfo** method.</span></span>

<span data-ttu-id="dad5a-114">L' **enregistreur** est un alias pour cet attribut.</span><span class="sxs-lookup"><span data-stu-id="dad5a-114">**Writer** is an alias for this attribute.</span></span>

<span data-ttu-id="dad5a-115">La constante du kit de développement logiciel (SDK) du format Windows Media pour cet attribut est g \_ wszWMWriter.</span><span class="sxs-lookup"><span data-stu-id="dad5a-115">The Windows Media Format SDK constant for this attribute is g\_wszWMWriter.</span></span>

<span data-ttu-id="dad5a-116">Pour déterminer si vous pouvez modifier la valeur de cet attribut, utilisez la méthode [Media. isReadOnlyItem](media-isreadonlyitem.md) .</span><span class="sxs-lookup"><span data-stu-id="dad5a-116">To determine whether you can change the value of this attribute, use the [Media.isReadOnlyItem](media-isreadonlyitem.md) method.</span></span>

## <a name="requirements"></a><span data-ttu-id="dad5a-117">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="dad5a-117">Requirements</span></span>



| <span data-ttu-id="dad5a-118">Condition requise</span><span class="sxs-lookup"><span data-stu-id="dad5a-118">Requirement</span></span> | <span data-ttu-id="dad5a-119">Valeur</span><span class="sxs-lookup"><span data-stu-id="dad5a-119">Value</span></span> |
|--------------------|---------------------------------------------------|
| <span data-ttu-id="dad5a-120">Version</span><span class="sxs-lookup"><span data-stu-id="dad5a-120">Version</span></span><br/> | <span data-ttu-id="dad5a-121">Lecteur Windows Media série 9 ou version ultérieure</span><span class="sxs-lookup"><span data-stu-id="dad5a-121">Windows Media Player 9 Series or later</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="dad5a-122">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="dad5a-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="dad5a-123">**Référence d’attribut**</span><span class="sxs-lookup"><span data-stu-id="dad5a-123">**Attribute Reference**</span></span>](attribute-reference.md)
</dt> <dt>

[<span data-ttu-id="dad5a-124">**Media. getItemInfoByType**</span><span class="sxs-lookup"><span data-stu-id="dad5a-124">**Media.getItemInfoByType**</span></span>](media-getiteminfobytype.md)
</dt> </dl>

 

 





