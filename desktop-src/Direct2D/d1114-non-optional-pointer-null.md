---
title: D1114 pointeur NULL non facultatif
ms.assetid: 62f0f247-8359-4f75-b3ce-195202d491d5
description: 'Le paramètre de l’interface :: Method n’est pas facultatif. Un pointeur NULL a été passé. Cela entraîne le blocage de Direct2D.'
keywords:
- D1114 pointeur facultatif non-valeur NULL
topic_type:
- apiref
api_name:
- D1114 Non Optional Pointer NULL
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.custom: seodec18
ms.openlocfilehash: abf8f070e339f2dcda5f818f5ffd5386c33d0e29
ms.sourcegitcommit: 80ee822f6ebcbcc8f60042e0d14a39ef6989c731
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/27/2021
ms.locfileid: "106521791"
---
# <a name="d1114-non-optional-pointer-null"></a><span data-ttu-id="beff0-106">D1114 : pointeur NULL non facultatif</span><span class="sxs-lookup"><span data-stu-id="beff0-106">D1114: Non Optional Pointer NULL</span></span>

<span data-ttu-id="beff0-107">Le \[ *paramètre* \] de paramètre pour *interface*::*Method* n’est pas facultatif.</span><span class="sxs-lookup"><span data-stu-id="beff0-107">The parameter \[*parameter*\] for *interface*::*method* is not optional.</span></span> <span data-ttu-id="beff0-108">Un pointeur **null** a été passé.</span><span class="sxs-lookup"><span data-stu-id="beff0-108">A **NULL** pointer was passed.</span></span> <span data-ttu-id="beff0-109">Cela entraîne le blocage de Direct2D.</span><span class="sxs-lookup"><span data-stu-id="beff0-109">This will cause Direct2D to crash.</span></span>

### <a name="placeholders"></a><span data-ttu-id="beff0-110">Espaces réservés</span><span class="sxs-lookup"><span data-stu-id="beff0-110">Placeholders</span></span>

<dl> <dt>

<span data-ttu-id="beff0-111"><span id="parameter"></span><span id="PARAMETER"></span>*paramètre*</span><span class="sxs-lookup"><span data-stu-id="beff0-111"><span id="parameter"></span><span id="PARAMETER"></span>*parameter*</span></span>
</dt> <dd>

<span data-ttu-id="beff0-112">Nom du paramètre qui contient le pointeur **null** .</span><span class="sxs-lookup"><span data-stu-id="beff0-112">The name of the parameter that contains the **NULL** pointer.</span></span>

</dd> <dt>

<span data-ttu-id="beff0-113"><span id="interface"></span><span id="INTERFACE"></span>*interface*</span><span class="sxs-lookup"><span data-stu-id="beff0-113"><span id="interface"></span><span id="INTERFACE"></span>*interface*</span></span>
</dt> <dd>

<span data-ttu-id="beff0-114">Nom de l’interface à laquelle la *méthode* appartient.</span><span class="sxs-lookup"><span data-stu-id="beff0-114">The name of the interface to which the *method* belongs.</span></span>

</dd> <dt>

<span data-ttu-id="beff0-115"><span id="method"></span><span id="METHOD"></span>*méthode*</span><span class="sxs-lookup"><span data-stu-id="beff0-115"><span id="method"></span><span id="METHOD"></span>*method*</span></span>
</dt> <dd>

<span data-ttu-id="beff0-116">Nom de la méthode qui a reçu le paramètre non valide.</span><span class="sxs-lookup"><span data-stu-id="beff0-116">The name of the method that received the invalid parameter.</span></span>

</dd> </dl> 




 

### <a name="examples"></a><span data-ttu-id="beff0-117">Exemples</span><span class="sxs-lookup"><span data-stu-id="beff0-117">Examples</span></span>

<span data-ttu-id="beff0-118">L’exemple suivant montre que la méthode [**FillGeometry**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-fillgeometry) reçoit un pointeur null pour le paramètre *Geometry* non facultatif.</span><span class="sxs-lookup"><span data-stu-id="beff0-118">The following example shows that the [**FillGeometry**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-fillgeometry) method receives a NULL pointer for the non-optional *geometry* parameter.</span></span>


```C++
        m_pRenderTarget->FillGeometry(NULL, m_pYellowGreenBrush);
```



<span data-ttu-id="beff0-119">Cet exemple génère le message de débogage suivant :</span><span class="sxs-lookup"><span data-stu-id="beff0-119">This example produces the following debug message:</span></span>

``` syntax
D2D DEBUG ERROR - The parameter [geometry] for ID2D1RenderTarget::FillGeometry is not optional. 
A NULL pointer was passed. This will cause Direct2D to crash.
```

## <a name="possible-causes"></a><span data-ttu-id="beff0-120">Causes possibles</span><span class="sxs-lookup"><span data-stu-id="beff0-120">Possible Causes</span></span>

<span data-ttu-id="beff0-121">Un pointeur NULL a été passé pour un paramètre non facultatif.</span><span class="sxs-lookup"><span data-stu-id="beff0-121">A NULL pointer was passed for a non-optional parameter.</span></span>

## <a name="fixes"></a><span data-ttu-id="beff0-122">Correctifs</span><span class="sxs-lookup"><span data-stu-id="beff0-122">Fixes</span></span>

<span data-ttu-id="beff0-123">Assurez-vous qu’un paramètre non facultatif n’a pas de pointeur NULL.</span><span class="sxs-lookup"><span data-stu-id="beff0-123">Ensure that a non-optional parameter does not have a NULL pointer.</span></span>

 

 
