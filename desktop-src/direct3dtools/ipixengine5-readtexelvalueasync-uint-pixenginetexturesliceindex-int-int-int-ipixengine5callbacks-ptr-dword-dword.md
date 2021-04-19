---
description: Lit une valeur Texel et retourne le résultat au asynchrnously hôte.
MS-HAID: vspixengine.IPixEngine5\_ReadTexelValueAsync\_UINT\_PixEngineTextureSliceIndex\_int\_int\_int\_IPixEngine5Callbacks\_ptr\_DWORD\_DWORD
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: 'IPixEngine5 :: ReadTexelValueAsync, méthode'
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 28C44D12-383D-4E91-8BB1-12869782533C
api_name:
- IPixEngine5.ReadTexelValueAsync
api_type:
- COM
api_location:
- vspixengine.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: ca3510b01038df3b07b3033364902f76f2e05b4e
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/06/2021
ms.locfileid: "106515544"
---
# <a name="span-idvspixengineipixengine5_readtexelvalueasync_uint_pixenginetexturesliceindex_int_int_int_ipixengine5callbacks_ptr_dword_dwordspanipixengine5readtexelvalueasync-method"></a><span data-ttu-id="6e03b-103"><span id="vspixengine.ipixengine5_readtexelvalueasync_uint_pixenginetexturesliceindex_int_int_int_ipixengine5callbacks_ptr_dword_dword"></span>IPixEngine5 :: ReadTexelValueAsync, méthode</span><span class="sxs-lookup"><span data-stu-id="6e03b-103"><span id="vspixengine.ipixengine5_readtexelvalueasync_uint_pixenginetexturesliceindex_int_int_int_ipixengine5callbacks_ptr_dword_dword"></span>IPixEngine5::ReadTexelValueAsync method</span></span>

<span data-ttu-id="6e03b-104">Lit une valeur Texel et retourne le résultat au asynchrnously hôte.</span><span class="sxs-lookup"><span data-stu-id="6e03b-104">Reads a texel value and returns the result to the host asynchrnously.</span></span>

## <a name="syntax"></a><span data-ttu-id="6e03b-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="6e03b-105">Syntax</span></span>


```C++
HRESULT ReadTexelValueAsync(
   UINT                       textureId,
   PixEngineTextureSliceIndex sliceIndex,
   int                        x,
   int                        y,
   int                        formatOverride,
   IPixEngine5Callbacks*      callbacks,
   DWORD                      requestCookie,
   DWORD                      progressIntervalMsecs
);
```

## <a name="parameters"></a><span data-ttu-id="6e03b-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="6e03b-106">Parameters</span></span>

<span data-ttu-id="6e03b-107">*textureId* </span><span class="sxs-lookup"><span data-stu-id="6e03b-107">*textureId* </span></span>  
<span data-ttu-id="6e03b-108">ID de la texture à partir de laquelle lire la valeur Texel.</span><span class="sxs-lookup"><span data-stu-id="6e03b-108">The ID of the texture to read the texel value from.</span></span>

<span data-ttu-id="6e03b-109">*sliceIndex* </span><span class="sxs-lookup"><span data-stu-id="6e03b-109">*sliceIndex* </span></span>  
<span data-ttu-id="6e03b-110">Index de la tranche dans la texture à partir duquel lire la valeur Texel.</span><span class="sxs-lookup"><span data-stu-id="6e03b-110">The index of the slice within the texture to read the texel value from.</span></span>

<span data-ttu-id="6e03b-111">*x* </span><span class="sxs-lookup"><span data-stu-id="6e03b-111">*x* </span></span>  
<span data-ttu-id="6e03b-112">Coordonnée de Texel x à lire.</span><span class="sxs-lookup"><span data-stu-id="6e03b-112">The x texel coordinate to read.</span></span>

<span data-ttu-id="6e03b-113">*y* </span><span class="sxs-lookup"><span data-stu-id="6e03b-113">*y* </span></span>  
<span data-ttu-id="6e03b-114">Coordonnée de Texel y à lire.</span><span class="sxs-lookup"><span data-stu-id="6e03b-114">The y texel coordinate to read.</span></span>

<span data-ttu-id="6e03b-115">*formatOverride* </span><span class="sxs-lookup"><span data-stu-id="6e03b-115">*formatOverride* </span></span>  
<span data-ttu-id="6e03b-116">Remplacement du format de couleur.</span><span class="sxs-lookup"><span data-stu-id="6e03b-116">The color format override.</span></span>

<span data-ttu-id="6e03b-117">*rappels* </span><span class="sxs-lookup"><span data-stu-id="6e03b-117">*callbacks* </span></span>  
<span data-ttu-id="6e03b-118">Adresse d’un objet qui fournit l’interface de rappels IPixEngine5.</span><span class="sxs-lookup"><span data-stu-id="6e03b-118">The address of an object that provides the IPixEngine5 callbacks interface.</span></span>

<span data-ttu-id="6e03b-119">*requestCookie* </span><span class="sxs-lookup"><span data-stu-id="6e03b-119">*requestCookie* </span></span>  
<span data-ttu-id="6e03b-120">Cookie qui identifie de façon unique la demande et qui peut être utilisé pour signaler qu’il doit être annulé.</span><span class="sxs-lookup"><span data-stu-id="6e03b-120">A cookie that uniquely identifies the request, and can be used to signal for it to be cancelled.</span></span>

<span data-ttu-id="6e03b-121">*progressIntervalMsecs* </span><span class="sxs-lookup"><span data-stu-id="6e03b-121">*progressIntervalMsecs* </span></span>  
<span data-ttu-id="6e03b-122">Non utilisé.</span><span class="sxs-lookup"><span data-stu-id="6e03b-122">Not used.</span></span>

## <a name="return-value"></a><span data-ttu-id="6e03b-123">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="6e03b-123">Return value</span></span>

<span data-ttu-id="6e03b-124">Si cette méthode est réussie, elle retourne la valeur **\_ OK**.</span><span class="sxs-lookup"><span data-stu-id="6e03b-124">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="6e03b-125">Sinon, elle retourne un code d’erreur **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="6e03b-125">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="6e03b-126">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="6e03b-126">Requirements</span></span>

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><tbody><tr class="odd"><td><p><span data-ttu-id="6e03b-127">En-tête</span><span class="sxs-lookup"><span data-stu-id="6e03b-127">Header</span></span></p></td><td><span data-ttu-id="6e03b-128">Vspixengine. h</span><span class="sxs-lookup"><span data-stu-id="6e03b-128">Vspixengine.h</span></span></td></tr></tbody></table>

## <a name="span-idsee_alsospansee-also"></a><span data-ttu-id="6e03b-129"><span id="see_also"></span>Voir aussi</span><span class="sxs-lookup"><span data-stu-id="6e03b-129"><span id="see_also"></span>See also</span></span>

[<span data-ttu-id="6e03b-130">**IPixEngine5**</span><span class="sxs-lookup"><span data-stu-id="6e03b-130">**IPixEngine5**</span></span>](/windows/desktop/direct3dtools/ipixengine5)

 

 
