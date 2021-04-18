---
title: AmbientAttributes. zIndex
description: L’attribut zIndex spécifie ou récupère l’ordre dans lequel le contrôle est rendu.
ms.assetid: b05c9efc-5d1d-4cba-89f4-b4200ce99e09
keywords:
- Lecteur Windows Media AmbientAttributes. zIndex
topic_type:
- apiref
api_name:
- AmbientAttributes.zIndex
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 52480cc387c0a9e5e45c4b8e8fd2dae4199dbd16
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106528956"
---
# <a name="ambientattributeszindex"></a><span data-ttu-id="9925f-104">AmbientAttributes. zIndex</span><span class="sxs-lookup"><span data-stu-id="9925f-104">AmbientAttributes.zIndex</span></span>

<span data-ttu-id="9925f-105">L’attribut **ZIndex** spécifie ou récupère l’ordre dans lequel le contrôle est rendu.</span><span class="sxs-lookup"><span data-stu-id="9925f-105">The **zIndex** attribute specifies or retrieves the order in which the control is rendered.</span></span>

``` syntax
        elementID.zIndex
```

## <a name="possible-values"></a><span data-ttu-id="9925f-106">Valeurs possibles</span><span class="sxs-lookup"><span data-stu-id="9925f-106">Possible Values</span></span>

<span data-ttu-id="9925f-107">Cet attribut est un **nombre** en lecture/écriture (**long**) avec une valeur par défaut de zéro.</span><span class="sxs-lookup"><span data-stu-id="9925f-107">This attribute is a read/write **Number** (**long**) with a default value of zero.</span></span> <span data-ttu-id="9925f-108">La plage est celle d’un entier long signé.</span><span class="sxs-lookup"><span data-stu-id="9925f-108">The range is that of a signed long integer.</span></span>

## <a name="remarks"></a><span data-ttu-id="9925f-109">Notes</span><span class="sxs-lookup"><span data-stu-id="9925f-109">Remarks</span></span>

<span data-ttu-id="9925f-110">L’image bitmap d’arrière-plan d’une **vue** ou d’un sous- **affichage** a un index z fixe égal à zéro.</span><span class="sxs-lookup"><span data-stu-id="9925f-110">The background bitmap of a **VIEW** or **SUBVIEW** has a fixed z index of zero.</span></span> <span data-ttu-id="9925f-111">Si vous souhaitez qu’un contrôle soit derrière l’arrière-plan, **ZIndex** doit être défini sur un nombre négatif.</span><span class="sxs-lookup"><span data-stu-id="9925f-111">If you want a control to be behind the background, the **zIndex** must be set to a negative number.</span></span>

<span data-ttu-id="9925f-112">L’index z d’une **vue** ou d’une sous- **vue** est un index absolu, tandis que l’index z d’un contrôle est relatif à l’index z de la **vue** ou de la sous- **vue** qui le contient.</span><span class="sxs-lookup"><span data-stu-id="9925f-112">The z index of a **VIEW** or **SUBVIEW** is an absolute index, while the z index of a control is relative to the z index of the **VIEW** or **SUBVIEW** that contains it.</span></span>

<span data-ttu-id="9925f-113">L’attribut **ZIndex** n’est pas pris en charge par les éléments **Browser** et **playlist** .</span><span class="sxs-lookup"><span data-stu-id="9925f-113">The **zIndex** attribute is not supported by the **BROWSER** and **PLAYLIST** elements.</span></span> <span data-ttu-id="9925f-114">Elle ne fonctionnera pas avec l’élément **vidéo** si vous utilisez la *vidéo*. **sans fenêtre** est défini sur false, ni avec l’élément **Effects** si **Effects**. **Windowed** a la valeur true.</span><span class="sxs-lookup"><span data-stu-id="9925f-114">It will not work with the **VIDEO** element if *VIDEO*.**windowless** is set to false, nor with the **EFFECTS** element if **EFFECTS**.**windowed** is set to true.</span></span>

<span data-ttu-id="9925f-115">Les éléments **BUTTONELEMENT** utilisent le **ZIndex** de leur **BUTTONGROUP**.</span><span class="sxs-lookup"><span data-stu-id="9925f-115">**BUTTONELEMENT** elements use the **zIndex** of their **BUTTONGROUP**.</span></span>

## <a name="requirements"></a><span data-ttu-id="9925f-116">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="9925f-116">Requirements</span></span>



| <span data-ttu-id="9925f-117">Condition requise</span><span class="sxs-lookup"><span data-stu-id="9925f-117">Requirement</span></span> | <span data-ttu-id="9925f-118">Valeur</span><span class="sxs-lookup"><span data-stu-id="9925f-118">Value</span></span> |
|--------------------|------------------------------------------------------|
| <span data-ttu-id="9925f-119">Version</span><span class="sxs-lookup"><span data-stu-id="9925f-119">Version</span></span><br/> | <span data-ttu-id="9925f-120">Lecteur Windows Media version 7,0 ou ultérieure</span><span class="sxs-lookup"><span data-stu-id="9925f-120">Windows Media Player version 7.0 or later</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="9925f-121">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="9925f-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9925f-122">**Attributs ambiants**</span><span class="sxs-lookup"><span data-stu-id="9925f-122">**Ambient Attributes**</span></span>](ambient-attributes.md)
</dt> </dl>

 

 





