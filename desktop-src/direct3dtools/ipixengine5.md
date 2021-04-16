---
description: Extensions de l’interface IPixEngine4 contenant des ajouts pour l’affichage des textures.
MS-HAID: vspixengine.IPixEngine5
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: Interface IPixEngine5
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 8995B617-6830-4A07-8C83-B5925E033967
api_name:
- IPixEngine5
api_type:
- COM
api_location:
- vspixengine.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 300ed31eae5d8ff4009f28691c5348db7cd89d6e
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/06/2021
ms.locfileid: "104521383"
---
# <a name="span-idvspixengineipixengine5spanipixengine5-interface"></a><span data-ttu-id="d0551-103"><span id="vspixengine.ipixengine5"></span>Interface IPixEngine5</span><span class="sxs-lookup"><span data-stu-id="d0551-103"><span id="vspixengine.ipixengine5"></span>IPixEngine5 interface</span></span>

<span data-ttu-id="d0551-104">Extensions de l’interface IPixEngine4 contenant des ajouts pour l’affichage des textures.</span><span class="sxs-lookup"><span data-stu-id="d0551-104">Extensions to the IPixEngine4 interface containing additions for viewing textures.</span></span>

## <a name="members"></a><span data-ttu-id="d0551-105">Membres</span><span class="sxs-lookup"><span data-stu-id="d0551-105">Members</span></span>

<span data-ttu-id="d0551-106">L’interface **IPixEngine5** hérite de l’interface [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) .</span><span class="sxs-lookup"><span data-stu-id="d0551-106">The **IPixEngine5** interface inherits from the [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="d0551-107">**IPixEngine5** a également les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="d0551-107">**IPixEngine5** also has these types of members:</span></span>

-   [<span data-ttu-id="d0551-108">Méthodes</span><span class="sxs-lookup"><span data-stu-id="d0551-108">Methods</span></span>](#methods)

### <a name="span-idmethodsspanmethods"></a><span data-ttu-id="d0551-109"><span id="methods"></span>Méthodes</span><span class="sxs-lookup"><span data-stu-id="d0551-109"><span id="methods"></span>Methods</span></span>

<span data-ttu-id="d0551-110">L’interface **IPixEngine5** possède ces méthodes.</span><span class="sxs-lookup"><span data-stu-id="d0551-110">The **IPixEngine5** interface has these methods.</span></span>

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><thead><tr class="header"><th style="text-align: left;"><span data-ttu-id="d0551-111">Méthode</span><span class="sxs-lookup"><span data-stu-id="d0551-111">Method</span></span></th><th style="text-align: left;"><span data-ttu-id="d0551-112">Description</span><span class="sxs-lookup"><span data-stu-id="d0551-112">Description</span></span></th></tr></thead><tbody><tr class="odd"><td style="text-align: left;"><span data-ttu-id="d0551-113"><a href="/windows/desktop/direct3dtools/ipixengine5-freetextureasync-uint-ipixengine5callbacks-ptr-dword-dword"><strong>FreeTextureAsync</strong></a></span><span class="sxs-lookup"><span data-stu-id="d0551-113"><a href="/windows/desktop/direct3dtools/ipixengine5-freetextureasync-uint-ipixengine5callbacks-ptr-dword-dword"><strong>FreeTextureAsync</strong></a></span></span></td><td style="text-align: left;"><p><span data-ttu-id="d0551-114">Libère une texture et avertit l’hôte de manière asynchrone.</span><span class="sxs-lookup"><span data-stu-id="d0551-114">Frees a texture and notifies the host asynchronously.</span></span></p></td></tr><tr class="even"><td style="text-align: left;"><span data-ttu-id="d0551-115"><a href="/windows/desktop/direct3dtools/ipixengine5-loadhistogramasync-uint-pixenginetexturesliceindex-int-bstr-ipixengine5callbacks-ptr-dword-dword"><strong>LoadHistogramAsync</strong></a></span><span class="sxs-lookup"><span data-stu-id="d0551-115"><a href="/windows/desktop/direct3dtools/ipixengine5-loadhistogramasync-uint-pixenginetexturesliceindex-int-bstr-ipixengine5callbacks-ptr-dword-dword"><strong>LoadHistogramAsync</strong></a></span></span></td><td style="text-align: left;"><p><span data-ttu-id="d0551-116">Demande asynchrone de chargement des données de l’histogramme.</span><span class="sxs-lookup"><span data-stu-id="d0551-116">An asynchronous request to load histogram data.</span></span></p></td></tr><tr class="odd"><td style="text-align: left;"><span data-ttu-id="d0551-117"><a href="/windows/desktop/direct3dtools/ipixengine5-loadtexturefromfileasync-bstr-bstr-ipixengine5callbacks-ptr-dword-dword"><strong>LoadTextureFromFileAsync</strong></a></span><span class="sxs-lookup"><span data-stu-id="d0551-117"><a href="/windows/desktop/direct3dtools/ipixengine5-loadtexturefromfileasync-bstr-bstr-ipixengine5callbacks-ptr-dword-dword"><strong>LoadTextureFromFileAsync</strong></a></span></span></td><td style="text-align: left;"><p><span data-ttu-id="d0551-118">Charge une texture à partir d’un fichier et avertit l’hôte de façon asynchrone lorsqu’il se termine.</span><span class="sxs-lookup"><span data-stu-id="d0551-118">Loads a texture from a file and notifies the host asynchronously when it completes.</span></span></p></td></tr><tr class="even"><td style="text-align: left;"><span data-ttu-id="d0551-119"><a href="/windows/desktop/direct3dtools/ipixengine5-loadtexturesliceasync-uint-pixenginetexturesliceindex-int-bstr-ipixengine5callbacks-ptr-dword-dword"><strong>LoadTextureSliceAsync</strong></a></span><span class="sxs-lookup"><span data-stu-id="d0551-119"><a href="/windows/desktop/direct3dtools/ipixengine5-loadtexturesliceasync-uint-pixenginetexturesliceindex-int-bstr-ipixengine5callbacks-ptr-dword-dword"><strong>LoadTextureSliceAsync</strong></a></span></span></td><td style="text-align: left;"><p><span data-ttu-id="d0551-120">Charge une tranche de texture et avertit l’hôte asynchrnously lorsqu’il se termine.</span><span class="sxs-lookup"><span data-stu-id="d0551-120">Loads a texture slice and notifies the host asynchrnously when it completes.</span></span></p></td></tr><tr class="odd"><td style="text-align: left;"><span data-ttu-id="d0551-121"><a href="/windows/desktop/direct3dtools/ipixengine5-readtexelvalueasync-uint-pixenginetexturesliceindex-int-int-int-ipixengine5callbacks-ptr-dword-dword"><strong>ReadTexelValueAsync</strong></a></span><span class="sxs-lookup"><span data-stu-id="d0551-121"><a href="/windows/desktop/direct3dtools/ipixengine5-readtexelvalueasync-uint-pixenginetexturesliceindex-int-int-int-ipixengine5callbacks-ptr-dword-dword"><strong>ReadTexelValueAsync</strong></a></span></span></td><td style="text-align: left;"><p><span data-ttu-id="d0551-122">Lit une valeur Texel et retourne le résultat au asynchrnously hôte.</span><span class="sxs-lookup"><span data-stu-id="d0551-122">Reads a texel value and returns the result to the host asynchrnously.</span></span></p></td></tr><tr class="even"><td style="text-align: left;"><span data-ttu-id="d0551-123"><a href="/previous-versions/windows/desktop/legacy/mt432769(v=vs.85)"><strong>RenderTextureAsync</strong></a></span><span class="sxs-lookup"><span data-stu-id="d0551-123"><a href="/previous-versions/windows/desktop/legacy/mt432769(v=vs.85)"><strong>RenderTextureAsync</strong></a></span></span></td><td style="text-align: left;"><p><span data-ttu-id="d0551-124">Génère le rendu d’une texture dans un fichier et retourne le résultat à l’hôte asynchrnously.</span><span class="sxs-lookup"><span data-stu-id="d0551-124">Renders a texture to a file and returns the result to the host asynchrnously.</span></span></p></td></tr><tr class="odd"><td style="text-align: left;"><span data-ttu-id="d0551-125"><a href="/windows/desktop/direct3dtools/ipixengine5-savetextureasync-uint-bstr-ipixengine5callbacks-ptr-dword-dword"><strong>SaveTextureAsync</strong></a></span><span class="sxs-lookup"><span data-stu-id="d0551-125"><a href="/windows/desktop/direct3dtools/ipixengine5-savetextureasync-uint-bstr-ipixengine5callbacks-ptr-dword-dword"><strong>SaveTextureAsync</strong></a></span></span></td><td style="text-align: left;"><p><span data-ttu-id="d0551-126">Enregistre une texture.</span><span class="sxs-lookup"><span data-stu-id="d0551-126">Saves a texture.</span></span></p></td></tr></tbody></table>

 

## <a name="requirements"></a><span data-ttu-id="d0551-127">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="d0551-127">Requirements</span></span>

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><tbody><tr class="odd"><td><p><span data-ttu-id="d0551-128">En-tête</span><span class="sxs-lookup"><span data-stu-id="d0551-128">Header</span></span></p></td><td><span data-ttu-id="d0551-129">Vspixengine. h</span><span class="sxs-lookup"><span data-stu-id="d0551-129">Vspixengine.h</span></span></td></tr></tbody></table>

 

 
