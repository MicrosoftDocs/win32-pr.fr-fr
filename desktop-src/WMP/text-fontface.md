---
title: TEXT. fontFace
description: L’attribut fontFace spécifie ou récupère le caractère du contrôle de texte.
ms.assetid: 3b39e245-139a-4361-b678-0f9e962996b7
keywords:
- TEXT. fontFace Windows Media Player
topic_type:
- apiref
api_name:
- TEXT.fontFace
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 183b25547e456cb90cac4d2137354679e13d8a96
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106526325"
---
# <a name="textfontface"></a><span data-ttu-id="1e7e5-104">TEXT. fontFace</span><span class="sxs-lookup"><span data-stu-id="1e7e5-104">TEXT.fontFace</span></span>

<span data-ttu-id="1e7e5-105">L’attribut **fontFace** spécifie ou récupère le caractère du contrôle de texte.</span><span class="sxs-lookup"><span data-stu-id="1e7e5-105">The **fontFace** attribute specifies or retrieves the typeface for the Text control.</span></span>

``` syntax
        elementID.fontFace
```

## <a name="possible-values"></a><span data-ttu-id="1e7e5-106">Valeurs possibles</span><span class="sxs-lookup"><span data-stu-id="1e7e5-106">Possible Values</span></span>

<span data-ttu-id="1e7e5-107">Cet attribut est une **chaîne** en lecture/écriture.</span><span class="sxs-lookup"><span data-stu-id="1e7e5-107">This attribute is a read/write **String**.</span></span>

## <a name="remarks"></a><span data-ttu-id="1e7e5-108">Notes</span><span class="sxs-lookup"><span data-stu-id="1e7e5-108">Remarks</span></span>

<span data-ttu-id="1e7e5-109">Cet attribut peut être le nom de toute police valide disponible sur Windows.</span><span class="sxs-lookup"><span data-stu-id="1e7e5-109">This attribute can be the name of any valid font available on Windows.</span></span> <span data-ttu-id="1e7e5-110">Le lecteur Windows Media ne prend pas en charge l’installation de polices. vous devez donc choisir une police sur le système souhaité.</span><span class="sxs-lookup"><span data-stu-id="1e7e5-110">Windows Media Player will not support installing fonts, so choose a font that you know will be on the intended system.</span></span>

<span data-ttu-id="1e7e5-111">Si le **fontFace** spécifié n’est pas disponible sur le système de l’utilisateur, le contrôle de texte prend par défaut la police système Windows.</span><span class="sxs-lookup"><span data-stu-id="1e7e5-111">If the **fontFace** specified is not available on the user's system, the Text control defaults to the Windows system font.</span></span>

<span data-ttu-id="1e7e5-112">Pour obtenir un exemple illustrant l’utilisation des attributs de l’élément de **texte** , consultez l’attribut [value](text-value.md) .</span><span class="sxs-lookup"><span data-stu-id="1e7e5-112">See the [value](text-value.md) attribute for a sample illustrating how the attributes of the **TEXT** element are used.</span></span>

## <a name="requirements"></a><span data-ttu-id="1e7e5-113">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="1e7e5-113">Requirements</span></span>



| <span data-ttu-id="1e7e5-114">Condition requise</span><span class="sxs-lookup"><span data-stu-id="1e7e5-114">Requirement</span></span> | <span data-ttu-id="1e7e5-115">Valeur</span><span class="sxs-lookup"><span data-stu-id="1e7e5-115">Value</span></span> |
|--------------------|------------------------------------------------------|
| <span data-ttu-id="1e7e5-116">Version</span><span class="sxs-lookup"><span data-stu-id="1e7e5-116">Version</span></span><br/> | <span data-ttu-id="1e7e5-117">Lecteur Windows Media version 7,0 ou ultérieure</span><span class="sxs-lookup"><span data-stu-id="1e7e5-117">Windows Media Player version 7.0 or later</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="1e7e5-118">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="1e7e5-118">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1e7e5-119">**Élément de texte**</span><span class="sxs-lookup"><span data-stu-id="1e7e5-119">**TEXT Element**</span></span>](text-element.md)
</dt> <dt>

[<span data-ttu-id="1e7e5-120">**TEXT. FontSize**</span><span class="sxs-lookup"><span data-stu-id="1e7e5-120">**TEXT.fontSize**</span></span>](text-fontsize.md)
</dt> </dl>

 

 





