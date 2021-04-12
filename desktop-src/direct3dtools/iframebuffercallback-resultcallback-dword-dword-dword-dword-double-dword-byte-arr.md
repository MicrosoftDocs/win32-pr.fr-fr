---
description: Rappel qui avertit l’hôte des informations trame retournées par la requête associée.
MS-HAID: vspixengine.IFrameBufferCallback\_ResultCallback\_DWORD\_DWORD\_DWORD\_DWORD\_double\_DWORD\_BYTE\_arr
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: 'IFrameBufferCallback :: ResultCallback, méthode'
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: F0276125-2DA9-45BC-A295-BD67C21EE601
api_name:
- IFrameBufferCallback.ResultCallback
api_type:
- COM
api_location:
- vspixengine.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 5433c7bbf5fe67455b60fd754eecb2c2877c5d6f
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/06/2021
ms.locfileid: "104109246"
---
# <a name="span-idvspixengineiframebuffercallback_resultcallback_dword_dword_dword_dword_double_dword_byte_arrspaniframebuffercallbackresultcallback-method"></a><span data-ttu-id="08688-103"><span id="vspixengine.iframebuffercallback_resultcallback_dword_dword_dword_dword_double_dword_byte_arr"></span>IFrameBufferCallback :: ResultCallback, méthode</span><span class="sxs-lookup"><span data-stu-id="08688-103"><span id="vspixengine.iframebuffercallback_resultcallback_dword_dword_dword_dword_double_dword_byte_arr"></span>IFrameBufferCallback::ResultCallback method</span></span>

<span data-ttu-id="08688-104">Rappel qui avertit l’hôte des informations trame retournées par la requête associée.</span><span class="sxs-lookup"><span data-stu-id="08688-104">A callback that notifies the host of framebuffer information returned by the associated request.</span></span>

## <a name="syntax"></a><span data-ttu-id="08688-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="08688-105">Syntax</span></span>


```C++
HRESULT ResultCallback(
   DWORD   frameNumber,
   DWORD   width,
   DWORD   height,
   DWORD   renderTargetPtr,
   double  frameDuraction,
   DWORD   size,
   BYTE [] count5_buffer
);
```

## <a name="parameters"></a><span data-ttu-id="08688-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="08688-106">Parameters</span></span>

<span data-ttu-id="08688-107">*frameNumber* </span><span class="sxs-lookup"><span data-stu-id="08688-107">*frameNumber* </span></span>  
<span data-ttu-id="08688-108">Numéro de frame.</span><span class="sxs-lookup"><span data-stu-id="08688-108">The frame number.</span></span>

<span data-ttu-id="08688-109">*Largeur* </span><span class="sxs-lookup"><span data-stu-id="08688-109">*width* </span></span>  
<span data-ttu-id="08688-110">Largeur du cadre.</span><span class="sxs-lookup"><span data-stu-id="08688-110">The width of the frame.</span></span>

<span data-ttu-id="08688-111">*celle* </span><span class="sxs-lookup"><span data-stu-id="08688-111">*height* </span></span>  
<span data-ttu-id="08688-112">Hauteur du cadre.</span><span class="sxs-lookup"><span data-stu-id="08688-112">The height of the frame.</span></span>

<span data-ttu-id="08688-113">*renderTargetPtr* </span><span class="sxs-lookup"><span data-stu-id="08688-113">*renderTargetPtr* </span></span>  
<span data-ttu-id="08688-114">Cible de rendu d’où proviennent les résultats.</span><span class="sxs-lookup"><span data-stu-id="08688-114">The render target that the results come from.</span></span> <span data-ttu-id="08688-115">Il s’agit toujours d’un emplacement spécifié par la demande de mémoire tampon de trame ou, s’il ne s’agit pas d’un appel de dessin, le premier RTV Bount à la source de sortie.</span><span class="sxs-lookup"><span data-stu-id="08688-115">It is always a slot specified by the frame buffer request, or if not a draw call, then the first RTV bount to the output source.</span></span>

<span data-ttu-id="08688-116">*frameDuraction* </span><span class="sxs-lookup"><span data-stu-id="08688-116">*frameDuraction* </span></span>  
<span data-ttu-id="08688-117">Non utilisé.</span><span class="sxs-lookup"><span data-stu-id="08688-117">Not used.</span></span>

<span data-ttu-id="08688-118">*corps* </span><span class="sxs-lookup"><span data-stu-id="08688-118">*size* </span></span>  
<span data-ttu-id="08688-119">Taille de la mémoire tampon de sortie en octets.</span><span class="sxs-lookup"><span data-stu-id="08688-119">The size of the output buffer in bytes.</span></span>

<span data-ttu-id="08688-120">*\_mémoire tampon count5* </span><span class="sxs-lookup"><span data-stu-id="08688-120">*count5\_buffer* </span></span>  
<span data-ttu-id="08688-121">Contenu de la cible de rendu au \_ format R8G8B8A8 UNORM.</span><span class="sxs-lookup"><span data-stu-id="08688-121">The contents of the render target in R8G8B8A8\_UNORM format.</span></span>

## <a name="return-value"></a><span data-ttu-id="08688-122">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="08688-122">Return value</span></span>

<span data-ttu-id="08688-123">Si cette méthode est réussie, elle retourne la valeur **\_ OK**.</span><span class="sxs-lookup"><span data-stu-id="08688-123">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="08688-124">Sinon, elle retourne un code d’erreur **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="08688-124">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="08688-125">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="08688-125">Requirements</span></span>

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><tbody><tr class="odd"><td><p><span data-ttu-id="08688-126">En-tête</span><span class="sxs-lookup"><span data-stu-id="08688-126">Header</span></span></p></td><td><span data-ttu-id="08688-127">Vspixengine. h</span><span class="sxs-lookup"><span data-stu-id="08688-127">Vspixengine.h</span></span></td></tr></tbody></table>

## <a name="span-idsee_alsospansee-also"></a><span data-ttu-id="08688-128"><span id="see_also"></span>Voir aussi</span><span class="sxs-lookup"><span data-stu-id="08688-128"><span id="see_also"></span>See also</span></span>

[<span data-ttu-id="08688-129">**IFrameBufferCallback**</span><span class="sxs-lookup"><span data-stu-id="08688-129">**IFrameBufferCallback**</span></span>](/windows/desktop/direct3dtools/iframebuffercallback)

 

 
