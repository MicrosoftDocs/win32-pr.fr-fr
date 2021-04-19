---
description: CryptXML fournit un ensemble d’API de bas niveau qui permet aux applications de créer et de vérifier des signatures enveloppes, enveloppantes et détachées. Vous pouvez utiliser CryptXML pour créer et vérifier le contenu stocké dans les éléments d’objet de signature, y compris les manifestes.
ms.assetid: 962dffdb-caa6-4aa7-b5c6-3a9de8cfaf6c
title: Fonctionnalité de l’API de signature numérique XML
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 67ae330fdd8ba75ece885e8ed0b7e2c91e60fc39
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106534292"
---
# <a name="xml-digital-signature-api-functionality"></a><span data-ttu-id="17ecd-104">Fonctionnalité de l’API de signature numérique XML</span><span class="sxs-lookup"><span data-stu-id="17ecd-104">XML Digital Signature API Functionality</span></span>

<span data-ttu-id="17ecd-105">CryptXML fournit un ensemble d’API de bas niveau qui permet aux applications de créer et de vérifier des signatures enveloppes, enveloppantes et détachées.</span><span class="sxs-lookup"><span data-stu-id="17ecd-105">CryptXML provides a low level set of APIs that allow applications to create and verify enveloped, enveloping, and detached signatures.</span></span> <span data-ttu-id="17ecd-106">Vous pouvez utiliser CryptXML pour créer et vérifier le contenu stocké dans les éléments d’objet de signature, y compris les manifestes.</span><span class="sxs-lookup"><span data-stu-id="17ecd-106">You can use CryptXML to create and verify content stored in signature object elements, including manifests.</span></span> <span data-ttu-id="17ecd-107">Une clé publique/privée, une clé partagée ou un certificat [*X. 509*](../secgloss/x-gly.md) ou une chaîne de certificats peuvent être utilisés pour signer et vérifier la [*signature numérique*](../secgloss/d-gly.md)XML.</span><span class="sxs-lookup"><span data-stu-id="17ecd-107">A public/private, shared key, or an [*X.509*](../secgloss/x-gly.md) certificate or certificate chain can be used to sign and verify the XML [*digital signature*](../secgloss/d-gly.md).</span></span>

<span data-ttu-id="17ecd-108">Les applications qui utilisent CryptXML pour vérifier les références externes (références qui ciblent un document ou un fichier externe en dehors du contexte du document) doivent résoudre les URI externes et récupérer les données à déchiffrer.</span><span class="sxs-lookup"><span data-stu-id="17ecd-108">Applications that use CryptXML to verify external references (references that target an external document or file outside of the document context) must resolve the external URIs and retrieve the data to be digested.</span></span>

<span data-ttu-id="17ecd-109">Pour plus d’informations sur les algorithmes de chiffrement pris en charge par CryptXML, consultez [algorithmes de chiffrement de signature numérique XML](xml-digital-signature-cryptographic-algorithms.md).</span><span class="sxs-lookup"><span data-stu-id="17ecd-109">For information about the cryptographic algorithms supported by CryptXML, see [XML Digital Signature Cryptographic Algorithms](xml-digital-signature-cryptographic-algorithms.md).</span></span>

<span data-ttu-id="17ecd-110">CryptXML fournit la prise en charge des algorithmes de canonisation avec les identificateurs suivants.</span><span class="sxs-lookup"><span data-stu-id="17ecd-110">CryptXML provides support for the canonicalization algorithms with the following identifiers.</span></span>



| <span data-ttu-id="17ecd-111">Constante</span><span class="sxs-lookup"><span data-stu-id="17ecd-111">Constant</span></span>                                              | <span data-ttu-id="17ecd-112">Valeur URI</span><span class="sxs-lookup"><span data-stu-id="17ecd-112">URI value</span></span>                                                                  |
|-------------------------------------------------------|----------------------------------------------------------------------------|
| <span data-ttu-id="17ecd-113">wszURI \_ canonicalisation, \_ C14N</span><span class="sxs-lookup"><span data-stu-id="17ecd-113">wszURI\_CANONICALIZATION\_C14N</span></span><br/>             | <span data-ttu-id="17ecd-114">"https://www.w3.org/TR/2001/REC-xml-c14n-20010315"</span><span class="sxs-lookup"><span data-stu-id="17ecd-114">"https://www.w3.org/TR/2001/REC-xml-c14n-20010315"</span></span><br/>               |
| <span data-ttu-id="17ecd-115">wszURI \_ Canonicalization \_ C14NC</span><span class="sxs-lookup"><span data-stu-id="17ecd-115">wszURI\_CANONICALIZATION\_C14NC</span></span><br/>            | <span data-ttu-id="17ecd-116">"https://www.w3.org/TR/2001/REC-xml-c14n-20010315\#WithComments"</span><span class="sxs-lookup"><span data-stu-id="17ecd-116">"https://www.w3.org/TR/2001/REC-xml-c14n-20010315\#WithComments"</span></span><br/> |
| <span data-ttu-id="17ecd-117">wszURI \_ canonisation \_ EXSLUSIVE \_ C14N</span><span class="sxs-lookup"><span data-stu-id="17ecd-117">wszURI\_CANONICALIZATION\_EXSLUSIVE\_C14N</span></span><br/>  | <span data-ttu-id="17ecd-118">"https://www.w3.org/2001/10/xml-exc-c14n\#"</span><span class="sxs-lookup"><span data-stu-id="17ecd-118">"https://www.w3.org/2001/10/xml-exc-c14n\#"</span></span><br/>                      |
| <span data-ttu-id="17ecd-119">wszURI \_ Canonicalization \_ EXSLUSIVE \_ C14NC</span><span class="sxs-lookup"><span data-stu-id="17ecd-119">wszURI\_CANONICALIZATION\_EXSLUSIVE\_C14NC</span></span><br/> | <span data-ttu-id="17ecd-120">"https://www.w3.org/2001/10/xml-exc-c14n\#WithComments"</span><span class="sxs-lookup"><span data-stu-id="17ecd-120">"https://www.w3.org/2001/10/xml-exc-c14n\#WithComments"</span></span><br/>          |



 

<span data-ttu-id="17ecd-121">CryptXML fournit la prise en charge de la transformation de signature enveloppée.</span><span class="sxs-lookup"><span data-stu-id="17ecd-121">CryptXML provides support for the enveloped signature transform.</span></span>



| <span data-ttu-id="17ecd-122">Constante</span><span class="sxs-lookup"><span data-stu-id="17ecd-122">Constant</span></span>                                       | <span data-ttu-id="17ecd-123">Valeur URI</span><span class="sxs-lookup"><span data-stu-id="17ecd-123">URI value</span></span>                                                           |
|------------------------------------------------|---------------------------------------------------------------------|
| <span data-ttu-id="17ecd-124">wszURI \_ xmlns \_ Transform \_ envelopped</span><span class="sxs-lookup"><span data-stu-id="17ecd-124">wszURI\_XMLNS\_TRANSFORM\_ENVELOPED</span></span><br/> | <span data-ttu-id="17ecd-125">"https://www.w3.org/2000/09/xmldsig\#enveloped-signature"</span><span class="sxs-lookup"><span data-stu-id="17ecd-125">"https://www.w3.org/2000/09/xmldsig\#enveloped-signature"</span></span><br/> |



 

<span data-ttu-id="17ecd-126">Par défaut, CryptXML ne prend pas en charge les transformations XPath ou XSLT.</span><span class="sxs-lookup"><span data-stu-id="17ecd-126">By default, CryptXML does not support XPath or XSLT transforms.</span></span> <span data-ttu-id="17ecd-127">Si nécessaire, les applications peuvent implémenter ces transformations par-dessus CryptXML.</span><span class="sxs-lookup"><span data-stu-id="17ecd-127">If required, applications can implement these transforms on top of CryptXML.</span></span>

 

 
