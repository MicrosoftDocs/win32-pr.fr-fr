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
# <a name="multimedia-streaming-objects"></a>Objets de streaming multimédia

> [!Note]  
> Cette API est déconseillée. Les nouvelles applications ne doivent pas l’utiliser.

 

Le tableau suivant décrit les objets de diffusion multimédia en continu.



<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th>CLSID</th>
<th>Description</th>
<th>Interfaces prises en charge</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>CLSID_AMMediaTypeStream</td>
<td>Peut créer des exemples de supports pour n’importe quel type de données pris en charge par DirectShow</td>
<td><ul>
<li><a href="/previous-versions/windows/desktop/api/amstream/nn-amstream-iammediastream"><strong>IAMMediaStream</strong></a></li>
<li><a href="/previous-versions/windows/desktop/api/mmstream/nn-mmstream-imediastream"><strong>IMediaStream</strong></a></li>
<li><a href="/windows/desktop/api/Strmif/nn-strmif-ipin"><strong>IPin</strong></a></li>
<li><a href="/windows/desktop/api/Strmif/nn-strmif-imeminputpin"><strong>IMemInputPin</strong></a></li>
</ul></td>
</tr>
<tr class="even">
<td>CLSID_AMAudioData</td>
<td>Implémentation de l’objet conteneur audio <a href="/previous-versions/windows/desktop/api/austream/nn-austream-iaudiodata"><strong>IAudioData</strong></a> .</td>
<td><ul>
<li><a href="/previous-versions/windows/desktop/api/austream/nn-austream-iaudiodata"><strong>IAudioData</strong></a></li>
</ul></td>
</tr>
<tr class="odd">
<td>CLSID_AMDirectDrawStream</td>
<td>Flux multimédia DirectDraw qui peut être ajouté à un flux multimédia DirectShow.</td>
<td><ul>
<li><a href="/previous-versions/windows/desktop/api/amstream/nn-amstream-iammediastream"><strong>IAMMediaStream</strong></a></li>
<li><a href="/previous-versions/windows/desktop/api/mmstream/nn-mmstream-imediastream"><strong>IMediaStream</strong></a></li>
<li><a href="/previous-versions/windows/desktop/api/ddstream/nn-ddstream-idirectdrawmediastream"><strong>IDirectDrawMediaStream</strong></a></li>
<li><a href="/windows/desktop/api/Strmif/nn-strmif-ipin"><strong>IPin</strong></a></li>
<li><a href="/windows/desktop/api/Strmif/nn-strmif-imeminputpin"><strong>IMemInputPin</strong></a></li>
</ul></td>
</tr>
<tr class="even">
<td>CLSID_AMMultiMediaStream</td>
<td>Implémentation DirectShow du flux multimédia.</td>
<td><ul>
<li><a href="/previous-versions/windows/desktop/api/amstream/nn-amstream-iammultimediastream"><strong>IAMMultiMediaStream</strong></a></li>
<li><a href="/previous-versions/windows/desktop/api/mmstream/nn-mmstream-imultimediastream"><strong>IMultiMediaStream</strong></a></li>
</ul></td>
</tr>
<tr class="odd">
<td>CLSID_MediaStreamFilter</td>
<td>Fournit la fonctionnalité de diffusion multimédia en continu pour l’objet CLSID_AMMultiMediaStream par le biais de l’interface <a href="/previous-versions/windows/desktop/api/amstream/nn-amstream-iammultimediastream"><strong>IAMMultiMediaStream</strong></a> .</td>
<td><ul>
<li><a href="/windows/desktop/api/Strmif/nn-strmif-ibasefilter"><strong>IBaseFilter</strong></a></li>
</ul></td>
</tr>
<tr class="even">
<td>N/A</td>
<td>Exemples créés par l’objet CLSID_AMMediaTypeStream.</td>
<td><ul>
<li><a href="/previous-versions/windows/desktop/api/mmstream/nn-mmstream-istreamsample"><strong>IStreamSample</strong></a></li>
<li><a href="/windows/desktop/api/Strmif/nn-strmif-imediasample"><strong>IMediaSample</strong></a></li>
<li><a href="/windows/desktop/api/Strmif/nn-strmif-imediasample2"><strong>IMediaSample2</strong></a></li>
</ul></td>
</tr>
<tr class="odd">
<td>N/A</td>
<td>Exemples créés par le flux DirectDraw.</td>
<td><ul>
<li><a href="/previous-versions/windows/desktop/api/mmstream/nn-mmstream-istreamsample"><strong>IStreamSample</strong></a></li>
<li><a href="/previous-versions/windows/desktop/api/ddstream/nn-ddstream-idirectdrawstreamsample"><strong>IDirectDrawStreamSample</strong></a></li>
<li><a href="/windows/desktop/api/Strmif/nn-strmif-imediasample"><strong>IMediaSample</strong></a></li>
</ul></td>
</tr>
</tbody>
</table>



 

 

 



