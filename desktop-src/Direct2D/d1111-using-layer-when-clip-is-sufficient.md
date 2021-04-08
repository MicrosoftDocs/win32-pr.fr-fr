---
title: D1111 utilisation de la couche lorsque l’élément est suffisant
ms.assetid: 07fe3c66-15be-408b-a30b-a7f52919c058
description: Une couche est utilisée avec un masque d’opacité NULL, une opacité de 1,0 et un masque géométrique rectangulaire aligné sur un axe. L’API clip push/pop doit obtenir les mêmes résultats avec des performances supérieures.
keywords:
- D1111 utilisant une couche quand l’élément est suffisamment Direct2D
topic_type:
- apiref
api_name:
- D1111 Using Layer When Clip Is Sufficient
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.custom: seodec18
ms.openlocfilehash: a30bbfd7b8ca448928249018a28bc4d6a8a2f57f
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "103730069"
---
# <a name="d1111-using-layer-when-clip-is-sufficient"></a><span data-ttu-id="e2a70-105">D1111 : utilisation de la couche lorsque l’élément est suffisant</span><span class="sxs-lookup"><span data-stu-id="e2a70-105">D1111: Using Layer When Clip Is Sufficient</span></span>

<span data-ttu-id="e2a70-106">PERF : une couche est utilisée avec un masque d’opacité **null** , une opacité de 1,0 et un masque géométrique rectangulaire aligné sur un axe.</span><span class="sxs-lookup"><span data-stu-id="e2a70-106">PERF - A layer is being used with a **NULL** opacity mask, 1.0 opacity, and an axis aligned rectangular geometric mask.</span></span> <span data-ttu-id="e2a70-107">L’API clip push/pop doit obtenir les mêmes résultats avec des performances supérieures.</span><span class="sxs-lookup"><span data-stu-id="e2a70-107">The Push/Pop Clip API should achieve the same results with higher performance.</span></span>

## <a name="placeholders"></a><span data-ttu-id="e2a70-108">Espaces réservés</span><span class="sxs-lookup"><span data-stu-id="e2a70-108">Placeholders</span></span>

<dl> <dt>

<span data-ttu-id="e2a70-109"><span id="interface"></span><span id="INTERFACE"></span>*interface*</span><span class="sxs-lookup"><span data-stu-id="e2a70-109"><span id="interface"></span><span id="INTERFACE"></span>*interface*</span></span>
</dt> <dd>

<span data-ttu-id="e2a70-110">Adresse de l’interface.</span><span class="sxs-lookup"><span data-stu-id="e2a70-110">The address of the interface.</span></span>

</dd> </dl> 

|             |             |
|-------------|-------------|
| <span data-ttu-id="e2a70-111">Niveau d’erreur</span><span class="sxs-lookup"><span data-stu-id="e2a70-111">Error Level</span></span> | <span data-ttu-id="e2a70-112">Information</span><span class="sxs-lookup"><span data-stu-id="e2a70-112">Information</span></span> |



 

## <a name="examples"></a><span data-ttu-id="e2a70-113">Exemples</span><span class="sxs-lookup"><span data-stu-id="e2a70-113">Examples</span></span>

<span data-ttu-id="e2a70-114">Le code suivant utilise [**PushLayer**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-pushlayer(constd2d1_layer_parameters__id2d1layer)) et [**PopLayer**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-poplayer) lorsque la couche contient uniquement une primitive (un rectangle) et que les champs de la structure des [**\_ \_ paramètres de couche d2d1**](/windows/desktop/api/d2d1/ns-d2d1-d2d1_layer_parameters) sont définis sur les valeurs par défaut.</span><span class="sxs-lookup"><span data-stu-id="e2a70-114">The following code uses the [**PushLayer**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-pushlayer(constd2d1_layer_parameters__id2d1layer)) and [**PopLayer**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-poplayer) when the layer contains only one primitive (a rectangle) and the fields of the [**D2D1\_LAYER\_PARAMETERS**](/windows/desktop/api/d2d1/ns-d2d1-d2d1_layer_parameters) structure are set to defaults.</span></span> <span data-ttu-id="e2a70-115">Pour connaître les valeurs par défaut de la structure des **\_ \_ paramètres de couche d2d1** , consultez [**LayerParameter**](/windows/desktop/api/d2d1helper/nf-d2d1helper-layerparameters).</span><span class="sxs-lookup"><span data-stu-id="e2a70-115">For the default values of the **D2D1\_LAYER\_PARAMETERS** structure, see [**LayerParameter**](/windows/desktop/api/d2d1helper/nf-d2d1helper-layerparameters).</span></span>


```C++
        ID2D1Layer *m_pLayer;

        hr = m_pRenderTarget->CreateLayer(D2D1::SizeF(100, 100), &m_pLayer);
        m_pRenderTarget->PushLayer(D2D1::LayerParameters(), m_pLayer);
        m_pRenderTarget->FillRectangle(D2D1::RectF(100, 50, 400, 160), m_pBlackBrush);
        m_pRenderTarget->PopLayer();
```



<span data-ttu-id="e2a70-116">Cet exemple génère le message de débogage suivant :</span><span class="sxs-lookup"><span data-stu-id="e2a70-116">This example produces the following debug message:</span></span>

``` syntax
DEBUG INFO - PERF - A layer is being used with a NULL opacity mask, 1.0 opacity, 
            and an axis aligned rectangular geometric mask.  
            The Push/Pop Clip API should achieve the same results with higher performance.
```

## <a name="possible-causes"></a><span data-ttu-id="e2a70-117">Causes possibles</span><span class="sxs-lookup"><span data-stu-id="e2a70-117">Possible Causes</span></span>

<span data-ttu-id="e2a70-118">Une couche a été utilisée lorsque les méthodes [**PushAxisAlignedClip**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-pushaxisalignedclip(constd2d1_rect_f__d2d1_antialias_mode)) et [**PopAxisAlignedClip**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-popaxisalignedclip) seraient suffisantes.</span><span class="sxs-lookup"><span data-stu-id="e2a70-118">A layer was used when the [**PushAxisAlignedClip**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-pushaxisalignedclip(constd2d1_rect_f__d2d1_antialias_mode)) and [**PopAxisAlignedClip**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-popaxisalignedclip) methods would have sufficed.</span></span>

 

 