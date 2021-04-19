---
description: Spécifie si la complexité de l’algorithme d’encodage audio est restreinte.
ms.assetid: a50b840f-9fe8-4291-b93f-f09c241fe802
title: MFPKEY_CONSTRAINENCOMPLEXITY, propriété (Wmcodecdsp. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bdc6e3d5a7077c72e5933ecbc235092174e263fe
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106534205"
---
# <a name="mfpkey_constrainencomplexity-property"></a><span data-ttu-id="f4b78-103">MFPKEY \_ propriété CONSTRAINENCOMPLEXITY</span><span class="sxs-lookup"><span data-stu-id="f4b78-103">MFPKEY\_CONSTRAINENCOMPLEXITY Property</span></span>

<span data-ttu-id="f4b78-104">Spécifie si la complexité de l’algorithme d’encodage audio est restreinte.</span><span class="sxs-lookup"><span data-stu-id="f4b78-104">Specifies whether the complexity of the audio encoding algorithm is constrained.</span></span>

## <a name="constant-for-ipropertybag"></a><span data-ttu-id="f4b78-105">Constante pour IPropertyBag</span><span class="sxs-lookup"><span data-stu-id="f4b78-105">Constant for IPropertyBag</span></span>

<span data-ttu-id="f4b78-106">Disponible uniquement à l’aide de [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore).</span><span class="sxs-lookup"><span data-stu-id="f4b78-106">Available only by using [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore).</span></span>

## <a name="data-type"></a><span data-ttu-id="f4b78-107">Type de données</span><span class="sxs-lookup"><span data-stu-id="f4b78-107">Data Type</span></span>

<span data-ttu-id="f4b78-108">**VT \_ bool**</span><span class="sxs-lookup"><span data-stu-id="f4b78-108">**VT\_BOOL**</span></span>

## <a name="default-value"></a><span data-ttu-id="f4b78-109">Valeur par défaut</span><span class="sxs-lookup"><span data-stu-id="f4b78-109">Default Value</span></span>

<span data-ttu-id="f4b78-110">**VARIANTE \_ false**</span><span class="sxs-lookup"><span data-stu-id="f4b78-110">**VARIANT\_FALSE**</span></span>

## <a name="remarks"></a><span data-ttu-id="f4b78-111">Notes</span><span class="sxs-lookup"><span data-stu-id="f4b78-111">Remarks</span></span>

<span data-ttu-id="f4b78-112">Si vous laissez cette propriété à sa valeur par défaut **Variant \_ false**, l’encodeur audio utilise son algorithme par défaut.</span><span class="sxs-lookup"><span data-stu-id="f4b78-112">If you leave this property at its default value of **VARIANT\_FALSE**, the audio encoder uses its default algorithm.</span></span> <span data-ttu-id="f4b78-113">L’algorithme par défaut dépend du type de sortie et de la version de Windows en cours d’exécution.</span><span class="sxs-lookup"><span data-stu-id="f4b78-113">The default algorithm depends on the output type and which version of Windows is running.</span></span> <span data-ttu-id="f4b78-114">Le tableau suivant décrit le comportement par défaut pour les différentes combinaisons.</span><span class="sxs-lookup"><span data-stu-id="f4b78-114">The following table describes the default behavior for the different combinations.</span></span>



| <span data-ttu-id="f4b78-115">Système d’exploitation</span><span class="sxs-lookup"><span data-stu-id="f4b78-115">Operating system</span></span> | <span data-ttu-id="f4b78-116">Comportement par défaut</span><span class="sxs-lookup"><span data-stu-id="f4b78-116">Default behavior</span></span>                                                                                                                                                                                    |
|------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f4b78-117">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="f4b78-117">Windows Vista</span></span>    | <span data-ttu-id="f4b78-118">Pour tous les types de sortie, l’encodeur audio utilise par défaut l’algorithme le plus complexe.</span><span class="sxs-lookup"><span data-stu-id="f4b78-118">For all output types, the audio encoder uses the most complex algorithm by default.</span></span>                                                                                                                 |
| <span data-ttu-id="f4b78-119">Windows 7</span><span class="sxs-lookup"><span data-stu-id="f4b78-119">Windows 7</span></span>        | <span data-ttu-id="f4b78-120">Pour les types de sortie standard et Professional, l’encodeur audio utilise l’algorithme le plus complexe par défaut.</span><span class="sxs-lookup"><span data-stu-id="f4b78-120">For Standard and Professional output types, the audio encoder uses the most complex algorithm by default.</span></span> <span data-ttu-id="f4b78-121">Pour les types de sortie sans perte, l’encodeur audio utilise l’algorithme le moins complexe par défaut.</span><span class="sxs-lookup"><span data-stu-id="f4b78-121">For Lossless output types, the audio encoder uses the least complex algorithm by default.</span></span> |



 

<span data-ttu-id="f4b78-122">Si vous affectez à cette propriété la valeur **Variant \_ true**, vous devez également spécifier une valeur de complexité en définissant la propriété [**MFPKEY \_ ENCCOMPLEXITY**](mfpkey-enccomplexityproperty.md) .</span><span class="sxs-lookup"><span data-stu-id="f4b78-122">If you set this property to **VARIANT\_TRUE**, you must also specify a complexity value by setting the [**MFPKEY\_ENCCOMPLEXITY**](mfpkey-enccomplexityproperty.md) property.</span></span>

## <a name="requirements"></a><span data-ttu-id="f4b78-123">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="f4b78-123">Requirements</span></span>



| <span data-ttu-id="f4b78-124">Condition requise</span><span class="sxs-lookup"><span data-stu-id="f4b78-124">Requirement</span></span> | <span data-ttu-id="f4b78-125">Valeur</span><span class="sxs-lookup"><span data-stu-id="f4b78-125">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="f4b78-126">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="f4b78-126">Minimum supported client</span></span><br/> | <span data-ttu-id="f4b78-127">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="f4b78-127">Windows Vista \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="f4b78-128">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="f4b78-128">Minimum supported server</span></span><br/> | <span data-ttu-id="f4b78-129">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="f4b78-129">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="f4b78-130">En-tête</span><span class="sxs-lookup"><span data-stu-id="f4b78-130">Header</span></span><br/>                   | <dl> <span data-ttu-id="f4b78-131"><dt>Wmcodecdsp. h</dt></span><span class="sxs-lookup"><span data-stu-id="f4b78-131"><dt>Wmcodecdsp.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f4b78-132">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="f4b78-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f4b78-133">Propriétés de la Media Foundation</span><span class="sxs-lookup"><span data-stu-id="f4b78-133">Media Foundation Properties</span></span>](media-foundation-properties.md)
</dt> </dl>

 

 
