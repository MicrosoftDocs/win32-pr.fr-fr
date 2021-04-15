---
description: Demandes de génération d’instructions de trace de nuanceur dans une demande de débogage. Le débogage basé sur la trace se produit sur le processeur (Warp) au lieu du GPU.
MS-HAID: vspixengine.IDebugShaderRequest2\_GenerateInstructions\_IPixErrorCallback\_ptr\_DebugShaderRequestInfo\_ptr\_PixelHistoryOperation\_ptr\_IDebugShaderCallback\_ptr
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: 'IDebugShaderRequest2 :: GenerateInstructions, méthode'
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 50685D38-AA85-43D7-9199-12B3776708C2
api_name:
- IDebugShaderRequest2.GenerateInstructions
api_type:
- COM
api_location:
- vspixengine.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: e9c1bc2f6b3f885159f21cd7e644545d7639d6b3
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/06/2021
ms.locfileid: "104521860"
---
# <a name="span-idvspixengineidebugshaderrequest2_generateinstructions_ipixerrorcallback_ptr_debugshaderrequestinfo_ptr_pixelhistoryoperation_ptr_idebugshadercallback_ptrspanidebugshaderrequest2generateinstructions-method"></a><span data-ttu-id="a5116-104"><span id="vspixengine.idebugshaderrequest2_generateinstructions_ipixerrorcallback_ptr_debugshaderrequestinfo_ptr_pixelhistoryoperation_ptr_idebugshadercallback_ptr"></span>IDebugShaderRequest2 :: GenerateInstructions, méthode</span><span class="sxs-lookup"><span data-stu-id="a5116-104"><span id="vspixengine.idebugshaderrequest2_generateinstructions_ipixerrorcallback_ptr_debugshaderrequestinfo_ptr_pixelhistoryoperation_ptr_idebugshadercallback_ptr"></span>IDebugShaderRequest2::GenerateInstructions method</span></span>

<span data-ttu-id="a5116-105">Demandes de génération d’instructions de trace de nuanceur dans une demande de débogage.</span><span class="sxs-lookup"><span data-stu-id="a5116-105">Requests to generate shader trace instructions in a debug request.</span></span> <span data-ttu-id="a5116-106">Le débogage basé sur la trace se produit sur le processeur (Warp) au lieu du GPU.</span><span class="sxs-lookup"><span data-stu-id="a5116-106">Trace-based debugging occurs on the CPU (warp) instead of the GPU.</span></span>

## <a name="syntax"></a><span data-ttu-id="a5116-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="a5116-107">Syntax</span></span>


```C++
HRESULT GenerateInstructions(
   IPixErrorCallback *      errorCallback,
   DebugShaderRequestInfo * requestInfo,
   PixelHistoryOperation *  pPixelHistory,
   IDebugShaderCallback *   pCallback
);
```

## <a name="parameters"></a><span data-ttu-id="a5116-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="a5116-108">Parameters</span></span>

<span data-ttu-id="a5116-109">*errorCallback* </span><span class="sxs-lookup"><span data-stu-id="a5116-109">*errorCallback* </span></span>  
<span data-ttu-id="a5116-110">Adresse d’un rappel pour les erreurs qui peuvent se produire lors de la génération des instructions de trace du nuanceur.</span><span class="sxs-lookup"><span data-stu-id="a5116-110">The address of a callback for errors that might occur while generating shader trace instructions.</span></span>

<span data-ttu-id="a5116-111">*requestInfo* </span><span class="sxs-lookup"><span data-stu-id="a5116-111">*requestInfo* </span></span>  
<span data-ttu-id="a5116-112">Adresse d’une structure DebugShaderRequestInfo qui décrit l’événement/vertex/pixel demandé.</span><span class="sxs-lookup"><span data-stu-id="a5116-112">The address of a DebugShaderRequestInfo structure that describes the requested event/vertex/pixel.</span></span>

<span data-ttu-id="a5116-113">*pPixelHistory* </span><span class="sxs-lookup"><span data-stu-id="a5116-113">*pPixelHistory* </span></span>  
<span data-ttu-id="a5116-114">Adresse des résultats de l’historique des pixels utilisée pour rechercher le pixel associé à déboguer.</span><span class="sxs-lookup"><span data-stu-id="a5116-114">The address of pixel history results used for finding the associated pixel to debug.</span></span> <span data-ttu-id="a5116-115">S’applique uniquement lors du débogage d’un nuanceur de pixels.</span><span class="sxs-lookup"><span data-stu-id="a5116-115">Only applies when debugging a pixel shader.</span></span>

<span data-ttu-id="a5116-116">*pCallback* </span><span class="sxs-lookup"><span data-stu-id="a5116-116">*pCallback* </span></span>  
<span data-ttu-id="a5116-117">Adresse d’un rappel utilisé pour notifier l’hôte de résultats.</span><span class="sxs-lookup"><span data-stu-id="a5116-117">The address of a callback used to notify the host of results.</span></span>

## <a name="return-value"></a><span data-ttu-id="a5116-118">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="a5116-118">Return value</span></span>

<span data-ttu-id="a5116-119">Si cette méthode est réussie, elle retourne la valeur **\_ OK**.</span><span class="sxs-lookup"><span data-stu-id="a5116-119">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="a5116-120">Sinon, elle retourne un code d’erreur **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="a5116-120">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="a5116-121">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="a5116-121">Requirements</span></span>

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><tbody><tr class="odd"><td><p><span data-ttu-id="a5116-122">En-tête</span><span class="sxs-lookup"><span data-stu-id="a5116-122">Header</span></span></p></td><td><span data-ttu-id="a5116-123">Vspixengine. h</span><span class="sxs-lookup"><span data-stu-id="a5116-123">Vspixengine.h</span></span></td></tr></tbody></table>

## <a name="span-idsee_alsospansee-also"></a><span data-ttu-id="a5116-124"><span id="see_also"></span>Voir aussi</span><span class="sxs-lookup"><span data-stu-id="a5116-124"><span id="see_also"></span>See also</span></span>

[<span data-ttu-id="a5116-125">**IDebugShaderRequest2**</span><span class="sxs-lookup"><span data-stu-id="a5116-125">**IDebugShaderRequest2**</span></span>](/windows/desktop/direct3dtools/idebugshaderrequest2)

 

 
