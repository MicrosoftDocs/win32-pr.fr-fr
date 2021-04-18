---
title: EDITBOX. fontFace
description: L’attribut fontFace spécifie ou récupère la police du texte dans le contrôle zone d’édition.
ms.assetid: 5fb5e6d2-8535-402e-9ca1-d43e334e94e3
keywords:
- EDITBOX. fontFace Windows Media Player
topic_type:
- apiref
api_name:
- EDITBOX.fontFace
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 49c5794da93821db840a48facbba45540da9249a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106526612"
---
# <a name="editboxfontface"></a><span data-ttu-id="7669d-104">EDITBOX. fontFace</span><span class="sxs-lookup"><span data-stu-id="7669d-104">EDITBOX.fontFace</span></span>

<span data-ttu-id="7669d-105">L’attribut **fontFace** spécifie ou récupère la police du texte dans le contrôle zone d’édition.</span><span class="sxs-lookup"><span data-stu-id="7669d-105">The **fontFace** attribute specifies or retrieves the font for text in the edit box control.</span></span>

``` syntax
        elementID.fontFace
```

## <a name="possible-values"></a><span data-ttu-id="7669d-106">Valeurs possibles</span><span class="sxs-lookup"><span data-stu-id="7669d-106">Possible Values</span></span>

<span data-ttu-id="7669d-107">Cet attribut est une **chaîne** en lecture/écriture.</span><span class="sxs-lookup"><span data-stu-id="7669d-107">This attribute is a read/write **String**.</span></span>

## <a name="remarks"></a><span data-ttu-id="7669d-108">Notes</span><span class="sxs-lookup"><span data-stu-id="7669d-108">Remarks</span></span>

<span data-ttu-id="7669d-109">Cet attribut peut être le nom de toute police valide disponible dans Windows.</span><span class="sxs-lookup"><span data-stu-id="7669d-109">This attribute can be the name of any valid font available in Windows.</span></span> <span data-ttu-id="7669d-110">Le lecteur Windows Media ne prend pas en charge l’installation de polices. vous devez donc choisir une police sur le système souhaité.</span><span class="sxs-lookup"><span data-stu-id="7669d-110">Windows Media Player will not support installing fonts, so choose a font that you know will be on the intended system.</span></span>

<span data-ttu-id="7669d-111">Si le **fontFace** spécifié n’est pas disponible sur le système de l’utilisateur, le contrôle de zone d’édition est défini par défaut sur la police système Windows.</span><span class="sxs-lookup"><span data-stu-id="7669d-111">If the **fontFace** specified is not available on the user's system, the edit box control defaults to the Windows system font.</span></span> <span data-ttu-id="7669d-112">La valeur par défaut pour les systèmes en langue anglaise est « Tahoma ».</span><span class="sxs-lookup"><span data-stu-id="7669d-112">The default value for English-language systems is "Tahoma".</span></span> <span data-ttu-id="7669d-113">Pour les systèmes internationaux, la valeur par défaut est chargée à partir d’un fichier de ressources.</span><span class="sxs-lookup"><span data-stu-id="7669d-113">For international systems, the default is loaded from a resource file.</span></span>

## <a name="requirements"></a><span data-ttu-id="7669d-114">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="7669d-114">Requirements</span></span>



| <span data-ttu-id="7669d-115">Condition requise</span><span class="sxs-lookup"><span data-stu-id="7669d-115">Requirement</span></span> | <span data-ttu-id="7669d-116">Valeur</span><span class="sxs-lookup"><span data-stu-id="7669d-116">Value</span></span> |
|--------------------|---------------------------------------------------------|
| <span data-ttu-id="7669d-117">Version</span><span class="sxs-lookup"><span data-stu-id="7669d-117">Version</span></span><br/> | <span data-ttu-id="7669d-118">Lecteur Windows Media pour Windows XP ou version ultérieure</span><span class="sxs-lookup"><span data-stu-id="7669d-118">Windows Media Player for Windows XP or later</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="7669d-119">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="7669d-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7669d-120">**Élément EDITBOX**</span><span class="sxs-lookup"><span data-stu-id="7669d-120">**EDITBOX Element**</span></span>](editbox-element.md)
</dt> <dt>

[<span data-ttu-id="7669d-121">**EDITBOX. FontSize**</span><span class="sxs-lookup"><span data-stu-id="7669d-121">**EDITBOX.fontSize**</span></span>](editbox-fontsize.md)
</dt> <dt>

[<span data-ttu-id="7669d-122">**EDITBOX. fontStyle**</span><span class="sxs-lookup"><span data-stu-id="7669d-122">**EDITBOX.fontStyle**</span></span>](editbox-fontstyle.md)
</dt> </dl>

 

 





