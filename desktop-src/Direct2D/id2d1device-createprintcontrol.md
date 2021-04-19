---
title: Méthodes ID2D1Device CreatePrintControl (D2d1 \_ 1. h)
description: Crée un objet ID2D1PrintControl qui convertit les primitives Direct2D stockées dans ID2D1CommandList en une représentation de page fixe. Le sous-système d’impression consomme alors les primitives.
ms.assetid: C8860AEE-807A-435E-9F44-B50545320EDA
keywords:
- Méthodes CreatePrintControl Direct2D
topic_type:
- apiref
api_location:
- d2d1_1.h
api_type:
- HeaderDef
ms.date: 07/02/2019
ms.topic: reference
ms.openlocfilehash: ec8705d73f40fc967b3247aaf81caebcade47b02
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106543162"
---
# <a name="id2d1devicecreateprintcontrol-methods"></a><span data-ttu-id="2d58e-105">ID2D1Device :: CreatePrintControl, méthodes</span><span class="sxs-lookup"><span data-stu-id="2d58e-105">ID2D1Device::CreatePrintControl methods</span></span>

<span data-ttu-id="2d58e-106">Crée un objet [**ID2D1PrintControl**](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1printcontrol) qui convertit les primitives [Direct2D](/windows/desktop/direct2d/direct2d-portal) stockées dans [**ID2D1CommandList**](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1commandlist) en une représentation de page fixe.</span><span class="sxs-lookup"><span data-stu-id="2d58e-106">Creates an [**ID2D1PrintControl**](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1printcontrol) object that converts [Direct2D](/windows/desktop/direct2d/direct2d-portal) primitives stored in [**ID2D1CommandList**](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1commandlist) into a fixed page representation.</span></span> <span data-ttu-id="2d58e-107">Le sous-système d’impression consomme alors les primitives.</span><span class="sxs-lookup"><span data-stu-id="2d58e-107">The print sub-system then consumes the primitives.</span></span>

### <a name="overload-list"></a><span data-ttu-id="2d58e-108">Liste de surcharge</span><span class="sxs-lookup"><span data-stu-id="2d58e-108">Overload list</span></span>



| <span data-ttu-id="2d58e-109">Méthode</span><span class="sxs-lookup"><span data-stu-id="2d58e-109">Method</span></span>                                                                                                                                                                           | <span data-ttu-id="2d58e-110">Description</span><span class="sxs-lookup"><span data-stu-id="2d58e-110">Description</span></span>                                                                                                                                                                                                                                                                               |
|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2d58e-111">[**CreatePrintControl (IWICImagingFactory \* , IPrintDocumentPackageTarget \* , d2d1, \_ Propriétés du contrôle d’impression \_ \_ \* , ID2D1PrintControl \* \* )**](/windows/win32/api/d2d1_1/nf-d2d1_1-id2d1device-createprintcontrol(iwicimagingfactory_iprintdocumentpackagetarget_constd2d1_print_control_properties_id2d1printcontrol))</span><span class="sxs-lookup"><span data-stu-id="2d58e-111">[**CreatePrintControl (IWICImagingFactory\*, IPrintDocumentPackageTarget\*, D2D1\_PRINT\_CONTROL\_PROPERTIES\*, ID2D1PrintControl\*\*)**](/windows/win32/api/d2d1_1/nf-d2d1_1-id2d1device-createprintcontrol(iwicimagingfactory_iprintdocumentpackagetarget_constd2d1_print_control_properties_id2d1printcontrol))</span></span> | <span data-ttu-id="2d58e-112">Crée un objet [**ID2D1PrintControl**](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1printcontrol) qui convertit les primitives [Direct2D](/windows/desktop/direct2d/direct2d-portal) stockées dans [**ID2D1CommandList**](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1commandlist) en une représentation de page fixe.</span><span class="sxs-lookup"><span data-stu-id="2d58e-112">Creates an [**ID2D1PrintControl**](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1printcontrol) object that converts [Direct2D](/windows/desktop/direct2d/direct2d-portal) primitives stored in [**ID2D1CommandList**](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1commandlist) into a fixed page representation.</span></span> <span data-ttu-id="2d58e-113">Le sous-système d’impression consomme alors les primitives.</span><span class="sxs-lookup"><span data-stu-id="2d58e-113">The print sub-system then consumes the primitives.</span></span><br/> |
| <span data-ttu-id="2d58e-114">[**CreatePrintControl (IWICImagingFactory \* , IPrintDocumentPackageTarget \* , d2d1 \_ Propriétés du contrôle d’impression \_ \_&, ID2D1PrintControl \* \* )**](/windows/win32/api/d2d1_1/nf-d2d1_1-id2d1device-createprintcontrol(iwicimagingfactory_iprintdocumentpackagetarget_constd2d1_print_control_properties__id2d1printcontrol))</span><span class="sxs-lookup"><span data-stu-id="2d58e-114">[**CreatePrintControl (IWICImagingFactory\*, IPrintDocumentPackageTarget\*, D2D1\_PRINT\_CONTROL\_PROPERTIES&, ID2D1PrintControl\*\*)**](/windows/win32/api/d2d1_1/nf-d2d1_1-id2d1device-createprintcontrol(iwicimagingfactory_iprintdocumentpackagetarget_constd2d1_print_control_properties__id2d1printcontrol))</span></span>    | <span data-ttu-id="2d58e-115">Crée un objet [**ID2D1PrintControl**](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1printcontrol) qui convertit les primitives [Direct2D](/windows/desktop/direct2d/direct2d-portal) stockées dans [**ID2D1CommandList**](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1commandlist) en une représentation de page fixe.</span><span class="sxs-lookup"><span data-stu-id="2d58e-115">Creates an [**ID2D1PrintControl**](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1printcontrol) object that converts [Direct2D](/windows/desktop/direct2d/direct2d-portal) primitives stored in [**ID2D1CommandList**](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1commandlist) into a fixed page representation.</span></span> <span data-ttu-id="2d58e-116">Le sous-système d’impression consomme alors les primitives.</span><span class="sxs-lookup"><span data-stu-id="2d58e-116">The print sub-system then consumes the primitives.</span></span><br/> |



## <a name="requirements"></a><span data-ttu-id="2d58e-117">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="2d58e-117">Requirements</span></span>



| <span data-ttu-id="2d58e-118">Condition requise</span><span class="sxs-lookup"><span data-stu-id="2d58e-118">Requirement</span></span> | <span data-ttu-id="2d58e-119">Valeur</span><span class="sxs-lookup"><span data-stu-id="2d58e-119">Value</span></span> |
|-------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="2d58e-120">En-tête</span><span class="sxs-lookup"><span data-stu-id="2d58e-120">Header</span></span><br/> | <dl> <span data-ttu-id="2d58e-121"><dt>D2d1 \_ 1. h</dt></span><span class="sxs-lookup"><span data-stu-id="2d58e-121"><dt>D2d1\_1.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2d58e-122">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="2d58e-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2d58e-123">**ID2D1Device**</span><span class="sxs-lookup"><span data-stu-id="2d58e-123">**ID2D1Device**</span></span>](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1device)
</dt> </dl>

<span data-ttu-id="2d58e-124">�</span><span class="sxs-lookup"><span data-stu-id="2d58e-124">�</span></span>

<span data-ttu-id="2d58e-125">�</span><span class="sxs-lookup"><span data-stu-id="2d58e-125">�</span></span>
