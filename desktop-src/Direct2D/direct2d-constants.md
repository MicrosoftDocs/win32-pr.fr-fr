---
title: Constantes Direct2D
description: Direct2D définit la liste suivante de constantes.
ms.assetid: 98a443af-4bb7-486d-bc87-ff34c3671bdd
topic_type:
- apiref
api_name:
- D2D1_APPEND_ALIGNED_ELEMENT
- D2D1_DEFAULT_FLATTENING_TOLERANCE
- D2D1_INVALID_PROPERTY_INDEX
- D2D1_INVALID_TAG
- D2D1_SCENE_REFERRED_SDR_WHITE_LEVEL
api_location:
- d2d1.h
- d2d1effects_2.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 09/19/2019
ms.openlocfilehash: bc25bf1055b923a383fc580a622e96d787ed13e6
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "106511381"
---
# <a name="direct2d-constants"></a><span data-ttu-id="3c298-103">Constantes Direct2D</span><span class="sxs-lookup"><span data-stu-id="3c298-103">Direct2D constants</span></span>

<span data-ttu-id="3c298-104">Les constantes suivantes sont déclarées dans `d2d1effectauthor.h` les `d2d1.h` `d2d1_1.h` fichiers d' `d2d1effects_2.h` en-tête,, et.</span><span class="sxs-lookup"><span data-stu-id="3c298-104">The following constants are declared in the `d2d1effectauthor.h`, `d2d1.h`, `d2d1_1.h`, and `d2d1effects_2.h` header files.</span></span>

## <a name="d2d1_append_aligned_element--1"></a><span data-ttu-id="3c298-105">D2D1_APPEND_ALIGNED_ELEMENT (-1)</span><span class="sxs-lookup"><span data-stu-id="3c298-105">D2D1_APPEND_ALIGNED_ELEMENT (-1)</span></span>
<span data-ttu-id="3c298-106">Utilisé lors de la compression d’éléments de disposition d’entrée.</span><span class="sxs-lookup"><span data-stu-id="3c298-106">Used when packing input layout elements.</span></span> <span data-ttu-id="3c298-107">Elle indique que les éléments doivent être empaquetés de façon contiguë.</span><span class="sxs-lookup"><span data-stu-id="3c298-107">It indicates that the elements must be packed contiguously.</span></span>

## <a name="d2d1_default_flattening_tolerance-025f"></a><span data-ttu-id="3c298-108">D2D1_DEFAULT_FLATTENING_TOLERANCE (0,25 f)</span><span class="sxs-lookup"><span data-stu-id="3c298-108">D2D1_DEFAULT_FLATTENING_TOLERANCE (0.25f)</span></span>
<span data-ttu-id="3c298-109">Tolérance par défaut pour les opérations de mise à plat géométrique.</span><span class="sxs-lookup"><span data-stu-id="3c298-109">The default tolerance for geometric flattening operations.</span></span>

## <a name="d2d1_invalid_property_index-uint_max"></a><span data-ttu-id="3c298-110">D2D1_INVALID_PROPERTY_INDEX (UINT_MAX)</span><span class="sxs-lookup"><span data-stu-id="3c298-110">D2D1_INVALID_PROPERTY_INDEX (UINT_MAX)</span></span>
<span data-ttu-id="3c298-111">Définit un index de propriété non valide.</span><span class="sxs-lookup"><span data-stu-id="3c298-111">Defines an invalid property index.</span></span>

<span data-ttu-id="3c298-112">Cette constante est retournée à partir de [**ID2D1Properties :: GetPropertyIndex**](/windows/win32/api/d2d1_1/nf-d2d1_1-id2d1properties-getpropertyindex) pour indiquer que la propriété nommée que vous avez fournie n’a pas d’index dans l’interface de propriété.</span><span class="sxs-lookup"><span data-stu-id="3c298-112">This constant is returned from [**ID2D1Properties::GetPropertyIndex**](/windows/win32/api/d2d1_1/nf-d2d1_1-id2d1properties-getpropertyindex) to indicate that the named property that you provided doesn't have an index in the property interface.</span></span>

<span data-ttu-id="3c298-113">Si vous transmettez cette constante à [**ID2D1Properties :: GetValue**](/windows/win32/api/d2d1_1/nf-d2d1_1-id2d1properties-getvalue(uint32_byte_uint32)) ou [**ID2D1Properties :: GetValueByName**](/windows/win32/api/d2d1_1/nf-d2d1_1-id2d1properties-getvaluebyname(pcwstr_byte_uint32)), l’appel échoue et la mémoire tampon de sortie est remplie de zéros.</span><span class="sxs-lookup"><span data-stu-id="3c298-113">If you pass this constant to [**ID2D1Properties::GetValue**](/windows/win32/api/d2d1_1/nf-d2d1_1-id2d1properties-getvalue(uint32_byte_uint32)) or [**ID2D1Properties::GetValueByName**](/windows/win32/api/d2d1_1/nf-d2d1_1-id2d1properties-getvaluebyname(pcwstr_byte_uint32)), then the call fails, and the output buffer is zero-filled.</span></span>

## <a name="d2d1_invalid_tag-ulonglong_max"></a><span data-ttu-id="3c298-114">D2D1_INVALID_TAG (ULONGLONG_MAX)</span><span class="sxs-lookup"><span data-stu-id="3c298-114">D2D1_INVALID_TAG (ULONGLONG_MAX)</span></span>
<span data-ttu-id="3c298-115">Réservé n’utilisez pas.</span><span class="sxs-lookup"><span data-stu-id="3c298-115">Reserved; don't use.</span></span>

## <a name="d2d1_scene_referred_sdr_white_level-800f"></a><span data-ttu-id="3c298-116">D2D1_SCENE_REFERRED_SDR_WHITE_LEVEL (80,0 f)</span><span class="sxs-lookup"><span data-stu-id="3c298-116">D2D1_SCENE_REFERRED_SDR_WHITE_LEVEL (80.0f)</span></span>
<span data-ttu-id="3c298-117">Nombre de nits utilisés par l’espace de couleurs sRVB ou ScRVB pour les valeurs de virgule flottante ou de virgule flottante de 1,0 f.</span><span class="sxs-lookup"><span data-stu-id="3c298-117">The number of nits that sRGB or scRGB color space uses for SDR white, or floating point values of 1.0f.</span></span> <span data-ttu-id="3c298-118">Cette valeur est constante uniquement lorsque l’espace colorimétrique utilise la luminance référencée par scène, ce qui est vrai pour le contenu HDR (High dynamique Range).</span><span class="sxs-lookup"><span data-stu-id="3c298-118">This value is constant only when the color space uses scene-referred luminance, which is true for high dynamic range (HDR) content.</span></span> <span data-ttu-id="3c298-119">Si l’espace colorimétrique utilise à la place la luminance référencée, le niveau de blanc SDR doit être interrogé à partir de l’affichage.</span><span class="sxs-lookup"><span data-stu-id="3c298-119">If the color space uses display-referred luminance instead, then the SDR white level should be queried from the display.</span></span>

## <a name="requirements"></a><span data-ttu-id="3c298-120">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="3c298-120">Requirements</span></span>

| <span data-ttu-id="3c298-121">Condition requise</span><span class="sxs-lookup"><span data-stu-id="3c298-121">Requirement</span></span> | <span data-ttu-id="3c298-122">Valeur</span><span class="sxs-lookup"><span data-stu-id="3c298-122">Value</span></span> |
|-|-|
| <span data-ttu-id="3c298-123">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="3c298-123">Minimum supported client</span></span> | <span data-ttu-id="3c298-124">Windows 7, Windows Vista avec SP2 et mise à jour de la plateforme pour les applications de bureau Windows Vista, applications \[ \| UWP\]</span><span class="sxs-lookup"><span data-stu-id="3c298-124">Windows 7, Windows Vista with SP2 and Platform Update for Windows Vista \[desktop apps \| UWP apps\]</span></span> |
| <span data-ttu-id="3c298-125">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="3c298-125">Minimum supported server</span></span> | <span data-ttu-id="3c298-126">Windows Server 2008 R2, Windows Server 2008 avec SP2 et mise à jour de la plateforme pour les applications de bureau Windows Server 2008 pour applications \[ \| UWP\]</span><span class="sxs-lookup"><span data-stu-id="3c298-126">Windows Server 2008 R2, Windows Server 2008 with SP2 and Platform Update for Windows Server 2008 \[desktop apps \| UWP apps\]</span></span> |
| <span data-ttu-id="3c298-127">Téléphone minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="3c298-127">Minimum supported phone</span></span> | <span data-ttu-id="3c298-128">Windows Phone 8,1 \[ Windows Phone silverlight 8,1 et les applications Windows Runtime \] , Windows Phone 8,1 \[ Windows Phone silverlight 8,1 et Windows Runtime apps\]</span><span class="sxs-lookup"><span data-stu-id="3c298-128">Windows Phone 8.1 \[Windows Phone Silverlight 8.1 and Windows Runtime apps\], Windows Phone 8.1 \[Windows Phone Silverlight 8.1 and Windows Runtime apps\]</span></span> |
| <span data-ttu-id="3c298-129">En-tête</span><span class="sxs-lookup"><span data-stu-id="3c298-129">Header</span></span> | <span data-ttu-id="3c298-130">d2d1effectauthor. h, d2d1. h, d2d1_1. h, d2d1effects_2. h</span><span class="sxs-lookup"><span data-stu-id="3c298-130">d2d1effectauthor.h, d2d1.h, d2d1_1.h, d2d1effects_2.h</span></span> |
