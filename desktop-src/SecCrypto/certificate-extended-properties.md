---
description: Les données contenues dans un certificat, une liste de révocation de certificats (CRL) ou un contexte de liste de certificats de confiance (CTL), y compris les extensions, sont en lecture seule et ne peuvent pas être modifiées.
ms.assetid: a9958c59-dc89-4d59-8ad3-6651ea4a1e56
title: Propriétés étendues du certificat
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f29853736433cb143a201ca352fceff0141cc96f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104114935"
---
# <a name="certificate-extended-properties"></a><span data-ttu-id="a850b-103">Propriétés étendues du certificat</span><span class="sxs-lookup"><span data-stu-id="a850b-103">Certificate Extended Properties</span></span>

<span data-ttu-id="a850b-104">Les données contenues dans un [*certificat*](../secgloss/c-gly.md), une [*liste de révocation de certificats*](../secgloss/c-gly.md) (CRL) ou un [*contexte*](../secgloss/c-gly.md)de liste de [*certificats de confiance*](../secgloss/c-gly.md) (CTL), y compris les extensions, sont en lecture seule et ne peuvent pas être modifiées.</span><span class="sxs-lookup"><span data-stu-id="a850b-104">The data in a [*certificate*](../secgloss/c-gly.md), [*certificate revocation list*](../secgloss/c-gly.md) (CRL), or [*certificate trust list*](../secgloss/c-gly.md) (CTL) [*context*](../secgloss/c-gly.md), including any extensions, is read-only and cannot be changed.</span></span> <span data-ttu-id="a850b-105">Toutefois, sur les plateformes Microsoft, les certificats CryptoAPI ont également des propriétés étendues dynamiques qui peuvent être ajoutées et modifiées.</span><span class="sxs-lookup"><span data-stu-id="a850b-105">However, on Microsoft platforms, CryptoAPI certificates also have dynamic extended properties that can be added and changed.</span></span>

> [!Note]  
> <span data-ttu-id="a850b-106">Les propriétés étendues sont associées à un certificat et ne font pas partie d’un certificat émis par une [*autorité de certification*](../secgloss/c-gly.md) (ca).</span><span class="sxs-lookup"><span data-stu-id="a850b-106">Extended properties are associated with a certificate and are not part of a certificate as issued by a [*certification authority*](../secgloss/c-gly.md) (CA).</span></span> <span data-ttu-id="a850b-107">Les propriétés étendues ne sont pas disponibles sur un certificat lorsqu’il est utilisé sur une plateforme non-Microsoft.</span><span class="sxs-lookup"><span data-stu-id="a850b-107">Extended properties are not available on a certificate when it is used on a non-Microsoft platform.</span></span>

 

<span data-ttu-id="a850b-108">Ces propriétés incluent des données qui :</span><span class="sxs-lookup"><span data-stu-id="a850b-108">These properties include data that:</span></span>

-   <span data-ttu-id="a850b-109">Se rapporte à la clé privée à utiliser avec le certificat.</span><span class="sxs-lookup"><span data-stu-id="a850b-109">Pertains to the private key to be used with the certificate.</span></span>
-   <span data-ttu-id="a850b-110">Indique le type de hachage à effectuer sur le certificat.</span><span class="sxs-lookup"><span data-stu-id="a850b-110">Indicates the type of hashes to be performed on the certificate.</span></span>
-   <span data-ttu-id="a850b-111">Fournit des informations définies par l’utilisateur associées au certificat.</span><span class="sxs-lookup"><span data-stu-id="a850b-111">Provides user-defined information associated with the certificate.</span></span>

<span data-ttu-id="a850b-112">Sur les plateformes Microsoft, les valeurs de ces propriétés sont jointes et déplacées avec le certificat.</span><span class="sxs-lookup"><span data-stu-id="a850b-112">On Microsoft platforms, values for these properties are attached to and move with the certificate.</span></span> <span data-ttu-id="a850b-113">Les propriétés prédéfinies actuellement identifiées par des ID de propriété incluent les propriétés suivantes :</span><span class="sxs-lookup"><span data-stu-id="a850b-113">Currently predefined properties identified with property IDs include the following properties:</span></span>

-   <span data-ttu-id="a850b-114">Ces propriétés lient un certificat à un CSP particulier et, dans ce CSP, à une clé privée particulière :</span><span class="sxs-lookup"><span data-stu-id="a850b-114">These properties tie a certificate to a particular CSP and, within that CSP, to a particular private key:</span></span>
    -   <span data-ttu-id="a850b-115">\_ \_ \_ ID prop du handle \_ de clé de certificat \_</span><span class="sxs-lookup"><span data-stu-id="a850b-115">CERT\_KEY\_PROV\_HANDLE\_PROP\_ID</span></span>
    -   <span data-ttu-id="a850b-116">ID de la clé de certificat \_ \_ Prov \_ info \_ prop \_</span><span class="sxs-lookup"><span data-stu-id="a850b-116">CERT\_KEY\_PROV\_INFO\_PROP\_ID</span></span>
    -   <span data-ttu-id="a850b-117">\_ID de \_ prop du contexte de clé du certificat \_ \_</span><span class="sxs-lookup"><span data-stu-id="a850b-117">CERT\_KEY\_CONTEXT\_PROP\_ID</span></span>
-   <span data-ttu-id="a850b-118">Ces propriétés indiquent l’algorithme de hachage à utiliser lors de l’exécution d’une opération de hachage :</span><span class="sxs-lookup"><span data-stu-id="a850b-118">These properties indicate the hashing algorithm to be used when a hashing operation is performed:</span></span>
    -   <span data-ttu-id="a850b-119">\_ID de \_ la \_ prop hash SHA1 \_ du certificat</span><span class="sxs-lookup"><span data-stu-id="a850b-119">CERT\_SHA1\_HASH\_PROP\_ID</span></span>
    -   <span data-ttu-id="a850b-120">\_ID de \_ la \_ prop Hash MD5 \_ du certificat</span><span class="sxs-lookup"><span data-stu-id="a850b-120">CERT\_MD5\_HASH\_PROP\_ID</span></span>

<span data-ttu-id="a850b-121">Pour obtenir la liste complète des propriétés de certificat étendues actuellement définies et des descriptions de la signification et de l’utilisation de chaque propriété, consultez [**CertGetCertificateContextProperty**](/windows/desktop/api/Wincrypt/nf-wincrypt-certgetcertificatecontextproperty) et [**CertSetCertificateContextProperty**](/windows/desktop/api/Wincrypt/nf-wincrypt-certsetcertificatecontextproperty).</span><span class="sxs-lookup"><span data-stu-id="a850b-121">For complete lists of currently defined extended certificate properties and descriptions of the meaning and use of each property, see [**CertGetCertificateContextProperty**](/windows/desktop/api/Wincrypt/nf-wincrypt-certgetcertificatecontextproperty) and [**CertSetCertificateContextProperty**](/windows/desktop/api/Wincrypt/nf-wincrypt-certsetcertificatecontextproperty).</span></span>

## <a name="related-topics"></a><span data-ttu-id="a850b-122">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="a850b-122">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="a850b-123">**CertGetCRLContextProperty**</span><span class="sxs-lookup"><span data-stu-id="a850b-123">**CertGetCRLContextProperty**</span></span>](/windows/desktop/api/Wincrypt/nf-wincrypt-certgetcrlcontextproperty)
</dt> <dt>

[<span data-ttu-id="a850b-124">**CertGetCTLContextProperty**</span><span class="sxs-lookup"><span data-stu-id="a850b-124">**CertGetCTLContextProperty**</span></span>](/windows/desktop/api/Wincrypt/nf-wincrypt-certgetctlcontextproperty)
</dt> <dt>

[<span data-ttu-id="a850b-125">**CertSetCRLContextProperty**</span><span class="sxs-lookup"><span data-stu-id="a850b-125">**CertSetCRLContextProperty**</span></span>](/windows/desktop/api/Wincrypt/nf-wincrypt-certsetcrlcontextproperty)
</dt> <dt>

[<span data-ttu-id="a850b-126">**CertSetCTLContextProperty**</span><span class="sxs-lookup"><span data-stu-id="a850b-126">**CertSetCTLContextProperty**</span></span>](/windows/desktop/api/Wincrypt/nf-wincrypt-certsetctlcontextproperty)
</dt> </dl>

 

 
