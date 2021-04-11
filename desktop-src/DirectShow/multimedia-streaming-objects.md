---
description: Objets de streaming multimédia
ms.assetid: 4f5460db-2670-41af-a57f-20cf706827e6
title: Objets de streaming multimédia
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 05762e4a3d7aa486b8a22b73905fc5d9c1610078
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/03/2021
ms.locfileid: "104321650"
---
# <a name="multimedia-streaming-objects"></a><span data-ttu-id="3c951-103">Objets de streaming multimédia</span><span class="sxs-lookup"><span data-stu-id="3c951-103">Multimedia Streaming Objects</span></span>

> [!Note]  
> <span data-ttu-id="3c951-104">Cette API est déconseillée.</span><span class="sxs-lookup"><span data-stu-id="3c951-104">This API is deprecated.</span></span> <span data-ttu-id="3c951-105">Les nouvelles applications ne doivent pas l’utiliser.</span><span class="sxs-lookup"><span data-stu-id="3c951-105">New applications should not use it.</span></span>

 

<span data-ttu-id="3c951-106">Le tableau suivant décrit les objets de diffusion multimédia en continu.</span><span class="sxs-lookup"><span data-stu-id="3c951-106">The following table describes the multimedia streaming objects.</span></span>



<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="3c951-107">CLSID</span><span class="sxs-lookup"><span data-stu-id="3c951-107">CLSID</span></span></th>
<th><span data-ttu-id="3c951-108">Description</span><span class="sxs-lookup"><span data-stu-id="3c951-108">Description</span></span></th>
<th><span data-ttu-id="3c951-109">Interfaces prises en charge</span><span class="sxs-lookup"><span data-stu-id="3c951-109">Interfaces supported</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="3c951-110">CLSID_AMMediaTypeStream</span><span class="sxs-lookup"><span data-stu-id="3c951-110">CLSID_AMMediaTypeStream</span></span></td>
<td><span data-ttu-id="3c951-111">Peut créer des exemples de supports pour n’importe quel type de données pris en charge par DirectShow</span><span class="sxs-lookup"><span data-stu-id="3c951-111">Can create media samples for any DirectShow-supported data type</span></span></td>
<td><ul>
<li><span data-ttu-id="3c951-112"><a href="/previous-versions/windows/desktop/api/amstream/nn-amstream-iammediastream"><strong>IAMMediaStream</strong></a></span><span class="sxs-lookup"><span data-stu-id="3c951-112"><a href="/previous-versions/windows/desktop/api/amstream/nn-amstream-iammediastream"><strong>IAMMediaStream</strong></a></span></span></li>
<li><span data-ttu-id="3c951-113"><a href="/previous-versions/windows/desktop/api/mmstream/nn-mmstream-imediastream"><strong>IMediaStream</strong></a></span><span class="sxs-lookup"><span data-stu-id="3c951-113"><a href="/previous-versions/windows/desktop/api/mmstream/nn-mmstream-imediastream"><strong>IMediaStream</strong></a></span></span></li>
<li><span data-ttu-id="3c951-114"><a href="/windows/desktop/api/Strmif/nn-strmif-ipin"><strong>IPin</strong></a></span><span class="sxs-lookup"><span data-stu-id="3c951-114"><a href="/windows/desktop/api/Strmif/nn-strmif-ipin"><strong>IPin</strong></a></span></span></li>
<li><span data-ttu-id="3c951-115"><a href="/windows/desktop/api/Strmif/nn-strmif-imeminputpin"><strong>IMemInputPin</strong></a></span><span class="sxs-lookup"><span data-stu-id="3c951-115"><a href="/windows/desktop/api/Strmif/nn-strmif-imeminputpin"><strong>IMemInputPin</strong></a></span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="3c951-116">CLSID_AMAudioData</span><span class="sxs-lookup"><span data-stu-id="3c951-116">CLSID_AMAudioData</span></span></td>
<td><span data-ttu-id="3c951-117">Implémentation de l’objet conteneur audio <a href="/previous-versions/windows/desktop/api/austream/nn-austream-iaudiodata"><strong>IAudioData</strong></a> .</span><span class="sxs-lookup"><span data-stu-id="3c951-117">Implementation of <a href="/previous-versions/windows/desktop/api/austream/nn-austream-iaudiodata"><strong>IAudioData</strong></a> audio container object.</span></span></td>
<td><ul>
<li><span data-ttu-id="3c951-118"><a href="/previous-versions/windows/desktop/api/austream/nn-austream-iaudiodata"><strong>IAudioData</strong></a></span><span class="sxs-lookup"><span data-stu-id="3c951-118"><a href="/previous-versions/windows/desktop/api/austream/nn-austream-iaudiodata"><strong>IAudioData</strong></a></span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="3c951-119">CLSID_AMDirectDrawStream</span><span class="sxs-lookup"><span data-stu-id="3c951-119">CLSID_AMDirectDrawStream</span></span></td>
<td><span data-ttu-id="3c951-120">Flux multimédia DirectDraw qui peut être ajouté à un flux multimédia DirectShow.</span><span class="sxs-lookup"><span data-stu-id="3c951-120">DirectDraw media stream that can be added to a DirectShow multimedia stream.</span></span></td>
<td><ul>
<li><span data-ttu-id="3c951-121"><a href="/previous-versions/windows/desktop/api/amstream/nn-amstream-iammediastream"><strong>IAMMediaStream</strong></a></span><span class="sxs-lookup"><span data-stu-id="3c951-121"><a href="/previous-versions/windows/desktop/api/amstream/nn-amstream-iammediastream"><strong>IAMMediaStream</strong></a></span></span></li>
<li><span data-ttu-id="3c951-122"><a href="/previous-versions/windows/desktop/api/mmstream/nn-mmstream-imediastream"><strong>IMediaStream</strong></a></span><span class="sxs-lookup"><span data-stu-id="3c951-122"><a href="/previous-versions/windows/desktop/api/mmstream/nn-mmstream-imediastream"><strong>IMediaStream</strong></a></span></span></li>
<li><span data-ttu-id="3c951-123"><a href="/previous-versions/windows/desktop/api/ddstream/nn-ddstream-idirectdrawmediastream"><strong>IDirectDrawMediaStream</strong></a></span><span class="sxs-lookup"><span data-stu-id="3c951-123"><a href="/previous-versions/windows/desktop/api/ddstream/nn-ddstream-idirectdrawmediastream"><strong>IDirectDrawMediaStream</strong></a></span></span></li>
<li><span data-ttu-id="3c951-124"><a href="/windows/desktop/api/Strmif/nn-strmif-ipin"><strong>IPin</strong></a></span><span class="sxs-lookup"><span data-stu-id="3c951-124"><a href="/windows/desktop/api/Strmif/nn-strmif-ipin"><strong>IPin</strong></a></span></span></li>
<li><span data-ttu-id="3c951-125"><a href="/windows/desktop/api/Strmif/nn-strmif-imeminputpin"><strong>IMemInputPin</strong></a></span><span class="sxs-lookup"><span data-stu-id="3c951-125"><a href="/windows/desktop/api/Strmif/nn-strmif-imeminputpin"><strong>IMemInputPin</strong></a></span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="3c951-126">CLSID_AMMultiMediaStream</span><span class="sxs-lookup"><span data-stu-id="3c951-126">CLSID_AMMultiMediaStream</span></span></td>
<td><span data-ttu-id="3c951-127">Implémentation DirectShow du flux multimédia.</span><span class="sxs-lookup"><span data-stu-id="3c951-127">DirectShow implementation of multimedia stream.</span></span></td>
<td><ul>
<li><span data-ttu-id="3c951-128"><a href="/previous-versions/windows/desktop/api/amstream/nn-amstream-iammultimediastream"><strong>IAMMultiMediaStream</strong></a></span><span class="sxs-lookup"><span data-stu-id="3c951-128"><a href="/previous-versions/windows/desktop/api/amstream/nn-amstream-iammultimediastream"><strong>IAMMultiMediaStream</strong></a></span></span></li>
<li><span data-ttu-id="3c951-129"><a href="/previous-versions/windows/desktop/api/mmstream/nn-mmstream-imultimediastream"><strong>IMultiMediaStream</strong></a></span><span class="sxs-lookup"><span data-stu-id="3c951-129"><a href="/previous-versions/windows/desktop/api/mmstream/nn-mmstream-imultimediastream"><strong>IMultiMediaStream</strong></a></span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="3c951-130">CLSID_MediaStreamFilter</span><span class="sxs-lookup"><span data-stu-id="3c951-130">CLSID_MediaStreamFilter</span></span></td>
<td><span data-ttu-id="3c951-131">Fournit la fonctionnalité de diffusion multimédia en continu pour l’objet CLSID_AMMultiMediaStream par le biais de l’interface <a href="/previous-versions/windows/desktop/api/amstream/nn-amstream-iammultimediastream"><strong>IAMMultiMediaStream</strong></a> .</span><span class="sxs-lookup"><span data-stu-id="3c951-131">Provides multimedia streaming functionality for the CLSID_AMMultiMediaStream object through the <a href="/previous-versions/windows/desktop/api/amstream/nn-amstream-iammultimediastream"><strong>IAMMultiMediaStream</strong></a> interface.</span></span></td>
<td><ul>
<li><span data-ttu-id="3c951-132"><a href="/windows/desktop/api/Strmif/nn-strmif-ibasefilter"><strong>IBaseFilter</strong></a></span><span class="sxs-lookup"><span data-stu-id="3c951-132"><a href="/windows/desktop/api/Strmif/nn-strmif-ibasefilter"><strong>IBaseFilter</strong></a></span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="3c951-133">N/A</span><span class="sxs-lookup"><span data-stu-id="3c951-133">N/A</span></span></td>
<td><span data-ttu-id="3c951-134">Exemples créés par l’objet CLSID_AMMediaTypeStream.</span><span class="sxs-lookup"><span data-stu-id="3c951-134">Samples created by the CLSID_AMMediaTypeStream object.</span></span></td>
<td><ul>
<li><span data-ttu-id="3c951-135"><a href="/previous-versions/windows/desktop/api/mmstream/nn-mmstream-istreamsample"><strong>IStreamSample</strong></a></span><span class="sxs-lookup"><span data-stu-id="3c951-135"><a href="/previous-versions/windows/desktop/api/mmstream/nn-mmstream-istreamsample"><strong>IStreamSample</strong></a></span></span></li>
<li><span data-ttu-id="3c951-136"><a href="/windows/desktop/api/Strmif/nn-strmif-imediasample"><strong>IMediaSample</strong></a></span><span class="sxs-lookup"><span data-stu-id="3c951-136"><a href="/windows/desktop/api/Strmif/nn-strmif-imediasample"><strong>IMediaSample</strong></a></span></span></li>
<li><span data-ttu-id="3c951-137"><a href="/windows/desktop/api/Strmif/nn-strmif-imediasample2"><strong>IMediaSample2</strong></a></span><span class="sxs-lookup"><span data-stu-id="3c951-137"><a href="/windows/desktop/api/Strmif/nn-strmif-imediasample2"><strong>IMediaSample2</strong></a></span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="3c951-138">N/A</span><span class="sxs-lookup"><span data-stu-id="3c951-138">N/A</span></span></td>
<td><span data-ttu-id="3c951-139">Exemples créés par le flux DirectDraw.</span><span class="sxs-lookup"><span data-stu-id="3c951-139">Samples created by the DirectDraw stream.</span></span></td>
<td><ul>
<li><span data-ttu-id="3c951-140"><a href="/previous-versions/windows/desktop/api/mmstream/nn-mmstream-istreamsample"><strong>IStreamSample</strong></a></span><span class="sxs-lookup"><span data-stu-id="3c951-140"><a href="/previous-versions/windows/desktop/api/mmstream/nn-mmstream-istreamsample"><strong>IStreamSample</strong></a></span></span></li>
<li><span data-ttu-id="3c951-141"><a href="/previous-versions/windows/desktop/api/ddstream/nn-ddstream-idirectdrawstreamsample"><strong>IDirectDrawStreamSample</strong></a></span><span class="sxs-lookup"><span data-stu-id="3c951-141"><a href="/previous-versions/windows/desktop/api/ddstream/nn-ddstream-idirectdrawstreamsample"><strong>IDirectDrawStreamSample</strong></a></span></span></li>
<li><span data-ttu-id="3c951-142"><a href="/windows/desktop/api/Strmif/nn-strmif-imediasample"><strong>IMediaSample</strong></a></span><span class="sxs-lookup"><span data-stu-id="3c951-142"><a href="/windows/desktop/api/Strmif/nn-strmif-imediasample"><strong>IMediaSample</strong></a></span></span></li>
</ul></td>
</tr>
</tbody>
</table>



 

 

 



