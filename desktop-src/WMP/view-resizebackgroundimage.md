---
title: VUE. resizeBackgroundImage
description: L’attribut resizeBackgroundImage spécifie ou récupère une valeur indiquant si l’image d’arrière-plan peut être redimensionnée.
ms.assetid: d18f3def-777f-4a71-961e-73bae98a4c64
keywords:
- AFFICHER. resizeBackgroundImage lecteur Windows Media
topic_type:
- apiref
api_name:
- VIEW.resizeBackgroundImage
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 397929d69cc6ac6ad51c29883898c153218afdca
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106525322"
---
# <a name="viewresizebackgroundimage"></a><span data-ttu-id="0a4e9-104">VUE. resizeBackgroundImage</span><span class="sxs-lookup"><span data-stu-id="0a4e9-104">VIEW.resizeBackgroundImage</span></span>

<span data-ttu-id="0a4e9-105">L’attribut **resizeBackgroundImage** spécifie ou récupère une valeur indiquant si l’image d’arrière-plan peut être redimensionnée.</span><span class="sxs-lookup"><span data-stu-id="0a4e9-105">The **resizeBackgroundImage** attribute specifies or retrieves a value indicating whether the background image can be resized.</span></span>

``` syntax
        elementID.resizeBackgroundImage
```

## <a name="possible-values"></a><span data-ttu-id="0a4e9-106">Valeurs possibles</span><span class="sxs-lookup"><span data-stu-id="0a4e9-106">Possible Values</span></span>

<span data-ttu-id="0a4e9-107">Cet attribut est une **valeur booléenne** en lecture/écriture.</span><span class="sxs-lookup"><span data-stu-id="0a4e9-107">This attribute is a read/write **Boolean**.</span></span>



| <span data-ttu-id="0a4e9-108">Valeurs</span><span class="sxs-lookup"><span data-stu-id="0a4e9-108">Values</span></span> | <span data-ttu-id="0a4e9-109">Description</span><span class="sxs-lookup"><span data-stu-id="0a4e9-109">Description</span></span>                                      |
|--------|--------------------------------------------------|
| <span data-ttu-id="0a4e9-110">true</span><span class="sxs-lookup"><span data-stu-id="0a4e9-110">true</span></span>   | <span data-ttu-id="0a4e9-111">L’image d’arrière-plan peut être redimensionnée.</span><span class="sxs-lookup"><span data-stu-id="0a4e9-111">The background image can be resized.</span></span>             |
| <span data-ttu-id="0a4e9-112">false</span><span class="sxs-lookup"><span data-stu-id="0a4e9-112">false</span></span>  | <span data-ttu-id="0a4e9-113">Par défaut.</span><span class="sxs-lookup"><span data-stu-id="0a4e9-113">Default.</span></span> <span data-ttu-id="0a4e9-114">Impossible de redimensionner l’image d’arrière-plan.</span><span class="sxs-lookup"><span data-stu-id="0a4e9-114">The background image cannot be resized.</span></span> |



 

## <a name="remarks"></a><span data-ttu-id="0a4e9-115">Notes</span><span class="sxs-lookup"><span data-stu-id="0a4e9-115">Remarks</span></span>

<span data-ttu-id="0a4e9-116">Si vous affectez à cet attribut la valeur true, l’image d’arrière-plan est redimensionnée pour s’ajuster aux valeurs actuelles des attributs **Width** et **Height** .</span><span class="sxs-lookup"><span data-stu-id="0a4e9-116">If you set this attribute to true, the background image will resize to fit the current values of the **width** and **height** attributes.</span></span>

## <a name="requirements"></a><span data-ttu-id="0a4e9-117">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="0a4e9-117">Requirements</span></span>



| <span data-ttu-id="0a4e9-118">Condition requise</span><span class="sxs-lookup"><span data-stu-id="0a4e9-118">Requirement</span></span> | <span data-ttu-id="0a4e9-119">Valeur</span><span class="sxs-lookup"><span data-stu-id="0a4e9-119">Value</span></span> |
|--------------------|---------------------------------------------------|
| <span data-ttu-id="0a4e9-120">Version</span><span class="sxs-lookup"><span data-stu-id="0a4e9-120">Version</span></span><br/> | <span data-ttu-id="0a4e9-121">Lecteur Windows Media série 9 ou version ultérieure</span><span class="sxs-lookup"><span data-stu-id="0a4e9-121">Windows Media Player 9 Series or later</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="0a4e9-122">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="0a4e9-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0a4e9-123">**Élément VIEW**</span><span class="sxs-lookup"><span data-stu-id="0a4e9-123">**VIEW Element**</span></span>](view-element.md)
</dt> <dt>

[<span data-ttu-id="0a4e9-124">**VIEW. backgroundImage**</span><span class="sxs-lookup"><span data-stu-id="0a4e9-124">**VIEW.backgroundImage**</span></span>](view-backgroundimage.md)
</dt> </dl>

 

 





