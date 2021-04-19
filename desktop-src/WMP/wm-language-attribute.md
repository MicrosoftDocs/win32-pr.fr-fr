---
title: Attribut WM/Language
description: L’attribut WM/Language est le langage de l’élément.
ms.assetid: aebfb518-61ca-4b75-875a-ce2127a74b67
keywords:
- Attribut WM/Language lecteur Windows Media
topic_type:
- apiref
api_name:
- WM/Language
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 172cc8498bf5360e29822a484bcc2ddacd70b8b7
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106539627"
---
# <a name="wmlanguage-attribute"></a><span data-ttu-id="010c8-104">Attribut WM/Language</span><span class="sxs-lookup"><span data-stu-id="010c8-104">WM/Language Attribute</span></span>

<span data-ttu-id="010c8-105">L’attribut **WM/Language** est le langage de l’élément.</span><span class="sxs-lookup"><span data-stu-id="010c8-105">The **WM/Language** attribute is the language of the item.</span></span>

## <a name="applies-to"></a><span data-ttu-id="010c8-106">S'applique à</span><span class="sxs-lookup"><span data-stu-id="010c8-106">Applies To</span></span>

-   [<span data-ttu-id="010c8-107">Éléments audio</span><span class="sxs-lookup"><span data-stu-id="010c8-107">Audio Items</span></span>](audio-item-attributes.md)
-   [<span data-ttu-id="010c8-108">Attributs de fichiers Windows Media couramment utilisés</span><span class="sxs-lookup"><span data-stu-id="010c8-108">Commonly Used Windows Media File Attributes</span></span>](commonly-used-windows-media-file-attributes.md)
-   [<span data-ttu-id="010c8-109">Éléments radio</span><span class="sxs-lookup"><span data-stu-id="010c8-109">Radio Items</span></span>](radio-item-attributes.md)
-   [<span data-ttu-id="010c8-110">Éléments vidéo</span><span class="sxs-lookup"><span data-stu-id="010c8-110">Video Items</span></span>](video-item-attributes.md)

## <a name="remarks"></a><span data-ttu-id="010c8-111">Notes</span><span class="sxs-lookup"><span data-stu-id="010c8-111">Remarks</span></span>

<span data-ttu-id="010c8-112">Cet attribut est stocké à la fois dans la bibliothèque et dans le fichier multimédia numérique.</span><span class="sxs-lookup"><span data-stu-id="010c8-112">This attribute is stored in both the library and the digital media file.</span></span>

<span data-ttu-id="010c8-113">Cet attribut peut avoir plusieurs valeurs.</span><span class="sxs-lookup"><span data-stu-id="010c8-113">This attribute may have multiple values.</span></span> <span data-ttu-id="010c8-114">Pour récupérer toutes les valeurs d’un attribut à valeurs multiples, vous devez utiliser la méthode **Media. getItemInfoByType** , et non la méthode **Media. getItemInfo** .</span><span class="sxs-lookup"><span data-stu-id="010c8-114">To retrieve all of the values for a multi-valued attribute, you must use the **Media.getItemInfoByType** method, not the **Media.getItemInfo** method.</span></span>

<span data-ttu-id="010c8-115">**Language** est un alias de cet attribut.</span><span class="sxs-lookup"><span data-stu-id="010c8-115">**Language** is an alias for this attribute.</span></span>

<span data-ttu-id="010c8-116">La constante du kit de développement logiciel (SDK) du format Windows Media pour cet attribut est g \_ wszWMLanguage.</span><span class="sxs-lookup"><span data-stu-id="010c8-116">The Windows Media Format SDK constant for this attribute is g\_wszWMLanguage.</span></span>

<span data-ttu-id="010c8-117">Pour déterminer si vous pouvez modifier la valeur de cet attribut, utilisez la méthode [Media. isReadOnlyItem](media-isreadonlyitem.md) .</span><span class="sxs-lookup"><span data-stu-id="010c8-117">To determine whether you can change the value of this attribute, use the [Media.isReadOnlyItem](media-isreadonlyitem.md) method.</span></span>

## <a name="requirements"></a><span data-ttu-id="010c8-118">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="010c8-118">Requirements</span></span>



| <span data-ttu-id="010c8-119">Condition requise</span><span class="sxs-lookup"><span data-stu-id="010c8-119">Requirement</span></span> | <span data-ttu-id="010c8-120">Valeur</span><span class="sxs-lookup"><span data-stu-id="010c8-120">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="010c8-121">Version</span><span class="sxs-lookup"><span data-stu-id="010c8-121">Version</span></span><br/> | <span data-ttu-id="010c8-122">Lecteur Windows Media série 9 ou version ultérieure (l’élément radio est pris en charge uniquement dans le lecteur Windows Media série 9)</span><span class="sxs-lookup"><span data-stu-id="010c8-122">Windows Media Player 9 Series or later (The radio item is supported only in Windows Media Player 9 Series)</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="010c8-123">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="010c8-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="010c8-124">**Référence d’attribut**</span><span class="sxs-lookup"><span data-stu-id="010c8-124">**Attribute Reference**</span></span>](attribute-reference.md)
</dt> <dt>

[<span data-ttu-id="010c8-125">**Media. getItemInfoByType**</span><span class="sxs-lookup"><span data-stu-id="010c8-125">**Media.getItemInfoByType**</span></span>](media-getiteminfobytype.md)
</dt> </dl>

 

 





