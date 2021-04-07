---
description: Demande à déboguer un nuanceur sur le GPU (débogage dynamique) vs CPU (débogage basé sur trace).
MS-HAID: vspixengine.IDebugLiveShaderRequest\_BeginDebugLiveShader\_DebugShaderRequestInfo\_ptr
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: 'IDebugLiveShaderRequest :: BeginDebugLiveShader, méthode'
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 805B2B68-C251-4192-85A3-F857B3F204C7
api_name:
- IDebugLiveShaderRequest.BeginDebugLiveShader
api_type:
- COM
api_location:
- vspixengine.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 2b09bff6a414df620e06263e13d94c2f39e36903
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/06/2021
ms.locfileid: "103746749"
---
# <a name="span-idvspixengineidebugliveshaderrequest_begindebugliveshader_debugshaderrequestinfo_ptrspanidebugliveshaderrequestbegindebugliveshader-method"></a><span data-ttu-id="b285b-103"><span id="vspixengine.idebugliveshaderrequest_begindebugliveshader_debugshaderrequestinfo_ptr"></span>IDebugLiveShaderRequest :: BeginDebugLiveShader, méthode</span><span class="sxs-lookup"><span data-stu-id="b285b-103"><span id="vspixengine.idebugliveshaderrequest_begindebugliveshader_debugshaderrequestinfo_ptr"></span>IDebugLiveShaderRequest::BeginDebugLiveShader method</span></span>

<span data-ttu-id="b285b-104">Demande à déboguer un nuanceur sur le GPU (débogage dynamique) vs CPU (débogage basé sur trace).</span><span class="sxs-lookup"><span data-stu-id="b285b-104">Requests to debug a shader on the GPU (live debugging) vs CPU (trace-based debugging).</span></span>

## <a name="syntax"></a><span data-ttu-id="b285b-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="b285b-105">Syntax</span></span>


```C++
HRESULT BeginDebugLiveShader(
   DebugShaderRequestInfo * requestInfo
);
```

## <a name="parameters"></a><span data-ttu-id="b285b-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="b285b-106">Parameters</span></span>

<span data-ttu-id="b285b-107">*requestInfo* </span><span class="sxs-lookup"><span data-stu-id="b285b-107">*requestInfo* </span></span>  
<span data-ttu-id="b285b-108">Adresse d’une structure DebugShaderRequestInfo qui décrit l’événement/vertex/pixel demandé.</span><span class="sxs-lookup"><span data-stu-id="b285b-108">The address of a DebugShaderRequestInfo structure that describes the requested event/vertex/pixel.</span></span>

## <a name="return-value"></a><span data-ttu-id="b285b-109">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="b285b-109">Return value</span></span>

<span data-ttu-id="b285b-110">Si cette méthode est réussie, elle retourne la valeur **\_ OK**.</span><span class="sxs-lookup"><span data-stu-id="b285b-110">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="b285b-111">Sinon, elle retourne un code d’erreur **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="b285b-111">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="b285b-112">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="b285b-112">Requirements</span></span>

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><tbody><tr class="odd"><td><p><span data-ttu-id="b285b-113">En-tête</span><span class="sxs-lookup"><span data-stu-id="b285b-113">Header</span></span></p></td><td><span data-ttu-id="b285b-114">Vspixengine. h</span><span class="sxs-lookup"><span data-stu-id="b285b-114">Vspixengine.h</span></span></td></tr></tbody></table>

## <a name="span-idsee_alsospansee-also"></a><span data-ttu-id="b285b-115"><span id="see_also"></span>Voir aussi</span><span class="sxs-lookup"><span data-stu-id="b285b-115"><span id="see_also"></span>See also</span></span>

[<span data-ttu-id="b285b-116">**IDebugLiveShaderRequest**</span><span class="sxs-lookup"><span data-stu-id="b285b-116">**IDebugLiveShaderRequest**</span></span>](/windows/desktop/direct3dtools/idebugliveshaderrequest)

 

 
