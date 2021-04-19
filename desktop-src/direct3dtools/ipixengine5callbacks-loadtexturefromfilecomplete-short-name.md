---
description: Fonction de rappel utilisée pour notifier l’hôte quand une charge de texture est terminée.
MS-HAID: vspixengine.IPixEngine5Callbacks\_LoadTextureFromFileComplete\_UINT\_PixEngineTextureDescriptor\_UINT\_PixEngineTextureSliceIndex\_arr\_PixEngineTextureSliceDescriptor\_arr\_UINT\_int\_arr\_PixEngineHistogram\_ptr
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: 'IPixEngine5Callbacks :: LoadTextureFromFileComplete, méthode'
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ef7fb4c38b733a7e85a237260404b5b253e3eb88
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/06/2021
ms.locfileid: "106515751"
---
# <a name="span-idvspixengineipixengine5callbacks_loadtexturefromfilecomplete_uint_pixenginetexturedescriptor_uint_pixenginetexturesliceindex_arr_pixenginetextureslicedescriptor_arr_uint_int_arr_pixenginehistogram_ptrspanipixengine5callbacksloadtexturefromfilecomplete-method"></a><span data-ttu-id="b7464-103"><span id="vspixengine.ipixengine5callbacks_loadtexturefromfilecomplete_uint_pixenginetexturedescriptor_uint_pixenginetexturesliceindex_arr_pixenginetextureslicedescriptor_arr_uint_int_arr_pixenginehistogram_ptr"></span>IPixEngine5Callbacks :: LoadTextureFromFileComplete, méthode</span><span class="sxs-lookup"><span data-stu-id="b7464-103"><span id="vspixengine.ipixengine5callbacks_loadtexturefromfilecomplete_uint_pixenginetexturedescriptor_uint_pixenginetexturesliceindex_arr_pixenginetextureslicedescriptor_arr_uint_int_arr_pixenginehistogram_ptr"></span>IPixEngine5Callbacks::LoadTextureFromFileComplete method</span></span>

<span data-ttu-id="b7464-104">Fonction de rappel utilisée pour notifier l’hôte quand une charge de texture est terminée.</span><span class="sxs-lookup"><span data-stu-id="b7464-104">A callback function used to notify the host when a texture load has been completed.</span></span>

## <a name="syntax"></a><span data-ttu-id="b7464-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="b7464-105">Syntax</span></span>


```C++
HRESULT LoadTextureFromFileComplete(
   UINT                               textureId,
   PixEngineTextureDescriptor         textureDesc,
   UINT                               numSlices,
   PixEngineTextureSliceIndex []      count2_sliceIndicies,
   PixEngineTextureSliceDescriptor [] count2_sliceDescriptors,
   UINT                               numFormatOverrides,
   int []                             count5_formatOverrides,
   PixEngineHistogram*                histogram
);
```

## <a name="parameters"></a><span data-ttu-id="b7464-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="b7464-106">Parameters</span></span>

<span data-ttu-id="b7464-107">*textureId* </span><span class="sxs-lookup"><span data-stu-id="b7464-107">*textureId* </span></span>  
<span data-ttu-id="b7464-108">ID de la texture chargée.</span><span class="sxs-lookup"><span data-stu-id="b7464-108">The ID of the loaded texture.</span></span>

<span data-ttu-id="b7464-109">*textureDesc* </span><span class="sxs-lookup"><span data-stu-id="b7464-109">*textureDesc* </span></span>  
<span data-ttu-id="b7464-110">Descripteur de texture de la texture chargée.</span><span class="sxs-lookup"><span data-stu-id="b7464-110">The texture descriptor of the loaded texture.</span></span>

<span data-ttu-id="b7464-111">*numSlices* </span><span class="sxs-lookup"><span data-stu-id="b7464-111">*numSlices* </span></span>  
<span data-ttu-id="b7464-112">Nombre de secteurs de la texture.</span><span class="sxs-lookup"><span data-stu-id="b7464-112">The number of slices the texture has.</span></span>

<span data-ttu-id="b7464-113">*count2 \_ sliceIndicies* </span><span class="sxs-lookup"><span data-stu-id="b7464-113">*count2\_sliceIndicies* </span></span>  
<span data-ttu-id="b7464-114">Les indices de tranche associés à la texture.</span><span class="sxs-lookup"><span data-stu-id="b7464-114">Slice indicies associated with the texture.</span></span>

<span data-ttu-id="b7464-115">*count2 \_ sliceDescriptors* </span><span class="sxs-lookup"><span data-stu-id="b7464-115">*count2\_sliceDescriptors* </span></span>  
<span data-ttu-id="b7464-116">Descripteurs pour chaque tranche.</span><span class="sxs-lookup"><span data-stu-id="b7464-116">Descriptors for each slice.</span></span>

<span data-ttu-id="b7464-117">*numFormatOverrides* </span><span class="sxs-lookup"><span data-stu-id="b7464-117">*numFormatOverrides* </span></span>  
<span data-ttu-id="b7464-118">Nombre de remplacements de format.</span><span class="sxs-lookup"><span data-stu-id="b7464-118">The number of format overrides.</span></span>

<span data-ttu-id="b7464-119">*count5 \_ formatOverrides* </span><span class="sxs-lookup"><span data-stu-id="b7464-119">*count5\_formatOverrides* </span></span>  
<span data-ttu-id="b7464-120">Le format remplace.</span><span class="sxs-lookup"><span data-stu-id="b7464-120">The format overrides.</span></span>

<span data-ttu-id="b7464-121">*histogramme* </span><span class="sxs-lookup"><span data-stu-id="b7464-121">*histogram* </span></span>  
<span data-ttu-id="b7464-122">Adresse des données d’histogramme pour la texture chargée.</span><span class="sxs-lookup"><span data-stu-id="b7464-122">The address of histogram data for the loaded texture.</span></span>

## <a name="return-value"></a><span data-ttu-id="b7464-123">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="b7464-123">Return value</span></span>

<span data-ttu-id="b7464-124">Si cette méthode est réussie, elle retourne la valeur **\_ OK**.</span><span class="sxs-lookup"><span data-stu-id="b7464-124">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="b7464-125">Sinon, elle retourne un code d’erreur **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="b7464-125">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="b7464-126">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="b7464-126">Requirements</span></span>

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><tbody><tr class="odd"><td><p><span data-ttu-id="b7464-127">En-tête</span><span class="sxs-lookup"><span data-stu-id="b7464-127">Header</span></span></p></td><td><span data-ttu-id="b7464-128">Vspixengine. h</span><span class="sxs-lookup"><span data-stu-id="b7464-128">Vspixengine.h</span></span></td></tr></tbody></table>

## <a name="span-idsee_alsospansee-also"></a><span data-ttu-id="b7464-129"><span id="see_also"></span>Voir aussi</span><span class="sxs-lookup"><span data-stu-id="b7464-129"><span id="see_also"></span>See also</span></span>

[<span data-ttu-id="b7464-130">**IPixEngine5Callbacks**</span><span class="sxs-lookup"><span data-stu-id="b7464-130">**IPixEngine5Callbacks**</span></span>](/windows/desktop/direct3dtools/ipixengine5callbacks)

 

 
