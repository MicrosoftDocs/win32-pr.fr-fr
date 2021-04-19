---
description: Demandes d’annulation de la génération des instructions de trace du nuanceur dans une demande de débogage.
MS-HAID: vspixengine.IDebugShaderCancel\_CancelGenerate\_DebugShaderRequestInfo\_ptr\_PixelHistoryOperation\_ptr
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: 'IDebugShaderCancel :: CancelGenerate, méthode'
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 10DA5080-3AA6-47AA-BFE7-774BC26C7F95
api_name:
- IDebugShaderCancel.CancelGenerate
api_type:
- COM
api_location:
- vspixengine.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 5c2754f0d390960775b11ac5da121d5e6a20705a
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/06/2021
ms.locfileid: "106513284"
---
# <a name="span-idvspixengineidebugshadercancel_cancelgenerate_debugshaderrequestinfo_ptr_pixelhistoryoperation_ptrspanidebugshadercancelcancelgenerate-method"></a><span data-ttu-id="6fa40-103"><span id="vspixengine.idebugshadercancel_cancelgenerate_debugshaderrequestinfo_ptr_pixelhistoryoperation_ptr"></span>IDebugShaderCancel :: CancelGenerate, méthode</span><span class="sxs-lookup"><span data-stu-id="6fa40-103"><span id="vspixengine.idebugshadercancel_cancelgenerate_debugshaderrequestinfo_ptr_pixelhistoryoperation_ptr"></span>IDebugShaderCancel::CancelGenerate method</span></span>

<span data-ttu-id="6fa40-104">Demandes d’annulation de la génération des instructions de trace du nuanceur dans une demande de débogage.</span><span class="sxs-lookup"><span data-stu-id="6fa40-104">Requests to cancel generation of shader trace instructions in a debug request.</span></span>

## <a name="syntax"></a><span data-ttu-id="6fa40-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="6fa40-105">Syntax</span></span>


```C++
HRESULT CancelGenerate(
   DebugShaderRequestInfo * requestInfo,
   PixelHistoryOperation *  pPixelHistory
);
```

## <a name="parameters"></a><span data-ttu-id="6fa40-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="6fa40-106">Parameters</span></span>

<span data-ttu-id="6fa40-107">*requestInfo* </span><span class="sxs-lookup"><span data-stu-id="6fa40-107">*requestInfo* </span></span>  
<span data-ttu-id="6fa40-108">Adresse d’une structure DebugShaderRequestInfo qui décrit l’événement/vertex/pixel demandé.</span><span class="sxs-lookup"><span data-stu-id="6fa40-108">The address of a DebugShaderRequestInfo structure that describes the requested event/vertex/pixel.</span></span>

<span data-ttu-id="6fa40-109">*pPixelHistory* </span><span class="sxs-lookup"><span data-stu-id="6fa40-109">*pPixelHistory* </span></span>  
<span data-ttu-id="6fa40-110">Adresse des résultats de l’historique des pixels utilisée pour rechercher le pixel associé à déboguer.</span><span class="sxs-lookup"><span data-stu-id="6fa40-110">The address of pixel history results used for finding the associated pixel to debug.</span></span> <span data-ttu-id="6fa40-111">S’applique uniquement lors du débogage d’un nuanceur de pixels.</span><span class="sxs-lookup"><span data-stu-id="6fa40-111">Only applies when debugging a pixel shader.</span></span>

## <a name="return-value"></a><span data-ttu-id="6fa40-112">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="6fa40-112">Return value</span></span>

<span data-ttu-id="6fa40-113">Si cette méthode est réussie, elle retourne la valeur **\_ OK**.</span><span class="sxs-lookup"><span data-stu-id="6fa40-113">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="6fa40-114">Sinon, elle retourne un code d’erreur **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="6fa40-114">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="6fa40-115">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="6fa40-115">Requirements</span></span>

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><tbody><tr class="odd"><td><p><span data-ttu-id="6fa40-116">En-tête</span><span class="sxs-lookup"><span data-stu-id="6fa40-116">Header</span></span></p></td><td><span data-ttu-id="6fa40-117">Vspixengine. h</span><span class="sxs-lookup"><span data-stu-id="6fa40-117">Vspixengine.h</span></span></td></tr></tbody></table>

## <a name="span-idsee_alsospansee-also"></a><span data-ttu-id="6fa40-118"><span id="see_also"></span>Voir aussi</span><span class="sxs-lookup"><span data-stu-id="6fa40-118"><span id="see_also"></span>See also</span></span>

[<span data-ttu-id="6fa40-119">**IDebugShaderCancel**</span><span class="sxs-lookup"><span data-stu-id="6fa40-119">**IDebugShaderCancel**</span></span>](/windows/desktop/direct3dtools/idebugshadercancel)

 

 
