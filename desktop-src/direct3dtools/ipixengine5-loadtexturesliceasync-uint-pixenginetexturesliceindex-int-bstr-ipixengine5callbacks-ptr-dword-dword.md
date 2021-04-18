---
description: Charge une tranche de texture et avertit l’hôte asynchrnously lorsqu’il se termine.
MS-HAID: vspixengine.IPixEngine5\_LoadTextureSliceAsync\_UINT\_PixEngineTextureSliceIndex\_int\_BSTR\_IPixEngine5Callbacks\_ptr\_DWORD\_DWORD
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: 'IPixEngine5 :: LoadTextureSliceAsync, méthode'
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 520DBB6D-D8F3-451F-942C-BE8428B9ADFF
api_name:
- IPixEngine5.LoadTextureSliceAsync
api_type:
- COM
api_location:
- vspixengine.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 505ccfd6668cbe08b4f62878b5f51e9c20185b41
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/06/2021
ms.locfileid: "106543436"
---
# <a name="span-idvspixengineipixengine5_loadtexturesliceasync_uint_pixenginetexturesliceindex_int_bstr_ipixengine5callbacks_ptr_dword_dwordspanipixengine5loadtexturesliceasync-method"></a><span data-ttu-id="e9c21-103"><span id="vspixengine.ipixengine5_loadtexturesliceasync_uint_pixenginetexturesliceindex_int_bstr_ipixengine5callbacks_ptr_dword_dword"></span>IPixEngine5 :: LoadTextureSliceAsync, méthode</span><span class="sxs-lookup"><span data-stu-id="e9c21-103"><span id="vspixengine.ipixengine5_loadtexturesliceasync_uint_pixenginetexturesliceindex_int_bstr_ipixengine5callbacks_ptr_dword_dword"></span>IPixEngine5::LoadTextureSliceAsync method</span></span>

<span data-ttu-id="e9c21-104">Charge une tranche de texture et avertit l’hôte asynchrnously lorsqu’il se termine.</span><span class="sxs-lookup"><span data-stu-id="e9c21-104">Loads a texture slice and notifies the host asynchrnously when it completes.</span></span>

## <a name="syntax"></a><span data-ttu-id="e9c21-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="e9c21-105">Syntax</span></span>


```C++
HRESULT LoadTextureSliceAsync(
   UINT                       textureId,
   PixEngineTextureSliceIndex sliceIndex,
   int                        formatOverride,
   BSTR                       histogramDataFileName,
   IPixEngine5Callbacks*      callbacks,
   DWORD                      requestCookie,
   DWORD                      progressIntervalMsecs
);
```

## <a name="parameters"></a><span data-ttu-id="e9c21-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="e9c21-106">Parameters</span></span>

<span data-ttu-id="e9c21-107">*textureId* </span><span class="sxs-lookup"><span data-stu-id="e9c21-107">*textureId* </span></span>  
<span data-ttu-id="e9c21-108">ID de la texture pour laquelle charger la tranche.</span><span class="sxs-lookup"><span data-stu-id="e9c21-108">The ID of the texture to load the slice for.</span></span>

<span data-ttu-id="e9c21-109">*sliceIndex* </span><span class="sxs-lookup"><span data-stu-id="e9c21-109">*sliceIndex* </span></span>  
<span data-ttu-id="e9c21-110">Index de la tranche à charger.</span><span class="sxs-lookup"><span data-stu-id="e9c21-110">The index of the slice to load.</span></span>

<span data-ttu-id="e9c21-111">*formatOverride* </span><span class="sxs-lookup"><span data-stu-id="e9c21-111">*formatOverride* </span></span>  
<span data-ttu-id="e9c21-112">Spécifie la substitution de format.</span><span class="sxs-lookup"><span data-stu-id="e9c21-112">Specifies the format override.</span></span>

<span data-ttu-id="e9c21-113">*histogramDataFileName* </span><span class="sxs-lookup"><span data-stu-id="e9c21-113">*histogramDataFileName* </span></span>  
<span data-ttu-id="e9c21-114">Chaîne COM contenant le nom du fichier de données de l’histogramme associé à la tranche de texture.</span><span class="sxs-lookup"><span data-stu-id="e9c21-114">A COM string containing the name of the histogram data file associated with the texture slice.</span></span>

<span data-ttu-id="e9c21-115">*rappels* </span><span class="sxs-lookup"><span data-stu-id="e9c21-115">*callbacks* </span></span>  
<span data-ttu-id="e9c21-116">Adresse d’un objet qui fournit l’interface de rappels IPixEngine5.</span><span class="sxs-lookup"><span data-stu-id="e9c21-116">The address of an object that provides the IPixEngine5 callbacks interface.</span></span>

<span data-ttu-id="e9c21-117">*requestCookie* </span><span class="sxs-lookup"><span data-stu-id="e9c21-117">*requestCookie* </span></span>  
<span data-ttu-id="e9c21-118">Cookie qui identifie de façon unique la demande et qui peut être utilisé pour signaler qu’il doit être annulé.</span><span class="sxs-lookup"><span data-stu-id="e9c21-118">A cookie that uniquely identifies the request, and can be used to signal for it to be cancelled.</span></span>

<span data-ttu-id="e9c21-119">*progressIntervalMsecs* </span><span class="sxs-lookup"><span data-stu-id="e9c21-119">*progressIntervalMsecs* </span></span>  
<span data-ttu-id="e9c21-120">Non utilisé.</span><span class="sxs-lookup"><span data-stu-id="e9c21-120">Not used.</span></span>

## <a name="return-value"></a><span data-ttu-id="e9c21-121">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="e9c21-121">Return value</span></span>

<span data-ttu-id="e9c21-122">Si cette méthode est réussie, elle retourne la valeur **\_ OK**.</span><span class="sxs-lookup"><span data-stu-id="e9c21-122">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="e9c21-123">Sinon, elle retourne un code d’erreur **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="e9c21-123">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="e9c21-124">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="e9c21-124">Requirements</span></span>

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><tbody><tr class="odd"><td><p><span data-ttu-id="e9c21-125">En-tête</span><span class="sxs-lookup"><span data-stu-id="e9c21-125">Header</span></span></p></td><td><span data-ttu-id="e9c21-126">Vspixengine. h</span><span class="sxs-lookup"><span data-stu-id="e9c21-126">Vspixengine.h</span></span></td></tr></tbody></table>

## <a name="span-idsee_alsospansee-also"></a><span data-ttu-id="e9c21-127"><span id="see_also"></span>Voir aussi</span><span class="sxs-lookup"><span data-stu-id="e9c21-127"><span id="see_also"></span>See also</span></span>

[<span data-ttu-id="e9c21-128">**IPixEngine5**</span><span class="sxs-lookup"><span data-stu-id="e9c21-128">**IPixEngine5**</span></span>](/windows/desktop/direct3dtools/ipixengine5)

 

 
