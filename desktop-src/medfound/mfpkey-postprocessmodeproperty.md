---
description: Spécifie le mode de traitement de la publication pour le décodeur.
ms.assetid: c6dab7f6-4a3e-45bb-b81c-5f4c39f9e954
title: MFPKEY_POSTPROCESSMODE, propriété (Wmcodecdsp. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a4002deae63f1bdaea09ca31dd95bfec1cb594fc
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106535401"
---
# <a name="mfpkey_postprocessmode-property"></a><span data-ttu-id="5f792-103">MFPKEY \_ propriété POSTPROCESSMODE</span><span class="sxs-lookup"><span data-stu-id="5f792-103">MFPKEY\_POSTPROCESSMODE Property</span></span>

<span data-ttu-id="5f792-104">Spécifie le mode de traitement de la publication pour le décodeur.</span><span class="sxs-lookup"><span data-stu-id="5f792-104">Specifies the post processing mode for the decoder.</span></span>

## <a name="constant-for-ipropertybag"></a><span data-ttu-id="5f792-105">Constante pour IPropertyBag</span><span class="sxs-lookup"><span data-stu-id="5f792-105">Constant for IPropertyBag</span></span>

<span data-ttu-id="5f792-106">**\_wszWMVCForcePostProcessMode g**</span><span class="sxs-lookup"><span data-stu-id="5f792-106">**g\_wszWMVCForcePostProcessMode**</span></span>

## <a name="data-type"></a><span data-ttu-id="5f792-107">Type de données</span><span class="sxs-lookup"><span data-stu-id="5f792-107">Data Type</span></span>

<span data-ttu-id="5f792-108">**VT \_**</span><span class="sxs-lookup"><span data-stu-id="5f792-108">**VT\_I4**</span></span>

## <a name="remarks"></a><span data-ttu-id="5f792-109">Notes</span><span class="sxs-lookup"><span data-stu-id="5f792-109">Remarks</span></span>

<span data-ttu-id="5f792-110">Définissez cette propriété sur l’une des valeurs suivantes.</span><span class="sxs-lookup"><span data-stu-id="5f792-110">Set this property to one of the following values.</span></span>



| <span data-ttu-id="5f792-111">Valeur</span><span class="sxs-lookup"><span data-stu-id="5f792-111">Value</span></span> | <span data-ttu-id="5f792-112">Signification</span><span class="sxs-lookup"><span data-stu-id="5f792-112">Meaning</span></span>                                                                                |
|-------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="5f792-113">-1</span><span class="sxs-lookup"><span data-stu-id="5f792-113">-1</span></span>    | <span data-ttu-id="5f792-114">Le décodeur définit le mode de traitement de publication de manière adaptative en fonction des ressources processeur disponibles.</span><span class="sxs-lookup"><span data-stu-id="5f792-114">The decoder sets the post processing mode adaptively based on available CPU resources.</span></span> |
| <span data-ttu-id="5f792-115">0</span><span class="sxs-lookup"><span data-stu-id="5f792-115">0</span></span>     | <span data-ttu-id="5f792-116">Le décodeur n’exécute aucun traitement de validation.</span><span class="sxs-lookup"><span data-stu-id="5f792-116">The decoder performs no post processing.</span></span>                                               |
| <span data-ttu-id="5f792-117">1</span><span class="sxs-lookup"><span data-stu-id="5f792-117">1</span></span>     | <span data-ttu-id="5f792-118">le décodeur récupère effectue un déblocage rapide.</span><span class="sxs-lookup"><span data-stu-id="5f792-118">fThe decoder performs fast deblocking.</span></span>                                                 |
| <span data-ttu-id="5f792-119">2</span><span class="sxs-lookup"><span data-stu-id="5f792-119">2</span></span>     | <span data-ttu-id="5f792-120">Le décodeur effectue un déblocage complet.</span><span class="sxs-lookup"><span data-stu-id="5f792-120">The decoder performs full deblocking.</span></span>                                                  |
| <span data-ttu-id="5f792-121">3</span><span class="sxs-lookup"><span data-stu-id="5f792-121">3</span></span>     | <span data-ttu-id="5f792-122">Le décodeur effectue un déblocage rapide et une désonne.</span><span class="sxs-lookup"><span data-stu-id="5f792-122">The decoder performs fast deblocking and deringing.</span></span>                                    |
| <span data-ttu-id="5f792-123">4</span><span class="sxs-lookup"><span data-stu-id="5f792-123">4</span></span>     | <span data-ttu-id="5f792-124">Le décodeur effectue un déblocage complet et une désonne.</span><span class="sxs-lookup"><span data-stu-id="5f792-124">The decoder performs full deblocking and deringing.</span></span>                                    |



 

<span data-ttu-id="5f792-125">Comme la valeur de cette propriété est comprise entre 0 et 4, la complexité du décodage, l’utilisation des ressources du processeur et la qualité de l’image augmentent.</span><span class="sxs-lookup"><span data-stu-id="5f792-125">As the value of this property goes from 0 to 4, the decoding complexity, use of CPU resources, and picture quality all increase.</span></span>

## <a name="requirements"></a><span data-ttu-id="5f792-126">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="5f792-126">Requirements</span></span>



| <span data-ttu-id="5f792-127">Condition requise</span><span class="sxs-lookup"><span data-stu-id="5f792-127">Requirement</span></span> | <span data-ttu-id="5f792-128">Valeur</span><span class="sxs-lookup"><span data-stu-id="5f792-128">Value</span></span> |
|-------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="5f792-129">Client</span><span class="sxs-lookup"><span data-stu-id="5f792-129">Client</span></span><br/> | <span data-ttu-id="5f792-130">Windows Vista ou Windows 7</span><span class="sxs-lookup"><span data-stu-id="5f792-130">Windows Vista or Windows 7</span></span><br/>                                                   |
| <span data-ttu-id="5f792-131">En-tête</span><span class="sxs-lookup"><span data-stu-id="5f792-131">Header</span></span><br/> | <dl> <span data-ttu-id="5f792-132"><dt>Wmcodecdsp. h</dt></span><span class="sxs-lookup"><span data-stu-id="5f792-132"><dt>Wmcodecdsp.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5f792-133">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="5f792-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5f792-134">Propriétés de la Media Foundation</span><span class="sxs-lookup"><span data-stu-id="5f792-134">Media Foundation Properties</span></span>](media-foundation-properties.md)
</dt> </dl>

 

 




