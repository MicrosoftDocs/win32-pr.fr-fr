---
description: CryptXML prend en charge en mode natif les URI listés ci-dessous.
ms.assetid: 012bad01-228a-4bb0-b883-0c2c7abd9271
title: Algorithmes de chiffrement de signature numérique XML
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 896348375d1d1a51288980aad3793dfffc69eb18
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106513418"
---
# <a name="xml-digital-signature-cryptographic-algorithms"></a><span data-ttu-id="ff26c-103">Algorithmes de chiffrement de signature numérique XML</span><span class="sxs-lookup"><span data-stu-id="ff26c-103">XML Digital Signature Cryptographic Algorithms</span></span>

<span data-ttu-id="ff26c-104">CryptXML prend en charge en mode natif les URI listés ci-dessous.</span><span class="sxs-lookup"><span data-stu-id="ff26c-104">CryptXML natively supports the URIs listed below.</span></span> <span data-ttu-id="ff26c-105">Si la prise en charge est requise pour les algorithmes de chiffrement et les transformations qui ne font pas partie de la prise en charge native, vous pouvez utiliser l' [API de chiffrement :](../seccng/cng-portal.md) [extensions de chiffrement de signature numérique](xml-digital-signature-cryptographic-extensions.md) nouvelle génération et XML pour prendre en charge de nouveaux algorithmes.</span><span class="sxs-lookup"><span data-stu-id="ff26c-105">If support is required for cryptographic algorithms and transforms that are not part of the native support, you can use [Cryptography API: Next Generation](../seccng/cng-portal.md) and [XML Digital Signature Cryptographic Extensions](xml-digital-signature-cryptographic-extensions.md) to support new algorithms.</span></span>

## <a name="supported-uris"></a><span data-ttu-id="ff26c-106">URI pris en charge</span><span class="sxs-lookup"><span data-stu-id="ff26c-106">Supported URIs</span></span>

<span data-ttu-id="ff26c-107">Méthodes Digest</span><span class="sxs-lookup"><span data-stu-id="ff26c-107">Digest Methods</span></span>



| <span data-ttu-id="ff26c-108">Constante</span><span class="sxs-lookup"><span data-stu-id="ff26c-108">Constant</span></span>                                 | <span data-ttu-id="ff26c-109">Valeur URI</span><span class="sxs-lookup"><span data-stu-id="ff26c-109">URI value</span></span>                                                   |
|------------------------------------------|-------------------------------------------------------------|
| <span data-ttu-id="ff26c-110">wszURI \_ xmlns \_ DIGSIG \_ SHA1</span><span class="sxs-lookup"><span data-stu-id="ff26c-110">wszURI\_XMLNS\_DIGSIG\_SHA1</span></span><br/>   | <span data-ttu-id="ff26c-111">"https://www.w3.org/2000/09/xmldsig\#sha1"</span><span class="sxs-lookup"><span data-stu-id="ff26c-111">"https://www.w3.org/2000/09/xmldsig\#sha1"</span></span><br/>        |
| <span data-ttu-id="ff26c-112">wszURI \_ xmlns \_ DIGSIG \_ SHA256</span><span class="sxs-lookup"><span data-stu-id="ff26c-112">wszURI\_XMLNS\_DIGSIG\_SHA256</span></span><br/> | <span data-ttu-id="ff26c-113">"https://www.w3.org/2001/04/xmlenc\#sha256"</span><span class="sxs-lookup"><span data-stu-id="ff26c-113">"https://www.w3.org/2001/04/xmlenc\#sha256"</span></span><br/>       |
| <span data-ttu-id="ff26c-114">wszURI \_ xmlns \_ DIGSIG \_ SHA384</span><span class="sxs-lookup"><span data-stu-id="ff26c-114">wszURI\_XMLNS\_DIGSIG\_SHA384</span></span><br/> | <span data-ttu-id="ff26c-115">"https://www.w3.org/2001/04/xmldsig-more\#sha384"</span><span class="sxs-lookup"><span data-stu-id="ff26c-115">"https://www.w3.org/2001/04/xmldsig-more\#sha384"</span></span><br/> |
| <span data-ttu-id="ff26c-116">wszURI \_ xmlns \_ DIGSIG \_ SHA512</span><span class="sxs-lookup"><span data-stu-id="ff26c-116">wszURI\_XMLNS\_DIGSIG\_SHA512</span></span><br/> | <span data-ttu-id="ff26c-117">"https://www.w3.org/2001/04/xmlenc\#sha512"</span><span class="sxs-lookup"><span data-stu-id="ff26c-117">"https://www.w3.org/2001/04/xmlenc\#sha512"</span></span><br/>       |



 

<span data-ttu-id="ff26c-118">Méthodes de signature</span><span class="sxs-lookup"><span data-stu-id="ff26c-118">Signature Methods</span></span>



| <span data-ttu-id="ff26c-119">Constante</span><span class="sxs-lookup"><span data-stu-id="ff26c-119">Constant</span></span>                                        | <span data-ttu-id="ff26c-120">Valeur URI</span><span class="sxs-lookup"><span data-stu-id="ff26c-120">URI value</span></span>                                                         |
|-------------------------------------------------|-------------------------------------------------------------------|
| <span data-ttu-id="ff26c-121">wszURI \_ xmlns \_ DIGSIG- \_ RSA \_ SHA1</span><span class="sxs-lookup"><span data-stu-id="ff26c-121">wszURI\_XMLNS\_DIGSIG\_RSA\_SHA1</span></span><br/>     | <span data-ttu-id="ff26c-122">"https://www.w3.org/2000/09/xmldsig\#rsa-sha1"</span><span class="sxs-lookup"><span data-stu-id="ff26c-122">"https://www.w3.org/2000/09/xmldsig\#rsa-sha1"</span></span><br/>          |
| <span data-ttu-id="ff26c-123">wszURI \_ xmlns \_ DIGSIG \_ DSA \_ SHA1</span><span class="sxs-lookup"><span data-stu-id="ff26c-123">wszURI\_XMLNS\_DIGSIG\_DSA\_SHA1</span></span><br/>     | <span data-ttu-id="ff26c-124">"https://www.w3.org/2000/09/xmldsig\#dsa-sha1"</span><span class="sxs-lookup"><span data-stu-id="ff26c-124">"https://www.w3.org/2000/09/xmldsig\#dsa-sha1"</span></span><br/>          |
| <span data-ttu-id="ff26c-125">wszURI \_ xmlns \_ DIGSIG \_ RSA \_ SHA256</span><span class="sxs-lookup"><span data-stu-id="ff26c-125">wszURI\_XMLNS\_DIGSIG\_RSA\_SHA256</span></span><br/>   | <span data-ttu-id="ff26c-126">"https://www.w3.org/2001/04/xmldsig-more\#rsa-sha256"</span><span class="sxs-lookup"><span data-stu-id="ff26c-126">"https://www.w3.org/2001/04/xmldsig-more\#rsa-sha256"</span></span><br/>   |
| <span data-ttu-id="ff26c-127">wszURI \_ xmlns \_ DIGSIG \_ RSA \_ SHA384</span><span class="sxs-lookup"><span data-stu-id="ff26c-127">wszURI\_XMLNS\_DIGSIG\_RSA\_SHA384</span></span><br/>   | <span data-ttu-id="ff26c-128">"https://www.w3.org/2001/04/xmldsig-more\#rsa-sha384"</span><span class="sxs-lookup"><span data-stu-id="ff26c-128">"https://www.w3.org/2001/04/xmldsig-more\#rsa-sha384"</span></span><br/>   |
| <span data-ttu-id="ff26c-129">wszURI \_ xmlns \_ DIGSIG \_ RSA \_ SHA512</span><span class="sxs-lookup"><span data-stu-id="ff26c-129">wszURI\_XMLNS\_DIGSIG\_RSA\_SHA512</span></span><br/>   | <span data-ttu-id="ff26c-130">"https://www.w3.org/2001/04/xmldsig-more\#rsa-sha512"</span><span class="sxs-lookup"><span data-stu-id="ff26c-130">"https://www.w3.org/2001/04/xmldsig-more\#rsa-sha512"</span></span><br/>   |
| <span data-ttu-id="ff26c-131">wszURI \_ xmlns \_ DIGSIG \_ ECDSA \_ SHA1</span><span class="sxs-lookup"><span data-stu-id="ff26c-131">wszURI\_XMLNS\_DIGSIG\_ECDSA\_SHA1</span></span><br/>   | <span data-ttu-id="ff26c-132">"https://www.w3.org/2001/04/xmldsig-more\#ecdsa-sha1"</span><span class="sxs-lookup"><span data-stu-id="ff26c-132">"https://www.w3.org/2001/04/xmldsig-more\#ecdsa-sha1"</span></span><br/>   |
| <span data-ttu-id="ff26c-133">wszURI \_ xmlns \_ DIGSIG \_ ECDSA \_ SHA256</span><span class="sxs-lookup"><span data-stu-id="ff26c-133">wszURI\_XMLNS\_DIGSIG\_ECDSA\_SHA256</span></span><br/> | <span data-ttu-id="ff26c-134">"https://www.w3.org/2001/04/xmldsig-more\#ecdsa-sha256"</span><span class="sxs-lookup"><span data-stu-id="ff26c-134">"https://www.w3.org/2001/04/xmldsig-more\#ecdsa-sha256"</span></span><br/> |
| <span data-ttu-id="ff26c-135">wszURI \_ xmlns \_ DIGSIG \_ ECDSA \_ SHA384</span><span class="sxs-lookup"><span data-stu-id="ff26c-135">wszURI\_XMLNS\_DIGSIG\_ECDSA\_SHA384</span></span><br/> | <span data-ttu-id="ff26c-136">"https://www.w3.org/2001/04/xmldsig-more\#ecdsa-sha384"</span><span class="sxs-lookup"><span data-stu-id="ff26c-136">"https://www.w3.org/2001/04/xmldsig-more\#ecdsa-sha384"</span></span><br/> |
| <span data-ttu-id="ff26c-137">wszURI \_ xmlns \_ DIGSIG \_ ECDSA \_ SHA512</span><span class="sxs-lookup"><span data-stu-id="ff26c-137">wszURI\_XMLNS\_DIGSIG\_ECDSA\_SHA512</span></span><br/> | <span data-ttu-id="ff26c-138">"https://www.w3.org/2001/04/xmldsig-more\#ecdsa-sha512"</span><span class="sxs-lookup"><span data-stu-id="ff26c-138">"https://www.w3.org/2001/04/xmldsig-more\#ecdsa-sha512"</span></span><br/> |
| <span data-ttu-id="ff26c-139">wszURI \_ xmlns \_ DIGSIG \_ HMAC \_ SHA1</span><span class="sxs-lookup"><span data-stu-id="ff26c-139">wszURI\_XMLNS\_DIGSIG\_HMAC\_SHA1</span></span><br/>    | <span data-ttu-id="ff26c-140">"https://www.w3.org/2000/09/xmldsig\#hmac-sha1"</span><span class="sxs-lookup"><span data-stu-id="ff26c-140">"https://www.w3.org/2000/09/xmldsig\#hmac-sha1"</span></span><br/>         |
| <span data-ttu-id="ff26c-141">wszURI \_ xmlns \_ DIGSIG \_ HMAC \_ SHA256</span><span class="sxs-lookup"><span data-stu-id="ff26c-141">wszURI\_XMLNS\_DIGSIG\_HMAC\_SHA256</span></span><br/>  | <span data-ttu-id="ff26c-142">"https://www.w3.org/2001/04/xmldsig-more\#hmac-sha256"</span><span class="sxs-lookup"><span data-stu-id="ff26c-142">"https://www.w3.org/2001/04/xmldsig-more\#hmac-sha256"</span></span><br/>  |
| <span data-ttu-id="ff26c-143">wszURI \_ xmlns \_ DIGSIG \_ HMAC \_ SHA384</span><span class="sxs-lookup"><span data-stu-id="ff26c-143">wszURI\_XMLNS\_DIGSIG\_HMAC\_SHA384</span></span><br/>  | <span data-ttu-id="ff26c-144">"https://www.w3.org/2001/04/xmldsig-more\#hmac-sha384"</span><span class="sxs-lookup"><span data-stu-id="ff26c-144">"https://www.w3.org/2001/04/xmldsig-more\#hmac-sha384"</span></span><br/>  |
| <span data-ttu-id="ff26c-145">wszURI \_ xmlns \_ DIGSIG \_ HMAC \_ SHA512</span><span class="sxs-lookup"><span data-stu-id="ff26c-145">wszURI\_XMLNS\_DIGSIG\_HMAC\_SHA512</span></span><br/>  | <span data-ttu-id="ff26c-146">"https://www.w3.org/2001/04/xmldsig-more\#hmac-sha512"</span><span class="sxs-lookup"><span data-stu-id="ff26c-146">"https://www.w3.org/2001/04/xmldsig-more\#hmac-sha512"</span></span><br/>  |



 

 

 
