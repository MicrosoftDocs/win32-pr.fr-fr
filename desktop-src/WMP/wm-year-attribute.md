---
title: Attribut WM/Year
description: L’attribut WM/Year est l’année de publication du contenu.
ms.assetid: b64e37f1-6f12-43a6-8a66-7d61b470853c
keywords:
- Attribut WM/Year lecteur Windows Media
topic_type:
- apiref
api_name:
- WM/Year
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 10bf10d4e905e10c74cfaf9986445ce9a68dc9b3
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106533126"
---
# <a name="wmyear-attribute"></a><span data-ttu-id="9e182-104">Attribut WM/Year</span><span class="sxs-lookup"><span data-stu-id="9e182-104">WM/Year Attribute</span></span>

<span data-ttu-id="9e182-105">L’attribut **WM/Year** est l’année de publication du contenu.</span><span class="sxs-lookup"><span data-stu-id="9e182-105">The **WM/Year** attribute is the year the content was published.</span></span>

## <a name="applies-to"></a><span data-ttu-id="9e182-106">S'applique à</span><span class="sxs-lookup"><span data-stu-id="9e182-106">Applies To</span></span>

-   [<span data-ttu-id="9e182-107">Éléments audio</span><span class="sxs-lookup"><span data-stu-id="9e182-107">Audio Items</span></span>](audio-item-attributes.md)
-   [<span data-ttu-id="9e182-108">Attributs de fichiers Windows Media couramment utilisés</span><span class="sxs-lookup"><span data-stu-id="9e182-108">Commonly Used Windows Media File Attributes</span></span>](commonly-used-windows-media-file-attributes.md)

## <a name="remarks"></a><span data-ttu-id="9e182-109">Notes</span><span class="sxs-lookup"><span data-stu-id="9e182-109">Remarks</span></span>

<span data-ttu-id="9e182-110">Cet attribut est stocké uniquement dans le fichier multimédia numérique.</span><span class="sxs-lookup"><span data-stu-id="9e182-110">This attribute is stored only in the digital media file.</span></span>

<span data-ttu-id="9e182-111">Pour déterminer si vous pouvez modifier la valeur de cet attribut, utilisez la méthode [Media. isReadOnlyItem](media-isreadonlyitem.md) .</span><span class="sxs-lookup"><span data-stu-id="9e182-111">To determine whether you can change the value of this attribute, use the [Media.isReadOnlyItem](media-isreadonlyitem.md) method.</span></span>

<span data-ttu-id="9e182-112">Cet attribut ne doit pas être utilisé dans le cadre d’une condition de requête.</span><span class="sxs-lookup"><span data-stu-id="9e182-112">This attribute should not be used as part of a query condition.</span></span> <span data-ttu-id="9e182-113">Elle est dérivée d’un autre attribut et ne peut pas être interrogée directement dans une collection de supports.</span><span class="sxs-lookup"><span data-stu-id="9e182-113">It is derived from another attribute and cannot be directly queried against in a media collection.</span></span>

<span data-ttu-id="9e182-114">La constante du kit de développement logiciel (SDK) du format Windows Media pour cet attribut est g \_ wszWMYear.</span><span class="sxs-lookup"><span data-stu-id="9e182-114">The Windows Media Format SDK constant for this attribute is g\_wszWMYear.</span></span>

## <a name="requirements"></a><span data-ttu-id="9e182-115">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="9e182-115">Requirements</span></span>



| <span data-ttu-id="9e182-116">Condition requise</span><span class="sxs-lookup"><span data-stu-id="9e182-116">Requirement</span></span> | <span data-ttu-id="9e182-117">Valeur</span><span class="sxs-lookup"><span data-stu-id="9e182-117">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9e182-118">Version</span><span class="sxs-lookup"><span data-stu-id="9e182-118">Version</span></span><br/> | <span data-ttu-id="9e182-119">Le lecteur Windows Media série 9 Windows Media Player 10 ou version ultérieure ne prend pas en charge cet attribut</span><span class="sxs-lookup"><span data-stu-id="9e182-119">Windows Media Player 9 Series Windows Media Player 10 or later does not support this attribute</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="9e182-120">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="9e182-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9e182-121">**Référence d’attribut**</span><span class="sxs-lookup"><span data-stu-id="9e182-121">**Attribute Reference**</span></span>](attribute-reference.md)
</dt> </dl>

 

 





