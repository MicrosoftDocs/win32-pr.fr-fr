---
description: 'Demande de démarrage du débogage d’un nuanceur. Cette requête contient deux parties : générer une trace et déboguer une trace.'
MS-HAID: vspixengine.IDebugShaderRequest2
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: Interface IDebugShaderRequest2
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 80F95900-F2E6-4B5C-B902-573280956E94
api_name:
- IDebugShaderRequest2
api_type:
- COM
api_location:
- vspixengine.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 7b7c183cc04422d47b8d6599c67f2e7c1f5e58cd
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/06/2021
ms.locfileid: "104109250"
---
# <a name="span-idvspixengineidebugshaderrequest2spanidebugshaderrequest2-interface"></a><span data-ttu-id="46145-104"><span id="vspixengine.idebugshaderrequest2"></span>Interface IDebugShaderRequest2</span><span class="sxs-lookup"><span data-stu-id="46145-104"><span id="vspixengine.idebugshaderrequest2"></span>IDebugShaderRequest2 interface</span></span>

<span data-ttu-id="46145-105">Demande de démarrage du débogage d’un nuanceur.</span><span class="sxs-lookup"><span data-stu-id="46145-105">Request to start debugging a shader.</span></span> <span data-ttu-id="46145-106">Cette requête contient deux parties : générer une trace et déboguer une trace.</span><span class="sxs-lookup"><span data-stu-id="46145-106">This request contains two parts: generate a trace, and debug a trace.</span></span>

## <a name="members"></a><span data-ttu-id="46145-107">Membres</span><span class="sxs-lookup"><span data-stu-id="46145-107">Members</span></span>

<span data-ttu-id="46145-108">L’interface **IDebugShaderRequest2** hérite de l’interface [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) .</span><span class="sxs-lookup"><span data-stu-id="46145-108">The **IDebugShaderRequest2** interface inherits from the [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="46145-109">**IDebugShaderRequest2** a également les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="46145-109">**IDebugShaderRequest2** also has these types of members:</span></span>

-   [<span data-ttu-id="46145-110">Méthodes</span><span class="sxs-lookup"><span data-stu-id="46145-110">Methods</span></span>](#methods)

### <a name="span-idmethodsspanmethods"></a><span data-ttu-id="46145-111"><span id="methods"></span>Méthodes</span><span class="sxs-lookup"><span data-stu-id="46145-111"><span id="methods"></span>Methods</span></span>

<span data-ttu-id="46145-112">L’interface **IDebugShaderRequest2** possède ces méthodes.</span><span class="sxs-lookup"><span data-stu-id="46145-112">The **IDebugShaderRequest2** interface has these methods.</span></span>

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><thead><tr class="header"><th style="text-align: left;"><span data-ttu-id="46145-113">Méthode</span><span class="sxs-lookup"><span data-stu-id="46145-113">Method</span></span></th><th style="text-align: left;"><span data-ttu-id="46145-114">Description</span><span class="sxs-lookup"><span data-stu-id="46145-114">Description</span></span></th></tr></thead><tbody><tr class="odd"><td style="text-align: left;"><span data-ttu-id="46145-115"><a href="/windows/desktop/direct3dtools/idebugshaderrequest2-begindebugshader-ipixerrorcallback-ptr-dword-byte-arr-dword-ptr"><strong>BeginDebugShader</strong></a></span><span class="sxs-lookup"><span data-stu-id="46145-115"><a href="/windows/desktop/direct3dtools/idebugshaderrequest2-begindebugshader-ipixerrorcallback-ptr-dword-byte-arr-dword-ptr"><strong>BeginDebugShader</strong></a></span></span></td><td style="text-align: left;"><p><span data-ttu-id="46145-116">Demande de démarrer le débogage de la liste d’instructions spécifiée.</span><span class="sxs-lookup"><span data-stu-id="46145-116">Requests to start debugging the specified list of instructions.</span></span></p></td></tr><tr class="even"><td style="text-align: left;"><span data-ttu-id="46145-117"><a href="/windows/desktop/direct3dtools/idebugshaderrequest2-generateinstructions-ipixerrorcallback-ptr-debugshaderrequestinfo-ptr-pixelhistoryoperation-ptr-idebugshadercallback-ptr"><strong>GenerateInstructions</strong></a></span><span class="sxs-lookup"><span data-stu-id="46145-117"><a href="/windows/desktop/direct3dtools/idebugshaderrequest2-generateinstructions-ipixerrorcallback-ptr-debugshaderrequestinfo-ptr-pixelhistoryoperation-ptr-idebugshadercallback-ptr"><strong>GenerateInstructions</strong></a></span></span></td><td style="text-align: left;"><p><span data-ttu-id="46145-118">Demandes de génération d’instructions de trace de nuanceur dans une demande de débogage.</span><span class="sxs-lookup"><span data-stu-id="46145-118">Requests to generate shader trace instructions in a debug request.</span></span> <span data-ttu-id="46145-119">Le débogage basé sur la trace se produit sur le processeur (Warp) au lieu du GPU.</span><span class="sxs-lookup"><span data-stu-id="46145-119">Trace-based debugging occurs on the CPU (warp) instead of the GPU.</span></span></p></td></tr></tbody></table>

 

## <a name="requirements"></a><span data-ttu-id="46145-120">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="46145-120">Requirements</span></span>

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><tbody><tr class="odd"><td><p><span data-ttu-id="46145-121">En-tête</span><span class="sxs-lookup"><span data-stu-id="46145-121">Header</span></span></p></td><td><span data-ttu-id="46145-122">Vspixengine. h</span><span class="sxs-lookup"><span data-stu-id="46145-122">Vspixengine.h</span></span></td></tr></tbody></table>

 

 
