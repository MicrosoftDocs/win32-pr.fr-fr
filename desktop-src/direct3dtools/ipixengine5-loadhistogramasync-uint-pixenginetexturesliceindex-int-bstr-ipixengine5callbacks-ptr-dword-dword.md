---
description: Demande asynchrone de chargement des données de l’histogramme.
MS-HAID: vspixengine.IPixEngine5\_LoadHistogramAsync\_UINT\_PixEngineTextureSliceIndex\_int\_BSTR\_IPixEngine5Callbacks\_ptr\_DWORD\_DWORD
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: 'IPixEngine5 :: LoadHistogramAsync, méthode'
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: A23CB3E0-B299-40FD-899E-9FE6E9177551
api_name:
- IPixEngine5.LoadHistogramAsync
api_type:
- COM
api_location:
- vspixengine.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 7c7128743c2086c0ddc2875c493dac98617986a6
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/06/2021
ms.locfileid: "106515909"
---
# <a name="span-idvspixengineipixengine5_loadhistogramasync_uint_pixenginetexturesliceindex_int_bstr_ipixengine5callbacks_ptr_dword_dwordspanipixengine5loadhistogramasync-method"></a><span data-ttu-id="951f6-103"><span id="vspixengine.ipixengine5_loadhistogramasync_uint_pixenginetexturesliceindex_int_bstr_ipixengine5callbacks_ptr_dword_dword"></span>IPixEngine5 :: LoadHistogramAsync, méthode</span><span class="sxs-lookup"><span data-stu-id="951f6-103"><span id="vspixengine.ipixengine5_loadhistogramasync_uint_pixenginetexturesliceindex_int_bstr_ipixengine5callbacks_ptr_dword_dword"></span>IPixEngine5::LoadHistogramAsync method</span></span>

<span data-ttu-id="951f6-104">Demande asynchrone de chargement des données de l’histogramme.</span><span class="sxs-lookup"><span data-stu-id="951f6-104">An asynchronous request to load histogram data.</span></span>

## <a name="syntax"></a><span data-ttu-id="951f6-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="951f6-105">Syntax</span></span>


```C++
HRESULT LoadHistogramAsync(
   UINT                       textureId,
   PixEngineTextureSliceIndex sliceIndex,
   int                        formatOverride,
   BSTR                       histogramDataFileName,
   IPixEngine5Callbacks*      callbacks,
   DWORD                      requestCookie,
   DWORD                      progressIntervalMsecs
);
```

## <a name="parameters"></a><span data-ttu-id="951f6-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="951f6-106">Parameters</span></span>

<span data-ttu-id="951f6-107">*textureId* </span><span class="sxs-lookup"><span data-stu-id="951f6-107">*textureId* </span></span>  
<span data-ttu-id="951f6-108">ID de la texture pour laquelle charger les données de l’histogramme.</span><span class="sxs-lookup"><span data-stu-id="951f6-108">The ID of the texture to load histogram data for.</span></span>

<span data-ttu-id="951f6-109">*sliceIndex* </span><span class="sxs-lookup"><span data-stu-id="951f6-109">*sliceIndex* </span></span>  
<span data-ttu-id="951f6-110">Index de la tranche pour laquelle charger les données de l’histogramme.</span><span class="sxs-lookup"><span data-stu-id="951f6-110">The index of the slice to load histogram data for.</span></span>

<span data-ttu-id="951f6-111">*formatOverride* </span><span class="sxs-lookup"><span data-stu-id="951f6-111">*formatOverride* </span></span>  
<span data-ttu-id="951f6-112">Spécifie la substitution de format.</span><span class="sxs-lookup"><span data-stu-id="951f6-112">Specifies the format override.</span></span>

<span data-ttu-id="951f6-113">*histogramDataFileName* </span><span class="sxs-lookup"><span data-stu-id="951f6-113">*histogramDataFileName* </span></span>  
<span data-ttu-id="951f6-114">Chaîne COM contenant le nom du fichier de données de l’histogramme.</span><span class="sxs-lookup"><span data-stu-id="951f6-114">A COM string containing the name of the histogram data file.</span></span>

<span data-ttu-id="951f6-115">*rappels* </span><span class="sxs-lookup"><span data-stu-id="951f6-115">*callbacks* </span></span>  
<span data-ttu-id="951f6-116">Adresse d’un objet qui fournit l’interface de rappels IPixEngine5.</span><span class="sxs-lookup"><span data-stu-id="951f6-116">The address of an object that provides the IPixEngine5 callbacks interface.</span></span>

<span data-ttu-id="951f6-117">*requestCookie* </span><span class="sxs-lookup"><span data-stu-id="951f6-117">*requestCookie* </span></span>  
<span data-ttu-id="951f6-118">Cookie qui identifie de façon unique la demande et qui peut être utilisé pour signaler qu’il doit être annulé.</span><span class="sxs-lookup"><span data-stu-id="951f6-118">A cookie that uniquely identifies the request, and can be used to signal for it to be cancelled.</span></span>

<span data-ttu-id="951f6-119">*progressIntervalMsecs* </span><span class="sxs-lookup"><span data-stu-id="951f6-119">*progressIntervalMsecs* </span></span>  
<span data-ttu-id="951f6-120">Non utilisé.</span><span class="sxs-lookup"><span data-stu-id="951f6-120">Not used.</span></span>

## <a name="return-value"></a><span data-ttu-id="951f6-121">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="951f6-121">Return value</span></span>

<span data-ttu-id="951f6-122">Si cette méthode est réussie, elle retourne la valeur **\_ OK**.</span><span class="sxs-lookup"><span data-stu-id="951f6-122">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="951f6-123">Sinon, elle retourne un code d’erreur **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="951f6-123">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="951f6-124">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="951f6-124">Requirements</span></span>

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><tbody><tr class="odd"><td><p><span data-ttu-id="951f6-125">En-tête</span><span class="sxs-lookup"><span data-stu-id="951f6-125">Header</span></span></p></td><td><span data-ttu-id="951f6-126">Vspixengine. h</span><span class="sxs-lookup"><span data-stu-id="951f6-126">Vspixengine.h</span></span></td></tr></tbody></table>

## <a name="span-idsee_alsospansee-also"></a><span data-ttu-id="951f6-127"><span id="see_also"></span>Voir aussi</span><span class="sxs-lookup"><span data-stu-id="951f6-127"><span id="see_also"></span>See also</span></span>

[<span data-ttu-id="951f6-128">**IPixEngine5**</span><span class="sxs-lookup"><span data-stu-id="951f6-128">**IPixEngine5**</span></span>](/windows/desktop/direct3dtools/ipixengine5)

 

 
