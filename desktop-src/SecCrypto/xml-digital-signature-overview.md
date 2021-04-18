---
description: XML est une norme du secteur pour la description des données structurées. Une signature numérique XML est une représentation XML d’une signature numérique qui permet de vérifier l’origine et l’intégrité du document XML et des données référencées en externe.
ms.assetid: 02ca8d9b-be08-4b15-895f-9c8c4b0ed536
title: Vue d’ensemble de la signature numérique XML
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b41a1b748305ab26b686e126cd201ad9e7f34d51
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106519138"
---
# <a name="xml-digital-signature-overview"></a><span data-ttu-id="9d890-104">Vue d’ensemble de la signature numérique XML</span><span class="sxs-lookup"><span data-stu-id="9d890-104">XML Digital Signature Overview</span></span>

<span data-ttu-id="9d890-105">XML est une norme du secteur pour la description des données structurées.</span><span class="sxs-lookup"><span data-stu-id="9d890-105">XML is an industry standard for describing structured data.</span></span> <span data-ttu-id="9d890-106">Une signature numérique XML est une représentation XML d’une [*signature numérique*](../secgloss/d-gly.md) qui permet de vérifier l’origine et l’intégrité du document XML et des données référencées en externe.</span><span class="sxs-lookup"><span data-stu-id="9d890-106">An XML Digital Signature is an XML representation of a [*digital signature*](../secgloss/d-gly.md) that provides the ability to verify the origin and integrity of XML document and externally referenced data.</span></span> <span data-ttu-id="9d890-107">Les signatures numériques XML peuvent être utilisées pour signer des données arbitraires, notamment un fragment ou un document XML, une page HTML, du texte brut ou des données codées en binaire, telles qu’un fichier JPEG.</span><span class="sxs-lookup"><span data-stu-id="9d890-107">XML digital signatures can be used to sign arbitrary data, including an XML document or fragment, an HTML page, plain text, or binary-encoded data such as a JPEG file.</span></span>

<span data-ttu-id="9d890-108">Le format de signature numérique XML pris en charge par l’API de signature numérique CryptXML est spécifié par la recommandation du W3C sur la syntaxe et le traitement des signatures XML (deuxième édition).</span><span class="sxs-lookup"><span data-stu-id="9d890-108">The XML digital signature format supported by the CryptXML digital signature API is specified by the XML Signature Syntax and Processing (Second Edition) W3C recommendation.</span></span>

<span data-ttu-id="9d890-109">La signature numérique CryptXML implémente la prise en charge des types de signature requis, des algorithmes de chiffrement, des algorithmes de canonisation et de la transformation enveloppée spécifiée.</span><span class="sxs-lookup"><span data-stu-id="9d890-109">The CryptXML digital signature implements support for the required signature types, cryptographic algorithms, canonicalization algorithms, and the specified enveloped transform.</span></span>

<span data-ttu-id="9d890-110">Les développeurs peuvent étendre l’ensemble par défaut des algorithmes de chiffrement pris en charge par CryptXML en créant des dll d’extension de chiffrement.</span><span class="sxs-lookup"><span data-stu-id="9d890-110">Developers can extend the default set of cryptographic algorithms supported by CryptXML by creating cryptographic extension DLLs.</span></span> <span data-ttu-id="9d890-111">Les développeurs peuvent également créer leurs propres transformations personnalisées et algorithmes de canonisation en plus de l’API CryptXML.</span><span class="sxs-lookup"><span data-stu-id="9d890-111">Developers can also create their own custom transforms and canonicalization algorithms on top of CryptXML API.</span></span> <span data-ttu-id="9d890-112">Les développeurs peuvent utiliser les API CryptXML avec les API de certificat Windows.</span><span class="sxs-lookup"><span data-stu-id="9d890-112">Developers can use the CryptXML APIs with the Windows certificate APIs.</span></span>

 

 
