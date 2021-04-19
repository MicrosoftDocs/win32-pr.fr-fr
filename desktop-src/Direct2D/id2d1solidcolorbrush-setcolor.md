---
title: Méthodes ID2D1SolidColorBrush SetColor
description: Spécifie la couleur de ce pinceau de couleur unie.
ms.assetid: 2900bf72-9641-419c-b0d7-334f14f8a474
keywords:
- Méthodes SetColor Direct2D
topic_type:
- apiref
api_location:
- D2d1.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
api_name: ''
ms.openlocfilehash: 580778135e840a69342ff34ffd8e415883317517
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106541671"
---
# <a name="id2d1solidcolorbrushsetcolor-methods"></a><span data-ttu-id="58ff9-104">ID2D1SolidColorBrush :: SetColor, méthodes</span><span class="sxs-lookup"><span data-stu-id="58ff9-104">ID2D1SolidColorBrush::SetColor methods</span></span>

<span data-ttu-id="58ff9-105">Spécifie la couleur de ce pinceau de couleur unie.</span><span class="sxs-lookup"><span data-stu-id="58ff9-105">Specifies the color of this solid color brush.</span></span>

### <a name="overload-list"></a><span data-ttu-id="58ff9-106">Liste de surcharge</span><span class="sxs-lookup"><span data-stu-id="58ff9-106">Overload list</span></span>



| <span data-ttu-id="58ff9-107">Méthode</span><span class="sxs-lookup"><span data-stu-id="58ff9-107">Method</span></span>                                                                          | <span data-ttu-id="58ff9-108">Description</span><span class="sxs-lookup"><span data-stu-id="58ff9-108">Description</span></span>                                                |
|:--------------------------------------------------------------------------------|:-----------------------------------------------------------|
| <span data-ttu-id="58ff9-109">[**SetColor (D2D1 de \_ couleur \_ F&)**](/windows/win32/api/d2d1/nf-d2d1-id2d1solidcolorbrush-setcolor(constd2d1_color_f_))</span><span class="sxs-lookup"><span data-stu-id="58ff9-109">[**SetColor(D2D1\_COLOR\_F&)**](/windows/win32/api/d2d1/nf-d2d1-id2d1solidcolorbrush-setcolor(constd2d1_color_f_))</span></span>  | <span data-ttu-id="58ff9-110">Spécifie la couleur de ce pinceau de couleur unie.</span><span class="sxs-lookup"><span data-stu-id="58ff9-110">Specifies the color of this solid-color brush.</span></span> <br/> |
| <span data-ttu-id="58ff9-111">[**SetColor ( \_ couleur d2d1 \_ F \* )**](/windows/win32/api/d2d1/nf-d2d1-id2d1solidcolorbrush-setcolor(constd2d1_color_f))</span><span class="sxs-lookup"><span data-stu-id="58ff9-111">[**SetColor(D2D1\_COLOR\_F\*)**](/windows/win32/api/d2d1/nf-d2d1-id2d1solidcolorbrush-setcolor(constd2d1_color_f))</span></span> | <span data-ttu-id="58ff9-112">Spécifie la couleur de ce pinceau de couleur unie.</span><span class="sxs-lookup"><span data-stu-id="58ff9-112">Specifies the color of this solid color brush.</span></span> <br/> |



## <a name="remarks"></a><span data-ttu-id="58ff9-113">Notes</span><span class="sxs-lookup"><span data-stu-id="58ff9-113">Remarks</span></span>

<span data-ttu-id="58ff9-114">Pour vous aider à créer des couleurs, Direct2D fournit la classe [**ColorF**](/windows/win32/api/d2d1helper/nl-d2d1helper-colorf) .</span><span class="sxs-lookup"><span data-stu-id="58ff9-114">To help create colors, Direct2D provides the [**ColorF**](/windows/win32/api/d2d1helper/nl-d2d1helper-colorf) class.</span></span> <span data-ttu-id="58ff9-115">Il offre plusieurs méthodes d’assistance pour la création de couleurs et fournit un jeu ou des couleurs prédéfinies.</span><span class="sxs-lookup"><span data-stu-id="58ff9-115">It offers several helper methods for creating colors and provides a set or predefined colors.</span></span>

## <a name="examples"></a><span data-ttu-id="58ff9-116">Exemples</span><span class="sxs-lookup"><span data-stu-id="58ff9-116">Examples</span></span>

<span data-ttu-id="58ff9-117">Le code suivant montre comment utiliser cette méthode.</span><span class="sxs-lookup"><span data-stu-id="58ff9-117">The following code shows how to use this method.</span></span>


```C++
        m_pSolidColorBrush->SetColor(
            D2D1::ColorF(
                0.0f,
                intensity,
                1.0f - intensity
                ));

        hr = m_pRealization->Fill(
                m_pRT,
                m_pSolidColorBrush,
                m_useRealizations ?
                    REALIZATION_RENDER_MODE_DEFAULT :
                    REALIZATION_RENDER_MODE_FORCE_UNREALIZED
                );
```



## <a name="requirements"></a><span data-ttu-id="58ff9-118">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="58ff9-118">Requirements</span></span>



| <span data-ttu-id="58ff9-119">Condition requise</span><span class="sxs-lookup"><span data-stu-id="58ff9-119">Requirement</span></span> | <span data-ttu-id="58ff9-120">Valeur</span><span class="sxs-lookup"><span data-stu-id="58ff9-120">Value</span></span> |
|--------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="58ff9-121">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="58ff9-121">Library</span></span><br/> | <dl> <span data-ttu-id="58ff9-122"><dt>D2d1. lib</dt></span><span class="sxs-lookup"><span data-stu-id="58ff9-122"><dt>D2d1.lib</dt></span></span> </dl> |
| <span data-ttu-id="58ff9-123">DLL</span><span class="sxs-lookup"><span data-stu-id="58ff9-123">DLL</span></span><br/>     | <dl> <span data-ttu-id="58ff9-124"><dt>D2d1.dll</dt></span><span class="sxs-lookup"><span data-stu-id="58ff9-124"><dt>D2d1.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="58ff9-125">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="58ff9-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="58ff9-126">**ID2D1SolidColorBrush**</span><span class="sxs-lookup"><span data-stu-id="58ff9-126">**ID2D1SolidColorBrush**</span></span>](/windows/win32/api/d2d1/nn-d2d1-id2d1solidcolorbrush)
</dt> </dl>

 

