---
description: Demande d’écriture d’une texture en mosaïques sous la forme d’un fichier DDS.
MS-HAID: vspixengine.ITileRequest
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: Interface ITileRequest
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: DBA493E7-EBB6-490D-BDC6-946265A474D6
api_name:
- ITileRequest
api_type:
- COM
api_location:
- vspixengine.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: ceb630661cfe67bc8beb28b2d1de2480726ec594
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/06/2021
ms.locfileid: "103746804"
---
# <a name="span-idvspixengineitilerequestspanitilerequest-interface"></a><span data-ttu-id="71d6f-103"><span id="vspixengine.itilerequest"></span>Interface ITileRequest</span><span class="sxs-lookup"><span data-stu-id="71d6f-103"><span id="vspixengine.itilerequest"></span>ITileRequest interface</span></span>

<span data-ttu-id="71d6f-104">Demande d’écriture d’une texture en mosaïques sous la forme d’un fichier DDS.</span><span class="sxs-lookup"><span data-stu-id="71d6f-104">Request for a tiled texture to be written as a DDS file.</span></span>

## <a name="members"></a><span data-ttu-id="71d6f-105">Membres</span><span class="sxs-lookup"><span data-stu-id="71d6f-105">Members</span></span>

<span data-ttu-id="71d6f-106">L’interface **ITileRequest** hérite de l’interface [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) .</span><span class="sxs-lookup"><span data-stu-id="71d6f-106">The **ITileRequest** interface inherits from the [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="71d6f-107">**ITileRequest** a également les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="71d6f-107">**ITileRequest** also has these types of members:</span></span>

-   [<span data-ttu-id="71d6f-108">Méthodes</span><span class="sxs-lookup"><span data-stu-id="71d6f-108">Methods</span></span>](#methods)

### <a name="span-idmethodsspanmethods"></a><span data-ttu-id="71d6f-109"><span id="methods"></span>Méthodes</span><span class="sxs-lookup"><span data-stu-id="71d6f-109"><span id="methods"></span>Methods</span></span>

<span data-ttu-id="71d6f-110">L’interface **ITileRequest** possède ces méthodes.</span><span class="sxs-lookup"><span data-stu-id="71d6f-110">The **ITileRequest** interface has these methods.</span></span>

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><thead><tr class="header"><th style="text-align: left;"><span data-ttu-id="71d6f-111">Méthode</span><span class="sxs-lookup"><span data-stu-id="71d6f-111">Method</span></span></th><th style="text-align: left;"><span data-ttu-id="71d6f-112">Description</span><span class="sxs-lookup"><span data-stu-id="71d6f-112">Description</span></span></th></tr></thead><tbody><tr class="odd"><td style="text-align: left;"><span data-ttu-id="71d6f-113"><a href="/windows/desktop/direct3dtools/itilerequest-requestbuffertileasync-eventid-dword-bstr-uint-ibufferobjectdatacallback-ptr-dword-dword"><strong>RequestBufferTileAsync</strong></a></span><span class="sxs-lookup"><span data-stu-id="71d6f-113"><a href="/windows/desktop/direct3dtools/itilerequest-requestbuffertileasync-eventid-dword-bstr-uint-ibufferobjectdatacallback-ptr-dword-dword"><strong>RequestBufferTileAsync</strong></a></span></span></td><td style="text-align: left;"><p><span data-ttu-id="71d6f-114">Demandes pour obtenir le contenu brut d’une vignette.</span><span class="sxs-lookup"><span data-stu-id="71d6f-114">Requests to get the raw contents of a tile.</span></span></p></td></tr><tr class="even"><td style="text-align: left;"><span data-ttu-id="71d6f-115"><a href="/windows/desktop/direct3dtools/itilerequest-requesttexturetileasync-eventid-dword-uint-uint-uint-uint-bstr-itexturecallback-ptr-dword-dword"><strong>RequestTextureTileAsync</strong></a></span><span class="sxs-lookup"><span data-stu-id="71d6f-115"><a href="/windows/desktop/direct3dtools/itilerequest-requesttexturetileasync-eventid-dword-uint-uint-uint-uint-bstr-itexturecallback-ptr-dword-dword"><strong>RequestTextureTileAsync</strong></a></span></span></td><td style="text-align: left;"><p><span data-ttu-id="71d6f-116">Demande à obtenir le contenu d’une texture en mosaïque sous la forme d’un. Fichier DDS (surface DirectDraw).</span><span class="sxs-lookup"><span data-stu-id="71d6f-116">Requests to get the contents of a tiled texture as a .DDS (DirectDraw Surface) file.</span></span></p></td></tr></tbody></table>

 

## <a name="requirements"></a><span data-ttu-id="71d6f-117">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="71d6f-117">Requirements</span></span>

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><tbody><tr class="odd"><td><p><span data-ttu-id="71d6f-118">En-tête</span><span class="sxs-lookup"><span data-stu-id="71d6f-118">Header</span></span></p></td><td><span data-ttu-id="71d6f-119">Vspixengine. h</span><span class="sxs-lookup"><span data-stu-id="71d6f-119">Vspixengine.h</span></span></td></tr></tbody></table>

 

 
