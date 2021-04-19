---
title: AmbientAttributes. Enabled
description: L’attribut enabled spécifie ou récupère une valeur indiquant si le contrôle est activé ou désactivé.
ms.assetid: cf96ab7c-8acd-42b6-b7ca-d084a89c97e2
keywords:
- Lecteur Windows Media activé pour AmbientAttributes.
topic_type:
- apiref
api_name:
- AmbientAttributes.enabled
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7c34d24e86118a1cca0939d535b6da6e86c2df34
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106527288"
---
# <a name="ambientattributesenabled"></a><span data-ttu-id="59ede-104">AmbientAttributes. Enabled</span><span class="sxs-lookup"><span data-stu-id="59ede-104">AmbientAttributes.enabled</span></span>

<span data-ttu-id="59ede-105">L’attribut **Enabled** spécifie ou récupère une valeur indiquant si le contrôle est activé ou désactivé.</span><span class="sxs-lookup"><span data-stu-id="59ede-105">The **enabled** attribute specifies or retrieves a value indicating whether the control is enabled or disabled.</span></span>

``` syntax
        elementID.enabled
```

## <a name="possible-values"></a><span data-ttu-id="59ede-106">Valeurs possibles</span><span class="sxs-lookup"><span data-stu-id="59ede-106">Possible Values</span></span>

<span data-ttu-id="59ede-107">Cet attribut est une **valeur booléenne** en lecture/écriture.</span><span class="sxs-lookup"><span data-stu-id="59ede-107">This attribute is a read/write **Boolean**.</span></span>



| <span data-ttu-id="59ede-108">Valeur</span><span class="sxs-lookup"><span data-stu-id="59ede-108">Value</span></span> | <span data-ttu-id="59ede-109">Description</span><span class="sxs-lookup"><span data-stu-id="59ede-109">Description</span></span>               |
|-------|---------------------------|
| <span data-ttu-id="59ede-110">true</span><span class="sxs-lookup"><span data-stu-id="59ede-110">true</span></span>  | <span data-ttu-id="59ede-111">Par défaut.</span><span class="sxs-lookup"><span data-stu-id="59ede-111">Default.</span></span> <span data-ttu-id="59ede-112">Contrôle activé.</span><span class="sxs-lookup"><span data-stu-id="59ede-112">Control enabled.</span></span> |
| <span data-ttu-id="59ede-113">false</span><span class="sxs-lookup"><span data-stu-id="59ede-113">false</span></span> | <span data-ttu-id="59ede-114">Contrôle désactivé.</span><span class="sxs-lookup"><span data-stu-id="59ede-114">Control disabled.</span></span>         |



 

## <a name="remarks"></a><span data-ttu-id="59ede-115">Notes</span><span class="sxs-lookup"><span data-stu-id="59ede-115">Remarks</span></span>

<span data-ttu-id="59ede-116">Si le contrôle est activé, il peut avoir un taquet de tabulation et recevra tous les événements ambiants.</span><span class="sxs-lookup"><span data-stu-id="59ede-116">If the control is enabled, it can have a tab stop, and will receive all ambient events.</span></span> <span data-ttu-id="59ede-117">Quand elle est désactivée, le contrôle n’a pas de taquet de tabulation et ne reçoit aucun événement de souris ou de clavier ambiant déclenché.</span><span class="sxs-lookup"><span data-stu-id="59ede-117">When disabled, the control does not have a tab stop, and does not receive any ambient mouse or keyboard events fired to it.</span></span> <span data-ttu-id="59ede-118">(Toutefois, il continuera à recevoir tous les autres événements ambiants qui lui sont déclenchés.)</span><span class="sxs-lookup"><span data-stu-id="59ede-118">(However, it will continue to receive all other ambient events fired to it.)</span></span>

<span data-ttu-id="59ede-119">Cet attribut n’est pas pris en charge pour l’élément **subview** .</span><span class="sxs-lookup"><span data-stu-id="59ede-119">This attribute is not supported for the **SUBVIEW** element.</span></span>

## <a name="requirements"></a><span data-ttu-id="59ede-120">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="59ede-120">Requirements</span></span>



| <span data-ttu-id="59ede-121">Condition requise</span><span class="sxs-lookup"><span data-stu-id="59ede-121">Requirement</span></span> | <span data-ttu-id="59ede-122">Valeur</span><span class="sxs-lookup"><span data-stu-id="59ede-122">Value</span></span> |
|--------------------|------------------------------------------------------|
| <span data-ttu-id="59ede-123">Version</span><span class="sxs-lookup"><span data-stu-id="59ede-123">Version</span></span><br/> | <span data-ttu-id="59ede-124">Lecteur Windows Media version 7,0 ou ultérieure</span><span class="sxs-lookup"><span data-stu-id="59ede-124">Windows Media Player version 7.0 or later</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="59ede-125">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="59ede-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="59ede-126">**Attributs ambiants**</span><span class="sxs-lookup"><span data-stu-id="59ede-126">**Ambient Attributes**</span></span>](ambient-attributes.md)
</dt> </dl>

 

 





