---
description: Spécifie les paramètres de qualité visuelle optimaux à utiliser pour l’encodeur de profil avancé Windows Media Video 9.
ms.assetid: 9449b5fa-4f13-4c33-bfdf-611720e8dd77
title: MFPKEY_COMPRESSIONOPTIMIZATIONTYPE, propriété (Wmcodecdsp. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3000caa10aa7db7d201cd11fd9a189fd6ac33591
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106524160"
---
# <a name="mfpkey_compressionoptimizationtype-property"></a><span data-ttu-id="33953-103">MFPKEY \_ propriété COMPRESSIONOPTIMIZATIONTYPE</span><span class="sxs-lookup"><span data-stu-id="33953-103">MFPKEY\_COMPRESSIONOPTIMIZATIONTYPE Property</span></span>

<span data-ttu-id="33953-104">Spécifie les paramètres de qualité visuelle optimaux à utiliser pour l’encodeur de profil avancé Windows Media Video 9.</span><span class="sxs-lookup"><span data-stu-id="33953-104">Specifies the optimal visual quality settings to use for the Windows Media Video 9 Advanced Profile encoder.</span></span>

## <a name="constant-for-ipropertybag"></a><span data-ttu-id="33953-105">Constante pour IPropertyBag</span><span class="sxs-lookup"><span data-stu-id="33953-105">Constant for IPropertyBag</span></span>

<span data-ttu-id="33953-106">\_wszWMVCCompressionOptimizationType g</span><span class="sxs-lookup"><span data-stu-id="33953-106">g\_wszWMVCCompressionOptimizationType</span></span>

## <a name="data-type"></a><span data-ttu-id="33953-107">Type de données</span><span class="sxs-lookup"><span data-stu-id="33953-107">Data Type</span></span>

<span data-ttu-id="33953-108">VT \_</span><span class="sxs-lookup"><span data-stu-id="33953-108">VT\_I4</span></span>

## <a name="default-value"></a><span data-ttu-id="33953-109">Valeur par défaut</span><span class="sxs-lookup"><span data-stu-id="33953-109">Default Value</span></span>

<span data-ttu-id="33953-110">0</span><span class="sxs-lookup"><span data-stu-id="33953-110">0</span></span>

## <a name="remarks"></a><span data-ttu-id="33953-111">Notes</span><span class="sxs-lookup"><span data-stu-id="33953-111">Remarks</span></span>

<span data-ttu-id="33953-112">Cette propriété offre un moyen rapide de configurer un certain nombre d’options d’encodage vidéo.</span><span class="sxs-lookup"><span data-stu-id="33953-112">This property provides a quick way to configure a number of video encoding options.</span></span> <span data-ttu-id="33953-113">Il peut être défini sur l’une des valeurs suivantes.</span><span class="sxs-lookup"><span data-stu-id="33953-113">It may be set to one of the following values.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="33953-114">Valeur</span><span class="sxs-lookup"><span data-stu-id="33953-114">Value</span></span></th>
<th><span data-ttu-id="33953-115">Description</span><span class="sxs-lookup"><span data-stu-id="33953-115">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="33953-116">0</span><span class="sxs-lookup"><span data-stu-id="33953-116">0</span></span></td>
<td><span data-ttu-id="33953-117">Le codec ne force pas l’optimisation et utilise toutes les fonctionnalités spécifiées par d’autres propriétés.</span><span class="sxs-lookup"><span data-stu-id="33953-117">The codec will not force optimization and will use whatever features are specified by other properties.</span></span> <span data-ttu-id="33953-118">Dans de nombreux cas, le codec utilise la logique interne pour déterminer les paramètres s’ils ne sont pas spécifiés.</span><span class="sxs-lookup"><span data-stu-id="33953-118">In many cases, the codec will use internal logic to determine settings if they are not specified.</span></span> <span data-ttu-id="33953-119">Il s’agit de la valeur par défaut.</span><span class="sxs-lookup"><span data-stu-id="33953-119">This is the default value.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="33953-120">1</span><span class="sxs-lookup"><span data-stu-id="33953-120">1</span></span></td>
<td><span data-ttu-id="33953-121">Active les fonctionnalités qui produiront la meilleure qualité visuelle. L’utilisation de cette valeur configure le codec comme si vous aviez défini les propriétés suivantes :</span><span class="sxs-lookup"><span data-stu-id="33953-121">Enables the features that will produce the best visual quality.Using this value configures the codec as if you had set the following properties:</span></span><br/>
<ul>
<li><span data-ttu-id="33953-122"><a href="mfpkey-bdeltaqpproperty.md">MFPKEY_BDELTAQP</a> = 1</span><span class="sxs-lookup"><span data-stu-id="33953-122"><a href="mfpkey-bdeltaqpproperty.md">MFPKEY_BDELTAQP</a> = 1</span></span></li>
<li><span data-ttu-id="33953-123"><a href="mfpkey-complexityexproperty.md">MFPKEY_COMPLEXITYEX</a> = 3</span><span class="sxs-lookup"><span data-stu-id="33953-123"><a href="mfpkey-complexityexproperty.md">MFPKEY_COMPLEXITYEX</a> = 3</span></span></li>
<li><span data-ttu-id="33953-124"><a href="mfpkey-loopfilterproperty.md">MFPKEY_LOOPFILTER</a> = 1</span><span class="sxs-lookup"><span data-stu-id="33953-124"><a href="mfpkey-loopfilterproperty.md">MFPKEY_LOOPFILTER</a> = 1</span></span></li>
<li><span data-ttu-id="33953-125"><a href="mfpkey-motionmatchmethodproperty.md">MFPKEY_MOTIONMATCHMETHOD</a> =-1</span><span class="sxs-lookup"><span data-stu-id="33953-125"><a href="mfpkey-motionmatchmethodproperty.md">MFPKEY_MOTIONMATCHMETHOD</a> = -1</span></span></li>
<li><span data-ttu-id="33953-126"><a href="mfpkey-motionsearchlevelproperty.md">MFPKEY_MOTIONSEARCHLEVEL</a> = 1</span><span class="sxs-lookup"><span data-stu-id="33953-126"><a href="mfpkey-motionsearchlevelproperty.md">MFPKEY_MOTIONSEARCHLEVEL</a> = 1</span></span></li>
<li><span data-ttu-id="33953-127"><a href="mfpkey-motionsearchrangeproperty.md">MFPKEY_MOTIONSEARCHRANGE</a> =-1</span><span class="sxs-lookup"><span data-stu-id="33953-127"><a href="mfpkey-motionsearchrangeproperty.md">MFPKEY_MOTIONSEARCHRANGE</a> = -1</span></span></li>
<li><span data-ttu-id="33953-128"><a href="mfpkey-numbframesproperty.md">MFPKEY_NUMBFRAMES</a> = 1</span><span class="sxs-lookup"><span data-stu-id="33953-128"><a href="mfpkey-numbframesproperty.md">MFPKEY_NUMBFRAMES</a> = 1</span></span></li>
</ul>
<span data-ttu-id="33953-129">Si vous définissez l’une des propriétés de la liste précédente, la valeur que vous définissez remplace les valeurs associées à ce paramètre, à l’exception de <a href="mfpkey-complexityexproperty.md">MFPKEY_COMPLEXITYEX</a>.</span><span class="sxs-lookup"><span data-stu-id="33953-129">If you set any of the properties in the previous list, the value you set overrides the values associated with this setting, except for <a href="mfpkey-complexityexproperty.md">MFPKEY_COMPLEXITYEX</a>.</span></span><br/></td>
</tr>
</tbody>
</table>



 

<span data-ttu-id="33953-130">Si vous affectez la valeur \_ 1 à la propriété MFPKEY COMPRESSIONOPTIMIZATIONTYPE, cela a également pour effet de définir le paramètre de Registre option DQuant sur 2 et le paramètre de Registre méthode de coût du vecteur de mouvement sur 1.</span><span class="sxs-lookup"><span data-stu-id="33953-130">Setting the value of the MFPKEY\_COMPRESSIONOPTIMIZATIONTYPE property to 1 also has the effect of setting the Dquant Option registry setting to 2, and the Motion Vector Cost Method registry setting to 1.</span></span> <span data-ttu-id="33953-131">Pour plus d’informations, consultez l’article Web [à l’aide des paramètres avancés du codec du profil avancé Windows Media Video 9](https://www.microsoft.com/windows/windowsmedia/howto/articles/codecadvancedsettings.aspx).</span><span class="sxs-lookup"><span data-stu-id="33953-131">For more information, see the web article [Using the Advanced Settings of the Windows Media Video 9 Advanced Profile Codec](https://www.microsoft.com/windows/windowsmedia/howto/articles/codecadvancedsettings.aspx).</span></span>

## <a name="requirements"></a><span data-ttu-id="33953-132">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="33953-132">Requirements</span></span>



| <span data-ttu-id="33953-133">Condition requise</span><span class="sxs-lookup"><span data-stu-id="33953-133">Requirement</span></span> | <span data-ttu-id="33953-134">Valeur</span><span class="sxs-lookup"><span data-stu-id="33953-134">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="33953-135">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="33953-135">Minimum supported client</span></span><br/> | <span data-ttu-id="33953-136">Applications de \[ Bureau Windows XP uniquement\]</span><span class="sxs-lookup"><span data-stu-id="33953-136">Windows XP \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="33953-137">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="33953-137">Minimum supported server</span></span><br/> | <span data-ttu-id="33953-138">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="33953-138">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="33953-139">En-tête</span><span class="sxs-lookup"><span data-stu-id="33953-139">Header</span></span><br/>                   | <dl> <span data-ttu-id="33953-140"><dt>Wmcodecdsp. h</dt></span><span class="sxs-lookup"><span data-stu-id="33953-140"><dt>Wmcodecdsp.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="33953-141">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="33953-141">See also</span></span>

<dl> <dt>

[<span data-ttu-id="33953-142">Propriétés de la Media Foundation</span><span class="sxs-lookup"><span data-stu-id="33953-142">Media Foundation Properties</span></span>](media-foundation-properties.md)
</dt> </dl>

 

 




