---
title: Valeur d’énumération D1115 non valide
description: Valeur d’énumération D1115 non valide
ms.assetid: cfffd2b8-a7d3-4a60-8586-81d8435936a6
keywords:
- Valeur d’énumération D1115 non valide Direct2D
topic_type:
- apiref
api_name:
- D1115 Enumeration Value Not Valid
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: edcfe70c67e61a3b8bfc435adfdaa017a1c62b22
ms.sourcegitcommit: 80ee822f6ebcbcc8f60042e0d14a39ef6989c731
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/27/2021
ms.locfileid: "106533525"
---
# <a name="d1115-enumeration-value-not-valid"></a><span data-ttu-id="c9afc-104">D1115 : valeur d’énumération non valide</span><span class="sxs-lookup"><span data-stu-id="c9afc-104">D1115: Enumeration Value Not Valid</span></span>

<span data-ttu-id="c9afc-105">Le paramètre de paramètre avec la valeur \[  \] \[  \] de valeur pour *interface*::*Method* n’est pas une valeur d’énumération valide.</span><span class="sxs-lookup"><span data-stu-id="c9afc-105">The parameter \[*parameter*\] with value \[*value*\] for *interface*::*method* is not a valid enumeration value.</span></span>

## <a name="placeholders"></a><span data-ttu-id="c9afc-106">Espaces réservés</span><span class="sxs-lookup"><span data-stu-id="c9afc-106">Placeholders</span></span>

<dl> <dt>

<span data-ttu-id="c9afc-107"><span id="parameter"></span><span id="PARAMETER"></span>*paramètre*</span><span class="sxs-lookup"><span data-stu-id="c9afc-107"><span id="parameter"></span><span id="PARAMETER"></span>*parameter*</span></span>
</dt> <dd>

<span data-ttu-id="c9afc-108">Nom du paramètre qui a reçu le type inattendu.</span><span class="sxs-lookup"><span data-stu-id="c9afc-108">The name of the parameter that received the unexpected type.</span></span>

</dd> <dt>

<span data-ttu-id="c9afc-109"><span id="value"></span><span id="VALUE"></span>*ajoutée*</span><span class="sxs-lookup"><span data-stu-id="c9afc-109"><span id="value"></span><span id="VALUE"></span>*value*</span></span>
</dt> <dd>

<span data-ttu-id="c9afc-110">Valeur d’énumération non valide.</span><span class="sxs-lookup"><span data-stu-id="c9afc-110">The invalid enumeration value.</span></span>

</dd> <dt>

<span data-ttu-id="c9afc-111"><span id="interface"></span><span id="INTERFACE"></span>*interface*</span><span class="sxs-lookup"><span data-stu-id="c9afc-111"><span id="interface"></span><span id="INTERFACE"></span>*interface*</span></span>
</dt> <dd>

<span data-ttu-id="c9afc-112">Nom de l’interface à laquelle la *méthode* appartient.</span><span class="sxs-lookup"><span data-stu-id="c9afc-112">The name of the interface to which the *method* belongs.</span></span>

</dd> <dt>

<span data-ttu-id="c9afc-113"><span id="method"></span><span id="METHOD"></span>*méthode*</span><span class="sxs-lookup"><span data-stu-id="c9afc-113"><span id="method"></span><span id="METHOD"></span>*method*</span></span>
</dt> <dd>

<span data-ttu-id="c9afc-114">Nom de la méthode qui a reçu la valeur d’énumération non valide.</span><span class="sxs-lookup"><span data-stu-id="c9afc-114">The name of the method that received the invalid enumeration value.</span></span>

</dd> </dl> 




 

## <a name="examples"></a><span data-ttu-id="c9afc-115">Exemples</span><span class="sxs-lookup"><span data-stu-id="c9afc-115">Examples</span></span>

<span data-ttu-id="c9afc-116">L’exemple suivant spécifie une valeur d’énumération de [**\_ \_ \_ type cible de rendu d2d1**](/windows/desktop/api/d2d1/ne-d2d1-d2d1_render_target_type) de 30, qui est en dehors de la plage attendue.</span><span class="sxs-lookup"><span data-stu-id="c9afc-116">The following example specifies a [**D2D1\_RENDER\_TARGET\_TYPE**](/windows/desktop/api/d2d1/ne-d2d1-d2d1_render_target_type) enumeration value of 30, which is outside the expected range.</span></span>


```C++
        hr = m_pD2DFactory->CreateHwndRenderTarget(
            D2D1::RenderTargetProperties((D2D1_RENDER_TARGET_TYPE)(30)),
            D2D1::HwndRenderTargetProperties(m_hwnd, size),
            &m_pRenderTarget
            );
```



<span data-ttu-id="c9afc-117">Cet exemple génère le message de débogage suivant :</span><span class="sxs-lookup"><span data-stu-id="c9afc-117">This example produces the following debug message:</span></span>

``` syntax
D2D DEBUG ERROR - The parameter [renderTargetProperties->type] with value [30] 
for ID2D1Factory::CreateHwndRenderTarget is not a valid enumeration value.
```

## <a name="possible-causes"></a><span data-ttu-id="c9afc-118">Causes possibles</span><span class="sxs-lookup"><span data-stu-id="c9afc-118">Possible Causes</span></span>

<span data-ttu-id="c9afc-119">Un paramètre A utilisé une valeur d’énumération non valide.</span><span class="sxs-lookup"><span data-stu-id="c9afc-119">A parameter used an invalid enumeration value.</span></span>

## <a name="fixes"></a><span data-ttu-id="c9afc-120">Correctifs</span><span class="sxs-lookup"><span data-stu-id="c9afc-120">Fixes</span></span>

<span data-ttu-id="c9afc-121">Utilisez une valeur d’énumération valide.</span><span class="sxs-lookup"><span data-stu-id="c9afc-121">Use a valid enumeration value.</span></span>

> [!Note]  
> <span data-ttu-id="c9afc-122">La couche de débogage vérifie actuellement uniquement les valeurs d’énumération individuelles ; elle ne vérifie pas si une combinaison au niveau du bit est valide.</span><span class="sxs-lookup"><span data-stu-id="c9afc-122">The debug layer currently checks only the individual enumeration values; it does not check whether a bitwise combination is valid.</span></span>

 

 

 
