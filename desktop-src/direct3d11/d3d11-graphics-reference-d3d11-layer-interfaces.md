---
title: Interfaces de couche
description: Cette section contient des informations sur les interfaces de couche.
ms.assetid: 100cb66a-9bf5-4d0b-9f03-ad7c00e76d9d
keywords:
- interfaces, couche Direct3D 11
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a57945866e8dea1b04c4066362105c8ac6e259a5
ms.sourcegitcommit: a716ca2a6a22a400f02c6b31699cf4da83ee3619
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/04/2020
ms.locfileid: "104991041"
---
# <a name="layer-interfaces"></a><span data-ttu-id="fa999-104">Interfaces de couche</span><span class="sxs-lookup"><span data-stu-id="fa999-104">Layer Interfaces</span></span>

<span data-ttu-id="fa999-105">Cette section contient des informations sur les interfaces de couche.</span><span class="sxs-lookup"><span data-stu-id="fa999-105">This section contains information about the layer interfaces.</span></span>


## <a name="in-this-section"></a><span data-ttu-id="fa999-106">Contenu de cette section</span><span class="sxs-lookup"><span data-stu-id="fa999-106">In this section</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="fa999-107">Rubrique</span><span class="sxs-lookup"><span data-stu-id="fa999-107">Topic</span></span></th>
<th><span data-ttu-id="fa999-108">Description</span><span class="sxs-lookup"><span data-stu-id="fa999-108">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="fa999-109"><a href="/windows/desktop/api/D3D11SDKLayers/nn-d3d11sdklayers-id3d11debug"><strong>ID3D11Debug</strong></a></span><span class="sxs-lookup"><span data-stu-id="fa999-109"><a href="/windows/desktop/api/D3D11SDKLayers/nn-d3d11sdklayers-id3d11debug"><strong>ID3D11Debug</strong></a></span></span><br/></td>
<td><span data-ttu-id="fa999-110">Une interface de débogage contrôle les paramètres de débogage, valide l’état du pipeline et ne peut être utilisée que si la couche de débogage est activée.</span><span class="sxs-lookup"><span data-stu-id="fa999-110">A debug interface controls debug settings, validates pipeline state and can only be used if the debug layer is turned on.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="fa999-111"><a href="/windows/desktop/api/D3D11SDKLayers/nn-d3d11sdklayers-id3d11infoqueue"><strong>ID3D11InfoQueue</strong></a></span><span class="sxs-lookup"><span data-stu-id="fa999-111"><a href="/windows/desktop/api/D3D11SDKLayers/nn-d3d11sdklayers-id3d11infoqueue"><strong>ID3D11InfoQueue</strong></a></span></span><br/></td>
<td><span data-ttu-id="fa999-112">Une interface d’informations de file d’attente stocke, récupère et filtre les messages de débogage.</span><span class="sxs-lookup"><span data-stu-id="fa999-112">An information-queue interface stores, retrieves, and filters debug messages.</span></span> <span data-ttu-id="fa999-113">La file d’attente se compose d’une file d’attente de messages, d’une pile de filtres de stockage facultative et d’une pile de filtres de récupération facultative.</span><span class="sxs-lookup"><span data-stu-id="fa999-113">The queue consists of a message queue, an optional storage filter stack, and a optional retrieval filter stack.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="fa999-114"><a href="/windows/desktop/api/D3D11SDKLayers/nn-d3d11sdklayers-id3d11refdefaulttrackingoptions"><strong>ID3D11RefDefaultTrackingOptions</strong></a></span><span class="sxs-lookup"><span data-stu-id="fa999-114"><a href="/windows/desktop/api/D3D11SDKLayers/nn-d3d11sdklayers-id3d11refdefaulttrackingoptions"><strong>ID3D11RefDefaultTrackingOptions</strong></a></span></span><br/></td>
<td><span data-ttu-id="fa999-115">L’interface de suivi par défaut définit les options de suivi par défaut.</span><span class="sxs-lookup"><span data-stu-id="fa999-115">The default tracking interface sets reference default tracking options.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="fa999-116"><a href="/windows/desktop/api/D3D11SDKLayers/nn-d3d11sdklayers-id3d11reftrackingoptions"><strong>ID3D11RefTrackingOptions</strong></a></span><span class="sxs-lookup"><span data-stu-id="fa999-116"><a href="/windows/desktop/api/D3D11SDKLayers/nn-d3d11sdklayers-id3d11reftrackingoptions"><strong>ID3D11RefTrackingOptions</strong></a></span></span><br/></td>
<td><span data-ttu-id="fa999-117">L’interface de suivi définit les options de suivi de référence.</span><span class="sxs-lookup"><span data-stu-id="fa999-117">The tracking interface sets reference tracking options.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="fa999-118"><a href="/windows/desktop/api/D3D11SDKLayers/nn-d3d11sdklayers-id3d11switchtoref"><strong>ID3D11SwitchToRef</strong></a></span><span class="sxs-lookup"><span data-stu-id="fa999-118"><a href="/windows/desktop/api/D3D11SDKLayers/nn-d3d11sdklayers-id3d11switchtoref"><strong>ID3D11SwitchToRef</strong></a></span></span><br/></td>
<td><blockquote>
[!Note]<br />
<span data-ttu-id="fa999-119">L’interface <a href="/windows/desktop/api/D3D11SDKLayers/nn-d3d11sdklayers-id3d11switchtoref"><strong>ID3D11SwitchToRef</strong></a> et ses méthodes ne sont pas prises en charge dans Direct3D 11.</span><span class="sxs-lookup"><span data-stu-id="fa999-119">The <a href="/windows/desktop/api/D3D11SDKLayers/nn-d3d11sdklayers-id3d11switchtoref"><strong>ID3D11SwitchToRef</strong></a> interface and its methods are not supported in Direct3D 11.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="fa999-120"><a href="/windows/desktop/api/D3D11SDKLayers/nn-d3d11sdklayers-id3d11tracingdevice"><strong>ID3D11TracingDevice</strong></a></span><span class="sxs-lookup"><span data-stu-id="fa999-120"><a href="/windows/desktop/api/D3D11SDKLayers/nn-d3d11sdklayers-id3d11tracingdevice"><strong>ID3D11TracingDevice</strong></a></span></span><br/></td>
<td><span data-ttu-id="fa999-121">L’interface du dispositif de suivi définit les informations de suivi du nuanceur, ce qui permet une journalisation précise et une lecture de l’exécution du nuanceur.</span><span class="sxs-lookup"><span data-stu-id="fa999-121">The tracing device interface sets shader tracking information, which enables accurate logging and playback of shader execution.</span></span><br/></td>
</tr>
</tbody>
</table>



 

## <a name="related-topics"></a><span data-ttu-id="fa999-122">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="fa999-122">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="fa999-123">Référence de couche</span><span class="sxs-lookup"><span data-stu-id="fa999-123">Layer Reference</span></span>](d3d11-graphics-reference-d3d11-layer.md)
</dt> </dl>

 

 





