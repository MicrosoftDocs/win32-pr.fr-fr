---
title: Vue d’ensemble de la couche XML
description: L’API XML dans WWSAPI est basée sur les objets lecteur XML et Writer XML, qui autorisent la lecture ou l’écriture de documents XML en mode avant uniquement. La couche XML offre à l’application un accès complet et un contrôle sur le contenu des messages.
ms.assetid: 938ca257-fbb8-4569-b791-2148abb1a5a5
keywords:
- Vue d’ensemble des couches XML Services Web pour Windows
- WWSAPI
- WWS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d9b5d062754adea7b48bd42a6a501ce17d0e332b
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103673338"
---
# <a name="xml-layer-overview"></a><span data-ttu-id="63262-107">Vue d’ensemble de la couche XML</span><span class="sxs-lookup"><span data-stu-id="63262-107">XML Layer Overview</span></span>

<span data-ttu-id="63262-108">L’API XML dans WWSAPI est basée sur les objets [lecteur XML](xml-reader.md) et [Writer XML](xml-writer.md) , qui autorisent la lecture ou l’écriture de documents XML en mode avant uniquement.</span><span class="sxs-lookup"><span data-stu-id="63262-108">The XML API in WWSAPI is based on the [XML Reader](xml-reader.md) and [XML Writer](xml-writer.md) objects, which allow reading or writing of XML documents in a forward only fashion.</span></span> <span data-ttu-id="63262-109">La couche XML offre à l’application un accès complet et un contrôle sur le contenu des messages.</span><span class="sxs-lookup"><span data-stu-id="63262-109">The XML Layer give the application full access to and control over the content of messages.</span></span>

## <a name="encoding"></a><span data-ttu-id="63262-110">Encodage</span><span class="sxs-lookup"><span data-stu-id="63262-110">Encoding</span></span>

<span data-ttu-id="63262-111">L’API XML prend en charge les documents encodés comme suit :</span><span class="sxs-lookup"><span data-stu-id="63262-111">The XML API supports documents encoded as:</span></span>

-   <span data-ttu-id="63262-112">Texte (UTF-8, UTF-16LE, UTF-16BE)</span><span class="sxs-lookup"><span data-stu-id="63262-112">Text (UTF-8, UTF-16LE, UTF-16BE)</span></span>
-   <span data-ttu-id="63262-113">Binary</span><span class="sxs-lookup"><span data-stu-id="63262-113">Binary</span></span>
-   <span data-ttu-id="63262-114">MTOM</span><span class="sxs-lookup"><span data-stu-id="63262-114">MTOM</span></span>

## <a name="storage"></a><span data-ttu-id="63262-115">Stockage</span><span class="sxs-lookup"><span data-stu-id="63262-115">Storage</span></span>

<span data-ttu-id="63262-116">L’API XML prend en charge le traitement des documents stockés en tant que :</span><span class="sxs-lookup"><span data-stu-id="63262-116">The XML API supports processing documents stored as:</span></span>

-   <span data-ttu-id="63262-117">Une mémoire tampon d’octets encodés</span><span class="sxs-lookup"><span data-stu-id="63262-117">An in-memory buffer of encoded bytes</span></span>
-   <span data-ttu-id="63262-118">Un flux</span><span class="sxs-lookup"><span data-stu-id="63262-118">A stream</span></span>
-   <span data-ttu-id="63262-119">Une [mémoire tampon XML](xml-buffer.md)</span><span class="sxs-lookup"><span data-stu-id="63262-119">An [XML Buffer](xml-buffer.md)</span></span>

<span data-ttu-id="63262-120">Une [mémoire tampon XML](xml-buffer.md) est une représentation en mémoire structurée d’un document XML.</span><span class="sxs-lookup"><span data-stu-id="63262-120">An [XML Buffer](xml-buffer.md) is a structured in-memory representation of an XML document.</span></span> <span data-ttu-id="63262-121">Il s’agit d’une représentation plus efficace qu’un document encodé comme octets.</span><span class="sxs-lookup"><span data-stu-id="63262-121">This is a more efficient representation than a document encoded as bytes.</span></span> <span data-ttu-id="63262-122">Un document XML stocké dans une mémoire tampon XML peut être parcouru, lu ou écrit.</span><span class="sxs-lookup"><span data-stu-id="63262-122">An XML document stored in an An XML Buffer can be navigated, read, or written.</span></span>

## <a name="io"></a><span data-ttu-id="63262-123">E/S</span><span class="sxs-lookup"><span data-stu-id="63262-123">I/O</span></span>

<span data-ttu-id="63262-124">L’API XML n’effectuera jamais d’e/s, sauf si elle est demandée spécifiquement.</span><span class="sxs-lookup"><span data-stu-id="63262-124">The XML API will never perform I/O unless specifically requested.</span></span> <span data-ttu-id="63262-125">En outre, toutes les e/s peuvent être lancées de manière asynchrone.</span><span class="sxs-lookup"><span data-stu-id="63262-125">Furthermore, any I/O may be initiated in an asynchronous fashion.</span></span> <span data-ttu-id="63262-126">Pour plus d’informations sur le traitement asynchrone avec l’API XML, consultez [**WsFillReader**](/windows/desktop/api/WebServices/nf-webservices-wsfillreader) et [**WsFlushWriter**](/windows/desktop/api/WebServices/nf-webservices-wsflushwriter) .</span><span class="sxs-lookup"><span data-stu-id="63262-126">See [**WsFillReader**](/windows/desktop/api/WebServices/nf-webservices-wsfillreader) and [**WsFlushWriter**](/windows/desktop/api/WebServices/nf-webservices-wsflushwriter) for details on asynchronous processing with the XML API.</span></span>

## <a name="processing"></a><span data-ttu-id="63262-127">Traitement en cours</span><span class="sxs-lookup"><span data-stu-id="63262-127">Processing</span></span>

<span data-ttu-id="63262-128">L’API XML a trois niveaux distincts au niveau desquels le document peut être traité.</span><span class="sxs-lookup"><span data-stu-id="63262-128">The XML API has three distinct levels at which the document may be processed.</span></span>

<span data-ttu-id="63262-129">Un document peut être traité à un [**nœud**](/windows/desktop/api/WebServices/ns-webservices-ws_xml_node) à la fois.</span><span class="sxs-lookup"><span data-stu-id="63262-129">A document may be processed a [**node**](/windows/desktop/api/WebServices/ns-webservices-ws_xml_node) at a time.</span></span> <span data-ttu-id="63262-130">Cela offre la gestion la plus fine du contenu XML et fournit une fidélité complète des données du document.</span><span class="sxs-lookup"><span data-stu-id="63262-130">This offers the most fine-grained handling of the XML content, and provides complete fidelity of data from the document.</span></span> <span data-ttu-id="63262-131">À ce niveau, les fonctions [**WsReadNode**](/windows/desktop/api/WebServices/nf-webservices-wsreadnode) et [**WsWriteNode**](/windows/desktop/api/WebServices/nf-webservices-wswritenode) et [**WsCopyNode**](/windows/desktop/api/WebServices/nf-webservices-wscopynode) sont utilisées.</span><span class="sxs-lookup"><span data-stu-id="63262-131">At this level, the functions [**WsReadNode**](/windows/desktop/api/WebServices/nf-webservices-wsreadnode) and [**WsWriteNode**](/windows/desktop/api/WebServices/nf-webservices-wswritenode) and [**WsCopyNode**](/windows/desktop/api/WebServices/nf-webservices-wscopynode) would be used.</span></span>

<span data-ttu-id="63262-132">Le niveau de contrôle suivant est des API telles que [**WsReadStartElement**](/windows/desktop/api/WebServices/nf-webservices-wsreadstartelement), [**WsReadValue**](/windows/desktop/api/WebServices/nf-webservices-wsreadvalue) et [**WsReadEndElement**](/windows/desktop/api/WebServices/nf-webservices-wsreadendelement).</span><span class="sxs-lookup"><span data-stu-id="63262-132">The next level of control are APIs like [**WsReadStartElement**](/windows/desktop/api/WebServices/nf-webservices-wsreadstartelement), [**WsReadValue**](/windows/desktop/api/WebServices/nf-webservices-wsreadvalue) and [**WsReadEndElement**](/windows/desktop/api/WebServices/nf-webservices-wsreadendelement).</span></span> <span data-ttu-id="63262-133">Ces API fournissent de nombreux genres de validation, ignorent l’espace blanc et les commentaires, et normalisent le texte et CDATA pour présenter le consommateur avec une vue plus simple du code XML.</span><span class="sxs-lookup"><span data-stu-id="63262-133">These APIs provide numerous kinds of validation, skip whitespace and comments, and normalize text and CDATA to present the consumer with a simpler view of the xml.</span></span>

<span data-ttu-id="63262-134">Le niveau de contrôle le plus élevé consiste à utiliser l’API de sérialisation.</span><span class="sxs-lookup"><span data-stu-id="63262-134">The highest level of control is to use the Serialization API.</span></span> <span data-ttu-id="63262-135">Ces API sont basées sur un mappage entre les types de données C et XML, et peuvent lire ou écrire une structure en mémoire complexe dans XML et en retour avec une fonction unique comme [**WsWriteElement**](/windows/desktop/api/WebServices/nf-webservices-wswriteelement) et [**WsReadElement**](/windows/desktop/api/WebServices/nf-webservices-wsreadelement).</span><span class="sxs-lookup"><span data-stu-id="63262-135">These APIs are driven off a mapping between C data types and XML, and can read or write a complex in-memory structure to xml and back with a single function like [**WsWriteElement**](/windows/desktop/api/WebServices/nf-webservices-wswriteelement) and [**WsReadElement**](/windows/desktop/api/WebServices/nf-webservices-wsreadelement).</span></span>

<span data-ttu-id="63262-136">Les API de canonisation XML peuvent être utilisées pour générer une forme canonique de code XML qui peut à son tour être utilisée pour générer des signatures de chiffrement sur du contenu XML.</span><span class="sxs-lookup"><span data-stu-id="63262-136">The XML Canonicalization APIs may be used to generate a canonical form of XML which may in turn be used for generating cryptographic signatures over XML content.</span></span>

## <a name="creating-a-writer"></a><span data-ttu-id="63262-137">Création d’un enregistreur</span><span class="sxs-lookup"><span data-stu-id="63262-137">Creating a writer</span></span>

<span data-ttu-id="63262-138">Pour créer et utiliser un enregistreur pour écrire dans une mémoire tampon :</span><span class="sxs-lookup"><span data-stu-id="63262-138">To create and use a writer to write to an in-memory buffer:</span></span>

``` syntax
WsCreateWriter              // Create an instance of a WS_XML_WRITER
// Initialize a WS_XML_WRITER_BUFFER_OUTPUT
WsSetOutput                 // Set the encoding and output of the writer along with any other writer properties
// Write Elements
WsGetWriterProperty(..., WS_XML_WRITER_PROPERTY_BYTES, ...)  // Get the generated bytes as a single byte array
// Use the generated bytes
WsFreeWriter                // Free the writer
```

<span data-ttu-id="63262-139">Pour créer et utiliser un enregistreur pour écrire dans un flux :</span><span class="sxs-lookup"><span data-stu-id="63262-139">To create and use a writer to write to a stream:</span></span>

``` syntax
WsCreateWriter              // Create an instance of a WS_XML_WRITER
// Initialize a WS_XML_WRITER_STREAM_OUTPUT
WsSetOutput                 // Set the encoding and output of the writer along with any other writer properties
// Write Elements
WsFlushWriter               // Force any buffered data to be written
WsFreeWriter                // Free the writer
```

<span data-ttu-id="63262-140">Pour créer et utiliser un enregistreur pour écrire dans une [ \_ \_ mémoire tampon XML WS](ws-xml-buffer.md):</span><span class="sxs-lookup"><span data-stu-id="63262-140">To create and use a writer to write to a [WS\_XML\_BUFFER](ws-xml-buffer.md):</span></span>

``` syntax
WsCreateXmlBuffer           // Create the buffer to write to
WsCreateWriter              // Create an instance of a WS_XML_WRITER
WsSetOutputToBuffer         // Set the output buffer along with any other writer properties
// Write Elements
WsFreeWriter                // Free the writer
// The buffer has the generated document
```

<span data-ttu-id="63262-141">Dans tous les cas, il est possible d’inclure le retrait de propriété du [**\_ \_ writer \_ \_ XML**](/windows/desktop/api/WebServices/ne-webservices-ws_xml_writer_property_id) de la propriété pour mettre en forme le code XML.</span><span class="sxs-lookup"><span data-stu-id="63262-141">In all cases, the property [**WS\_XML\_WRITER\_PROPERTY\_INDENT**](/windows/desktop/api/WebServices/ne-webservices-ws_xml_writer_property_id) may be included to format the xml.</span></span>

## <a name="writing-elements"></a><span data-ttu-id="63262-142">Écriture d'éléments</span><span class="sxs-lookup"><span data-stu-id="63262-142">Writing Elements</span></span>

<span data-ttu-id="63262-143">Pour écrire un élément dans un enregistreur :</span><span class="sxs-lookup"><span data-stu-id="63262-143">To write an element to a writer:</span></span>

``` syntax
WsWriteStartElement          // Write a start element
for each attribute
{
// Write an attribute using either
WsWriteStartAttribute    // Write a start attribute
// Write Content
WsWriteEndAttribute      // Write an end attribute
// Or one of the following
WsWriteXmlnsAttribute    // Write an explicit xmlns attribute
}
// Write Elements or Content
WsWriteEndElement
```

<span data-ttu-id="63262-144">Vous pouvez également utiliser les éléments suivants :</span><span class="sxs-lookup"><span data-stu-id="63262-144">The following may also be used:</span></span>

``` syntax
WsWriteArray                 // Write an array of primitive values as a series of repeated elements
```

## <a name="writing-content"></a><span data-ttu-id="63262-145">Écriture de contenu</span><span class="sxs-lookup"><span data-stu-id="63262-145">Writing Content</span></span>

<span data-ttu-id="63262-146">Pour écrire du contenu dans un élément ou un attribut, les éléments suivants peuvent être utilisés :</span><span class="sxs-lookup"><span data-stu-id="63262-146">To write content to an element or attribute, the following may be used:</span></span>

``` syntax
WsWriteChars                 // Write unicode characters from memory
WsWriteCharsUtf8             // Write UTF-8 encoded characters from memory
WsWriteBytes                 // Write binary data encoded as base64
WsPushBytes                  // Direct the writer to request that bytes be written
WsPullBytes                  // Direct the writer to read the bytes to be written
WsWriteValue                 // Write primitive values such as ints and BOOLs
WsWriteText                  // Write an WS_XML_TEXT
WsWriteQualifiedName         // Write a qualified name
```

<span data-ttu-id="63262-147">Les éléments suivants peuvent être utilisés pour écrire dans un document, mais ils ne peuvent pas être utilisés dans un attribut.</span><span class="sxs-lookup"><span data-stu-id="63262-147">The following can be used to write to a document, but may not be used when within an attribute.</span></span>

``` syntax
WsWriteNode                  // Write a single WS_XML_NODE
WsCopyNode                   // Copy a single node, or an entire WS_XML_ELEMENT_NODE and children from an WS_XML_READER
```

<span data-ttu-id="63262-148">Les éléments suivants peuvent être utilisés pour écrire une section CDATA dans un document texte :</span><span class="sxs-lookup"><span data-stu-id="63262-148">The following may be used to write a CDATA section in a text document:</span></span>

``` syntax
WsWriteStartCData            // Start a CDATA section in a text encoding
// Write Content
WsWriteEndCData              // End a CDATA section in text encoding
```

## <a name="miscellaneous"></a><span data-ttu-id="63262-149">Divers</span><span class="sxs-lookup"><span data-stu-id="63262-149">Miscellaneous</span></span>

``` syntax
WsGetPrefixFromNamespace     // Find a prefix bound to a namespace
```

## <a name="creating-a-reader"></a><span data-ttu-id="63262-150">Création d’un lecteur</span><span class="sxs-lookup"><span data-stu-id="63262-150">Creating a reader</span></span>

<span data-ttu-id="63262-151">Pour créer et utiliser un lecteur pour lire à partir d’une mémoire tampon en mémoire :</span><span class="sxs-lookup"><span data-stu-id="63262-151">To create and use a reader to read from an in-memory buffer:</span></span>

``` syntax
WsCreateReader              // Create an instance of a WS_XML_READER
// Initialize a WS_XML_READER_BUFFER_INPUT
WsSetInput                  // Set the encoding and input of the reader along with any other reader properties
// Read Elements
WsFreeReader                // Free the reader
```

<span data-ttu-id="63262-152">Pour créer et utiliser un lecteur pour effectuer un lecteur à partir d’un flux :</span><span class="sxs-lookup"><span data-stu-id="63262-152">To create and use a reader to reader from a stream:</span></span>

``` syntax
WsCreateReader              // Create an instance of a WS_XML_READER
// Initialize a WS_XML_READER_STREAM_INPUT
WsSetInput                  // Set the encoding and input of the reader along with any other reader properties
WsFillReader                // Populate the reader with data from the underlying stream
// Read Elements
WsFreeReader                // Free the reader
```

<span data-ttu-id="63262-153">Pour créer et utiliser un lecteur pour lire à partir d’une [ \_ \_ mémoire tampon XML WS](ws-xml-buffer.md):</span><span class="sxs-lookup"><span data-stu-id="63262-153">To create and use a reader to read from a [WS\_XML\_BUFFER](ws-xml-buffer.md):</span></span>

``` syntax
WsCreateXmlBuffer           // Create the buffer to write to
WsCreateReader              // Create an instance of a WS_XML_READER
WsSetInputToBuffer          // Set the input buffer along with any other reader properties
// Read Elements
WsFreeReader                // Free the reader
```

## <a name="reading-elements"></a><span data-ttu-id="63262-154">Lecture d'éléments</span><span class="sxs-lookup"><span data-stu-id="63262-154">Reading Elements</span></span>

<span data-ttu-id="63262-155">Pour lire un élément d’un lecteur :</span><span class="sxs-lookup"><span data-stu-id="63262-155">To read an element from a reader:</span></span>

``` syntax
WsReadToStartElement         // Skip whitespace and comments to position the reader on a specific element
for each attribute of interest
{
WsFindAttribute          // Try Locate the attribute
if (found)
{
WsReadStartAttribute // Set the reader to read the attribute
// Read Content
WsReadEndAttribute   // Return the reader to the element
}
}
WsReadStartElement           // Advance the reader past the current element
// Read Elements or Content
WsWriteEndElement            // Advance the reader past the corresponding end element
```

<span data-ttu-id="63262-156">Vous pouvez également utiliser les éléments suivants :</span><span class="sxs-lookup"><span data-stu-id="63262-156">The following may also be used:</span></span>

``` syntax
WsReadArray                  // Read an array of primitive values as a series of repeated elements
```

## <a name="reading-content"></a><span data-ttu-id="63262-157">Lecture du contenu</span><span class="sxs-lookup"><span data-stu-id="63262-157">Reading Content</span></span>

<span data-ttu-id="63262-158">Pour lire le contenu d’un élément ou d’un attribut, les éléments suivants peuvent être utilisés :</span><span class="sxs-lookup"><span data-stu-id="63262-158">To read content from an element or attribute, the following may be used:</span></span>

``` syntax
WsReadChars                 // Read characters to memory as unicode
WsReadCharsUtf8             // Read characters to memory encoded as UTF-8
WsReadBytes                 // Read binary data encoded as base64
WsReadValue                 // Read primitive values such as ints and BOOLs
WsReadQualifiedName         // Read a qualified name
```

<span data-ttu-id="63262-159">Les éléments suivants peuvent être utilisés pour inspecter le nœud actuel sur lequel le lecteur est positionné :</span><span class="sxs-lookup"><span data-stu-id="63262-159">The following may be used to inspect the current node the reader is positioned on:</span></span>

``` syntax
WsGetReaderNode             // Get the current node
```

## <a name="using-a-buffer"></a><span data-ttu-id="63262-160">Utilisation d’une mémoire tampon</span><span class="sxs-lookup"><span data-stu-id="63262-160">Using a buffer</span></span>

<span data-ttu-id="63262-161">Lors de l’écriture dans une [ \_ \_ mémoire tampon XML WS](ws-xml-buffer.md) , les éléments suivants peuvent être utilisés :</span><span class="sxs-lookup"><span data-stu-id="63262-161">When writing to a [WS\_XML\_BUFFER](ws-xml-buffer.md) the following may be used:</span></span>

``` syntax
WsGetWriterPosition          // Get the current position of the writer in the document
WsSetWriterPosition          // Set the current position of the writer in the document
WsMoveWriter                 // Move relative to the current position in the document
WsRemoveNode                 // Delete an element or text from a document
```

<span data-ttu-id="63262-162">Lors de la lecture à partir d’une [ \_ \_ mémoire tampon XML WS](ws-xml-buffer.md) , les éléments suivants peuvent être utilisés :</span><span class="sxs-lookup"><span data-stu-id="63262-162">When reading from a [WS\_XML\_BUFFER](ws-xml-buffer.md) the following may be used:</span></span>

``` syntax
WsGetReaderPosition          // Get the current position of the reader in the document
WsSetReaderPosition          // Set the current position of the reader in the document
WsMoveReader                 // Move relative to the current position in the document
```

<span data-ttu-id="63262-163">Les éléments suivants peuvent être utilisés pour modifier [une \_ \_ mémoire tampon XML WS](ws-xml-buffer.md):</span><span class="sxs-lookup"><span data-stu-id="63262-163">The following may be used to modify a [WS\_XML\_BUFFER](ws-xml-buffer.md):</span></span>

``` syntax

WsRemoveNode                 // Delete an element or text from a document
```

## <a name="other"></a><span data-ttu-id="63262-164">Autres</span><span class="sxs-lookup"><span data-stu-id="63262-164">Other</span></span>

``` syntax
WsGetNamespaceFromPrefix     // Find a namespace bound to a prefix
WsGetXmlAttribute            // Find an "xml:space" or "xml:lang" attribute in scope
```

 

 




