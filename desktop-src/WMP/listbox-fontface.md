---
title: LISTBOX. fontFace
description: L’attribut fontFace spécifie ou récupère la police du contrôle de zone de liste.
ms.assetid: 15e3180a-6e1e-4654-a0bb-164d66a86a26
keywords:
- LISTBOX. fontFace Windows Media Player
topic_type:
- apiref
api_name:
- LISTBOX.fontFace
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 82c03c367001b307dd8bd5059ec7e3f4a0b364e6
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106532617"
---
# <a name="listboxfontface"></a><span data-ttu-id="74141-104">LISTBOX. fontFace</span><span class="sxs-lookup"><span data-stu-id="74141-104">LISTBOX.fontFace</span></span>

<span data-ttu-id="74141-105">L’attribut **fontFace** spécifie ou récupère la police du contrôle de zone de liste.</span><span class="sxs-lookup"><span data-stu-id="74141-105">The **fontFace** attribute specifies or retrieves the font for the list box control.</span></span>

``` syntax
        elementID.fontFace
```

## <a name="possible-values"></a><span data-ttu-id="74141-106">Valeurs possibles</span><span class="sxs-lookup"><span data-stu-id="74141-106">Possible Values</span></span>

<span data-ttu-id="74141-107">Cet attribut est une **chaîne** en lecture/écriture.</span><span class="sxs-lookup"><span data-stu-id="74141-107">This attribute is a read/write **String**.</span></span>

## <a name="remarks"></a><span data-ttu-id="74141-108">Notes</span><span class="sxs-lookup"><span data-stu-id="74141-108">Remarks</span></span>

<span data-ttu-id="74141-109">Cet attribut peut être le nom de toute police valide disponible dans Windows.</span><span class="sxs-lookup"><span data-stu-id="74141-109">This attribute can be the name of any valid font available in Windows.</span></span> <span data-ttu-id="74141-110">Le lecteur Windows Media ne prend pas en charge l’installation de polices. vous devez donc choisir une police sur le système souhaité.</span><span class="sxs-lookup"><span data-stu-id="74141-110">Windows Media Player will not support installing fonts, so choose a font that you know will be on the intended system.</span></span>

<span data-ttu-id="74141-111">Si le **fontFace** spécifié n’est pas disponible sur le système de l’utilisateur, le contrôle de zone de liste est défini par défaut sur la police système Windows.</span><span class="sxs-lookup"><span data-stu-id="74141-111">If the **fontFace** specified is not available on the user's system, the list box control defaults to the Windows system font.</span></span> <span data-ttu-id="74141-112">La valeur par défaut pour les systèmes en langue anglaise est « Tahoma ».</span><span class="sxs-lookup"><span data-stu-id="74141-112">The default value for English-language systems is "Tahoma".</span></span> <span data-ttu-id="74141-113">Pour les systèmes internationaux, la valeur par défaut est chargée à partir d’un fichier de ressources.</span><span class="sxs-lookup"><span data-stu-id="74141-113">For international systems, the default is loaded from a resource file.</span></span>

## <a name="requirements"></a><span data-ttu-id="74141-114">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="74141-114">Requirements</span></span>



| <span data-ttu-id="74141-115">Condition requise</span><span class="sxs-lookup"><span data-stu-id="74141-115">Requirement</span></span> | <span data-ttu-id="74141-116">Valeur</span><span class="sxs-lookup"><span data-stu-id="74141-116">Value</span></span> |
|--------------------|---------------------------------------------------------|
| <span data-ttu-id="74141-117">Version</span><span class="sxs-lookup"><span data-stu-id="74141-117">Version</span></span><br/> | <span data-ttu-id="74141-118">Lecteur Windows Media pour Windows XP ou version ultérieure</span><span class="sxs-lookup"><span data-stu-id="74141-118">Windows Media Player for Windows XP or later</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="74141-119">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="74141-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="74141-120">**Élément LISTBOX**</span><span class="sxs-lookup"><span data-stu-id="74141-120">**LISTBOX Element**</span></span>](listbox-element.md)
</dt> <dt>

[<span data-ttu-id="74141-121">**LISTBOX. FontSize**</span><span class="sxs-lookup"><span data-stu-id="74141-121">**LISTBOX.fontSize**</span></span>](listbox-fontsize.md)
</dt> <dt>

[<span data-ttu-id="74141-122">**LISTBOX. fontStyle**</span><span class="sxs-lookup"><span data-stu-id="74141-122">**LISTBOX.fontStyle**</span></span>](listbox-fontstyle.md)
</dt> </dl>

 

 





