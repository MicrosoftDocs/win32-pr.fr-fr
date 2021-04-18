---
title: Méthodes ID2D1Geometry ComputeLength
description: Calcule la longueur de la géométrie comme si chaque segment était déroulé dans une ligne.
ms.assetid: 4659d880-0aa3-485d-ac71-044d9ace6759
keywords:
- Méthodes ComputeLength Direct2D
topic_type:
- apiref
api_location:
- D2d1.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
api_name: ''
ms.openlocfilehash: b49b1beb0525d95967ad903b0f0fb3c464edf4d7
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106543363"
---
# <a name="id2d1geometrycomputelength-methods"></a><span data-ttu-id="f1f96-104">ID2D1Geometry :: ComputeLength, méthodes</span><span class="sxs-lookup"><span data-stu-id="f1f96-104">ID2D1Geometry::ComputeLength methods</span></span>

<span data-ttu-id="f1f96-105">Calcule la longueur de la géométrie comme si chaque segment était déroulé dans une ligne.</span><span class="sxs-lookup"><span data-stu-id="f1f96-105">Calculates the length of the geometry as though each segment were unrolled into a line.</span></span>

### <a name="overload-list"></a><span data-ttu-id="f1f96-106">Liste de surcharge</span><span class="sxs-lookup"><span data-stu-id="f1f96-106">Overload list</span></span>



| <span data-ttu-id="f1f96-107">Méthode</span><span class="sxs-lookup"><span data-stu-id="f1f96-107">Method</span></span>                                                                                                                          | <span data-ttu-id="f1f96-108">Description</span><span class="sxs-lookup"><span data-stu-id="f1f96-108">Description</span></span>                                                                                         |
|:--------------------------------------------------------------------------------------------------------------------------------|:----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f1f96-109">[**ComputeLength (D2D1 \_ Matrix \_ matrice \_ F&, float \* )**](/windows/win32/api/d2d1/nf-d2d1-id2d1geometry-computelength(constd2d1_matrix_3x2_f_float))</span><span class="sxs-lookup"><span data-stu-id="f1f96-109">[**ComputeLength(D2D1\_MATRIX\_3X2\_F&,FLOAT\*)**](/windows/win32/api/d2d1/nf-d2d1-id2d1geometry-computelength(constd2d1_matrix_3x2_f_float))</span></span>              | <span data-ttu-id="f1f96-110">Calcule la longueur de la géométrie comme si chaque segment était déroulé dans une ligne.</span><span class="sxs-lookup"><span data-stu-id="f1f96-110">Calculates the length of the geometry as though each segment were unrolled into a line.</span></span><br/>  |
| <span data-ttu-id="f1f96-111">[**ComputeLength (D2D1 \_ Matrix \_ matrice \_ F \* , float \* )**](/windows/win32/api/d2d1/nf-d2d1-id2d1geometry-computelength(constd2d1_matrix_3x2_f_float))</span><span class="sxs-lookup"><span data-stu-id="f1f96-111">[**ComputeLength(D2D1\_MATRIX\_3X2\_F\*,FLOAT\*)**](/windows/win32/api/d2d1/nf-d2d1-id2d1geometry-computelength(constd2d1_matrix_3x2_f_float))</span></span>             | <span data-ttu-id="f1f96-112">Calcule la longueur de la géométrie comme si chaque segment était déroulé dans une ligne.</span><span class="sxs-lookup"><span data-stu-id="f1f96-112">Calculates the length of the geometry as though each segment were unrolled into a line.</span></span><br/>  |
| <span data-ttu-id="f1f96-113">[**ComputeLength (D2D1 \_ Matrix \_ matrice \_ F&, float, float \* )**](/windows/win32/api/d2d1/nf-d2d1-id2d1geometry-computelength(constd2d1_matrix_3x2_f__float_float))</span><span class="sxs-lookup"><span data-stu-id="f1f96-113">[**ComputeLength(D2D1\_MATRIX\_3X2\_F&,FLOAT,FLOAT\*)**](/windows/win32/api/d2d1/nf-d2d1-id2d1geometry-computelength(constd2d1_matrix_3x2_f__float_float))</span></span>  | <span data-ttu-id="f1f96-114">Calcule la longueur de la géométrie comme si chaque segment était déroulé dans une ligne.</span><span class="sxs-lookup"><span data-stu-id="f1f96-114">Calculates the length of the geometry as though each segment were unrolled into a line.</span></span><br/>  |
| <span data-ttu-id="f1f96-115">[**ComputeLength (D2D1 \_ Matrix \_ matrice \_ F \* , float, float \* )**](/windows/win32/api/d2d1/nf-d2d1-id2d1geometry-computelength(constd2d1_matrix_3x2_f_float))</span><span class="sxs-lookup"><span data-stu-id="f1f96-115">[**ComputeLength(D2D1\_MATRIX\_3X2\_F\*,FLOAT,FLOAT\*)**](/windows/win32/api/d2d1/nf-d2d1-id2d1geometry-computelength(constd2d1_matrix_3x2_f_float))</span></span> | <span data-ttu-id="f1f96-116">Calcule la longueur de la géométrie comme si chaque segment était déroulé dans une ligne.</span><span class="sxs-lookup"><span data-stu-id="f1f96-116">Calculates the length of the geometry as though each segment were unrolled into a line.</span></span> <br/> |



## <a name="examples"></a><span data-ttu-id="f1f96-117">Exemples</span><span class="sxs-lookup"><span data-stu-id="f1f96-117">Examples</span></span>

<span data-ttu-id="f1f96-118">Le code suivant montre comment utiliser **ComputeLength** pour calculer la longueur d’une géométrie de tracé spécifiée.</span><span class="sxs-lookup"><span data-stu-id="f1f96-118">The following code shows how to use **ComputeLength** to compute the length of a specified path geometry.</span></span>


```C++
float length = 0;
hr = m_pPathGeometry->ComputeLength(
    NULL, //no transform
    &length
    );

if (SUCCEEDED(hr))
{
    m_Animation.SetStart(0);        //start at beginning of path
    m_Animation.SetEnd(length);     //length at end of path
    m_Animation.SetDuration(5.0f);  //seconds

    ZeroMemory(&m_DwmTimingInfo, sizeof(m_DwmTimingInfo));
    m_DwmTimingInfo.cbSize = sizeof(m_DwmTimingInfo);

    // Get the composition refresh rate. If the DWM isn't running,
    // get the refresh rate from GDI -- probably going to be 60Hz
    if (FAILED(DwmGetCompositionTimingInfo(NULL, &m_DwmTimingInfo)))
    {
        HDC hdc = GetDC(m_hwnd);
        m_DwmTimingInfo.rateCompose.uiDenominator = 1;
        m_DwmTimingInfo.rateCompose.uiNumerator = GetDeviceCaps(hdc, VREFRESH);
        ReleaseDC(m_hwnd, hdc);
    }

    ShowWindow(m_hwnd, SW_SHOWNORMAL);

    UpdateWindow(m_hwnd);
}
```



## <a name="requirements"></a><span data-ttu-id="f1f96-119">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="f1f96-119">Requirements</span></span>



| <span data-ttu-id="f1f96-120">Condition requise</span><span class="sxs-lookup"><span data-stu-id="f1f96-120">Requirement</span></span> | <span data-ttu-id="f1f96-121">Valeur</span><span class="sxs-lookup"><span data-stu-id="f1f96-121">Value</span></span> |
|--------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="f1f96-122">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="f1f96-122">Library</span></span><br/> | <dl> <span data-ttu-id="f1f96-123"><dt>D2d1. lib</dt></span><span class="sxs-lookup"><span data-stu-id="f1f96-123"><dt>D2d1.lib</dt></span></span> </dl> |
| <span data-ttu-id="f1f96-124">DLL</span><span class="sxs-lookup"><span data-stu-id="f1f96-124">DLL</span></span><br/>     | <dl> <span data-ttu-id="f1f96-125"><dt>D2d1.dll</dt></span><span class="sxs-lookup"><span data-stu-id="f1f96-125"><dt>D2d1.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f1f96-126">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="f1f96-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f1f96-127">**ID2D1Geometry**</span><span class="sxs-lookup"><span data-stu-id="f1f96-127">**ID2D1Geometry**</span></span>](/windows/win32/api/d2d1/nn-d2d1-id2d1geometry)
</dt> </dl>

 

