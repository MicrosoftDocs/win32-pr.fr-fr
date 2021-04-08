---
title: Canonisation XML
description: La canonisation XML résout le problème lié à la conversion d’un ensemble de nœuds XML en octets de sorte que les modifications importantes apportées au XML (telles que la modification de l’ordre des attributs dans un élément) ne modifient pas le formulaire d’octet résultant.
ms.assetid: a64303a1-efc4-4c91-ab8d-3e389a655b3e
keywords:
- Services Web de canonisation XML pour Windows
- WWSAPI
- WWS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bab8b1aa00b99b604276a479f1a47aacb5bd8b1e
ms.sourcegitcommit: a716ca2a6a22a400f02c6b31699cf4da83ee3619
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/04/2020
ms.locfileid: "103842901"
---
# <a name="xml-canonicalization"></a><span data-ttu-id="01e1a-106">Canonisation XML</span><span class="sxs-lookup"><span data-stu-id="01e1a-106">XML Canonicalization</span></span>

<span data-ttu-id="01e1a-107">La canonisation XML résout le problème lié à la conversion d’un ensemble de nœuds XML en octets de sorte que les modifications importantes apportées au XML (telles que la modification de l’ordre des attributs dans un élément) ne modifient pas le formulaire d’octet résultant.</span><span class="sxs-lookup"><span data-stu-id="01e1a-107">XML canonicalization solves the problem of converting a set of XML nodes into bytes in such a way that trivial changes to the XML (such as changing the order of attributes in an element) do not change the resulting byte form.</span></span> <span data-ttu-id="01e1a-108">Les octets obtenus à partir de la canonicalisation sont couramment utilisés pour générer une signature de chiffrement sur le contenu XML.</span><span class="sxs-lookup"><span data-stu-id="01e1a-108">The bytes obtained from canonicalization are commonly used to generate a cryptographic signature over XML content.</span></span>


<span data-ttu-id="01e1a-109">Les algorithmes de canonisation XML couramment utilisés normalisent les aspects suivants :</span><span class="sxs-lookup"><span data-stu-id="01e1a-109">The commonly used XML canonicalization algorithms standardize the following aspects:</span></span>

-   <span data-ttu-id="01e1a-110">Encodage de caractères (UTF-8 sans préambule)</span><span class="sxs-lookup"><span data-stu-id="01e1a-110">Character encoding (UTF-8 without preamble)</span></span>
-   <span data-ttu-id="01e1a-111">Sauts de ligne et autres formes de caractères</span><span class="sxs-lookup"><span data-stu-id="01e1a-111">Linefeed and other character forms</span></span>
-   <span data-ttu-id="01e1a-112">Ordre des attributs dans un élément</span><span class="sxs-lookup"><span data-stu-id="01e1a-112">Attribute order in an element</span></span>
-   <span data-ttu-id="01e1a-113">Formulaire d’élément vide</span><span class="sxs-lookup"><span data-stu-id="01e1a-113">Empty element form</span></span>
-   <span data-ttu-id="01e1a-114">Déclaration d’espaces de noms de rendu</span><span class="sxs-lookup"><span data-stu-id="01e1a-114">Rendering namespace declarations</span></span>

<span data-ttu-id="01e1a-115">Les API [**WsStartReaderCanonicalization**](/windows/desktop/api/WebServices/nf-webservices-wsstartreadercanonicalization) et [**WsEndReaderCanonicalization**](/windows/desktop/api/WebServices/nf-webservices-wsendreadercanonicalization) fournissent la fonctionnalité de canonisation XML lors de la lecture d’un document.</span><span class="sxs-lookup"><span data-stu-id="01e1a-115">The APIs [**WsStartReaderCanonicalization**](/windows/desktop/api/WebServices/nf-webservices-wsstartreadercanonicalization) and [**WsEndReaderCanonicalization**](/windows/desktop/api/WebServices/nf-webservices-wsendreadercanonicalization) provide the XML canonicalization functionality while reading a document.</span></span>

<span data-ttu-id="01e1a-116">Les API [**WsStartWriterCanonicalization**](/windows/desktop/api/WebServices/nf-webservices-wsstartwritercanonicalization) et [**WsEndWriterCanonicalization**](/windows/desktop/api/WebServices/nf-webservices-wsendwritercanonicalization) fournissent la fonctionnalité de canonisation XML lors de l’écriture d’un document.</span><span class="sxs-lookup"><span data-stu-id="01e1a-116">The APIs [**WsStartWriterCanonicalization**](/windows/desktop/api/WebServices/nf-webservices-wsstartwritercanonicalization) and [**WsEndWriterCanonicalization**](/windows/desktop/api/WebServices/nf-webservices-wsendwritercanonicalization) provide the XML canonicalization functionality while writing a document.</span></span>

<span data-ttu-id="01e1a-117">Les énumérations suivantes sont utilisées avec la canonisation :</span><span class="sxs-lookup"><span data-stu-id="01e1a-117">The following enumerations are used with canonicalization:</span></span>

-   [<span data-ttu-id="01e1a-118">**\_ \_ algorithme de canonisation WS XML \_**</span><span class="sxs-lookup"><span data-stu-id="01e1a-118">**WS\_XML\_CANONICALIZATION\_ALGORITHM**</span></span>](/windows/desktop/api/WebServices/ne-webservices-ws_xml_canonicalization_algorithm)
-   [<span data-ttu-id="01e1a-119">**\_ID de \_ propriété de canonisation WS XML \_ \_**</span><span class="sxs-lookup"><span data-stu-id="01e1a-119">**WS\_XML\_CANONICALIZATION\_PROPERTY\_ID**</span></span>](/windows/desktop/api/WebServices/ne-webservices-ws_xml_canonicalization_property_id)

<span data-ttu-id="01e1a-120">Les fonctions suivantes sont utilisées avec la canonisation :</span><span class="sxs-lookup"><span data-stu-id="01e1a-120">The following functions are used with canonicalization:</span></span>

-   [<span data-ttu-id="01e1a-121">**WsEndReaderCanonicalization**</span><span class="sxs-lookup"><span data-stu-id="01e1a-121">**WsEndReaderCanonicalization**</span></span>](/windows/desktop/api/WebServices/nf-webservices-wsendreadercanonicalization)
-   [<span data-ttu-id="01e1a-122">**WsEndWriterCanonicalization**</span><span class="sxs-lookup"><span data-stu-id="01e1a-122">**WsEndWriterCanonicalization**</span></span>](/windows/desktop/api/WebServices/nf-webservices-wsendwritercanonicalization)
-   [<span data-ttu-id="01e1a-123">**WsStartReaderCanonicalization**</span><span class="sxs-lookup"><span data-stu-id="01e1a-123">**WsStartReaderCanonicalization**</span></span>](/windows/desktop/api/WebServices/nf-webservices-wsstartreadercanonicalization)
-   [<span data-ttu-id="01e1a-124">**WsStartWriterCanonicalization**</span><span class="sxs-lookup"><span data-stu-id="01e1a-124">**WsStartWriterCanonicalization**</span></span>](/windows/desktop/api/WebServices/nf-webservices-wsstartwritercanonicalization)

<span data-ttu-id="01e1a-125">Les structures suivantes sont utilisées avec la canonisation :</span><span class="sxs-lookup"><span data-stu-id="01e1a-125">The following structures are used with canonicalization:</span></span>

-   [<span data-ttu-id="01e1a-126">**\_ \_ \_ préfixes inclusives de canonisation WS XML \_**</span><span class="sxs-lookup"><span data-stu-id="01e1a-126">**WS\_XML\_CANONICALIZATION\_INCLUSIVE\_PREFIXES**</span></span>](/windows/desktop/api/WebServices/ns-webservices-ws_xml_canonicalization_inclusive_prefixes)
-   [<span data-ttu-id="01e1a-127">**\_propriété de \_ canonisation WS \_ XML**</span><span class="sxs-lookup"><span data-stu-id="01e1a-127">**WS\_XML\_CANONICALIZATION\_PROPERTY**</span></span>](/windows/desktop/api/WebServices/ns-webservices-ws_xml_canonicalization_property)

 

 




