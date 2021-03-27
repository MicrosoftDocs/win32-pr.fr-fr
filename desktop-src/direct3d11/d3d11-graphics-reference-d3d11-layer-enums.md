---
title: Énumérations de couche
description: Cette section contient des informations sur les énumérations de couche.
ms.assetid: 0fd0456b-2638-4b4c-8a34-a3e104a1a034
keywords:
- énumérations, couche Direct3D 11
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e1e1cca3fa500a529930c8d0c39005697045d18b
ms.sourcegitcommit: a716ca2a6a22a400f02c6b31699cf4da83ee3619
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/04/2020
ms.locfileid: "104971831"
---
# <a name="layer-enumerations"></a><span data-ttu-id="dc4da-104">Énumérations de couche</span><span class="sxs-lookup"><span data-stu-id="dc4da-104">Layer Enumerations</span></span>

<span data-ttu-id="dc4da-105">Cette section contient des informations sur les énumérations de couche.</span><span class="sxs-lookup"><span data-stu-id="dc4da-105">This section contains information about the layer enumerations.</span></span>


## <a name="in-this-section"></a><span data-ttu-id="dc4da-106">Contenu de cette section</span><span class="sxs-lookup"><span data-stu-id="dc4da-106">In this section</span></span>



| <span data-ttu-id="dc4da-107">Rubrique</span><span class="sxs-lookup"><span data-stu-id="dc4da-107">Topic</span></span>                                                                                             | <span data-ttu-id="dc4da-108">Description</span><span class="sxs-lookup"><span data-stu-id="dc4da-108">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                             |
|---------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="dc4da-109">**\_Catégorie de message d3d11 \_**</span><span class="sxs-lookup"><span data-stu-id="dc4da-109">**D3D11\_MESSAGE\_CATEGORY**</span></span>](/windows/desktop/api/D3D11SDKLayers/ne-d3d11sdklayers-d3d11_message_category)<br/>                             | <span data-ttu-id="dc4da-110">Catégories de messages de débogage.</span><span class="sxs-lookup"><span data-stu-id="dc4da-110">Categories of debug messages.</span></span> <span data-ttu-id="dc4da-111">Cela permet d’identifier la catégorie d’un message lors de l’extraction d’un message avec [**ID3D11InfoQueue :: GetMessage**](/windows/desktop/api/D3D11SDKLayers/nf-d3d11sdklayers-id3d11infoqueue-getmessage) et lors de l’ajout d’un message avec [**ID3D11InfoQueue :: AddMessage**](/windows/desktop/api/D3D11SDKLayers/nf-d3d11sdklayers-id3d11infoqueue-addmessage).</span><span class="sxs-lookup"><span data-stu-id="dc4da-111">This will identify the category of a message when retrieving a message with [**ID3D11InfoQueue::GetMessage**](/windows/desktop/api/D3D11SDKLayers/nf-d3d11sdklayers-id3d11infoqueue-getmessage) and when adding a message with [**ID3D11InfoQueue::AddMessage**](/windows/desktop/api/D3D11SDKLayers/nf-d3d11sdklayers-id3d11infoqueue-addmessage).</span></span> <span data-ttu-id="dc4da-112">Lors de la création d’un [**filtre de file d’attente d’informations**](/windows/desktop/api/D3D11SDKLayers/ns-d3d11sdklayers-d3d11_info_queue_filter), ces valeurs peuvent être utilisées pour autoriser ou refuser les catégories de messages à traverser les filtres de stockage et de récupération.</span><span class="sxs-lookup"><span data-stu-id="dc4da-112">When creating an [**info queue filter**](/windows/desktop/api/D3D11SDKLayers/ns-d3d11sdklayers-d3d11_info_queue_filter), these values can be used to allow or deny any categories of messages to pass through the storage and retrieval filters.</span></span><br/> |
| [<span data-ttu-id="dc4da-113">**\_ID de message d3d11 \_**</span><span class="sxs-lookup"><span data-stu-id="dc4da-113">**D3D11\_MESSAGE\_ID**</span></span>](/windows/desktop/api/D3D11SDKLayers/ne-d3d11sdklayers-d3d11_message_id)<br/>                                         | <span data-ttu-id="dc4da-114">Déboguez les messages pour la configuration d’un filtre de file d’attente d’informations (consultez [**d3d11 \_ info \_ Queue \_ Filter**](/windows/desktop/api/D3D11SDKLayers/ns-d3d11sdklayers-d3d11_info_queue_filter)); Utilisez ces messages pour autoriser ou refuser les catégories de message à traverser les filtres de stockage et de récupération.</span><span class="sxs-lookup"><span data-stu-id="dc4da-114">Debug messages for setting up an info-queue filter (see [**D3D11\_INFO\_QUEUE\_FILTER**](/windows/desktop/api/D3D11SDKLayers/ns-d3d11sdklayers-d3d11_info_queue_filter)); use these messages to allow or deny message categories to pass through the storage and retrieval filters.</span></span> <span data-ttu-id="dc4da-115">Ces ID sont utilisés par des méthodes telles que [**ID3D11InfoQueue :: GetMessage**](/windows/desktop/api/D3D11SDKLayers/nf-d3d11sdklayers-id3d11infoqueue-getmessage) ou [**ID3D11InfoQueue :: AddMessage**](/windows/desktop/api/D3D11SDKLayers/nf-d3d11sdklayers-id3d11infoqueue-addmessage).</span><span class="sxs-lookup"><span data-stu-id="dc4da-115">These IDs are used by methods such as [**ID3D11InfoQueue::GetMessage**](/windows/desktop/api/D3D11SDKLayers/nf-d3d11sdklayers-id3d11infoqueue-getmessage) or [**ID3D11InfoQueue::AddMessage**](/windows/desktop/api/D3D11SDKLayers/nf-d3d11sdklayers-id3d11infoqueue-addmessage).</span></span> <br/>                                                             |
| [<span data-ttu-id="dc4da-116">**\_Gravité du message d3d11 \_**</span><span class="sxs-lookup"><span data-stu-id="dc4da-116">**D3D11\_MESSAGE\_SEVERITY**</span></span>](/windows/desktop/api/D3D11SDKLayers/ne-d3d11sdklayers-d3d11_message_severity)<br/>                             | <span data-ttu-id="dc4da-117">Déboguez les niveaux de gravité des messages pour une file d’attente d’informations.</span><span class="sxs-lookup"><span data-stu-id="dc4da-117">Debug message severity levels for an information queue.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                      |
| [<span data-ttu-id="dc4da-118">**\_Indicateurs d3d11 RLDO \_**</span><span class="sxs-lookup"><span data-stu-id="dc4da-118">**D3D11\_RLDO\_FLAGS**</span></span>](/windows/desktop/api/D3D11SDKLayers/ne-d3d11sdklayers-d3d11_rldo_flags)<br/>                                         | <span data-ttu-id="dc4da-119">Options de la quantité d’informations à signaler sur la durée de vie d’un objet appareil.</span><span class="sxs-lookup"><span data-stu-id="dc4da-119">Options for the amount of information to report about a device object's lifetime.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                            |
| [<span data-ttu-id="dc4da-120">**\_Options de suivi du nuanceur d3d11 \_ \_**</span><span class="sxs-lookup"><span data-stu-id="dc4da-120">**D3D11\_SHADER\_TRACKING\_OPTIONS**</span></span>](/windows/win32/api/d3d11sdklayers/ne-d3d11sdklayers-d3d11_shader_tracking_options)<br/>              | <span data-ttu-id="dc4da-121">Options qui spécifient comment effectuer le suivi du débogage du nuanceur.</span><span class="sxs-lookup"><span data-stu-id="dc4da-121">Options that specify how to perform shader debug tracking.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                   |
| [<span data-ttu-id="dc4da-122">**\_Type de \_ ressource de suivi du NUANCEur d3d11 \_ \_**</span><span class="sxs-lookup"><span data-stu-id="dc4da-122">**D3D11\_SHADER\_TRACKING\_RESOURCE\_TYPE**</span></span>](/windows/desktop/api/D3D11SDKLayers/ne-d3d11sdklayers-d3d11_shader_tracking_resource_type)<br/> | <span data-ttu-id="dc4da-123">Indique les types de ressources à suivre.</span><span class="sxs-lookup"><span data-stu-id="dc4da-123">Indicates which resource types to track.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                                     |



 

## <a name="related-topics"></a><span data-ttu-id="dc4da-124">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="dc4da-124">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="dc4da-125">Référence de couche</span><span class="sxs-lookup"><span data-stu-id="dc4da-125">Layer Reference</span></span>](d3d11-graphics-reference-d3d11-layer.md)
</dt> </dl>

 

 





