---
description: Demande de démarrer le débogage de la liste d’instructions spécifiée.
MS-HAID: vspixengine.IDebugShaderRequest2\_BeginDebugShader\_IPixErrorCallback\_ptr\_DWORD\_BYTE\_arr\_DWORD\_ptr
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: 'IDebugShaderRequest2 :: BeginDebugShader, méthode'
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: B454D673-C14F-4A8F-9DA7-2C47510BE5DA
api_name:
- IDebugShaderRequest2.BeginDebugShader
api_type:
- COM
api_location:
- vspixengine.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 39f6749a233140b745097bc1270963e50d0f11fb
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/06/2021
ms.locfileid: "104109254"
---
# <a name="span-idvspixengineidebugshaderrequest2_begindebugshader_ipixerrorcallback_ptr_dword_byte_arr_dword_ptrspanidebugshaderrequest2begindebugshader-method"></a><span data-ttu-id="dc76f-103"><span id="vspixengine.idebugshaderrequest2_begindebugshader_ipixerrorcallback_ptr_dword_byte_arr_dword_ptr"></span>IDebugShaderRequest2 :: BeginDebugShader, méthode</span><span class="sxs-lookup"><span data-stu-id="dc76f-103"><span id="vspixengine.idebugshaderrequest2_begindebugshader_ipixerrorcallback_ptr_dword_byte_arr_dword_ptr"></span>IDebugShaderRequest2::BeginDebugShader method</span></span>

<span data-ttu-id="dc76f-104">Demande de démarrer le débogage de la liste d’instructions spécifiée.</span><span class="sxs-lookup"><span data-stu-id="dc76f-104">Requests to start debugging the specified list of instructions.</span></span>

## <a name="syntax"></a><span data-ttu-id="dc76f-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="dc76f-105">Syntax</span></span>


```C++
HRESULT BeginDebugShader(
   IPixErrorCallback * errorCallback,
   DWORD               instructionStreamSize,
   BYTE []             count1_instructionStream,
   DWORD *             pDevice
);
```

## <a name="parameters"></a><span data-ttu-id="dc76f-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="dc76f-106">Parameters</span></span>

<span data-ttu-id="dc76f-107">*errorCallback* </span><span class="sxs-lookup"><span data-stu-id="dc76f-107">*errorCallback* </span></span>  
<span data-ttu-id="dc76f-108">Adresse d’un rappel pour les erreurs qui peuvent se produire pendant le débogage.</span><span class="sxs-lookup"><span data-stu-id="dc76f-108">The address of a callback for errors that might occur during debugging.</span></span>

<span data-ttu-id="dc76f-109">*instructionStreamSize* </span><span class="sxs-lookup"><span data-stu-id="dc76f-109">*instructionStreamSize* </span></span>  
<span data-ttu-id="dc76f-110">Nombre d’instructions dans le flux d’instructions.</span><span class="sxs-lookup"><span data-stu-id="dc76f-110">The number of instructions in the instruction stream.</span></span>

<span data-ttu-id="dc76f-111">*count1 \_ instructionStream* </span><span class="sxs-lookup"><span data-stu-id="dc76f-111">*count1\_instructionStream* </span></span>  
<span data-ttu-id="dc76f-112">Flux d’instructions spécifié.</span><span class="sxs-lookup"><span data-stu-id="dc76f-112">The specified instruction stream.</span></span>

<span data-ttu-id="dc76f-113">*pDevice* </span><span class="sxs-lookup"><span data-stu-id="dc76f-113">*pDevice* </span></span>  
<span data-ttu-id="dc76f-114">Adresse à passer au moteur de débogage pour communiquer avec cette session de débogage (moteur de débogage ReadProcessMemory sur cette adresse).</span><span class="sxs-lookup"><span data-stu-id="dc76f-114">The address to pass to the debug engine for communicating with this debug session (debug engine readprocessmemory on this address).</span></span>

## <a name="return-value"></a><span data-ttu-id="dc76f-115">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="dc76f-115">Return value</span></span>

<span data-ttu-id="dc76f-116">Si cette méthode est réussie, elle retourne la valeur **\_ OK**.</span><span class="sxs-lookup"><span data-stu-id="dc76f-116">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="dc76f-117">Sinon, elle retourne un code d’erreur **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="dc76f-117">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="dc76f-118">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="dc76f-118">Requirements</span></span>

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><tbody><tr class="odd"><td><p><span data-ttu-id="dc76f-119">En-tête</span><span class="sxs-lookup"><span data-stu-id="dc76f-119">Header</span></span></p></td><td><span data-ttu-id="dc76f-120">Vspixengine. h</span><span class="sxs-lookup"><span data-stu-id="dc76f-120">Vspixengine.h</span></span></td></tr></tbody></table>

## <a name="span-idsee_alsospansee-also"></a><span data-ttu-id="dc76f-121"><span id="see_also"></span>Voir aussi</span><span class="sxs-lookup"><span data-stu-id="dc76f-121"><span id="see_also"></span>See also</span></span>

[<span data-ttu-id="dc76f-122">**IDebugShaderRequest2**</span><span class="sxs-lookup"><span data-stu-id="dc76f-122">**IDebugShaderRequest2**</span></span>](/windows/desktop/direct3dtools/idebugshaderrequest2)

 

 
