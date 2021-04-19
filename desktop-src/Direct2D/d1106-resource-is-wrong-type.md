---
title: Le type de la ressource D1106 est incorrect
ms.assetid: 79a618cb-1d05-4895-b801-7663890b456a
description: La ressource donnée n’est pas d’un type attendu.
keywords:
- Le type de ressource D1106 est incorrect.
topic_type:
- apiref
api_name:
- D1106 Resource Is Wrong Type
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.custom: seodec18
ms.openlocfilehash: 5c38ef36319b8021de918a798c94a3be0683a7b7
ms.sourcegitcommit: 80ee822f6ebcbcc8f60042e0d14a39ef6989c731
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/27/2021
ms.locfileid: "106530057"
---
# <a name="d1106-resource-is-wrong-type"></a><span data-ttu-id="703ef-104">D1106 : type de ressource incorrect</span><span class="sxs-lookup"><span data-stu-id="703ef-104">D1106: Resource Is Wrong Type</span></span>

<span data-ttu-id="703ef-105">La \[ *ressource* \] de ressource donnée n’est pas d’un type attendu.</span><span class="sxs-lookup"><span data-stu-id="703ef-105">The given resource \[*resource*\] is not of an expected type.</span></span>

## <a name="placeholders"></a><span data-ttu-id="703ef-106">Espaces réservés</span><span class="sxs-lookup"><span data-stu-id="703ef-106">Placeholders</span></span>

<dl> <dt>

<span data-ttu-id="703ef-107"><span id="resource"></span><span id="RESOURCE"></span>*ressource*</span><span class="sxs-lookup"><span data-stu-id="703ef-107"><span id="resource"></span><span id="RESOURCE"></span>*resource*</span></span>
</dt> <dd>

<span data-ttu-id="703ef-108">Adresse de la ressource.</span><span class="sxs-lookup"><span data-stu-id="703ef-108">The address of the resource.</span></span>

</dd> </dl> 




 

## <a name="possible-causes"></a><span data-ttu-id="703ef-109">Causes possibles</span><span class="sxs-lookup"><span data-stu-id="703ef-109">Possible Causes</span></span>

<span data-ttu-id="703ef-110">Une interface a été incorrectement castée et utilisée comme paramètre pour une méthode ou une fonction.</span><span class="sxs-lookup"><span data-stu-id="703ef-110">An interface was improperly cast and used as a parameter for a method or function.</span></span>

## <a name="examples"></a><span data-ttu-id="703ef-111">Exemples</span><span class="sxs-lookup"><span data-stu-id="703ef-111">Examples</span></span>

<span data-ttu-id="703ef-112">L’exemple suivant passe un [**ID2D1SolidColorBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1solidcolorbrush) lorsqu’un [**ID2D1Geometry**](/windows/win32/api/d2d1/nn-d2d1-id2d1geometry) est attendu.</span><span class="sxs-lookup"><span data-stu-id="703ef-112">The following example passes an [**ID2D1SolidColorBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1solidcolorbrush) when an [**ID2D1Geometry**](/windows/win32/api/d2d1/nn-d2d1-id2d1geometry) is expected.</span></span>


```C++
        m_pRenderTarget->FillGeometry(
            (ID2D1Geometry*)m_pYellowGreenBrush,
            m_pYellowGreenBrush
            );
```



<span data-ttu-id="703ef-113">Cet exemple génère le message de débogage suivant :</span><span class="sxs-lookup"><span data-stu-id="703ef-113">This example produces the following debug message:</span></span>

``` syntax
DEBUG ERROR - The given resource[003A2C98] is not of an expected type
```

## <a name="fixes"></a><span data-ttu-id="703ef-114">Correctifs</span><span class="sxs-lookup"><span data-stu-id="703ef-114">Fixes</span></span>

<span data-ttu-id="703ef-115">Utilisez le type requis par la méthode.</span><span class="sxs-lookup"><span data-stu-id="703ef-115">Use the type required by the method.</span></span>

 

 
