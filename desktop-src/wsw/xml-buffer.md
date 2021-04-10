---
title: Mémoire tampon XML
description: Une mémoire tampon XML fournit un stockage en mémoire efficace pour les données XML arbitraires.
ms.assetid: e379628b-c6f8-48b1-8109-59fb604f2bcb
keywords:
- Services Web de tampon XML pour Windows
- WWSAPI
- WWS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ab71121dc451c9ccb186c754d537836f9e899fa9
ms.sourcegitcommit: a716ca2a6a22a400f02c6b31699cf4da83ee3619
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/04/2020
ms.locfileid: "103941483"
---
# <a name="xml-buffer"></a><span data-ttu-id="223ed-106">Mémoire tampon XML</span><span class="sxs-lookup"><span data-stu-id="223ed-106">XML Buffer</span></span>

<span data-ttu-id="223ed-107">Une mémoire tampon XML fournit un stockage en mémoire efficace pour les données XML arbitraires.</span><span class="sxs-lookup"><span data-stu-id="223ed-107">An XML Buffer provides efficient in-memory storage for arbitrary XML data.</span></span>


<span data-ttu-id="223ed-108">Pour lire des données à partir d’une mémoire tampon XML, utilisez un [lecteur XML](xml-reader.md) et appelez [**WsSetInputToBuffer**](/windows/desktop/api/WebServices/nf-webservices-wssetinputtobuffer) avec la mémoire tampon XML.</span><span class="sxs-lookup"><span data-stu-id="223ed-108">To read data from an XML Buffer, use a [XML Reader](xml-reader.md) and call [**WsSetInputToBuffer**](/windows/desktop/api/WebServices/nf-webservices-wssetinputtobuffer) with the XML Buffer.</span></span> <span data-ttu-id="223ed-109">Le lecteur sera positionné au début du document.</span><span class="sxs-lookup"><span data-stu-id="223ed-109">The reader will be positioned at the start of the document.</span></span>

<span data-ttu-id="223ed-110">Pour insérer des données dans une mémoire tampon, utilisez un [Writer XML](xml-writer.md) et appelez [**WsSetOutputToBuffer**](/windows/desktop/api/WebServices/nf-webservices-wssetoutputtobuffer) avec la mémoire tampon XML.</span><span class="sxs-lookup"><span data-stu-id="223ed-110">To insert data into a buffer, use a [XML Writer](xml-writer.md) and call [**WsSetOutputToBuffer**](/windows/desktop/api/WebServices/nf-webservices-wssetoutputtobuffer) with the XML Buffer.</span></span> <span data-ttu-id="223ed-111">Le writer sera positionné à la fin du document.</span><span class="sxs-lookup"><span data-stu-id="223ed-111">The writer will be positioned at the end of the document.</span></span>

<span data-ttu-id="223ed-112">Une fois qu’un lecteur a été défini sur une mémoire tampon XML, en plus de toutes les API de lecture XML, [**WsMoveReader**](/windows/desktop/api/WebServices/nf-webservices-wsmovereader) peut être utilisé pour parcourir le lecteur à travers le document.</span><span class="sxs-lookup"><span data-stu-id="223ed-112">Once a reader has been set to an XML Buffer, in addition to all of the XML Reader APIs, [**WsMoveReader**](/windows/desktop/api/WebServices/nf-webservices-wsmovereader) may be used to navigate the reader through the document.</span></span> <span data-ttu-id="223ed-113">[**WsGetReaderPosition**](/windows/desktop/api/WebServices/nf-webservices-wsgetreaderposition) et [**WsSetReaderPosition**](/windows/desktop/api/WebServices/nf-webservices-wssetreaderposition) peuvent également être utilisés pour enregistrer une position dans le document et y revenir ultérieurement.</span><span class="sxs-lookup"><span data-stu-id="223ed-113">[**WsGetReaderPosition**](/windows/desktop/api/WebServices/nf-webservices-wsgetreaderposition) and [**WsSetReaderPosition**](/windows/desktop/api/WebServices/nf-webservices-wssetreaderposition) may also be used to record a position in the document and return to it later.</span></span>

<span data-ttu-id="223ed-114">Une fois qu’un enregistreur a été défini sur une mémoire tampon XML, en plus de toutes les API du Writer XML, [**WsMoveWriter**](/windows/desktop/api/WebServices/nf-webservices-wsmovewriter) peut être utilisé pour parcourir l’enregistreur dans le document.</span><span class="sxs-lookup"><span data-stu-id="223ed-114">Once a writer has been set to an XML Buffer, in addition to all of the XML Writer APIs, [**WsMoveWriter**](/windows/desktop/api/WebServices/nf-webservices-wsmovewriter) may be used to navigate the writer through the document.</span></span> <span data-ttu-id="223ed-115">[**WsGetWriterPosition**](/windows/desktop/api/WebServices/nf-webservices-wsgetwriterposition) et [**WsSetWriterPosition**](/windows/desktop/api/WebServices/nf-webservices-wssetwriterposition) peuvent également être utilisés pour enregistrer une position dans le document et y revenir ultérieurement.</span><span class="sxs-lookup"><span data-stu-id="223ed-115">[**WsGetWriterPosition**](/windows/desktop/api/WebServices/nf-webservices-wsgetwriterposition) and [**WsSetWriterPosition**](/windows/desktop/api/WebServices/nf-webservices-wssetwriterposition) may also be used to record a position in the document and return to it later.</span></span> <span data-ttu-id="223ed-116">Le writer insère toujours des données avant le nœud auquel il est positionné.</span><span class="sxs-lookup"><span data-stu-id="223ed-116">The writer always inserts data before the node to which it is positioned.</span></span>

<span data-ttu-id="223ed-117">Les nœuds peuvent être supprimés de la mémoire tampon XML en obtenant la position du nœud à l’aide de [**WsGetReaderPosition**](/windows/desktop/api/WebServices/nf-webservices-wsgetreaderposition) ou [**WsGetWriterPosition**](/windows/desktop/api/WebServices/nf-webservices-wsgetwriterposition) , puis en appelant [**WsRemoveNode**](/windows/desktop/api/WebServices/nf-webservices-wsremovenode) avec cette position.</span><span class="sxs-lookup"><span data-stu-id="223ed-117">Nodes may be deleted from the XML Buffer by obtaining the position of the node using [**WsGetReaderPosition**](/windows/desktop/api/WebServices/nf-webservices-wsgetreaderposition) or [**WsGetWriterPosition**](/windows/desktop/api/WebServices/nf-webservices-wsgetwriterposition) and then calling [**WsRemoveNode**](/windows/desktop/api/WebServices/nf-webservices-wsremovenode) with that position.</span></span> <span data-ttu-id="223ed-118">Pour les éléments, cette opération supprimera l’élément, tous ses enfants, y compris son élément de fin correspondant.</span><span class="sxs-lookup"><span data-stu-id="223ed-118">For elements, this will delete the element, all its children including its matching end element.</span></span>

<span data-ttu-id="223ed-119">Une position est représentée par la valeur de la [**\_ \_ \_ position du nœud XML WS**](/windows/desktop/api/WebServices/ns-webservices-ws_xml_node_position).</span><span class="sxs-lookup"><span data-stu-id="223ed-119">A position is represented by the value [**WS\_XML\_NODE\_POSITION**](/windows/desktop/api/WebServices/ns-webservices-ws_xml_node_position).</span></span> <span data-ttu-id="223ed-120">Les positions sont spécifiques à une mémoire tampon XML particulière et sont uniquement valides tant que la mémoire tampon XML est valide.</span><span class="sxs-lookup"><span data-stu-id="223ed-120">Positions are specific to a particular XML Buffer, and are only valid as long as the XML Buffer is valid.</span></span>

<span data-ttu-id="223ed-121">Les énumérations suivantes sont utilisées avec les mémoires tampons XML :</span><span class="sxs-lookup"><span data-stu-id="223ed-121">The following enumerations are used with XML buffers:</span></span>

-   [<span data-ttu-id="223ed-122">**\_passage \_ de WS à**</span><span class="sxs-lookup"><span data-stu-id="223ed-122">**WS\_MOVE\_TO**</span></span>](/windows/desktop/api/WebServices/ne-webservices-ws_move_to)
-   [<span data-ttu-id="223ed-123">**\_ID de \_ propriété de tampon XML \_ WS \_**</span><span class="sxs-lookup"><span data-stu-id="223ed-123">**WS\_XML\_BUFFER\_PROPERTY\_ID**</span></span>](/windows/win32/api/webservices/ne-webservices-ws_xml_reader_property_id)

<span data-ttu-id="223ed-124">Les fonctions suivantes sont utilisées avec les mémoires tampons XML :</span><span class="sxs-lookup"><span data-stu-id="223ed-124">The following functions are used with XML buffers:</span></span>

-   [<span data-ttu-id="223ed-125">**WsCreateXmlBuffer**</span><span class="sxs-lookup"><span data-stu-id="223ed-125">**WsCreateXmlBuffer**</span></span>](/windows/desktop/api/WebServices/nf-webservices-wscreatexmlbuffer)
-   [<span data-ttu-id="223ed-126">**WsRemoveNode**</span><span class="sxs-lookup"><span data-stu-id="223ed-126">**WsRemoveNode**</span></span>](/windows/desktop/api/WebServices/nf-webservices-wsremovenode)

<span data-ttu-id="223ed-127">Le handle suivant est utilisé avec les mémoires tampons XML :</span><span class="sxs-lookup"><span data-stu-id="223ed-127">The following handle is used with XML buffers:</span></span>

-   [<span data-ttu-id="223ed-128">\_ \_ mémoire tampon XML WS</span><span class="sxs-lookup"><span data-stu-id="223ed-128">WS\_XML\_BUFFER</span></span>](ws-xml-buffer.md)

<span data-ttu-id="223ed-129">Les structures suivantes sont utilisées avec les tampons XML :</span><span class="sxs-lookup"><span data-stu-id="223ed-129">The following structures are used with XML buffers:</span></span>

-   [<span data-ttu-id="223ed-130">**\_propriété de \_ tampon \_ XML WS**</span><span class="sxs-lookup"><span data-stu-id="223ed-130">**WS\_XML\_BUFFER\_PROPERTY**</span></span>](/windows/desktop/api/WebServices/ns-webservices-ws_xml_buffer_property)
-   [<span data-ttu-id="223ed-131">**\_position du \_ nœud \_ XML WS**</span><span class="sxs-lookup"><span data-stu-id="223ed-131">**WS\_XML\_NODE\_POSITION**</span></span>](/windows/desktop/api/WebServices/ns-webservices-ws_xml_node_position)

 

 




